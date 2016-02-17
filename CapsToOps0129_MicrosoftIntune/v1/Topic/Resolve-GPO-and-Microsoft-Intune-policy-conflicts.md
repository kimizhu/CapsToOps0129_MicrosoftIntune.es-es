---
title: Resolver conflictos de directivas de Microsoft Intune y GPO
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e76af5b7-e933-442c-a9d3-3b42c5f5868b
---
# Resolver conflictos de directivas de Microsoft Intune y GPO
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] utiliza directivas que le ayudan a administrar la configuración de los equipos que administra. Por ejemplo, podría utilizar una directiva para controlar la configuración del Firewall de Windows en los equipos. Muchas de las opciones de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] son similares a las opciones que se pueden configurar con la directiva de grupo de Windows. Sin embargo, es posible que, en ocasiones, los dos métodos entren en conflicto.

Cuando se producen conflictos, la directiva de grupo de nivel de dominio tiene prioridad sobre la directiva de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], a menos que el equipo no pueda iniciar sesión en el dominio. En este caso, la directiva de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] se aplica al equipo cliente.

## <a name="BKMK_plan"></a>Qué hacer si se utiliza la directiva de grupo
Compruebe que las directivas que aplica no se administran mediante la directiva de grupo. Para evitar conflictos, podría emplear uno o más de los siguientes métodos:

-   Mueva los equipos a una unidad organizativa (OU) de Active Directory que no tenga aplicada la configuración de la directiva de grupo antes de instalar el cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. También es posible bloquear la herencia de directivas de grupo en las OU que contienen equipos inscritos en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a los que no desea aplicar la configuración de la directiva de grupo.

-   Utilice un filtro WMI o un filtro de seguridad para restringir los objetos de directiva de grupo únicamente a los equipos que no se administran mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Para obtener información y ejemplos acerca de cómo hacerlo, consulte [Filtrado de los objetos de directiva de grupo existentes para evitar conflictos con la directiva de Microsoft Intune](../Topic/Resolve-GPO-and-Microsoft-Intune-policy-conflicts.md#BKMK_Filter) a continuación.

-   Deshabilite o quite los objetos de directiva de grupo que entran en conflicto con las directivas de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

Para obtener más información acerca de Active Directory y la directiva de grupo de Windows, consulte la documentación de Windows Server.

### <a name="BKMK_Filter"></a>Filtrado de los objetos de directiva de grupo existentes para evitar conflictos con la directiva de Microsoft Intune
Si identificó objetos de directiva de grupo (GPO) cuya configuración entra en conflicto con las directivas de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], puede utilizar cualquiera de los métodos de filtrado siguientes para restringir esos GPO únicamente a los equipos que no se administran mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

#### Utilice filtros WMI.
Los filtros WMI aplican selectivamente los GPO a los equipos que cumplen las condiciones de una consulta. Para aplicar un filtro WMI, implemente una instancia de clase WMI en todos los equipos de la empresa antes de inscribir ningún equipo en el servicio [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

##### <a name="BKMK_filters"></a>Para aplicar filtros WMI a un GPO

1.  Cree un archivo de objeto de administración. Para ello, copie y pegue lo siguiente en un archivo de texto y, a continuación, guarde este archivo en una ubicación adecuada como **WIT.mof**. Este archivo contiene la instancia de clase WMI que deberá implementar en los equipos que desea inscribir en el servicio de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    ```
    //Beginning of MOF file. #pragma classflags("forceupdate") #pragma namespace ("\\\\.\\Root") instance of __Namespace { Name = "WindowsIntune"; }; #pragma namespace ("\\\\.\\Root\\WindowsIntune") [ Description("This class defines Microsoft Intune common properties") ] class WindowsIntune_ManagedNode { [ read, Description("This defines whether Microsoft Intune Policy is enabled"): DisableOverride ToSubClass ] boolean WindowsIntunePolicyEnabled; [ read, key, Description("This property defines the version." "Example: 1.0"): ToSubClass ] string Version; }; instance of WindowsIntune_ManagedNode { Version = "1.0"; WindowsIntunePolicyEnabled = 1; };
    ```

2.  Para implementar el archivo puede utilizar tanto una secuencia de comandos de inicio, como la directiva de grupo. A continuación se indica el comando de implementación de la secuencia de comandos de inicio. La instancia de clase WMI debe ser implementada antes de inscribir cualquier equipo cliente en el servicio de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    **C:/Windows/System32/Wbem/MOFCOMP &lt;path to MOF file&gt;\wit.mof**

3.  Ejecute cualquiera de los siguientes comandos para crear los filtros WMI, en función de si el GPO que desea filtrar se aplica a equipos administrados mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] o a equipos que no se administran mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    -   Para GPO que se aplican a equipos no administrados mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], utilice lo siguiente:

        ```
        Namespace:root\WindowsIntune Query:  SELECT WindowsIntunePolicyEnabled FROM WindowsIntune_ManagedNode WHERE WindowsIntunePolicyEnabled=0
        ```

    -   Para GPO que corresponden a equipos administrados mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], utilice lo siguiente:

        ```
        Namespace:root\WindowsIntune Query:  SELECT WindowsIntunePolicyEnabled FROM WindowsIntune_ManagedNode WHERE WindowsIntunePolicyEnabled=1
        ```

4.  Edite el GPO en la Consola de administración de directivas de grupo para aplicar el filtro WMI que creó en el paso anterior.

    -   Para los GPO que solo deberían aplicarse a equipos que desea administrar mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], aplique el filtro **WindowsIntunePolicyEnabled=1**.

    -   Para los GPO que solo deberían aplicarse a equipos que no desea administrar mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], aplique el filtro **WindowsIntunePolicyEnabled=0**.

Para obtener más información acerca de cómo aplicar filtros WMI en la directiva de grupo, consulte la entrada de blog [Security Filtering, WMI Filtering, and Item-level Targeting in Group Policy Preferences (Filtrado de seguridad, filtrado WMI y destinatarios en el ámbito del elemento en las preferencias de directiva de grupo)](http://go.microsoft.com/fwlink/?LinkId=177883).

#### Utilizar filtros de grupo de seguridad
La directiva de grupo le permite aplicar los GPO únicamente a los grupos de seguridad especificados en el área **Filtrado de seguridad** de la Consola de administración de directivas de grupo para un GPO seleccionado. De forma predeterminada, los GPO se aplican a **Usuarios autenticados**.

-   En el complemento **Usuarios y equipos de Active Directory**, cree un nuevo grupo de seguridad que contenga los equipos y cuentas de usuario que no desea administrar mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Por ejemplo, el nombre del grupo podría ser **Fuera de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**.

-   En la Consola de administración de directivas de grupo, en la ficha **Delegación** del GPO seleccionado, haga clic con el botón secundario en el nuevo grupo de seguridad para delegar los permisos **Lectura** y **Aplicar directiva de grupos** apropiados en los usuarios y equipos del grupo de seguridad. (Los permisos **Aplicar directiva de grupo** están disponibles en el cuadro de diálogo **Avanzadas**).

-   A continuación, aplique el nuevo filtro de grupo de seguridad a un GPO seleccionado y quite el filtro predeterminado **Usuarios autenticados**.

El nuevo grupo de seguridad debe mantenerse inscrito en los cambios del servicio de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## Vea también
[Administrar equipos Windows con Microsoft Intune](../Topic/Manage-Windows-PCs-with-Microsoft-Intune.md)

