---
title: Configuraci&#243;n de directivas de configuraci&#243;n de Windows Phone en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 83f7469c-272e-43f2-8139-b0d7bc34f43f
---
# Configuraci&#243;n de directivas de configuraci&#243;n de Windows Phone en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt1" class="tgtSentence">Utilice la <token>wit_firstref</token> <ui>Directiva de configuración general de Windows Phone</ui> para configurar las opciones siguientes para dispositivos Windows Phone 8.1: </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="9084f4531606892c31a2ead7f489fef6" id="tgt2" class="tgtSentence">
                <ui>Configuración de seguridad de dispositivos móviles</ui>: elija entre una lista de configuraciones predefinidas que permiten controlar una variedad de características y la funcionalidad en el dispositivo.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b867f2c930c20cdfee8a7dead1c841fb" id="tgt3" class="tgtSentence">
                <ui>Aplicaciones conformes y no conformes</ui>: especifique una lista de las aplicaciones conformes y de las no conformes en su empresa.</caps:sentence>
              <caps:sentence sentenceid="16ba12117d7711b60fc986484fd88959" id="tgt4" class="tgtSentence"> Los dispositivos de Windows Phone pueden bloquear o permitir la instalación de estas aplicaciones.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="a69d9719aa0a733ed0443cfd645e6faa" id="tgt5" class="tgtSentence">Crear una directiva de configuración general de Windows Phone</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence sentenceid="9dc7ba9f0d89c8147f4845291698164b" id="tgt6" class="tgtSentence">Para proporcionar la configuración básica de una directiva de configuración</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt7" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Información general</ui> &gt; <ui>Agregar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt8" class="tgtSentence">Haga clic en <ui>Windows</ui> &gt; <ui>Configuración general (Windows Phone 8.1 y posterior)</ui> y, a continuación, haga clic en <ui>Crear directiva</ui>.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="4b9abd1274d5812dfcbd169d7f6d79f6" id="tgt9" class="tgtSentence">No se puede crear una directiva de configuración usando la configuración recomendada.</caps:sentence>
                      <caps:sentence sentenceid="fe89ac88e33f0367b7d852c33cec8222" id="tgt10" class="tgtSentence"> Debe crear una directiva personalizada.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt11" class="tgtSentence">En la sección <ui>General</ui> de la página <ui>Crear directiva</ui>, especifique un nombre y una descripción para la nueva directiva.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="7ff845438279ad7c9c1a743c93c485cb" id="tgt12" class="tgtSentence">Use la información que encontrará en las secciones siguientes para ayudarle a proporcionar la configuración de la directiva.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt13" class="tgtSentence">Cuando haya terminado haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt14" class="tgtSentence">La nueva directiva se muestra en el nodo <ui>Directivas de configuración</ui> del área de trabajo <ui>Directiva</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Settings" expanded="true">
        <title>
          <caps:sentence sentenceid="f74d8a54de873d1aa99b3e65f54da222" id="tgt15" class="tgtSentence">Configuración de Windows Phone</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section address="BKMK_sec" expanded="true">
            <title>
              <caps:sentence sentenceid="4dfc8238219173ac50d6f602bd6f59cd" id="tgt16" class="tgtSentence">Configuración de seguridad</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt17" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt18" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="00e48d1f688610a2c1bc595a2aaad4db" id="tgt19" class="tgtSentence">Requerir una contraseña para desbloquear dispositivos móviles</caps:sentence>
                        </ui>
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
                          <caps:sentence sentenceid="dca92e82330f06a43bed4c39a9ae8a45" id="tgt21" class="tgtSentence">Tipo de contraseña obligatoria</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="673ec97b13a814ace1bdb7efea92d383" id="tgt22" class="tgtSentence">(especifica el tipo de contraseña que será necesario, como solo numérica o alfanumérica).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt23" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="484685f502a8f416bcf92e78a2b673ec" id="tgt24" class="tgtSentence">Tipo de contraseña requerida: número mínimo de conjuntos de caracteres</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="f436d05af8cc158ec3146b927d809dd9" id="tgt25" class="tgtSentence">Hay cuatro conjuntos de caracteres: letras minúsculas, letras mayúsculas, símbolos y números.</caps:sentence>
                        <caps:sentence sentenceid="256ecca469c924c14a7ad824a453e019" id="tgt26" class="tgtSentence"> Esta configuración especifica cuántos conjuntos de caracteres diferentes deben incluirse en la contraseña.</caps:sentence>
                        <caps:sentence sentenceid="50aad4a3d8ba306bf04418b5e31363f3" id="tgt27" class="tgtSentence"> Sin embargo, para dispositivos iOS, especifica el número de caracteres de símbolos que deben incluirse en la contraseña.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt28" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2f276c6158fbb9b45297b2600181d32d" id="tgt29" class="tgtSentence">Longitud mínima de contraseña</caps:sentence>
                        </ui>
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
                          <caps:sentence sentenceid="9903f598b57a7f39747ca848a1376d18" id="tgt31" class="tgtSentence">Permitir contraseñas sencillas</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="4f1e869c0cf4719448849db8258003df" id="tgt32" class="tgtSentence">Contraseñas sencillas serían, por ejemplo, "0000" y "1234".</caps:sentence>
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
                          <caps:sentence sentenceid="aad4971834ff738bf7c82b31d2513c23" id="tgt34" class="tgtSentence">Número de errores de inicio de sesión repetidos que se permiten antes de que se borre el dispositivo</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt35" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9c77c0d298b482fc19eba178ba592b67" id="tgt36" class="tgtSentence">Minutos de inactividad antes de que se apague la pantalla</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt37" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2fb470a15f63e1990f7635ac30db44d7" id="tgt38" class="tgtSentence">Expiración de contraseña (días)</caps:sentence>
                        </ui>
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
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0e592e13acb6618a4ca5a3126b0bfa63" id="tgt42" class="tgtSentence">
                          <ui>Recordar historial de la contraseña</ui>: <ui>Impedir la reutilización de contraseñas anteriores</ui></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt43" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="ddd65d7d92420afaf23beb9ab9cd3be7" id="tgt44" class="tgtSentence">Configuración de cifrado</caps:sentence>
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
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt46" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6ee61936fa4604c18cfc32efd91b93d5" id="tgt47" class="tgtSentence">Requerir cifrado en dispositivo móvil</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="564ef91f4823aa9f094932a962d6f442" id="tgt48" class="tgtSentence">Para dispositivos de Windows Phone 8, debe establecerse en <ui>Sí</ui>.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt49" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="621e3306e54a1464a3b513c46e371145" id="tgt50" class="tgtSentence">Configuración del sistema</caps:sentence>
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
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt52" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0404a8a7a4917a78c040cfb0df59a1df" id="tgt53" class="tgtSentence">Permitir captura de pantalla</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt54" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8105846d4b7150b1c6849bc3e7994889" id="tgt55" class="tgtSentence">Permitir el envío de datos de diagnóstico</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt56" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="cb3b851ef85207fa479d6e0aec32b937" id="tgt57" class="tgtSentence">Configuración de nube: cuentas y sincronización</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt58" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt59" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="34d59c1187653c22ca1945abd1e99469" id="tgt60" class="tgtSentence">Permitir cuenta de Microsoft</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt61" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_email" expanded="true">
            <title>
              <caps:sentence sentenceid="b70b51c3cbc157e714fc4f486985d666" id="tgt62" class="tgtSentence">Configuración de correo electrónico</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt63" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt64" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="bb8e3c8fd2e7c158822256e459ec0edc" id="tgt65" class="tgtSentence">Permitir cuentas de correo electrónico personalizadas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt66" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_browser" expanded="true">
            <title>
              <caps:sentence sentenceid="06746f3d881795846a0870dc6d355fd7" id="tgt67" class="tgtSentence">Configuración de la aplicación: explorador</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt68" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt69" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a0c48d4afe3535baaeabfa7149c6ef7a" id="tgt70" class="tgtSentence">Permitir explorador web</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt71" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_apps" expanded="true">
            <title>
              <caps:sentence sentenceid="1fc255764272758aa0421dbfe0ddf895" id="tgt72" class="tgtSentence">Configuración de la aplicación: aplicaciones</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt73" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt74" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f956e1c595e427cc2f06ff42da87a73f" id="tgt75" class="tgtSentence">Permitir almacén de aplicaciones</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt76" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_hard" expanded="true">
            <title>
              <caps:sentence sentenceid="8868ff8ede3d8e50302ccfd0fbe08fa2" id="tgt77" class="tgtSentence">Configuración de funcionalidades del dispositivo: hardware</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt78" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt79" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="05dd919b3a7292227de28546f39f4928" id="tgt80" class="tgtSentence">Permitir cámara</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt81" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ce113c55d1b3a3b1616bd8d58f2d6fdb" id="tgt82" class="tgtSentence">Permitir almacenamiento extraíble</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt83" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8dc8bec3c22373dd8447523e6202a5d4" id="tgt84" class="tgtSentence">Permitir Wi-Fi</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt85" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5e2d5cfbfc5736a9055a62acc9465520" id="tgt86" class="tgtSentence">Permitir Wi-Fi Tethering</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt87" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6da9e7b6cf656a40f0f3079fe763e272" id="tgt88" class="tgtSentence">Permitir la conexión automática a zonas Wi-Fi gratuitas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt89" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="051640f64cfb604b6ba0ea831cb32db8" id="tgt90" class="tgtSentence">Permitir informar de zonas Wi-Fi</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="27d14c21167377dfb78d30d1e745302e" id="tgt91" class="tgtSentence">(enviar información acerca de las conexiones Wi-Fi para ayudar a detectar conexiones cercanas)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt92" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2c41b4c56056968e9f89851a7650f6ed" id="tgt93" class="tgtSentence">Permitir geolocalización</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="54d1d9dc079a0e71d46173926b7bdac9" id="tgt94" class="tgtSentence">(permite que el dispositivo use la información de ubicación)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt95" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1773b705c6c985b2c179ff71b1d8a9eb" id="tgt96" class="tgtSentence">Permitir NFC</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="61d63d3ebe635c14c40732c4174c93f3" id="tgt97" class="tgtSentence">(permite las operaciones que usan la transmisión de datos en proximidad)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt98" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f5b02fb1ac756124bdb8eaa270d0c1b2" id="tgt99" class="tgtSentence">Permitir Bluetooth</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt100" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="ac27b430b679e95693410b0ae55eafde" id="tgt101" class="tgtSentence">Configuración de funcionalidades del dispositivo: características</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt102" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt103" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f98807ee3f4cbb43e555d032ecbbcb5c" id="tgt104" class="tgtSentence">Permitir copiar y pegar</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt105" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
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
          <caps:sentence sentenceid="8bff424d0224a4f2de8d47c72d3c5d5e" id="tgt106" class="tgtSentence">Configuración de aplicaciones conformes y no conformes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt107" class="tgtSentence">En la lista <ui>Aplicaciones conformes y no conformes</ui>, especifique una lista de aplicaciones conformes y no conformes con la siguiente información:</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="c1299a8b219c4112805453d837121bd0" id="tgt108" class="tgtSentence">Una única directiva solo puede contener una lista de aplicaciones conformes o una lista de aplicaciones no conformes.</caps:sentence>
              <caps:sentence sentenceid="f4e2743b4e4a1030b988853359027ef7" id="tgt109" class="tgtSentence"> No se pueden especificar ambas en la misma directiva.</caps:sentence>
            </para>
          </alert>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt110" class="tgtSentence">Nombre de la configuración</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt111" class="tgtSentence">Más información</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="fce018c75600450dd688541e64847a19" id="tgt112" class="tgtSentence">Bloquear dispositivos para que no abran las aplicaciones de la lista</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d8a748bcdc442fc6fa2da80615fb7d0c" id="tgt113" class="tgtSentence">Enumera las aplicaciones que no se administran mediante Intune y que los usuarios no pueden instalar ni ejecutar.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="db4daaf38a9a8ab33711961318147fdd" id="tgt114" class="tgtSentence">Permitir que los dispositivos instalen solo las aplicaciones de la lista</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b790b11361a95dbde029bc7767462abf" id="tgt115" class="tgtSentence">Enumera las aplicaciones que los usuarios pueden instalar.</caps:sentence>
                    <caps:sentence sentenceid="ae6e67552c03d01ae9814d7aeceb41e3" id="tgt116" class="tgtSentence"> Los usuarios no pueden instalar ninguna otra aplicación.</caps:sentence>
                    <caps:sentence sentenceid="6b27131c3416a447442571ae9c7f7aed" id="tgt117" class="tgtSentence"> Las aplicaciones que se administran mediante Intune están permitidas automáticamente.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="34ec78fcc91ffb1e54cd85e4a0924332" id="tgt118" class="tgtSentence">Agregar</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="97ff0bf051e8d71f2fa56ad9e1d379f3" id="tgt119" class="tgtSentence">Agrega una aplicación a la lista seleccionada.</caps:sentence>
                    <caps:sentence sentenceid="8b2f232fb20cca820395359d982061a6" id="tgt120" class="tgtSentence"> Especifique un nombre de su elección, opcionalmente el editor de la aplicación y la dirección URL de la aplicación en la tienda de aplicaciones.</caps:sentence>
                  </para>
                  <para>
                    <link xlink:href="83f7469c-272e-43f2-8139-b0d7bc34f43f#BKMK_URL">How to specify URLs to app stores</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="a77d6ccb4852f72efd606dc871ce3f13" id="tgt121" class="tgtSentence">Importar aplicaciones</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="92c0c5285655182a570246150fc0111f" id="tgt122" class="tgtSentence">Importa la lista de las aplicaciones que ha especificado en un archivo de valores separados por comas.</caps:sentence>
                    <caps:sentence sentenceid="ee0f8201f33794e40e9c176e2b3b6528" id="tgt123" class="tgtSentence"> Utilice el formato, nombre de la aplicación, editor, dirección URL de la aplicación en el archivo.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="de95b43bceeb4b998aed4aed5cef1ae7" id="tgt124" class="tgtSentence">Editar</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="71d20d96ebad4906a8030b19200e3024" id="tgt125" class="tgtSentence">Permite editar el nombre, el editor y la dirección URL de la aplicación seleccionada.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="099af53f601532dbd31e0ea99ffdeb64" id="tgt126" class="tgtSentence">Eliminar</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0044665f0e60b0bb03d6119bf1432176" id="tgt127" class="tgtSentence">Elimina la aplicación seleccionada de la lista.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="9bb317e1ae28616129f5e46d6aa13408" id="tgt128" class="tgtSentence">Si especifica una lista de aplicaciones permitidas para dispositivos de Windows Phone 8.1, debe agregar la aplicación Portal de empresa a esta lista o se bloqueará.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5d355fa5eb823fb88bc9f63121b58ba4" id="tgt129" class="tgtSentence">Implementar la directiva de configuración</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fde06fc41b756f980cfbc8b4242322ed" id="tgt130" class="tgtSentence">Implemente la directiva de configuración en uno o más grupos de usuarios o dispositivos de su organización.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="ad5c1bcb5291ef46b20f2e8f623f5ca4" id="tgt131" class="tgtSentence">Para obtener más información sobre cómo implementar directivas, consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="bda4ffeb1979df370a82567754ec29ab" id="tgt132" class="tgtSentence">En el área de trabajo <ui>Directiva</ui>, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención.</caps:sentence>
                  <caps:sentence sentenceid="f38e8d4a29f6e64f69b2faa73bb44771" id="tgt133" class="tgtSentence"> Además, aparece un resumen de estado en el área de trabajo <ui>Panel</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="ba0732ef3c018e9295d416bc74ec9c95" id="tgt134" class="tgtSentence">Información de referencia para las aplicaciones conformes y no conformes</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section address="BKMK_URL" expanded="false">
            <title>
              <caps:sentence sentenceid="330c9c0b571a4b62a77c080ece3521dc" id="tgt135" class="tgtSentence">Cómo especificar las direcciones URL de tiendas de aplicaciones</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="d7c816d6ab2c47ffee896ad051c731db" id="tgt136" class="tgtSentence">Para especificar una dirección URL de la aplicación en la lista de aplicaciones compatibles y no compatibles, utilice el siguiente formato:</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1d78457e80b3c77f152c8c399312bb34" id="tgt137" class="tgtSentence">Desde la página de <externalLink><linkText>aplicaciones y juegos para Windows Phone</linkText><linkUri>http://www.windowsphone.com/en-us/store/overview</linkUri></externalLink>, busque la aplicación que desea usar.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8bc0e29294eac202915189f625e5db3b" id="tgt138" class="tgtSentence">Abra la página de la aplicación y copie la dirección URL en el Portapapeles.</caps:sentence>
                <caps:sentence sentenceid="1bd3ec773068356fadace92225487e6a" id="tgt139" class="tgtSentence"> Ya puede utilizarla como dirección URL en una la lista de aplicaciones conformes o no conformes.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a85de7d13e3457644fdb999d70b70c31" id="tgt140" class="tgtSentence">
                  <ui>Ejemplo:</ui> busque la aplicación Skype en la tienda.</caps:sentence>
                <caps:sentence sentenceid="e2b41b597d335f9c843c126deb06ca4e" id="tgt141" class="tgtSentence"> La dirección URL que utilice será <ui>http://www.windowsphone.com/es-es/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51</ui>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
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
          <caps:sentence id="src1" class="srcSentence">Use the <token>wit_firstref</token> <ui>Windows Phone general configuration policy</ui> to configure the following settings for Windows Phone 8.1 devices:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">
                <ui>Mobile device security settings</ui> – Choose from a list of predefined settings that let you control a range of features and functionality on the device.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">
                <ui>Compliant and noncompliant apps</ui> - Specify a list of apps that are compliant, or not compliant in your company.</caps:sentence>
              <caps:sentence id="src4" class="srcSentence"> Windows Phone devices can block, or allow installation of these apps.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Create a Windows Phone general configuration policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence id="src6" class="srcSentence">To provide basic settings for the configuration policy</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Overview</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Click <ui>Windows</ui> &gt; <ui>General Configuration (Windows Phone 8.1 and later)</ui> and then click <ui>Create Policy</ui>.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src9" class="srcSentence">You cannot create a configuration policy using recommended settings.</caps:sentence>
                      <caps:sentence id="src10" class="srcSentence"> You must create a custom policy.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">In the <ui>General</ui> section of the <ui>Create Policy</ui> page, specify a name and a description for the new policy.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Use the information in the following sections to help you supply settings for the policy.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">When you are finished, click <ui>Save Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src14" class="srcSentence">The new policy displays in the <ui>Configuration Policies</ui> node of the <ui>Policy</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Settings" expanded="true">
        <title>
          <caps:sentence id="src15" class="srcSentence">Settings for Windows Phone</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section address="BKMK_sec" expanded="true">
            <title>
              <caps:sentence id="src16" class="srcSentence">Security settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src17" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src18" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src19" class="srcSentence">Require a password to unlock mobile devices</caps:sentence>
                        </ui>
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
                          <caps:sentence id="src21" class="srcSentence">Required password type</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">(specifies the type of password that will be required, such as numeric only, or alphanumeric)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src23" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src24" class="srcSentence">Required password type – Minimum number of character sets</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src25" class="srcSentence">There are four character sets, lowercase letters, uppercase letters, numbers, and symbols.</caps:sentence>
                        <caps:sentence id="src26" class="srcSentence"> This setting specifies how many different character sets must be included in the password).</caps:sentence>
                        <caps:sentence id="src27" class="srcSentence"> However, for iOS devices, this specifies the number of symbol characters must be included in the password)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src28" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src29" class="srcSentence">Minimum password length</caps:sentence>
                        </ui>
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
                          <caps:sentence id="src31" class="srcSentence">Allow simple passwords</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src32" class="srcSentence">Simple passwords include ‘0000’ and ‘1234’</caps:sentence>
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
                          <caps:sentence id="src34" class="srcSentence">Number of repeated sign-in failures to allow before the device is wiped</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src36" class="srcSentence">Minutes of inactivity before screen turns off</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src38" class="srcSentence">Password expiration (days)</caps:sentence>
                        </ui>
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
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">
                          <ui>Remember password history</ui> – <ui>Prevent reuse of previous passwords</ui></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src44" class="srcSentence">Encryption settings</caps:sentence>
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
                    <TD>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src47" class="srcSentence">Require encryption on mobile device</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src48" class="srcSentence">For Windows Phone 8 devices, you must set this to <ui>Yes</ui>.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src50" class="srcSentence">System settings</caps:sentence>
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
                        <caps:sentence id="src52" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src53" class="srcSentence">Allow screen capture</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src55" class="srcSentence">Allow diagnostic data submission</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src57" class="srcSentence">Cloud settings – accounts and synchronization</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src59" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src60" class="srcSentence">Allow Microsoft account</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src61" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_email" expanded="true">
            <title>
              <caps:sentence id="src62" class="srcSentence">Email settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src65" class="srcSentence">Allow custom email accounts</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_browser" expanded="true">
            <title>
              <caps:sentence id="src67" class="srcSentence">Application settings - browser</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src70" class="srcSentence">Allow web browser</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_apps" expanded="true">
            <title>
              <caps:sentence id="src72" class="srcSentence">Application settings - apps</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src73" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src75" class="srcSentence">Allow application store</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src76" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_hard" expanded="true">
            <title>
              <caps:sentence id="src77" class="srcSentence">Device capabilities settings - hardware</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src78" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src79" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src80" class="srcSentence">Allow camera</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src82" class="srcSentence">Allow removable storage</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src83" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src84" class="srcSentence">Allow Wi-Fi</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src85" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src86" class="srcSentence">Allow Wi-Fi tethering</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src88" class="srcSentence">Allow automatic connection to free Wi-Fi hotspots</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src90" class="srcSentence">Allow Wi-Fi hotspot reporting</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src91" class="srcSentence">(send information about Wi-Fi connections to help discover nearby connections)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src93" class="srcSentence">Allow geolocation</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src94" class="srcSentence">(allows the device to utilize location information)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src96" class="srcSentence">Allow NFC</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src97" class="srcSentence">(allows operations that use near field communication)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src98" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src99" class="srcSentence">Allow Bluetooth</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src100" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src101" class="srcSentence">Device capabilities settings - features</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src103" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src104" class="srcSentence">Allow copy and paste</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src105" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
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
          <caps:sentence id="src106" class="srcSentence">Settings for compliant and noncompliant apps</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src107" class="srcSentence">In the <ui>Compliant &amp; Noncompliant Apps</ui> list, specify a list of compliant or noncompliant apps using the following information:</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src108" class="srcSentence">A single policy can only contain a list of compliant, or a list of noncompliant apps.</caps:sentence>
              <caps:sentence id="src109" class="srcSentence"> You cannot specify both in the same policy.</caps:sentence>
            </para>
          </alert>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">Setting name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">More information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src112" class="srcSentence">Block devices from opening the listed apps</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src113" class="srcSentence">Lists the apps that are not managed by Intune which users are not allowed to install and run.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src114" class="srcSentence">Allow devices to install only the listed apps</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">Lists the apps that users are allowed to install.</caps:sentence>
                    <caps:sentence id="src116" class="srcSentence"> Users cannot install any other apps.</caps:sentence>
                    <caps:sentence id="src117" class="srcSentence"> Apps that are managed by Intune are automatically allowed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src118" class="srcSentence">Add</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src119" class="srcSentence">Adds an app to the selected list.</caps:sentence>
                    <caps:sentence id="src120" class="srcSentence"> Specify a name of your choice, optionally the app publisher, and the URL to the app in the app store.</caps:sentence>
                  </para>
                  <para>
                    <link xlink:href="83f7469c-272e-43f2-8139-b0d7bc34f43f#BKMK_URL">How to specify URLs to app stores</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src121" class="srcSentence">Import Apps</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src122" class="srcSentence">Imports a list of apps you have specified in a comma-separated values file.</caps:sentence>
                    <caps:sentence id="src123" class="srcSentence"> Use the format, application name, publisher, app URL in the file.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src124" class="srcSentence">Edit</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src125" class="srcSentence">Let’s you edit the name, publisher and URL of the selected app.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src126" class="srcSentence">Delete</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src127" class="srcSentence">Deletes the selected app from the list.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="important">
            <para>
              <caps:sentence id="src128" class="srcSentence">If you specify a list of allowed apps for Windows Phone 8.1 devices, you must add the Company Portal app to this list, or else it will be blocked.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src129" class="srcSentence">Deploy the Configuration Policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">Deploy the configuration policy to one or more groups of users or devices in your organization.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src131" class="srcSentence">For more information about how to deploy policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src132" class="srcSentence">A status summary and alerts In the <ui>Policy</ui> workspace identify issues with the policy that require your attention.</caps:sentence>
                  <caps:sentence id="src133" class="srcSentence"> Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src134" class="srcSentence">Reference information for compliant and noncompliant apps</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section address="BKMK_URL" expanded="false">
            <title>
              <caps:sentence id="src135" class="srcSentence">How to specify URLs to app stores</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src136" class="srcSentence">To specify an app URL in the compliant and noncompliant apps list, use the following format:</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src137" class="srcSentence">From the <externalLink><linkText>Windows Phone Apps+Games</linkText><linkUri>http://www.windowsphone.com/en-us/store/overview</linkUri></externalLink> page, search for the app you want to use.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src138" class="srcSentence">Open the app’s page, and copy the URL to the clipboard.</caps:sentence>
                <caps:sentence id="src139" class="srcSentence"> You can now use this as the URL in either the compliant or noncompliant apps list.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src140" class="srcSentence">
                  <ui>Example:</ui> Search the store for the Skype app.</caps:sentence>
                <caps:sentence id="src141" class="srcSentence"> The URL you use will be <ui>http://www.windowsphone.com/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51</ui>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>