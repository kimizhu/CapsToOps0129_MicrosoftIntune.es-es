---
title: Capacidades de administraci&#243;n de dispositivos m&#243;viles en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f23b3ee7-78da-4e53-9fc2-78e58401bcf9
---
# Capacidades de administraci&#243;n de dispositivos m&#243;viles en Microsoft Intune
Intune admite la administración de dispositivos móviles de Windows Phone, iOS y Android. También admite la administración de equipos con Windows RT, Windows y Mac OS X como dispositivos móviles. Los usuarios usan el *portal de empresa* para instalar aplicaciones, inscribir y quitar dispositivos, y como ayuda para ponerse en contacto con su departamento de TI o departamento de soporte técnico. Para inscribir dispositivos móviles, debe establecer [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] como su *autoridad de dispositivo móvil* y, a continuación, configurar la infraestructura para admitir las plataformas que desea administrar. Esto requiere el establecimiento de una relación de confianza con el dispositivo.

## <a name="BKMK_MobileDeviceReqs"></a>Dispositivos móviles compatibles
Los requisitos para administrar un dispositivo móvil y el nivel de administración que tiene dependen de si administra el dispositivo directamente o utiliza Exchange ActiveSync:

-   **Administración directa**: los diferentes tipos de dispositivos móviles tienen requisitos diferentes para la administración directa. Por ejemplo, para administrar dispositivos iOS, necesita un certificado del servicio de notificaciones push de Apple y, para administrar aplicaciones de un dispositivo [!INCLUDE[winblue_winrt_2](../Token/winblue_winrt_2_md.md)], necesita claves de instalación de prueba y un certificado de firma de código.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] puede administrar los siguientes dispositivos con la administración de dispositivos móviles:

    -   Apple iOS 7.1 y versiones posteriores

        > [!NOTE]
        > Los dispositivos iOS 6.0 ya inscritos permanecerán inscritos, pero los dispositivos nuevos deben ejecutar iOS versión 7.1 o posterior para poder inscribirse en Intune.

    -   Google Android 4.0 y versiones posteriores (incluido Samsung KNOX)

    -   Windows Phone 8.0 y versiones posteriores

    -   Windows RT y Windows 8.1 RT

    -   Equipos Windows 8.1 y posteriores (administrados como dispositivos móviles; véase [Funciones de administración de equipos Windows en Microsoft Intune](../Topic/Windows-PC-management-capabilities-in-Microsoft-Intune.md))

    -   Mac OS X 10.9 y versiones posteriores

    Antes de poder administrar directamente dispositivos móviles debe [Configurar la entidad de administración de dispositivos móviles como Microsoft Intune](../Topic/Set-mobile-device-management-authority-and-configure-Microsoft-Intune.md).

-   **Exchange ActiveSync**: para administrar dispositivos con Exchange ActiveSync es necesario que instale On-Premises Connector o use el conector integrado Service to Service Connector para conectarse a su servidor Exchange Server.

    Para obtener información acerca de los requisitos de hardware y software para instalar On-Premises Connector, consulte [Requisitos para On-Premises Connector](../Topic/Network-infrastructure-requirements-for-Microsoft-Intune.md#BKMK_ExchanceConnectorReqs).

    Para obtener información acerca de cómo usar On-Premises Connector o Service to Service Connector con Exchange, consulte [Configurar la administración de dispositivos móviles con Exchange ActiveSync en Microsoft Intune](../Topic/Mobile-device-management-with-Exchange-ActiveSync-and-Microsoft-Intune.md).

## Características de administración de dispositivos móviles
Intune admite la administración de dispositivos móviles de Windows Phone, iOS y Android. También admite la administración de equipos con Windows RT y Windows como dispositivos móviles.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] puede administrar los dispositivos de los usuarios, popularmente conocidos como "Bring Your Own Device" (BYOD). También puede administrar dispositivos de empresa, incluidos los escenarios donde la empresa proporciona una lista de dispositivos que los usuarios pueden elegir, conocidos como "Choose Your Own Device" (CYOD).

Puede inscribir dispositivos para satisfacer las necesidades de su organización:

|Tipo de inscripción|BYOD|CYOD|Dispositivo compartido con cuenta de administrador|Dispositivo compartido sin una cuenta de usuario|
|-----------------------|--------|--------|------------------------------------------------------|----------------------------------------------------|
|**Descripción**|Dispositivo personal inscrito mediante Microsoft Intune|Dispositivo propiedad de la organización para un solo usuario|Dispositivo propiedad de la organización que se administra con una cuenta de administrador y se comparte entre varios usuarios.|Dispositivo sin usuario propiedad de la organización utilizado por muchos usuarios.|
|**Usuario del dispositivo**|Propietario|Usuario asignado|Ninguna cuenta específica del usuario|Ningún usuario específico|
|**Quién inscribe**|Propietario|Administrador|Administrador de dispositivos|Cualquiera|
|**Que anula la inscripción**|Propietario o administrador|Administrador|Administrador|Administrador|
|**Quién puede restablecer**|Propietario o administrador|Administrador|Administrador|Administrador|
Para inscribir dispositivos móviles, debe establecer [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] como su *autoridad de dispositivo móvil* y, a continuación, configurar la infraestructura para admitir las plataformas que desea administrar. Esto requiere el establecimiento de una relación de confianza con el dispositivo.

La administración, el inventario, la implementación de aplicaciones, el aprovisionamiento y la retirada se controlan a través de la consola de administración de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Los usuarios obtienen acceso al portal de empresa que les permite instalar aplicaciones, inscribir y quitar dispositivos, y les ayuda a ponerse en contacto con su departamento de TI o departamento de soporte técnico.

Las **capacidades de la administración de dispositivos móviles (MDM)** difieren en las plataformas de dispositivos móviles, pero todas las plataformas admiten lo siguiente:

-   **Certificado, correo electrónico, perfiles de VPN y Wi-Fi.** Puede implementar perfiles de certificados en dispositivos móviles y también implementar correo electrónico, perfiles de VPN y Wi-Fi. Consulte [Habilitar el acceso a los recursos de empresa con Microsoft Intune](../Topic/Enable-access-to-company-resources-with-Microsoft-Intune---deleted.md).

-   **Administrar dispositivos iOS propiedad de la empresa** Puede configurar dispositivos para la inscripción y distribuirlos después a usuarios específicos, o bien puede inscribir dispositivos para que los puedan compartir varios usuarios. Consulte [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).

-   **Administración de aplicaciones móviles.** Las aplicaciones móviles administradas pueden configurarse para restringir ciertas operaciones de aplicaciones, como copiar y pegar, para ayudar a proteger los datos de su organización. También puede usar el explorador administrado para controlar los sitios que pueden visitar los usuarios. Consulte [Proteger datos mediante las directivas de administración de aplicaciones móviles con Microsoft Intune](../Topic/Configure-and-deploy-mobile-application-management-policies-in-the-Microsoft-Intune-console.md) y [Administrar el acceso a Internet mediante directivas de explorador administrado con Microsoft Intune](../Topic/Manage-Internet-access-using-managed-browser-policies-with-Microsoft-Intune.md).

-   **Acceso condicional.** Use las directivas de acceso condicional de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] para controlar el acceso a correo electrónico de Microsoft Exchange local desde dispositivos móviles, incluso cuando el dispositivo no se administre mediante Intune. Consulte [Administrar el acceso al correo electrónico y SharePoint con Microsoft Intune](../Topic/Manage-access-to-email-and-SharePoint-with-Microsoft-Intune.md).

-   **Las capacidades de administración de contraseñas** varían ligeramente de una plataforma para dispositivos móviles a otra, pero todas las plataformas permiten exigir una contraseña, limitar el número de intentos con error, limitar los minutos antes de que la pantalla se bloquee, establecer el plazo de expiración de una contraseña e impedir contraseñas usadas previamente.

-   **Configuración de aplicaciones.** Puede controlar la configuración del explorador y de aplicaciones, para establecer, por ejemplo, si se pueden usar tiendas de aplicaciones en los dispositivos móviles.

-   **Capacidades de dispositivo, móvil y voz.** Puede permitir o prohibir el uso de una cámara, controlar la configuración de roaming y habilitar o deshabilitar el asistente de voz de iOS y las características de marcación por voz.

-   **Restablecer códigos de acceso, bloqueo, borrar o retirar dispositivos de forma selectiva.** Puede restablecer los códigos de acceso si los usuarios dejan de tener acceso a sus dispositivos, bloquear dispositivos extraviados o robados, e incluso borrar los datos de dispositivos extraviados o robados.

## Seguridad y configuración de dispositivos

|Capacidad|Detalles|Más información|
|-------------|------------|-------------------|
|Directivas de configuración|Las directivas de configuración de dispositivos móviles permiten administrar numerosas opciones y características de los dispositivos móviles de su organización.|[Configuración de directivas de configuración de iOS en Microsoft Intune](../Topic/iOS-configuration-policy-settings-in-Microsoft-Intune.md)<br /><br />[Configuración de directivas de configuración de Android en Microsoft Intune](../Topic/Android-configuration-policy-settings-in-Microsoft-Intune.md)<br /><br />[Configuración de directivas de configuración de Windows en Microsoft Intune](../Topic/Windows-configuration-policy-settings-in-Microsoft-Intune.md)<br /><br />[Configuración de directivas de configuración de Windows Phone en Microsoft Intune](../Topic/Windows-Phone-configuration-policy-settings-in-Microsoft-Intune.md)<br /><br />[Configuración de directivas de Exchange ActiveSync en Microsoft Intune](../Topic/Exchange-ActiveSync-policy-settings-in-Microsoft-Intune.md)<br /><br />[Configuración de directivas de seguridad de dispositivos móviles en Microsoft Intune](../Topic/Mobile-device-security-policy-settings-in-Microsoft-Intune.md)|
|Directivas personalizadas|Use directivas personalizadas cuando las directivas de configuración no contengan la configuración que necesita. Para dispositivos iOS, puede importar la configuración exportada desde la herramienta Apple Configurator. Para otros dispositivos, puede usar la configuración OMA-URI para configurar opciones y características en el dispositivo.|[Configuración de directivas personalizadas de iOS en Microsoft Intune](../Topic/iOS-custom-policy-settings-in-Microsoft-Intune.md)<br /><br />[Configuración de directivas personalizadas de Android en Microsoft Intune](../Topic/Android-custom-policy-settings-in-Microsoft-Intune.md)<br /><br />[Configuración de directivas personalizadas de Windows Phone en Microsoft Intune](../Topic/Windows-Phone-custom-policy-settings-in-Microsoft-Intune.md)<br /><br />[Configuración de directivas personalizadas de Windows 10 en Microsoft Intune](../Topic/Windows-10-custom-policy-settings-in-Microsoft-Intune.md)|
|Eliminación remota, bloqueo remoto y restablecimiento de código de acceso|Borrar información confidencial tras la pérdida o el robo de un dispositivo. Por ejemplo, puede bloquear el dispositivo de forma remota, restaurar la configuración de fábrica o borrar solo los datos corporativos.|[Ayude a proteger sus datos mediante la eliminación remota, el bloqueo remoto o el restablecimiento de código de acceso mediante Microsoft Intune.](../Topic/Help-protect-your-data-with-remote-wipe,-remote-lock,-or-passcode-reset-using-Microsoft-Intune.md)|
|Modo de quiosco|Le permite bloquear determinadas características de dispositivos móviles, como la funcionalidad de captura de pantalla y el interruptor de alimentación. También le permite restringir dispositivos para que ejecuten una única aplicación que especifique.|[Configuración de directivas de configuración de iOS en Microsoft Intune](../Topic/iOS-configuration-policy-settings-in-Microsoft-Intune.md)|

## Administración de aplicaciones

|Capacidad|Detalles|Más información|
|-------------|------------|-------------------|
|Administración e implementación de aplicaciones|Proporciona diversas herramientas que le ayudarán a administrar aplicaciones móviles durante todo su ciclo de vida, incluida la implementación de aplicaciones desde archivos de instalación y tiendas de aplicaciones, la supervisión detallada del estado de las aplicaciones y la eliminación de aplicaciones.|[Implementar aplicaciones en dispositivos móviles en Microsoft Intune](../Topic/Deploy-apps-to-mobile-devices-in-Microsoft-Intune---deleted.md)|
|Aplicaciones conformes y no conformes|Le permite especificar listas de aplicaciones conformes (que los usuarios pueden instalar) y aplicaciones no conformes (que los usuarios no deben instalar).|[Configuración de directivas de configuración de iOS en Microsoft Intune](../Topic/iOS-configuration-policy-settings-in-Microsoft-Intune.md)|
|Administración de aplicaciones móviles|Configure restricciones para las aplicaciones mediante una directiva de administración de aplicaciones móviles. Esto contribuye a aumentar la seguridad de los datos de su empresa mediante la restricción de operaciones como la funcionalidad de copiar y pegar, la realización de copias de seguridad externas de los datos y la transferencia de datos entre las aplicaciones.|[Proteger datos mediante las directivas de administración de aplicaciones móviles con Microsoft Intune](../Topic/Configure-and-deploy-mobile-application-management-policies-in-the-Microsoft-Intune-console.md)<br /><br />[Preparar aplicaciones iOS para la administración de aplicaciones móviles con la herramienta de ajuste de aplicaciones de Microsoft Intune](../Topic/Prepare-iOS-apps-for-mobile-application-management-with-the-Microsoft-Intune-App-Wrapping-Tool.md)<br /><br />[Preparar aplicaciones de Android para la administración de aplicaciones móviles con Microsoft Intune App Wrapping Tool](../Topic/Prepare-Android-apps-for-mobile-application-management-with-the-Microsoft-Intune-App-Wrapping-Tool.md)<br /><br />[Aplicaciones de Microsoft que puede utilizar con las directivas de administración de aplicaciones móviles de Microsoft Intune](../Topic/Microsoft-apps-you-can-use-with-Microsoft-Intune-mobile-application-management-policies.md)|
|Explorador administrado|Tras implementar el explorador administrado para los usuarios, puede configurar una directiva de explorador administrado para controlar los sitios web que pueden visitar. Además, también puede aplicar directivas de administración de aplicaciones móviles al explorador administrado.|[Administrar el acceso a Internet mediante directivas de explorador administrado con Microsoft Intune](../Topic/Manage-Internet-access-using-managed-browser-policies-with-Microsoft-Intune.md)|

## Acceso a los recursos de la empresa

|Capacidad|Detalles|Más información|
|-------------|------------|-------------------|
|Perfiles de certificado|Permite crear e implementar perfiles de certificado de confianza y certificados de protocolo de inscripción de certificados simple (SCEP) que pueden utilizarse para ayudar a proteger y autenticar los perfiles de Wi-Fi, VPN y correo electrónico.|[Habilitar el acceso a los recursos de empresa mediante perfiles de certificados con Microsoft Intune](../Topic/Enable-access-to-company-resources-using-certificate-profiles-with-Microsoft-Intune.md)|
|Perfiles de Wi-Fi|Implementar la configuración de red inalámbrica para los usuarios. Mediante la implementación de esta configuración, se minimiza la intervención del usuario final necesaria para conectarse a la red corporativa.|[Ayudar a los usuarios a conectarse a las redes de la compañía mediante perfiles de Wi-Fi con Microsoft Intune](../Topic/Help-users-connect-to-company-networks-using-Wi-Fi-profiles-with-Microsoft-Intune.md)|
|Perfiles de correo electrónico|Crear e implementar la configuración de correo electrónico para los dispositivos. Esto permite a los usuarios obtener acceso al correo electrónico corporativo en sus dispositivos personales sin tener que realizar ninguna configuración.|[Configurar el acceso al correo electrónico corporativo mediante perfiles de correo electrónico con Microsoft Intune](../Topic/Configure-access-to-corporate-email-using-email-profiles-with-Microsoft-Intune.md)|
|Perfiles de VPN|Permite implementar la configuración de VPN a los usuarios y dispositivos de su organización. Mediante la implementación de esta configuración, se minimiza la intervención del usuario final necesaria para conectarse a los recursos de la red de la empresa.|[Ayudar a los usuarios a conectarse a su trabajo con perfiles de VPN con Microsoft Intune](../Topic/Help-users-connect-to-their-work-using-VPN-profiles-with-Microsoft-Intune.md)|
|Directivas de acceso condicional|Administre el acceso al correo electrónico de Microsoft Exchange y SharePoint Online a partir de dispositivos que no se administren con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|[Administrar el acceso al correo electrónico y SharePoint con Microsoft Intune](../Topic/Manage-access-to-email-and-SharePoint-with-Microsoft-Intune.md)|

## Inventario e informes

|Capacidad|Detalles|Más información|
|-------------|------------|-------------------|
|Inventario e informes|Obtenga información acerca de los dispositivos que usted administra y el software que estos utilizan.<br /><br />Puede filtrar estos informes de varias maneras, por ejemplo, por plataforma de dispositivo y si el dispositivo cumple las normas corporativas.|[Comprender las operaciones de Microsoft Intune mediante informes](../Topic/Understand-Microsoft-Intune-operations-by-using-reports.md)|

## Vea también
[Introducción a Microsoft Intune](../Topic/Introduction-to-Microsoft-Intune.md)
[Preparar la inscripción de dispositivos en Microsoft Intune](../Topic/Get-ready-to-enroll-devices-in-Microsoft-Intune.md)
[Administrar dispositivos móviles y equipos desde la nube](http://technet.microsoft.com/library/dn715906.aspx)
[Guía de consideraciones de diseño para Bring Your Own Device (BYOD)](http://technet.microsoft.com/library/dn656905.aspx)
[Suscríbase para disfrutar de una prueba gratuita](https://account.manage.microsoft.com/Signup/MainSignUp.aspx?OfferId=A77BE827-FC8B-4EF2-A0F5-7CD6C813AA65&ali=1)
[Cómo comprar Intune](http://technet.microsoft.com/library/dn646949.aspx)
[Introducción al uso de Microsoft Intune](../Topic/Start-using-Microsoft-Intune.md)
[Descripción del servicio Microsoft Intune](../Topic/Microsoft-Intune-Service-Description.md)
[Empezar a trabajar con una versión de prueba de 30 días de Microsoft Intune](../Topic/Get-started-with-a-30-day-trial-of-Microsoft-Intune.md)

