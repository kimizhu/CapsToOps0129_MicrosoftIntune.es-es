---
title: Introducci&#243;n a una suscripci&#243;n de pago de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: d158503c-1276-422b-ab81-5f66c1cd7e7a
---
# Introducci&#243;n a una suscripci&#243;n de pago de Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f716ac2d78f1254442bfc407cc38bfab" id="tgt1" class="tgtSentence">Tanto si empieza con una prueba gratuita de 30 días como con una suscripción de pago, Microsoft Intune proporciona una manera rápida y fácil de administrar los dispositivos móviles y equipos de su organización.</caps:sentence>
          <caps:sentence sentenceid="f629f2897971d13568d8158121caf8ac" id="tgt2" class="tgtSentence"> En este tema se muestran los pasos a seguir para configurar una instancia que solo está en la nube de <token>wit_firstref</token>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3f0f8eb313c35054af8f3ebd9d440f41" id="tgt3" class="tgtSentence">Si adquiere al menos 150 licencias de Microsoft Intune en un plan elegible, puede usar el "beneficio del Centro FastTrack", un servicio donde los especialistas en Microsoft trabajan con usted para preparar su entorno para Intune.</caps:sentence>
          <caps:sentence sentenceid="78876cede6e051df998fab51465986f4" id="tgt4" class="tgtSentence"> Consulte <externalLink><linkText>Descripción del beneficio de servicio de Microsoft Intune</linkText><linkUri>https://technet.microsoft.com/library/mt228265.aspx</linkUri></externalLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ea698d75c36b5ddbb573fc590c2af6cc" id="tgt5" class="tgtSentence">Los primeros pasos de una suscripción de pago de Intune son muy similares a los de una <externalLink><linkText>prueba gratuita de 30 días</linkText><linkUri>https://technet.microsoft.com/library/dn646983.aspx</linkUri></externalLink>.</caps:sentence>
          <caps:sentence sentenceid="f3f430b0b4fe1db481cbaa14fdd71084" id="tgt6" class="tgtSentence"> Pero en este tema también se cubren algunas áreas adicionales que la mayoría de personas no tendrán que tratar en las implementaciones de prueba, entre las que se incluyen:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="52a34a138cdcc2644f1307c4de8b8000" id="tgt7" class="tgtSentence">Sincronización de cuentas locales de Active Directory con Intune y Azure Active Directory</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="d3f0a480853d2966263d63731527f2d0" id="tgt8" class="tgtSentence">Consideraciones sobre el servicio de dominio y DNS</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8241b7ab6a781cdd9624c64f1d850f06" id="tgt9" class="tgtSentence">Personalización de las características de Intune para su uso en producción</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="e687519a6c776c73d43fb8b9d7a5c876" id="tgt10" class="tgtSentence">Este tema se centra en la configuración de Intune como servicio independiente.</caps:sentence>
            <caps:sentence sentenceid="7f03ec9164a857655b9a6d07248aef1b" id="tgt11" class="tgtSentence"> Si actualmente usa Microsoft System Center Configuration Manager (ConfigMgr) para administrar equipos y servidores, puede conectar Intune con Configuration Manager en una implementación híbrida.</caps:sentence>
            <caps:sentence sentenceid="2fa8229e6b356ee32674f426b14afaaf" id="tgt12" class="tgtSentence"> Esta configuración ofrece varias ventajas y aprovecha la infraestructura local existente.</caps:sentence>
            <caps:sentence sentenceid="78876cede6e051df998fab51465986f4" id="tgt13" class="tgtSentence"> Vea <externalLink><linkText>Administración de dispositivos móviles con Configuration Manager y Microsoft Intune</linkText><linkUri>https://technet.microsoft.com/library/jj884158.aspx</linkUri></externalLink> para obtener más información sobre las implementaciones híbridas de Intune y Configuration Manager.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="9cfdb68e3099bd19e0667068a62a3ece" id="tgt14" class="tgtSentence">Antes de comenzar</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="165d88c34b9d265d5f73fddef049af59" id="tgt15" class="tgtSentence">Empezar con una suscripción de pago significa que <externalLink><linkText>completó una versión de prueba de Intune</linkText><linkUri>https://technet.microsoft.com/library/dn646983.aspx</linkUri></externalLink> y que está listo para implementar Intune y realizar cambios en su infraestructura de red.</caps:sentence>
            <caps:sentence sentenceid="173b915621468b19e0d19a028b100f76" id="tgt16" class="tgtSentence"> Esto puede abarcar desde simplemente agregar o actualizar los registros DNS internos y externos hasta conectar sus cuentas de Active Directory a Azure Active Directory.</caps:sentence>
            <caps:sentence sentenceid="9dc1e0636c4c182bdca7ad102ca05e9d" id="tgt17" class="tgtSentence"> Cualquiera que sea la combinación de características de administración de dispositivos móviles de Intune que aproveche, deberá planear cuidadosamente la interacción de Intune con sus servicios y componentes de red.</caps:sentence>
            <caps:sentence sentenceid="427367f1bbdf1e7f2aff966210759a0e" id="tgt18" class="tgtSentence"> En concreto, debe revisar:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="a733612084a65afc1788c44f0d3c7634" id="tgt19" class="tgtSentence">
                  <legacyBold>Cómo administrará la identidad de usuario</legacyBold>: para la mayoría de organizaciones de nivel medio y nivel de empresa, la forma más conveniente de administrar la identidad de usuario con Intune es conectar los servicios de directorio existentes a Intune a través de Azure Active Directory.</caps:sentence>
                <caps:sentence sentenceid="7a06feeb6d075547cef74e7d2462ea82" id="tgt20" class="tgtSentence"> Esto es especialmente cierto si ya usa otros servicios de nube de Microsoft, como Office 365 o Exchange Online.</caps:sentence>
                <caps:sentence sentenceid="be1773f1672a72c73e5252317fea8a9c" id="tgt21" class="tgtSentence"> La sincronización de las cuentas de usuario con <externalLink><linkText>Microsoft AD Connect</linkText><linkUri>https://www.microsoft.com/download/details.aspx?id=47594</linkUri></externalLink> es una manera rápida y sencilla de conectar la instancia de Active Directory local a Azure Active Directory y configurar una experiencia de autenticación de inicio de sesión único para los usuarios.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1a600e16f64bbf2729b68547041b719b" id="tgt22" class="tgtSentence">
                  <legacyBold>Cómo se verán afectados los DNS</legacyBold>: si quiere usar un nombre de dominio personalizado en lugar del dominio onmicrosoft.com predeterminado que genera el servicio de Intune, al configurar Azure (u otros servicios en la nube de Microsoft) es necesario actualizar algunos de los registros DNS públicos.</caps:sentence>
                <caps:sentence sentenceid="917458e5c5305b3278d428fc0d3d52e9" id="tgt23" class="tgtSentence"> Los registros DNS son necesarios para que los dispositivos móviles puedan localizar el servicio Intune, así como para que otros servicios de administración de movilidad funcionen correctamente.</caps:sentence>
                <caps:sentence sentenceid="83105d1019e4891b10c085da09e8c030" id="tgt24" class="tgtSentence"> Deberá decidir si quiere administrar los registros DNS en el host DNS o dejar que Azure u Office 365 creen y administren los registros DNS de su dominio después de haberlos modificado para que apunten a estos servicios.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ae7ed9d1fdf39520344565eee2483ddf" id="tgt25" class="tgtSentence">¿Listo para comenzar?</caps:sentence>
            <caps:sentence sentenceid="3d9184f658e4cbb1cb7fe373692d2ac0" id="tgt26" class="tgtSentence"> Para iniciar la suscripción pagada a Intune, necesitará lo siguiente:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="99ed1cdd7c99b12a08652a5e99f536d5" id="tgt27" class="tgtSentence">
           Un dispositivo con un explorador web habilitado para Silverlight que pueda usar para acceder a los sitios web en los que creará las cuentas de usuario (el <embeddedLabel>Portal de cuentas de Intune</embeddedLabel>) y en los que administrará los dispositivos, los grupos y las directivas (la <embeddedLabel>Consola de administración de Intune</embeddedLabel>).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ae4a092776f33b41b5f62754fae60078" id="tgt28" class="tgtSentence">
           Otro dispositivo con un explorador web que pueda usar para acceder al portal de empresa con el fin de ver cómo la mayoría de usuarios de <token>wit_nextref</token> inscriben y administran sus dispositivos, buscan e instalan software, y solicitan ayuda a los administradores.</caps:sentence>
                <caps:sentence sentenceid="e790e06e10502d78be5d26232fae24a7" id="tgt29" class="tgtSentence"> En lugar de usar otro dispositivo con un explorador web, puede usar el ajuste “modo de privacidad” en el mismo explorador que usa para la administración de <token>wit_nextref</token> (por ejemplo: en Internet Explorer, puede hacer clic en <ui>Herramientas</ui> &gt; <ui>Exploración InPrivate</ui>).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2bd64bd32056072ed36e6355b94da5ea" id="tgt30" class="tgtSentence">
           Si tiene una cuenta de Microsoft Online Services, necesitará credenciales de administrador para esa cuenta.</caps:sentence>
                <caps:sentence sentenceid="2bdb2fb7025750b72bb4b52df58b2ccf" id="tgt31" class="tgtSentence"> Si no tiene una cuenta de este tipo o si solo quiere usar este inquilino de Intune con fines de evaluación, no necesita credenciales de administrador de inquilinos.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="84f0adeb04f20986d1e19791b19fcc7f" id="tgt32" class="tgtSentence">
           Si va a administrar dispositivos de iOS o Windows Phone con Intune, necesitará certificados (o claves) y cuentas para recuperar dichos certificados.</caps:sentence>
                <caps:sentence sentenceid="640b90b4e79487a5c7fe24cd37e44c0b" id="tgt33" class="tgtSentence"> Los dispositivos Android no necesitan certificados adicionales:</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="34a6e5d64ade17ef4e51612c50dd72f5" id="tgt34" class="tgtSentence">Plataforma</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ab3259eabfda655690d59aefca17f756" id="tgt35" class="tgtSentence">Requisitos de certificado</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt36" class="tgtSentence">Más información</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="29777c09c4d10e222863eca49091ebc0" id="tgt37" class="tgtSentence">
                   Windows Phone 8.1 y <token>winphone8_client_1</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6bda7521bfb63aa1a7c28522c299b612" id="tgt38" class="tgtSentence">No es necesario ningún certificado para los usuarios de Windows Phone 8.1 que instalen la aplicación de portal de empresa desde la Tienda.</caps:sentence>
                        <caps:sentence sentenceid="661da19850cf36eac8aca5e39277c5c7" id="tgt39" class="tgtSentence"> Se requiere un certificado Symantec en Windows Phone 8.0 o si usa Intune para implementar la aplicación de portal de empresa en dispositivos Windows Phone 8.1.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e3aaba704845ef99a933ccf191dd787d" id="tgt40" class="tgtSentence">Esta guía presupone que los usuarios obtendrán la aplicación del portal de empresa de la Tienda desde un dispositivo Windows Phone 8.1 o posterior.</caps:sentence>
                        <caps:sentence sentenceid="0f7aaa2f2b6fd4bb3d9a817353983744" id="tgt41" class="tgtSentence"> Para obtener información sobre el soporte técnico de Windows Phone 8.0, vea <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Set up Windows Phone management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="595077e2c36638f388814d08152b719a" id="tgt42" class="tgtSentence">
                  Dispositivos Windows 10, <token>winblue_winrt_2</token>, <token>win8RT_client_1</token>, o <token>winblue_client_2</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1f3406931ab09b76a2c74533fc93f405" id="tgt43" class="tgtSentence">No hay requisitos de certificado para inscribir dispositivos Windows RT y Windows.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5058f1af8388633f609cadb75a75dc9d" id="tgt44" class="tgtSentence">
                          <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be Managed by Intune</link>.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="da5d01ccbd98496aea51cdbbae671f59" id="tgt45" class="tgtSentence">iOS o Mac OS X</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b134f6982d0432a26f914236c233fc7b" id="tgt46" class="tgtSentence">Obtenga un certificado del servicio de notificaciones push de Apple.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5a7cf9300c87d3ef6ebde83a702220fb" id="tgt47" class="tgtSentence">Solicite a Apple un certificado de servicio de notificaciones push de Apple, tal como se describe a continuación: <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Start managing iOS devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </listItem>
          </list>
        </content>
      </section>
      <section address="Step1" expanded="true">
        <title>
          <caps:sentence sentenceid="6bcead0b46c85aca93b67ef043f48453" id="tgt48" class="tgtSentence">Paso 1: Registrarse o iniciar sesión en Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="300ab4a1dadb2e2153532043d8f86fa2" id="tgt49" class="tgtSentence">Antes de registrarse o iniciar sesión en Intune, debe tener en cuenta lo siguiente:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f8f79359e30aec95ee5f62ea542e076a" id="tgt50" class="tgtSentence">Si la organización ya tiene una cuenta de trabajo o académica de Microsoft Online Services</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="dad666cfe971b6a07310989948a1c7dd" id="tgt51" class="tgtSentence">Si tiene un contrato Enterprise o un contrato de licencias por volumen equivalente con Microsoft</caps:sentence>
              </para>
            </listItem>
          </list>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aca6632ac0524c927acaf39d3afec2f4" id="tgt52" class="tgtSentence">Registre una cuenta NUEVA, si cumple alguna de las siguientes opciones:</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aa5299cbcad6f25505650f207bd9d3af" id="tgt53" class="tgtSentence">Inicie sesión con su cuenta de TRABAJO o ACADÉMICA si:</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4e7727ae8c8b925ee9705bc11067aab4" id="tgt54" class="tgtSentence">
                          <embeddedLabel>No tiene una cuenta de trabajo o académica.</embeddedLabel> Se suministra una cuenta de trabajo o académica al firmar un contrato de licencias por volumen con Microsoft o suscribirse a Office 365.</caps:sentence>
                        <caps:sentence sentenceid="e97b0125d9352822ba0a00f688d4c6f6" id="tgt55" class="tgtSentence"> Si su organización no ha firmado un Contrato Enterprise o un contrato de licencias por volumen equivalente con Microsoft (o tiene una cuenta de Office 365), no dispone de una cuenta de Microsoft Online Services que pueda usar para iniciar sesión en Microsoft Online Services.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ba5573358da7ed1e06edc1a8aef7b23e" id="tgt56" class="tgtSentence">
                          <embeddedLabel>Descartará el inquilino de Intune tras completar la prueba de 30 días.</embeddedLabel> Si usa la suscripción de prueba gratuita de <token>wit_nextref</token> con fines de evaluación únicamente y tiene previsto rehacer la configuración del servicio <token>wit_nextref</token> y el aprovisionamiento de dispositivos, deberá registrarse para obtener una cuenta nueva.</caps:sentence>
                        <caps:sentence sentenceid="263586ad67d631b089612d62738606a4" id="tgt57" class="tgtSentence"> Esta es la opción recomendada si tiene la intención de usar <token>wit_nextref</token> con System Center 2012 Configuration Manager.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="important">
                    <para>
                      <caps:sentence sentenceid="985da9f53d3ceb9576fa782f2e2b32cc" id="tgt58" class="tgtSentence">Si se registra para una cuenta nueva, después no podrá utilizar una cuenta de trabajo o académica existente para administrar esa cuenta ni combinarla con contratos de licencias por volumen existentes.</caps:sentence>
                    </para>
                  </alert>
                  <para></para>
                </TD>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="3992510defc50f1858f7fc797c863e36" id="tgt59" class="tgtSentence">Tiene una cuenta de trabajo o académica suministrada con un contrato de licencias por volumen o una suscripción a Office 365 y usa esta versión de prueba para evaluar <token>wit_nextref</token>.</caps:sentence>
                    </embeddedLabel>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence sentenceid="90e4a1a311adce28bd2c892a0c552fc1" id="tgt60" class="tgtSentence">Si va a configurar <token>wit_nextref</token> en una cuenta existente, le recomendamos que consulte <link xlink:href="3b4e778d-ac13-4c23-974f-5122f74626bc">Configure Microsoft Intune</link> antes de continuar con los pasos siguientes.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
            </tbody>
          </table>
          <procedure address="BKMK_ToSignUpforSubscription" expanded="true">
            <title>
              <caps:sentence sentenceid="3555133b92fda8c56521d00deb443335" id="tgt61" class="tgtSentence">Registro o inicio de sesión en Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="11326bf9695e7dbca512166e2b4d695b" id="tgt62" class="tgtSentence">En primer lugar, <externalLink><linkText>haga clic aquí para visitar la página de registro de Intune</linkText><linkUri>https://portal.office.com/Signup/Signup.aspx?OfferId=40BE278A-DFD1-470a-9EF7-9F2596EA7FF9&amp;dl=INTUNE_A&amp;ali=1#0 </linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt63" class="tgtSentence">En la página de <ui>Registro</ui>, inicie sesión o regístrese.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="dc92e8cecf74b08b0b6e54f936a4149a" id="tgt64" class="tgtSentence">Tras completar el proceso de registro, se iniciará sesión automáticamente en la cuenta de administrador de inquilinos de <token>wit_icp_1</token>.</caps:sentence>
                  <caps:sentence sentenceid="633dd09852763b5e45ff3c99d1d76a45" id="tgt65" class="tgtSentence"> También se envía un mensaje de correo electrónico con los datos de su cuenta a la dirección de correo electrónico que especificó al realizar el registro.</caps:sentence>
                  <caps:sentence sentenceid="22c6546b4a09911ac81795315c83f234" id="tgt66" class="tgtSentence"> Este mensaje confirma que la suscripción está activa.</caps:sentence>
                  <caps:sentence sentenceid="11d3cf0f8c18164870d00e474a728f2a" id="tgt67" class="tgtSentence"> Si inicia sesión, se le dirigirá automáticamente al portal de administración de Intune.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_ConfigureDomain">
        <title>
          <caps:sentence sentenceid="f843400d1cab1ef7e3bbc6d1e5d5e4dc" id="tgt68" class="tgtSentence">Paso 2: Configurar un nombre de dominio personalizado</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e6dcdb79d138fe36d54b44d6d9d8cc9c" id="tgt69" class="tgtSentence">De manera predeterminada, <token>wit_firstref</token> usa el nombre de dominio que seleccionó al suscribirse al servicio, con el formato <ui>&lt;dominio&gt;.onmicrosoft.com</ui>.</caps:sentence>
            <caps:sentence sentenceid="77d29f97a224183330cdf5e28b6c9006" id="tgt70" class="tgtSentence"> Si su organización posee un dominio personalizado, puede configurar la instancia de <token>wit_nextref</token> para que use ese dominio en lugar del dominio proporcionado con la suscripción.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1f36783cd8fb1206de9382e358371134" id="tgt71" class="tgtSentence">Le recomendamos encarecidamente que, antes de crear nuevas cuentas de usuario o sincronizar cuentas de su instancia de Active Directory, decida si va a usar únicamente el dominio .onmicrosoft.com o va a agregar uno o más nombres de dominios personalizados.</caps:sentence>
            <caps:sentence sentenceid="9f5a5e7884f2d356ae84b03bdca1bc7f" id="tgt72" class="tgtSentence"> Si no configura un nombre de dominio y un sufijo personalizados, cada cuenta de usuario que se importe recibirá el sufijo onmicrosoft.com para el nombre principal de usuario (UPN).</caps:sentence>
            <caps:sentence sentenceid="b4e8dd211da65725cb3f6caf5fab0643" id="tgt73" class="tgtSentence"> Configurar un dominio personalizado antes de agregar usuarios puede ayudar a simplificar la administración de las identidades de usuario para la suscripción, ya que permite a los usuarios iniciar sesión con las credenciales que usan para acceder a otros recursos del dominio.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8c09db1482cf73766a199138c36f06a4" id="tgt74" class="tgtSentence">Como las tareas para configurar <token>wit_nextref</token> de forma que use el nombre de dominio personalizado de las organizaciones son las mismas que para otros inquilinos de Azure AD, use la información y los procedimientos que se describen en <externalLink><linkText>Agregar el dominio</linkText><linkUri>http://technet.microsoft.com/library/hh969247.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0a4e5fa97d40710bd3b16744cbaab497" id="tgt75" class="tgtSentence">Para obtener más información acerca del uso de un dominio personalizado con un servicio basado en la nube de Microsoft, vea <externalLink><linkText>Administración de dominios de Internet</linkText><linkUri>http://technet.microsoft.com/library/hh969248.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="9052be419f45fc5869c4f10e199e6399" id="tgt76" class="tgtSentence">Al suscribirse a un servicio basado en la nube de Microsoft, la instancia de ese servicio se convierte en un inquilino de Microsoft Azure Active Directory (Azure AD), que proporciona servicios de identidad y directorio al servicio en la nube.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="d3dec703138771807e7b767d293a65ea" id="tgt77" class="tgtSentence">Para obtener más información acerca de su inquilino de Azure AD, vea <externalLink><linkText>¿Qué es un inquilino de Windows Azure AD?</linkText><linkUri>http://technet.microsoft.com/library/jj573650.aspx</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section address="BKMK_SyncUsersFromAD">
        <title>
          <caps:sentence sentenceid="5045607049949c0d397006d501b46353" id="tgt78" class="tgtSentence">Paso 3: Sincronizar Active Directory y agregar usuarios a Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="231a8e7d7351b92281c8ca02e46b2abd" id="tgt79" class="tgtSentence">Tal como se dijo anteriormente, puede configurar la sincronización de directorios para importar las cuentas de usuario desde su instancia local de Active Directory a la administración de identidades de Microsoft Azure Active Directory.</caps:sentence>
            <caps:sentence sentenceid="181d133f3de6eb68931d1dfe9a58f135" id="tgt80" class="tgtSentence"> Además, al activar la sincronización de directorios en el inquilino de Intune, activa esta característica para todos los servicios de nube de Microsoft a los que esté suscrito.</caps:sentence>
            <caps:sentence sentenceid="ee56b69c4896f58c791a32b9c0a2bbc1" id="tgt81" class="tgtSentence"> Al utilizar varios servicios con la misma instancia de Azure AD, las cuentas de usuarios que sincronice estarán disponibles para cada servicio basado en la nube que comparta la instancia de Azure AD.</caps:sentence>
            <caps:sentence sentenceid="7639c939e65ad36c40f5f998cc768ec3" id="tgt82" class="tgtSentence"> Tener el servicio local de Active Directory conectado con todos los servicios basados en Azure Active Directory facilita la administración de identidades de usuario en gran medida.</caps:sentence>
            <caps:sentence sentenceid="2adb1a8107fdcc2bf1a4532a6990810e" id="tgt83" class="tgtSentence"> También puede configurar características de inicio de sesión único para que la experiencia de autenticación resulte fácil y familiar a los usuarios.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt84" class="tgtSentence">El <externalLink><linkText>Asistente de Azure AD Connect</linkText><linkUri>https://www.microsoft.com/download/details.aspx?id=47594</linkUri></externalLink> es la única herramienta y experiencia guiada que conectará su infraestructura de identidad local con la nube.</caps:sentence>
            <caps:sentence sentenceid="8abca209d0cfffe0304cdfbbda7b0784" id="tgt85" class="tgtSentence">  Elija la topología según sus necesidades (directorio único o varios directorios, sincronización de contraseñas o federación) y el Asistente implementará y configurará todos los componentes necesarios para preparar la conexión y ejecutarla, incluidos los servicios de sincronización, los servicios de federación de Active Directory (AD FS) y el módulo de PowerShell de Azure AD.</caps:sentence>
            <caps:sentence sentenceid="2b2dfed46a172095c09326cab33613c5" id="tgt86" class="tgtSentence"> Azure AD Connect abarca funciones que se publicaron anteriormente, como la Sincronización de directorios y la Sincronización de Azure AD.</caps:sentence>
            <caps:sentence sentenceid="2a4e636e2b4a4b06927a54e5f369f3c5" id="tgt87" class="tgtSentence"> Obtenga más información sobre la integración de directorios en <externalLink><linkText>Integración de directorios</linkText><linkUri>http://technet.microsoft.com/library/jj573653.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f139c8fc16efbd381a14906f98b0761f" id="tgt88" class="tgtSentence">Tras agregar usuarios adicionales a la suscripción de Intune, es recomendable conceder credenciales administrativas a algunas cuentas de usuario.</caps:sentence>
            <caps:sentence sentenceid="b75c325390e5e46eaa2cf1dd94a78f4a" id="tgt89" class="tgtSentence"> La consola que debe usar para asignar credenciales administrativas depende del tipo de administrador que quiera asignar:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f8b0d8601b389b7f8462d41037b2007f" id="tgt90" class="tgtSentence">
                  <embeddedLabel>Administrador de inquilinos</embeddedLabel>: para asignar este tipo de administrador y administrar su suscripción, incluida la facturación, el almacenamiento en la nube y los usuarios que pueden usar <token>wit_nextref</token>, use el <embeddedLabel><token>wit_icp_1</token></embeddedLabel>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f8b0d8601b389b7f8462d41037b2007f" id="tgt91" class="tgtSentence">
                  <embeddedLabel>Administrador de servicios</embeddedLabel>: para asignar este tipo de administrador para las tareas habituales, como la administración de dispositivos móviles o equipos, la implementación de directivas o software y la ejecución de informes, use la <embeddedLabel><token>wit_adminconsole</token></embeddedLabel>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="48fcfd6e524e106cde00ce10592035ca" id="tgt92" class="tgtSentence">Para obtener más información sobre las cuentas de administrador, vea <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268#BKMK_AdminAccounts">Intune administrator accounts</link></caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f437bb55445388dbe46c91737c36fd23" id="tgt93" class="tgtSentence">Para obtener más información sobre los beneficios de sincronizar cuentas de usuario de su directorio local con Azure AD, vea <externalLink><linkText>Similitudes entre Active Directory y Azure AD</linkText><linkUri>http://technet.microsoft.com/library/dn518177.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_AssignWitLicenses">
        <title>
          <caps:sentence sentenceid="d476bf0960d1185b667675e781df97c1" id="tgt94" class="tgtSentence">Paso 4: Administrar licencias de Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a8878429f5a079d7d8fee26e30d43fa2" id="tgt95" class="tgtSentence">Un usuario debe tener una licencia para la suscripción de Intune antes de poder iniciar sesión y usar el servicio.</caps:sentence>
            <caps:sentence sentenceid="f2c5cf56de3ad62460022b3dc0e0ba79" id="tgt96" class="tgtSentence"> Cuando los usuarios tienen una licencia, son miembros del grupo de usuarios de <token>wit_firstref</token>.</caps:sentence>
            <caps:sentence sentenceid="ccec2324b466bfe6d198134bf4d78e37" id="tgt97" class="tgtSentence"> Este grupo incluye a todos los usuarios que tienen una licencia de uso de la suscripción.</caps:sentence>
            <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt98" class="tgtSentence">
              <embeddedLabel>Cada licencia de usuario permite inscribir hasta cinco dispositivos</embeddedLabel>.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="02843a8b7395e35301dfa8c0b65ab33b" id="tgt99" class="tgtSentence">
                  <embeddedLabel>Al usar <token>wit_icp_2</token> para agregar usuarios</embeddedLabel> a la suscripción, ya sea manualmente o mediante la importación en masa mediante un archivo CSV, <token>wit_nextref</token> asigna a cada cuenta de usuario una licencia disponible.</caps:sentence>
                <caps:sentence sentenceid="754e7fb366e51055b65cae7e7452dee8" id="tgt100" class="tgtSentence"> Si no hay una licencia disponible, no se asignará la licencia.</caps:sentence>
                <caps:sentence sentenceid="e0c0b6981f09538f8916989c5257172a" id="tgt101" class="tgtSentence"> Ambos métodos ofrecen la opción de no asignar licencias a las nuevas cuentas de usuario en el momento de agregarlas a la suscripción.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fc763cb31e9938f37737394681228f83" id="tgt102" class="tgtSentence">
                  <embeddedLabel>Al importar usuarios desde la instancia local de Active Directory</embeddedLabel>, <token>wit_nextref</token> no asigna una licencia a cada cuenta de usuario.</caps:sentence>
                <caps:sentence sentenceid="90a809bd0b12df66356fd0f268b94ab8" id="tgt103" class="tgtSentence"> En su lugar, tendrá que editar posteriormente la cuenta de usuario para asignar una licencia al usuario.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d11e6e67c43a22f3ef63cd043456d758" id="tgt104" class="tgtSentence">
                  <embeddedLabel>Cuando la suscripción comparte Azure AD con otros inquilinos de Azure AD</embeddedLabel>, tiene acceso a los usuarios agregados a esos servicios.</caps:sentence>
                <caps:sentence sentenceid="1e0d34407f824106000cf3fa4baa4199" id="tgt105" class="tgtSentence"> Estos usuarios no tienen una licencia para <token>wit_nextref</token> hasta que le asigne una licencia a cada uno de ellos.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="73b2a820cad766bc267997d671921178" id="tgt106" class="tgtSentence">Si la opción de asignar o revocar una licencia de <token>wit_nextref</token> está deshabilitada, la suscripción podría incluir opciones de licencias por volumen, como las disponibles al usar <externalLink><linkText>Enterprise Mobility Suite</linkText><linkUri>http://www.microsoft.com/server-cloud/products/enterprise-mobility-suite/default.aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence sentenceid="dbd4987a06d29791f27ec90d329fa4bd" id="tgt107" class="tgtSentence"> Para obtener información acerca de cómo asignar o revocar licencias, consulte la documentación de las opciones de licencia.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="Step3" expanded="true">
        <title>
          <caps:sentence sentenceid="31825e25fe5d4f7a1a56baac9979aa83" id="tgt108" class="tgtSentence">Paso 5: Crear grupos para organizar usuarios y dispositivos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="902ce6ab3337de9d748dde1562a4cefd" id="tgt109" class="tgtSentence">Los grupos de <token>wit_nextref</token> ofrecen una gran flexibilidad para administrar los dispositivos y usuarios.</caps:sentence>
            <caps:sentence sentenceid="d706f68d2ffd6eb78c13b818e0ad5389" id="tgt110" class="tgtSentence"> Puede configurar los grupos para que se adapten a las necesidades de su organización (por ejemplo, por ubicación geográfica, departamento o características del hardware) y usarlos para realizar una amplia variedad de tareas administrativas, desde implementar directivas para un conjunto de usuarios hasta implementar aplicaciones en un conjunto de dispositivos.</caps:sentence>
          </para>
          <para></para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="8d18cc695293fda22645a516102649df" id="tgt111" class="tgtSentence">Creación de un grupo de dispositivos</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="231d3aed688848a9d9519d8935008928" id="tgt112" class="tgtSentence">Use los grupos de dispositivos para implementar aplicaciones y actualizaciones, y configurar otras características.</caps:sentence>
                <caps:sentence sentenceid="f07847ac9101417795aaf78809714773" id="tgt113" class="tgtSentence"> Por ejemplo, configure un grupo "Mis dispositivos" siguiendo estos pasos:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt114" class="tgtSentence">En la <externalLink><linkText>consola de administración de Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Grupos</ui> &gt; <ui>Información general</ui> &gt; <ui>Crear grupo</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4079902f721aa1dc05159ff969035f5d" id="tgt115" class="tgtSentence">Como <embeddedLabel>Nombre del grupo</embeddedLabel>, escriba “Mis dispositivos”; en la lista del grupo primario seleccione <embeddedLabel>Todos los dispositivos</embeddedLabel> y después haga clic en <ui>Siguiente</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt116" class="tgtSentence">En la página <ui>Definir criterios de pertenencia</ui>, seleccione <embeddedLabel>Todos los dispositivos</embeddedLabel> para indicar que el grupo incluye tanto dispositivos móviles como equipos.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt117" class="tgtSentence">En la página <ui>Definir pertenencia directa</ui>, haga clic en <embeddedLabel>Siguiente</embeddedLabel>.</caps:sentence>
                    <caps:sentence sentenceid="1fbda84ad49f7d80c56df6d391be6601" id="tgt118" class="tgtSentence"> Si previamente creó un grupo que no incluía todos los dispositivos y quería agregar dispositivos específicos al nuevo grupo, puede hacerlo aquí.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt119" class="tgtSentence">En la página <ui>Resumen</ui>, revise las acciones que se van a realizar y, a continuación, haga clic en <ui>Finalizar</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="0db75d0aec9dc01ec9aa603cd0cdce0c" id="tgt120" class="tgtSentence">El grupo que se acaba de crear se encuentra en la lista <ui>Grupos</ui>, en el área de trabajo <ui>Grupos</ui>, dentro de <embeddedLabel>Todos los dispositivos</embeddedLabel>.</caps:sentence>
                <caps:sentence sentenceid="9fbfdf7aa4c5de6ec931d6f9764a4c8f" id="tgt121" class="tgtSentence"> Aquí también puede editar o eliminar el grupo.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="2ccb91e3e9d58a5ef912a0d0e1f4d277" id="tgt122" class="tgtSentence">Creación de un grupo de usuarios</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="e5fd5c2fc49a0352228654be50d50780" id="tgt123" class="tgtSentence">Use grupos de usuarios para implementar las directivas de software y dispositivos.</caps:sentence>
                <caps:sentence sentenceid="2041d3d7fc8ba82cf5e89f85c52b9ca1" id="tgt124" class="tgtSentence"> Por ejemplo, configure un grupo "Usuarios de Intune" siguiendo estos pasos:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt125" class="tgtSentence">En la <externalLink><linkText>consola de administración de Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Grupos</ui> &gt; <ui>Información general</ui> &gt; <ui>Crear grupo</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4079902f721aa1dc05159ff969035f5d" id="tgt126" class="tgtSentence">Como <embeddedLabel>Nombre del grupo</embeddedLabel>, escriba “Usuarios de Intune”; en la lista del grupo primario seleccione <embeddedLabel>Todos los usuarios</embeddedLabel> y, después, haga clic en <ui>Siguiente</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt127" class="tgtSentence">En la página <ui>Definir criterios de pertenencia</ui>, establezca <ui>Iniciar pertenencia a grupos con</ui> en <ui>Todos los usuarios del grupo primario</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fbe61e5fb5cf7459e7f0ef57a2fda844" id="tgt128" class="tgtSentence">Al lado de <embeddedLabel>Excluir los miembros de estos grupos de seguridad</embeddedLabel>, haga clic en <embeddedLabel>Examinar</embeddedLabel> y, después, seleccione <ui>Administrador de la compañía</ui>.</caps:sentence>
                    <caps:sentence sentenceid="d60da6b920a7059eff1bb779bd6f40ed" id="tgt129" class="tgtSentence"> Esta exclusión le permite administrar el grupo de Usuarios de Intune sin que se vea afectada la cuenta de Administrador de empresa (también conocido como administrador de inquilinos).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt130" class="tgtSentence">En la página <ui>Definir pertenencia directa</ui>, haga clic en <embeddedLabel>Siguiente</embeddedLabel>.</caps:sentence>
                    <caps:sentence sentenceid="93d8eb9154df6f24f890975224ee7913" id="tgt131" class="tgtSentence"> Aquí no tiene que hacer nada, ya que desea que el grupo Usuarios de Intune incluya a todos los usuarios salvo el administrador de la empresa.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt132" class="tgtSentence">En la página <ui>Resumen</ui>, revise las acciones que se van a realizar y, a continuación, haga clic en <ui>Finalizar</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="0db75d0aec9dc01ec9aa603cd0cdce0c" id="tgt133" class="tgtSentence">El grupo que se acaba de crear se encuentra en la lista <ui>Grupos</ui>, en el área de trabajo <ui>Grupos</ui>, dentro de <embeddedLabel>Todos los usuarios</embeddedLabel>.</caps:sentence>
                <caps:sentence sentenceid="9fbfdf7aa4c5de6ec931d6f9764a4c8f" id="tgt134" class="tgtSentence"> Aquí también puede editar o eliminar el grupo.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="05c2e7401296f58eb6e552c205147831" id="tgt135" class="tgtSentence">Para obtener más información sobre el uso de grupos, consulte <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use Groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="Step4" expanded="true">
        <title>
          <caps:sentence sentenceid="fa41a4df1b867cedec3032c774bbcb49" id="tgt136" class="tgtSentence">Paso 6: Crear directivas y publicar una aplicación</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a8a321851e678a342be057ae5e30e283" id="tgt137" class="tgtSentence">Las directivas de <token>wit_nextref</token> le proporcionan una configuración que le ayuda a controlar la configuración de seguridad en dispositivos móviles, a mantener la configuración de Firewall de Windows y Endpoint Protection de los equipos, y a implementar aplicaciones.</caps:sentence>
            <caps:sentence sentenceid="24800f3018e57d504f7744979abb05f8" id="tgt138" class="tgtSentence"> Si planea usar Intune para configurar dispositivos que van a usarse en producción después de la versión de prueba, es de gran importancia que siga las instrucciones de <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Configure policy for mobile devices in Microsoft Intune</link> y <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="0843e33b7a4632e2b8eb427c5c8ead84" id="tgt139" class="tgtSentence">Puede realizar dos tipos de instalaciones de aplicación mediante Intune.</caps:sentence>
            <caps:sentence sentenceid="630af92259b34fe6e82ef27d3ec198b9" id="tgt140" class="tgtSentence"> El primer tipo es una <legacyBold>instalación requerida</legacyBold>, que implementa automáticamente la aplicación en los equipos administrados.</caps:sentence>
            <caps:sentence sentenceid="e83840104ca38273e1019a2a7b97a40b" id="tgt141" class="tgtSentence"> El segundo es una <legacyBold>instalación disponible</legacyBold>, que implementa la aplicación o un vínculo a la aplicación de portal de empresa de Intune, de forma que los usuarios pueden elegir si quieren instalarlo en sus equipos o en sus dispositivos móviles.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="566b5db6392dff724e19d4c5daa80230" id="tgt142" class="tgtSentence">Antes de usar Intune para implementar aplicaciones, asegúrese de que tiene las licencias apropiadas para publicar, distribuir y usar la aplicación.</caps:sentence>
            <caps:sentence sentenceid="fc2403706e1f4165e8bf190b1d3cd775" id="tgt143" class="tgtSentence"> El área de trabajo Licencias permite agregar y administrar información de contratos de licencias para aplicaciones o software adquiridos a través de contratos de licencias por volumen de Microsoft o de otros fabricantes adquiridos por otros medios.</caps:sentence>
            <caps:sentence sentenceid="436f3af65dce14d652d54bf6ac14200b" id="tgt144" class="tgtSentence"> Después puede crear informes de licencia que muestren la información de uso de las licencias administradas en toda la compañía y le mantengan informado de la actividad de uso de licencias.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1667acc3b4c25214b4bd1eeefede5a8a" id="tgt145" class="tgtSentence">Por medio de estos pasos, se establece una directiva de configuración de dispositivos móviles y una directiva de firewall para equipos Windows, y se configurar Skype como instalación disponible para dispositivos móviles después de haberse inscrito.</caps:sentence>
            <caps:sentence sentenceid="048ec8cd50527abfafacb47b8f27579f" id="tgt146" class="tgtSentence"> Después de agregar e implementar una nueva directiva, todos los usuarios o dispositivos del grupo en el que se ha implementado la directiva heredan la configuración como directiva de línea de base.</caps:sentence>
            <caps:sentence sentenceid="f48ccdca55207c0485aad1af701202a3" id="tgt147" class="tgtSentence"> Puede revisar y editar los detalles de estas directivas en cualquier momento más adelante desde el área de trabajo de la Directiva.</caps:sentence>
          </para>
          <procedure expanded="true">
            <title>
              <caps:sentence sentenceid="cc67870df06ef28b77e928d2e30af7f3" id="tgt148" class="tgtSentence">Creación e implementación de una directiva de configuración de dispositivo móvil</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt149" class="tgtSentence">Abra la <externalLink><linkText>consola de administración de Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a0ee12f9384564e8aed10a645e0a29eb" id="tgt150" class="tgtSentence">En el panel de la izquierda, haga clic en el icono <ui>Directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt151" class="tgtSentence">En la lista <ui>Tareas</ui> de la página <ui>Información general de directivas</ui>, haga clic en <ui>Agregar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="b38bb80f7b7f5dd9e62c7355c1d36301" id="tgt152" class="tgtSentence"> En la lista de directivas, expanda la plataforma para la que quiere crear una directiva, seleccione <ui>Configuración general</ui>, elija <ui>Crear e implementar una directiva con la configuración recomendada</ui> y haga clic en <ui>Crear directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="64aaaf966ef0bf0a24f2e1cf0a17069a" id="tgt153" class="tgtSentence">Cuando se le pida <ui>Seleccionar los grupos en los que quiere implementar esta directiva</ui>, seleccione <ui>Mis usuarios de prueba</ui> de la lista y haga clic en <ui>Agregar</ui> &gt; <ui>Aceptar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="6657cd4c2251c9914b15d124292e878a" id="tgt154" class="tgtSentence">La directiva aparecerá en la lista de directivas de configuración y se implementará al grupo <ui>Mis usuarios de pruebas</ui>.</caps:sentence>
                  <caps:sentence sentenceid="f36a7afd4ca10f6514de8a76b54b4d1f" id="tgt155" class="tgtSentence"> Haga doble clic en la directiva para ver su configuración.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="true">
            <title>
              <caps:sentence sentenceid="5af5312711de3e4154d9fd8eafca7245" id="tgt156" class="tgtSentence">Publicación de la aplicación de Skype para dispositivos móviles</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt157" class="tgtSentence">En la <externalLink><linkText>consola de administración de Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en el icono <ui>Aplicaciones</ui> y, luego, en <ui>Aplicaciones</ui> &gt; <ui>Agregar aplicación</ui>.</caps:sentence>
                    <caps:sentence sentenceid="60ab622426a76c724fa473ded4287eaa" id="tgt158" class="tgtSentence"> Si se le solicitan sus credenciales de <token>wit_nextref</token>, especifíquelas.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="0aba49aa1480b69479b1182c63e784f9" id="tgt159" class="tgtSentence">Al iniciar el <embeddedLabel>editor de software de Intune</embeddedLabel> por primera vez, se producirá una breve demora mientras se instala la aplicación.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d2c04c3bcbd23695a5a7243390ee921c" id="tgt160" class="tgtSentence">
                Revise la advertencia de seguridad y haga clic en <ui>Ejecutar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt161" class="tgtSentence">En la página <ui>Antes de comenzar</ui>, haga clic en <ui>Siguiente</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt162" class="tgtSentence">En la página <ui>Instalación de software</ui>, en <ui>Seleccionar cómo el software debe ponerse a disposición de los dispositivos</ui>, seleccione <ui>Vínculo externo</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="64dcd71bb43433626470d0d8c87e347f" id="tgt163" class="tgtSentence">Especifique el vínculo externo del software en <ui>Especificar la dirección URL</ui> y, a continuación, haga clic en <ui>Siguiente</ui>.</caps:sentence>
                    <caps:sentence sentenceid="8dbab34a42c878950bec876f4c0b902e" id="tgt164" class="tgtSentence"> Asegúrese de preceder la dirección URL con <legacyBold>http://</legacyBold>.</caps:sentence>
                    <caps:sentence sentenceid="9fb0463c4d10fb15b0a8b20b27de9c07" id="tgt165" class="tgtSentence"> Para la aplicación de Skype, use el vínculo siguiente que coincida con la plataforma de dispositivo móvil que emplea:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt166" class="tgtSentence">
                          <embeddedLabel>iOS:</embeddedLabel> <externalLink><linkText>https://itunes.apple.com/es/app/skype-for-iphone/id304878510?mt%3D8</linkText><linkUri>https://itunes.apple.com/us/app/skype-for-iphone/id304878510?mt%3D8</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt167" class="tgtSentence">
                          <embeddedLabel>Android:</embeddedLabel> <externalLink><linkText>https://play.google.com/store/apps/details?id=com.skype.raider</linkText><linkUri>https://play.google.com/store/apps/details?id=com.skype.raider</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt168" class="tgtSentence">
                          <embeddedLabel>Windows Phone 8 o Windows Phone 8.1:</embeddedLabel> <externalLink><linkText>http://www.windowsphone.com/es-es/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51</linkText><linkUri>http://www.windowsphone.com/en-us/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt169" class="tgtSentence">En la página <ui>Descripción del software</ui>, proporcione la información que desea que los usuarios vean en el portal de empresa para el software y, a continuación, haga clic en <ui>Siguiente</ui>.</caps:sentence>
                    <caps:sentence sentenceid="97f592205562199b8073000d43c71be5" id="tgt170" class="tgtSentence"> Están disponibles los siguientes valores de configuración (este ejemplo hace referencia a Skype):</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="57caaaa3def65c87f65fb4ad3d489e5a" id="tgt171" class="tgtSentence">
                          <legacyBold>Publicador</legacyBold>: escriba el nombre del publicador, "Microsoft". </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="88185ee36b2baf5e64a4a1d2e8bed743" id="tgt172" class="tgtSentence">
                          <legacyBold>Nombre</legacyBold>: escriba <embeddedLabel>Skype</embeddedLabel>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c88e9b15e88445390feb212979ffc23a" id="tgt173" class="tgtSentence">
                          <legacyBold>Descripción</legacyBold>: escriba una descripción del software, como <embeddedLabel>Aplicación de comunicación Skype</embeddedLabel>. </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="454b13ac784c57577cdf67b2b973ebbd" id="tgt174" class="tgtSentence">
                          <legacyBold>Categoría</legacyBold>: seleccione la categoría más adecuada para el software, como <embeddedLabel>Colaboración</embeddedLabel>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f90adaaebff9d5c69d792885016798b4" id="tgt175" class="tgtSentence">
                          <legacyBold>Mostrar esta aplicación como destacada y resaltarla en el portal de empresa</legacyBold>: seleccione esta opción para que, en los dispositivos móviles, la aplicación se muestre de forma destacada en el portal de empresa.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="1ebfcefd6d209280bbd536064bcaa884" id="tgt176" class="tgtSentence">
                          <legacyBold>Icono</legacyBold>: elija si quiere asociar un icono al software.</caps:sentence>
                        <caps:sentence sentenceid="7a717d29de5e56bac161ce80947323cf" id="tgt177" class="tgtSentence"> El tamaño máximo del icono es 250 x 250 píxeles.</caps:sentence>
                        <caps:sentence sentenceid="12c7d0e8fdb84868d3ba9585d87c9393" id="tgt178" class="tgtSentence"> El tamaño recomendado es 32 x 32 píxeles.</caps:sentence>
                        <caps:sentence sentenceid="375c9b99d61872ffb69176290dcb7c3a" id="tgt179" class="tgtSentence"> Este valor es opcional para el inquilino de prueba de Intune.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt180" class="tgtSentence">En la página <ui>Resumen</ui>, compruebe la información del software y, a continuación, haga clic en <ui>Cargar</ui>.</caps:sentence>
                    <caps:sentence sentenceid="9c246454e1fc1fdab04143e527678570" id="tgt181" class="tgtSentence"> Haga clic en <ui>Cerrar</ui> para salir del asistente.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt182" class="tgtSentence">En la <externalLink><linkText>consola de administración de Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Aplicaciones</ui> &gt; <ui>Aplicaciones</ui> &gt; <ui>Skype</ui> &gt; <ui>Administrar la implementación</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt183" class="tgtSentence">En la página <ui>Seleccionar grupos</ui>, seleccione <ui>Mis usuarios de prueba</ui> para implementar el software en ese grupo de usuarios y, a continuación, haga clic en <ui>Agregar</ui> &gt; <ui>Siguiente</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt184" class="tgtSentence">En la página <ui>Acción de implementación</ui>, seleccione <ui>Instalación disponible</ui> en la columna <ui>Aprobación</ui> para su grupo.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt185" class="tgtSentence">Haga clic en <ui>Finalizar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="cbc48cad1228f2bb33bc63bb8b4782ed" id="tgt186" class="tgtSentence">La aplicación Skype ahora se puede instalar en dispositivos móviles desde el portal de empresa, pero primero debe instalar el software de <token>wit_nextref</token> en equipos y dispositivos móviles.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_ConfigureCompanyPortal">
        <title>
          <caps:sentence sentenceid="46c94158fc52ea69ab26c62d21c9ba4f" id="tgt187" class="tgtSentence">Paso 7: Personalizar el portal de empresa</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt188" class="tgtSentence">El <token>wit_iwportal_1</token> es el lugar donde los usuarios acceden a los datos de la empresa y pueden realizar tareas comunes, como inscribir dispositivos, instalar aplicaciones y buscar información de ayuda del departamento de TI.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9497c9d728f416a8477d3356e0ff8828" id="tgt189" class="tgtSentence">Al personalizar el portal de empresa, los valores de configuración se aplicarán tanto al sitio web como a las aplicaciones del portal de empresa.</caps:sentence>
          </para>
          <procedure expanded="true" address="BKMK_ToCustomizeCompanyPortal">
            <title>
              <caps:sentence sentenceid="3a064b0b9e01dfff8d3958f44c342998" id="tgt190" class="tgtSentence">Configuración para personalizar el portal de empresa</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt191" class="tgtSentence">En la <externalLink><linkText>consola de administrador de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Portal de empresa</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="bc6c35cb92615f724c1e68459fef160b" id="tgt192" class="tgtSentence">Configure uno o más de los siguientes elementos opcionales.</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b06b1fdffac8a8d7f85ec0d73a8c9b4d" id="tgt193" class="tgtSentence">Área de configuración</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="bfaad773361a781112fb325b433d54f7" id="tgt194" class="tgtSentence">Nombre del campo</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="6e97c2db4d6d812002d257c5625125e9" id="tgt195" class="tgtSentence">Longitud máxima de caracteres</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt196" class="tgtSentence">Más información</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD rowspan="6">
                          <para>
                            <caps:sentence sentenceid="80f41ee55ae984604a7bd65a194d73ab" id="tgt197" class="tgtSentence">Información de contacto y declaración de privacidad de la empresa</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9bb4c85dfbafa8c61f627241bb21358c" id="tgt198" class="tgtSentence">Nombre de la empresa</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d645920e395fedad7bbbed0eca3fe2e0" id="tgt199" class="tgtSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e163c87f97ede943ecc0ad5150dfd0e2" id="tgt200" class="tgtSentence">Es el nombre que se muestra como título del portal de empresa.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="16576d71cb733d359db3b6e40b97b228" id="tgt201" class="tgtSentence">Nombre del contacto del departamento de TI</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d645920e395fedad7bbbed0eca3fe2e0" id="tgt202" class="tgtSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="974edf181ade78ffb7241bf97b9d5083" id="tgt203" class="tgtSentence">Es el nombre que se muestra en la página <ui>Contacto de TI</ui>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="965d8e507652fcc1b19d4b13823cf800" id="tgt204" class="tgtSentence">Número de teléfono del departamento de TI</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="98f13708210194c475687be6106a3b84" id="tgt205" class="tgtSentence">20</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="65e0114a82b32a48ec5af50a41b2d3df" id="tgt206" class="tgtSentence">Es el número de contacto que se muestra en la página <ui>Contacto de TI</ui>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="17301e373b6094b08e5cf38e75d1a0b3" id="tgt207" class="tgtSentence">Dirección de correo electrónico del departamento de TI</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d645920e395fedad7bbbed0eca3fe2e0" id="tgt208" class="tgtSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="31bd76e4f571d40223816e8c5f288cdf" id="tgt209" class="tgtSentence">Es la dirección de contacto que se muestra en la página <ui>Contacto de TI</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="bac5314577aa12f439fa36cf4330ab96" id="tgt210" class="tgtSentence">Debe especificar una dirección de correo electrónico válida con el formato <userInput>alias@domainname.com</userInput>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt211" class="tgtSentence">Información adicional</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="da4fb5c6e93e74d3df8527599fa62642" id="tgt212" class="tgtSentence">120</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="0a4109098d37608f6585e276d67047a8" id="tgt213" class="tgtSentence">Se muestra en la página <ui>Contacto de TI</ui>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2ddf6ec5ba19603e0bbf4dd9dd16b1c5" id="tgt214" class="tgtSentence">Dirección URL de la declaración de privacidad de la empresa</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d1fe173d08e959397adf34b1d77e88d7" id="tgt215" class="tgtSentence">79</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="175727eec4cd6ffc901ad78b72e62191" id="tgt216" class="tgtSentence">Puede especificar su propia declaración de privacidad de la empresa, que aparece cuando los usuarios hagan clic en los vínculos de privacidad del portal de empresa.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="0472d2a822cb582a87d6bb241f912301" id="tgt217" class="tgtSentence">Debe especificar una dirección URL válida con el formato <userInput>https://www.contoso.com</userInput>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD rowspan="2">
                          <para>
                            <caps:sentence sentenceid="a4a0cf3b94f4024c16574d3f299f1c1e" id="tgt218" class="tgtSentence">Contactos de soporte técnico</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a1139ec9f31e95e744ec5a994f6e15fb" id="tgt219" class="tgtSentence">Dirección URL del sitio web de soporte:</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7ef605fc8dba5425d6965fbd4c8fbe1f" id="tgt220" class="tgtSentence">150</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f77ead1287db660ad16fe436ed7c7ade" id="tgt221" class="tgtSentence">Si tiene un sitio web de soporte que desea que utilicen los usuarios finales, especifique la dirección URL aquí.</caps:sentence>
                            <caps:sentence sentenceid="e383a6033d2f9bcf460bc85f2cd9673b" id="tgt222" class="tgtSentence"> El formato de la dirección URL debe ser <userInput>https://www.contoso.com</userInput>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="69bbef7c22fdfd3a84ae3f2eb515f26f" id="tgt223" class="tgtSentence">Si no especifica una dirección URL, no se mostrará ningún sitio web de soporte en la página <ui>Contacto de TI</ui> del portal de empresa.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="ca75dc95767c2d020aba7b02bb2837c8" id="tgt224" class="tgtSentence">Nombre del sitio web</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d645920e395fedad7bbbed0eca3fe2e0" id="tgt225" class="tgtSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="100c1c9fca941c2033c1772e0757c657" id="tgt226" class="tgtSentence">Este nombre es el nombre descriptivo que se muestra para la dirección URL del sitio web de soporte.</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e63d54d32c6ef36898a448b157c2719f" id="tgt227" class="tgtSentence">Si solo especifica una dirección URL de sitio web de soporte sin nombre descriptivo, se mostrará <ui>Ir a sitio web de TI</ui> en la página <ui>Contactar con TI</ui> del portal de empresa.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD rowspan="3">
                          <para>
                            <caps:sentence sentenceid="50a04ed5229b48c39039e72dbedb84fc" id="tgt228" class="tgtSentence">Personalización</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="50806248555606b2a51599138f16c2e9" id="tgt229" class="tgtSentence">Color del tema</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4b99c13013f59eb4aa6fc87d531d9c24" id="tgt230" class="tgtSentence">No aplicable</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f14122331d56a0996b939f974850112b" id="tgt231" class="tgtSentence">Seleccione el color del tema que se aplicará al portal de empresa.</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f6c1de868188712d2b05e2f32659ccfa" id="tgt232" class="tgtSentence">Incluir el logotipo de la empresa</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4b99c13013f59eb4aa6fc87d531d9c24" id="tgt233" class="tgtSentence">No aplicable</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="86636fac9d8e40f9e61c5e7e8b5829a6" id="tgt234" class="tgtSentence">Si habilita esta opción, puede cargar el logotipo de su empresa para que se muestre en el portal de empresa.</caps:sentence>
                            <caps:sentence sentenceid="446a0243f5e7b01e37a746c71baf2c2c" id="tgt235" class="tgtSentence"> Puede cargar dos logotipos:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="9562d2823694124a4187690543d9eb87" id="tgt236" class="tgtSentence">Un logotipo que se muestra cuando el fondo del portal de empresa es blanco</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="008848a756c926fec2fd9c71caac0583" id="tgt237" class="tgtSentence">Un logotipo que se muestra cuando se utiliza para el fondo del portal de empresa el color del tema seleccionado</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <para>
                            <caps:sentence sentenceid="2df8f1bfa0cf61868ef3b080347a1f22" id="tgt238" class="tgtSentence">Cada logotipo debe ser un archivo de tipo .png o .jpg y debe cumplir los siguientes criterios:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="7350e7b91330cbbdc7f2bbc050a60650" id="tgt239" class="tgtSentence">Resolución máxima de 400 x 100 píxeles</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="8b57a9deb971de85472a4d8745ed9090" id="tgt240" class="tgtSentence">Tamaño de 750 KB como máximo</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e646bd3ec8157320c646ae3df4c64e50" id="tgt241" class="tgtSentence">Elección de un fondo para la aplicación de portal de empresa de <token>win8_client_2</token></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4b99c13013f59eb4aa6fc87d531d9c24" id="tgt242" class="tgtSentence">No aplicable</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2108e0f45b2c1cb850b5c341526c2ec7" id="tgt243" class="tgtSentence">Esta opción de configuración solo afecta al fondo de la aplicación de portal de empresa para <token>win8_client_2</token>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt244" class="tgtSentence">Haga clic en <ui>Guardar</ui> para guardar los cambios.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="4d2f1a2e8e21bffe8aafcaa7a13ec0eb" id="tgt245" class="tgtSentence">Después de guardar los cambios puede utilizar los vínculos que aparecen en la parte inferior de la página del <ui>Portal de empresa</ui> de la consola de administración para ver el sitio web del portal de empresa.</caps:sentence>
                  <caps:sentence sentenceid="0807d1e3cc22f55e2220391b59ce2c71" id="tgt246" class="tgtSentence"> Estos vínculos no se pueden cambiar.</caps:sentence>
                  <caps:sentence sentenceid="1ccb48a7b8cfc8ec25c97e4c65abffda" id="tgt247" class="tgtSentence"> Cuando un usuario inicia sesión, estos vínculos muestran las suscripciones en el portal de empresa.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="Step5" expanded="true">
        <title>
          <caps:sentence sentenceid="118a220075d9446a6e1b49bd06cbb300" id="tgt248" class="tgtSentence">Paso 8: Inscribir equipos en Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f1bad5e9b1f61c9f835fd22052613802" id="tgt249" class="tgtSentence">Puede instalar el software de cliente de <token>wit_nextref</token> en los equipos de alguna de las siguientes formas:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="ce5e33133c939503d42d666db2a6a77f" id="tgt250" class="tgtSentence">Los usuarios pueden usar un instalador proporcionado por el administrador para inscribirse manualmente</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="356464023a0325e716430b9038462c47" id="tgt251" class="tgtSentence">El software de <token>wit_nextref</token> puede incluirse en una imagen de SO o implementarse mediante la Directiva de grupo</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="977b769708b270bbc273f62413bc50df" id="tgt252" class="tgtSentence">Los usuarios finales también pueden inscribir automáticamente sus dispositivos por medio del portal de empresa de <token>wit_firstref</token></caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="32ab4153375d385b3d6ae81a309ab08b" id="tgt253" class="tgtSentence">Cada equipo inscrito está vinculado a la cuenta de usuario que se utilizó para instalar el software cliente.</caps:sentence>
            <caps:sentence sentenceid="f16e169ab1f5eb03d1a0a698bbf7b019" id="tgt254" class="tgtSentence"> Microsoft Intune Endpoint Protection también se instala de forma predeterminada durante la instalación de cliente de Intune en los equipos.</caps:sentence>
            <caps:sentence sentenceid="9eb3ae8fa9dfc080d73d3864a807557d" id="tgt255" class="tgtSentence"> Endpoint Protection contribuye a la seguridad de los equipos de su organización al proporcionar protección en tiempo real contra amenazas potenciales, mantener actualizadas las definiciones de software malintencionado y ejecutar exámenes programados automáticamente.</caps:sentence>
            <caps:sentence sentenceid="187d60fff6b2798d43e6e725ce4c63ae" id="tgt256" class="tgtSentence"> Para mayor seguridad, también puede usar las directivas de Intune para administrar la configuración de Firewall de Windows en los equipos administrados.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5c574c2ce945d8316ca01e56bb548d77" id="tgt257" class="tgtSentence">Lo que debe saber antes de empezar:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="44eb4a00219592c0f5d5ea04447be9fd" id="tgt258" class="tgtSentence">Para poder instalar el software cliente, el usuario debe ser administrador del equipo.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="adcea97639acf6a03275b132d53e528c" id="tgt259" class="tgtSentence">La inscripción automática requiere que esté instalado Internet Explorer en el equipo cliente.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f27842e450a48e7919b71487e067ea77" id="tgt260" class="tgtSentence">Cada vez que un usuario inscribe automáticamente un equipo, utiliza una licencia de <token>wit_firstref</token>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e4ee29910343259f71d5440afddefd8c" id="tgt261" class="tgtSentence">Debe utilizar una cuenta de trabajo o académica de Microsoft Online Services para inscribir automáticamente un equipo.</caps:sentence>
                <caps:sentence sentenceid="b53aa5252c8c3aee2df8e5b9e2e80ac0" id="tgt262" class="tgtSentence"> Se trata de la cuenta que utilizó para iniciar sesión o la cuenta de administrador que se creó cuando se registró para la prueba gratuita.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="2dbfdff62fdd4435252a64a08ebf83ac" id="tgt263" class="tgtSentence">En este ejemplo se usa el método de inscripción automática:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt264" class="tgtSentence">En la <externalLink><linkText>consola de administración de Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Portal de empresa</ui> y vaya al final de la pantalla.</caps:sentence>
                <caps:sentence sentenceid="869aa2e57f526dbda4a32e6b9f6cf86e" id="tgt265" class="tgtSentence"> Copie la dirección URL que se muestra en <ui>Portal de empresa de Intune</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5e760ff30358b675373f5c7e21c2a992" id="tgt266" class="tgtSentence">Utilice Internet Explorer para visitar la dirección URL del portal de empresa que adquirió en el paso anterior e inicie sesión con sus credenciales de administrador.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt267" class="tgtSentence">Haga clic en <ui>Agregar dispositivo</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt268" class="tgtSentence">Haga clic en <ui>Descargar software</ui> y, a continuación, en <ui>Ejecutar</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt269" class="tgtSentence">Haga clic en <ui>Siguiente</ui> para iniciar el Asistente para la instalación de <token>wit_firstref</token>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2cd806a671c80ccf7c83ea4a4f35260b" id="tgt270" class="tgtSentence">Cuando haya finalizado el Asistente para la instalación, haga clic en <ui>Finalizar</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ddf17fc7894cf72ade97323197b171f8" id="tgt271" class="tgtSentence">Para obtener más información acerca de la administración de equipos mediante <token>wit_nextref</token>, consulte <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be managed by Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b0e32c991dfd7befb8ebe2e54dc9b555" id="tgt272" class="tgtSentence">Para obtener más información acerca de la administración de software mediante <token>wit_nextref</token>, consulte <link xlink:href="5b49d81d-8a28-4d78-a21b-6614920a7b82">Manage software with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="Step6" expanded="true">
        <title>
          <caps:sentence sentenceid="739d06d3058bc6a82d61c01f5736959c" id="tgt273" class="tgtSentence">Paso 9: Inscribir dispositivos móviles e instalar una aplicación</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e519d541bd7bb7c411f0a650e1289f7e" id="tgt274" class="tgtSentence">Para configurar la administración de dispositivos móviles con Intune, primero debe establecer la entidad de administración de dispositivos móviles, habilitar la administración de plataformas de dispositivos e inscribir sus dispositivos con la aplicación del portal de empresa.</caps:sentence>
            <caps:sentence sentenceid="ff1d43ede2bfa6f58cd9400d72714f28" id="tgt275" class="tgtSentence"> Posteriormente, puede implementar la aplicación Microsoft Skype que publicó.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="40b0f1eb9993c21c2d628a71d3055e13" id="tgt276" class="tgtSentence">Habilitar la administración de dispositivos e inscribir dispositivos</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt277" class="tgtSentence">
                      <embeddedLabel>Convertir Intune en su entidad de administración de dispositivos móviles</embeddedLabel>
                      <br />En la <externalLink><linkText>consola de administración de Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui> y, luego, en <ui>Configurar entidad de MDM</ui> en <ui>Tareas</ui>.</caps:sentence>
                    <caps:sentence sentenceid="c0a500b8fb422e9590506aa1459c4776" id="tgt278" class="tgtSentence">  Haga clic en <ui>Sí</ui> en el cuadro de diálogo Entidad de MDM.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="200b0116ac2aa3e51d0a657cfeb83876" id="tgt279" class="tgtSentence">
                      <embeddedLabel>Habilitación de MDM para su plataforma de dispositivo</embeddedLabel>
                      <br />Habilitación de la administración de dispositivos móviles para la plataforma de dispositivo que desea administrar.</caps:sentence>
                    <caps:sentence sentenceid="f8a682d66ce3de58a2df7fd290687704" id="tgt280" class="tgtSentence"> Los requisitos necesarios varían según la plataforma:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="80219166c3d3f038c1a3799845545f82" id="tgt281" class="tgtSentence">
                          <embeddedLabel>iOS y Mac OS X</embeddedLabel>: consulte <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Set up iOS management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="80219166c3d3f038c1a3799845545f82" id="tgt282" class="tgtSentence">
                          <embeddedLabel>Windows Phone</embeddedLabel>: consulte <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Set up Windows Phone management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9d4e891992bcb69b759ec4e29264d447" id="tgt283" class="tgtSentence">
                          <embeddedLabel>Android</embeddedLabel>: los dispositivos móviles Android permiten a los usuarios inscribirse mediante la aplicación Portal de empresa, disponible en Google Play.</caps:sentence>
                        <caps:sentence sentenceid="68b2fbaa00b39392cb6dfa27deeabc8e" id="tgt284" class="tgtSentence"> No se requiere ninguna configuración adicional en Intune.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="853ae90f0351324bd73ea615e6487517" id="tgt285" class="tgtSentence">
                      <embeddedLabel>Inscribir dispositivos</embeddedLabel>:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="404587f525772cc3d94d516b0ee17bb3" id="tgt286" class="tgtSentence">
                          <embeddedLabel>Android</embeddedLabel>: instale la aplicación <ui>Portal de empresa de Intune</ui> de Microsoft Corporation, disponible en <externalLink><linkText>Google Play</linkText><linkUri>http://go.microsoft.com/fwlink/p/?LinkId=386612</linkUri></externalLink> e inicie sesión con las credenciales de usuario de Intune agregadas anteriormente.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="404587f525772cc3d94d516b0ee17bb3" id="tgt287" class="tgtSentence">
                          <embeddedLabel>iOS y Mac OS X</embeddedLabel>: instale la aplicación <ui>Portal de empresa de Microsoft Intune</ui> de Microsoft Corporation, disponible en App Store, e inicie sesión con las credenciales de usuario de Intune agregadas anteriormente.</caps:sentence>
                        <caps:sentence sentenceid="5c43821480580ddd18f45f98ae4db8e9" id="tgt288" class="tgtSentence"> Consulte <ui>Dispositivos inscritos</ui> para agregar el dispositivo.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f75132817f647ace33eee99c7949baa6" id="tgt289" class="tgtSentence">
                          <embeddedLabel>Windows Phone 8.1</embeddedLabel>: los usuarios deben instalar la aplicación <ui>Portal de empresa</ui> de Microsoft Corporation disponible en la Tienda de Windows Phone e iniciar sesión con las credenciales de usuario de Intune agregadas anteriormente.</caps:sentence>
                        <caps:sentence sentenceid="7e7309c5dc1a8a75499274c3c25077d8" id="tgt290" class="tgtSentence">  Consulte <ui>Dispositivos inscritos </ui> para agregar el dispositivo.<ui></ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="afd97dfc4973a178fd4a70c6e7c732bb" id="tgt291" class="tgtSentence">
                          <embeddedLabel>Windows Phone 8.0 </embeddedLabel>: los usuarios deben hacer clic en <ui>configuración del sistema</ui> &gt; <ui>aplicaciones de la compañía</ui> e iniciar sesión usando las credenciales de usuario de Intune agregadas anteriormente.</caps:sentence>
                        <caps:sentence sentenceid="1f802e1d645f632facd3cf39ce59a497" id="tgt292" class="tgtSentence"> La aplicación de portal de empresa se implementa en el teléfono.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="ea6a17d77b012113a5ea26c9e24e89cd" id="tgt293" class="tgtSentence">Si se le pide una <ui>dirección de servidor</ui>, escriba “manage.microsoft.com”.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="5622cde8fde107230ede3cc661406799" id="tgt294" class="tgtSentence">Abra el portal de empresa en el dispositivo móvil, seleccione <ui>Aplicaciones</ui> e instale <ui>Microsoft Skype</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence sentenceid="cf88674febdb52c69bbfc8e9942cc381" id="tgt295" class="tgtSentence">Para obtener más información acerca de la administración de dispositivos móviles mediante <token>wit_nextref</token>, consulte <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage Mobile Devices with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="485192fc8154e7a2a3fce28d1b02efa6" id="tgt296" class="tgtSentence">Tareas posteriores a la configuración</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="19e99304a48dd547e2e8deec510341d0" id="tgt297" class="tgtSentence">Después de completar los pasos de configuración inicial para una suscripción de pago de Intune, considere la posibilidad de habilitar las funciones adicionales de administración de dispositivos móviles.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f50afbaecc6fe608f03e672bd5539dd5" id="tgt298" class="tgtSentence">
                  <legacyBold>Conectar Exchange a Intune</legacyBold>: en el caso de los usuarios con dispositivos móviles que no se hayan inscrito en Intune, puede habilitar la administración de Exchange ActiveSync mediante un conector para Exchange local y para Exchange Online en Microsoft Office 365.</caps:sentence>
                <caps:sentence sentenceid="9a76b3282712c2b463d0a7d6e8043436" id="tgt299" class="tgtSentence"> Exchange Connector le conecta con la implementación de Exchange y le permite administrar los dispositivos móviles a través de la consola de administración de Intune.</caps:sentence>
                <caps:sentence sentenceid="b5b9f45bb1c4d5f850d0a730f4169533" id="tgt300" class="tgtSentence"> Para obtener más información sobre Exchange Connector, consulte <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Mobile device management with Exchange ActiveSync and Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4e0f18efba708372e43c567e31a79b2a" id="tgt301" class="tgtSentence">
                  <legacyBold>Informes de Intune</legacyBold>: Microsoft Intune proporciona alertas e informes que puede usar para supervisar los dispositivos, así como el estado de la licencia de software y las acciones que afectan a los dispositivos (por ejemplo, borrar un dispositivo).</caps:sentence>
                <caps:sentence sentenceid="f8ffa50d491d9f4257ddc1e9fc49f7d9" id="tgt302" class="tgtSentence">  Para obtener más información sobre los informes, vea <link xlink:href="0f7dc155-cb8e-477b-ba02-2623194a9575">Monitoring and reporting with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5160ef7a7a552413f3c0d40c3cf088a4" id="tgt303" class="tgtSentence">
                  <legacyBold>Proteger los recursos de la empresa</legacyBold>: una vez configurado Intune e inscritos los dispositivos, querrá asegurarse de protegerlos ante la pérdida de datos y otras amenazas.</caps:sentence>
                <caps:sentence sentenceid="43d03f893ee8f63b6db8893f31064088" id="tgt304" class="tgtSentence"> Para obtener más información sobre cómo proteger los recursos, vea <link xlink:href="71e0cbf3-2bfb-412e-8a12-8503df08b4cf">Protect company resources with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1bfd1a23-681d-4cc8-834c-c7856d69d409">Get started with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Whether you start with a 30-day free trial,  or start with a paid subscription, Microsoft Intune provides a quick and easy way for you to manage mobile devices and computers in your organization.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> This topic  leads you through the steps of setting up a cloud-only instance of <token>wit_firstref</token>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">If you purchase at least 150 licenses for Microsoft Intune in an eligible plan, you can use the "FastTrack Center Benefit," a service where Microsoft specialists work with you to get your environment ready for Intune.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> See <externalLink><linkText>Microsoft Intune Service Benefit Description</linkText><linkUri>https://technet.microsoft.com/library/mt228265.aspx</linkUri></externalLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">Getting started with a paid subscription of Intune shares many of the same steps as starting with a <externalLink><linkText>free 30-day trial</linkText><linkUri>https://technet.microsoft.com/library/dn646983.aspx</linkUri></externalLink>.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> However  in this topic, you'll also cover some additional areas that most people might not need to address in trial deployments, including:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Synchronizing on-premises Active Directory accounts with Intune and Azure Active Directory</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Domain and DNS service considerations</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Customizing Intune features for production use</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="important">
          <para>
            <caps:sentence id="src10" class="srcSentence">This topic focuses on configuring Intune as a standalone service.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> If you're currently using Microsoft System Center Configuration Manager (ConfigMgr) to manage computers and servers, you can connect Intune with ConfgMgr in a hybrid deployment.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> This configuration offers several benefits and leverages your existing on-premises infrastructure.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> See <externalLink><linkText>Manage Mobile Devices with Configuration Manager and Microsoft Intune</linkText><linkUri>https://technet.microsoft.com/library/jj884158.aspx</linkUri></externalLink> for more information about hybrid Intune and ConfigMgr deployments.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Before you begin</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">Starting with a paid subscription means that you've <externalLink><linkText>completed an Intune trial</linkText><linkUri>https://technet.microsoft.com/library/dn646983.aspx</linkUri></externalLink> and that you're ready to deploy Intune and make changes to your existing network infrastructure.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> This could range from simply adding or updating your internal and external DNS records to connecting your existing Active Directory accounts to Azure Active Directory.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> Whatever mix of Intune  mobile device management features you leverage, you'll need to  carefully plan how Intune will interact with your existing network components and services.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> Specifically, you should review:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src19" class="srcSentence">
                  <legacyBold>How you'll manage user identity</legacyBold>:  For most medium-level and enterprise-level organizations, connecting your existing directory services to Intune via Azure Active Directory is the best and most convenient way to manage user identity with Intune.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> This is especially true if you already use other Microsoft cloud services, such as Office 365 or Exchange Online.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> Synchronizing your existing user accounts using <externalLink><linkText>Microsoft's AD Connect</linkText><linkUri>https://www.microsoft.com/download/details.aspx?id=47594</linkUri></externalLink> is a quick and easy way to connect your on-premises Active Directory to Azure Active Directory and configure a single sign-on authentication experience for your users.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">
                  <legacyBold>How DNS will be impacted</legacyBold>: If you want to use your own domain name instead of the default onmicrosoft.com domain generated by the Intune service, some public DNS record updates will be needed when configuring Azure (or other Microsoft cloud services) to use your custom domain.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> DNS records are required so that mobile devices can locate the Intune service, as well as making other mobility management services work correctly.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> You'll need to decide if you want  to manage your DNS records at your DNS host  or have Azure or Office 365 create and manage the DNS records for your domain after you change your DNS records to point to these services.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src25" class="srcSentence">Ready to get started?</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> You'll need the following when starting your paid subscription to Intune:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src27" class="srcSentence">
           A device with a Silverlight-enabled web browser that you can use to access the websites where you'll  create Intune user accounts (the <embeddedLabel>Intune Account Portal</embeddedLabel>) and where you'll manage devices, groups, and policies  (the <embeddedLabel>Intune administration console</embeddedLabel>).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src28" class="srcSentence">
           A second device with a web browser, which you can use to access the company portal to see how most <token>wit_nextref</token> users will enroll and manage their devices, find and install software, and request help from administrators.</caps:sentence>
                <caps:sentence id="src29" class="srcSentence"> Instead of using a second device with a web browser, you can use the “privacy mode” setting on the same browser that you use for <token>wit_nextref</token> administration (for example: in Internet Explorer, you can click <ui>Tools</ui> &gt; <ui>InPrivate Browsing</ui>).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src30" class="srcSentence">
           If you have an existing Microsoft Online Services account, you'll need the administrator credentials for that account.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence"> If you don’t have such an account, or if you want to use this Intune tenant for evaluation purposes only, you don't need tenant administrator credentials.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src32" class="srcSentence">
           If you'll manage iOS or Windows Phone devices with Intune, you'll need certificates (or keys) and accounts to retrieve those certificates.</caps:sentence>
                <caps:sentence id="src33" class="srcSentence"> Android devices don't need any additional certificates:</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">Platform</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">Certificate Requirements</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">More information</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">
                   Windows Phone 8.1 and <token>winphone8_client_1</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">No certificate is required for Windows Phone 8.1 users who install the company portal app from the Store.</caps:sentence>
                        <caps:sentence id="src39" class="srcSentence"> A Symantec certificate is required for Windows Phone 8.0 or to use Intune to deploy the company portal app to Windows Phone 8.1 devices.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">This guidance assumes your users get the company portal app from the Store on a Windows Phone 8.1 or later device.</caps:sentence>
                        <caps:sentence id="src41" class="srcSentence"> For information about Windows Phone 8.0 support, see <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Set up Windows Phone management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">
                  Windows 10, <token>winblue_winrt_2</token>, <token>win8RT_client_1</token>, or <token>winblue_client_2</token> devices</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">There are no certificate requirements for enrolling Windows RT and Windows devices.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">
                          <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be Managed by Intune</link>.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">iOS or Mac OS X</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Get an Apple Push Notification service certificate.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src47" class="srcSentence">Request an Apple Push Notification service certificate from Apple, as described here: <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Start managing iOS devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </listItem>
          </list>
        </content>
      </section>
      <section address="Step1" expanded="true">
        <title>
          <caps:sentence id="src48" class="srcSentence">Step 1: Sign up or sign in to Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src49" class="srcSentence">Before  you either sign up or sign in to Intune,  you should consider the following:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src50" class="srcSentence">Whether your organization already has a Microsoft Online Services work or school account</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src51" class="srcSentence">Whether you have an Enterprise Agreement or equivalent volume licensing agreement with Microsoft</caps:sentence>
              </para>
            </listItem>
          </list>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">Sign up for a NEW account if either of the following is true:</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">Sign in with your WORK or SCHOOL account if:</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">
                          <embeddedLabel>You don’t have a work or school account.</embeddedLabel> A work or school account is provided when you sign a volume licensing agreement with Microsoft or subscribe to Office 365.</caps:sentence>
                        <caps:sentence id="src55" class="srcSentence"> If your organization has not signed an Enterprise Agreement or equivalent volume licensing agreement with Microsoft (or has an Office 365 account), then you do not have a Microsoft Online Services account that you can use to sign in to Microsoft Online Services.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">
                          <embeddedLabel>You will discard your Intune tenant after completing the 30-day trial.</embeddedLabel> You should sign up for a new account if you are using your <token>wit_nextref</token> free trial subscription for evaluation purposes only, and you plan to redo your <token>wit_nextref</token> service setup and device provisioning after the trial.</caps:sentence>
                        <caps:sentence id="src57" class="srcSentence"> This is the recommended option if you plan to use <token>wit_nextref</token> with System Center 2012 Configuration Manager.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="important">
                    <para>
                      <caps:sentence id="src58" class="srcSentence">If you sign up for a new account, you cannot later use an existing work or school account to manage that account, or combine it with existing volume licensing agreements.</caps:sentence>
                    </para>
                  </alert>
                  <para></para>
                </TD>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src59" class="srcSentence">You have a work or school account provided with a volume licensing agreement or Office 365 subscription, and you are using this trial to evaluate <token>wit_nextref</token>.</caps:sentence>
                    </embeddedLabel>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence id="src60" class="srcSentence">If you are setting up <token>wit_nextref</token> on an existing account, we recommend that you review <link xlink:href="3b4e778d-ac13-4c23-974f-5122f74626bc">Configure Microsoft Intune</link> before continuing with these steps.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
            </tbody>
          </table>
          <procedure address="BKMK_ToSignUpforSubscription" expanded="true">
            <title>
              <caps:sentence id="src61" class="srcSentence">Sign up or sign in to Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">First, <externalLink><linkText>click here to visit the Intune Sign up page</linkText><linkUri>https://portal.office.com/Signup/Signup.aspx?OfferId=40BE278A-DFD1-470a-9EF7-9F2596EA7FF9&amp;dl=INTUNE_A&amp;ali=1#0 </linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">On the <ui>Sign up</ui> page, sign in or sign up.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src64" class="srcSentence">If  you complete the sign-up process, you're automatically signed in to the <token>wit_icp_1</token> with the tenant administrator account.</caps:sentence>
                  <caps:sentence id="src65" class="srcSentence"> An email message that contains your account information is also sent to the email address that you provided during sign-up.</caps:sentence>
                  <caps:sentence id="src66" class="srcSentence"> This email confirms your subscription is active.</caps:sentence>
                  <caps:sentence id="src67" class="srcSentence"> If you sign in, you're automatically directed to the Intune admin portal.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_ConfigureDomain">
        <title>
          <caps:sentence id="src68" class="srcSentence">Step 2: Configure a custom domain name</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src69" class="srcSentence">By default, <token>wit_firstref</token> uses the domain name that you select when you subscribe to the service, which looks like <ui>&lt;domain&gt;.onmicrosoft.com</ui>.</caps:sentence>
            <caps:sentence id="src70" class="srcSentence"> When your organization owns a custom domain, you can configure your instance of <token>wit_nextref</token> to use that domain instead of the domain name provided with your subscription.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src71" class="srcSentence">Before you create new user accounts or synchronize accounts from your on-premises Active Directory, we strongly recommend that you decide whether to use only the .onmicrosoft.com domain or to add one or more of your custom domain names.</caps:sentence>
            <caps:sentence id="src72" class="srcSentence"> If you don't configure a custom domain name and suffix, each user account you import receives the onmicrosoft.com suffix for its user principal name (UPN).</caps:sentence>
            <caps:sentence id="src73" class="srcSentence"> Configuring a custom domain before adding users can help simplify the management of user identities for your subscription by enabling users to sign in with the credentials they use to access other domain resources.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src74" class="srcSentence">Because the tasks to configure <token>wit_nextref</token> to use your organizations custom domain name are the same as for other Azure AD tenants, use the information and procedures found in <externalLink><linkText>Add your domain</linkText><linkUri>http://technet.microsoft.com/library/hh969247.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src75" class="srcSentence">For more information about using your custom domain with a cloud-based service from Microsoft, see <externalLink><linkText>Internet domain management</linkText><linkUri>http://technet.microsoft.com/library/hh969248.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src76" class="srcSentence">When you subscribe to a cloud-based service from Microsoft, your instance of that service becomes a tenant of Microsoft Azure Active Directory (Azure AD), which provides identity and directory services for your cloud-based service.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src77" class="srcSentence">For more information about your Azure AD tenant, see <externalLink><linkText>What is an Azure AD tenant?</linkText><linkUri>http://technet.microsoft.com/library/jj573650.aspx</linkUri></externalLink>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section address="BKMK_SyncUsersFromAD">
        <title>
          <caps:sentence id="src78" class="srcSentence">Step 3: Synchronize Active Directory and add users to Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src79" class="srcSentence">As mentioned, you can configure directory synchronization to import user accounts from your on-premises Active Directory to Microsoft Azure Active Directory.</caps:sentence>
            <caps:sentence id="src80" class="srcSentence"> Additionally, when you activate directory synchronization in your Intune tenant, you are turning on this feature across  all the Microsoft cloud services that you are subscribed to.</caps:sentence>
            <caps:sentence id="src81" class="srcSentence"> When you use multiple services with the same Azure AD, the user accounts that you synchronize are available to each cloud-based service that shares your Azure AD.</caps:sentence>
            <caps:sentence id="src82" class="srcSentence"> Having your on-premises Active Directory service connected with all of your Azure Active Directory-based services makes managing user identity much simpler.</caps:sentence>
            <caps:sentence id="src83" class="srcSentence"> You can also configure single sign-on features to make the authentication experience for your users familiar and easy.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src84" class="srcSentence">The <externalLink><linkText>Azure AD Connect wizard</linkText><linkUri>https://www.microsoft.com/download/details.aspx?id=47594</linkUri></externalLink> is the single tool and guided experience for connecting your on-premises identity infrastructure to the cloud.</caps:sentence>
            <caps:sentence id="src85" class="srcSentence">  Choose your topology and needs (single or multiple directories, password sync or federation), and the wizard will deploy and configure all components required to get your connection up and running, including sync services, Active Directory Federation Services (AD FS), and the Azure AD PowerShell module.</caps:sentence>
            <caps:sentence id="src86" class="srcSentence"> Azure AD Connect encompasses functionality that was previously released as Dirsync and Azure AD Sync.</caps:sentence>
            <caps:sentence id="src87" class="srcSentence"> Learn more about directory integration at <externalLink><linkText>Directory integration</linkText><linkUri>http://technet.microsoft.com/library/jj573653.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src88" class="srcSentence">After you've added users to your Intune subscription, we recommend that you grant a few user accounts administrative credentials.</caps:sentence>
            <caps:sentence id="src89" class="srcSentence"> The console that you use to assign administrative credentials depends on the type of administrator you want to assign:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src90" class="srcSentence">
                  <embeddedLabel>Tenant administrator</embeddedLabel>: Use the <embeddedLabel><token>wit_icp_1</token></embeddedLabel> to assign this type of administrator to manage your subscription, including billing, cloud storage, and managing the users who can use <token>wit_nextref</token>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src91" class="srcSentence">
                  <embeddedLabel>Service administrator</embeddedLabel>: Use the <embeddedLabel><token>wit_adminconsole</token></embeddedLabel> to assign this type of administrator for day-to-day tasks including management of mobile devices or computers, deploying policy or software, and running reports.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src92" class="srcSentence">To learn more about administrator accounts, see <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268#BKMK_AdminAccounts">Intune administrator accounts</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src93" class="srcSentence">To learn about the benefits of synchronizing user accounts from your local directory to Azure AD, see <externalLink><linkText>Similarities between Active Directory and Azure AD</linkText><linkUri>http://technet.microsoft.com/library/dn518177.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_AssignWitLicenses">
        <title>
          <caps:sentence id="src94" class="srcSentence">Step 4: Manage Intune licenses</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src95" class="srcSentence">A user must have a license to your Intune subscription before they can sign in to use the service.</caps:sentence>
            <caps:sentence id="src96" class="srcSentence"> When users have a license, they are a member of the <token>wit_firstref</token> user group.</caps:sentence>
            <caps:sentence id="src97" class="srcSentence"> This group includes all users who have a license to use the subscription.</caps:sentence>
            <caps:sentence id="src98" class="srcSentence">
              <embeddedLabel>Each user license supports enrolling up to five devices</embeddedLabel>.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src99" class="srcSentence">
                  <embeddedLabel>When you use the <token>wit_icp_2</token> to add users</embeddedLabel> to your subscription, either manually or by bulk import from a CSV file, <token>wit_nextref</token> assigns an available license to each user account.</caps:sentence>
                <caps:sentence id="src100" class="srcSentence"> If you do not have an available license, then no license is assigned.</caps:sentence>
                <caps:sentence id="src101" class="srcSentence"> With both methods, you have the option to not assign licenses to the new user accounts at the time you add them to your subscription.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src102" class="srcSentence">
                  <embeddedLabel>When you import users from your on-premises Active Directory</embeddedLabel>, <token>wit_nextref</token> does not assign a license to each user account.</caps:sentence>
                <caps:sentence id="src103" class="srcSentence"> Instead, at a later time, you must edit the user account to assign a license to the user.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src104" class="srcSentence">
                  <embeddedLabel>When your subscription shares Azure AD with other Azure AD tenants</embeddedLabel>, you have access to users that were added to those services.</caps:sentence>
                <caps:sentence id="src105" class="srcSentence"> These users do not have a license to <token>wit_nextref</token> until you assign a license to each of them.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src106" class="srcSentence">If the option to assign or revoke a license to <token>wit_nextref</token> is disabled, your subscription might include volume licensing options, such as the options available when using <externalLink><linkText>Enterprise Mobility Suite</linkText><linkUri>http://www.microsoft.com/server-cloud/products/enterprise-mobility-suite/default.aspx</linkUri></externalLink>.</caps:sentence>
            <caps:sentence id="src107" class="srcSentence"> For information on how to assign or revoke licenses, see the documentation for your licensing options.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="Step3" expanded="true">
        <title>
          <caps:sentence id="src108" class="srcSentence">Step 5: Create groups to organize users and devices</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src109" class="srcSentence">Groups in <token>wit_nextref</token> give you great flexibility for managing your devices and users.</caps:sentence>
            <caps:sentence id="src110" class="srcSentence"> You can set up groups to suit your organizational needs (for example, by geographic location, department, or hardware characteristics) and use them to perform a wide variety of administrative tasks, from deploying policies for a set of users to deploying applications to a set of devices.</caps:sentence>
          </para>
          <para></para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src111" class="srcSentence">Create a device group</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src112" class="srcSentence">Use device groups to deploy apps and updates, and configure other features.</caps:sentence>
                <caps:sentence id="src113" class="srcSentence"> For example, set up a "My Devices" group using the following steps:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>Overview</ui> &gt; <ui>Create Group</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">For the <embeddedLabel>Group name</embeddedLabel>, type “My Devices” and, from the parent group list, select <embeddedLabel>All Devices</embeddedLabel>, and then click <ui>Next</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">On the <ui>Define Membership Criteria</ui> page, select <embeddedLabel>All devices</embeddedLabel> to indicate that the group includes both mobile devices and computers.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">On the <ui>Define Direct Membership</ui> page, click <embeddedLabel>Next</embeddedLabel>.</caps:sentence>
                    <caps:sentence id="src118" class="srcSentence"> If you previously created a group that did not include all devices, and you wanted to add specific devices to your new group, you can do that here.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src119" class="srcSentence">On the <ui>Summary</ui> page, review the actions that will be taken, and then click <ui>Finish</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src120" class="srcSentence">You can find the newly created group in the <ui>Groups</ui> list, in the <ui>Groups</ui> workspace, under <embeddedLabel>All Devices</embeddedLabel>.</caps:sentence>
                <caps:sentence id="src121" class="srcSentence"> From here, you can also edit or delete the group.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src122" class="srcSentence">Create a user group</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src123" class="srcSentence">Use user groups to deploy software and device policies.</caps:sentence>
                <caps:sentence id="src124" class="srcSentence"> For example, set up an "Intune Users" group using the following steps:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src125" class="srcSentence">In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>Overview</ui> &gt; <ui>Create Group</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">For the <embeddedLabel>Group name</embeddedLabel>, type “Intune Users” and, from the parent group list, select <embeddedLabel>All Users</embeddedLabel>, and then click <ui>Next</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src127" class="srcSentence">On the <ui>Define Membership Criteria</ui> page, set <ui>Start group membership with</ui> to <ui>All users in the Parent group</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">Beside <embeddedLabel>Exclude members from these security groups</embeddedLabel>, click <embeddedLabel>Browse</embeddedLabel> and then select <ui>Company Administrator</ui>.</caps:sentence>
                    <caps:sentence id="src129" class="srcSentence"> This exclusion lets you manage the Intune Users group without affecting the Company Administrator account (also known as the tenant administrator).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">On the <ui>Define Direct Membership</ui> page, click <embeddedLabel>Next</embeddedLabel>.</caps:sentence>
                    <caps:sentence id="src131" class="srcSentence"> You don’t need to do anything here because you want the Intune Users group to include all users, except for the Company Administrator.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src132" class="srcSentence">On the <ui>Summary</ui> page, review the actions that will be taken, and then click <ui>Finish</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src133" class="srcSentence">You can find the newly created group in the <ui>Groups</ui> list, in the <ui>Groups</ui> workspace, under <embeddedLabel>All Users</embeddedLabel>.</caps:sentence>
                <caps:sentence id="src134" class="srcSentence"> From here, you can also edit or delete the group.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src135" class="srcSentence">To learn more about using groups, see <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use Groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="Step4" expanded="true">
        <title>
          <caps:sentence id="src136" class="srcSentence">Step 6: Create policies and publish an app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src137" class="srcSentence">
              <token>wit_nextref</token> policies provide settings that help you control the security settings on mobile devices, maintain Windows Firewall and Endpoint Protection settings for computers, and deploy applications.</caps:sentence>
            <caps:sentence id="src138" class="srcSentence"> If you are planning to use Intune for devices that you configure for production use after the trial, it's absolutely essential that you follow the instructions in <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Configure policy for mobile devices in Microsoft Intune</link> and <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src139" class="srcSentence">You can perform two types of app installations using Intune.</caps:sentence>
            <caps:sentence id="src140" class="srcSentence"> The first is a <legacyBold>required install</legacyBold>, which automatically deploys the app to managed computers.</caps:sentence>
            <caps:sentence id="src141" class="srcSentence"> The other is an <legacyBold>available install</legacyBold>, which deploys the app, or a link to the app, to the Intune company portal so that users can choose whether to install it on their computers or on their mobile devices.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src142" class="srcSentence">Before using Intune to deploy apps, make sure that you have the appropriate licenses to publish, distribute, and use the app.</caps:sentence>
            <caps:sentence id="src143" class="srcSentence"> The Licenses workspace lets you add and manage license agreement information for apps or software purchased through Microsoft Volume Licensing agreements, and for Microsoft or non-Microsoft software that was purchased by other means.</caps:sentence>
            <caps:sentence id="src144" class="srcSentence"> You can then create license reports that display managed license usage information throughout your company to stay informed of license usage activity.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src145" class="srcSentence">In these steps, you'll set up a mobile device configuration policy and a Windows computer firewall policy, and configure Skype as an available install for mobile devices after they're enrolled.</caps:sentence>
            <caps:sentence id="src146" class="srcSentence"> After you add and deploy a new policy, all users or devices in the group to which you deployed the policy inherit the settings as their baseline policy.</caps:sentence>
            <caps:sentence id="src147" class="srcSentence"> You can always review and edit the details of these policies later from the Policy workspace.</caps:sentence>
          </para>
          <procedure expanded="true">
            <title>
              <caps:sentence id="src148" class="srcSentence">Create and deploy a mobile device configuration policy</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src149" class="srcSentence">Open the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src150" class="srcSentence">In the left pane, click the <ui>Policy</ui> icon.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">In the <ui>Tasks</ui> list on the <ui>Policy Overview</ui> page, click <ui>Add Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src152" class="srcSentence"> In the policy list, expand the platform you want to create a policy for, then select <ui>General Configuration</ui>, choose <ui>Create and Deploy a Policy with the Recommended Settings</ui>, and then click <ui>Create Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">When prompted to <ui>Select the groups to which you want to deploy this policy</ui>, select <ui>My Trial Users</ui> from the list, and click <ui>Add</ui> &gt; <ui>OK</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src154" class="srcSentence">Your policy appears in the list of configuration policies, and has been deployed to the <ui>My Trial Users</ui> group.</caps:sentence>
                  <caps:sentence id="src155" class="srcSentence"> Double-click the policy to view its settings.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="true">
            <title>
              <caps:sentence id="src156" class="srcSentence">Publish the Skype app for mobile devices</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click the <ui>Apps</ui> icon, then click <ui>Apps</ui> &gt; <ui>Add App</ui>.</caps:sentence>
                    <caps:sentence id="src158" class="srcSentence"> If prompted, enter your <token>wit_nextref</token> credentials.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src159" class="srcSentence">When you start the <embeddedLabel>Intune Software Publisher</embeddedLabel> for the first time, a short delay occurs while the application is installed.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">
                Review the security warning and click <ui>Run</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src161" class="srcSentence">On the <ui>Before you begin</ui> page, click <ui>Next</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">On the <ui>Software setup</ui> page in <ui>Select how this software is made available to devices</ui>, select <ui>External link</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">Enter the external link for the software in <ui>Specify the URL</ui>, and then click <ui>Next</ui>.</caps:sentence>
                    <caps:sentence id="src164" class="srcSentence"> Make sure that you preface the URL with <legacyBold>http://</legacyBold>.</caps:sentence>
                    <caps:sentence id="src165" class="srcSentence"> For the Skype app, use the link below that matches the mobile device platform you're using:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src166" class="srcSentence">
                          <embeddedLabel>iOS:</embeddedLabel> <externalLink><linkText>https://itunes.apple.com/us/app/skype-for-iphone/id304878510?mt%3D8</linkText><linkUri>https://itunes.apple.com/us/app/skype-for-iphone/id304878510?mt%3D8</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src167" class="srcSentence">
                          <embeddedLabel>Android:</embeddedLabel> <externalLink><linkText>https://play.google.com/store/apps/details?id=com.skype.raider</linkText><linkUri>https://play.google.com/store/apps/details?id=com.skype.raider</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src168" class="srcSentence">
                          <embeddedLabel>Windows Phone 8 or Windows Phone 8.1:</embeddedLabel> <externalLink><linkText>http://www.windowsphone.com/en-us/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51</linkText><linkUri>http://www.windowsphone.com/en-us/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51</linkUri></externalLink></caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">On the <ui>Software description</ui> page, provide the information that you want users to see in the company portal for the software, and then click <ui>Next</ui>.</caps:sentence>
                    <caps:sentence id="src170" class="srcSentence"> The following settings are available (this example refers to Skype):</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src171" class="srcSentence">
                          <legacyBold>Publisher:</legacyBold> Enter the name of the publisher, "Microsoft" </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src172" class="srcSentence">
                          <legacyBold>Name: </legacyBold>Enter <embeddedLabel>Skype</embeddedLabel></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src173" class="srcSentence">
                          <legacyBold>Description:</legacyBold> Enter a description for the software, such as <embeddedLabel>Skype communication app</embeddedLabel> </caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src174" class="srcSentence">
                          <legacyBold>Category: </legacyBold>Select the category that best fits this software, such as <embeddedLabel>Collaboration</embeddedLabel></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src175" class="srcSentence">
                          <legacyBold>Display this as a featured app and highlight it in the company portal:</legacyBold> Select this option to display the app prominently in the company portal on mobile devices.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src176" class="srcSentence">
                          <legacyBold>Icon: </legacyBold>Choose whether to associate an icon with the software.</caps:sentence>
                        <caps:sentence id="src177" class="srcSentence"> The maximum size for the icon is 250 x 250 pixels.</caps:sentence>
                        <caps:sentence id="src178" class="srcSentence"> The recommended size is 32 x 32 pixels.</caps:sentence>
                        <caps:sentence id="src179" class="srcSentence"> This setting is optional for the Intune trial tenant.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">On the <ui>Summary</ui> page, verify the software information, and then click <ui>Upload</ui>.</caps:sentence>
                    <caps:sentence id="src181" class="srcSentence"> Click <ui>Close</ui> to exit the wizard.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Apps</ui> &gt; <ui>Apps</ui> &gt; <ui>Skype</ui> &gt; <ui>Manage Deployment</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">On the <ui>Select Groups</ui> page, select <ui>My Trial Users</ui> to deploy the software to that user group, and then click <ui>Add</ui> &gt; <ui>Next</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">On the <ui>Deployment Action</ui> page, select <ui>Available Install</ui> from the <ui>Approval</ui> column for your group.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src185" class="srcSentence">Click <ui>Finish</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src186" class="srcSentence">The Skype app is now available to install on mobile devices from the company portal, but first you need to install <token>wit_nextref</token> software on computers and mobile devices.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_ConfigureCompanyPortal">
        <title>
          <caps:sentence id="src187" class="srcSentence">Step 7: Customize the company portal</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src188" class="srcSentence">The <token>wit_iwportal_1</token> is where users access company data and can do common tasks like enrolling devices, installing apps, and locating information for assistance from your IT department.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src189" class="srcSentence">When you customize the company portal, the configurations apply to both the company portal website and company portal apps.</caps:sentence>
          </para>
          <procedure expanded="true" address="BKMK_ToCustomizeCompanyPortal">
            <title>
              <caps:sentence id="src190" class="srcSentence">Settings for customizing the company portal</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administrator console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Company Portal</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src192" class="srcSentence">Configure one or more of the following optional items.</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src193" class="srcSentence">Configuration area</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src194" class="srcSentence">Field name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src195" class="srcSentence">Maximum character length</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src196" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD rowspan="6">
                          <para>
                            <caps:sentence id="src197" class="srcSentence">Company contact information and privacy statement</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src198" class="srcSentence">Company name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src199" class="srcSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src200" class="srcSentence">This name is displayed as the title of the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src201" class="srcSentence">IT department contact name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src202" class="srcSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src203" class="srcSentence">This name is displayed on the <ui>Contact IT</ui> page.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src204" class="srcSentence">IT department phone number</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src205" class="srcSentence">20</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src206" class="srcSentence">This contact number is displayed on the <ui>Contact IT</ui> page.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src207" class="srcSentence">IT department email address</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src208" class="srcSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src209" class="srcSentence">This contact address is displayed on the <ui>Contact IT</ui> page.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src210" class="srcSentence">You must enter a valid email address in the format <userInput>alias@domainname.com</userInput>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src211" class="srcSentence">Additional information</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src212" class="srcSentence">120</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src213" class="srcSentence">Displayed on the <ui>Contact IT</ui> page.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src214" class="srcSentence">Company privacy statement URL</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src215" class="srcSentence">79</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src216" class="srcSentence">You can specify your own company privacy statement that appears when users click the privacy links from the company portal.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src217" class="srcSentence">You must enter a valid URL in the format <userInput>https://www.contoso.com</userInput>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD rowspan="2">
                          <para>
                            <caps:sentence id="src218" class="srcSentence">Support contacts</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src219" class="srcSentence">Support website URL</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src220" class="srcSentence">150</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src221" class="srcSentence">If you have a support website that you want your users to use, specify the URL here.</caps:sentence>
                            <caps:sentence id="src222" class="srcSentence"> The URL must be in the format <userInput>https://www.contoso.com</userInput>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src223" class="srcSentence">If you don't specify a URL, nothing is displayed for the support website on the <ui>Contact IT</ui> page in the company portal.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src224" class="srcSentence">Website name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src225" class="srcSentence">40</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src226" class="srcSentence">This name is the friendly name that is displayed for the URL to the support website.</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src227" class="srcSentence">If you specify a support website URL and no friendly name, then <ui>Go to IT website</ui> is displayed on the <ui>Contact IT</ui> page in the company portal.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD rowspan="3">
                          <para>
                            <caps:sentence id="src228" class="srcSentence">Customization</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src229" class="srcSentence">Theme color</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src230" class="srcSentence">Not applicable</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src231" class="srcSentence">Select a theme color to apply to the company portal.</caps:sentence>
                          </para>
                          <para></para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src232" class="srcSentence">Include company logo</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src233" class="srcSentence">Not applicable</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src234" class="srcSentence">When you enable this option, you can upload your company logo to show in your company portal.</caps:sentence>
                            <caps:sentence id="src235" class="srcSentence"> You can upload two logos:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src236" class="srcSentence">One logo that is displayed when the company portal background is white</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src237" class="srcSentence">One logo that is displayed when the company portal background uses your selected theme color</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <para>
                            <caps:sentence id="src238" class="srcSentence">Each logo must be a .png or .jpg file type and meet the following criteria:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src239" class="srcSentence">Maximum resolution of 400 x 100 pixels</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src240" class="srcSentence">Size of 750 KB or less</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src241" class="srcSentence">Choose a background for <token>win8_client_2</token> company portal app</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src242" class="srcSentence">Not applicable</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src243" class="srcSentence">This setting affects the background for the <token>win8_client_2</token> company portal app only.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src244" class="srcSentence">Click <ui>Save</ui> to save your changes.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src245" class="srcSentence">After you save your changes, you can use the links provided at the bottom of the <ui>Company Portal</ui> page of the administration console to view the company portal website.</caps:sentence>
                  <caps:sentence id="src246" class="srcSentence"> These links cannot be changed.</caps:sentence>
                  <caps:sentence id="src247" class="srcSentence"> When a user signs in, these links display your subscriptions in the company portal.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="Step5" expanded="true">
        <title>
          <caps:sentence id="src248" class="srcSentence">Step 8: Enroll computers in Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src249" class="srcSentence">You can install the <token>wit_nextref</token> client software on computers in the following ways:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src250" class="srcSentence">Users can use an installer provided by the administrator to manually enroll</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src251" class="srcSentence">
                  <token>wit_nextref</token> software can be included in an OS image or deployed using Group Policy</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src252" class="srcSentence">End users can also self-enroll their devices through the <token>wit_firstref</token> company portal</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src253" class="srcSentence">Each enrolled computer is linked to the user account that was used to install the client software.</caps:sentence>
            <caps:sentence id="src254" class="srcSentence"> Microsoft Intune Endpoint Protection is also installed by default during Intune client installation on computers.</caps:sentence>
            <caps:sentence id="src255" class="srcSentence"> Endpoint Protection helps to secure the computers in your organization by providing real-time protection against potential threats, keeping malicious software definitions up to date, and automatically running scheduled scans.</caps:sentence>
            <caps:sentence id="src256" class="srcSentence"> For added security, you can also use Intune policies to manage Windows Firewall settings on managed computers.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src257" class="srcSentence">What to know before you start:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src258" class="srcSentence">The user must be an administrator on the computer to install the client software.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src259" class="srcSentence">Self-enrolling requires that Internet Explorer is installed on the client computer.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src260" class="srcSentence">Each time a user self-enrolls a computer, it uses a <token>wit_firstref</token> license.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src261" class="srcSentence">You must use a Microsoft Online Services work or school account to self-enroll a computer.</caps:sentence>
                <caps:sentence id="src262" class="srcSentence"> This is the account that you used to sign in, or the administrator account that was created when you signed up for the free trial.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src263" class="srcSentence">For this example, you'll use the self-enrollment approach:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src264" class="srcSentence">In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Company Portal</ui>, and then scroll to the bottom of the screen.</caps:sentence>
                <caps:sentence id="src265" class="srcSentence"> Copy the URL shown under <ui>Intune company portal</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src266" class="srcSentence">Use Internet Explorer to browse to the company portal URL that you acquired in the previous step, and log in with your administrator credentials.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src267" class="srcSentence">Click <ui>Add Device</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src268" class="srcSentence">Click <ui>Download Software</ui> and then click <ui>Run</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src269" class="srcSentence">Click <ui>Next</ui> to start the <token>wit_firstref</token> Setup wizard.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src270" class="srcSentence">When the Setup wizard has completed, click <ui>Finish</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src271" class="srcSentence">To learn more about computer management using <token>wit_nextref</token>, see <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be managed by Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src272" class="srcSentence">To learn more about software management using <token>wit_nextref</token>, see <link xlink:href="5b49d81d-8a28-4d78-a21b-6614920a7b82">Manage software with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="Step6" expanded="true">
        <title>
          <caps:sentence id="src273" class="srcSentence">Step 9: Enroll mobile devices and install an app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src274" class="srcSentence">To set up mobile device management with Intune, you must  first set the mobile device management authority,  enable management for device platforms, and enroll your devices with the company portal app.</caps:sentence>
            <caps:sentence id="src275" class="srcSentence"> You can then deploy the Microsoft Skype application that you published.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src276" class="srcSentence">Enable device management and enroll devices</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src277" class="srcSentence">
                      <embeddedLabel>Make Intune your mobile device management authority</embeddedLabel>
                      <br />In the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui>, and click <ui>Set MDM Authority</ui> under <ui>Tasks</ui>.</caps:sentence>
                    <caps:sentence id="src278" class="srcSentence">  Click <ui>Yes</ui> in the MDM Authority dialog box.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src279" class="srcSentence">
                      <embeddedLabel>Enable MDM for your device platform</embeddedLabel>
                      <br />Enable mobile device management for the device platform you want to manage.</caps:sentence>
                    <caps:sentence id="src280" class="srcSentence"> Depending on your platform, different requirements are needed:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src281" class="srcSentence">
                          <embeddedLabel>iOS and Mac OS X</embeddedLabel>: see <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Set up iOS management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src282" class="srcSentence">
                          <embeddedLabel>Windows Phone</embeddedLabel>: see <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Set up Windows Phone management with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src283" class="srcSentence">
                          <embeddedLabel>Android</embeddedLabel>: Android mobile devices allow users to enroll using the company portal app available from Google Play.</caps:sentence>
                        <caps:sentence id="src284" class="srcSentence"> No additional configuration in Intune is required.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src285" class="srcSentence">
                      <embeddedLabel>Enroll devices</embeddedLabel>:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src286" class="srcSentence">
                          <embeddedLabel>Android</embeddedLabel> - Install the <ui>Intune Company Portal</ui> app from Microsoft Corporation available on <externalLink><linkText>Google Play</linkText><linkUri>http://go.microsoft.com/fwlink/p/?LinkId=386612</linkUri></externalLink> and sign in with the Intune user credentials added above.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src287" class="srcSentence">
                          <embeddedLabel>iOS and Mac OS X</embeddedLabel> - Install the <ui>Microsoft Intune Company Portal</ui> app from Microsoft Corporation available in the App Store and sign in with the Intune user credentials added above.</caps:sentence>
                        <caps:sentence id="src288" class="srcSentence"> View <ui>Enrolled devices</ui> to add your device.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src289" class="srcSentence">
                          <embeddedLabel>Windows Phone 8.1</embeddedLabel>- Users install the <ui>Company Portal</ui> app from Microsoft Corporation available in the Windows Phone store and sign in with the Intune user credentials added above.</caps:sentence>
                        <caps:sentence id="src290" class="srcSentence">  View <ui>Enrolled devices</ui> to add your device.<ui></ui></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src291" class="srcSentence">
                          <embeddedLabel>Windows Phone 8.0 </embeddedLabel> - Users click <ui>system settings</ui> &gt; <ui>company apps</ui>, and sign in with Intune user credentials added above.</caps:sentence>
                        <caps:sentence id="src292" class="srcSentence"> The company portal app is deployed to your phone.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src293" class="srcSentence">If prompted for a <ui>Server address</ui>, type “manage.microsoft.com”.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src294" class="srcSentence">Open the company portal on the mobile device, choose <ui>Apps</ui>, and then install <ui>Microsoft Skype</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence id="src295" class="srcSentence">To learn more about mobile device management using <token>wit_nextref</token>, see <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage Mobile Devices with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src296" class="srcSentence">Post-configuration tasks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src297" class="srcSentence">After you complete the initial configuration steps for an Intune  paid subscription, you should consider enabling additional mobile device management functionality.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src298" class="srcSentence">
                  <legacyBold>Connect Exchange to Intune:</legacyBold> For users with mobile devices  that haven't  enrolled in Intune, you can enable Exchange ActiveSync management using a connector for on-premises Exchange and for Exchange Online in  Microsoft Office 365.</caps:sentence>
                <caps:sentence id="src299" class="srcSentence"> The Exchange connector connects you with your Exchange deployment and lets you manage mobile devices through the Intune administration console.</caps:sentence>
                <caps:sentence id="src300" class="srcSentence"> To learn more about the Exchange connector, see <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac">Mobile device management with Exchange ActiveSync and Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src301" class="srcSentence">
                  <legacyBold>Intune reports:</legacyBold> Microsoft Intune provides alerts and reports that you can use to help monitor devices, as well as software license status and actions that affect devices (such as wiping a device).</caps:sentence>
                <caps:sentence id="src302" class="srcSentence">  To learn more about reporting, see <link xlink:href="0f7dc155-cb8e-477b-ba02-2623194a9575">Monitoring and reporting with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src303" class="srcSentence">
                  <legacyBold>Protecting company resources:</legacyBold>  After you've configured Intune and enrolled your devices, you'll want to make sure that you're protecting devices against data loss and other threats.</caps:sentence>
                <caps:sentence id="src304" class="srcSentence"> To learn more about protecting resources, see <link xlink:href="71e0cbf3-2bfb-412e-8a12-8503df08b4cf">Protect company resources with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="1bfd1a23-681d-4cc8-834c-c7856d69d409">Get started with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>