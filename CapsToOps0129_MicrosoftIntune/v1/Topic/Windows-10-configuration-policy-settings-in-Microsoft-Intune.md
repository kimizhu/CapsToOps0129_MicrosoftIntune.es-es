---
title: Configuraci&#243;n de directivas de configuraci&#243;n de Windows 10 en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 00a602d9-b339-4fd8-ab70-defbf6686855
---
# Configuraci&#243;n de directivas de configuraci&#243;n de Windows 10 en Microsoft Intune
Use la [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] **directiva de configuración general** de Windows 10 para configurar las opciones de los dispositivos inscritos (tanto móviles como de escritorio) con Windows 10 y Windows 10 Mobile:

## Crear una directiva de configuración general de Windows 10

#### Para proporcionar la configuración básica de una directiva de configuración

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Directiva** &gt; **Información general** &gt; **Agregar directiva**.

2.  Haga clic en **Windows** &gt; **Configuración general (Windows 10 Desktop, Windows 10 Mobile y posterior)** y luego haga clic en **Crear directiva**.

    > [!NOTE]
    > No se puede crear una directiva de configuración usando la configuración recomendada. Debe crear una directiva personalizada.

3.  En la sección **General** de la página **Crear directiva**, especifique un nombre y una descripción para la nueva directiva.

4.  Use la información que encontrará en las secciones siguientes para ayudarle a proporcionar la configuración de la directiva.

5.  Cuando haya terminado haga clic en **Guardar directiva**.

La nueva directiva se muestra en el nodo **Directivas de configuración** del área de trabajo **Directiva**.

## Configuración de seguridad

### Contraseña

|Nombre de la configuración|Windows 10 Escritorio|Windows 10 Móvil|
|------------------------------|-------------------------|--------------------|
|**Requerir contraseña para desbloquear dispositivos**|Sí|Sí|
|**Tipo de contraseña obligatoria**<br /><br />(Especifica el tipo de contraseña que será necesario, por ejemplo, solo numérica o alfanumérica)|Sí|Sí|
|**Tipo de contraseña necesaria**: **Número mínimo de conjuntos de caracteres**<br /><br />Hay cuatro conjuntos de caracteres: letras minúsculas, letras mayúsculas, números y símbolos. Esta configuración especifica cuántos conjuntos de caracteres diferentes deben incluirse en la contraseña.|Sí|Sí|
|**Longitud mínima de la contraseña (solo Windows 10 Escritorio)** **Important:** Esta configuración ya no es compatible y se eliminará en el futuro. Puede usar la configuración siguiente de Windows 10 Mobile para los equipos de escritorio.|Sí|No|
|**Longitud mínima de la contraseña (solo Windows 10 Móvil)**|No|Sí|
|**Número de errores de inicio de sesión repetidos que se permiten antes de que se borre el dispositivo**|Sí|Sí|
|**Minutos de inactividad antes de que se apague la pantalla**|Sí|Sí|
|**Expiración de contraseña (días)**|Sí|Sí|
|**Recordar el historial de contraseñas**|Sí|Sí|
|**Recordar historial de contraseñas**: **Impedir la reutilización de contraseñas anteriores**|Sí|Sí|
|**Permitir contraseña de imagen y PIN**<br /><br />Le permite usar gestos simples en una imagen o un PIN sencillo para iniciar sesión.|Sí|No|
|**Requerir una contraseña cuando el dispositivo vuelva de un estado de inactividad**|No|Sí|

### Cifrado

|Nombre de la configuración|Windows 10 Escritorio|Windows 10 Móvil|
|------------------------------|-------------------------|--------------------|
|**Requerir cifrado en dispositivo móvil**|No|Sí|

### System

|Nombre de la configuración|Windows 10 Escritorio|Windows 10 Móvil|
|------------------------------|-------------------------|--------------------|
|**Permitir captura de pantalla**|No|Sí|
|**Permitir cancelar suscripción manualmente**<br /><br />Permite al usuario eliminar manualmente la cuenta del área de trabajo desde el dispositivo.|Sí|Sí|
|**Permitir la instalación de certificado raíz manualmente**<br /><br />Especifica si el usuario puede instalar certificados raíz manualmente.|No|Sí|
|**Permitir que datos de diagnóstico y uso se envíen a Microsoft**|Sí|Sí|

## Configuración de nube

### Cuenta y sincronización

|Nombre de la configuración|Windows 10 Escritorio|Windows 10 Móvil|
|------------------------------|-------------------------|--------------------|
|**Permitir cuenta de Microsoft**|Sí|Sí|
|**Permitir añadir cuentas que no son de Microsoft de forma manual**|Sí|Sí|
|**Permitir la sincronización de la configuración de las cuentas de Microsoft**|Sí|Sí|

## Configuración de correo electrónico

|Nombre de la configuración|Windows 10 Escritorio|Windows 10 Móvil|
|------------------------------|-------------------------|--------------------|
|**Hacer que la cuenta Microsoft sea opcional en la aplicación Windows Mail**|Sí|No|

## Configuración de aplicaciones

### Microsoft Edge

|Nombre de la configuración|Windows 10 Escritorio|Windows 10 Móvil|
|------------------------------|-------------------------|--------------------|
|**Permitir explorador web**|No|Sí|
|**Permitir sugerencias de búsqueda en la barra de direcciones**|Sí|Sí|
|**Permitir enviar tráfico de intranet a Internet Explorer**|Sí|No|
|**Permitir no rastrear**|Sí|Sí|
|**Habilitar SmartScreen**|Sí|Sí|
|**Permitir Active scripting**|Sí|Sí|
|**Permitir elementos emergentes**|Sí|No|
|**Permitir cookies**|Sí|Sí|
|**Permitir autorrellenar**|Sí|No|
|**Permitir administrador de contraseñas**|Sí|Sí|
|**Ubicación de la lista de sitios de Modo de empresa**<br /><br />Especifica dónde se encuentra la lista de sitios web que se abrirá en modo de empresa. Los usuarios no pueden editar esta lista.|Sí|No|

### Aplicaciones

|Nombre de la configuración|Windows 10 Escritorio|Windows 10 Móvil|
|------------------------------|-------------------------|--------------------|
|**Permitir almacén de aplicaciones**|No|Sí|

## Configuración de las capacidades de los dispositivos

### Móvil

|Nombre de la configuración|Windows 10 Escritorio|Windows 10 Móvil|
|------------------------------|-------------------------|--------------------|
|**Permitir itinerancia de datos**|Sí|Sí|
|**Permitir VPN sobre móvil**|Sí|Sí|
|**Permitir itinerancia de VPN sobre móvil**|Sí|Sí|

### Hardware

|Nombre de la configuración|Windows 10 Escritorio|Windows 10 Móvil|
|------------------------------|-------------------------|--------------------|
|**Permitir cámara**|Sí|Sí|
|**Permitir almacenamiento extraíble**|Sí|Sí|
|**Permitir Wi-Fi**|No|Sí|
|**Permitir compartir Internet**|Sí|Sí|
|**Permitir la configuración Wi-Fi manual**|No|Sí|
|**Permitir la conexión automática a zonas Wi-Fi gratuitas**|Sí|Sí|
|**Permitir geolocalización**<br /><br />Especifica si el dispositivo puede usar información de servicios de ubicación.|Sí|Sí|
|**Permitir NFC**|Sí|Sí|
|**Permitir Bluetooth**|Sí|Sí|
|**Permitir modo visible de Bluetooth**|Sí|Sí|
|**Permitir anuncios de Bluetooth**<br /><br />Permite que los dispositivos reciban anuncios a través de Bluetooth.|Sí|Sí|
|**Permitir modo conectable de Bluetooth** **Important:** Esta configuración ya no es compatible con Windows 10 y se eliminará en el futuro.|Sí|Sí|
|**Permitir restablecer teléfono**|Sí|Sí|
|**Permitir conexión USB**|Sí|Sí|
|**Permitir modo antirrobo**<br /><br />Permite habilitar el modo antirrobo de Windows.|Sí|Sí|

### Funciones

|Nombre de la configuración|Windows 10 Escritorio|Windows 10 Móvil|
|------------------------------|-------------------------|--------------------|
|**Permitir copiar y pegar**|No|Sí|
|**Permitir grabación de voz**|No|Sí|
|**Permitir a Cortana**|Sí|Sí|
|**Permitir notificaciones del centro de actividades**|No|Sí|

## Configuración de actualizaciones

|Nombre de la configuración|Descripción|Windows 10 Escritorio|Windows 10 Móvil|
|------------------------------|---------------|-------------------------|--------------------|
|**Permitir actualizaciones automáticas**|Habilite esta configuración para permitir las actualizaciones automáticas. Luego, configure una de las opciones siguientes para controlar el comportamiento de las actualizaciones:<br /><br /><ul><li>**Notificar descarga**</li><li>**Instalar automáticamente en tiempo de mantenimiento**</li><li>**Instalar y reiniciar automáticamente en tiempo de mantenimiento**</li><li>**Instalar y reiniciar automáticamente a la hora programada**<br /><br />    Cuando esta opción está seleccionada, también puede configurar los valores siguientes:<br /><br /><ul><li>**Suprimir notificación para el usuario final**</li><li>**Definir el día de instalación para las actualizaciones programadas**</li></ul></li></ul>|Sí|No|

## Implementar la directiva de configuración

1.  Implemente la directiva de configuración en uno o más grupos de usuarios o dispositivos de su organización.

Para obtener más información sobre cómo implementar directivas, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

En el área de trabajo **Directiva**, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención. Además, aparece un resumen de estado en el área de trabajo **Panel**.

## Vea también
[Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md)

