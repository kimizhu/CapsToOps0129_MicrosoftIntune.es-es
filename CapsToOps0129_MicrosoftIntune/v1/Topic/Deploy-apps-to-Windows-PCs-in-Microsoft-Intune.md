---
title: Implementar aplicaciones en equipos Windows en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4105b676-11f1-4cd2-88a4-b37d186cdbdb
---
# Implementar aplicaciones en equipos Windows en Microsoft Intune
Ahora que ya [conoce los conceptos básicos](https://technet.microsoft.com/library/dn646955.aspx) de la implementación de aplicaciones de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], en este tema aprenderá a configurar e implementar aplicaciones en los equipos Windows que administre. Por lo general, esto implica tres pasos:

-   [Configurar la aplicación](#BKMK_Conf)

-   [Implementar la aplicación](#BKMK_Depl)

-   [Supervisar la aplicación](#BKMK_Monitor)

Para obtener información sobre cómo actualizar y retirar aplicaciones, consulte [Actualizar aplicaciones con Microsoft Intune](../Topic/Update-apps-using-Microsoft-Intune.md).

> [!IMPORTANT]
> La información de este tema le ayudará a implementar aplicaciones en [equipos Windows administrados mediante software cliente](https://technet.microsoft.com/library/dn646959.aspx). Si desea implementar aplicaciones en [equipos Windows inscritos](https://technet.microsoft.com/library/mt346003.aspx) y otros dispositivos móviles, consulte [Implementar aplicaciones en dispositivos móviles en Microsoft Intune](../Topic/Deploy-apps-to-mobile-devices-in-Microsoft-Intune---deleted.md).

## <a name="BKMK_Conf"></a>Configurar la aplicación
En este procedimiento, usará el Editor de software de Intune para configurar las propiedades de la aplicación y cargarla en su espacio de almacenamiento en la nube.

#### Para configurar una aplicación

1.  En la [consola de administrador de Microsoft Intune](https://manage.microsoft.com), haga clic en **Aplicaciones** &gt; **Agregar aplicaciones** para iniciar el Editor de software de Intune.

    > [!TIP]
    > Deberá escribir su nombre de usuario y contraseña de Intune para que se inicie el editor.

2.  En la página **Instalación de software** del editor de software, configure lo siguiente:

    **Seleccione cómo debe ponerse a disposición de los dispositivos este software**: seleccione **Instalador de software** y especifique:

    |Configuración|Detalles|
    |-----------------|------------|
    |**Seleccionar el tipo de archivo instalador de software**|Indica el tipo de software que desea implementar. En el caso de un equipo Windows, elija **Windows Installer**.|
    |**Especifique la ubicación de los archivos de instalación del software**|Escriba la ubicación de los archivos de instalación o haga clic en **Examinar** para seleccionar la ubicación en una lista.|
    |**Incluir archivos y subcarpetas adicionales de la misma carpeta**|Cierto software que usa Windows Installer necesita los archivos auxiliares que normalmente se encuentran en la misma carpeta que los archivos de instalación. Seleccione esta opción si también desea implementar estos archivos auxiliares.|
    Este tipo de instalación usa parte del espacio de almacenamiento en la nube.

3.  En la página **Descripción del software**, configure las siguientes opciones:

    > [!TIP]
    > En función del archivo instalador que use, algunos de estos valores podrían especificarse automáticamente o no aparecer.

    |Configuración|Detalles|
    |-----------------|------------|
    |**Publicador**|Escriba el nombre del publicador de la aplicación.|
    |**Nombre**|Escriba el nombre de la aplicación tal como se mostrará en el portal de empresa. **Tip:** Asegúrese de que todos los nombres de aplicación que usa son únicos. Si el mismo nombre de aplicación existe dos veces, solo se mostrará a los usuarios una de las aplicaciones en el portal de empresa.|
    |**Descripción**|Escriba una descripción de la aplicación. Se mostrará a los usuarios en el portal de empresa.|
    |**Dirección URL para información del software**|(opcional) Escriba una dirección URL de un sitio web que contenga información sobre esta aplicación. La dirección URL se mostrará a los usuarios en el portal de empresa.|
    |**Dirección URL de privacidad**|(opcional) Escriba una dirección URL de un sitio web que contenga información de privacidad sobre esta aplicación. La dirección URL se mostrará a los usuarios en el portal de empresa.|
    |**Categoría**|(opcional) Seleccione una de las categorías de aplicaciones integradas. Así les resultará más fácil a los usuarios encontrar la aplicación cuando exploren el portal de empresa.|
    |**Icono**|(opcional) Cargue un icono que se asociará con la aplicación. Será el icono que se muestre con la aplicación cuando los usuarios examinen el portal de empresa.|

4.  En la página **Requisitos**, seleccione los requisitos que deben cumplirse para que la aplicación pueda empezar a instalarse en un dispositivo:

    -   **Arquitectura**: seleccione si esta aplicación puede instalarse en un sistema operativo de 32 bits, 64 bits o en ambos.

    -   **Sistema operativo**: seleccione el sistema operativo mínimo en el que se puede instalar esta aplicación.

5.  Solo para el tipo de archivo **Windows Installer** (solo exe): en la página **Reglas de detección**, puede configurar reglas para detectar si la aplicación que está configurando ya está instalada en un equipo, o bien puede usar las reglas de detección predeterminadas para que las versiones de la aplicación instaladas anteriormente se sobrescriban de manera automática. Las reglas que puede configurar son las siguientes:

    -   **El archivo ya existe**: especifique la ruta de acceso del archivo que desea detectar. Puede buscar en **%ProgramFiles%** (busca en **Archivos de programa**\*&lt;ruta de acceso&gt;* y **Archivos de programa (x86)**\*&lt;ruta de acceso&gt;*) en el equipo o en **%SystemDrive%** (busca en la unidad raíz del equipo, normalmente C:)

        .

    -   **Existe un código de producto MSI**: haga clic en **Examinar** para elegir el archivo Windows Installer (msi) que desea detectar.

    -   **Existe la clave del Registro**: especifique una clave del Registro que comience con **HKEY_LOCAL_MACHINE\**. Se busca en las rutas de acceso del Registro de 32 bits y 64 bits. Si la clave especificada existe en ambas ubicaciones, se cumple la regla de detección.

    Si la aplicación cumple alguna de las reglas que configuró, no se instalará.

6.  Solo para el tipo de archivo **Windows Installer** (msi y exe): en la página **Argumentos de línea de comandos**, elija si desea proporcionar argumentos de línea de comandos opcionales para el instalador. Por ejemplo, algunos instaladores podrían admitir el argumento **/q** para realizar una instalación silenciosa sin intervención del usuario.

7.  Solo para el tipo de archivo **Windows Installer** (solo exe): en la página **Códigos de retorno**, puede agregar nuevos códigos de error que Intune interpretará cuando la aplicación se instale en un equipo Windows administrado.

    De forma predeterminada, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] usa códigos de retorno estándar del sector para informar de una instalación correcta o incorrecta de un paquete de aplicación:

    -   **0**: correcto

    -   **3010**: correcto con reinicio

    También puede agregar sus propios códigos de retorno a esta lista. Si especifica una lista de códigos de retorno y la instalación de la aplicación devuelve un código que no se encuentra en la lista, se interpreta como un error.

8.  En la página **Resumen**, revise la información que especificó. Cuando esté listo, haga clic en **Cargar**.

9. Haga clic en **Cerrar** para finalizar.

La aplicación se muestra en el nodo **Aplicaciones** del área de trabajo **Aplicaciones**.

## <a name="BKMK_Depl"></a>Implementar la aplicación
En este procedimiento, implementará la aplicación en los dispositivos o para los usuarios seleccionados.

#### Para implementar la aplicación

1.  En la [consola de administrador de Microsoft Intune](https://manage.microsoft.com), haga clic en **Aplicaciones** &gt; **Aplicaciones** para ver la lista de aplicaciones que administra.

2.  Seleccione la aplicación que desea implementar y haga clic en **Administrar la implementación**.

3.  En primer lugar, en el cuadro de diálogo *&lt;nombre de la aplicación&gt;*, en la página **Seleccionar grupos**, seleccione los grupos de usuarios o dispositivos en los que desea implementar la aplicación.

4.  En la página **Acción de implementación**, configure lo siguiente:

    |Configuración|Detalles|
    |-----------------|------------|
    |**Aprobación**|Elija una de las siguientes opciones para la implementación:<br /><br />-   **Requerida** (instalación obligatoria)<br />-   **Disponible** (los usuarios la instalan desde el portal de empresa a petición)<br />-   **No aplicable** (la aplicación no se instala o no se muestra en el portal de empresa)<br />-   **Desinstalar** (la aplicación se desinstalará de los dispositivos de destino)|
    |**Fecha límite**|En el caso de las instalaciones necesarias, elija cuándo se implementará la aplicación. Puede elegir entre los valores predefinidos, o bien seleccionar **Personalizado** para configurar su propia fecha límite.|

## <a name="BKMK_Monitor"></a>Supervisar la aplicación
Puede ver las aplicaciones que administra y su estado de implementación en la consola de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

### Para ver las aplicaciones que administra y su estado
En el área de trabajo **Aplicaciones**, haga clic en el nodo **Aplicaciones**.

Se mostrará la lista de aplicaciones que administra. Puede hacer clic en cualquier aplicación para ver el estado de la instalación en el panel inferior de las ventanas de la consola. Haga clic en este estado para ver más detalles. Por ejemplo, si se muestra el estado **1 usuario tiene este software disponible**, puede hacer clic en el mensaje para ver el nombre del usuario.

> [!TIP]
> Puede usar la lista desplegable **Filtros** para mostrar solo las aplicaciones que cumplen los criterios que especifique, como las aplicaciones que no se pudieron instalar o las aplicaciones que se implementaron correctamente.
> 
> ![](../Image/App-filters.JPG)

Además, el área de trabajo **Panel** muestra información general sobre el estado de las aplicaciones. Si hace clic en cualquier parte de la información general, accederá a la lista de aplicaciones.

### Para ver información más detallada sobre una aplicación
En la lista de aplicaciones, seleccione cualquier aplicación y haga clic en **Ver propiedades**.

En la página **Propiedades del software** de la aplicación, haga clic en una de estas pestañas:

-   **General**: muestra información general sobre la aplicación y su estado de instalación.

-   **Dispositivos**: muestra los dispositivos que instalaron correctamente una determinada implementación de la aplicación.

-   **Usuarios**: muestra los usuarios cuyos dispositivos instalaron correctamente una determinada implementación de la aplicación.

Al igual que antes, puede usar la lista desplegable **Filtros** para configurar los valores mostrados en cada una de las pestañas.

## Vea también
[Implementar y configurar aplicaciones con Microsoft Intune](../Topic/Deploy-and-configure-apps-with-Microsoft-Intune.md)

