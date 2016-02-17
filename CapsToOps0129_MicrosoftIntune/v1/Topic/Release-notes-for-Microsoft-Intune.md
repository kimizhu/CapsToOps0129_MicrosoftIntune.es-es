---
title: Notas de la versi&#243;n para Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: db9479b2-582d-4a1a-9fbc-fbfc6c680e6f
---
# Notas de la versi&#243;n para Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ee411d41ebf4c8c648c681b9303577d1" id="tgt1" class="tgtSentence">
            <token>wit_firstref</token> es una solución de administración cliente integrada y basada en la nube que proporciona herramientas, informes y licencias de las actualizaciones más recientes de Windows. Además, ayuda a mantener los equipos actualizados y seguros.</caps:sentence>
          <caps:sentence sentenceid="4eeb80cd540c584438674fd06b445a93" id="tgt2" class="tgtSentence"> Asimismo, <token>wit_nextref</token> le permite administrar dispositivos móviles en la red mediante Exchange ActiveSync o directamente con <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence sentenceid="78eb966bc4febb19a1d11eb2233995d3" id="tgt3" class="tgtSentence"> En las siguientes Notas de la versión se describe información importante y problemas conocidos de <token>wit_firstref</token>.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="db9479b2-582d-4a1a-9fbc-fbfc6c680e6f#BKMK_WitRelnoteInstall">Installation, Deployment, and Enrollment</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="db9479b2-582d-4a1a-9fbc-fbfc6c680e6f#BKMK_WitRelnoteAlerts">Alerts</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_WitRelnoteInstall" expanded="true">
        <title>
          <caps:sentence sentenceid="a0e4f7322014c0f20506e7344cd26b5a" id="tgt4" class="tgtSentence">Instalación, implementación e inscripción</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="05b0b88fbbf67eed45031f0a201b896c" id="tgt5" class="tgtSentence">Los problemas siguientes pueden producirse durante la implementación del software cliente, la preparación del dispositivo cliente para <token>wit_firstref</token> o la inscripción del dispositivo.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="03b15ae186f90660419db25153fa0303" id="tgt6" class="tgtSentence">Cuando inscribe un dispositivo Windows 8.1 que debe autenticarse en un servidor proxy, el proceso de inscripción produce un error sin ninguna indicación visible sobre la causa del error</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="53caff112f3e3afe001c14ef0415b053" id="tgt7" class="tgtSentence">
                  <embeddedLabel>Problema:</embeddedLabel> cuando inscribe un dispositivo de <token>winblue_client_2</token> y el dispositivo se debe autenticar en un servidor proxy durante el proceso de inscripción, la inscripción produce un error si el dispositivo no ha almacenado en caché las credenciales del servidor proxy.</caps:sentence>
                <caps:sentence sentenceid="1400b193e4a0ea2a91590a1bd3edf530" id="tgt8" class="tgtSentence"> Cuando las credenciales del servidor proxy no se almacenan en la caché del dispositivo, el proceso de inscripción debe esperar a que el usuario escriba sus credenciales.</caps:sentence>
                <caps:sentence sentenceid="7fdb211dfba6e1f60bc2b245eb3f51e8" id="tgt9" class="tgtSentence"> Sin embargo, no se muestra ningún mensaje para proporcionar las credenciales del servidor proxy durante el proceso de inscripción.</caps:sentence>
                <caps:sentence sentenceid="6b4259084f46338b9865e9c6a878f24a" id="tgt10" class="tgtSentence"> El resultado es que el proceso de inscripción no se puede autenticar en el servidor proxy y no se envía ninguna indicación visible de este error al usuario.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="fa1ab3a1054eeb12e2c3a1e7549e7957" id="tgt11" class="tgtSentence">
                  <embeddedLabel>Solución:</embeddedLabel> para los dispositivos de <token>winblue_client_2</token> que deban inscribirse en una red que requiera el uso de un servidor proxy autenticado, configure y guarde las credenciales del servidor proxy antes de inscribir el dispositivo.</caps:sentence>
                <caps:sentence sentenceid="c92fb0d25d67e938dff2d0f63ba79f8f" id="tgt12" class="tgtSentence"> Para configurar y guardar las credenciales en un dispositivo con <token>winblue_client_2</token>:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt13" class="tgtSentence">En el dispositivo con <token>winblue_client_2</token>, abra <ui>Internet Explorer</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="308787c18196c23def7f892e8080a3ec" id="tgt14" class="tgtSentence">Cuando se le pidan las credenciales del servidor proxy, escríbalas y, a continuación, seleccione la opción <ui>Recordar mis credenciales</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ac43760dc82568798e506da9b81a6d00" id="tgt15" class="tgtSentence">Inscriba el dispositivo.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="a118778abc6c60daae61460fa8b55bdf" id="tgt16" class="tgtSentence">Los dispositivos Windows Phone 8.1 no podrán inscribirse en Microsoft Intune cuando la autenticación de dispositivo está habilitada en AD FS</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="1952520bc1d744fcf6554c48c4c2d8e2" id="tgt17" class="tgtSentence">
                  <embeddedLabel>Problema:</embeddedLabel> si inscribe un dispositivo de Windows Phone 8.1, la inscripción generará un error si la configuración opcional de autenticación de dispositivos está habilitada como parte de la directiva de autenticación global en los Servicios de federación de Active Directory (AD FS).</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="0fcdf79a1308d31ee0a4236b30ea46ce" id="tgt18" class="tgtSentence">
                  <embeddedLabel>Solución:</embeddedLabel> deshabilite la autenticación de dispositivos en el servidor de AD FS; para ello, desactive <ui>Habilitar autenticación de dispositivos</ui> en <ui>Editar directiva de autenticación global</ui>.</caps:sentence>
                <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt19" class="tgtSentence"> Para obtener más información, consulte <externalLink><linkText>Configuración de directivas de autenticación</linkText><linkUri>http://technet.microsoft.com/library/dn486781.aspx</linkUri></externalLink></caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="630609101c97d9f4ea693ee03c11998a" id="tgt20" class="tgtSentence">Configurar la opción "Permitir contenido para adultos en el almacén multimedia" puede afectar al modo en que se muestra la configuración del dispositivo</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="9d1a93b2a9235fa77504513a76f78140" id="tgt21" class="tgtSentence">
                  <embeddedLabel>Problema:</embeddedLabel> si una directiva de dispositivo móvil tiene configurada la opción <ui>Permitir contenido para adultos en el almacén multimedia</ui> y se aplica a un dispositivo iOS 5 o iOS 6, es posible que el estado de todas las opciones del dispositivo muestre el valor <ui>Cumple</ui>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1c4db9f1d8779c90d2a508f9de7da915" id="tgt22" class="tgtSentence">
                  <embeddedLabel>Solución:</embeddedLabel> para ver el estado correcto de la configuración del dispositivo, quite la opción <ui>Permitir contenido para adultos en el almacén multimedia</ui> de la directiva y vuelva a aplicar la configuración.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="8d5ff6241c464d8ccce8f693f7c45048" id="tgt23" class="tgtSentence">Cuando especifica directivas o aplicaciones en grupos de Microsoft Intune, los dispositivos que pertenecen al grupo Dispositivos sin agrupar no reciben la directiva ni las aplicaciones</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt24" class="tgtSentence">
                  <embeddedLabel> Problema:</embeddedLabel>
                  <token>wit_nextref</token> no aplica correctamente directivas ni aplicaciones a un dispositivo que permanece en el grupo <ui>Dispositivos sin agrupar</ui>.</caps:sentence>
                <caps:sentence sentenceid="3bceccb2a788e05a9b432b502add4941" id="tgt25" class="tgtSentence"> Esto se produce incluso cuando la directiva o la aplicación se especifica para un grupo distinto del grupo <ui>Dispositivos sin agrupar</ui>.</caps:sentence>
                <caps:sentence sentenceid="08a861bab11d62b9c19ec95e451de6b4" id="tgt26" class="tgtSentence"> No se muestra ningún error para este problema.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1ad9e5ce6afa2c554bc0f2834341e754" id="tgt27" class="tgtSentence">
                  <embeddedLabel>Solución:</embeddedLabel> quite los dispositivos del grupo <ui>Dispositivos sin agrupar</ui> y asegúrese de que permanecen como miembros de otro grupo que sí recibe directivas y aplicaciones.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="8c93342642308752737a3aedf169ed62" id="tgt28" class="tgtSentence">La herramienta de ajuste de aplicaciones de Microsoft Intune para Android no presenta ninguna capacidad de desinstalación integrada </caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="e3eeec7429afcf2f106d86cd22d3db7c" id="tgt29" class="tgtSentence">
                  <embeddedLabel>Problema:</embeddedLabel> la <ui>herramienta de ajuste de aplicaciones de Microsoft para Android</ui> no tiene funciones integradas para desinstalar la herramienta.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="6d1098e8d203e84e8dc5ac7b63d02ce0" id="tgt30" class="tgtSentence">
                  <embeddedLabel>Solución:</embeddedLabel> vaya a la ubicación donde instaló la herramienta y elimine el directorio.</caps:sentence>
                <caps:sentence sentenceid="2b6d8f5048a9469cbd3d9102c53a3818" id="tgt31" class="tgtSentence"> La ubicación predeterminada es: <ui>C:\Archivos de programa (x86)\Administración de aplicaciones móviles de Microsoft Intune\Android\Herramienta de ajuste de aplicaciones</ui>.</caps:sentence>
                <caps:sentence sentenceid="60dc279c08c23711839cebf4861a0dd5" id="tgt32" class="tgtSentence"> Para obtener más información acerca de la herramienta de ajuste de aplicaciones, consulte <externalLink><linkText>Prepare Android apps for mobile application management</linkText><linkUri>http://technet.microsoft.com/library/mt147413.aspx</linkUri></externalLink>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_WitRelnoteAlerts" expanded="true">
        <title>
          <caps:sentence sentenceid="abca7cba75e5a9ff86b1490f32891f82" id="tgt33" class="tgtSentence">Alertas</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0491e3276991f1d32a3ac0780fbb1a65" id="tgt34" class="tgtSentence">A continuación, se describen los problemas conocidos con alertas de esta versión de <token>wit_nextref</token>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="4d012850499f8a3665d0e81fc7746b24" id="tgt35" class="tgtSentence">La asistencia remota no está disponible en equipos que ejecutan Windows 8 o Windows 8.1</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="d93f87b91555f880ef01ed661eaccdd8" id="tgt36" class="tgtSentence">
                  <embeddedLabel>Problema:</embeddedLabel> en esta versión, la característica de asistencia remota no está disponible en equipos que ejecutan Windows 8 o Windows 8.1.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5d5c9df1760974a5df51f9609f380703" id="tgt37" class="tgtSentence">
                  <embeddedLabel>Solución:</embeddedLabel> ninguna</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="43990721137e2346e758067085a51961" id="tgt38" class="tgtSentence">Es posible que las notificaciones de alerta para destinatarios que se han agregado automáticamente no funcionen</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="971d3ab9b51c01eb55d5c2b66b3ed827" id="tgt39" class="tgtSentence">
                  <embeddedLabel>Problema:</embeddedLabel> Si un destinatario se agregó automáticamente a una notificación de alerta, es posible que no siempre reciba una notificación.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5d06c7d5e63993b8d2247911b9114f18" id="tgt40" class="tgtSentence">
                  <embeddedLabel>Solución alternativa:</embeddedLabel> Para asegurarse de que los destinatarios reciban la notificación de mensaje, debe agregar manualmente los destinatarios a las notificaciones de alerta.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="110cbdbf-8f9b-4c1b-9e3e-184113cd711c">Technical reference for Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">
            <token>wit_firstref</token> is an integrated, cloud-based client management solution that provides tools, reports, and upgrade licenses to the latest version of Windows, and helps keep your computers up-to-date and secure.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> In addition, <token>wit_nextref</token> lets you manage mobile devices on the network either through Exchange ActiveSync or directly through <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The following release notes describe important information and known issues in <token>wit_firstref</token>.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="db9479b2-582d-4a1a-9fbc-fbfc6c680e6f#BKMK_WitRelnoteInstall">Installation, Deployment, and Enrollment</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="db9479b2-582d-4a1a-9fbc-fbfc6c680e6f#BKMK_WitRelnoteAlerts">Alerts</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_WitRelnoteInstall" expanded="true">
        <title>
          <caps:sentence id="src4" class="srcSentence">Installation, Deployment, and Enrollment</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">The following issues can occur during client software deployment, client device preparation for <token>wit_firstref</token>, or device enrollment.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src6" class="srcSentence">When you enroll a Windows 8.1 device that must authenticate to a proxy server, the enrollment process fails with no visible indication as to the cause of the failure</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src7" class="srcSentence">
                  <embeddedLabel>Issue:</embeddedLabel>  When you enroll a <token>winblue_client_2</token> device and the device must authenticate to a proxy server during the enrollment process, the enrollment fails if the device has not cached the proxy server credentials.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> When the credentials for the proxy server are not cached on the device, the enrolment process must wait for the user to enter the credentials.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> However, the prompt to provide the proxy server credentials does not display during the enrollment process.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> The result is that the enrollment process cannot authenticate to the proxy server and there is no visible indication of this failure presented to the user.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src11" class="srcSentence">
                  <embeddedLabel>Workaround:</embeddedLabel>  For <token>winblue_client_2</token> devices that must enroll on a network that requires use of an authenticated proxy server, configure and save the credentials for the proxy server prior to enrollment of the device.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> To configure and save the credentials on a <token>winblue_client_2</token> device:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">On the <token>winblue_client_2</token> device, open <ui>Internet Explorer</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">When prompted for the proxy server credentials, enter the credentials and then select the option <ui>Remember my credentials</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">Enroll the device.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src16" class="srcSentence">Windows Phone 8.1 devices fail to enroll with Microsoft Intune when device authentication is enabled in AD FS</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src17" class="srcSentence">
                  <embeddedLabel>Issue:</embeddedLabel>  When you enroll a Windows Phone 8.1 device, enrollment fails if the optional setting for device authentication is enabled as part of global authentication policy in Active Directory Federated Services (AD FS).</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src18" class="srcSentence">
                  <embeddedLabel>Workaround:</embeddedLabel>  Disable device authentication on the AD FS server by unchecking <ui>Enable device authentication</ui> in <ui>Edit Global Authentication Policy</ui>.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> For more information, see <externalLink><linkText>Configuring Authentication Policies</linkText><linkUri>http://technet.microsoft.com/library/dn486781.aspx</linkUri></externalLink></caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src20" class="srcSentence">Configuring the “Allow adult content in media store” setting may affect how device settings display</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src21" class="srcSentence">
                  <embeddedLabel>Issue:</embeddedLabel> If a mobile device policy has the <ui>Allow adult content in media store</ui> setting configured, and is applied to an iOS 5 or iOS 6 device, the status of all settings for that device may display as <ui>Conforms</ui>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src22" class="srcSentence">
                  <embeddedLabel>Workaround:</embeddedLabel> To see the correct status of the device settings, remove the <ui>Allow adult content in media store</ui> setting from the policy, and reapply.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src23" class="srcSentence">When you specify policies or applications to Microsoft Intune groups, devices that are members of the Ungrouped Devices group do not receive policy or applications</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src24" class="srcSentence">
                  <embeddedLabel>Issue:</embeddedLabel> <token>wit_nextref</token> does not correctly apply policies and applications to a device that remains in the <ui>Ungrouped Devices</ui> group.</caps:sentence>
                <caps:sentence id="src25" class="srcSentence"> This occurs even when the policy or application is specified to a group other than the <ui>Ungrouped Devices</ui> group.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> There are no errors displayed for this problem.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src27" class="srcSentence">
                  <embeddedLabel>Workaround:</embeddedLabel> Remove the devices from the <ui>Ungrouped Devices</ui> group, and ensure the devices remain as members of at least one other group that receives policy and applications.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src28" class="srcSentence">Microsoft Intune App Wrapping Tool for Android has no built-in uninstall capability </caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src29" class="srcSentence">
                  <embeddedLabel>Issue:</embeddedLabel>  The <ui>Microsoft App Wrapping Tool for Android</ui> does not have built-in functionality for uninstalling the tool.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src30" class="srcSentence">
                  <embeddedLabel>Workaround:</embeddedLabel> Browse to the location where you installed the tool, and delete the directory.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence"> The default installation location is: <ui>C:\Program Files (x86)\Microsoft Intune Mobile Application Management\Android\App Wrapping Tool</ui>.</caps:sentence>
                <caps:sentence id="src32" class="srcSentence"> For more information about the app wrapping tool, see <externalLink><linkText>Prepare Android apps for mobile application management</linkText><linkUri>http://technet.microsoft.com/library/mt147413.aspx</linkUri></externalLink>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_WitRelnoteAlerts" expanded="true">
        <title>
          <caps:sentence id="src33" class="srcSentence">Alerts</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src34" class="srcSentence">The following are known issues with alerts in this release of <token>wit_nextref</token>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src35" class="srcSentence">Remote assistance is not available on computers that run Windows 8 or Windows 8.1</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src36" class="srcSentence">
                  <embeddedLabel>Issue:</embeddedLabel> In this release, the remote assistance feature is not available on computers that run Windows 8 or Windows 8.1.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src37" class="srcSentence">
                  <embeddedLabel>Workaround:</embeddedLabel> None.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src38" class="srcSentence">Alert notifications for recipients that are automatically added may not work</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src39" class="srcSentence">
                  <embeddedLabel>Issue:</embeddedLabel> If a recipient is automatically added to an alert notification, they may not always receive a notification.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src40" class="srcSentence">
                  <embeddedLabel>Workaround:</embeddedLabel> To make sure that recipients will receive message notification, you should manually add recipients to alert notifications.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="110cbdbf-8f9b-4c1b-9e3e-184113cd711c">Technical reference for Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>