---
title: Configurar el acceso al correo electr&#243;nico corporativo mediante perfiles de correo electr&#243;nico con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 10f0cd61-e514-4e44-b13e-aeb85a8e53ae
---
# Configurar el acceso al correo electr&#243;nico corporativo mediante perfiles de correo electr&#243;nico con Microsoft Intune
En [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], los perfiles de correo electrónico le ayudan a crear, implementar y supervisar la configuración de correo electrónico de Exchange ActiveSync en los dispositivos.Esto permite a los usuarios obtener acceso al correo electrónico corporativo en sus dispositivos personales sin tener que realizar ninguna configuración.

Puede utilizar perfiles de correo electrónico para configurar los siguientes tipos de dispositivo:

-   Dispositivos que ejecutan Windows Phone 8 y versiones posteriores

-   Dispositivos que ejecutan iOS 5 y versiones posteriores

-   Dispositivos que ejecutan Samsung KNOX Standard (4.0 y versiones posteriores)

Además de configurar una cuenta de correo electrónico en el dispositivo, también puede configurar opciones de sincronización como, por ejemplo, la cantidad de correo electrónico que se sincronizará y, en función el tipo de dispositivo, los tipos de contenido que se sincronizarán.

> [!IMPORTANT]
> Siempre que sea posible, elija las opciones más seguras que permitan sus sistemas operativos cliente e infraestructura de correo electrónico.Los perfiles de correo electrónico constituyen un método muy práctico para administrar y distribuir de forma centralizada la configuración de correo electrónico que sus dispositivos ya admiten.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] no agrega ninguna funcionalidad de correo electrónico.

## Cómo se protegen los perfiles de correo electrónico
Los perfiles de correo electrónico se pueden proteger con uno de estos dos métodos:

### Certificados
Cuando se crea el perfil de correo electrónico, puede elegir un perfil de certificado SCEP que ha creado previamente en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].Esto se conoce como certificado de identidad y se utiliza para autenticar con un perfil de certificado de confianza (o un certificado raíz) que ha creado para establecer que el dispositivo del usuario tiene permiso para conectarse.El certificado de confianza se implementa en el equipo que autentica la conexión de correo electrónico, por lo general, el servidor de Exchange.

Para obtener más información acerca de cómo crear y usar perfiles de certificado en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Habilitar el acceso a los recursos de empresa mediante perfiles de certificados con Microsoft Intune](../Topic/Enable-access-to-company-resources-using-certificate-profiles-with-Microsoft-Intune.md).

### Nombre de usuario y contraseña
El usuario se autentica en el servidor de Exchange proporcionando su nombre de usuario y contraseña.

La contraseña no está incluida en el perfil de correo electrónico, por lo que el usuario deberá proporcionarla al conectarse al correo electrónico.

### Crear un perfil de correo electrónico

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Directiva** &gt; **Agregar directiva**.

2.  Configure uno de los siguientes tipos de directivas:

    -   **Perfil de correo electrónico para Samsung KNOX estándar (4.0 y versiones posteriores)**

    -   **Perfil de correo electrónico (iOS 5 y versiones posteriores)**

    -   **Perfil de correo electrónico (Windows Phone 8 y versiones posteriores)**

    Solo puede crear e implementar una directiva de perfiles de correo electrónico personalizada.La configuración recomendada no está disponible.

    Si necesita más información acerca de cómo crear e implementar directivas, consulte el tema [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

3.  Utilice la tabla siguiente para ayudarle a configurar las opciones del perfil de correo electrónico de Samsung KNOX:

    |Nombre de la configuración|Más información|
    |------------------------------|-------------------|
    |**Nombre**|Escriba un nombre único para el perfil de correo electrónico.|
    |**Descripción**|Proporcione una descripción general del perfil de correo electrónico y otra información relevante que le ayude a encontrarlo.|
    |**Host**|Especifique el nombre de host del servidor de Exchange Server de su empresa que hospeda los servicios de Exchange ActiveSync.|
    |**Nombre de cuenta**|Especifique el nombre para mostrar de la cuenta de correo electrónico tal y como aparecerá para los usuarios en sus dispositivos.|
    |**Nombre de usuario**|Seleccione cómo se obtendrá el nombre de usuario de la cuenta de correo electrónico:<br /><br />-   Para un servidor de Exchange local, seleccione **Nombre de usuario**.<br />-   En el caso de Office 365, seleccione **Nombre principal del usuario**.|
    |**Dirección de correo electrónico**|Seleccione cómo se generará la dirección de correo electrónico del usuario en cada dispositivo:<br /><br />-   **Dirección SMTP principal**: use la dirección SMTP principal de los usuarios para iniciar sesión en Exchange.<br />-   **Nombre principal del usuario**: use el nombre principal del usuario completo como dirección de correo electrónico.|
    |**Método de autenticación**|Seleccione el método de autenticación que utiliza el perfil de correo electrónico:<br /><br />-   **Nombre de usuario y contraseña**<br />-   **Certificados**|
    |**Seleccionar un certificado de cliente para la autenticación de cliente (certificado de identidad)**|Seleccione el certificado SCEP de cliente que creó previamente y que se utilizará para autenticar la conexión de Exchange.Para obtener más información acerca de cómo utilizar perfiles de certificado en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Habilitar el acceso a los recursos de empresa mediante perfiles de certificados con Microsoft Intune](../Topic/Enable-access-to-company-resources-using-certificate-profiles-with-Microsoft-Intune.md). **Note:** Esta opción solo se muestra cuando el método de autenticación es **Certificados**.|
    |**Utilizar S/MIME**|Enviar correo electrónico saliente mediante cifrado S/MIME.|
    |**Certificado de firma**|Seleccione el certificado de firma que se utilizará para firmar el correo electrónico saliente. **Note:** Esta opción se muestra solo cuando se selecciona **Utilizar S/MIME**.|
    |**Número de días de correo electrónico para sincronizar**|En la lista desplegable, seleccione el número de días de correo electrónico que quiere sincronizar o seleccione **Sin límite** para sincronizar todo el correo electrónico disponible.|
    |**Programación de sincronización**|Seleccione la programación por la que los dispositivos sincronizarán los datos de Exchange Server.También puede seleccionar **Cuando lleguen los mensajes**, que sincroniza los datos tan pronto como llegan, o **Manual**, para que el usuario del dispositivo deba iniciar la sincronización.|
    |**Usar SSL**|Use la comunicación de Capa de sockets seguros (SSL) al enviar correos electrónicos, recibir correos electrónicos y comunicarse con Exchange Server. **Note:** Para dispositivos que ejecutan Samsung KNOX 4.0 o posterior, es necesario exportar el certificado SSL de Exchange Server e implementarlo como perfil de certificado de confianza de Android en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] no admite el acceso a este certificado si está instalado en el servidor de Exchange Server por otros medios.|
    |**Tipo de contenido para sincronizar**|Seleccione los tipos de contenido que quiere sincronizar con los dispositivos.Elija de entre las siguientes opciones:<br /><br />-   **Correo electrónico**<br />-   **Contactos**<br />-   **Calendario**<br />-   **Tareas**<br />-   **Notas**|
    Utilice la tabla siguiente como ayuda para configurar las opciones del perfil de correo electrónico de iOS:

    |Nombre de la configuración|Más información|
    |------------------------------|-------------------|
    |**Nombre**|Escriba un nombre único para el perfil de correo electrónico.|
    |**Descripción**|Proporcione una descripción general del perfil de correo electrónico y otra información relevante que le ayude a encontrarlo.|
    |**Host**|Especifique el nombre de host del servidor de Exchange Server de su empresa que hospeda los servicios de Exchange ActiveSync.|
    |**Nombre de cuenta**|Especifique el nombre para mostrar de la cuenta de correo electrónico tal y como aparecerá para los usuarios en sus dispositivos.|
    |**Nombre de usuario**|Seleccione cómo se genera el nombre de usuario para la cuenta de correo electrónico en cada dispositivo.Puede seleccionar una de las siguientes opciones de la lista desplegable:<br /><br />-   **Dirección SMTP principal**: use la dirección SMTP principal de los usuarios para iniciar sesión en Exchange.<br />-   **Nombre principal del usuario**: use el nombre principal del usuario completo para iniciar sesión en Exchange.|
    |**Dirección de correo electrónico**|Seleccione cómo se genera la dirección de correo electrónico para el usuario en cada dispositivo.Puede seleccionar una de las siguientes opciones de la lista desplegable:<br /><br />-   **Dirección SMTP principal**: use la dirección SMTP principal de los usuarios para iniciar sesión en Exchange.<br />-   **Nombre principal del usuario**: use el nombre principal del usuario completo como dirección de correo electrónico.|
    |**Método de autenticación**|Seleccione el método de autenticación que utiliza el perfil de correo electrónico:<br /><br />-   **Nombre de usuario y contraseña**<br />-   **Certificados**|
    |**Seleccionar un certificado de cliente para la autenticación de cliente (certificado de identidad)**|Seleccione el certificado SCEP de cliente que creó previamente y que se utilizará para autenticar la conexión de Exchange.Para obtener más información acerca de cómo utilizar perfiles de certificado en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Habilitar el acceso a los recursos de empresa mediante perfiles de certificados con Microsoft Intune](../Topic/Enable-access-to-company-resources-using-certificate-profiles-with-Microsoft-Intune.md). **Note:** Esta opción solo se muestra cuando el método de autenticación es **Certificados**.|
    |**Utilizar S/MIME**|Enviar correo electrónico saliente mediante cifrado S/MIME.|
    |**Certificado de firma**|También puede seleccionar el certificado de firma que se utilizará para firmar el correo electrónico saliente. **Note:** Esta opción se muestra solo cuando se selecciona **Utilizar S/MIME**.|
    |**Número de días de correo electrónico para sincronizar**|En la lista desplegable, seleccione el número de días de correo electrónico que quiere sincronizar o seleccione **Sin límite** para sincronizar todo el correo electrónico disponible.|
    |**Usar SSL**|Use la comunicación de Capa de sockets seguros (SSL) al enviar correos electrónicos, recibir correos electrónicos y comunicarse con Exchange Server.|
    |**Permitir que los mensajes se muevan a otras cuentas de correo electrónico**|Permita a los usuarios mover los mensajes de correo electrónico entre las distintas cuentas que han configurado en su dispositivo.|
    |**Permitir que se envíe correo electrónico desde aplicaciones de terceros**|Permita a los usuarios enviar correo electrónico desde aplicaciones que no son la aplicación de correo electrónico predeterminada.|
    |**Sincronizar las direcciones de correo electrónico usadas recientemente**|Sincronice la lista de direcciones de correo electrónico que se han utilizado recientemente en el dispositivo.|
    Utilice la tabla siguiente como ayuda para configurar las opciones del perfil de correo electrónico de Windows Phone:

    |Nombre de la configuración|Más información|
    |------------------------------|-------------------|
    |**Nombre**|Escriba un nombre único para el perfil de correo electrónico.|
    |**Descripción**|Proporcione una descripción general del perfil de correo electrónico y otra información relevante que le ayude a encontrarlo.|
    |**Host**|Especifique el nombre de host del servidor de Exchange Server de su empresa que hospeda los servicios de Exchange ActiveSync.|
    |**Nombre de cuenta**|Especifique el nombre para mostrar de la cuenta de correo electrónico tal y como aparecerá para los usuarios en sus dispositivos.|
    |**Nombre de usuario**|Seleccione cómo se genera el nombre de usuario para la cuenta de correo electrónico en cada dispositivo.Puede seleccionar una de las siguientes opciones de la lista desplegable:<br /><br />-   **Dirección SMTP principal**: use la dirección SMTP principal de los usuarios para iniciar sesión en Exchange.<br />-   **Nombre principal del usuario**: use el nombre principal del usuario completo para iniciar sesión en Exchange.|
    |**Dirección de correo electrónico**|Seleccione cómo se genera la dirección de correo electrónico para el usuario en cada dispositivo cliente.Puede seleccionar una de las siguientes opciones de la lista desplegable:<br /><br />-   **Dirección SMTP principal** Se usa la dirección SMTP principal de los usuarios para iniciar sesión en Exchange.<br />-   **Nombre principal de usuario** Se usa el nombre principal de usuario completo como dirección de correo electrónico.|
    |**Número de días de correo electrónico para sincronizar**|En la lista desplegable, seleccione el número de días de correo electrónico que quiere sincronizar o seleccione **Sin límite** para sincronizar todo el correo electrónico disponible.|
    |**Programación de sincronización**|Seleccione la programación por la que los dispositivos sincronizarán los datos de Exchange Server.También puede seleccionar **Cuando lleguen los mensajes**, que sincroniza los datos tan pronto como llegan, o **Manual**, para que el usuario del dispositivo deba iniciar la sincronización.|
    |**Usar SSL**|Use la comunicación de Capa de sockets seguros (SSL) al enviar correos electrónicos, recibir correos electrónicos y comunicarse con Exchange Server.|
    |**Tipo de contenido para sincronizar**|Seleccione los tipos de contenido que quiere sincronizar con los dispositivos.Elija de entre las siguientes opciones:<br /><br />-   **Correo electrónico**<br />-   **Contactos**<br />-   **Calendario**<br />-   **Tareas**|
    > [!IMPORTANT]
    > Si ha implementado un perfil de correo electrónico y después cambiar los valores de **Host de Exchange ActiveSync** o **Dirección de correo electrónico**, debe eliminar el perfil de correo electrónico existente y crear uno nuevo con los valores necesarios.

4.  Cuando haya terminado haga clic en **Guardar directiva**.

La nueva directiva se muestra en el nodo **Directivas de configuración** del área de trabajo **Directiva**.

### Implementar un perfil de correo electrónico

1.  Implemente el perfil de correo electrónico en uno o más grupos de usuarios o dispositivos de su organización.

Para obtener más información sobre cómo implementar directivas, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

En el área de trabajo **Directiva** de la página **General**, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención.Además, aparece un resumen de estado en el área de trabajo **Panel**.

> [!NOTE]
> Si desea quitar un perfil de correo electrónico de un dispositivo, edite la implementación y quite los grupos de los que sea miembro el dispositivo.

## Pasos siguientes
Tras una implementación correcta, se pueden aprovisionar los dispositivos del usuario con la configuración correcta para tener acceso al correo electrónico corporativo.

## Vea también
[Habilitar el acceso a los recursos de empresa con Microsoft Intune](../Topic/Enable-access-to-company-resources-with-Microsoft-Intune---deleted.md)

