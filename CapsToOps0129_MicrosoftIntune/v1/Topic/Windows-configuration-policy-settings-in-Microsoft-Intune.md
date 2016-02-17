---
title: Configuraci&#243;n de directivas de configuraci&#243;n de Windows en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6982a2bc-aafa-475a-9236-4840b709e5a1
---
# Configuraci&#243;n de directivas de configuraci&#243;n de Windows en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt1" class="tgtSentence">Use la <ui>Directiva de configuración de Windows</ui> de <token>wit_firstref</token> para configurar opciones de inscripción de dispositivos Windows 8 y Windows 8.1:</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="7f18e94bc26c93ba8e532af8c1ecd320" id="tgt2" class="tgtSentence">Crear una directiva de configuración general de Windows</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence sentenceid="9dc7ba9f0d89c8147f4845291698164b" id="tgt3" class="tgtSentence">Para proporcionar la configuración básica de una directiva de configuración</caps:sentence>
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
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt5" class="tgtSentence">Haga clic en <ui>Windows</ui> &gt; <ui>Configuración general (Windows 8.1 y versiones posteriores)</ui> y, a continuación, haga clic en <ui>Crear directiva</ui>.</caps:sentence>
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
          <caps:sentence sentenceid="42cbbeb6138c167aed3c73484420b411" id="tgt12" class="tgtSentence">Configuración para dispositivos Windows inscritos</caps:sentence>
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
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt15" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt16" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="dca92e82330f06a43bed4c39a9ae8a45" id="tgt17" class="tgtSentence">Tipo de contraseña obligatoria</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="673ec97b13a814ace1bdb7efea92d383" id="tgt18" class="tgtSentence">(especifica el tipo de contraseña que será necesario, como solo numérica o alfanumérica).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt19" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt20" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="484685f502a8f416bcf92e78a2b673ec" id="tgt21" class="tgtSentence">Tipo de contraseña requerida: número mínimo de conjuntos de caracteres</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="f436d05af8cc158ec3146b927d809dd9" id="tgt22" class="tgtSentence">Hay cuatro conjuntos de caracteres: letras minúsculas, letras mayúsculas, símbolos y números.</caps:sentence>
                        <caps:sentence sentenceid="256ecca469c924c14a7ad824a453e019" id="tgt23" class="tgtSentence"> Esta configuración especifica cuántos conjuntos de caracteres diferentes deben incluirse en la contraseña.</caps:sentence>
                        <caps:sentence sentenceid="50aad4a3d8ba306bf04418b5e31363f3" id="tgt24" class="tgtSentence"> Sin embargo, para dispositivos iOS, especifica el número de caracteres de símbolos que deben incluirse en la contraseña.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt25" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt26" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2f276c6158fbb9b45297b2600181d32d" id="tgt27" class="tgtSentence">Longitud mínima de contraseña</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt28" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt29" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt30" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="aad4971834ff738bf7c82b31d2513c23" id="tgt31" class="tgtSentence">Número de errores de inicio de sesión repetidos que se permiten antes de que se borre el dispositivo</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt32" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt33" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9c77c0d298b482fc19eba178ba592b67" id="tgt34" class="tgtSentence">Minutos de inactividad antes de que se apague la pantalla</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt35" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt36" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2fb470a15f63e1990f7635ac30db44d7" id="tgt37" class="tgtSentence">Expiración de contraseña (días)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt38" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt39" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="bd7e3f529ae9c075d09f3b7116bbe632" id="tgt40" class="tgtSentence">Recordar el historial de contraseñas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt41" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt42" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0e592e13acb6618a4ca5a3126b0bfa63" id="tgt43" class="tgtSentence">
                          <ui>Recordar historial de la contraseña</ui>: <ui>Impedir la reutilización de contraseñas anteriores</ui></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt44" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt45" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="599a1558c182afbc03db5b8265350ffe" id="tgt46" class="tgtSentence">Permitir contraseña de imagen y PIN</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt47" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt48" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="68e4641564f690bdbe6df84b5e166781" id="tgt49" class="tgtSentence">
                  <superscript>1</superscript> Si se implementa una directiva de longitud de contraseña para dispositivos que ejecutan Windows RT, los usuarios se verán obligados a restablecer su contraseña, aunque la contraseña actual cumpla los requisitos de la directiva.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="ddd65d7d92420afaf23beb9ab9cd3be7" id="tgt50" class="tgtSentence">Configuración de cifrado</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt51" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt52" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt53" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6ee61936fa4604c18cfc32efd91b93d5" id="tgt54" class="tgtSentence">Requerir cifrado en dispositivo móvil</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt55" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                      <para>
                        <caps:sentence sentenceid="564ef91f4823aa9f094932a962d6f442" id="tgt56" class="tgtSentence">Para dispositivos de Windows Phone 8, debe establecerse en <ui>Sí</ui>.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt57" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt58" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="13255e2083914b35540684da63ec3fac" id="tgt59" class="tgtSentence">
                  <superscript>1</superscript> Información adicional para los dispositivos que ejecutan Windows 8.1</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="04aa2a349c54b727768bc4f5c9a2af37" id="tgt60" class="tgtSentence">Para forzar el cifrado en los dispositivos que ejecutan Windows 8.1, debe instalar la <externalLink><linkText>Actualización de cliente de diciembre de 2014 MDM en Windows </linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> en cada dispositivo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0e1479825d5ecb3b7572092ad74979a7" id="tgt61" class="tgtSentence">Si habilita este valor para dispositivos de Windows 8.1, todos los usuarios del dispositivo deben tener una cuenta de Microsoft.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1f6cf6b88c6face55c624e6b0e0d530" id="tgt62" class="tgtSentence">Para que el cifrado funcione, el dispositivo debe cumplir los requisitos de certificación de hardware de Microsoft <externalLink><linkText>InstantGo</linkText><linkUri>http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1a43fc77f8aeb73b1f10a0d0ac884235" id="tgt63" class="tgtSentence">Al exigir el cifrado en un dispositivo, solo se puede acceder a la clave de recuperación desde la cuenta de Microsoft de los usuarios, a la que se accede desde su cuenta de OneDrive.</caps:sentence>
                    <caps:sentence sentenceid="28e69dac0d8510fdc2168d3f84e4282a" id="tgt64" class="tgtSentence"> No se puede recuperar esta clave en nombre de un usuario.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="8e00380a370cea8bf75a0c532842e34f" id="tgt65" class="tgtSentence">Configuración de malware</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt66" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt67" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt68" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="bde056659cf8d8d00c90cf82f2fd8739" id="tgt69" class="tgtSentence">Requerir firewall de red</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt70" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt71" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e193432d344954d2ff1ed1f9e7ae2aa2" id="tgt72" class="tgtSentence">Habilitar SmartScreen</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt73" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt74" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="621e3306e54a1464a3b513c46e371145" id="tgt75" class="tgtSentence">Configuración del sistema</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt76" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt77" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt78" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3b6305eb7e96c55a1375646e0e48a023" id="tgt79" class="tgtSentence">Requerir actualizaciones automáticas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt80" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt81" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f88e0a610ae00360d5981961a873a90c" id="tgt82" class="tgtSentence">Requerir actualizaciones automáticas: clasificación mínima de actualizaciones para instalar automáticamente </caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt83" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                      <para>
                        <caps:sentence sentenceid="208ad7a1e1ad18e9901df8bd6050904e" id="tgt84" class="tgtSentence">Seleccione la clasificación de actualizaciones que se instalarán automáticamente:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="8631d949e5d4532385c465e03ab33254" id="tgt85" class="tgtSentence">
                              <ui>Importante</ui>: instala todas las actualizaciones que se clasifican como importantes.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ddde09bf2eeb57f460d6b83247833078" id="tgt86" class="tgtSentence">
                              <ui>Recomendada</ui>: instala todas las actualizaciones que se clasifican como importantes o recomendadas.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt87" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt88" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a33b7f65aa61e08d39296d64a265d815" id="tgt89" class="tgtSentence">Control de cuentas de usuario</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt90" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt91" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8105846d4b7150b1c6849bc3e7994889" id="tgt92" class="tgtSentence">Permitir el envío de datos de diagnóstico</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt93" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt94" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="9dbefa36f3fb44490f39123ff8a41561" id="tgt95" class="tgtSentence">
                  <superscript>1</superscript> Para forzar el cifrado en los dispositivos que ejecutan Windows 1, debe instalar la <externalLink><linkText>Actualización de cliente de diciembre de 8.1 MDM en Windows</linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> en cada dispositivo.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_cloud" expanded="true">
            <title>
              <caps:sentence sentenceid="5ac5d7b85913db1a420f267dcaa4b286" id="tgt96" class="tgtSentence">Configuración de nube: documentos y datos</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt97" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt98" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt99" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="735bff1b7ea46e575f38d35c8075f761" id="tgt100" class="tgtSentence">Dirección URL de carpetas de trabajo</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="03ad9effd4c60820b30ddc0e4a299de8" id="tgt101" class="tgtSentence">(establece la dirección URL de la carpeta de trabajo para permitir que los documentos se sincronicen en todos los dispositivos)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt102" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt103" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_email" expanded="true">
            <title>
              <caps:sentence sentenceid="b70b51c3cbc157e714fc4f486985d666" id="tgt104" class="tgtSentence">Configuración de correo electrónico</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt105" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt106" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt107" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="eeafdcc3ddf2a74a877fb9a274423661" id="tgt108" class="tgtSentence">Hacer que la cuenta Microsoft sea opcional en la aplicación Windows Mail</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt109" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt110" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_browser" expanded="true">
            <title>
              <caps:sentence sentenceid="06746f3d881795846a0870dc6d355fd7" id="tgt111" class="tgtSentence">Configuración de la aplicación: explorador</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt112" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt113" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt114" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e047ee944ff7459a4014e5e126e5e963" id="tgt115" class="tgtSentence">Permitir el autorrelleno</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt116" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt117" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1b2a6b1dd6c8827b383f55ca82da08c8" id="tgt118" class="tgtSentence">Permitir bloqueador de elementos emergentes</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt119" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt120" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6ff864914a0d00af70203ffdaab9015e" id="tgt121" class="tgtSentence">Permitir complementos</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt122" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt123" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e1c3ff920a64a9bd299d2d0f8b43d0fa" id="tgt124" class="tgtSentence">Permitir Active scripting</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt125" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt126" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="dcc733e492fd957f1d798d9c0050f31e" id="tgt127" class="tgtSentence">Permitir advertencias de fraude</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt128" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt129" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b95f6e0fbf9465ba046084e9c23da640" id="tgt130" class="tgtSentence">Permitir el acceso a sitios de intranet por la entrada de una sola palabra</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="a4018b221eb67660c98822d4feae0bbf" id="tgt131" class="tgtSentence">(permite el uso de una sola palabra para dirigir Internet Explorer a un sitio web como, por ejemplo, "Bing")</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt132" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt133" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="beb88125affa16172ecab8ead56124c3" id="tgt134" class="tgtSentence">Permitir la detección automática de redes de intranet</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt135" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt136" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4b9d9dc6621cf87b4c15ae9dff57114a" id="tgt137" class="tgtSentence">Nivel de seguridad de Internet</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt138" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt139" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e89cd4dd97c7f886785b6ffbab06e79e" id="tgt140" class="tgtSentence">Nivel de seguridad de intranet</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt141" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt142" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="55dc66e16dbee875acc2f3fcb9afb0ed" id="tgt143" class="tgtSentence">Nivel de seguridad de sitios de confianza</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt144" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt145" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="27af881ca31cfcd20f86a5256a215cf5" id="tgt146" class="tgtSentence">Nivel de seguridad de sitios restringidos</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt147" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt148" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2396b23f36a57f25d78bc6029de6fd63" id="tgt149" class="tgtSentence">Enviar encabezado Do Not Track</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt150" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt151" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="90695fab9db4ed43a3e3a73ed6a0b3b4" id="tgt152" class="tgtSentence">Permitir el acceso al menú Modo de empresa</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt153" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt154" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9d283a482cbd56c47e4fbee8fe755804" id="tgt155" class="tgtSentence">Ubicación de la lista de sitios de Modo de empresa</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt156" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt157" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="52e183edd25a42305b595b80551ab7a9" id="tgt158" class="tgtSentence">Configuración de funcionalidades del dispositivo: datos móviles</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt159" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt160" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt161" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c2d252651547ad4dfa328dcf51811431" id="tgt162" class="tgtSentence">Permitir itinerancia de datos</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt163" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt164" class="tgtSentence">No</caps:sentence>
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
          <caps:sentence sentenceid="5d355fa5eb823fb88bc9f63121b58ba4" id="tgt165" class="tgtSentence">Implementar la directiva de configuración</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fde06fc41b756f980cfbc8b4242322ed" id="tgt166" class="tgtSentence">Implemente la directiva de configuración en uno o más grupos de usuarios o dispositivos de su organización.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="ad5c1bcb5291ef46b20f2e8f623f5ca4" id="tgt167" class="tgtSentence">Para obtener más información sobre cómo implementar directivas, consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="bda4ffeb1979df370a82567754ec29ab" id="tgt168" class="tgtSentence">En el área de trabajo <ui>Directiva</ui>, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención.</caps:sentence>
                  <caps:sentence sentenceid="f38e8d4a29f6e64f69b2faa73bb44771" id="tgt169" class="tgtSentence"> Además, aparece un resumen de estado en el área de trabajo <ui>Panel</ui>.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Use the <token>wit_firstref</token> <ui>Windows general configuration policy</ui> to configure settings for enrolled Windows 8, and Windows 8.1 devices:</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Create a Windows general configuration policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence id="src3" class="srcSentence">To provide basic settings for the configuration policy</caps:sentence>
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
                    <caps:sentence id="src5" class="srcSentence">Click <ui>Windows</ui> &gt; <ui>General Configuration (Windows 8.1 and later)</ui> and then click <ui>Create Policy</ui>.</caps:sentence>
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
          <caps:sentence id="src12" class="srcSentence">Settings for enrolled Windows devices</caps:sentence>
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
                    <TD>
                      <para>
                        <caps:sentence id="src15" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src16" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src17" class="srcSentence">Required password type</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src18" class="srcSentence">(specifies the type of password that will be required, such as numeric only, or alphanumeric)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src19" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src21" class="srcSentence">Required password type – Minimum number of character sets</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">There are four character sets, lowercase letters, uppercase letters, numbers, and symbols.</caps:sentence>
                        <caps:sentence id="src23" class="srcSentence"> This setting specifies how many different character sets must be included in the password).</caps:sentence>
                        <caps:sentence id="src24" class="srcSentence"> However, for iOS devices, this specifies the number of symbol characters must be included in the password)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src25" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src26" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src27" class="srcSentence">Minimum password length</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src28" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src29" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src30" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src31" class="srcSentence">Number of repeated sign-in failures to allow before the device is wiped</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src32" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src33" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src34" class="srcSentence">Minutes of inactivity before screen turns off</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src37" class="srcSentence">Password expiration (days)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src39" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src40" class="srcSentence">Remember password history</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src41" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">
                          <ui>Remember password history</ui> – <ui>Prevent reuse of previous passwords</ui></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src46" class="srcSentence">Allow picture password and PIN</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src47" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src48" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src49" class="srcSentence">
                  <superscript>1</superscript> When you set deploy a password length policy to devices that run Windows RT, users will be forced to reset their password, even if their current password complies with the policy requirements.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src50" class="srcSentence">Encryption settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src54" class="srcSentence">Require encryption on mobile device</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src55" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">For Windows Phone 8 devices, you must set this to <ui>Yes</ui>.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src57" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src59" class="srcSentence">
                  <superscript>1</superscript> Additional information for devices that run Windows 8.1</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">To enforce encryption on devices that run Windows 8.1, you must install the <externalLink><linkText>December 2014 MDM client update for Windows</linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> on each device.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">If you enable this setting for Windows 8.1 devices, all users of the device must have a Microsoft Account.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">For encryption to work, the device must meet the Microsoft <externalLink><linkText>InstantGo</linkText><linkUri>http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/</linkUri></externalLink> hardware certification requirements.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">When you enforce encryption on a device, the recovery key is only accessible from the users Microsoft Account, accessed from their OneDrive account.</caps:sentence>
                    <caps:sentence id="src64" class="srcSentence"> You cannot recover this key on behalf of a user.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src65" class="srcSentence">Malware settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src67" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src69" class="srcSentence">Require network firewall</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src70" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src72" class="srcSentence">Enable SmartScreen</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src73" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src75" class="srcSentence">System settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src76" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src77" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src78" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src79" class="srcSentence">Require automatic updates</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src82" class="srcSentence">Require automatic updates – Minimum classification of updates to install automatically </caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src83" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                      <para>
                        <caps:sentence id="src84" class="srcSentence">Choose the classification of updates that will be installed automatically:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src85" class="srcSentence">
                              <ui>Important</ui> – Installs all updates classified as important.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src86" class="srcSentence">
                              <ui>Recommended</ui> – Installs all updates classified as important or recommended.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src89" class="srcSentence">User Account Control</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src91" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src92" class="srcSentence">Allow diagnostic data submission</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src93" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src94" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src95" class="srcSentence">
                  <superscript>1</superscript> To enforce encryption on devices that run Windows 8.1, you must install the <externalLink><linkText>December 2014 MDM client update for Windows</linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> on each device.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_cloud" expanded="true">
            <title>
              <caps:sentence id="src96" class="srcSentence">Cloud settings – documents and data</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src97" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src98" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src99" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src100" class="srcSentence">Work Folders URL</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">(sets the URL of the work folder to allow documents to be synchronized across devices)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src103" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_email" expanded="true">
            <title>
              <caps:sentence id="src104" class="srcSentence">Email settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src105" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src108" class="srcSentence">Make Microsoft account optional in Windows Mail application</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src109" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src110" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_browser" expanded="true">
            <title>
              <caps:sentence id="src111" class="srcSentence">Application settings - browser</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src112" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src113" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src114" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src115" class="srcSentence">Allow autofill</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src116" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src117" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src118" class="srcSentence">Allow pop-up blocker</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src121" class="srcSentence">Allow plug-ins</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src122" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src123" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src124" class="srcSentence">Allow active scripting</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src125" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src126" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src127" class="srcSentence">Allow fraud warning</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src128" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src129" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src130" class="srcSentence">Allow intranet site for single word entry</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src131" class="srcSentence">(allows use of a single word to direct Internet Explorer to a web site, such as ‘Bing’)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src132" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src133" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src134" class="srcSentence">Allow automatic detection of intranet network</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src135" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src136" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src137" class="srcSentence">Security level for Internet</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src138" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src139" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src140" class="srcSentence">Security level for intranet</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src141" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src142" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src143" class="srcSentence">Security level for trusted sites</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src144" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src145" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src146" class="srcSentence">Security level for restricted sites</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src147" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src148" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src149" class="srcSentence">Send Do Not Track header</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src150" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src151" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src152" class="srcSentence">Allow Enterprise Mode menu access</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src153" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src154" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src155" class="srcSentence">Enterprise Mode site list location</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src156" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src157" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src158" class="srcSentence">Device capabilities settings - cellular</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src159" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src160" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src161" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src162" class="srcSentence">Allow data roaming</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src163" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src164" class="srcSentence">No</caps:sentence>
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
          <caps:sentence id="src165" class="srcSentence">Deploy the Configuration Policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">Deploy the configuration policy to one or more groups of users or devices in your organization.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src167" class="srcSentence">For more information about how to deploy policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src168" class="srcSentence">A status summary and alerts in the <ui>Policy</ui> workspace identify issues with the policy that require your attention.</caps:sentence>
                  <caps:sentence id="src169" class="srcSentence"> Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</caps:sentence>
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