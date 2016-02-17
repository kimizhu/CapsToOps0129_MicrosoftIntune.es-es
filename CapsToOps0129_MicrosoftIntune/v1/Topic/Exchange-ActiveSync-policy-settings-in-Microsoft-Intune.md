---
title: Configuraci&#243;n de directivas de Exchange ActiveSync en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9cbb826-b155-4df6-abf3-60c6f05b2783
---
# Configuraci&#243;n de directivas de Exchange ActiveSync en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt1" class="tgtSentence">Use la directiva de Exchange ActiveSync de <token>wit_firstref</token> para configurar las opciones que le permitirán controlar una variedad de características y funciones en los dispositivos administrados por Exchange ActiveSync.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="e0444af5272f266ad4398eebba8e7697" id="tgt2" class="tgtSentence">Crear una directiva de Exchange ActiveSync</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence sentenceid="b6204d2ef7b1a50184f07c97e6b02b15" id="tgt3" class="tgtSentence">Proporcionar una configuración básica para la directiva</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt4" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Información general</ui> &gt; <ui>Agregar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt5" class="tgtSentence">Haga clic en <ui>Configuración de dispositivos móviles comunes</ui> &gt; <ui>Exchange ActiveSync</ui> y, a continuación, en <ui>Crear directiva</ui>.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="4b9abd1274d5812dfcbd169d7f6d79f6" id="tgt6" class="tgtSentence">No se puede crear una directiva de configuración usando la configuración recomendada.</caps:sentence>
                      <caps:sentence sentenceid="fe89ac88e33f0367b7d852c33cec8222" id="tgt7" class="tgtSentence"> Debe crear una directiva personalizada.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt8" class="tgtSentence">En la sección <ui>General</ui> de la página <ui>Crear directiva</ui>, especifique un nombre y una descripción para la nueva directiva.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="7ff845438279ad7c9c1a743c93c485cb" id="tgt9" class="tgtSentence">Use la información que encontrará en las secciones siguientes para ayudarle a proporcionar la configuración de la directiva.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt10" class="tgtSentence">Cuando haya terminado haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt11" class="tgtSentence">La nueva directiva se muestra en el nodo <ui>Directivas de configuración</ui> del área de trabajo <ui>Directiva</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Settings" expanded="true">
        <title>
          <caps:sentence sentenceid="980229f763fb0d14c87b21c9d3c55431" id="tgt12" class="tgtSentence">Configuración de directiva para dispositivos administrados con Exchange ActiveSync</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section address="BKMK_sec" expanded="true">
            <title>
              <caps:sentence sentenceid="4dfc8238219173ac50d6f602bd6f59cd" id="tgt13" class="tgtSentence">Configuración de seguridad</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt14" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="00e48d1f688610a2c1bc595a2aaad4db" id="tgt15" class="tgtSentence">Requerir una contraseña para desbloquear dispositivos móviles</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="dca92e82330f06a43bed4c39a9ae8a45" id="tgt16" class="tgtSentence">Tipo de contraseña obligatoria</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="673ec97b13a814ace1bdb7efea92d383" id="tgt17" class="tgtSentence">(especifica el tipo de contraseña que será necesario, como solo numérica o alfanumérica).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2f276c6158fbb9b45297b2600181d32d" id="tgt18" class="tgtSentence">Longitud mínima de contraseña</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9903f598b57a7f39747ca848a1376d18" id="tgt19" class="tgtSentence">Permitir contraseñas sencillas</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="4f1e869c0cf4719448849db8258003df" id="tgt20" class="tgtSentence">Contraseñas sencillas serían, por ejemplo, "0000" y "1234".</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="aad4971834ff738bf7c82b31d2513c23" id="tgt21" class="tgtSentence">Número de errores de inicio de sesión repetidos que se permiten antes de que se borre el dispositivo</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2fb470a15f63e1990f7635ac30db44d7" id="tgt22" class="tgtSentence">Expiración de contraseña (días)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="bd7e3f529ae9c075d09f3b7116bbe632" id="tgt23" class="tgtSentence">Recordar el historial de contraseñas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0e592e13acb6618a4ca5a3126b0bfa63" id="tgt24" class="tgtSentence">
                          <ui>Recordar historial de la contraseña</ui>: <ui>Impedir la reutilización de contraseñas anteriores</ui></caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c6f50988cb876f83b08878649ee5446b" id="tgt25" class="tgtSentence">Minutos de inactividad antes de que se pida la contraseña</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="ddd65d7d92420afaf23beb9ab9cd3be7" id="tgt26" class="tgtSentence">Configuración de cifrado</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt27" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6ee61936fa4604c18cfc32efd91b93d5" id="tgt28" class="tgtSentence">Requerir cifrado en dispositivo móvil</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt29" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                      <para>
                        <caps:sentence sentenceid="564ef91f4823aa9f094932a962d6f442" id="tgt30" class="tgtSentence">Para dispositivos de Windows Phone 8, debe establecerse en <ui>Sí</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1c6a02e9c0537efec3523bc6efa08377" id="tgt31" class="tgtSentence">Para habilitar el cifrado en dispositivos iOS, habilite la opción <ui>Requerir una contraseña para desbloquear dispositivos móviles</ui>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt32" class="tgtSentence">
                          <ui>Requerir cifrado en tarjetas de almacenamiento</ui> </caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="13255e2083914b35540684da63ec3fac" id="tgt33" class="tgtSentence">
                  <superscript>1</superscript> Información adicional para los dispositivos que ejecutan Windows 8.1</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="04aa2a349c54b727768bc4f5c9a2af37" id="tgt34" class="tgtSentence">Para forzar el cifrado en los dispositivos que ejecutan Windows 8.1, debe instalar la <externalLink><linkText>Actualización de cliente de diciembre de 2014 MDM en Windows </linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> en cada dispositivo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0e1479825d5ecb3b7572092ad74979a7" id="tgt35" class="tgtSentence">Si habilita este valor para dispositivos de Windows 8.1, todos los usuarios del dispositivo deben tener una cuenta de Microsoft.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1f6cf6b88c6face55c624e6b0e0d530" id="tgt36" class="tgtSentence">Para que el cifrado funcione, el dispositivo debe cumplir los requisitos de certificación de hardware de Microsoft <externalLink><linkText>InstantGo</linkText><linkUri>http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1a43fc77f8aeb73b1f10a0d0ac884235" id="tgt37" class="tgtSentence">Al exigir el cifrado en un dispositivo, solo se puede acceder a la clave de recuperación desde la cuenta de Microsoft de los usuarios, a la que se accede desde su cuenta de OneDrive.</caps:sentence>
                    <caps:sentence sentenceid="28e69dac0d8510fdc2168d3f84e4282a" id="tgt38" class="tgtSentence"> No se puede recuperar esta clave en nombre de un usuario.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_email" expanded="true">
            <title>
              <caps:sentence sentenceid="b70b51c3cbc157e714fc4f486985d666" id="tgt39" class="tgtSentence">Configuración de correo electrónico</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt40" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="17836474810ec136a53ef50ae13b53ae" id="tgt41" class="tgtSentence">Permitir a los usuarios descargar datos adjuntos de correo electrónico</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1d04bab799f80dd2c6becf1583d443e9" id="tgt42" class="tgtSentence">Periodo de sincronización del correo electrónico</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt43" class="tgtSentence">
                          <ui>Permitir que los dispositivos móviles que no son totalmente compatibles con la configuración de Exchange ActiveSync se sincronicen con Exchange</ui> </caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_browser" expanded="true">
            <title>
              <caps:sentence sentenceid="c002414c276c89f77a31d4d03490ad21" id="tgt44" class="tgtSentence">Aplicaciones: explorador</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt45" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a0c48d4afe3535baaeabfa7149c6ef7a" id="tgt46" class="tgtSentence">Permitir explorador web</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_hard" expanded="true">
            <title>
              <caps:sentence sentenceid="ade9c8cd967ad19943fd9b282086154a" id="tgt47" class="tgtSentence">Capacidades del dispositivo: hardware</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt48" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="05dd919b3a7292227de28546f39f4928" id="tgt49" class="tgtSentence">Permitir cámara</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5d355fa5eb823fb88bc9f63121b58ba4" id="tgt50" class="tgtSentence">Implementar la directiva de configuración</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fde06fc41b756f980cfbc8b4242322ed" id="tgt51" class="tgtSentence">Implemente la directiva de configuración en uno o más grupos de usuarios o dispositivos de su organización.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="ad5c1bcb5291ef46b20f2e8f623f5ca4" id="tgt52" class="tgtSentence">Para obtener más información sobre cómo implementar directivas, consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="bda4ffeb1979df370a82567754ec29ab" id="tgt53" class="tgtSentence">En el área de trabajo <ui>Directiva</ui>, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención.</caps:sentence>
                  <caps:sentence sentenceid="f38e8d4a29f6e64f69b2faa73bb44771" id="tgt54" class="tgtSentence"> Además, aparece un resumen de estado en el área de trabajo <ui>Panel</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the <token>wit_firstref</token> Exchange ActiveSync policy to configure settings that let you control a range of features and functionality on devices that are managed by Exchange ActiveSync.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Create an Exchange ActiveSync policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence id="src3" class="srcSentence">To provide basic settings for the policy</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src4" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Overview</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">Click <ui>Common Mobile Device Settings</ui> &gt; <ui>Exchange ActiveSync</ui> and then click <ui>Create Policy</ui>.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src6" class="srcSentence">You cannot create a configuration policy using recommended settings.</caps:sentence>
                      <caps:sentence id="src7" class="srcSentence"> You must create a custom policy.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">In the <ui>General</ui> section of the <ui>Create Policy</ui> page, specify a name and a description for the new policy.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Use the information in the following sections to help you supply settings for the policy.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">When you are finished, click <ui>Save Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src11" class="srcSentence">The new policy displays in the <ui>Configuration Policies</ui> node of the <ui>Policy</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Settings" expanded="true">
        <title>
          <caps:sentence id="src12" class="srcSentence">Policy settings for devices managed by Exchange ActiveSync</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section address="BKMK_sec" expanded="true">
            <title>
              <caps:sentence id="src13" class="srcSentence">Security settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src15" class="srcSentence">Require a password to unlock mobile devices</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src16" class="srcSentence">Required password type</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src17" class="srcSentence">(specifies the type of password that will be required, such as numeric only, or alphanumeric)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src18" class="srcSentence">Minimum password length</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src19" class="srcSentence">Allow simple passwords</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">Simple passwords include ‘0000’ and ‘1234’</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src21" class="srcSentence">Number of repeated sign-in failures to allow before the device is wiped</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src22" class="srcSentence">Password expiration (days)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src23" class="srcSentence">Remember password history</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src24" class="srcSentence">
                          <ui>Remember password history</ui> – <ui>Prevent reuse of previous passwords</ui></caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src25" class="srcSentence">Minutes of inactivity before password is required</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src26" class="srcSentence">Encryption settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src27" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src28" class="srcSentence">Require encryption on mobile device</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src29" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                      <para>
                        <caps:sentence id="src30" class="srcSentence">For Windows Phone 8 devices, you must set this to <ui>Yes</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src31" class="srcSentence">To enable encryption on iOS devices, enable the setting <ui>Require a password to unlock mobile devices</ui>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src32" class="srcSentence">
                          <ui>Require encryption on storage cards</ui> </caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src33" class="srcSentence">
                  <superscript>1</superscript> Additional information for devices that run Windows 8.1</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">To enforce encryption on devices that run Windows 8.1, you must install the <externalLink><linkText>December 2014 MDM client update for Windows</linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> on each device.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">If you enable this setting for Windows 8.1 devices, all users of the device must have a Microsoft Account.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">For encryption to work, the device must meet the Microsoft <externalLink><linkText>InstantGo</linkText><linkUri>http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/</linkUri></externalLink> hardware certification requirements.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">When you enforce encryption on a device, the recovery key is only accessible from the users Microsoft Account, accessed from their OneDrive account.</caps:sentence>
                    <caps:sentence id="src38" class="srcSentence"> You cannot recover this key on behalf of a user.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_email" expanded="true">
            <title>
              <caps:sentence id="src39" class="srcSentence">Email settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src41" class="srcSentence">Allow users to download email attachments</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src42" class="srcSentence">Email synchronization period</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">
                          <ui>Allow mobile devices that don’t fully support Exchange ActiveSync settings to synchronize with Exchange</ui> </caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_browser" expanded="true">
            <title>
              <caps:sentence id="src44" class="srcSentence">Applications - Browser</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src46" class="srcSentence">Allow web browser</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_hard" expanded="true">
            <title>
              <caps:sentence id="src47" class="srcSentence">Device capabilities - hardware</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src48" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src49" class="srcSentence">Allow camera</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src50" class="srcSentence">Deploy the Configuration Policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">Deploy the configuration policy to one or more groups of users or devices in your organization.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src52" class="srcSentence">For more information about how to deploy policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src53" class="srcSentence">A status summary and alerts In the <ui>Policy</ui> workspace identify issues with the policy that require your attention.</caps:sentence>
                  <caps:sentence id="src54" class="srcSentence"> Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>