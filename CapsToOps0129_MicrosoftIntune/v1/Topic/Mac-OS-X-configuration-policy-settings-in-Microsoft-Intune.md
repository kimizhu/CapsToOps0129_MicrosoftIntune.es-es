---
title: Configuraci&#243;n de directivas de configuraci&#243;n de Mac OS X en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 98b2f19b-bee8-42d7-a215-a716d56a25a3
---
# Configuraci&#243;n de directivas de configuraci&#243;n de Mac OS X en Microsoft Intune
Use la **directiva de configuración general de Mac OS X** de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] a fin de configurar las opciones para:

-   **Configuración de seguridad de los dispositivos**: elija entre las opciones de una lista de configuraciones predefinidas que permiten controlar diversas características y funcionalidades en el dispositivo.

-   **Aplicaciones conformes y no conformes**: especifique una lista de las aplicaciones conformes y de las no conformes en su empresa. El informe de aplicaciones no compatibles puede usarse para comparar la compatibilidad de las aplicaciones especificadas en la lista frente a las aplicaciones que los usuarios han instalado (pero en realidad no pueden bloquear la instalación de la aplicación).

## Creación de una directiva de configuración general de Mac OS X

#### Para proporcionar la configuración básica de una directiva de configuración

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Directiva** &gt; **Información general** &gt; **Agregar directiva**.

2.  Haga clic en **Mac OS X** &gt; **Configuración general** y, después, en **Crear directiva**.

    > [!NOTE]
    > No se puede crear una directiva de configuración usando la configuración recomendada. Debe crear una directiva personalizada.

3.  En la sección **General** de la página **Crear directiva**, especifique un nombre y una descripción para la nueva directiva.

4.  Use la información que encontrará en las secciones siguientes para ayudarle a proporcionar la configuración de la directiva.

5.  Cuando haya terminado haga clic en **Guardar directiva**.

La nueva directiva se muestra en el nodo **Directivas de configuración** del área de trabajo **Directiva**.

## Configuración de dispositivos Mac OS X
Si el valor que busca no aparece en esta lista, puede crearlo mediante una directiva personalizada de Mac OS X que le permita importar la configuración que ha creado con la herramienta Apple Configurator. Para obtener más información, vea [Configuración de directivas personalizadas de Mac OS X en Microsoft Intune](../Topic/Mac-OS-X-custom-policy-settings-in-Microsoft-Intune.md).

### Configuración de contraseña

|Nombre de la configuración|Descripción|
|------------------------------|---------------|
|**Requerir contraseña para desbloquear dispositivos**|Especifica si el usuario debe utilizar una contraseña para acceder a su equipo Mac. **Important:** A diferencia de los dispositivos iOS, en los dispositivos Mac OS X no se envía una notificación al usuario inmediatamente para que actualice su contraseña para cumplir con esta configuración.|
|**Tipo de contraseña obligatoria**|Especifica si la contraseña usada solo puede ser numérica o si debe ser **alfanumérica** (contener letras y números). **Important:** Esta configuración solo es compatible con Mac OS X versión 10.10.3 y posteriores.|
|**Número de caracteres complejos requeridos en la contraseña**|Especifica el número de caracteres complejos que requiere la contraseña (de **0** a **4**).<br /><br />Un carácter complejo es un símbolo, como “**?**”.|
|**Longitud mínima de contraseña**|Especifica la longitud mínima de la contraseña (entre **4** y **14** caracteres).|
|**Permitir contraseñas sencillas**|Permite el uso de contraseñas sencillas, como "**0000**" o "**1234**".|
|**Minutos de inactividad antes de que se pida la contraseña**|Especifica el tiempo que el equipo debe estar inactivo antes de que se solicite una contraseña para desbloquearlo.|
|**Expiración de contraseña (días)**|Especifica cuántos días deben transcurrir para que el usuario deba cambiar la contraseña (de **1** a **255** días).|
|**Recordar el historial de contraseñas**|Esta configuración se utiliza para evitar que el usuario emplee una contraseña usada previamente. Al establecerla, también puede indicar la opción **Impedir la reutilización de contraseñas anteriores** para especificar el número de contraseñas usadas previamente que no se pueden volver a usar (de **1** a **24**).|
|**Minutos de inactividad antes de que se active el protector de pantalla**|Especifica el tiempo durante el que el equipo debe estar inactivo antes de que se active el protector de pantalla.|

## Configuración de aplicaciones conformes y no conformes
En la **Lista de aplicaciones compatibles y no compatibles para Mac OS X**, habilite **Configuración administrada para dispositivos** y especifique una lista de las aplicaciones conformes y no conformes con la siguiente información:

> [!NOTE]
> Una única directiva solo puede contener una lista de aplicaciones conformes o una lista de aplicaciones no conformes. No se pueden especificar ambas en la misma directiva.
> 
> [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] permite informar sobre los dispositivos con aplicaciones no compatibles. No bloquea la instalación ni quita las aplicaciones no compatibles.

|Nombre de la configuración|Descripción|
|------------------------------|---------------|
|**Notificar la no compatibilidad cuando los usuarios instalan las aplicaciones de la lista**|Enumera las aplicaciones Mac OS X que no se permite instalar a los usuarios. Si los usuarios instalan cualquiera de estas aplicaciones, se notificará en los **Informes de aplicaciones no compatibles**.|
|**Notificar la no compatibilidad cuando los usuarios instalan las aplicaciones que no están en la lista**|Enumera las aplicaciones Mac OS X que los usuarios pueden instalar. Si los usuarios instalan otras aplicaciones, se notificará en los **Informes de aplicaciones no compatibles**.|
|**Agregar**|Agrega una aplicación a la lista seleccionada. Especifique un nombre de su elección (opcionalmente, el editor de la aplicación) y el identificador de paquete de la aplicación. **Tip:** Para buscar el identificador de paquete de una aplicación, siga estos pasos en un equipo Mac que tenga la aplicación instalada:<ol><li>Abra la carpeta en la que está instalada la aplicación (por ejemplo, **/Applications**)</li><li>Seleccione el paquete *&lt;nombre de la aplicación&gt;***.app** y elija **Mostrar contenido del paquete**</li><li>Abra el archivo **Info.plist**</li><li>Compruebe el valor asociado a la clave **CFBundleIdentifier**</li></ol>El formato del identificador de paquete es **com.contoso.appname**|
|**Importar aplicaciones**|Importa la lista de las aplicaciones que ha especificado en un archivo de valores separados por comas. Use el formato, el nombre de la aplicación, el editor y el identificador de paquete de la aplicación en el archivo.|
|**Editar**|Permite editar el nombre, el editor y el identificador de paquete de la aplicación seleccionada.|
|**Eliminar**|Elimina la aplicación seleccionada de la lista.|
> [!TIP]
> Para obtener más información acerca de los informes de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Comprender las operaciones de Microsoft Intune mediante informes](../Topic/Understand-Microsoft-Intune-operations-by-using-reports.md).

## Implementación de la directiva de configuración
Implemente la directiva de configuración en uno o más grupos de usuarios o dispositivos de su organización.

Para obtener más información sobre cómo implementar las directivas, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

En el área de trabajo **Directiva**, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención. Además, aparece un resumen de estado en el área de trabajo **Panel**.

> [!IMPORTANT]
> Cuando un dispositivo Mac OS X está en modo de suspensión, no se pueden entregar ni inventariar las directivas y los perfiles. Como resultado, la consola de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] puede mostrar temporalmente el estado **Configuraciones de directivas con errores** hasta que el dispositivo salga del modo de suspensión.

## Supervisar las aplicaciones conformes y no conformes
Use los **Informes de aplicaciones no compatibles** para ver la compatibilidad de las aplicaciones que especificó.

#### Para ejecutar el informe

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Informes** &gt; **Informes de aplicaciones no compatibles**.

2.  Seleccione los grupos de dispositivos que quiere comprobar, si quiere comprobar las aplicaciones conformes, las aplicaciones no conformes o ambas y, a continuación, haga clic en **Ver informe**.

## Vea también
[Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md)

