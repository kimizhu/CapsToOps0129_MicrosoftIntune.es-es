---
title: Usar un dispositivo Windows con Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0de5f03a-c288-423b-b9ea-493a39eb715a
---
# Usar un dispositivo Windows con Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence sentenceid="efe775eb937389b784eaa8421d6cb86a" id="tgt1" class="tgtSentence">Siga estos pasos para las tareas que necesita hacer en el equipo o dispositivo Windows si la empresa usa Microsoft Intune:</caps:sentence>
        </para>
        <table border="1">
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="54daf68978f49ad4d646edd222e602f1" id="tgt2" class="tgtSentence">Categoría de la tarea:</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e86e187e7bbea2eea4ad12ab7734221e" id="tgt3" class="tgtSentence">Tareas que puede realizar</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e6a2a3272b06e3df4f17efdd8970c4a3" id="tgt4" class="tgtSentence">Instalación de aplicaciones del Portal de empresa e inscripción a Intune</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_windows_enroll_instrucs">Enroll your device in Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_what_happns_enroll_all">What happens when I install the Company Portal app and enroll my device in Intune?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_what_IT_can_see">What can my IT admin see when I enroll my device in Intune?</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f043154e08f9b3476e587eb2d7bdb007" id="tgt5" class="tgtSentence">Cosas que puede hacer cuando el dispositivo está inscrito en Intune</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_whatis_cp_website">What is the Company Portal website?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_install_comp_apps">Install company apps</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_encrypt_device">Encrypt your device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_erase_lost_device">Reset (erase) your lost or stolen device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_unenroll_device">Unenroll your device from Intune</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section expanded="true" address="BKMK_windows_enroll_instrucs">
        <title>
          <caps:sentence sentenceid="77956432d1ee5eec1f0a618647bbc6a4" id="tgt6" class="tgtSentence">Inscripción del dispositivo en Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="83f5c2932ca49c0cf70926ff42419945" id="tgt7" class="tgtSentence">Para inscribirse, use el vínculo que corresponda al dispositivo que está usando:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="#BKMK_enrollment_w10">Windows 10</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_enrollment_w81orwrt81">Windows 8.1 or Windows RT 8.1</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_enrollment_rt">Windows RT</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_enrollment_81">Windows Phone 8.1</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_enrollment_wp8">Windows Phone 8</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section expanded="false" address="BKMK_enrollment_w10">
            <title>
              <caps:sentence sentenceid="a57b7503c9abb46897e25ecedd505cd1" id="tgt8" class="tgtSentence">Windows 10</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="94f1492f6d274db2e649a11db5e4d80a" id="tgt9" class="tgtSentence">Para inscribir su dispositivo:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="23516a9b34e924080e29e4f693f1921e" id="tgt10" class="tgtSentence">Vaya a <ui>Configuración</ui> de Windows y pulse <ui>Cuentas</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="4c9802b2-e99d-49bb-8ed2-12755f4ac7fb"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt11" class="tgtSentence">Pulse <ui>Su cuenta</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="af0ec2cb-e0aa-434e-9ed5-d37760c6d9b5"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt12" class="tgtSentence">Pulse <ui>Agregar una cuenta de trabajo o escuela</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="a66586cf-6d54-4838-ba3a-8c68b7967b29"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="49e0ae1cb1953cd3ae491633486d34fb" id="tgt13" class="tgtSentence">Inicie sesión con las credenciales de su trabajo o escuela.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="62f563e3-67d3-4d4d-8f04-d59b800fd8b5"></image>
                  </mediaLink>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="bce617b405840125581c9134ae72f378" id="tgt14" class="tgtSentence">Si, después de seguir los pasos anteriores, no consigue acceder al correo electrónico, archivos y otros datos del trabajo o centro educativo, vuelva a <ui>Cuentas</ui> y pulse <ui>Acceso al trabajo</ui>.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c55778b21e2e3ca75ba30f0480c86acd" id="tgt15" class="tgtSentence">Si ve su cuenta profesional o educativa, felicidades.</caps:sentence>
                    <caps:sentence sentenceid="f3727ede0d6f171e07294dec443f43d9" id="tgt16" class="tgtSentence"> Está conectado.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d2339e7732ddd27c47b8f2715909e2af" id="tgt17" class="tgtSentence">Si no la ve, pulse <ui>Conectar</ui>, y, a continuación, inicie sesión con sus credenciales del trabajo o centro educativo.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="856f23c4281aa869eb6e88376f4c9290" id="tgt18" class="tgtSentence">También se recomienda instalar la aplicación Portal de empresa, que le permitirá identificar fácilmente y obtener las aplicaciones de la empresa que son relevantes para usted y su rol.</caps:sentence>
                <caps:sentence sentenceid="cc32de009e3b7a4a80deb1749e0798c7" id="tgt19" class="tgtSentence"> Según la forma en que su empresa configuró Intune, la aplicación Portal de empresa se pudo haber instalado como parte del proceso de inscripción.</caps:sentence>
                <caps:sentence sentenceid="c1d575489b65c8ba758732716aa7ee80" id="tgt20" class="tgtSentence"> Para comprobar si tiene la aplicación, busque <ui>Portal de empresa</ui> en su lista de aplicaciones.</caps:sentence>
                <caps:sentence sentenceid="077ade8ab3af7ae46b5ae6275f6c1836" id="tgt21" class="tgtSentence"> Si no ve el Portal de empresa en su lista de aplicaciones, siga estos pasos para instalarlo.</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt22" class="tgtSentence">Pulse en <ui>Inicio</ui> &gt; <ui>Almacén</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt23" class="tgtSentence">Pulse en <ui>Buscar</ui> y escriba <ui>portal de empresa</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="6c09ca8a2f87996472a563c9eeb0b0f2" id="tgt24" class="tgtSentence">En la lista de resultados, pulse <ui>Portal de empresa</ui> &gt; <ui>Instalar</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d557f8fe2e2d0413015912477de1658c" id="tgt25" class="tgtSentence">Pulse <ui>Instalar</ui> o <ui>Libre</ui>.</caps:sentence>
                    <caps:sentence sentenceid="b693edb2bebbf1c2e112141075730df0" id="tgt26" class="tgtSentence"> La opción que se muestra dependerá de cómo la empresa haya configurado la aplicación.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false" address="BKMK_enrollment_w81orwrt81">
            <title>
              <caps:sentence sentenceid="fa726eae40323459ba5300b8be0e326e" id="tgt27" class="tgtSentence">Windows 8.1 o Windows RT 8.1</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="94f1492f6d274db2e649a11db5e4d80a" id="tgt28" class="tgtSentence">Para inscribir su dispositivo:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1d838bef11950cceb3391aa9929d969d" id="tgt29" class="tgtSentence">En el dispositivo, pulse <ui>Configuración</ui> &gt; <ui>Configuración de PC</ui> &gt; <ui>Red</ui> &gt; <ui>Área de trabajo</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="f0627ed5-a0a7-4ab3-8773-b8a5e433edaf"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5fa15152f4b2e752d841f806ba94b0dc" id="tgt30" class="tgtSentence">Escriba una dirección de correo electrónico profesional o educativa para el identificador de usuario y pulse <ui>Participar</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="85b997e325084a770f54193934e7da25" id="tgt31" class="tgtSentence"> Si el identificador de usuario no es necesario, entonces se usará la dirección de correo electrónico que especificó al iniciar sesión en este dispositivo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="decc61a215121631baf94104bbae3fae" id="tgt32" class="tgtSentence">Escriba la contraseña del correo electrónico de su empresa o centro educativo.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="1986dad1-9170-4dce-89ac-dc8ec498ea42"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt33" class="tgtSentence">En <ui>Activar la administración de dispositivos</ui>, pulse <ui>Activar</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="f9b63797-2cb2-4077-8f6e-fb4be0ea374c"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt34" class="tgtSentence">En el cuadro de diálogo <ui>Permitir aplicaciones y servicios del administrador de TI</ui>, seleccione <ui>Acepto</ui> y luego pulse <ui>Activar</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="a3a520b1-fed3-4475-987a-2ed5cc207b8f"></image>
                  </mediaLink>
                  <para>
                    <caps:sentence sentenceid="75300ee6393a3bcefcc30f52e6295edf" id="tgt35" class="tgtSentence">Cuando se haya registrado correctamente, verá la siguiente pantalla.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="4a53448b-4d2b-41a8-8c29-8dd1a8dc44f2"></image>
                  </mediaLink>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="856f23c4281aa869eb6e88376f4c9290" id="tgt36" class="tgtSentence">También se recomienda instalar la aplicación Portal de empresa, que le permitirá identificar fácilmente y obtener las aplicaciones de la empresa que son relevantes para usted y su rol.</caps:sentence>
                <caps:sentence sentenceid="cc32de009e3b7a4a80deb1749e0798c7" id="tgt37" class="tgtSentence"> Según la forma en que su empresa configuró Intune, la aplicación Portal de empresa se pudo haber instalado como parte del proceso de inscripción.</caps:sentence>
                <caps:sentence sentenceid="c1d575489b65c8ba758732716aa7ee80" id="tgt38" class="tgtSentence"> Para comprobar si tiene la aplicación, busque <ui>Portal de empresa</ui> en su lista de aplicaciones.</caps:sentence>
                <caps:sentence sentenceid="077ade8ab3af7ae46b5ae6275f6c1836" id="tgt39" class="tgtSentence"> Si no ve el Portal de empresa en su lista de aplicaciones, siga estos pasos para instalarlo.</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt40" class="tgtSentence">Pulse en <ui>Inicio</ui> &gt; <ui>Almacén</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt41" class="tgtSentence">Pulse en <ui>Buscar</ui> y escriba <ui>portal de empresa</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="6c09ca8a2f87996472a563c9eeb0b0f2" id="tgt42" class="tgtSentence">En la lista de resultados, pulse <ui>Portal de empresa</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d557f8fe2e2d0413015912477de1658c" id="tgt43" class="tgtSentence">Pulse <ui>Instalar</ui> o <ui>Libre</ui>.</caps:sentence>
                    <caps:sentence sentenceid="b693edb2bebbf1c2e112141075730df0" id="tgt44" class="tgtSentence"> La opción que se muestra dependerá de cómo la empresa haya configurado la aplicación.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false" address="BKMK_enrollment_rt">
            <title>
              <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt45" class="tgtSentence">Windows RT</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="94f1492f6d274db2e649a11db5e4d80a" id="tgt46" class="tgtSentence">Para inscribir su dispositivo:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt47" class="tgtSentence">Pulse <ui>Inicio</ui> y escriba <ui>Configuración del sistema</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="63329fb3f948aa6694f0f379778b5053" id="tgt48" class="tgtSentence">Pulse el cuadro de diálogo para abrir <ui>Aplicaciones de empresa</ui>.</caps:sentence>
                    <caps:sentence sentenceid="e7973fc9e77742fa39d0d901adbfe7b5" id="tgt49" class="tgtSentence"> Se le pedirá que acepte los términos y condiciones de su empresa.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ba3d0f462c754ee45808434363373db4" id="tgt50" class="tgtSentence">Inicie sesión con sus credenciales.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="856f23c4281aa869eb6e88376f4c9290" id="tgt51" class="tgtSentence">También se recomienda instalar la aplicación Portal de empresa, que le permitirá identificar fácilmente y obtener las aplicaciones de la empresa que son relevantes para usted y su rol.</caps:sentence>
                <caps:sentence sentenceid="cc32de009e3b7a4a80deb1749e0798c7" id="tgt52" class="tgtSentence"> Según la forma en que su empresa configuró Intune, la aplicación Portal de empresa se pudo haber instalado como parte del proceso de inscripción.</caps:sentence>
                <caps:sentence sentenceid="c1d575489b65c8ba758732716aa7ee80" id="tgt53" class="tgtSentence"> Para comprobar si tiene la aplicación, busque <ui>Portal de empresa</ui> en su lista de aplicaciones.</caps:sentence>
                <caps:sentence sentenceid="077ade8ab3af7ae46b5ae6275f6c1836" id="tgt54" class="tgtSentence"> Si no ve el Portal de empresa en su lista de aplicaciones, siga estos pasos para instalarlo.</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt55" class="tgtSentence">Pulse en <ui>Inicio</ui> &gt; <ui>Almacén</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt56" class="tgtSentence">Pulse en <ui>Buscar</ui> y escriba <ui>portal de empresa</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="6c09ca8a2f87996472a563c9eeb0b0f2" id="tgt57" class="tgtSentence">En la lista de resultados, pulse <ui>Portal de empresa</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt58" class="tgtSentence">Pulse <ui>Portal de empresa</ui> &gt; <ui>Instalar</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false" address="BKMK_enrollment_81">
            <title>
              <caps:sentence sentenceid="4693857bd32521105efeea9c79338cde" id="tgt59" class="tgtSentence">Windows Phone 8,1</caps:sentence>
            </title>
            <content>
              <para></para>
              <para>
                <caps:sentence sentenceid="2b8067fb0323534bfea2697390121fd4" id="tgt60" class="tgtSentence">Para inscribir el dispositivo en Intune, siga las instrucciones que se aplican a su empresa:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="#BKMK_comp_allows_cp">If your company lets you use the Company Portal from the Windows Store</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="#BKMK_comp_doesnt_allow_cp">If you aren’t allowed to access the Windows Store from your Windows Phone, or if you don’t have a Microsoft Account</link>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section address="BKMK_comp_allows_cp" expanded="false">
                <title>
                  <caps:sentence sentenceid="f84c2af95ccab3888a86926a6862078c" id="tgt61" class="tgtSentence">Si su empresa le permite usar el Portal de empresa desde la Tienda Windows</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="904dea5c75092e221f1c7542ad861f20" id="tgt62" class="tgtSentence">Instale la aplicación del Portal de empresa en su dispositivo:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt63" class="tgtSentence">Pulse en <ui>Inicio</ui> &gt; <ui>Almacén</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt64" class="tgtSentence">Pulse en <ui>Buscar</ui> y escriba <ui>portal de empresa</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="6c09ca8a2f87996472a563c9eeb0b0f2" id="tgt65" class="tgtSentence">En la lista de resultados, pulse <ui>Portal de empresa</ui>.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="89b255ef-e266-416d-a63b-9e1f7900d774"></image>
                      </mediaLink>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt66" class="tgtSentence">Pulse <ui>Portal de empresa</ui> &gt; <ui>Instalar</ui>.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="384372c5-bb31-40db-9026-fa46f75fd0f3"></image>
                      </mediaLink>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="ddf106a72884bcedab805b5a76155ce4" id="tgt67" class="tgtSentence">Inscriba su dispositivo:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="43a7f0bdc7e31a903929e89a0df2c178" id="tgt68" class="tgtSentence">En el dispositivo, abra la aplicación <ui>Portal de empresa de Microsoft Intune</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="026a28d2079c48cac94232555e209c68" id="tgt69" class="tgtSentence">Proporcione sus credenciales.</caps:sentence>
                        <caps:sentence sentenceid="69b11eb80e7bf244476a231742c4b0de" id="tgt70" class="tgtSentence"> Se le pedirá que acepte los términos y condiciones de su empresa, si es necesario.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="71fc82bf067fe524374a37d76fa156e5" id="tgt71" class="tgtSentence">Deslice rápidamente a <ui>Mis dispositivos</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt72" class="tgtSentence">Pulse en <ui>Toque para inscribir o identificar el dispositivo</ui>.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="2337ae7a-7c04-4dcc-bab4-dbe8b08fd30a"></image>
                      </mediaLink>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt73" class="tgtSentence">Pulse en <ui>Inscribir el dispositivo</ui>.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="c328bf4a-44a3-48c4-8656-0af5d1350195"></image>
                      </mediaLink>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt74" class="tgtSentence">Pulse en <ui>Agregar cuenta</ui>.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="39691416-afe3-411a-9e0b-7c642f0c5241"></image>
                      </mediaLink>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="06f2428511fe94c5a508f5c6754608d9" id="tgt75" class="tgtSentence">Escriba información adicional cuando se le solicite y, a continuación, pulse en <ui>iniciar sesión</ui> para completar la inscripción.</caps:sentence>
                        <caps:sentence sentenceid="6fc26cb86b3f6cae397038832327a15e" id="tgt76" class="tgtSentence"> Ahora debería aparecer su cuenta de área de trabajo en la página <ui>Configuración</ui> &gt; <ui>Área de trabajo</ui>.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="75f82638-825d-4ea5-bfc8-6899bae8964c"></image>
                      </mediaLink>
                    </listItem>
                  </list>
                </content>
              </section>
              <section address="BKMK_comp_doesnt_allow_cp">
                <title>
                  <caps:sentence sentenceid="f79ef31c687081a27b4bd46f72d7fba4" id="tgt77" class="tgtSentence">Si no está autorizado para acceder a la Tienda Windows desde su Windows Phone o no tiene una cuenta Microsoft</caps:sentence>
                </title>
                <content>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt78" class="tgtSentence">Pulse <ui>Configuración</ui> &gt; <ui>Área de trabajo</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt79" class="tgtSentence">Pulse en <ui>agregar cuenta</ui> y, a continuación, inicie sesión con su cuenta profesional.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="e7704b47579a2b16561af5a21140980d" id="tgt80" class="tgtSentence">Escriba información adicional cuando se le solicite y, a continuación, pulse en <ui>iniciar sesión</ui> para completar la inscripción.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c5066cfd21ce2eba14a21468e1cae5c0" id="tgt81" class="tgtSentence">Si se le pide que instale la aplicación de empresa o un concentrador, asegúrese de que está activada la casilla correspondiente y pulse en <ui>listo</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="3db4497f59381bfe7e90e326f1e7cf57" id="tgt82" class="tgtSentence">Si su administrador de TI configuró el Portal de empresa para que se instale durante la inscripción, lo verá en la lista de aplicaciones.</caps:sentence>
                  </para>
                </content>
              </section>
            </sections>
          </section>
          <section expanded="true" address="BKMK_enrollment_wp8">
            <title>
              <caps:sentence sentenceid="e8d2fb426803ec5ca779721a20e31ea4" id="tgt83" class="tgtSentence">Windows Phone 8</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="ddf106a72884bcedab805b5a76155ce4" id="tgt84" class="tgtSentence">Inscriba su dispositivo:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1d838bef11950cceb3391aa9929d969d" id="tgt85" class="tgtSentence">En el dispositivo, pulse <ui>Configuración</ui> &gt; <ui>Aplicaciones de empresa</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt86" class="tgtSentence">Pulse en <ui>agregar cuenta</ui> y, a continuación, inicie sesión con su cuenta profesional.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5ec4f71cd15940dc9e852f3fd65b3d71" id="tgt87" class="tgtSentence">Después de que la cuenta se agregue correctamente, se le pedirá que instale la aplicación de empresa o un concentrador.</caps:sentence>
                    <caps:sentence sentenceid="4d59c5c442094c964dceace2f01cf145" id="tgt88" class="tgtSentence"> Asegúrese de que está activada la casilla correspondiente y, a continuación, pulse en <ui>listo</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="d8803351960d9b4d57c84a4296974d36" id="tgt89" class="tgtSentence">El Portal de empresa aparecerá en la lista de aplicaciones después de instalarse.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <maml:section expanded="true" address="BKMK_win_install_comp_apps" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="f3b75dac002bfedf4bf2490755da963d" id="tgt90" class="tgtSentence">Instalar aplicaciones de empresa</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="2d5a4eebfaf348c097ce2509288ef568" id="tgt91" class="tgtSentence">En <maml:ui>Aplicaciones</maml:ui>, seleccione una aplicación.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt92" class="tgtSentence">Pulse <maml:ui>Tienda</maml:ui> &gt; <maml:ui>instalar</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section expanded="true" address="BKMK_win_whatis_cp_website">
        <title>
          <caps:sentence sentenceid="ccd935f9f23cff38cb90ccc56a125c5d" id="tgt93" class="tgtSentence">¿Qué es el sitio web del Portal de empresa?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="986215bc9877ad4f1c9a37fe6c61cf70" id="tgt94" class="tgtSentence">El sitio web del Portal de empresa es la interfaz web de la empresa que utiliza para administrar los dispositivos y equipos de trabajo, así como los dispositivos y equipos personales que decide usar en el trabajo.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3441568050c2e3d649eefbf1f866dae1" id="tgt95" class="tgtSentence">Una vez agregado el equipo o dispositivo al Portal de empresa, puede:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="3dc0b17542da2ec9d90ff0965d19aef1" id="tgt96" class="tgtSentence">Buscar y descargar aplicaciones de empresa</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="24f36f38ee72b6fa42d0813821d7a74a" id="tgt97" class="tgtSentence">Administrar dispositivos que ha agregado al Portal de empresa</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ed64c84b76d070c3000586dc8cade916" id="tgt98" class="tgtSentence">Buscar información de contacto para el administrador de TI</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="0fcf080dfd657a9002b287689ccf1b79" id="tgt99" class="tgtSentence">Al agregar un equipo o dispositivo al Portal de empresa, puede que se instale algún software o se descargue alguna aplicación (en función del dispositivo).</caps:sentence>
            <caps:sentence sentenceid="88979f566721038ff94ad975d202e55f" id="tgt100" class="tgtSentence"> También proporciona al administrador de TI permiso para administrar el dispositivo, a fin de ayudar a proteger la información de la empresa en el dispositivo.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="true" address="BKMK_win_encrypt_device">
        <title>
          <caps:sentence sentenceid="71589dcc021fa7128be6ce02c4bae40c" id="tgt101" class="tgtSentence">Cifrado del dispositivo</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="24014e807abe91180edf3f185c9b66f8" id="tgt102" class="tgtSentence">Puede cifrar el dispositivo agregando una cuenta Microsoft o habilitando BitLocker.</caps:sentence>
          </para>
          <para>
            <ui>
              <caps:sentence sentenceid="57f049214cccb01cb817cbbb21b62a1f" id="tgt103" class="tgtSentence">Opción 1: agregar una cuenta de Microsoft</caps:sentence>
            </ui>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="493fc5632cdde183aa43731c8dd63143" id="tgt104" class="tgtSentence">Busque e inicie la aplicación <ui>Configuración de PC</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt105" class="tgtSentence">Haga clic en <ui>Cuentas</ui> &gt; <ui>Su cuenta</ui> y, después, haga clic en <ui>Conectar a una cuenta Microsoft</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="851116caa4a0456605a67974f94a5f0a" id="tgt106" class="tgtSentence">Siga las instrucciones que aparecen.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0b547cb1e39a3c19be4421f95bedb157" id="tgt107" class="tgtSentence">Asegúrese de que el dispositivo esté inscrito en <token>wit_firstref</token> siguiendo las instrucciones que se indican en <externalLink><linkText>Inscribir su dispositivo para usarlo en el trabajo</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=519071</linkUri></externalLink>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <ui>
              <caps:sentence sentenceid="fdd40109065df7219789e603b0274498" id="tgt108" class="tgtSentence">Opción 2: habilitar BitLocker</caps:sentence>
            </ui>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="493fc5632cdde183aa43731c8dd63143" id="tgt109" class="tgtSentence">Busque e inicie la aplicación <ui>Administrar BitLocker</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt110" class="tgtSentence">Haga clic en <ui>Activar BitLocker</ui> y siga las instrucciones indicadas para cifrar cada una de las unidades.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0b547cb1e39a3c19be4421f95bedb157" id="tgt111" class="tgtSentence">Asegúrese de que el dispositivo esté inscrito en <token>wit_firstref</token> siguiendo las instrucciones que se indican en <externalLink><linkText>Inscribir su dispositivo para usarlo en el trabajo</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=519071</linkUri></externalLink>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <maml:section expanded="true" address="BKMK_win_unenroll_device" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="e7334a6647a4beaf7b7148ac205d9349" id="tgt112" class="tgtSentence">Anulación de la inscripción del dispositivo en Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="38be995b6ca1514592b6e0e3d05c18a4" id="tgt113" class="tgtSentence">Si inscribió un dispositivo en Intune, pero ya no desea usarlo para el trabajo o la escuela y no necesita acceder al correo electrónico, a las aplicaciones o a otros recursos del trabajo o la escuela, debe anular la inscripción del dispositivo.</caps:sentence>
            <caps:sentence sentenceid="47f8091ce1c42f9f17dd3f60ce3cb2b2" id="tgt114" class="tgtSentence">   Una vez que se anule la inscripción de su dispositivo de Intune, ya no podrá acceder a estos recursos.</caps:sentence>
          </maml:para>
          <maml:list class="bullet">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="f7f81911bb81a06e3f7ecca441e2db08" id="tgt115" class="tgtSentence">Desde la lista de aplicaciones, pulse en la aplicación <maml:ui>Portal de empresa</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="8bb370fc8c793a3e48c63078eb21d130" id="tgt116" class="tgtSentence">Inicie sesión con las credenciales de su trabajo o escuela.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="2d5a4eebfaf348c097ce2509288ef568" id="tgt117" class="tgtSentence">En <maml:ui>Mis dispositivos</maml:ui>, seleccione el dispositivo cuya inscripción desee anular.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt118" class="tgtSentence">Pulse en <maml:ui>Quitar</maml:ui> &gt; <maml:ui>Quitar</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section expanded="true" address="BKMK_win_erase_lost_device">
        <title>
          <caps:sentence sentenceid="c06b6d82e53b630aa8f19483e6047696" id="tgt119" class="tgtSentence">Restablecer (borrar) el dispositivo perdido o robado</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="25c5afd9a776dc51030b16195ab0a2bd" id="tgt120" class="tgtSentence">Si pierde o le roban el teléfono, puede restablecer los valores predeterminados de fábrica en el dispositivo.</caps:sentence>
          </para>
          <alert class="warning">
            <para>
              <caps:sentence sentenceid="cc052fb10fe9bbbc80b2b6df67c21fb9" id="tgt121" class="tgtSentence">Al hacerlo, quitará de él su información personal y de trabajo.</caps:sentence>
            </para>
          </alert>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="584ae3f5871f02f190ba7c45c0987bc0" id="tgt122" class="tgtSentence">En el explorador, abra el Portal de empresa e inicie sesión en su cuenta profesional.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt123" class="tgtSentence">En <ui>Mis dispositivos</ui>, haga clic en el dispositivo perdido o robado.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt124" class="tgtSentence">Haga clic en <ui>Restablecer</ui> &gt; <ui>Restablecer</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="843a6cd618daa054e4a48332cc86acbe" id="tgt125" class="tgtSentence">Si no puede restablecer el dispositivo perdido o robado, póngase en contacto con TI para restablecerlo por usted.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section address="BKMK_what_happns_enroll_all">
        <title>
          <caps:sentence sentenceid="c7771a0e09cd91e94fb6776ff1223ac3" id="tgt126" class="tgtSentence">¿Qué ocurrirá cuando instale la aplicación Portal de empresa e inscriba el dispositivo en Intune?</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section address="BKMK_what_happens_w10" expanded="true">
            <title>
              <caps:sentence sentenceid="cd7bae8efb7a91e15bd84c21183d20eb" id="tgt127" class="tgtSentence">¿Qué ocurrirá cuando instale la aplicación Portal de empresa e inscriba el dispositivo Windows 10 en Intune?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4d1ead9c6f9785639ee99ab6d1b9d5f5" id="tgt128" class="tgtSentence">Cuando instale la aplicación Portal de empresa y use la aplicación para inscribir su dispositivo Windows 10 Enterprise o Professional en Intune, podrá usar la aplicación Portal de empresa para:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cd1a40a617eb283f621ef494fdaa498f" id="tgt129" class="tgtSentence">Acceder a la red, el correo electrónico y los archivos de trabajo de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="365f2777fae357fc28b1489affab4a54" id="tgt130" class="tgtSentence">Obtener aplicaciones de empresa desde el portal de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="7c7476a0520e0468f40a091eecb0d594" id="tgt131" class="tgtSentence">Configurar automáticamente su cuenta de correo electrónico de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="66b07c74bf99f92822a9939daafde7d3" id="tgt132" class="tgtSentence">Restablecer su teléfono a la configuración de fábrica si lo pierde o se lo roban</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="3c7c24bdc237c5619253277c977b01dd" id="tgt133" class="tgtSentence">Para conocer los pasos necesarios para realizar la inscripción, consulte <link xlink:href="#BKMK_enrollment_w10">Windows 10</link>.</caps:sentence>
                <caps:sentence sentenceid="565e2895147ebd93314f8e0df0e43e56" id="tgt134" class="tgtSentence"> Para obtener más información acerca de lo que el administrador de TI puede y no puede ver en su dispositivo, consulte <link xlink:href="#BKMK_win_what_IT_can_see">What can my IT admin see when I enroll my device in Intune?</link></caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="082d088b89e9db215e7c674b756c69fb" id="tgt135" class="tgtSentence">Cuando agrega un equipo:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a8d018490001a2179c6d369a97eaf592" id="tgt136" class="tgtSentence">Se instalarán algunas aplicaciones de software en el equipo para que el administrador de TI pueda administrar el equipo y para permitirle obtener recursos de la empresa, como aplicaciones o información de soporte técnico.</caps:sentence>
                    <caps:sentence sentenceid="4e94326d14ba00a66011735bde89d1b6" id="tgt137" class="tgtSentence"> El administrador de TI puede actualizar automáticamente este software.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fb23e798b0afe15d04c4d48e98be279b" id="tgt138" class="tgtSentence">Se puede instalar <token>wit_firstref</token> Endpoint Protection en el equipo.</caps:sentence>
                    <caps:sentence sentenceid="cf17ce605f9ace59bbbb95514b8bfbfe" id="tgt139" class="tgtSentence"> Se trata de software que permite detectar virus y malware.</caps:sentence>
                    <caps:sentence sentenceid="79d739203fe62ed49485c1ad992efd8e" id="tgt140" class="tgtSentence"> Para obtener más información, vea la <externalLink><linkText>Declaración de privacidad de Endpoint Protection</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=247324</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="24cc4bd15737627dad9ee3e7e309c67f" id="tgt141" class="tgtSentence">El administrador de TI puede realizar un inventario de todo el software instalado en el equipo, incluido el software que usted haya instalado.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1aa6cfa75e3c98c83374293c4279f76" id="tgt142" class="tgtSentence">Debe aceptar los términos y condiciones.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fc0e5e4cc8883c0a49ce30e8fc1f809b" id="tgt143" class="tgtSentence">El administrador de TI puede recopilar o eliminar datos de la unidad de disco duro del equipo.</caps:sentence>
                    <caps:sentence sentenceid="3f588ad256a6d06d68ad1b9cd2e2a06e" id="tgt144" class="tgtSentence"> El administrador de TI también puede borrar todo el disco duro.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="58ab554374c33e90a110f01e1b2f85b6" id="tgt145" class="tgtSentence">El administrador de TI puede instalar aplicaciones y actualizaciones en el equipo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="381571e11f49c2734b064f362163bffc" id="tgt146" class="tgtSentence">El administrador de TI puede aplicar directivas en el equipo.</caps:sentence>
                    <caps:sentence sentenceid="9c2674194dcb722b9057b7b1cdd8bfeb" id="tgt147" class="tgtSentence"> Por ejemplo, se le podría exigir establecer una contraseña o un PIN en el equipo, lo que podría impedir el acceso al equipo o eliminar todos los datos del disco duro del equipo tras varios intentos incorrectos de introducir la contraseña.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_what_happens_w81">
            <title>
              <caps:sentence sentenceid="f54cbaa810e9549e6620922855fc4897" id="tgt148" class="tgtSentence">¿Qué ocurrirá cuando instale la aplicación Portal de empresa e inscriba el dispositivo Windows 8.1 o Windows RT en Intune?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="b774caaa8453e30ae983b4c249a965f8" id="tgt149" class="tgtSentence">Cuando instale la aplicación Portal de empresa y use la aplicación para inscribir su dispositivo Windows 8.1 Enterprise o Professional o Windows RT en Intune, podrá usar la aplicación Portal de empresa para:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cd1a40a617eb283f621ef494fdaa498f" id="tgt150" class="tgtSentence">Acceder a la red, el correo electrónico y los archivos de trabajo de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="365f2777fae357fc28b1489affab4a54" id="tgt151" class="tgtSentence">Obtener aplicaciones de empresa desde el portal de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="7c7476a0520e0468f40a091eecb0d594" id="tgt152" class="tgtSentence">Configurar automáticamente su cuenta de correo electrónico de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="66b07c74bf99f92822a9939daafde7d3" id="tgt153" class="tgtSentence">Restablecer su teléfono a la configuración de fábrica si lo pierde o se lo roban</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="3c7c24bdc237c5619253277c977b01dd" id="tgt154" class="tgtSentence">Para conocer los pasos necesarios para realizar la inscripción, consulte <link xlink:href="#BKMK_enrollment_w81orwrt81">Windows 8.1 or Windows RT 8.1</link>.</caps:sentence>
                <caps:sentence sentenceid="565e2895147ebd93314f8e0df0e43e56" id="tgt155" class="tgtSentence"> Para obtener más información acerca de lo que el administrador de TI puede y no puede ver en su dispositivo, consulte <link xlink:href="#BKMK_win_what_IT_can_see">What can my IT admin see when I enroll my device in Intune?</link></caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="082d088b89e9db215e7c674b756c69fb" id="tgt156" class="tgtSentence">Cuando agrega un equipo:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a8d018490001a2179c6d369a97eaf592" id="tgt157" class="tgtSentence">Se instalarán algunas aplicaciones de software en el equipo para que el administrador de TI pueda administrar el equipo y para permitirle obtener recursos de la empresa, como aplicaciones o información de soporte técnico.</caps:sentence>
                    <caps:sentence sentenceid="4e94326d14ba00a66011735bde89d1b6" id="tgt158" class="tgtSentence"> El administrador de TI puede actualizar automáticamente este software.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fb23e798b0afe15d04c4d48e98be279b" id="tgt159" class="tgtSentence">Se puede instalar <token>wit_firstref</token> Endpoint Protection en el equipo.</caps:sentence>
                    <caps:sentence sentenceid="cf17ce605f9ace59bbbb95514b8bfbfe" id="tgt160" class="tgtSentence"> Se trata de software que permite detectar virus y malware.</caps:sentence>
                    <caps:sentence sentenceid="79d739203fe62ed49485c1ad992efd8e" id="tgt161" class="tgtSentence"> Para obtener más información, vea la <externalLink><linkText>Declaración de privacidad de Endpoint Protection</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=247324</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="24cc4bd15737627dad9ee3e7e309c67f" id="tgt162" class="tgtSentence">El administrador de TI puede realizar un inventario de todo el software instalado en el equipo, incluido el software que usted haya instalado.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1aa6cfa75e3c98c83374293c4279f76" id="tgt163" class="tgtSentence">Debe aceptar los términos y condiciones.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fc0e5e4cc8883c0a49ce30e8fc1f809b" id="tgt164" class="tgtSentence">El administrador de TI puede recopilar o eliminar datos de la unidad de disco duro del equipo.</caps:sentence>
                    <caps:sentence sentenceid="3f588ad256a6d06d68ad1b9cd2e2a06e" id="tgt165" class="tgtSentence"> El administrador de TI también puede borrar todo el disco duro.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="58ab554374c33e90a110f01e1b2f85b6" id="tgt166" class="tgtSentence">El administrador de TI puede instalar aplicaciones y actualizaciones en el equipo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="381571e11f49c2734b064f362163bffc" id="tgt167" class="tgtSentence">El administrador de TI puede aplicar directivas en el equipo.</caps:sentence>
                    <caps:sentence sentenceid="9c2674194dcb722b9057b7b1cdd8bfeb" id="tgt168" class="tgtSentence"> Por ejemplo, se le podría exigir establecer una contraseña o un PIN en el equipo, lo que podría impedir el acceso al equipo o eliminar todos los datos del disco duro del equipo tras varios intentos incorrectos de introducir la contraseña.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_what_happens_phone8" expanded="false">
            <title>
              <caps:sentence sentenceid="fdeb95621394040dcd0f50cf74ef95fc" id="tgt169" class="tgtSentence">¿Qué ocurrirá cuando instale la aplicación Portal de empresa e inscriba el dispositivo Windows Phone 8.1 o Windows Phone 8 en Intune?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="38a0d9f8e1ac4f121636cf94b3f9c935" id="tgt170" class="tgtSentence">Cuando instale la aplicación Portal de empresa y use la aplicación para inscribir su dispositivo Windows Phone 8.1 o Windows Phone 8 en Intune, podrá usar la aplicación Portal de empresa para:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cd1a40a617eb283f621ef494fdaa498f" id="tgt171" class="tgtSentence">Acceder a la red, el correo electrónico y los archivos de trabajo de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="365f2777fae357fc28b1489affab4a54" id="tgt172" class="tgtSentence">Obtener aplicaciones de empresa desde el portal de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="7c7476a0520e0468f40a091eecb0d594" id="tgt173" class="tgtSentence">Configurar automáticamente su cuenta de correo electrónico de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="66b07c74bf99f92822a9939daafde7d3" id="tgt174" class="tgtSentence">Restablecer su teléfono a la configuración de fábrica si lo pierde o se lo roban</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="4334146c058a9ec4982d53c1f31033ca" id="tgt175" class="tgtSentence">Para conocer los pasos necesarios para realizar la inscripción, consulte <link xlink:href="#BKMK_enrollment_81">Windows Phone 8.1</link> o <link xlink:href="#BKMK_enrollment_wp8">Windows Phone 8</link>.</caps:sentence>
                <caps:sentence sentenceid="534143229d09c97873adf98d33bb164b" id="tgt176" class="tgtSentence">  Para obtener más información acerca de lo que el administrador de TI puede y no puede ver en su dispositivo, consulte <link xlink:href="#BKMK_win_what_IT_can_see">What can my IT admin see when I enroll my device in Intune?</link>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="23f663883db5b48d9aba399a77e97bc9" id="tgt177" class="tgtSentence">Al agregar un dispositivo Windows Phone, da permiso al administrador de TI para acceder al dispositivo.</caps:sentence>
                <caps:sentence sentenceid="c1c2c0f76e506e4c114e45f70033641c" id="tgt178" class="tgtSentence"> El administrador puede hacer cosas como:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="76a4245a8c5b0d78004dbb5765c6cdb2" id="tgt179" class="tgtSentence">Restablecer la configuración predeterminada de fábrica del dispositivo.</caps:sentence>
                    <caps:sentence sentenceid="ec2b174c8222d31c80eac2abd68f4f60" id="tgt180" class="tgtSentence"> Esto es útil en caso de pérdida o robo del dispositivo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e420302b302b097db9467e4f027fbb50" id="tgt181" class="tgtSentence">Quitar todos los datos relacionados con la empresa y las aplicaciones empresariales que se instalaron.</caps:sentence>
                    <caps:sentence sentenceid="bebc79fbe14286bcca2d83d606469094" id="tgt182" class="tgtSentence"> Los datos personales y la configuración no se quitan.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9ce5937038a7840eaa9bbba565e419a8" id="tgt183" class="tgtSentence">Forzarle a establecer una contraseña o un PIN para el dispositivo, lo que podría bloquear el dispositivo o restablecer la configuración predeterminada del dispositivo (operación que podría incluir la eliminación de datos) tras varios intentos incorrectos de introducir la contraseña.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ed0a4efdcc1da1f65e1659cb638273cd" id="tgt184" class="tgtSentence">Forzar el cifrado de todos los datos en el dispositivo.</caps:sentence>
                    <caps:sentence sentenceid="069e34665f9e53073d27ad97b440e0ce" id="tgt185" class="tgtSentence"> Esto ayuda a proteger los datos en caso de pérdida o robo del dispositivo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1aa6cfa75e3c98c83374293c4279f76" id="tgt186" class="tgtSentence">Debe aceptar los términos y condiciones.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="466db659a4654d16823b3248008f1b41" id="tgt187" class="tgtSentence">Deshabilitar la tarjeta SD.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="432e255d49c1a89a239a20eff0618ddb" id="tgt188" class="tgtSentence">Instalar actualizaciones de aplicaciones en el dispositivo.</caps:sentence>
                    <caps:sentence sentenceid="17977be0622b44eaa8c64cf5eaa0d045" id="tgt189" class="tgtSentence"> Esto se aplica solo a las actualizaciones.</caps:sentence>
                    <caps:sentence sentenceid="cd4fa67d78f750e2a2cb51ddac7a284e" id="tgt190" class="tgtSentence"> El administrador no puede forzar la instalación de nuevas aplicaciones en el dispositivo, pero puede elegir instalar aplicaciones visibles en el portal de empresa.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="83b8192b6896161c5e67d19884f81dfc" id="tgt191" class="tgtSentence">Una vez agregado el dispositivo al portal de empresa, hará lo siguiente cada 8 horas aproximadamente: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5ba4cc4bde2dd286214e46b9c9155365" id="tgt192" class="tgtSentence">Descargar las actualizaciones de directivas o aplicaciones proporcionadas por el administrador de TI.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2e2ccf77ad7f22df14b4b4ec20b03448" id="tgt193" class="tgtSentence">Enviar actualizaciones de inventario de hardware.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="46161e3bf6e2b057efb82dbbf8d294e9" id="tgt194" class="tgtSentence">Enviar actualizaciones de inventario de aplicaciones de empresa.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_what_happens_vista">
            <title>
              <caps:sentence sentenceid="95e4bdbd5532ebea2c0026f0732e6079" id="tgt195" class="tgtSentence">¿Qué ocurrirá cuando instale la aplicación Portal de empresa e inscriba el dispositivo Windows 7 o Vista en Intune?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="2ff49bd9602cff071633c2ab6d3d5eb3" id="tgt196" class="tgtSentence">Cuando instale la aplicación Portal de empresa y use la aplicación para inscribir su dispositivo Windows 7 o Vista en Intune, podrá usar la aplicación Portal de empresa para:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cd1a40a617eb283f621ef494fdaa498f" id="tgt197" class="tgtSentence">Acceder a la red, el correo electrónico y los archivos de trabajo de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="365f2777fae357fc28b1489affab4a54" id="tgt198" class="tgtSentence">Obtener aplicaciones de empresa desde el portal de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="7c7476a0520e0468f40a091eecb0d594" id="tgt199" class="tgtSentence">Configurar automáticamente su cuenta de correo electrónico de la empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="66b07c74bf99f92822a9939daafde7d3" id="tgt200" class="tgtSentence">Restablecer su teléfono a la configuración de fábrica si lo pierde o se lo roban</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="7d4cc546e4bfdaef4cb3f5043b049bab" id="tgt201" class="tgtSentence">Para obtener más información acerca de lo que el administrador de TI puede y no puede ver en su dispositivo, consulte <link xlink:href="#BKMK_win_what_IT_can_see">What can my IT admin see when I enroll my device in Intune?</link>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="082d088b89e9db215e7c674b756c69fb" id="tgt202" class="tgtSentence">Cuando agrega un equipo:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a8d018490001a2179c6d369a97eaf592" id="tgt203" class="tgtSentence">Se instalarán algunas aplicaciones de software en el equipo para que el administrador de TI pueda administrar el equipo y para permitirle obtener recursos de la empresa, como aplicaciones o información de soporte técnico.</caps:sentence>
                    <caps:sentence sentenceid="4e94326d14ba00a66011735bde89d1b6" id="tgt204" class="tgtSentence"> El administrador de TI puede actualizar automáticamente este software.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fb23e798b0afe15d04c4d48e98be279b" id="tgt205" class="tgtSentence">Se puede instalar <token>wit_firstref</token> Endpoint Protection en el equipo.</caps:sentence>
                    <caps:sentence sentenceid="cf17ce605f9ace59bbbb95514b8bfbfe" id="tgt206" class="tgtSentence"> Se trata de software que permite detectar virus y malware.</caps:sentence>
                    <caps:sentence sentenceid="79d739203fe62ed49485c1ad992efd8e" id="tgt207" class="tgtSentence"> Para obtener más información, vea la <externalLink><linkText>Declaración de privacidad de Endpoint Protection</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=247324</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="24cc4bd15737627dad9ee3e7e309c67f" id="tgt208" class="tgtSentence">El administrador de TI puede realizar un inventario de todo el software instalado en el equipo, incluido el software que usted haya instalado.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1aa6cfa75e3c98c83374293c4279f76" id="tgt209" class="tgtSentence">Debe aceptar los términos y condiciones.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fc0e5e4cc8883c0a49ce30e8fc1f809b" id="tgt210" class="tgtSentence">El administrador de TI puede recopilar o eliminar datos de la unidad de disco duro del equipo.</caps:sentence>
                    <caps:sentence sentenceid="3f588ad256a6d06d68ad1b9cd2e2a06e" id="tgt211" class="tgtSentence"> El administrador de TI también puede borrar todo el disco duro.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="58ab554374c33e90a110f01e1b2f85b6" id="tgt212" class="tgtSentence">El administrador de TI puede instalar aplicaciones y actualizaciones en el equipo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="381571e11f49c2734b064f362163bffc" id="tgt213" class="tgtSentence">El administrador de TI puede aplicar directivas en el equipo.</caps:sentence>
                    <caps:sentence sentenceid="9c2674194dcb722b9057b7b1cdd8bfeb" id="tgt214" class="tgtSentence"> Por ejemplo, se le podría exigir establecer una contraseña o un PIN en el equipo, lo que podría impedir el acceso al equipo o eliminar todos los datos del disco duro del equipo tras varios intentos incorrectos de introducir la contraseña.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_win_what_IT_can_see">
        <title>
          <caps:sentence sentenceid="092899a89841e4cd42d93f2e7a265e66" id="tgt215" class="tgtSentence">¿Qué puede ver mi administrador de TI cuando inscriba el dispositivo en Intune?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9580373c6a8f78a774ff06c526b5e360" id="tgt216" class="tgtSentence">Cuando inscribe su dispositivo en Intune, el administrador de TI tiene permiso para administrar el dispositivo, a fin de ayudarle a proteger la información de la empresa que tiene en el mismo.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49b5c06f816b80fa0b53001b7e064dd0" id="tgt217" class="tgtSentence">TI no puede ver</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="919967a6e68fc799764ccfadd49d0d82" id="tgt218" class="tgtSentence">TI puede ver</caps:sentence>
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
                        <caps:sentence sentenceid="7b15a2dc20f223897228983bcb839a0d" id="tgt219" class="tgtSentence">Historial de llamadas</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b5c1e4334dd619fce44e7a047bd05a8d" id="tgt220" class="tgtSentence">Mensajes de texto</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="936249fa98a3357097ff1f12312225b4" id="tgt221" class="tgtSentence">Correo electrónico personal, contactos y calendario</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="827a82394f446cc4d02c0fd5e61f331b" id="tgt222" class="tgtSentence">Historial web</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d5189de027922f81005951e6efe0efd5" id="tgt223" class="tgtSentence">Ubicación</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b99bbccd22c782c7f7019bad4a0628f2" id="tgt224" class="tgtSentence">Álbum de cámara</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2c5a2582707f1495992f8b6befe92a6c" id="tgt225" class="tgtSentence">Datos personales</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="72122ce96bfec66e2396d2e25225d70a" id="tgt226" class="tgtSentence">Propietario</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="712778275c556c187fb77a2b8a2af8c4" id="tgt227" class="tgtSentence">Nombre del dispositivo</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c9f4029ce9dcf8ff7f8f1b70edead843" id="tgt228" class="tgtSentence">Número de serie</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c2904bca62b22443d6cf5e9d89cab204" id="tgt229" class="tgtSentence">Fabricante</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="20f35e630daf44dbfa4c3f68f5399d8c" id="tgt230" class="tgtSentence">Modelo</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d83f147fd8043b67aa813f44f597b39b" id="tgt231" class="tgtSentence">Sistema operativo</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="93a4cf66e1c393e83e3c39b8446f1b71" id="tgt232" class="tgtSentence">Aplicaciones de empresa</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a2da362c93e6fb8f4d57947fe2b2d8fd" id="tgt233" class="tgtSentence">Aplicaciones personales</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use these steps  for tasks that you need to do on your Windows device or computer when your company is using Microsoft Intune:</caps:sentence>
        </para>
        <table border="1">
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src2" class="srcSentence">Task category</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Tasks you can do</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Company Portal app installation and Intune enrollment</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_windows_enroll_instrucs">Enroll your device in Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_what_happns_enroll_all">What happens when I install the Company Portal app and enroll my device in Intune?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_what_IT_can_see">What can my IT admin see when I enroll my device in Intune?</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Things you can do when your device is enrolled in Intune</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_whatis_cp_website">What is the Company Portal website?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_install_comp_apps">Install company apps</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_encrypt_device">Encrypt your device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_erase_lost_device">Reset (erase) your lost or stolen device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_win_unenroll_device">Unenroll your device from Intune</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section expanded="true" address="BKMK_windows_enroll_instrucs">
        <title>
          <caps:sentence id="src6" class="srcSentence">Enroll your device in Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">To enroll, use the link that corresponds to the device you are using:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="#BKMK_enrollment_w10">Windows 10</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_enrollment_w81orwrt81">Windows 8.1 or Windows RT 8.1</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_enrollment_rt">Windows RT</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_enrollment_81">Windows Phone 8.1</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_enrollment_wp8">Windows Phone 8</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section expanded="false" address="BKMK_enrollment_w10">
            <title>
              <caps:sentence id="src8" class="srcSentence">Windows 10</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src9" class="srcSentence">To enroll your device:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Go to Windows <ui> Settings</ui> and tap <ui>Accounts</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="4c9802b2-e99d-49bb-8ed2-12755f4ac7fb"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Tap <ui>Your account</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="af0ec2cb-e0aa-434e-9ed5-d37760c6d9b5"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Tap <ui>Add a work or school account</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="a66586cf-6d54-4838-ba3a-8c68b7967b29"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Sign in with your work or school credentials.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="62f563e3-67d3-4d4d-8f04-d59b800fd8b5"></image>
                  </mediaLink>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src14" class="srcSentence">If you followed the steps above, but still can't access your work or school email, files, and other data, go back to <ui>Accounts</ui> and tap <ui>Work access</ui>.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">If you see your work or school account, congratulations.</caps:sentence>
                    <caps:sentence id="src16" class="srcSentence"> You’re connected.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">If you don’t see your work or school account, tap <ui>Connect</ui>, and then sign in with your work or school credentials.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src18" class="srcSentence">We also recommend that you install the Company Portal app, which lets you easily identify and get the company apps that are relevant to you and your role.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> Depending on how your company  configured Intune, the Company Portal app may have been installed as part of your enrollment process.</caps:sentence>
                <caps:sentence id="src20" class="srcSentence"> To check if you have the app, look for <ui>Company Portal</ui> in your apps list.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> If you don't see the Company Portal in your list of apps, follow these steps to install it.</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">Tap <ui>Start</ui> &gt; <ui>Store</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Tap <ui>Search</ui> and type <ui>company portal</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">In the list of results, tap <ui>Company Portal</ui> &gt; <ui>Install</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Tap  either <ui>Install</ui> or <ui>Free</ui>.</caps:sentence>
                    <caps:sentence id="src26" class="srcSentence"> The option shown depends on how your company configured the app.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false" address="BKMK_enrollment_w81orwrt81">
            <title>
              <caps:sentence id="src27" class="srcSentence">Windows 8.1 or Windows RT 8.1</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src28" class="srcSentence">To enroll your device:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">On the device, tap <ui>Settings</ui> &gt; <ui>PC Settings</ui> &gt; <ui>Network</ui> &gt; <ui>Workplace</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="f0627ed5-a0a7-4ab3-8773-b8a5e433edaf"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Enter your work or school email for the User ID, if required, and then tap <ui>Join</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src31" class="srcSentence"> If your user ID is not required,  the email address that you entered when you logged into this device is used.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Type the password for your work or school email.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="1986dad1-9170-4dce-89ac-dc8ec498ea42"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Under <ui>Turn on device management</ui>, tap <ui>Turn on</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="f9b63797-2cb2-4077-8f6e-fb4be0ea374c"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">In the <ui>Allow apps and services from IT admin</ui> dialog,  select the  <ui>I agree</ui> check box, and then tap <ui>Turn on</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="a3a520b1-fed3-4475-987a-2ed5cc207b8f"></image>
                  </mediaLink>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">When you have successfully enrolled, you'll see the following screen.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="4a53448b-4d2b-41a8-8c29-8dd1a8dc44f2"></image>
                  </mediaLink>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src36" class="srcSentence">We also recommend that you install the Company Portal app, which lets you easily identify and get the company apps that are relevant to you and your role.</caps:sentence>
                <caps:sentence id="src37" class="srcSentence"> Depending on how your company  configured Intune, the Company Portal app may have been installed as part of your enrollment process.</caps:sentence>
                <caps:sentence id="src38" class="srcSentence"> To check if you have the app, look for <ui>Company Portal</ui> in your apps list.</caps:sentence>
                <caps:sentence id="src39" class="srcSentence"> If you don't see the Company Portal in your list of apps, follow these steps to install it.</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Tap <ui>Start</ui> &gt; <ui>Store</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Tap <ui>Search</ui> and type <ui>company portal</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">In the list of results, tap <ui>Company Portal</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Tap  either <ui>Install</ui> or <ui>Free</ui>.</caps:sentence>
                    <caps:sentence id="src44" class="srcSentence"> The option shown depends on how your company configured the app.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false" address="BKMK_enrollment_rt">
            <title>
              <caps:sentence id="src45" class="srcSentence">Windows RT</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src46" class="srcSentence">To enroll your device:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">Tap <ui>Start</ui>, and then type <ui>System Configuration</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Tap the dialog box to open the <ui>Company Apps</ui>.</caps:sentence>
                    <caps:sentence id="src49" class="srcSentence"> You may be asked to accept your company’s Terms and Conditions.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">Sign in using your credentials.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src51" class="srcSentence">We also recommend that you install the Company Portal app, which lets you easily identify and get the company apps that are relevant to you and your role.</caps:sentence>
                <caps:sentence id="src52" class="srcSentence"> Depending on how your company  configured Intune, the Company Portal app may have been installed as part of your enrollment process.</caps:sentence>
                <caps:sentence id="src53" class="srcSentence"> To check if you have the app, look for <ui>Company Portal</ui> in your apps list.</caps:sentence>
                <caps:sentence id="src54" class="srcSentence"> If you don't see the Company Portal in your list of apps, follow these steps to install it.</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">Tap <ui>Start</ui> &gt; <ui>Store</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">Tap <ui>Search</ui> and type <ui>company portal</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">In the list of results, tap <ui>Company Portal</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">Tap <ui>Company Portal</ui> &gt; <ui>Install</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false" address="BKMK_enrollment_81">
            <title>
              <caps:sentence id="src59" class="srcSentence">Windows Phone 8.1</caps:sentence>
            </title>
            <content>
              <para></para>
              <para>
                <caps:sentence id="src60" class="srcSentence">To enroll your device in Intune, follow the instructions that apply to your company:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="#BKMK_comp_allows_cp">If your company lets you use the Company Portal from the Windows Store</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="#BKMK_comp_doesnt_allow_cp">If you aren’t allowed to access the Windows Store from your Windows Phone, or if you don’t have a Microsoft Account</link>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section address="BKMK_comp_allows_cp" expanded="false">
                <title>
                  <caps:sentence id="src61" class="srcSentence">If your company lets you use the Company Portal from the Windows Store</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">Install the Company Portal app on your device:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">Tap <ui>Start</ui> &gt; <ui>Store</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">Tap <ui>Search</ui> and type <ui>company portal</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src65" class="srcSentence">In the list of results, tap <ui>Company Portal</ui>.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="89b255ef-e266-416d-a63b-9e1f7900d774"></image>
                      </mediaLink>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">Tap <ui>Company Portal </ui> &gt; <ui>Install</ui>.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="384372c5-bb31-40db-9026-fa46f75fd0f3"></image>
                      </mediaLink>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">Enroll your device:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">On the device, open the <ui>Microsoft Intune Company Portal</ui> app.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">Provide your credentials.</caps:sentence>
                        <caps:sentence id="src70" class="srcSentence"> You may be asked to accept your company’s Terms and Conditions, if applicable.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">Swipe to <ui>My Devices</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src72" class="srcSentence">Tap <ui>Tap to enroll or identify this device</ui>.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="2337ae7a-7c04-4dcc-bab4-dbe8b08fd30a"></image>
                      </mediaLink>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src73" class="srcSentence">Tap <ui>Enroll this device</ui>.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="c328bf4a-44a3-48c4-8656-0af5d1350195"></image>
                      </mediaLink>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">Tap <ui>Add account</ui>.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="39691416-afe3-411a-9e0b-7c642f0c5241"></image>
                      </mediaLink>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src75" class="srcSentence">Enter additional information as requested and then tap <ui>sign in</ui> to complete the enrollment.</caps:sentence>
                        <caps:sentence id="src76" class="srcSentence"> You should now see your workplace account listed on the <ui>Settings</ui> &gt; <ui>Workplace</ui> page.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="75f82638-825d-4ea5-bfc8-6899bae8964c"></image>
                      </mediaLink>
                    </listItem>
                  </list>
                </content>
              </section>
              <section address="BKMK_comp_doesnt_allow_cp">
                <title>
                  <caps:sentence id="src77" class="srcSentence">If you aren’t allowed to access the Windows Store from your Windows Phone, or if you don’t have a Microsoft Account</caps:sentence>
                </title>
                <content>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src78" class="srcSentence">Tap <ui> Settings</ui> &gt; <ui>workplace</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src79" class="srcSentence">Tap <ui>add account</ui>, and then sign in using your work account.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">Enter additional information as requested, and then tap <ui>sign in</ui> to complete the enrollment.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">If prompted to install the company app or Hub, make sure the relevant box is checked and then tap <ui>done</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">If your IT admin has configured the Company Portal to be installed  during enrollment, you will see the Company Portal appear in your app list.</caps:sentence>
                  </para>
                </content>
              </section>
            </sections>
          </section>
          <section expanded="true" address="BKMK_enrollment_wp8">
            <title>
              <caps:sentence id="src83" class="srcSentence">Windows Phone 8</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src84" class="srcSentence">Enroll your device:</caps:sentence>
              </para>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">On the device, tap <ui> Settings</ui> &gt; <ui>company apps</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">Tap <ui>add account</ui>, and then sign in using your work account.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">After the account is successfully added, you should be prompted to install the company app or Hub.</caps:sentence>
                    <caps:sentence id="src88" class="srcSentence"> Make sure the relevant box is checked and then tap <ui>done</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src89" class="srcSentence">The Company Portal will appear in your app list after it is installed.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <maml:section expanded="true" address="BKMK_win_install_comp_apps" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src90" class="srcSentence">Install company apps</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src91" class="srcSentence">In <maml:ui>Apps</maml:ui>, select an app.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src92" class="srcSentence">Tap <maml:ui>Store</maml:ui> &gt; <maml:ui>install</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section expanded="true" address="BKMK_win_whatis_cp_website">
        <title>
          <caps:sentence id="src93" class="srcSentence">What is the Company Portal website?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src94" class="srcSentence">The Company Portal website is your company’s web interface that you use to  manage your work computers and devices, and your personal computers and devices that you choose to use at work.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src95" class="srcSentence">Once you add your computer or device to the Company Portal, you can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src96" class="srcSentence">Browse for and download company apps</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src97" class="srcSentence">Manage devices that you have added to the Company Portal</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src98" class="srcSentence">Find contact information for your IT administrator</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src99" class="srcSentence">When you add a computer or device to the Company Portal, some software may be installed or an app may be downloaded (depending on the device).</caps:sentence>
            <caps:sentence id="src100" class="srcSentence"> You are also giving your IT administrator permission to manage your device to help protect the company information on the device.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="true" address="BKMK_win_encrypt_device">
        <title>
          <caps:sentence id="src101" class="srcSentence">Encrypt your device</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src102" class="srcSentence">You can encrypt your device either by adding a Microsoft account or by enabling BitLocker.</caps:sentence>
          </para>
          <para>
            <ui>
              <caps:sentence id="src103" class="srcSentence">Option 1: Add a Microsoft account</caps:sentence>
            </ui>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src104" class="srcSentence">Search for, then start the <ui>PC Settings</ui> app.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src105" class="srcSentence">Click <ui>Accounts</ui> &gt; <ui>Your account</ui>, and then click <ui>Connect to a Microsoft account</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src106" class="srcSentence">Follow the instructions shown.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src107" class="srcSentence">Ensure that your device is enrolled with <token>wit_firstref</token> by following the instructions in <externalLink><linkText>Enroll your device to use it at work</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=519071</linkUri></externalLink>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <ui>
              <caps:sentence id="src108" class="srcSentence">Option 2: Enable BitLocker</caps:sentence>
            </ui>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src109" class="srcSentence">Search for, then start the <ui>Manage BitLocker</ui> app.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src110" class="srcSentence">Click <ui>Turn on BitLocker</ui>, then follow the instructions shown to encrypt each of your drives.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src111" class="srcSentence">Ensure that your device is enrolled with <token>wit_firstref</token> by following the instructions in <externalLink><linkText>Enroll your device to use it at work</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=519071</linkUri></externalLink>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <maml:section expanded="true" address="BKMK_win_unenroll_device" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src112" class="srcSentence">Unenroll your device from Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src113" class="srcSentence">If you enrolled in Intune, but no longer want to use your device for work or school and don't need to access work or school email, apps, or other resources, you need to unenroll your device.</caps:sentence>
            <caps:sentence id="src114" class="srcSentence">   Once you unenroll your device from Intune, you will no longer be able to access these resources.</caps:sentence>
          </maml:para>
          <maml:list class="bullet">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src115" class="srcSentence">From your apps list, tap the <maml:ui>Company Portal</maml:ui> app.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src116" class="srcSentence">Sign in using your work or school credentials.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src117" class="srcSentence">In <maml:ui>My Devices</maml:ui>, select the device you want to unenroll.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src118" class="srcSentence">Tap <maml:ui>Remove</maml:ui> &gt; <maml:ui>Remove</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section expanded="true" address="BKMK_win_erase_lost_device">
        <title>
          <caps:sentence id="src119" class="srcSentence">Reset (erase) your lost or stolen device</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src120" class="srcSentence">If your phone is lost or stolen, you can reset it to factory defaults.</caps:sentence>
          </para>
          <alert class="warning">
            <para>
              <caps:sentence id="src121" class="srcSentence">Resetting a device to factor defaults removes both your personal and work information from it.</caps:sentence>
            </para>
          </alert>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src122" class="srcSentence">In your browser, open your Company Portal, and sign in to your work account.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src123" class="srcSentence">Under <ui>My Devices</ui>, click the lost or stolen device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src124" class="srcSentence">Click <ui>Reset</ui> &gt; <ui>Reset</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src125" class="srcSentence">If you are unable to reset your lost or stolen device, contact IT to reset it for you.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section address="BKMK_what_happns_enroll_all">
        <title>
          <caps:sentence id="src126" class="srcSentence">What happens when I install the Company Portal app and enroll my device in Intune?</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section address="BKMK_what_happens_w10" expanded="true">
            <title>
              <caps:sentence id="src127" class="srcSentence">What happens when I install the Company Portal app and enroll my Windows 10 device in Intune?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src128" class="srcSentence">When you install the Company Portal app and then use the app to enroll your Windows 10 Enterprise  or Professional device in Intune, you can then use the Company Portal app to:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src129" class="srcSentence">Access the company’s network, and your email and work files</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">Get company apps from the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src131" class="srcSentence">Automatically configure your company email account</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src132" class="srcSentence">Reset your phone to factory settings if it is lost or stolen</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src133" class="srcSentence">For the steps to enroll, see <link xlink:href="#BKMK_enrollment_w10">Windows 10</link>.</caps:sentence>
                <caps:sentence id="src134" class="srcSentence"> For information about what your IT admin can and can't see on your device, see <link xlink:href="#BKMK_win_what_IT_can_see">What can my IT admin see when I enroll my device in Intune?</link></caps:sentence>
              </para>
              <para>
                <caps:sentence id="src135" class="srcSentence">When you add a computer:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">You’ll have some software installed on your computer to make it possible for your IT administrator to manage the computer, and make it possible for you to get to company resources like apps and support information.</caps:sentence>
                    <caps:sentence id="src137" class="srcSentence"> This software may be updated automatically by your IT administrator.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src138" class="srcSentence">
                      <token>wit_firstref</token> Endpoint Protection may be installed on your computer.</caps:sentence>
                    <caps:sentence id="src139" class="srcSentence"> This is software that checks for viruses and malware.</caps:sentence>
                    <caps:sentence id="src140" class="srcSentence"> For more information, please refer to the <externalLink><linkText>Endpoint Protection Privacy Statement</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=247324</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">Your IT administrator can take an inventory of all of the software installed on the computer, including software you have personally installed.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src142" class="srcSentence">Require you to accept terms and conditions.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src143" class="srcSentence">Your IT administrator can collect or delete data from your computer’s hard drive.</caps:sentence>
                    <caps:sentence id="src144" class="srcSentence"> Your IT administrator could also delete the entire hard drive.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src145" class="srcSentence">Your IT administrator can install apps and updates on your computer.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src146" class="srcSentence">Your IT administrator may enforce policies on the computer.</caps:sentence>
                    <caps:sentence id="src147" class="srcSentence"> For example, you might be required to set a password or PIN on the computer, which may lock you out of the computer, or delete all data from your computer’s hard drive, if there are too many incorrect password attempts.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_what_happens_w81">
            <title>
              <caps:sentence id="src148" class="srcSentence">What happens when I install the Company Portal app and enroll my Windows 8.1 or Windows RT device in Intune?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src149" class="srcSentence">When you install the Company Portal app and then use the app to enroll your Windows 8.1 Enterprise  or Professional or Windows RT device in Intune, you can then use the Company Portal app to:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src150" class="srcSentence">Access the company’s network, and your email and work files</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">Get company apps from the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">Automatically configure your company email account</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">Reset your phone to factory settings if it is lost or stolen</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src154" class="srcSentence">For the steps to enroll, see <link xlink:href="#BKMK_enrollment_w81orwrt81">Windows 8.1 or Windows RT 8.1</link>.</caps:sentence>
                <caps:sentence id="src155" class="srcSentence"> For information about what your IT admin can and can't see on your device, see <link xlink:href="#BKMK_win_what_IT_can_see">What can my IT admin see when I enroll my device in Intune?</link></caps:sentence>
              </para>
              <para>
                <caps:sentence id="src156" class="srcSentence">When you add a computer:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">You’ll have some software installed on your computer to make it possible for your IT administrator to manage the computer, and make it possible for you to get to company resources like apps and support information.</caps:sentence>
                    <caps:sentence id="src158" class="srcSentence"> This software may be updated automatically by your IT administrator.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">
                      <token>wit_firstref</token> Endpoint Protection may be installed on your computer.</caps:sentence>
                    <caps:sentence id="src160" class="srcSentence"> This is software that checks for viruses and malware.</caps:sentence>
                    <caps:sentence id="src161" class="srcSentence"> For more information, please refer to the <externalLink><linkText>Endpoint Protection Privacy Statement</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=247324</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">Your IT administrator can take an inventory of all of the software installed on the computer, including software you have personally installed.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">Require you to accept terms and conditions.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src164" class="srcSentence">Your IT administrator can collect or delete data from your computer’s hard drive.</caps:sentence>
                    <caps:sentence id="src165" class="srcSentence"> Your IT administrator could also delete the entire hard drive.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">Your IT administrator can install apps and updates on your computer.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">Your IT administrator may enforce policies on the computer.</caps:sentence>
                    <caps:sentence id="src168" class="srcSentence"> For example, you might be required to set a password or PIN on the computer, which may lock you out of the computer, or delete all data from your computer’s hard drive, if there are too many incorrect password attempts.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_what_happens_phone8" expanded="false">
            <title>
              <caps:sentence id="src169" class="srcSentence">What happens when I install the Company Portal app and enroll my Windows Phone 8.1 or Windows Phone 8 device in Intune?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src170" class="srcSentence">When you install the Company Portal app and then use the app to enroll your Windows Phone 8.1 or Windows Phone 8 device in Intune, you can then use the Company Portal app to:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">Access the company’s network, and your email and work files</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">Get company apps from the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src173" class="srcSentence">Automatically configure your company email account</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src174" class="srcSentence">Reset your phone to factory settings if it is lost or stolen</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src175" class="srcSentence">For the steps to enroll, see<link xlink:href="#BKMK_enrollment_81">Windows Phone 8.1</link> or <link xlink:href="#BKMK_enrollment_wp8">Windows Phone 8</link>.</caps:sentence>
                <caps:sentence id="src176" class="srcSentence">  For information about what your IT admin can and can't see on your device, see <link xlink:href="#BKMK_win_what_IT_can_see">What can my IT admin see when I enroll my device in Intune?</link>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src177" class="srcSentence">When you add your Windows Phone device, you are giving your IT administrator permission to access the device.</caps:sentence>
                <caps:sentence id="src178" class="srcSentence"> They can do things like:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">Reset your device back to manufacturer’s default settings.</caps:sentence>
                    <caps:sentence id="src180" class="srcSentence"> This is helpful if the device is lost or stolen.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src181" class="srcSentence">Remove all company related data and business apps that were installed.</caps:sentence>
                    <caps:sentence id="src182" class="srcSentence"> Your personal data and settings aren’t removed.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">Force you to have a password or PIN on the device, which may lock you out of the device, or reset your device back to manufacturer’s default settings, which may include the deletion of data, if there are too many incorrect password attempts.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">Force all the data on the device to be encrypted.</caps:sentence>
                    <caps:sentence id="src185" class="srcSentence"> This helps protect the data if the device is lost or stolen.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">Require you to accept terms and conditions.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">Disable the SD card.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src188" class="srcSentence">Install updates to apps on your device.</caps:sentence>
                    <caps:sentence id="src189" class="srcSentence"> This applies to updates only.</caps:sentence>
                    <caps:sentence id="src190" class="srcSentence"> Your IT administrator cannot force new apps to install on your device, but you can choose to install apps you see in the company portal.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">After your device is added to the company portal, approximately every 8 hours it will: </caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src192" class="srcSentence">Download any policy or app updates that your IT administrator has made available.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src193" class="srcSentence">Send any hardware inventory updates.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src194" class="srcSentence">Send any company app inventory updates.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_what_happens_vista">
            <title>
              <caps:sentence id="src195" class="srcSentence">What happens when I install the Company Portal app and enroll my Windows 7 or  Vista device in Intune?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src196" class="srcSentence">When you install the Company Portal app and then use the app to enroll your Windows 7 or Vista device in Intune, you can then use the Company Portal app to:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src197" class="srcSentence">Access the company’s network, and your email and work files</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src198" class="srcSentence">Get company apps from the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src199" class="srcSentence">Automatically configure your company email account</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">Reset your phone to factory settings if it is lost or stolen</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src201" class="srcSentence">For information about what your IT admin can and can't see on your device, see <link xlink:href="#BKMK_win_what_IT_can_see">What can my IT admin see when I enroll my device in Intune?</link>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src202" class="srcSentence">When you add a computer:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src203" class="srcSentence">You’ll have some software installed on your computer to make it possible for your IT administrator to manage the computer, and make it possible for you to get to company resources like apps and support information.</caps:sentence>
                    <caps:sentence id="src204" class="srcSentence"> This software may be updated automatically by your IT administrator.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src205" class="srcSentence">
                      <token>wit_firstref</token> Endpoint Protection may be installed on your computer.</caps:sentence>
                    <caps:sentence id="src206" class="srcSentence"> This is software that checks for viruses and malware.</caps:sentence>
                    <caps:sentence id="src207" class="srcSentence"> For more information, please refer to the <externalLink><linkText>Endpoint Protection Privacy Statement</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=247324</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src208" class="srcSentence">Your IT administrator can take an inventory of all of the software installed on the computer, including software you have personally installed.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src209" class="srcSentence">Require you to accept terms and conditions.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src210" class="srcSentence">Your IT administrator can collect or delete data from your computer’s hard drive.</caps:sentence>
                    <caps:sentence id="src211" class="srcSentence"> Your IT administrator could also delete the entire hard drive.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">Your IT administrator can install apps and updates on your computer.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src213" class="srcSentence">Your IT administrator may enforce policies on the computer.</caps:sentence>
                    <caps:sentence id="src214" class="srcSentence"> For example, you might be required to set a password or PIN on the computer, which may lock you out of the computer, or delete all data from your computer’s hard drive, if there are too many incorrect password attempts.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_win_what_IT_can_see">
        <title>
          <caps:sentence id="src215" class="srcSentence">What can my IT admin see when I enroll my device in Intune?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src216" class="srcSentence">When  you enroll your device in Intune, you are giving your IT administrator permission to manage your device to help protect the company information on the device.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src217" class="srcSentence">IT cannot see</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src218" class="srcSentence">IT can see</caps:sentence>
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
                        <caps:sentence id="src219" class="srcSentence">Call history</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src220" class="srcSentence">Text messages</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src221" class="srcSentence">Personal email, contacts, and calendar</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src222" class="srcSentence">Web history</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src223" class="srcSentence">Location</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src224" class="srcSentence">Camera roll</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src225" class="srcSentence">Personal data</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src226" class="srcSentence">Owner</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src227" class="srcSentence">Device name</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src228" class="srcSentence">Serial number</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src229" class="srcSentence">Manufacturer</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src230" class="srcSentence">Model</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src231" class="srcSentence">Operating system</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src232" class="srcSentence">Company apps</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src233" class="srcSentence">Personal apps</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>