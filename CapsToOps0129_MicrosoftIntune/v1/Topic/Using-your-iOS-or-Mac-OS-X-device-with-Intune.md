---
title: Usar un dispositivo iOS con Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3d648819-b866-412b-bd19-ac4505eb5eaf
robots: noindex
---
# Usar un dispositivo iOS con Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence sentenceid="75a37d64ef8c3c83c8e12236a6e20471" id="tgt1" class="tgtSentence">Para las tareas que necesita realizar en el dispositivo iOS, si la empresa usa Microsoft Intune, siga estos pasos:</caps:sentence>
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
                      <link xlink:href="#BKMK_ios_signin_cp">Install and sign in to the Company Portal app</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_enroll_your_device">Enroll your device in Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_what_happ_enroll">What happens when I install the Company Portal app and enroll my device in Intune?</link>
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
                      <link xlink:href="#BKMK_ios_whatis_cp_website">What is the Company Portal website and what can I do with it?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_erase_lost_device">Reset (erase) your lost or stolen device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_data_collect">Turn off Microsoft usage data collection</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_unenroll_device">Unenroll your device from Intune</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c6dc0f40f1debc9ce66e6c01a76742f2" id="tgt6" class="tgtSentence">Solucionar problemas con el dispositivo </caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_fix_issues">Fix issues when your device is enrolled in Intune</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <maml:section expanded="true" address="BKMK_ios_signin_cp" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="fcc6e39b54334b6698afbc39c70d2d83" id="tgt7" class="tgtSentence">Instale e inicie sesión en la aplicación Portal de empresa de Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="bcc9ebff81099e0055eecc4f9b04f424" id="tgt8" class="tgtSentence">El Portal de empresa es una aplicación que se instala en el dispositivo y que le proporciona acceso a las aplicaciones, correo electrónico y red de su empresa o centro educativo.</caps:sentence>
            <caps:sentence sentenceid="c4be065ac83e30901401d1098791a413" id="tgt9" class="tgtSentence">  Antes de que pueda obtener acceso, debe instalar la aplicación Portal de empresa y, a continuación, usar la aplicación para inscribir el dispositivo en Microsoft Intune.</caps:sentence>
            <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt10" class="tgtSentence"> Para obtener más información, consulte <maml:link xlink:href="#BKMK_ios_what_happ_enroll">¿Qué ocurrirá cuando instale la aplicación Portal de empresa e inscriba el dispositivo en Intune?</maml:link>.</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt11" class="tgtSentence">Abra la <maml:ui>Tienda de aplicaciones</maml:ui> y busque <maml:ui>Intune</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="23bd19fcedd382955bc35818765ace04" id="tgt12" class="tgtSentence">Descargue la aplicación <maml:ui>Portal de empresa de Microsoft Intune</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="6d9d1904-1462-4c29-a3e6-daccf5b8ec7e"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="64df2b8e2dde54d36299361d4189328a" id="tgt13" class="tgtSentence">Abra la aplicación Portal de empresa, escriba el correo electrónico y la contraseña del trabajo o del centro educativo y, a continuación, pulse <maml:ui>Iniciar sesión</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:para>
                <caps:sentence sentenceid="266b3e7b012119fb91d6962911283bb6" id="tgt14" class="tgtSentence">Si va a iniciar sesión en la aplicación Portal de empresa por primera vez y su empresa o centro educativo usan Intune, se le solicitará que inscriba su dispositivo en Intune.</caps:sentence>
                <caps:sentence sentenceid="5e948074b31b8a9455d72a9372e2f24d" id="tgt15" class="tgtSentence"> Para inscribirlo, siga los pasos que encontrará en <maml:link xlink:href="#BKMK_ios_enroll_your_device">Inscripción del dispositivo en Intune</maml:link>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section address="BKMK_ios_enroll_your_device" expanded="true" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="77956432d1ee5eec1f0a618647bbc6a4" id="tgt16" class="tgtSentence">Inscripción del dispositivo en Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="f420ae496d933fa61a4e7dbd20f20bf2" id="tgt17" class="tgtSentence">Si inscribe el dispositivo en Intune, podrá obtener acceso a la red de la empresa, al correo electrónico y archivos del trabajo y, asimismo, podrá conseguir aplicaciones de empresa.</caps:sentence>
            <caps:sentence sentenceid="e518b87c92ded097371c65588339b8cd" id="tgt18" class="tgtSentence"> Si desea obtener más información cuando inscriba su dispositivo, consulte <maml:link xlink:href="#BKMK_ios_what_happ_enroll">¿Qué ocurrirá cuando instale la aplicación Portal de empresa e inscriba el dispositivo en Intune?</maml:link>.</caps:sentence>
          </maml:para>
          <maml:para>
            <caps:sentence sentenceid="94f1492f6d274db2e649a11db5e4d80a" id="tgt19" class="tgtSentence">Para inscribir su dispositivo:</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="34467dfcfb57ed5e287c4f9586a2a48e" id="tgt20" class="tgtSentence">Siga los pasos indicados en <maml:link xlink:href="#BKMK_ios_signin_cp">Instale e inicie sesión en la aplicación Portal de empresa de Intune</maml:link>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt21" class="tgtSentence">En la pantalla <maml:ui>Inscripción de dispositivos</maml:ui>de la aplicación Portal de empresa, pulse <maml:ui>Inscribir</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="0e518c1a-34a8-4b41-bb1d-d178fc7d1b1f"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt22" class="tgtSentence">En la pantalla <maml:ui>Instalar perfil</maml:ui>, pulse <maml:ui>Instalar</maml:ui> y escriba su contraseña, si se le pide.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="08071677-4fc9-4f8d-988c-096ad4fc307b"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="4c3e12f452674bf9900d2c3dd5d0ea85" id="tgt23" class="tgtSentence"> Pulse <maml:ui>Instalar</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="2952ad68-e279-4c29-8276-af6b0d38650b"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="4c3e12f452674bf9900d2c3dd5d0ea85" id="tgt24" class="tgtSentence"> Pulse <maml:ui>Instalar</maml:ui> para indicar que ha leído la advertencia.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="565f3b1a-671a-4b8c-acfe-967d12e6bdcc"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="4c3e12f452674bf9900d2c3dd5d0ea85" id="tgt25" class="tgtSentence"> Pulse <maml:ui>De confianza</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="17627759-2f98-4847-b72d-33b3defd1ef4"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt26" class="tgtSentence">Pulse <maml:ui>Listo</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="5e9d1770-83cd-4df0-b0a9-3f24ee7792f7"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt27" class="tgtSentence">Pulse en <maml:ui>Aceptar</maml:ui>.</caps:sentence>
                <caps:sentence sentenceid="15afcd6e39bd01b0c0fe0a0b0212d290" id="tgt28" class="tgtSentence"> El dispositivo ya está inscrito en Intune.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="818c0228-bbe4-4760-9590-bc9146820ab5"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section address="BKMK_ios_what_happ_enroll">
        <title>
          <caps:sentence sentenceid="c7771a0e09cd91e94fb6776ff1223ac3" id="tgt29" class="tgtSentence">¿Qué ocurrirá cuando instale la aplicación Portal de empresa e inscriba el dispositivo en Intune?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f0401535f7b1ac877b8f6af14bd6c40d" id="tgt30" class="tgtSentence">Empiece instalando la aplicación Portal de empresa y, a continuación, use la aplicación para inscribir el dispositivo en Intune.</caps:sentence>
            <caps:sentence sentenceid="9af3ed7432137e078ac63133e9bdc49a" id="tgt31" class="tgtSentence"> Una vez que el dispositivo esté inscrito, puede usar la aplicación Portal de empresa para:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="cd1a40a617eb283f621ef494fdaa498f" id="tgt32" class="tgtSentence">Acceder a la red, el correo electrónico y los archivos de trabajo de la empresa</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="365f2777fae357fc28b1489affab4a54" id="tgt33" class="tgtSentence">Obtener aplicaciones de empresa desde el portal de la empresa</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7c7476a0520e0468f40a091eecb0d594" id="tgt34" class="tgtSentence">Configurar automáticamente su cuenta de correo electrónico de la empresa</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="66b07c74bf99f92822a9939daafde7d3" id="tgt35" class="tgtSentence">Restablecer su teléfono a la configuración de fábrica si lo pierde o se lo roban</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="9580373c6a8f78a774ff06c526b5e360" id="tgt36" class="tgtSentence">Cuando inscribe su dispositivo en Intune, el administrador de TI tiene permiso para administrar el dispositivo, a fin de ayudarle a proteger la información de la empresa que tiene en el mismo.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49b5c06f816b80fa0b53001b7e064dd0" id="tgt37" class="tgtSentence">TI no puede ver</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="919967a6e68fc799764ccfadd49d0d82" id="tgt38" class="tgtSentence">TI puede ver</caps:sentence>
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
                        <caps:sentence sentenceid="7b15a2dc20f223897228983bcb839a0d" id="tgt39" class="tgtSentence">Historial de llamadas</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b5c1e4334dd619fce44e7a047bd05a8d" id="tgt40" class="tgtSentence">Mensajes de texto</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="936249fa98a3357097ff1f12312225b4" id="tgt41" class="tgtSentence">Correo electrónico personal, contactos y calendario</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="827a82394f446cc4d02c0fd5e61f331b" id="tgt42" class="tgtSentence">Historial web</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d5189de027922f81005951e6efe0efd5" id="tgt43" class="tgtSentence">Ubicación</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b99bbccd22c782c7f7019bad4a0628f2" id="tgt44" class="tgtSentence">Álbum de cámara</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2c5a2582707f1495992f8b6befe92a6c" id="tgt45" class="tgtSentence">Datos personales</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="72122ce96bfec66e2396d2e25225d70a" id="tgt46" class="tgtSentence">Propietario</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="712778275c556c187fb77a2b8a2af8c4" id="tgt47" class="tgtSentence">Nombre del dispositivo</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c9f4029ce9dcf8ff7f8f1b70edead843" id="tgt48" class="tgtSentence">Número de serie</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c2904bca62b22443d6cf5e9d89cab204" id="tgt49" class="tgtSentence">Fabricante</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="20f35e630daf44dbfa4c3f68f5399d8c" id="tgt50" class="tgtSentence">Modelo</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d83f147fd8043b67aa813f44f597b39b" id="tgt51" class="tgtSentence">Sistema operativo</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="93a4cf66e1c393e83e3c39b8446f1b71" id="tgt52" class="tgtSentence">Aplicaciones de empresa</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a2da362c93e6fb8f4d57947fe2b2d8fd" id="tgt53" class="tgtSentence">Aplicaciones personales</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="87ad91150c1a3f3a735dfa76718c903b" id="tgt54" class="tgtSentence">Cuando el dispositivo esté inscrito, el Administrador de TI podrá:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="3b4e79bf899b6aaddd519b0e6a8dfadd" id="tgt55" class="tgtSentence">Restablecer la configuración predeterminada de fábrica del dispositivo, si este se le pierde o se lo roban.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0dc37493c4cb02c084f4aa01567938fa" id="tgt56" class="tgtSentence">Quitar todos los datos relacionados con la empresa y las aplicaciones empresariales que se instalaron.</caps:sentence>
                <caps:sentence sentenceid="4764910b571c675b37c4a88b110b1379" id="tgt57" class="tgtSentence"> Los datos personales y la configuración no se quitan.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3dadb4ca038f02975523eaee5a2f3ada" id="tgt58" class="tgtSentence">Exigir el uso de una contraseña o un PIN en el dispositivo.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1aa6cfa75e3c98c83374293c4279f76" id="tgt59" class="tgtSentence">Debe aceptar los términos y condiciones.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f9877cfa9f701abb70b52dc01c3d35e7" id="tgt60" class="tgtSentence">Habilitar o deshabilitar la cámara en el dispositivo.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c097c9b938d8422cf97d12d1efc19333" id="tgt61" class="tgtSentence">Habilitar o deshabilitar la exploración web en el dispositivo.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5362d8d186d4d7498f369f45a4547e14" id="tgt62" class="tgtSentence">Habilitar o deshabilitar la copia de seguridad en iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c13f97c1c50716363f864c2b1cce7d9e" id="tgt63" class="tgtSentence">Habilitar o deshabilitar la sincronización de documentos con iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="79bb1f540ce994a1ab04f0803c3f033a" id="tgt64" class="tgtSentence">Habilitar o deshabilitar la transmisión de fotos a iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4398056c852a7df9e0825a7d639a7ca5" id="tgt65" class="tgtSentence">Habilitar o deshabilitar la movilidad de datos en el dispositivo.</caps:sentence>
                <caps:sentence sentenceid="49bd0633453334131f4aad248ba87925" id="tgt66" class="tgtSentence"> Si se permite la movilidad de datos, podrían aplicarse cargos por movilidad.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ba05f106b31276b3e2bf67f2114f974f" id="tgt67" class="tgtSentence">Habilitar o deshabilitar la movilidad de voz en el dispositivo.</caps:sentence>
                <caps:sentence sentenceid="98d43910f63da52b360113bdb24faa04" id="tgt68" class="tgtSentence"> Si se permite la movilidad de voz, podrían aplicarse cargos por movilidad.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f1715a111d5a7fc544a6292a3e7c22be" id="tgt69" class="tgtSentence">Habilitar o deshabilitar en el dispositivo la sincronización automática de archivos en modo de movilidad.</caps:sentence>
                <caps:sentence sentenceid="9662708499169149cc1ab97ce2053f05" id="tgt70" class="tgtSentence"> Si se permite la sincronización automática de archivos, podrían aplicarse cargos por movilidad.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="d25157643cd285dd22c4250eb1198755" id="tgt71" class="tgtSentence">Para conocer los pasos necesarios para inscribir su dispositivo en Intune, consulte <link xlink:href="#BKMK_ios_enroll_your_device">Enroll your device in Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="true" address="BKMK_ios_whatis_cp_website">
        <title>
          <caps:sentence sentenceid="631be7185536cbfc0dd9092b681d30e8" id="tgt72" class="tgtSentence">¿Qué es el sitio web del Portal de empresa y qué puedo hacer con él?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt73" class="tgtSentence">El <externalLink><linkText>sitio web del Portal de empresa</linkText><linkUri>http://portal.manage.microsoft.com</linkUri></externalLink> es la interfaz web de la empresa que se usa para administrar tanto los equipos y dispositivos de trabajo como aquellos dispositivos personales que usa para trabajar.</caps:sentence>
            <caps:sentence sentenceid="70037d25cd497b5572e18d1bc35334bc" id="tgt74" class="tgtSentence"> La mayoría de tareas que puede realizar mediante la aplicación Portal de empresa que instaló en el dispositivo, también puede realizarlas en este sitio web .</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="14d658610fe447e446e50ce288d1edc1" id="tgt75" class="tgtSentence">Puede llevar a cabo las siguientes tareas desde el sitio web del Portal de empresa:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="3dc0b17542da2ec9d90ff0965d19aef1" id="tgt76" class="tgtSentence">Buscar y descargar aplicaciones de empresa</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f82609801e7080daebaa60a46cd06e57" id="tgt77" class="tgtSentence">Cambiar el nombre del dispositivo</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2e254e163be6b2905cf22931f4eb4fe0" id="tgt78" class="tgtSentence">Anular la inscripción del dispositivo en Intune</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="680b802dd6afc46294bf85411f86cccf" id="tgt79" class="tgtSentence">Restablecer la configuración predeterminada de fábrica del dispositivo móvil</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ed64c84b76d070c3000586dc8cade916" id="tgt80" class="tgtSentence">Buscar información de contacto para el administrador de TI</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_ios_erase_lost_device">
        <title>
          <caps:sentence sentenceid="c06b6d82e53b630aa8f19483e6047696" id="tgt81" class="tgtSentence">Restablecer (borrar) el dispositivo perdido o robado</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="245c5877e7e6a3fcf2677b171d1a6d0d" id="tgt82" class="tgtSentence">Si se pierde o roban un teléfono con una inscripción a Intune, puede restablecer la configuración predeterminada de fábrica a través de la aplicación del Portal de empresa desde otro dispositivo.</caps:sentence>
          </para>
          <alert class="warning">
            <para>
              <caps:sentence sentenceid="dcc73e1b3a07aa18eea2923969792157" id="tgt83" class="tgtSentence">Restablecer los valores predeterminados de fábrica del dispositivo quita su información personal y del trabajo de este.</caps:sentence>
            </para>
          </alert>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="c249a580a5b0e0bb1a4d4d9fbde2c950" id="tgt84" class="tgtSentence">En la aplicación del Portal de empresa, en <ui>Mis dispositivos</ui>, seleccione el dispositivo que quiera borrar.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="298eb8b721760a1ff208e241dcde7e9b" id="tgt85" class="tgtSentence">Pulse <ui>Restablecer</ui> &gt; <ui>Restablecer</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="843a6cd618daa054e4a48332cc86acbe" id="tgt86" class="tgtSentence">Si no puede restablecer el dispositivo perdido o robado, póngase en contacto con TI para restablecerlo por usted.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <maml:section address="BKMK_ios_data_collect" expanded="true" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="b321241f2502b5448f5ba9814524413f" id="tgt87" class="tgtSentence">Desactivar la recopilación de datos de uso de Microsoft</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="613c5729b5d70fe8a98c7d50505d4ea7" id="tgt88" class="tgtSentence">Para mejorar sus productos y servicios, Microsoft recopila automáticamente datos anónimos sobre la confiabilidad, el rendimiento y el uso de la aplicación Portal de empresa.</caps:sentence>
            <caps:sentence sentenceid="4150fed1487d3933fae6b75759c4e79e" id="tgt89" class="tgtSentence"> Puede desactivar la recopilación de datos configurando el uso de datos en la aplicación Portal de empresa.</caps:sentence>
            <caps:sentence sentenceid="e1193143312e8b74386d45adac2e9d42" id="tgt90" class="tgtSentence"> Los administradores de TI no tienen ningún control sobre la recopilación de estos datos y no pueden cambiar la selección de este ajuste.</caps:sentence>
          </maml:para>
        </maml:content>
      </maml:section>
      <section address="BKMK_ios_unenroll_device">
        <title>
          <caps:sentence sentenceid="e7334a6647a4beaf7b7148ac205d9349" id="tgt91" class="tgtSentence">Anulación de la inscripción del dispositivo en Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a0c8593b0b5f285d2c025132d17200c6" id="tgt92" class="tgtSentence">Cuando anule la inscripción del dispositivo de Intune, el dispositivo ya no podrá tener acceso a recursos de empresa e Intune ya no lo administrará.</caps:sentence>
            <caps:sentence sentenceid="8a58ef3bea6c65abe73ee3e2bc7eb650" id="tgt93" class="tgtSentence"> Para obtener más información acerca de la anulación de la inscripción sigue los pasos siguientes.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="33ec116fa4d3a05cebd927de0897af22" id="tgt94" class="tgtSentence">Para anular la inscripción del dispositivo en Intune:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="c249a580a5b0e0bb1a4d4d9fbde2c950" id="tgt95" class="tgtSentence">En la aplicación del Portal de empresa, en <ui>Mis dispositivos</ui>, seleccione el dispositivo correspondiente.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="298eb8b721760a1ff208e241dcde7e9b" id="tgt96" class="tgtSentence">Pulse <ui>Quitar</ui> &gt; <ui>Quitar</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="715a45f185a63212c320c5ddbe6feb5f" id="tgt97" class="tgtSentence">Cuando se anula la inscripción de un dispositivo de Intune, ocurre lo siguiente:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="a30b38d6fe341a32afb8c1fa2ae6f00d" id="tgt98" class="tgtSentence">El dispositivo deja de aparecer en el Portal de empresa.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="debcc4cc4b3dff0ce773acfc3cba2baa" id="tgt99" class="tgtSentence">No se podrán instalar aplicaciones desde el Portal de empresa.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8a62e1aa36796068c996249797b79a25" id="tgt100" class="tgtSentence">Dejará de aplicarse cualquier configuración que se haya modificado en el dispositivo cuando se agregó, por ejemplo, la opción para deshabilitar la cámara o exigir una determinada longitud de contraseña.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e2e05eddbfd9df781fb51550906d96c8" id="tgt101" class="tgtSentence">Es posible que deje de tener acceso en su dispositivo a algunos recursos de la empresa, como recursos compartidos de archivos o sitios web internos.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="29251bb2bd6e6f53b0484ae712b196d0" id="tgt102" class="tgtSentence">No se podrán utilizar las aplicaciones y los datos de la empresa.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8e9ba66b81a76d53ce5a21a6475c7517" id="tgt103" class="tgtSentence">No se podrá conectar a la red de su empresa mediante Wi-Fi o una red privada virtual (VPN).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7faad2ae257ea90bfa9dde6cb649cd47" id="tgt104" class="tgtSentence">Los perfiles de correo electrónico de empresa se quitan del dispositivo.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a1e7c55d94cbaa4a92d89ae197836b91" id="tgt105" class="tgtSentence">Los dispositivos que están configurados para el correo electrónico no aparecerán en el sitio web o en la aplicación Portal de empresa.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section address="BKMK_ios_fix_issues">
        <title>
          <caps:sentence sentenceid="b04d8428c19a919568ee64f356b58ed8" id="tgt106" class="tgtSentence">Corregir problemas cuando el dispositivo está inscrito en Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="14d9b1747154aba835a2f168930e2506" id="tgt107" class="tgtSentence">Si se produce un error mientras usa la aplicación Portal de empresa, puede enviar información sobre el error y que así le sea más fácil a su administrador de TI solucionar el problema.</caps:sentence>
            <caps:sentence sentenceid="41058755961023d4116f03f243580ef1" id="tgt108" class="tgtSentence"> Puede enviar información de errores de maneras diferentes:</caps:sentence>
          </para>
          <maml:list class="bullet" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="ee20a7ba889a5cb252dfa456cd075774" id="tgt109" class="tgtSentence">Pulsando <maml:ui>Informe</maml:ui> en los mensajes de alerta de error.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="ee20a7ba889a5cb252dfa456cd075774" id="tgt110" class="tgtSentence">Pulsando <maml:ui>Enviar un informe de diagnóstico</maml:ui> en la pantalla “Acerca de” de la aplicación Portal de empresa</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="2856feee4e3cbc9d037d7caa3dc09853" id="tgt111" class="tgtSentence">Agitando el dispositivo mientras se encuentra en la aplicación Portal de empresa y, a continuación, pulsando en <maml:ui>Correo electrónico</maml:ui> cuando aparezca la alerta de diagnóstico.</caps:sentence>
                <caps:sentence sentenceid="a33a5b0675fc3271d2a688ea32558807" id="tgt112" class="tgtSentence"> Si la alerta no aparece cuando agite el dispositivo, abra <maml:ui>Configuración</maml:ui> &gt; <maml:ui>Portal de empresa</maml:ui> y asegúrese de que la opción <maml:ui>Gesto de sacudida</maml:ui> está activada.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use these steps for tasks that you need to do on your iOS device when your company is using Microsoft Intune:</caps:sentence>
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
                      <link xlink:href="#BKMK_ios_signin_cp">Install and sign in to the Company Portal app</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_enroll_your_device">Enroll your device in Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_what_happ_enroll">What happens when I install the Company Portal app and enroll my device in Intune?</link>
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
                      <link xlink:href="#BKMK_ios_whatis_cp_website">What is the Company Portal website and what can I do with it?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_erase_lost_device">Reset (erase) your lost or stolen device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_data_collect">Turn off Microsoft usage data collection</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_unenroll_device">Unenroll your device from Intune</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Fix issues with your device </caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_fix_issues">Fix issues when your device is enrolled in Intune</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <maml:section expanded="true" address="BKMK_ios_signin_cp" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src7" class="srcSentence">Install and sign in to the Intune Company Portal app</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src8" class="srcSentence">The Company Portal is an app that you install on your device to give you access to your company or school apps, email, and network.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence">  Before you can get access, you must install the Company Portal app, and then  use the app to enroll your device in Microsoft Intune.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> For more information, see <maml:link xlink:href="#BKMK_ios_what_happ_enroll">What happens when I install the Company Portal app and enroll my device in Intune?</maml:link>.</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src11" class="srcSentence">Open the <maml:ui>App Store</maml:ui> and search for <maml:ui>intune</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src12" class="srcSentence">Download the <maml:ui>Microsoft Intune Company Portal</maml:ui> app.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="6d9d1904-1462-4c29-a3e6-daccf5b8ec7e"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src13" class="srcSentence">Open the Company Portal app, enter your work or school email and password, and then tap <maml:ui>Sign in</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:para>
                <caps:sentence id="src14" class="srcSentence">If you are signing into the Company Portal app for the first time, and your company or school is using Intune, you will be prompted to enroll your device in Intune.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> To enroll, follow the steps in <maml:link xlink:href="#BKMK_ios_enroll_your_device">Enroll your device in Intune</maml:link>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section address="BKMK_ios_enroll_your_device" expanded="true" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src16" class="srcSentence">Enroll your device in Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src17" class="srcSentence">Enrolling your device in Intune enables you to access the company’s network, your work email and work files, and lets you get company apps.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> For more about what happens when you enroll your device, see <maml:link xlink:href="#BKMK_ios_what_happ_enroll">What happens when I install the Company Portal app and enroll my device in Intune?</maml:link>.</caps:sentence>
          </maml:para>
          <maml:para>
            <caps:sentence id="src19" class="srcSentence">To enroll your device:</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src20" class="srcSentence">Follow the steps in  <maml:link xlink:href="#BKMK_ios_signin_cp">Install and sign in to the Intune Company Portal app</maml:link>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src21" class="srcSentence">On the <maml:ui>Device Enrollment</maml:ui> screen in the Company Portal app, tap <maml:ui>Enroll</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="0e518c1a-34a8-4b41-bb1d-d178fc7d1b1f"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src22" class="srcSentence">On the <maml:ui>Install Profile</maml:ui> screen, tap <maml:ui>Install</maml:ui>, and enter your passcode, if prompted.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="08071677-4fc9-4f8d-988c-096ad4fc307b"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src23" class="srcSentence"> Tap <maml:ui>Install</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="2952ad68-e279-4c29-8276-af6b0d38650b"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src24" class="srcSentence"> Tap <maml:ui>Install</maml:ui> to indicate that you've read the warning.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="565f3b1a-671a-4b8c-acfe-967d12e6bdcc"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src25" class="srcSentence"> Tap <maml:ui>Trust</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="17627759-2f98-4847-b72d-33b3defd1ef4"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src26" class="srcSentence">Tap <maml:ui>Done</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="5e9d1770-83cd-4df0-b0a9-3f24ee7792f7"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src27" class="srcSentence">Tap <maml:ui>OK</maml:ui>.</caps:sentence>
                <caps:sentence id="src28" class="srcSentence"> Your device is now enrolled in Intune.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="818c0228-bbe4-4760-9590-bc9146820ab5"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section address="BKMK_ios_what_happ_enroll">
        <title>
          <caps:sentence id="src29" class="srcSentence">What happens when I install the Company Portal app and enroll my device in Intune?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src30" class="srcSentence">You start by installing the Company Portal app, and then use the app to enroll your device in Intune.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> Once your device is enrolled, you  can use the Company Portal app to:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src32" class="srcSentence">Access the company’s network, and your email and work files</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src33" class="srcSentence">Get company apps from the Company Portal</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src34" class="srcSentence">Automatically configure your company email account</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src35" class="srcSentence">Reset your phone to factory settings if it is lost or stolen</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src36" class="srcSentence">When  you enroll your device in Intune, you are giving your IT administrator permission to manage your device to help protect the company information on the device.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">IT cannot see</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">IT can see</caps:sentence>
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
                        <caps:sentence id="src39" class="srcSentence">Call history</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">Text messages</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src41" class="srcSentence">Personal email, contacts, and calendar</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">Web history</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">Location</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">Camera roll</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">Personal data</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Owner</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src47" class="srcSentence">Device name</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src48" class="srcSentence">Serial number</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">Manufacturer</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">Model</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">Operating system</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">Company apps</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">Personal apps</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src54" class="srcSentence">When your device is enrolled, your IT administrator can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src55" class="srcSentence">Reset your device back to manufacturer’s default settings if the device is lost or stolen.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src56" class="srcSentence">Remove all installed company-related data and business apps.</caps:sentence>
                <caps:sentence id="src57" class="srcSentence"> Your personal data and settings aren’t removed.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src58" class="srcSentence">Require you to have a password or PIN on the device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src59" class="srcSentence">Require you to accept terms and conditions.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src60" class="srcSentence">Enable or disable the camera on your device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src61" class="srcSentence">Enable or disable web browsing on your device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src62" class="srcSentence">Enable or disable backup to iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src63" class="srcSentence">Enable or disable document sync to iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src64" class="srcSentence">Enable or disable Photo Stream to iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src65" class="srcSentence">Enable or disable data roaming on your device.</caps:sentence>
                <caps:sentence id="src66" class="srcSentence"> If data roaming is allowed, roaming charges may be incurred.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src67" class="srcSentence">Enable or disable voice roaming on your device.</caps:sentence>
                <caps:sentence id="src68" class="srcSentence"> If voice roaming is allowed, roaming charges may be incurred.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src69" class="srcSentence">Enable or disable automatic file synchronization while in roaming mode on your device.</caps:sentence>
                <caps:sentence id="src70" class="srcSentence"> If automatic file synchronization is allowed, roaming charges may be incurred.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src71" class="srcSentence">For the steps on how to enroll your device, see <link xlink:href="#BKMK_ios_enroll_your_device">Enroll your device in Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="true" address="BKMK_ios_whatis_cp_website">
        <title>
          <caps:sentence id="src72" class="srcSentence">What is the Company Portal website and what can I do with it?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src73" class="srcSentence">The <externalLink><linkText>Company Portal website</linkText><linkUri>http://portal.manage.microsoft.com</linkUri></externalLink> is your company’s web interface that you use to manage your work computers and devices, and your personal computers and devices that you choose to use at work.</caps:sentence>
            <caps:sentence id="src74" class="srcSentence"> You can do most of the same tasks on this website that you can do by using the Company Portal app that you install on your device.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src75" class="srcSentence">You can do the following tasks from the Company Portal website:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src76" class="srcSentence">Browse for and download company apps</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src77" class="srcSentence">Rename your device</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src78" class="srcSentence">Remove your device from Intune</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src79" class="srcSentence">Reset your mobile device to its factory default settings</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src80" class="srcSentence">Find contact information for your IT administrator</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_ios_erase_lost_device">
        <title>
          <caps:sentence id="src81" class="srcSentence">Reset (erase) your lost or stolen device</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src82" class="srcSentence">If a phone that has been enrolled in Intune is lost or stolen, you can reset it to factory default settings by using the Company Portal app from a different device.</caps:sentence>
          </para>
          <alert class="warning">
            <para>
              <caps:sentence id="src83" class="srcSentence">Resetting a device to factor defaults removes both your personal and work information from it!</caps:sentence>
            </para>
          </alert>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src84" class="srcSentence">In the Company Portal app, under <ui>My Devices</ui>,  select the device you want to erase.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src85" class="srcSentence">Tap  <ui>Reset</ui> &gt; <ui>Reset</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src86" class="srcSentence">If you are unable to reset your lost or stolen device, contact IT to reset it for you.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <maml:section address="BKMK_ios_data_collect" expanded="true" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src87" class="srcSentence">Turn off Microsoft usage data collection</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src88" class="srcSentence">In order to improve its products and services, Microsoft automatically collects anonymous data about the reliability and performance of the Company Portal app and how it is used.</caps:sentence>
            <caps:sentence id="src89" class="srcSentence"> You can turn off the collection of that data by using the Usage Data setting in the Company Portal app.</caps:sentence>
            <caps:sentence id="src90" class="srcSentence"> IT administrators have no control over the collection of the data, and they cannot change your selection for the setting.</caps:sentence>
          </maml:para>
        </maml:content>
      </maml:section>
      <section address="BKMK_ios_unenroll_device">
        <title>
          <caps:sentence id="src91" class="srcSentence">Unenroll your device from Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src92" class="srcSentence">When you unenroll your device from Intune, your device will not longer be able to access company resources and will no longer be managed by Intune.</caps:sentence>
            <caps:sentence id="src93" class="srcSentence"> More information about unenrolling follows the steps.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src94" class="srcSentence">To unenroll your device from Intune:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src95" class="srcSentence">In the Company Portal app, under <ui>My Devices</ui>,  select the device you want to unenroll.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src96" class="srcSentence">Tap  <ui>Remove</ui> &gt; <ui>Remove</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src97" class="srcSentence">When you unenroll your device from Intune, here's what happens:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src98" class="srcSentence">Your device won’t appear in the Company Portal anymore</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src99" class="srcSentence">You can’t install apps from the Company Portal anymore.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src100" class="srcSentence">Any settings that were changed on your device when you added it (for example, disabling the camera, or requiring a certain password length) will no longer apply.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src101" class="srcSentence">You might not have access to some company resources, such as file shares or internal web sites, on your device anymore.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src102" class="srcSentence">You can’t use company apps and company data on your device anymore.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src103" class="srcSentence">You might not be able to connect to your company network using Wi-Fi or a virtual private network (VPN) anymore.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src104" class="srcSentence">Company email profiles are removed from the device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src105" class="srcSentence">Devices that are configured for email only won't appear in the Company Portal app or website anymore.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section address="BKMK_ios_fix_issues">
        <title>
          <caps:sentence id="src106" class="srcSentence">Fix issues when your device is enrolled in Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src107" class="srcSentence">If you get an error while you’re using the Company Portal app, you can send information about the error to help your IT admin troubleshoot the problem.</caps:sentence>
            <caps:sentence id="src108" class="srcSentence"> You can send error information in different ways:</caps:sentence>
          </para>
          <maml:list class="bullet" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src109" class="srcSentence">By tapping <maml:ui>Report</maml:ui> on error alert messages.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src110" class="srcSentence">By tapping <maml:ui>Send Diagnostic Report</maml:ui> on the About screen of the Company Portal app</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src111" class="srcSentence">By shaking your device while you’re in the Company Portal app, and then tapping <maml:ui>Email</maml:ui> when the Diagnostics alert appears.</caps:sentence>
                <caps:sentence id="src112" class="srcSentence"> If the alert doesn’t appear when you shake the device, open <maml:ui>Settings</maml:ui> &gt; <maml:ui>Company Portal</maml:ui>, and make sure that the <maml:ui>Shake Gesture</maml:ui> option is on.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>