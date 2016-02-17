---
title: Administrar el acceso al correo electr&#243;nico y SharePoint con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c564d292-b83b-440d-bf08-3f5b299b7a5e
---
# Administrar el acceso al correo electr&#243;nico y SharePoint con Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5ea1dbff21eb406c22da2faad041cabe" id="tgt1" class="tgtSentence">
      Use el <ui>acceso condicional</ui> en <token>wit_firstref</token> para proteger el correo electrónico y otros servicios en función de las condiciones que especifique.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fc087165e3eee884dfd5b240d035967d" id="tgt2" class="tgtSentence">Vea este vídeo de cuatro minutos para ver una descripción general de cómo puede utilizar esta característica en su organización.</caps:sentence>
        </para>
        <mediaLink>
          <image xlink:href="3ee132cd-8505-49dc-82a7-66c314772a40"></image>
          <video player="sp_generic_640x360" videotype="single" videoid="4f914891-1913-41be-9d36-214645b27791"></video>
        </mediaLink>
        <para></para>
        <para>
          <caps:sentence sentenceid="45175056d3aa73e12e6e0c72060aebf0" id="tgt3" class="tgtSentence">A continuación se muestra un ejemplo de flujo típico de acceso condicional:</caps:sentence>
        </para>
        <mediaLink>
          <image xlink:href="17245b6f-0c9a-498d-97b9-1b801f4c0d7b"></image>
        </mediaLink>
        <para>
          <caps:sentence sentenceid="b7863a28a5b615299a2ca5b515dc3488" id="tgt4" class="tgtSentence">Use el acceso condicional para administrar el acceso a Microsoft <ui>Exchange local</ui>, <ui>Exchange Online</ui>, <ui>Exchange Online dedicado</ui>, y <ui>SharePoint Online</ui>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f86193e12d48e883eccb91faf98f4f39" id="tgt5" class="tgtSentence">Puede controlar el acceso a Exchange Online y Exchange local desde las siguientes aplicaciones de correo:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="ae3469219b07d38ed04e0465aa95bc10" id="tgt6" class="tgtSentence">La aplicación integrada para Android 4.0 y versiones posteriores, Samsung Knox 4.0 Standard y versiones posteriores</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ab2677f8da2dd8230b12c5cd630b6f68" id="tgt7" class="tgtSentence">La aplicación integrada para iOS 7.1 y versiones posteriores</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="c65d5939ab13722a0dd866236ce9f408" id="tgt8" class="tgtSentence">La aplicación integrada para Windows Phone 8.1 y versiones posteriores</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="bc3e9c61ed710a391fc73bf6792cd808" id="tgt9" class="tgtSentence">La aplicación de correo en Windows 8.1 y versiones posteriores</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="488a78fa0ee5c4d8021d3a96c8295f98" id="tgt10" class="tgtSentence">La aplicación Microsoft Outlook para Android e iOS (solo para Exchange Online)</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="980f8095ce51d6fb95b2dee9c6d78aec" id="tgt11" class="tgtSentence">Puede controlar el acceso a SharePoint Online desde las siguientes aplicaciones para plataformas que se indican:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="b888cb70de139848da1f0c2c796d83d9" id="tgt12" class="tgtSentence">Microsoft Office Mobile (Android)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f109a7d88c6f20d7dee4ebdfd54eeb86" id="tgt13" class="tgtSentence">Microsoft OneDrive (Android e iOS)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e46817072f7e0ce53882fe1c62acded8" id="tgt14" class="tgtSentence">Microsoft Word (iOS)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="27e1ca96ccbef8c07897bb61c1f6b40b" id="tgt15" class="tgtSentence">Microsoft Excel (iOS)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="223bc820d2a3cb379ba586edbb7ead3c" id="tgt16" class="tgtSentence">Microsoft PowerPoint (iOS)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="1c43deeaba61747d5cccd4e0f356839e" id="tgt17" class="tgtSentence">Microsoft OneNote (iOS)</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="8693da8a4740645d72b6de200e32ac19" id="tgt18" class="tgtSentence">Las aplicaciones de escritorio de Office pueden tener acceso a Exchange Online y SharePoint Online en equipos que ejecutan:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="715d52bfea35b434174df252d7c0058e" id="tgt19" class="tgtSentence">Aplicaciones de escritorio de Office 2013 y versiones posteriores con la <externalLink><linkText>autenticación moderna</linkText><linkUri>https://blogs.office.com/2015/03/23/office-2013-modern-authentication-public-preview-announced/</linkUri></externalLink> habilitada.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e9bcd87be6a35d0ec76364d3bb20f48c" id="tgt20" class="tgtSentence">Windows 7.0 y posterior</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="eba5da5eb654129af41865254de419df" id="tgt21" class="tgtSentence">Los equipos deben estar unidos a un dominio o ser compatibles con las directivas establecidas <token>wit_nextref</token>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="6dc9ebef48f1d752b7ee0db4e70f6468" id="tgt22" class="tgtSentence">Para implementar el acceso condicional, se configuran dos tipos de directivas en <token>wit_nextref</token>:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="579b8f51f1aabfdcd7a7c4fd9a352203" id="tgt23" class="tgtSentence">
                <ui>Las directivas de cumplimiento</ui> son directivas opcionales que se pueden implementar en usuarios y dispositivos y evaluar opciones como:</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence sentenceid="15472cd29f632e34f039403f2e635f66" id="tgt24" class="tgtSentence">Código de acceso</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence sentenceid="5bdf74912a51c34815f11e9a3d20b609" id="tgt25" class="tgtSentence">Cifrado</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence sentenceid="20254e8bd65e0e70f11991cd41058da7" id="tgt26" class="tgtSentence">Si el dispositivo está desbloqueado o modificado</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence sentenceid="e38167ab1b8f58dfe22da52218e652d5" id="tgt27" class="tgtSentence">Si el correo electrónico en el dispositivo administrado por una directiva de <token>wit_nextref</token></caps:sentence>
                </para>
              </listItem>
            </list>
            <para>
              <caps:sentence sentenceid="b1fb1c89a57499cab3898764c798190e" id="tgt28" class="tgtSentence">Si no hay ninguna directiva de cumplimiento implementada en un dispositivo, las directivas de acceso condicional aplicables tratarán el dispositivo como compatible.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0b3321101021ad2f94e5a8e2de4ff6a9" id="tgt29" class="tgtSentence">Las <ui>directivas de acceso condicional</ui> se configuran para un servicio particular y definen reglas, como las dirigidas a los grupos de usuarios de <token>wit_nextref</token> o grupos de usuarios de seguridad de Azure Active Directory, y el modo en que se administrarán los dispositivos que no se pueden inscribir con <token>wit_nextref</token>.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="78b6af95727755f530d909b9083031bd" id="tgt30" class="tgtSentence">A diferencia de otras directivas de <token>wit_nextref</token>, no se implementan directivas de acceso condicional.</caps:sentence>
              <caps:sentence sentenceid="7d0bb9503cd4f2b7bc8baf56c9740c82" id="tgt31" class="tgtSentence"> En su lugar, al configurar estas una vez, se aplicarán a todos los usuarios objetivo.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="7387a81fdfb5d5bb5c2cf82021297380" id="tgt32" class="tgtSentence">Cuando los dispositivos no cumplen las condiciones que configure, se indica al usuario el proceso que debe seguir para registrar el dispositivo en cuestión y corregir el problema que impide que cumpla los requisitos.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="7f647459281ffd7949e7a7849de46088" id="tgt33" class="tgtSentence">Introducción al acceso condicional</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e2e4ac746ff60fde090e3f38a9ba7c76" id="tgt34" class="tgtSentence">Antes de empezar a utilizar el acceso condicional, asegúrese de que tiene los requisitos adecuados en su lugar:</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="5445eb8c9421e61de2b612dd65e09d8d" id="tgt35" class="tgtSentence">El acceso condicional no funciona con dispositivos inscritos con el <externalLink><linkText>administrador de inscripción de dispositivos</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764961.aspx</linkUri></externalLink>, ya que el dispositivo no está vinculado a un usuario en Azure Active Directory.</caps:sentence>
            </para>
          </alert>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="#Exo">Exchange Online (using the shared multi-tenant environment)</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#ExoDedicated">Exchange Online Dedicated</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#ExOnPrem">Exchange On-premises</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#Spo">SharePoint Online</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#PC">Conditional Access for PCs</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="Exo">
            <title>
              <caps:sentence sentenceid="57377227262ab645f013adfa0291b1b8" id="tgt36" class="tgtSentence">Exchange Online (mediante el entorno de varios inquilinos compartido)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a64c880bfbcd7399f76a16d5e7c20f33" id="tgt37" class="tgtSentence">El acceso condicional a Exchange Online admite dispositivos que ejecutan:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e371c33cfc3f053a58994dafe8e67de2" id="tgt38" class="tgtSentence">Windows 8.1 y versiones posteriores (si cuando están inscritos con <token>wit_nextref</token>)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1de4c21610a380efcdf5586d79b2b831" id="tgt39" class="tgtSentence">Windows 7.0 o posterior (si están unidos a un dominio) </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0c22af16b4df02e420abe803e8c325e1" id="tgt40" class="tgtSentence">Windows Phone 8.1 y versiones posteriores</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a3fd80a6345c43b6f755f910e3578d3d" id="tgt41" class="tgtSentence">iOS 7.1 y versiones posteriores</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c022f0fcb0fb75f7b011c1e6f4224d0f" id="tgt42" class="tgtSentence">Android 4.0 y versiones posterior, Samsung Knox Standard 4.0 y versiones posteriores</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="622265abb6dae29b175ef6389d65a247" id="tgt43" class="tgtSentence">Además:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="01745fdb598c1b7d9f3c0255f93a63ea" id="tgt44" class="tgtSentence">Los dispositivos deben registrarse con el servicio de registro de dispositivos de Azure Active Directory (AAD DRS).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="aaa312e950e44aed9e035268fc090074" id="tgt45" class="tgtSentence">Los equipos unidos a un dominio se deben registrar automáticamente con Azure Active Directory a través de una  directiva de grupo o MSI.</caps:sentence>
                    <caps:sentence sentenceid="90adbbe7112a5ab0269194573e650cc6" id="tgt46" class="tgtSentence"> La sección <link xlink:href="#PC">Conditional Access for PCs</link> de este tema describe todos los requisitos para habilitar el acceso condicional para un equipo.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="1508d46355ec113a455792897d1ef3ff" id="tgt47" class="tgtSentence">AAD DRS se activará automáticamente para los clientes de Intune y Office 365.</caps:sentence>
                    <caps:sentence sentenceid="696997a1bc1dde5599bccbd210b0b3d8" id="tgt48" class="tgtSentence"> Los clientes que ya hayan implementado el servicio de registro de dispositivos de ADFS no podrán ver los dispositivos registrados en la instancia local de Active Directory.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c11dffc44fa55181edc4d276ee5f687b" id="tgt49" class="tgtSentence">Debe utilizar una suscripción de Office 365 que incluya Exchange Online (por ejemplo, E3) y los usuarios deben tener licencia para Exchange Online.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="65a96ea800acf77272d9e4285f72bb89" id="tgt50" class="tgtSentence">El <ui>conector de servicio a servicio de Microsoft Intune</ui> opcional conecta <token>wit_nextref</token> a Microsoft Exchange Online y hace que sea más fácil administrar información de dispositivos a través de la consola de <token>wit_nextref</token> (consulte <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Set up mobile device management using Exchange ActiveSync in Microsoft Intune</link>).</caps:sentence>
                    <caps:sentence sentenceid="10e2288f724b64e1cc7030957dc5d4b3" id="tgt51" class="tgtSentence"> No necesita usar el conector para utilizar directivas de cumplimiento ni de acceso condicional, pero sí para ejecutar informes que ayuden a evaluar el impacto del acceso condicional.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="41f4d1381de848619fb4f6834816a0ef" id="tgt52" class="tgtSentence">Si configura el conector, algunas directivas de Exchange ActiveSync de <token>wit_nextref</token> pueden verse en la consola de Office pero no se establecen como directivas predeterminadas y no afectarán a los dispositivos.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="ce5bccb5e8f71bf5232094544ae7c875" id="tgt53" class="tgtSentence">No configure el conector de servicio a servicio si piensa utilizar el acceso condicional para Exchange Online y Exchange local</caps:sentence>
                    </para>
                  </alert>
                </listItem>
              </list>
            </content>
          </section>
          <section address="ExoDedicated">
            <title>
              <caps:sentence sentenceid="43df6b136d7172bfc6b4dd4989cc5a6f" id="tgt54" class="tgtSentence">Exchange Online Dedicated</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="bb0ceb4dd3d84c4f85e0bdefb70f9cb8" id="tgt55" class="tgtSentence">El acceso condicional a Exchange Online Dedicated admite dispositivos que ejecutan:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="70fc6073bc4dfdc911a88f9c35fe4b0b" id="tgt56" class="tgtSentence">Windows 8 y versiones posteriores (cuando están inscritos con <token>wit_nextref</token>)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1de4c21610a380efcdf5586d79b2b831" id="tgt57" class="tgtSentence">Windows 7.0 o posterior (si están unidos a un dominio) </caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="1e74443970b5f2307f0e16ba10861098" id="tgt58" class="tgtSentence">Acceso condicional a equipos unidos a un dominio solo con inquilinos en el nuevo entorno dedicado de Exchange Online.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="24be3ee92f62c3c9274ca8059075f436" id="tgt59" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a2be7e81467e4c9603345595ffeda9fc" id="tgt60" class="tgtSentence">Cualquier dispositivo iOS que utilice un cliente de correo electrónico de Exchange ActiveSync (EAS)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="49b75cbc456d74e43518d6aaf643af5f" id="tgt61" class="tgtSentence">Android 4 y versiones más recientes.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a1dd131ffe64947ce9b6ed2be0b68587" id="tgt62" class="tgtSentence">Para los inquilinos en el entorno heredado de Exchange Online Dedicated:</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="b33042d475c3bf67fc260ff7386c37a6" id="tgt63" class="tgtSentence">Debe utilizar el <ui>conector de Exchange local</ui> que conecta <token>wit_nextref</token> a Microsoft Exchange local.</caps:sentence>
                    <caps:sentence sentenceid="ef48d3d0cd13e70cf075694e809a2f89" id="tgt64" class="tgtSentence"> Esto le permite administrar dispositivos a través de la consola de <token>wit_nextref</token> (consulte <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Set up mobile device management using Exchange ActiveSync in Windows Intune</link>).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1a78f989a57845ad58a4e496fb15684f" id="tgt65" class="tgtSentence">Para los inquilinos en el nuevo entorno de Exchange Online Dedicated:</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="65a96ea800acf77272d9e4285f72bb89" id="tgt66" class="tgtSentence">El <ui>conector de servicio a servicio de Microsoft Intune</ui> opcional conecta <token>wit_nextref</token> a Microsoft Exchange Online y hace que sea más fácil administrar información de dispositivos a través de la consola de <token>wit_nextref</token> (consulte <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Set up mobile device management using Exchange ActiveSync in Microsoft Intune</link>).</caps:sentence>
                    <caps:sentence sentenceid="10e2288f724b64e1cc7030957dc5d4b3" id="tgt67" class="tgtSentence"> No necesita usar el conector para utilizar directivas de cumplimiento ni de acceso condicional, pero sí para ejecutar informes que ayuden a evaluar el impacto del acceso condicional.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="7d8c46e9622c1505321f93ced720fb3c" id="tgt68" class="tgtSentence">Asegúrese de que está utilizando la versión más reciente del <ui>conector de Exchange local</ui>.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section address="ExOnPrem">
            <title>
              <caps:sentence sentenceid="ac78d1841b8e4b28fccf06905e1c3e36" id="tgt69" class="tgtSentence">Exchange local</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="f0fb09ccb3f39d91e38a58dfe238c1a7" id="tgt70" class="tgtSentence">El acceso condicional a Exchange local admite lo siguiente:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="70fc6073bc4dfdc911a88f9c35fe4b0b" id="tgt71" class="tgtSentence">Windows 8 y versiones posteriores (cuando están inscritos con <token>wit_nextref</token>)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="24be3ee92f62c3c9274ca8059075f436" id="tgt72" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a2be7e81467e4c9603345595ffeda9fc" id="tgt73" class="tgtSentence">Cualquier dispositivo iOS que utilice un cliente de correo electrónico de Exchange ActiveSync (EAS)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="49b75cbc456d74e43518d6aaf643af5f" id="tgt74" class="tgtSentence">Android 4 y versiones más recientes.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="622265abb6dae29b175ef6389d65a247" id="tgt75" class="tgtSentence">Además:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1e03b86fb8ba5b5a16d7a1ab64c5dc12" id="tgt76" class="tgtSentence">Su versión de Exchange debe ser Exchange 2010 o posterior.</caps:sentence>
                    <caps:sentence sentenceid="5cc6fd405bdd293381570628afd6dceb" id="tgt77" class="tgtSentence"> Se admite la matriz del servidor de acceso de cliente (CAS) del servidor de Exchange.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="f2d411ef02a525247d38aebd64d80138" id="tgt78" class="tgtSentence">Si su entorno de Exchange se encuentra en una configuración de servidor CAS, debe instalar el conector de Exchange local en cualquiera de los servidores CAS.</caps:sentence>
                    </para>
                  </alert>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="52a181ee41ad0096b14e6e06311ca78e" id="tgt79" class="tgtSentence">Exchange ActiveSync se puede configurar con autenticación basada en certificados o con la entrada de credenciales de usuario</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b33042d475c3bf67fc260ff7386c37a6" id="tgt80" class="tgtSentence">Debe utilizar el <ui>conector de Exchange local</ui> que conecta <token>wit_nextref</token> a Microsoft Exchange local.</caps:sentence>
                    <caps:sentence sentenceid="ef48d3d0cd13e70cf075694e809a2f89" id="tgt81" class="tgtSentence"> Esto le permite administrar dispositivos a través de la consola de <token>wit_nextref</token> (consulte <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Set up mobile device management using Exchange ActiveSync in Windows Intune</link>).</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence sentenceid="de691cac3c2e34204ce42128b729661e" id="tgt82" class="tgtSentence">Asegúrese de que está usando la versión más reciente del <ui>conector de Exchange local</ui>.</caps:sentence>
                      <caps:sentence sentenceid="08128b9291ccba92ab2a7c73bcd991c5" id="tgt83" class="tgtSentence"> El conector de Exchange local que tiene disponible en la consola de Intune es específico para su inquilino de Intune y no puede usarlo con otro inquilino.</caps:sentence>
                      <caps:sentence sentenceid="89bf14ee9a62466d8c9cc4df573d7f64" id="tgt84" class="tgtSentence"> Asimismo, también debe asegurarse de que el conector de Exchange de su inquilino está instalado en un solo equipo y no en varios.</caps:sentence>
                    </para>
                  </alert>
                </listItem>
              </list>
            </content>
          </section>
          <section address="Spo">
            <title>
              <caps:sentence sentenceid="6b89685b3aaec0e47a3b495aac387e40" id="tgt85" class="tgtSentence">SharePoint Online</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="76b799f57bf0a626aefc0ef09e20ad2f" id="tgt86" class="tgtSentence">El acceso condicional a SharePoint Online admite dispositivos que ejecutan:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e371c33cfc3f053a58994dafe8e67de2" id="tgt87" class="tgtSentence">Windows 8.1 y versiones posteriores (si cuando están inscritos con <token>wit_nextref</token>)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1de4c21610a380efcdf5586d79b2b831" id="tgt88" class="tgtSentence">Windows 7.0 o posterior (si están unidos a un dominio) </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0c22af16b4df02e420abe803e8c325e1" id="tgt89" class="tgtSentence">Windows Phone 8.1 y versiones posteriores</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="bc0eba3b995c5fd928c97d64f1223e88" id="tgt90" class="tgtSentence"> iOS 7.1 y versiones posteriores</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="789992796a71ee7950c45f57150df96c" id="tgt91" class="tgtSentence">Android 4.0 y versiones posteriores, Samsung Knox Standard 4.0 o versiones posteriores</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="622265abb6dae29b175ef6389d65a247" id="tgt92" class="tgtSentence">Además:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="01745fdb598c1b7d9f3c0255f93a63ea" id="tgt93" class="tgtSentence">Los dispositivos deben registrarse con el servicio de registro de dispositivos de Azure Active Directory (AAD DRS).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="1508d46355ec113a455792897d1ef3ff" id="tgt94" class="tgtSentence">AAD DRS se activará automáticamente para los clientes de Intune y Office 365.</caps:sentence>
                    <caps:sentence sentenceid="696997a1bc1dde5599bccbd210b0b3d8" id="tgt95" class="tgtSentence"> Los clientes que ya hayan implementado el servicio de registro de dispositivos de ADFS no podrán ver los dispositivos registrados en la instancia local de Active Directory.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="aaa312e950e44aed9e035268fc090074" id="tgt96" class="tgtSentence">Los equipos unidos a un dominio se deben registrar automáticamente con Azure Active Directory a través de una  directiva de grupo o MSI.</caps:sentence>
                    <caps:sentence sentenceid="90adbbe7112a5ab0269194573e650cc6" id="tgt97" class="tgtSentence"> La sección <link xlink:href="#PC">Conditional Access for PCs</link> de este tema describe todos los requisitos para habilitar el acceso condicional para un equipo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d7bff287591d40209c45d1984276b607" id="tgt98" class="tgtSentence">Es necesaria una suscripción de SharePoint Online y los usuarios deben tener licencia para SharePoint Online.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section address="PC">
        <title>
          <caps:sentence sentenceid="a195d47b85d167c64361582196a16980" id="tgt99" class="tgtSentence">Acceso condicional para equipos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d6d9660918eb3977b3ce3f897c1456f9" id="tgt100" class="tgtSentence">Puede configurar el acceso condicional para equipos que ejecutan aplicaciones de escritorio de Office, para que tengan acceso a <ui>Exchange Online</ui> y <ui>SharePoint Online</ui> en los equipos que cumplen los requisitos siguientes: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="4260ab8f2f2583dc32748c340b168ce8" id="tgt101" class="tgtSentence">El equipo debe ejecutar Windows 7.0 o posterior.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9fc4b1ec38b8d4022b05cf57ce9c9df3" id="tgt102" class="tgtSentence">El equipo debe estar unido a un dominio o ser compatible</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="209d5bc65e91441a1fe606576589a34f" id="tgt103" class="tgtSentence">Para ser compatible, el equipo debe estar inscrito en <token>wit_nextref</token> y cumplir las directivas.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="07f2a9d1dbb86a2aaefd874fe575d663" id="tgt104" class="tgtSentence">Los equipos unidos a un dominio deben configurarse para que <externalLink><linkText>registren automáticamente el dispositivo</linkText><linkUri>https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-automatic-device-registration-windows7/</linkUri></externalLink> con Azure Active Directory.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="061927e9a5e3a9701e406e7d34d83104" id="tgt105" class="tgtSentence">
                  <externalLink>
                    <linkText>La autenticación moderna de Office 365 debe estar habilitada</linkText>
                    <linkUri>https://blogs.office.com/2015/03/23/office-2013-modern-authentication-public-preview-announced/</linkUri>
                  </externalLink> y tener las últimas actualizaciones de Office.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e8651790ccac88836bcf0fde479eb44b" id="tgt106" class="tgtSentence">La autenticación moderna aporta inicio de sesión basado en Active Directory Authentication Library (AAL) para los clientes de Windows en Office 2013 y habilita una mejor seguridad como la <ui>autenticación multifactor</ui> y la <ui>autenticación basada en certificados</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="efd61a5c38f5d99dacb56459eb9ad70d" id="tgt107" class="tgtSentence">Configure reglas de notificaciones de ADFS para bloquear protocolos de autenticación no moderna.</caps:sentence>
                <caps:sentence sentenceid="629f74bbde293635329904ad6182d373" id="tgt108" class="tgtSentence"> Las instrucciones detalladas se describen en el Escenario 3: <externalLink><linkText>Bloquear todo el acceso externo a Office 365 excepto las aplicaciones basadas en explorador</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn592182.aspx</linkUri></externalLink>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <nextSteps>
        <content>
          <para>
            <caps:sentence sentenceid="3c3d06c9fc60c897243547b052fe7950" id="tgt109" class="tgtSentence">Lea los siguientes temas para obtener información sobre cómo configurar directivas de cumplimiento y las directivas de acceso condicional para su escenario requiere:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="0775107a-6662-41c8-9404-be14bbb599f3">Manage device compliance with compliance policies for Microsoft Intune</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="09c82f5d-531c-474d-add6-784c83f96d93">Manage email access with Microsoft Intune</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="b088e5a0-fd4a-4fe7-aa49-cb9c8cfb1585">Manage SharePoint Online access with Microsoft Intune</link>
              </para>
            </listItem>
          </list>
        </content>
      </nextSteps>
      <relatedTopics>
        <link xlink:href="71e0cbf3-2bfb-412e-8a12-8503df08b4cf">Protect company resources with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">
      Use <ui>conditional access</ui> in <token>wit_firstref</token> to help secure email and other services depending on conditions you specify.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">Watch this four minute video to see an overview of how you can use this feature in your organization.</caps:sentence>
        </para>
        <mediaLink>
          <image xlink:href="3ee132cd-8505-49dc-82a7-66c314772a40"></image>
          <video player="sp_generic_640x360" videotype="single" videoid="4f914891-1913-41be-9d36-214645b27791"></video>
        </mediaLink>
        <para></para>
        <para>
          <caps:sentence id="src3" class="srcSentence">A typical flow for conditional access might look as follows:</caps:sentence>
        </para>
        <mediaLink>
          <image xlink:href="17245b6f-0c9a-498d-97b9-1b801f4c0d7b"></image>
        </mediaLink>
        <para>
          <caps:sentence id="src4" class="srcSentence">Use conditional access to manage access to Microsoft <ui>Exchange On-premises</ui>, <ui>Exchange Online</ui>, <ui>Exchange Online Dedicated</ui>, and <ui>SharePoint Online</ui>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">You can control access to Exchange Online and Exchange On-premises from the following mail apps:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">The built-in app for Android 4.0 and later, Samsung Knox 4.0 Standard and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">The built-in app for iOS 7.1 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">The built-in app for Windows Phone 8.1 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">The mail application on Windows 8.1 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">The Microsoft Outlook app for Android and iOS (for Exchange Online only)</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src11" class="srcSentence">You can control access to SharePoint Online from the following apps for the listed platforms:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Microsoft Office Mobile (Android)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src13" class="srcSentence">Microsoft OneDrive (Android and iOS)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src14" class="srcSentence">Microsoft Word (iOS)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">Microsoft Excel (iOS)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">Microsoft PowerPoint (iOS)</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src17" class="srcSentence">Microsoft OneNote (iOS)</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src18" class="srcSentence">Office desktop applications can access Exchange Online and SharePoint Online on PCs running:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src19" class="srcSentence">Office desktop 2013 and later with <externalLink><linkText>modern authentication</linkText><linkUri>https://blogs.office.com/2015/03/23/office-2013-modern-authentication-public-preview-announced/</linkUri></externalLink> enabled.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src20" class="srcSentence">Windows 7.0 and later</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence id="src21" class="srcSentence">PCs should be domain joined or be complaint with the policies set in <token>wit_nextref</token>.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src22" class="srcSentence">To implement conditional access, you configure two policy types in <token>wit_nextref</token>:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src23" class="srcSentence">
                <ui>Compliance policies</ui> are optional policies you can deploy to users and devices and evaluate settings like:</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence id="src24" class="srcSentence">Passcode</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence id="src25" class="srcSentence">Encryption</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence id="src26" class="srcSentence">Whether the device is jailbroken or rooted</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Whether email on the device is managed by an <token>wit_nextref</token> policy</caps:sentence>
                </para>
              </listItem>
            </list>
            <para>
              <caps:sentence id="src28" class="srcSentence">If no compliance policy is deployed to a device, then any applicable conditional access policies will treat the device as compliant.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src29" class="srcSentence">
                <ui>Conditional access policies</ui> are configured for a particular service, and define rules such as which Azure Active Directory security user groups or <token>wit_nextref</token> user groups will be targeted and how devices that cannot enroll with <token>wit_nextref</token> will be managed.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src30" class="srcSentence">Unlike other <token>wit_nextref</token> policies, you do not deploy conditional access policies.</caps:sentence>
              <caps:sentence id="src31" class="srcSentence"> Instead, you configure these once, and they apply to all targeted users.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src32" class="srcSentence">When devices do not meet the conditions you configure, the user is guided though the process of enrolling the device and fixing the issue that prevents the device from being compliant.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src33" class="srcSentence">Getting started with conditional access</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src34" class="srcSentence">Before you start using conditional access, ensure that you have the correct requirements in place:</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src35" class="srcSentence">Conditional access does not work with devices enrolled with <externalLink><linkText>device enrollment manager</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764961.aspx</linkUri></externalLink> since the device is not linked to a user in Azure Active Directory.</caps:sentence>
            </para>
          </alert>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="#Exo">Exchange Online (using the shared multi-tenant environment)</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#ExoDedicated">Exchange Online Dedicated</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#ExOnPrem">Exchange On-premises</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#Spo">SharePoint Online</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#PC">Conditional Access for PCs</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="Exo">
            <title>
              <caps:sentence id="src36" class="srcSentence">Exchange Online (using the shared multi-tenant environment)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src37" class="srcSentence">Conditional access to Exchange Online supports devices that run:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Windows 8.1 and later (when enrolled with <token>wit_nextref</token>)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Windows 7.0 or later (when domain joined) </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Windows Phone 8.1 and later</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">iOS 7.1 and later</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Android 4.0 and later, Samsung Knox Standard 4.0 and later</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src43" class="srcSentence">Additionally:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Devices must be registered with the Azure Active Directory Device Registration Service (AAD DRS).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Domain joined PCs must be automatically registered with Azure Active Directory through group policy or MSI.</caps:sentence>
                    <caps:sentence id="src46" class="srcSentence"> The <link xlink:href="#PC">Conditional Access for PCs</link> section in this topic describes all the requirements for enabling conditional access for a PC.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">AAD DRS will be activated automatically for Intune and Office 365 customers.</caps:sentence>
                    <caps:sentence id="src48" class="srcSentence"> Customers who have already deployed the ADFS Device Registration Service will not see registered devices in their on-premises Active Directory.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">You must use an Office 365 subscription that includes Exchange Online (such as E3) and users must be licensed for Exchange Online.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">The optional <ui>Microsoft Intune service to service connector</ui> connects <token>wit_nextref</token> to Microsoft Exchange Online and helps you manage device information through the <token>wit_nextref</token> console (see <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Set up mobile device management using Exchange ActiveSync in Microsoft Intune</link>).</caps:sentence>
                    <caps:sentence id="src51" class="srcSentence"> You do not need to use the connector to use compliance policies or conditional access policies, but is required to run reports that help evaluate the impact of conditional access.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">If you configure the connector, some Exchange ActiveSync policies from <token>wit_nextref</token> might be visible in the Office console but are not set as default policies and do not affect devices.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src53" class="srcSentence">Do not configure the service to service connector if you intend to use conditional access for both Exchange Online and Exchange On-premises</caps:sentence>
                    </para>
                  </alert>
                </listItem>
              </list>
            </content>
          </section>
          <section address="ExoDedicated">
            <title>
              <caps:sentence id="src54" class="srcSentence">Exchange Online Dedicated</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src55" class="srcSentence">Conditional access to Exchange Online Dedicated supports devices that run:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">Windows 8 and later (when enrolled with <token>wit_nextref</token>)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">Windows 7.0 or later (when domain joined) </caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">Conditional access to domain joined PCs only to tenants in the new Exchange Online dedicated environment.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">Any iOS device that uses an Exchange ActiveSync (EAS) email client</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">Android 4 and later.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">For tenants in the legacy Exchange Online Dedicated environment:</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">You must use the <ui>on-premises Exchange connector</ui> which connects <token>wit_nextref</token> to Microsoft Exchange On-premises.</caps:sentence>
                    <caps:sentence id="src64" class="srcSentence"> This lets you manage devices through the <token>wit_nextref</token> console (see <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Set up mobile device management using Exchange ActiveSync in Windows Intune</link>).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">For tenants in the new Exchange Online Dedicated environment:</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">The optional <ui>Microsoft Intune service to service connector</ui> connects <token>wit_nextref</token> to Microsoft Exchange Online and helps you manage device information through the <token>wit_nextref</token> console (see <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Set up mobile device management using Exchange ActiveSync in Microsoft Intune</link>).</caps:sentence>
                    <caps:sentence id="src67" class="srcSentence"> You do not need to use the connector to use compliance policies or conditional access policies, but is required to run reports that help evaluate the impact of conditional access.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <alert class="important">
                <para>
                  <caps:sentence id="src68" class="srcSentence">Ensure that you are using the latest version of the <ui>on-premises Exchange connector</ui>.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section address="ExOnPrem">
            <title>
              <caps:sentence id="src69" class="srcSentence">Exchange On-premises</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src70" class="srcSentence">Conditional access to Exchange On-premises supports:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">Windows 8 and later (when enrolled with <token>wit_nextref</token>)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">Any iOS device that uses an Exchange ActiveSync (EAS) email client</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">Android 4 and later.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src75" class="srcSentence">Additionally:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src76" class="srcSentence">Your Exchange version must be Exchange 2010 or later.</caps:sentence>
                    <caps:sentence id="src77" class="srcSentence"> Exchange server Client Access Server (CAS) array is supported.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src78" class="srcSentence">If your Exchange environment is in a CAS server configuration, then you must install the on-premises Exchange connector on any one of the CAS servers.</caps:sentence>
                    </para>
                  </alert>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">Exchange ActiveSync can be configured with certificate based authentication, or user credential entry</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">You must use the <ui>on-premises Exchange connector</ui> which connects <token>wit_nextref</token> to Microsoft Exchange On-premises.</caps:sentence>
                    <caps:sentence id="src81" class="srcSentence"> This lets you manage devices through the <token>wit_nextref</token> console (see <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Set up mobile device management using Exchange ActiveSync in Windows Intune</link>).</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence id="src82" class="srcSentence">Make sure that you are using the latest version of the <ui>on-premises Exchange connector</ui>.</caps:sentence>
                      <caps:sentence id="src83" class="srcSentence"> The on-premise Exchange connector available to you in the Intune console is specific to your Intune tenant and cannot be used with any other tenant.</caps:sentence>
                      <caps:sentence id="src84" class="srcSentence"> You should also ensure that the exchange connector for your tenant is installed on exactly one machine and not on multiple machines.</caps:sentence>
                    </para>
                  </alert>
                </listItem>
              </list>
            </content>
          </section>
          <section address="Spo">
            <title>
              <caps:sentence id="src85" class="srcSentence">SharePoint Online</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src86" class="srcSentence">Conditional access to SharePoint Online supports devices that run:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">Windows 8.1 and later (when enrolled with <token>wit_nextref</token>)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">Windows 7.0 or later (when domain joined) </caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">Windows Phone 8.1 and later</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src90" class="srcSentence"> iOS 7.1 and later</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">Android 4.0 and later, Samsung Knox Standard 4.0 or later</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src92" class="srcSentence">Additionally:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">Devices must be registered with the Azure Active Directory Device Registration Service (AAD DRS).</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">AAD DRS will be activated automatically for Intune and Office 365 customers.</caps:sentence>
                    <caps:sentence id="src95" class="srcSentence"> Customers who have already deployed the ADFS Device Registration Service will not see registered devices in their on-premises Active Directory.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">Domain joined PCs must be automatically registered with Azure Active Directory through group policy or MSI.</caps:sentence>
                    <caps:sentence id="src97" class="srcSentence"> The <link xlink:href="#PC">Conditional Access for PCs</link> section in this topic describes all the requirements for enabling conditional access for a PC.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src98" class="srcSentence">A SharePoint Online subscription is required and users must be licensed for SharePoint Online.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section address="PC">
        <title>
          <caps:sentence id="src99" class="srcSentence">Conditional Access for PCs</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src100" class="srcSentence">You can setup conditional access for PCs that run Office desktop applications to access <ui>Exchange Online</ui> and <ui>SharePoint Online</ui> for PCs that meet the following requirements: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src101" class="srcSentence">The PC must be running Windows 7.0 or later.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src102" class="srcSentence">The PC must either be domain joined or compliant.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src103" class="srcSentence">In order to be compliant, the PC must be enrolled in <token>wit_nextref</token> and comply with the policies.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src104" class="srcSentence">For domain joined PCs, you must  set it up to <externalLink><linkText>automatically register the device</linkText><linkUri>https://azure.microsoft.com/en-us/documentation/articles/active-directory-conditional-access-automatic-device-registration-windows7/</linkUri></externalLink> with Azure Active Directory.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src105" class="srcSentence">
                  <externalLink>
                    <linkText>Office 365 modern authentication must be enabled</linkText>
                    <linkUri>https://blogs.office.com/2015/03/23/office-2013-modern-authentication-public-preview-announced/</linkUri>
                  </externalLink>, and have all the latest Office updates.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src106" class="srcSentence">Modern authentication brings Active Directory Authentication Library (ADAL) based sign-in to Office 2013 Windows clients and enables better security like <ui>multi-factor authentication</ui>, and <ui>certificate-based authentication</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src107" class="srcSentence">Setup ADFS claims rules to block non-modern authentication protocols.</caps:sentence>
                <caps:sentence id="src108" class="srcSentence"> Step by step instructions are detailed in scenario 3 - <externalLink><linkText>block all access to O365 except browser based applications</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn592182.aspx</linkUri></externalLink>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <nextSteps>
        <content>
          <para>
            <caps:sentence id="src109" class="srcSentence">Read the following topics to learn how to configure compliance policies and conditional access policies for your required scenario:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="0775107a-6662-41c8-9404-be14bbb599f3">Manage device compliance with compliance policies for Microsoft Intune</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="09c82f5d-531c-474d-add6-784c83f96d93">Manage email access with Microsoft Intune</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="b088e5a0-fd4a-4fe7-aa49-cb9c8cfb1585">Manage SharePoint Online access with Microsoft Intune</link>
              </para>
            </listItem>
          </list>
        </content>
      </nextSteps>
      <relatedTopics>
        <link xlink:href="71e0cbf3-2bfb-412e-8a12-8503df08b4cf">Protect company resources with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>