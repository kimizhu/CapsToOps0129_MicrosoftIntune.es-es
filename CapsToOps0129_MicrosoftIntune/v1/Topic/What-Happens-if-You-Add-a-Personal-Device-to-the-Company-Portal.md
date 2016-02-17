---
title: Implicaciones de agregar un dispositivo personal al portal de empresa
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5703d18a-8b5b-4f47-a393-c2cc6cf7a614
---
# Implicaciones de agregar un dispositivo personal al portal de empresa
Si agrega un dispositivo al portal de empresa, podrá encontrar fácilmente aplicaciones para instalar, ver otros dispositivos agregados y encontrar los datos de contacto del administrador de TI. También proporciona al administrador de TI permiso para administrar el dispositivo, a fin de ayudar a proteger la información de la empresa en el dispositivo. Cada dispositivo se agrega de forma ligeramente diferente, algunos a través de la configuración del dispositivo y otros mediante la descarga de una aplicación de la tienda de aplicaciones del dispositivo.

## <a name="BKMK_IT_can_see"></a>Lo que TI puede y no puede ver cuando se inscribe un dispositivo en Intune
Para conocer los pasos para inscribir su dispositivo en Intune, consulte [Enroll your device in Microsoft Intune](../Topic/Enroll-your-device-in-Microsoft-Intune.md).

|TI no puede ver|TI puede ver|
|-------------------|----------------|
|-   Historial de llamadas<br />-   Mensajes de texto<br />-   Correo electrónico personal, contactos y calendario<br />-   Historial web<br />-   Ubicación<br />-   Álbum de cámara<br />-   Datos personales|-   Propietario<br />-   Nombre del dispositivo<br />-   Número de serie<br />-   Fabricante<br />-   Modelo<br />-   Sistema operativo<br />-   Aplicaciones de empresa<br />-   Aplicaciones personales|
Para obtener más detalles, seleccione el vínculo que corresponda al tipo de dispositivo:

-   [Windows Vista, Windows 7, Windows 8, Windows 8.1 Enterprise y Professional y Windows 10](#BKMK_what_happens_vista)

-   [Windows RT](#BKMK_what_happens_rt)

-   [Windows Phone 8 o Windows Phone 8.1](#BKMK_what_happens_phone8)

-   [Dispositivos iOS (iPhone y iPad)](#BKMK_what_happens_ios)

-   [Dispositivos Android](#BKMK_what_happens_android)

-   [Dispositivos configurados para correo electrónico únicamente](#BKMK_what_happens_email)

## <a name="BKMK_what_happens_vista"></a>Windows Vista, Windows 7, Windows 8, Windows 8.1 Enterprise y Professional y Windows 10
Cuando agrega un equipo:

-   Se instalarán algunas aplicaciones de software en el equipo para que el administrador de TI pueda administrar el equipo y para permitirle obtener recursos de la empresa, como aplicaciones o información de soporte técnico. El administrador de TI puede actualizar automáticamente este software.

-   Se puede instalar [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Endpoint Protection en el equipo. Se trata de software que permite detectar virus y malware. Para obtener más información, vea la [Declaración de privacidad de Endpoint Protection](http://go.microsoft.com/fwlink/?LinkID=247324).

-   El administrador de TI puede realizar un inventario de todo el software instalado en el equipo, incluido el software que usted haya instalado.

-   Debe aceptar los términos y condiciones.

-   El administrador de TI puede recopilar o eliminar datos de la unidad de disco duro del equipo. El administrador de TI también puede borrar todo el disco duro.

-   El administrador de TI puede instalar aplicaciones y actualizaciones en el equipo.

-   El administrador de TI puede aplicar directivas en el equipo. Por ejemplo, se le podría exigir establecer una contraseña o un PIN en el equipo, lo que podría impedir el acceso al equipo o eliminar todos los datos del disco duro del equipo tras varios intentos incorrectos de introducir la contraseña.

## <a name="BKMK_what_happens_rt"></a>Windows RT
Al agregar un dispositivo Windows RT, da permiso al administrador de TI para acceder al dispositivo. El administrador puede hacer cosas como:

-   Restablecer la configuración predeterminada de fábrica del dispositivo. Esto es útil en caso de pérdida o robo del dispositivo.

-   Quitar todos los datos relacionados con la empresa y las aplicaciones empresariales que se instalaron. La configuración personal y de datos no se quita.

-   Debe aceptar los términos y condiciones.

-   Forzarle a establecer una contraseña o un PIN para el dispositivo, lo que podría bloquear el dispositivo o restablecer la configuración predeterminada del dispositivo (operación que podría incluir la eliminación de datos) tras varios intentos incorrectos de introducir la contraseña.

-   Habilitar o deshabilitar el uso de una contraseña de imagen en el dispositivo.

-   Instalar actualizaciones de aplicaciones en el dispositivo.

    > [!NOTE]
    > Esto se aplica solo a las actualizaciones. El administrador no puede forzar la instalación de nuevas aplicaciones en el dispositivo, pero puede elegir instalar aplicaciones visibles en el portal de empresa.

## <a name="BKMK_what_happens_phone8"></a>Windows Phone 8 o Windows Phone 8.1
Al agregar un dispositivo Windows Phone, da permiso al administrador de TI para acceder al dispositivo. El administrador puede hacer cosas como:

-   Restablecer la configuración predeterminada de fábrica del dispositivo. Esto es útil en caso de pérdida o robo del dispositivo.

-   Quitar todos los datos relacionados con la empresa y las aplicaciones empresariales que se instalaron. Los datos personales y la configuración no se quitan.

-   Forzarle a establecer una contraseña o un PIN para el dispositivo, lo que podría bloquear el dispositivo o restablecer la configuración predeterminada del dispositivo (operación que podría incluir la eliminación de datos) tras varios intentos incorrectos de introducir la contraseña.

-   Forzar el cifrado de todos los datos en el dispositivo. Esto ayuda a proteger los datos en caso de pérdida o robo del dispositivo.

-   Debe aceptar los términos y condiciones.

-   Deshabilitar la tarjeta SD.

-   Instalar actualizaciones de aplicaciones en el dispositivo. Esto se aplica solo a las actualizaciones. El administrador no puede forzar la instalación de nuevas aplicaciones en el dispositivo, pero puede elegir instalar aplicaciones visibles en el portal de empresa.

-   Una vez agregado el dispositivo al portal de empresa, hará lo siguiente cada 8 horas aproximadamente:

    -   Descargar las actualizaciones de directivas o aplicaciones proporcionadas por el administrador de TI.

    -   Enviar actualizaciones de inventario de hardware.

    -   Enviar actualizaciones de inventario de aplicaciones de empresa.

## <a name="BKMK_what_happens_ios"></a>Dispositivos iOS (iPhone y iPad)
Al agregar un dispositivo iPhone o iPad, da permiso al administrador de TI para acceder al dispositivo. El administrador puede hacer cosas como:

-   Restablecer la configuración predeterminada de fábrica del dispositivo. Esto es útil en caso de pérdida o robo del dispositivo.

-   Quitar todos los datos relacionados con la empresa y las aplicaciones empresariales que se instalaron. Los datos personales y la configuración no se quitan.

-   Exigir el uso de una contraseña o un PIN en el dispositivo.

-   Debe aceptar los términos y condiciones.

-   Habilitar o deshabilitar la cámara en el dispositivo.

-   Habilitar o deshabilitar la exploración web en el dispositivo.

-   Habilitar o deshabilitar la copia de seguridad en iCloud.

-   Habilitar o deshabilitar la sincronización de documentos con iCloud.

-   Habilitar o deshabilitar la transmisión de fotos a iCloud.

-   Habilitar o deshabilitar la movilidad de datos en el dispositivo. Si se permite la movilidad de datos, podrían aplicarse cargos por movilidad.

-   Habilitar o deshabilitar la movilidad de voz en el dispositivo. Si se permite la movilidad de voz, podrían aplicarse cargos por movilidad.

-   Habilitar o deshabilitar en el dispositivo la sincronización automática de archivos en modo de movilidad. Si se permite la sincronización automática de archivos, podrían aplicarse cargos por movilidad.

## <a name="BKMK_what_happens_android"></a>Dispositivos Android
> [!IMPORTANT]
> Si habilita el registro detallado en el dispositivo y envía registros al administrador, los registros que envíe incluirán la dirección de correo electrónico.

Al agregar un dispositivo Android, da permiso al administrador de TI para acceder al dispositivo. El administrador puede hacer cosas como:

-   Restablecer la configuración predeterminada de fábrica del dispositivo. Esto es útil en caso de pérdida o robo del dispositivo.

-   Quitar todos los datos relacionados con la empresa. Los datos personales y la configuración no se quitan.

-   Forzarle a establecer una contraseña o un PIN para el dispositivo, lo que podría bloquear el dispositivo o restablecer la configuración predeterminada del dispositivo (operación que podría incluir la eliminación de datos) tras varios intentos incorrectos de introducir la contraseña.

-   Debe aceptar los términos y condiciones.

-   Habilitar o deshabilitar la cámara en el dispositivo.

-   Forzar el cifrado de todos los datos, incluidos los datos empresa y los personales, en el dispositivo. Esto ayuda a proteger los datos en caso de pérdida o robo del dispositivo.

-   Una vez agregado el dispositivo al portal de empresa, hará lo siguiente cada 8 horas aproximadamente:

    -   Descargar las actualizaciones de directivas o aplicaciones proporcionadas por el administrador de TI.

    -   Enviar actualizaciones de inventario de hardware (estas actualizaciones no contienen información personal).

    -   Enviar actualizaciones de inventario de aplicaciones de empresa (estas actualizaciones no contienen información personal).

## <a name="BKMK_what_happens_email"></a>Dispositivos configurados para correo electrónico únicamente
Si configura el dispositivo para poder usar el correo electrónico de empresa, está dando permiso al administrador de TI para acceder al dispositivo. Algunas de las cosas que el administrador de TI puede hacer son:

-   Restablezca manualmente la configuración predeterminada del fabricante del dispositivo o configure el dispositivo para restablecerlo si hay demasiados intentos de contraseña incorrectos. Esto es útil en caso de pérdida o robo del dispositivo.

    > [!IMPORTANT]
    > Al restablecer la configuración predeterminada de fábrica del dispositivo se eliminarán todos los datos de empresa y personales, así como las aplicaciones instaladas.

-   Exigir el cifrado del dispositivo y las tarjetas de almacenamiento extraíbles.

-   Habilitar o deshabilitar la descarga de archivos adjuntos de correo electrónico en el dispositivo.

-   Especificar la frecuencia de comprobación de correo electrónico de empresa en el dispositivo.

-   Habilitar o deshabilitar la exploración web en el dispositivo.

-   Establecer requisitos para la contraseña o el PIN usado en el dispositivo. Por ejemplo, pueden:

    -   Exigir el uso de una contraseña con una longitud específica, entre 4 y 18 letras o números.

    -   Exigir la combinación de mayúsculas y minúsculas que debe tener la contraseña.

    -   Exigir el uso de letras y símbolos, además de números.

    -   Controlar cuánto tiempo puede estar inactivo el dispositivo antes de tener que escribir una contraseña para desbloquearlo.

    -   Impedir el uso de contraseñas utilizadas previamente.

    -   Forzar el restablecimiento de la configuración de fábrica predeterminada en caso de que se realicen varios intentos incorrectos de introducir la contraseña. Esto ayuda a proteger el dispositivo en caso de pérdida o robo.

