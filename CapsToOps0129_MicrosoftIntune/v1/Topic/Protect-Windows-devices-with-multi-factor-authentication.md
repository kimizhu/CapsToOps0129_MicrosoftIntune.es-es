---
title: Proteger dispositivos Windows con la autenticaci&#243;n multifactor en Microsoft Intune
ms.custom: na
ms.prod: configuration-manager
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9b4f197d-bc10-4bee-91c9-19bcc8287d36
---
# Proteger dispositivos Windows con la autenticaci&#243;n multifactor en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="cda3e3d84142fe9ef657541162eb882f" id="tgt1" class="tgtSentence">
            <token>wit_nextref</token> integra la autenticación multifactor (MFA) para que pueda proteger mejor sus recursos corporativos al solicitar una comprobación adicional a los usuarios más allá del nombre de usuario y la contraseña (por ejemplo, con una llamada de teléfono o un mensaje de texto).</caps:sentence>
          <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt2" class="tgtSentence">
            <token>wit_nextref</token> admite el uso de MFA durante la inscripción de dispositivos Windows 8.1 (o posteriores), Windows Phone 8.1 o Windows 10 Mobile (tenga en cuenta que el requisito de MFA se puede asignar por usuario o por grupo en el servidor de ADFS).</caps:sentence>
          <caps:sentence sentenceid="73df8c200bbc31f8a620e3e4f311d17c" id="tgt3" class="tgtSentence"> Si su organización tiene una infraestructura de TI local que incluye un dominio de Active Directory con Servicios de federación de Active Directory (ADFS) configurados, puede configurar MFA en el servidor de federación y, después, habilitarla para la inscripción en <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence sentenceid="c8d8a4337607b5be0274200e19dbdb46" id="tgt4" class="tgtSentence"> Si configura MFA en el servidor de federación, pero no habilita MFA para la inscripción en <token>wit_nextref</token>, los usuarios tendrán que utilizar MFA cada vez que accedan a los recursos corporativos.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0b259e735537b10e35a55f0cb20c31c5" id="tgt5" class="tgtSentence">También puede utilizar MFA de Azure Active Directory (AAD) para exigir MFA cada vez que los usuarios accedan a los recursos corporativos. Este requisito se puede habilitar por usuario.</caps:sentence>
          <caps:sentence sentenceid="d86a1bd1ccd05708e4002c3f5dce41ff" id="tgt6" class="tgtSentence"> MFA de AAD es un servicio en la nube que no requiere ninguna infraestructura de TI local.</caps:sentence>
          <caps:sentence sentenceid="d9adea05ab017e838423772be64a3480" id="tgt7" class="tgtSentence"> Para obtener información sobre la configuración de MFA de AAD, consulte <externalLink><linkText>Adición de Multi-Factor Authentication a Azure Active Directory</linkText><linkUri>http://technet.microsoft.com/library/dn249466.aspx</linkUri></externalLink></caps:sentence>
        </para>
      </introduction>
      <section address="Reqs_MFA">
        <title>
          <caps:sentence sentenceid="a17978fcfdc98a5ed73b1ab0d8f0deac" id="tgt8" class="tgtSentence">Requisitos de infraestructura local para MFA de ADFS</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8368691819b6838404277760c32888f3" id="tgt9" class="tgtSentence">Para configurar la autenticación multifactor, necesita lo siguiente:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence sentenceid="6d28eb0315c352b12526a4612af2084e" id="tgt10" class="tgtSentence">Un dominio de Active Directory al que esté unido el servidor de ADFS.</caps:sentence>
                </embeddedLabel>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3e9b58e736d94d512dd6edd8ea37500d" id="tgt11" class="tgtSentence">
                  <embeddedLabel>n servidor de Servicios de federación de Active Directory (ADFS), configurado para MFA.</embeddedLabel> Un servidor que ejecute Windows Server 2012 R2, configurado como servidor de ADFS.</caps:sentence>
                <caps:sentence sentenceid="030f8aea112aa9436ca3c63736a381bd" id="tgt12" class="tgtSentence"> Para obtener más información, consulte: <externalLink><linkText>Usar Multi-Factor Authentication con AD FS de Windows Server 2012 R2</linkText><linkUri>http://msdn.microsoft.com/library/azure/dn807157.aspx</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="06b0cb623f2c97d422567be6b75e4386" id="tgt13" class="tgtSentence">Todos los servidores enumerados anteriormente deben cumplir los requisitos del sistema que se proporcionan en <externalLink><linkText>Requisitos del sistema e información para la instalación de Windows Server 2012 R2</linkText><linkUri>http://technet.microsoft.com/library/dn303418.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="45256369c6eaca60bf7c8f595c7f6e37" id="tgt14" class="tgtSentence">Solicitar MFA de ADFS durante la inscripción de dispositivos Windows</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f08649bf1f5a45a1e49e96035bd5b47b" id="tgt15" class="tgtSentence">Para obtener información sobre cómo habilitar MFA en ADFS, consulte <externalLink><linkText>Administrar riesgos con la autenticación adicional de Multi-Factor Authentication para aplicaciones confidenciales</linkText><linkUri>http://technet.microsoft.com/library/dn280949.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="d7d587596e49f7569850113c4d64665b" id="tgt16" class="tgtSentence">Solicitar MFA durante la inscripción en la consola de administrador de Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="72efbbb0edb0d34caaf3ef7d2fc8f145" id="tgt17" class="tgtSentence">En la consola de administración de Intune, haga clic en <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui> &gt; <ui>Multi-factor Authentication</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="e4f4a8e3f4597ea7fbd8494b77bd482c" id="tgt18" class="tgtSentence">Habilite MFA en su inquilino de Azure AD o en el entorno local antes de que necesite MFA para realizar la inscripción de dispositivos Windows en Intune.</caps:sentence>
                    <caps:sentence sentenceid="daee6794fed9a641a384f5802e40d332" id="tgt19" class="tgtSentence"> Si no lo hace, los usuarios recibirán un mensaje de error cuando intenten inscribir sus dispositivos Windows.</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence sentenceid="b290f50b49d7c05fb0211bcf149524a2" id="tgt20" class="tgtSentence">Si primero no habilita MFA en el inquilino de Azure AD antes de que se le solicite para realizar la inscripción de Intune y tiene configurada la inscripción automática de MDM durante la conexión con Azure AD, los usuarios recibirán un mensaje de error cuando intenten conectar a Azure AD sus dispositivos Windows.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt21" class="tgtSentence">Haga clic en <ui>Configurar Multi-factor Authentication</ui> y, a continuación, haga clic en <ui>Habilitar Multi-factor Authentication</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="71e0cbf3-2bfb-412e-8a12-8503df08b4cf">Protect company resources with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">
            <token>wit_nextref</token> integrates multi-factor authentication (MFA) to allow you to better secure your corporate resources by requiring additional verification from users beyond their usernames and passwords (for example, using a phone call or text message).</caps:sentence>
          <caps:sentence id="src2" class="srcSentence">
            <token>wit_nextref</token> supports the use of MFA during enrollment of Windows 8.1 or later, Windows Phone 8.1, or Windows 10 Mobile devices (and the MFA requirement can be assigned on a per-user or per-group basis on the ADFS server).</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> If your organization has on-premises IT infrastructure that includes an Active Directory domain with Active Directory Federation Services (ADFS) configured, you can configure MFA on your federation server and then enable MFA for enrollment in <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> If you configure MFA on your federation server, but you don’t enable MFA for enrollment in <token>wit_nextref</token>, users will need to use MFA each time that they access corporate resources.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">You can also use Azure Active Directory (AAD) MFA to require MFA each time that users access corporate resources, and this requirement can be enabled on a per-user basis.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> AAD MFA is a cloud service that does not require any on-premises IT infrastructure.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> To learn how to set up AAD MFA, see <externalLink><linkText>Adding Multi-Factor Authentication to Azure Active Directory.</linkText><linkUri>http://technet.microsoft.com/library/dn249466.aspx</linkUri></externalLink></caps:sentence>
        </para>
      </introduction>
      <section address="Reqs_MFA">
        <title>
          <caps:sentence id="src8" class="srcSentence">On-premises infrastructure requirements for ADFS MFA</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src9" class="srcSentence">To set up multi-factor authentication, you need:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <embeddedLabel>
                  <caps:sentence id="src10" class="srcSentence">An Active Directory domain to which the ADFS server is joined.</caps:sentence>
                </embeddedLabel>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">
                  <embeddedLabel>Active Directory Federation Services (ADFS) server, configured for MFA.</embeddedLabel> A server running Windows Server 2012 R2, set up as an ADFS server.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> For more information, see: <externalLink><linkText>Using Multi-Factor Authentication with Windows Server 2012 R2 AD FS</linkText><linkUri>http://msdn.microsoft.com/library/azure/dn807157.aspx</linkUri></externalLink></caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src13" class="srcSentence">All of the servers listed above must meet the system requirements provided in <externalLink><linkText>System Requirements and Installation Information for Windows Server 2012 R2</linkText><linkUri>http://technet.microsoft.com/library/dn303418.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Requiring ADFS MFA during enrollment of Windows devices</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">For information about how to enable MFA in ADFS, see <externalLink><linkText>Manage Risk with Additional Multi-Factor Authentication for Sensitive Applications</linkText><linkUri>http://technet.microsoft.com/library/dn280949.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src16" class="srcSentence">To require enrollment MFA in the Intune Admin Console</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">In the Intune administration console, click <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Multi-factor authentication</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Enable MFA in your Azure AD tenant or on-premises environment before you require MFA for Intune enrollment of Windows devices.</caps:sentence>
                    <caps:sentence id="src19" class="srcSentence"> If you do not, users will receive an error message when they try to enroll their Windows devices.</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence id="src20" class="srcSentence">If you do not first enable MFA in your Azure AD tenant before requiring it for Intune enrollment, and automatic MDM enrollment during Azure AD Join is configured, users will receive an error message when they attempt to Azure AD join their Windows devices.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">Click <ui>Configure Multi-factor Authentication</ui>, and then click <ui>Enable Multi-factor Authentication</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="71e0cbf3-2bfb-412e-8a12-8503df08b4cf">Protect company resources with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>