---
title: Configuraci&#243;n de directivas de configuraci&#243;n de iOS en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ab46be6c-ab73-4c99-8492-66d1dd418293
---
# Configuraci&#243;n de directivas de configuraci&#243;n de iOS en Microsoft Intune
Utilice la [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] **Directiva de configuración general de iOS** para configurar opciones para:

-   **Configuración de seguridad de dispositivos móviles**: elija entre una lista de configuraciones predefinidas que permiten controlar una variedad de características y la funcionalidad en el dispositivo.

-   **Pantalla completa**: bloquee un dispositivo para permitir que solo funcionen determinadas características. Por ejemplo, puede permitir que un dispositivo ejecute solo una aplicación administrada que especifique, o puede deshabilitar los botones de volumen de un dispositivo. Esta configuración podría utilizarse para un modelo de demostración de un dispositivo o para un dispositivo que está dedicado a realizar solo una función, como un dispositivo de punto de venta.

-   **Aplicaciones conformes y no conformes**: especifique una lista de las aplicaciones conformes y de las no conformes en su empresa. En los dispositivos iOS y Android, el **informe de aplicaciones no conformes** puede utilizarse para comparar la conformidad de las aplicaciones especificadas en la lista con las aplicaciones que los usuarios han instalado (pero en realidad no pueden impedir la instalación de la aplicación).

> [!TIP]
> Puede configurar los términos y condiciones de los usuarios para asegurarse de que saben que las aplicaciones de su dispositivo, incluidas las aplicaciones personales, se evaluarán y que las aplicaciones no conformes se bloquearán o se notificarán como no conformes. Los usuarios deben aceptar estos términos y condiciones para poder inscribir su dispositivo y utilizar el portal de empresa para obtener aplicaciones. Para obtener más información acerca del uso de los términos y condiciones, consulte [Working with terms and conditions policies in Microsoft Intune](http://msdn.microsoft.com/en-us/library/ce59fb93-01fd-4822-a57d-45ca7d89843d).

## Crear una directiva de configuración general de iOS

#### Para proporcionar la configuración básica de una directiva de configuración

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Directiva** &gt; **Información general** &gt; **Agregar directiva**.

2.  Haga clic en **iOS** &gt; **Configuración general** y, a continuación, en **Crear directiva**.

    > [!NOTE]
    > No se puede crear una directiva de configuración usando la configuración recomendada. Debe crear una directiva personalizada.

3.  En la sección **General** de la página **Crear directiva**, especifique un nombre y una descripción para la nueva directiva.

4.  Use la información que encontrará en las secciones siguientes para ayudarle a proporcionar la configuración de la directiva.

5.  Cuando haya terminado haga clic en **Guardar directiva**.

La nueva directiva se muestra en el nodo **Directivas de configuración** del área de trabajo **Directiva**.

## <a name="BKMK_Settings"></a>Configuración de dispositivos iOS
Si el valor que busca no aparece en esta lista, puede crearlo mediante una directiva personalizada de iOS que le permita importar la configuración creada con [Apple Configurator](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12). Para obtener más información, vea [Configuración de directivas personalizadas de iOS en Microsoft Intune](../Topic/iOS-custom-policy-settings-in-Microsoft-Intune.md).

### <a name="BKMK_sec"></a>Configuración de seguridad

|Nombre de la configuración|iOS|
|------------------------------|-------|
|**Requerir una contraseña para desbloquear dispositivos móviles**|Sí|
|**Tipo de contraseña obligatoria**<br /><br />(especifica el tipo de contraseña que será necesario, como solo numérica o alfanumérica).|Sí|
|**Tipo de contraseña requerida: número mínimo de conjuntos de caracteres**<br /><br />Hay cuatro conjuntos de caracteres: letras minúsculas, letras mayúsculas, símbolos y números. Esta configuración especifica cuántos conjuntos de caracteres diferentes deben incluirse en la contraseña. Sin embargo, para dispositivos iOS, especifica el número de caracteres de símbolos que deben incluirse en la contraseña.|Sí|
|**Longitud mínima de contraseña**|Sí|
|**Permitir contraseñas sencillas**<br /><br />Contraseñas sencillas serían, por ejemplo, "0000" y "1234".|Sí|
|**Número de errores de inicio de sesión repetidos que se permiten antes de que se borre el dispositivo**|Sí|
|**Minutos de inactividad antes de que se apague la pantalla**<sup>1</sup>|Sí|
|**Expiración de contraseña (días)**|Sí|
|**Recordar el historial de contraseñas**|Sí|
|**Recordar historial de la contraseña**: **Impedir la reutilización de contraseñas anteriores**|Sí|
|**Minutos de inactividad antes de que se pida la contraseña**<sup>1</sup>|Sí|
|**Permitir desbloqueo mediante huellas digitales**|iOS 7.1 y versiones posteriores|
<sup>1</sup> En los dispositivos iOS, cuando configura las opciones **Minutos de inactividad antes de que se apague la pantalla** y **Minutos de inactividad antes de que sea necesaria la contraseña**, estas se aplican en secuencia. Por ejemplo, si establece el valor para ambas opciones en **5** minutos, la pantalla se apagará automáticamente transcurridos 5 minutos y el dispositivo se bloqueará pasados 5 minutos más. Sin embargo, si el usuario apaga la pantalla manualmente, la segunda opción se aplica inmediatamente. En el mismo ejemplo, una vez que el usuario apague la pantalla, el dispositivo se bloqueará 5 minutos más tarde.

### Configuración del sistema

|Nombre de la configuración|iOS|
|------------------------------|-------|
|**Permitir capturas de pantalla**|Sí|
|**Permitir centro de control en la pantalla de bloqueo**|iOS 7.1 y versiones posteriores|
|**Permitir vista de notificaciones en la pantalla de bloqueo**|iOS 7.1 y versiones posteriores|
|**Permitir vista de hoy en la pantalla de bloqueo**|iOS 7.1 y versiones posteriores|
|**Permitir el envío de datos de diagnóstico**|Sí|
|**Permitir certificados TLS que no son de confianza**|Sí|
|**Permitir libreta con dispositivo bloqueado**|Sí|

### <a name="BKMK_cloud"></a>Configuración de nube: documentos y datos

|Nombre de la configuración|iOS|
|------------------------------|-------|
|**Permitir copias de seguridad en iCloud**|Sí|
|**Permitir sincronización de documentos en iCloud**|Sí|
|**Permitir sincronización de Photo Stream en iCloud**|Sí|
|**Requerir copia de seguridad cifrada**|Sí|

### <a name="BKMK_browser"></a>Configuración de la aplicación: explorador

|Nombre de la configuración|iOS|
|------------------------------|-------|
|**Permitir Safari**|Sí|
|**Permitir el autorrelleno**|Sí|
|**Permitir bloqueador de elementos emergentes**|Sí|
|**Permitir cookies**|Sí|
|**Permitir scripting de Java**|Sí|
|**Permitir advertencias de fraude**|Sí|

### <a name="BKMK_apps"></a>Configuración de la aplicación: aplicaciones

|Nombre de la configuración|iOS|
|------------------------------|-------|
|**Permitir almacén de aplicaciones**|Sí|
|**Requerir una contraseña para tener acceso al almacén de aplicaciones**|Sí|
|**Permitir compras dentro de la aplicación**|Sí|
|**Permitir documentos administrados en otras aplicaciones no administradas**|iOS 7.1 y versiones posteriores|
|**Permitir documentos no administrados en otras aplicaciones administradas**|iOS 7.1 y versiones posteriores|
|**Permitir videoconferencias**|Sí|
|**Permitir contenido para adultos en el almacén multimedia**|Sí|

### Configuración de aplicaciones: juegos

|Nombre de la configuración|iOS|
|------------------------------|-------|
|**Permitir agregar amigos al centro de juegos**|Sí|
|**Permitir juegos multijugador**|Sí|

### <a name="BKMK_hard"></a>Configuración de funcionalidades del dispositivo: hardware

|Nombre de la configuración|iOS|
|------------------------------|-------|
|**Permitir cámara**|Sí|

### Configuración de funcionalidades del dispositivo: datos móviles

|Nombre de la configuración|iOS|
|------------------------------|-------|
|**Permitir itinerancia de voz**|Sí|
|**Permitir itinerancia de datos**|Sí|
|**Permitir captura de fondo global durante la itinerancia**|Sí|

### Configuración de funcionalidades del dispositivo: características

|Nombre de la configuración|iOS|
|------------------------------|-------|
|**Permitir Siri**|Sí|
|**Permitir Siri con el dispositivo bloqueado**|Sí|
|**Permitir la marcación por voz**|Sí|
|**Permitir el uso compartido del Portapapeles entre aplicaciones**|No|
|**Permitir YouTube**|No|

## Configuración de aplicaciones conformes y no conformes
En la lista **Aplicaciones conformes y no conformes**, especifique una lista de aplicaciones conformes y no conformes con la siguiente información:

> [!NOTE]
> Una única directiva solo puede contener una lista de aplicaciones conformes o una lista de aplicaciones no conformes. No se pueden especificar ambas en la misma directiva.

|Nombre de la configuración|Más información|
|------------------------------|-------------------|
|**Notificar la no compatibilidad cuando los usuarios instalan las aplicaciones de la lista**|Enumera las aplicaciones que no se administran mediante Intune y que los usuarios no pueden instalar ni ejecutar.|
|**No informar de incompatibilidad cuando los usuarios instalan las aplicaciones enumeradas.**|Enumera las aplicaciones que los usuarios pueden instalar. Los usuarios no pueden instalar ninguna otra aplicación. Las aplicaciones que se administran mediante Intune están permitidas automáticamente.|
|**Agregar**|Agrega una aplicación a la lista seleccionada. Especifique un nombre de su elección, opcionalmente el editor de la aplicación y la dirección URL de la aplicación en la tienda de aplicaciones.<br /><br />[Cómo especificar las direcciones URL de tiendas de aplicaciones](../Topic/iOS-configuration-policy-settings-in-Microsoft-Intune.md#BKMK_URL)|
|**Importar aplicaciones**|Importa la lista de las aplicaciones que ha especificado en un archivo de valores separados por comas. Utilice el formato, nombre de la aplicación, editor, dirección URL de la aplicación en el archivo.|
|**Editar**|Permite editar el nombre, el editor y la dirección URL de la aplicación seleccionada.|
|**Eliminar**|Elimina la aplicación seleccionada de la lista.|

## Configuración del modo de pantalla completa
Especifique la siguiente configuración para los **dispositivos iOS**:

|Nombre de la configuración|Más información|
|------------------------------|-------------------|
|**Seleccione una aplicación administrada que se permitirá ejecutar cuando el dispositivo esté en modo de quiosco**|Haga clic en **Examinar** y, a continuación, especifique la aplicación administrada, o una aplicación de una tienda que se podrá ejecutar cuando el dispositivo esté en modo de quiosco. No se podrá ejecutar ninguna otra aplicación en el dispositivo.<br /><br />[Cómo especificar las direcciones URL de tiendas de aplicaciones](../Topic/iOS-configuration-policy-settings-in-Microsoft-Intune.md#BKMK_URL).|
|**Permitir la interacción táctil**|Habilita o deshabilita la pantalla táctil en el dispositivo.|
|**Permitir la rotación de pantalla**|Habilita o deshabilita el cambio de orientación de la pantalla cuando el dispositivo gira.|
|**Permitir los botones de volumen**|Habilita o deshabilita el uso de los botones de volumen en el dispositivo.|
|**Permite el conmutador de timbre**|Habilita o deshabilita el conmutador de timbre (silencio) en el dispositivo.|
|**Permitir el botón de reactivación de suspensión de pantalla**|Habilita o deshabilita el botón de reactivación de la suspensión de pantalla en el dispositivo.|
|**Permitir el bloqueo automático**|Habilita o deshabilita el bloqueo automático del dispositivo.|
|**Habilitar audio mono**|Habilita o deshabilita la configuración de accesibilidad **Audio mono**.|
|**Habilitar VoiceOver**|Habilita o deshabilita la opción de accesibilidad **VoiceOver**, que lee en voz alta el texto de la pantalla del dispositivo.|
|**Habilitar los ajustes de VoiceOver**|Habilita o deshabilita los ajustes de VoiceOver, que permiten ajustar la función VoiceOver (por ejemplo, la rapidez con la que se lee el texto en pantalla en voz alta).|
|**Habilitar zoom**|Habilita o deshabilita la configuración de accesibilidad de **Zoom**, que permite usar un toque para hacer zoom en la pantalla del dispositivo.|
|**Habilitar los ajustes de zoom**|Habilita o deshabilita los ajustes de zoom que permiten ajustar la función de zoom.|
|**Habilitar invertir colores**|Habilita o deshabilita la configuración de accesibilidad **Invertir colores**, que ajusta la pantalla para ayudar a los usuarios con discapacidades visuales.|
|**Habilitar los ajustes de invertir colores**|Habilita o deshabilita los ajustes de invertir colores que permiten ajustar la función de invertir colores.|
|**Habilitar la interacción táctil de asistencia**|Habilita o deshabilita la configuración de accesibilidad **Interacción táctil de asistencia** que ayuda a los usuarios a realizar gestos en pantalla que podrían resultarles difíciles.|
|**Habilitar los ajustes de la interacción táctil de asistencia**|Habilita o deshabilita los ajustes de la interacción táctil de asistencia que le permiten ajustar la función de interacción táctil de asistencia.|
|**Habilitar la selección de voz**|Habilita o deshabilita la configuración de accesibilidad **Reproducir selección** que lee en voz alta el texto que seleccione.|
> [!NOTE]
> Las siguientes notas se aplican a la configuración del modo de quiosco para dispositivos iOS:
> 
> -   Antes de configurar un dispositivo iOS para el modo de quiosco, debe usar la [herramienta Apple Configurator](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12) o el administrador de inscripción de dispositivos para ajustar el dispositivo en el modo de supervisión. Para obtener más información acerca de la herramienta Apple Configurator, consulte la documentación de Apple.
> -   Si la aplicación de iOS que especifique se instala después de implementar la directiva de configuración, el dispositivo no pasará al modo de quiosco hasta que se reinicie.

## Implementar la directiva de configuración

1.  Implemente la directiva de configuración en uno o más grupos de usuarios o dispositivos de su organización.

Para obtener más información sobre cómo implementar directivas, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

En el área de trabajo **Directiva**, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención. Además, aparece un resumen de estado en el área de trabajo **Panel**.

## Información de referencia para las aplicaciones conformes y no conformes

### Supervisar las aplicaciones conformes y no conformes
Utilice el **Informe de aplicaciones no conformes** para ver la conformidad de las aplicaciones permitidas y bloqueadas.

##### Para ejecutar el informe de aplicaciones no conformes

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Informes** &gt; **Informe de aplicaciones no conformes**.

2.  Seleccione los grupos de dispositivos que quiere comprobar, si quiere comprobar las aplicaciones conformes, las aplicaciones no conformes o ambas y, a continuación, haga clic en **Ver informe**.

### <a name="BKMK_URL"></a>Cómo especificar las direcciones URL de tiendas de aplicaciones
Para especificar una dirección URL de aplicación en la lista de aplicaciones conformes y no conformes o en la opción **Seleccione una aplicación administrada que se podrá ejecutar cuando el dispositivo esté en modo de pantalla completa** (solo iOS), use el siguiente formato:

Con la ayuda de un motor de búsqueda, busque la aplicación que desea usar en iTunes App Store y abra la página de la aplicación.

Copie la dirección URL de la página y úsela como dirección URL para configurar la lista de aplicaciones conformes y no conformes o la aplicación que desea ejecutar en modo de quiosco.

**Ejemplo:** busque **Microsoft Word for iPad**. La dirección URL que utilice será **https://itunes.apple.com/es/app/microsoft-word-for-ipad/id586447913?mt=8**.

> [!NOTE]
> También puede utilizar el software de iTunes para encontrar la aplicación y, a continuación, utilizar el comando **Copiar vínculo** para obtener la dirección URL de la aplicación.

## Vea también
[Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md)

