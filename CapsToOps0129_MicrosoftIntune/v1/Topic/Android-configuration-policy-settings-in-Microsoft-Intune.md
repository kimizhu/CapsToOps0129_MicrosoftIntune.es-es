---
title: Configuraci&#243;n de directivas de configuraci&#243;n de Android en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 71cc39cf-e726-40fd-8d08-78776e099a4b
---
# Configuraci&#243;n de directivas de configuraci&#243;n de Android en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt1" class="tgtSentence">Use la directiva de configuración general de <token>wit_firstref</token> <ui>Android</ui> para configurar opciones para:</caps:sentence>
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
              <caps:sentence sentenceid="ba903a82a0ccb2a98037568fa9cd5f1a" id="tgt3" class="tgtSentence">
                <ui>Modo de quiosco</ui> (solo para dispositivos Samsung KNOX): permite bloquear un dispositivo para que solo funcionen determinadas características.</caps:sentence>
              <caps:sentence sentenceid="2c6fb3f48b9d1860382c944e1113b7d4" id="tgt4" class="tgtSentence"> Por ejemplo, puede permitir que un dispositivo ejecute solo una aplicación administrada que especifique, o puede deshabilitar los botones de volumen de un dispositivo.</caps:sentence>
              <caps:sentence sentenceid="444ac9245463abe6f6f9d66e022ef3bf" id="tgt5" class="tgtSentence"> Esta configuración podría utilizarse para un modelo de demostración de un dispositivo o para un dispositivo que está dedicado a realizar solo una función, como un dispositivo de punto de venta.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b867f2c930c20cdfee8a7dead1c841fb" id="tgt6" class="tgtSentence">
                <ui>Aplicaciones conformes y no conformes</ui>: especifique una lista de las aplicaciones conformes y de las no conformes en su empresa.</caps:sentence>
              <caps:sentence sentenceid="6c5eec99d0921f746103b3e6d6afe593" id="tgt7" class="tgtSentence"> En los dispositivos iOS y Android, el <ui>informe de aplicaciones no conformes</ui> puede utilizarse para comparar la conformidad de las aplicaciones especificadas en la lista con las aplicaciones que los usuarios han instalado (pero en realidad no pueden impedir la instalación de la aplicación).</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="tip">
          <para>
            <caps:sentence sentenceid="fd8fb89ab35cc7d5ae6f970bbeced672" id="tgt8" class="tgtSentence">Puede configurar los términos y condiciones de los usuarios para asegurarse de que saben que las aplicaciones de su dispositivo, incluidas las aplicaciones personales, se evaluarán y que las aplicaciones no conformes se bloquearán o se notificarán como no conformes.</caps:sentence>
            <caps:sentence sentenceid="ea62d5391640f774bc479e85c70ca500" id="tgt9" class="tgtSentence"> Los usuarios deben aceptar estos términos y condiciones para poder inscribir su dispositivo y utilizar el portal de empresa para obtener aplicaciones.</caps:sentence>
            <caps:sentence sentenceid="2eb26fdcf519e62427a8d8a1da1cb4bf" id="tgt10" class="tgtSentence"> Para obtener más información acerca del uso de los términos y condiciones, consulte <legacyLink xlink:href="ce59fb93-01fd-4822-a57d-45ca7d89843d">Working with terms and conditions policies in Microsoft Intune</legacyLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="b96a82e458b8dcd2378b5d5679a47fd7" id="tgt11" class="tgtSentence">Crear una directiva de configuración de Android</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence sentenceid="9dc7ba9f0d89c8147f4845291698164b" id="tgt12" class="tgtSentence">Para proporcionar la configuración básica de una directiva de configuración</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt13" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Información general</ui> &gt; <ui>Agregar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt14" class="tgtSentence">Haga clic en <ui>Android</ui> &gt; <ui>Configuración general</ui> y, a continuación, haga clic en <ui>Crear directiva</ui>.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="4b9abd1274d5812dfcbd169d7f6d79f6" id="tgt15" class="tgtSentence">No se puede crear una directiva de configuración usando la configuración recomendada.</caps:sentence>
                      <caps:sentence sentenceid="fe89ac88e33f0367b7d852c33cec8222" id="tgt16" class="tgtSentence"> Debe crear una directiva personalizada.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt17" class="tgtSentence">En la sección <ui>General</ui> de la página <ui>Crear directiva</ui>, especifique un nombre y una descripción para la nueva directiva.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="7ff845438279ad7c9c1a743c93c485cb" id="tgt18" class="tgtSentence">Use la información que encontrará en las secciones siguientes para ayudarle a proporcionar la configuración de la directiva.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt19" class="tgtSentence">Cuando haya terminado haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt20" class="tgtSentence">La nueva directiva se muestra en el nodo <ui>Directivas de configuración</ui> del área de trabajo <ui>Directiva</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Settings" expanded="true">
        <title>
          <caps:sentence sentenceid="877611791a34b253de5b0ac18b83e55e" id="tgt21" class="tgtSentence">Configuración de directivas de seguridad de dispositivos móviles para dispositivos Android</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c0e114420d048d3c7fc44ef0edf93e9b" id="tgt22" class="tgtSentence">Si el valor que busca no aparece en esta lista, puede crearlo mediante una directiva personalizada de Android que le permita usar la configuración de OMA-URI para controlar el dispositivo.</caps:sentence>
            <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt23" class="tgtSentence"> Para obtener más información, vea <link xlink:href="15904440-5a05-47c9-818e-48073b4090e7">Use Android custom policies to manage device settings with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_sec" expanded="false">
            <title>
              <caps:sentence sentenceid="7fcb03667ac96d450113254eb851fc99" id="tgt24" class="tgtSentence">Configuración de contraseña</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt25" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d08f1456c676326b2b51e3fac93cb52c" id="tgt26" class="tgtSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8e38ef954d44cbd0f2295011883c7fbe" id="tgt27" class="tgtSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="00e48d1f688610a2c1bc595a2aaad4db" id="tgt28" class="tgtSentence">Requerir una contraseña para desbloquear dispositivos móviles</caps:sentence>
                        </ui>
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
                          <caps:sentence sentenceid="2f276c6158fbb9b45297b2600181d32d" id="tgt31" class="tgtSentence">Longitud mínima de contraseña</caps:sentence>
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
                          <caps:sentence sentenceid="aad4971834ff738bf7c82b31d2513c23" id="tgt34" class="tgtSentence">Número de errores de inicio de sesión repetidos que se permiten antes de que se borre el dispositivo</caps:sentence>
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
                          <caps:sentence sentenceid="9c77c0d298b482fc19eba178ba592b67" id="tgt37" class="tgtSentence">Minutos de inactividad antes de que se apague la pantalla</caps:sentence>
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
                          <caps:sentence sentenceid="2fb470a15f63e1990f7635ac30db44d7" id="tgt40" class="tgtSentence">Expiración de contraseña (días)</caps:sentence>
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
                        <ui>
                          <caps:sentence sentenceid="bd7e3f529ae9c075d09f3b7116bbe632" id="tgt43" class="tgtSentence">Recordar el historial de contraseñas</caps:sentence>
                        </ui>
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
                        <caps:sentence sentenceid="0e592e13acb6618a4ca5a3126b0bfa63" id="tgt46" class="tgtSentence">
                          <ui>Recordar historial de la contraseña</ui>: <ui>Impedir la reutilización de contraseñas anteriores</ui></caps:sentence>
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
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9e9b99fa7ec9aee1de52865489683bc6" id="tgt49" class="tgtSentence">Calidad de contraseña</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt50" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt51" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d0569abb86c04c16833d42071ed293ff" id="tgt52" class="tgtSentence">Permitir desbloqueo mediante huellas digitales</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt53" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt54" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="ddd65d7d92420afaf23beb9ab9cd3be7" id="tgt55" class="tgtSentence">Configuración de cifrado</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt56" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d08f1456c676326b2b51e3fac93cb52c" id="tgt57" class="tgtSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8e38ef954d44cbd0f2295011883c7fbe" id="tgt58" class="tgtSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6ee61936fa4604c18cfc32efd91b93d5" id="tgt59" class="tgtSentence">Requerir cifrado en dispositivo móvil</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt60" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt61" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt62" class="tgtSentence">
                          <ui>Requerir cifrado en tarjetas de almacenamiento</ui> </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt63" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt64" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="621e3306e54a1464a3b513c46e371145" id="tgt65" class="tgtSentence">Configuración del sistema</caps:sentence>
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
                        <caps:sentence sentenceid="d08f1456c676326b2b51e3fac93cb52c" id="tgt67" class="tgtSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8e38ef954d44cbd0f2295011883c7fbe" id="tgt68" class="tgtSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0404a8a7a4917a78c040cfb0df59a1df" id="tgt69" class="tgtSentence">Permitir captura de pantalla</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt70" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt71" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8105846d4b7150b1c6849bc3e7994889" id="tgt72" class="tgtSentence">Permitir el envío de datos de diagnóstico</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt73" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt74" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="608181c0e21051993fa84c1754b29b65" id="tgt75" class="tgtSentence">Permitir el restablecimiento de la configuración de fábrica</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt76" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt77" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_cloud" expanded="false">
            <title>
              <caps:sentence sentenceid="5ac5d7b85913db1a420f267dcaa4b286" id="tgt78" class="tgtSentence">Configuración de nube: documentos y datos</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt79" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt80" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d08f1456c676326b2b51e3fac93cb52c" id="tgt81" class="tgtSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d4ee6da051209c3d059005435cf4410a" id="tgt82" class="tgtSentence">Permitir copia de seguridad de Google</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt83" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt84" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="cb3b851ef85207fa479d6e0aec32b937" id="tgt85" class="tgtSentence">Configuración de nube: cuentas y sincronización</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt86" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d08f1456c676326b2b51e3fac93cb52c" id="tgt87" class="tgtSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8e38ef954d44cbd0f2295011883c7fbe" id="tgt88" class="tgtSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4e6ab245815ee0f96be82e5c04ec4629" id="tgt89" class="tgtSentence">Permitir la sincronización automática de la cuenta de Google</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt90" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt91" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_browser" expanded="false">
            <title>
              <caps:sentence sentenceid="06746f3d881795846a0870dc6d355fd7" id="tgt92" class="tgtSentence">Configuración de la aplicación: explorador</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt93" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d08f1456c676326b2b51e3fac93cb52c" id="tgt94" class="tgtSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8e38ef954d44cbd0f2295011883c7fbe" id="tgt95" class="tgtSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a0c48d4afe3535baaeabfa7149c6ef7a" id="tgt96" class="tgtSentence">Permitir explorador web</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt97" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt98" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e047ee944ff7459a4014e5e126e5e963" id="tgt99" class="tgtSentence">Permitir el autorrelleno</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt100" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt101" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1b2a6b1dd6c8827b383f55ca82da08c8" id="tgt102" class="tgtSentence">Permitir bloqueador de elementos emergentes</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt103" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt104" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2c3b0c032374c0766b908511ca23da8c" id="tgt105" class="tgtSentence">Permitir cookies</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt106" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt107" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e1c3ff920a64a9bd299d2d0f8b43d0fa" id="tgt108" class="tgtSentence">Permitir Active scripting</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt109" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt110" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_apps" expanded="false">
            <title>
              <caps:sentence sentenceid="1fc255764272758aa0421dbfe0ddf895" id="tgt111" class="tgtSentence">Configuración de la aplicación: aplicaciones</caps:sentence>
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
                        <caps:sentence sentenceid="d08f1456c676326b2b51e3fac93cb52c" id="tgt113" class="tgtSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8e38ef954d44cbd0f2295011883c7fbe" id="tgt114" class="tgtSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="906dba97fd22562740295b8cc8c23643" id="tgt115" class="tgtSentence">Permitir Google Play Store</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt116" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt117" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_hard" expanded="false">
            <title>
              <caps:sentence sentenceid="8868ff8ede3d8e50302ccfd0fbe08fa2" id="tgt118" class="tgtSentence">Configuración de funcionalidades del dispositivo: hardware</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt119" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d08f1456c676326b2b51e3fac93cb52c" id="tgt120" class="tgtSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8e38ef954d44cbd0f2295011883c7fbe" id="tgt121" class="tgtSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="05dd919b3a7292227de28546f39f4928" id="tgt122" class="tgtSentence">Permitir cámara</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt123" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt124" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ce113c55d1b3a3b1616bd8d58f2d6fdb" id="tgt125" class="tgtSentence">Permitir almacenamiento extraíble</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt126" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt127" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8dc8bec3c22373dd8447523e6202a5d4" id="tgt128" class="tgtSentence">Permitir Wi-Fi</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt129" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt130" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5e2d5cfbfc5736a9055a62acc9465520" id="tgt131" class="tgtSentence">Permitir Wi-Fi Tethering</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt132" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt133" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2c41b4c56056968e9f89851a7650f6ed" id="tgt134" class="tgtSentence">Permitir geolocalización</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="54d1d9dc079a0e71d46173926b7bdac9" id="tgt135" class="tgtSentence">(permite que el dispositivo use la información de ubicación)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt136" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt137" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1773b705c6c985b2c179ff71b1d8a9eb" id="tgt138" class="tgtSentence">Permitir NFC</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="61d63d3ebe635c14c40732c4174c93f3" id="tgt139" class="tgtSentence">(permite las operaciones que usan la transmisión de datos en proximidad)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt140" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt141" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f5b02fb1ac756124bdb8eaa270d0c1b2" id="tgt142" class="tgtSentence">Permitir Bluetooth</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt143" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt144" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0036c994fc54780c3fe33b48bbb6ad2b" id="tgt145" class="tgtSentence">Permitir desconectar</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt146" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt147" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt148" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="b08c860e8631d03c9bd34d33411dffda" id="tgt149" class="tgtSentence">
                  <superscript>1</superscript> Si se deshabilita esta opción, la opción <ui>Número de errores de inicio de sesión repetidos que se permiten antes de que se eliminen los datos del dispositivo</ui> de los dispositivos Samsung KNOX no funciona.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="52e183edd25a42305b595b80551ab7a9" id="tgt150" class="tgtSentence">Configuración de funcionalidades del dispositivo: datos móviles</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt151" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d08f1456c676326b2b51e3fac93cb52c" id="tgt152" class="tgtSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8e38ef954d44cbd0f2295011883c7fbe" id="tgt153" class="tgtSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7b57e74c6890ff3c771ae41ec0178dcd" id="tgt154" class="tgtSentence">Permitir itinerancia de voz</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt155" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt156" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c2d252651547ad4dfa328dcf51811431" id="tgt157" class="tgtSentence">Permitir itinerancia de datos</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt158" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt159" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7a4807d26f0a57c865542194b3a896f4" id="tgt160" class="tgtSentence">Permitir mensajería SMS y MMS</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt161" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt162" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="ac27b430b679e95693410b0ae55eafde" id="tgt163" class="tgtSentence">Configuración de funcionalidades del dispositivo: características</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt164" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d08f1456c676326b2b51e3fac93cb52c" id="tgt165" class="tgtSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8e38ef954d44cbd0f2295011883c7fbe" id="tgt166" class="tgtSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="de8cad2852e0f20cb63cfb0a37fda788" id="tgt167" class="tgtSentence">Permitir asistente de voz</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt168" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt169" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0e9d7a3a8a5a48009347229ab6b471a1" id="tgt170" class="tgtSentence">Permitir la marcación por voz</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt171" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt172" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f98807ee3f4cbb43e555d032ecbbcb5c" id="tgt173" class="tgtSentence">Permitir copiar y pegar</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt174" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt175" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="86346db0261d443bbddafdcb103c6d61" id="tgt176" class="tgtSentence">Permitir el uso compartido del Portapapeles entre aplicaciones</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt177" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt178" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f3848a5ba1d65031d70a43ab92edfddf" id="tgt179" class="tgtSentence">Permitir YouTube</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt180" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt181" class="tgtSentence">Sí</caps:sentence>
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
          <caps:sentence sentenceid="8bff424d0224a4f2de8d47c72d3c5d5e" id="tgt182" class="tgtSentence">Configuración de aplicaciones conformes y no conformes</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt183" class="tgtSentence">En la lista <ui>Aplicaciones conformes y no conformes</ui>, especifique una lista de aplicaciones conformes y no conformes con la siguiente información:</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="c1299a8b219c4112805453d837121bd0" id="tgt184" class="tgtSentence">Una única directiva solo puede contener una lista de aplicaciones conformes o una lista de aplicaciones no conformes.</caps:sentence>
              <caps:sentence sentenceid="f4e2743b4e4a1030b988853359027ef7" id="tgt185" class="tgtSentence"> No se pueden especificar ambas en la misma directiva.</caps:sentence>
            </para>
          </alert>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt186" class="tgtSentence">Nombre de la configuración</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt187" class="tgtSentence">Más información</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="c1966248ab12e62afa1037d9a426e025" id="tgt188" class="tgtSentence">Notificar la no compatibilidad cuando los usuarios instalan las aplicaciones de la lista</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d8a748bcdc442fc6fa2da80615fb7d0c" id="tgt189" class="tgtSentence">Enumera las aplicaciones que no se administran mediante Intune y que los usuarios no pueden instalar ni ejecutar.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="14482e173701f808de2be505ae0fbf9e" id="tgt190" class="tgtSentence">No informar de incompatibilidad cuando los usuarios instalan las aplicaciones enumeradas.</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b790b11361a95dbde029bc7767462abf" id="tgt191" class="tgtSentence">Enumera las aplicaciones que los usuarios pueden instalar.</caps:sentence>
                    <caps:sentence sentenceid="ae6e67552c03d01ae9814d7aeceb41e3" id="tgt192" class="tgtSentence"> Los usuarios no pueden instalar ninguna otra aplicación.</caps:sentence>
                    <caps:sentence sentenceid="6b27131c3416a447442571ae9c7f7aed" id="tgt193" class="tgtSentence"> Las aplicaciones que se administran mediante Intune están permitidas automáticamente.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="34ec78fcc91ffb1e54cd85e4a0924332" id="tgt194" class="tgtSentence">Agregar</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="97ff0bf051e8d71f2fa56ad9e1d379f3" id="tgt195" class="tgtSentence">Agrega una aplicación a la lista seleccionada.</caps:sentence>
                    <caps:sentence sentenceid="8b2f232fb20cca820395359d982061a6" id="tgt196" class="tgtSentence"> Especifique un nombre de su elección, opcionalmente el editor de la aplicación y la dirección URL de la aplicación en la tienda de aplicaciones.</caps:sentence>
                  </para>
                  <para>
                    <link xlink:href="ab46be6c-ab73-4c99-8492-66d1dd418293#BKMK_URL">How to specify URLs to app stores</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="a77d6ccb4852f72efd606dc871ce3f13" id="tgt197" class="tgtSentence">Importar aplicaciones</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="92c0c5285655182a570246150fc0111f" id="tgt198" class="tgtSentence">Importa la lista de las aplicaciones que ha especificado en un archivo de valores separados por comas.</caps:sentence>
                    <caps:sentence sentenceid="ee0f8201f33794e40e9c176e2b3b6528" id="tgt199" class="tgtSentence"> Utilice el formato, nombre de la aplicación, editor, dirección URL de la aplicación en el archivo.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="de95b43bceeb4b998aed4aed5cef1ae7" id="tgt200" class="tgtSentence">Editar</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="71d20d96ebad4906a8030b19200e3024" id="tgt201" class="tgtSentence">Permite editar el nombre, el editor y la dirección URL de la aplicación seleccionada.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="099af53f601532dbd31e0ea99ffdeb64" id="tgt202" class="tgtSentence">Eliminar</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0044665f0e60b0bb03d6119bf1432176" id="tgt203" class="tgtSentence">Elimina la aplicación seleccionada de la lista.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="082d3cfb64c18ea0c95eafa4383368e0" id="tgt204" class="tgtSentence">Configuración del modo de pantalla completa</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a07dcc82e15c156d5ab1d0be2beb8d99" id="tgt205" class="tgtSentence">Especifique la siguiente configuración para los <ui>dispositivos Samsung KNOX</ui>:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt206" class="tgtSentence">Nombre de la configuración</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt207" class="tgtSentence">Más información</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="27b1aa1c8639502e35f9d549216cc3b3" id="tgt208" class="tgtSentence">Seleccione una aplicación administrada que se permitirá ejecutar cuando el dispositivo esté en modo de quiosco</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt209" class="tgtSentence">Haga clic en <ui>Examinar</ui>, seleccione la aplicación administrada, o una aplicación de una tienda, que se permitirá ejecutar cuando el dispositivo esté en modo de quiosco.</caps:sentence>
                    <caps:sentence sentenceid="4408d8d3247ce4d9beea62dff541f326" id="tgt210" class="tgtSentence"> No se podrá ejecutar ninguna otra aplicación en el dispositivo.</caps:sentence>
                  </para>
                  <para>
                    <link xlink:href="ab46be6c-ab73-4c99-8492-66d1dd418293#BKMK_URL">How to specify URLs to app stores</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="6720319ce5e2e87025163c58c4e4a2f9" id="tgt211" class="tgtSentence">Permitir los botones de volumen</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="98bcd1f1d63b6e092c47d84b7e6f9a95" id="tgt212" class="tgtSentence">Habilita o deshabilita el uso de los botones de volumen en el dispositivo.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="4e3f69630f83470802bc2ff6bbc7dc1c" id="tgt213" class="tgtSentence">Permitir el botón de reactivación de suspensión de pantalla</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="94669f2883d79f07da363f3cc1f3006e" id="tgt214" class="tgtSentence">Habilita o deshabilita el botón de reactivación de la suspensión de pantalla en el dispositivo.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5d355fa5eb823fb88bc9f63121b58ba4" id="tgt215" class="tgtSentence">Implementar la directiva de configuración</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fde06fc41b756f980cfbc8b4242322ed" id="tgt216" class="tgtSentence">Implemente la directiva de configuración en uno o más grupos de usuarios o dispositivos de su organización.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="ad5c1bcb5291ef46b20f2e8f623f5ca4" id="tgt217" class="tgtSentence">Para obtener más información sobre cómo implementar directivas, consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="bda4ffeb1979df370a82567754ec29ab" id="tgt218" class="tgtSentence">En el área de trabajo <ui>Directiva</ui>, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención.</caps:sentence>
                  <caps:sentence sentenceid="f38e8d4a29f6e64f69b2faa73bb44771" id="tgt219" class="tgtSentence"> Además, aparece un resumen de estado en el área de trabajo <ui>Panel</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="ba0732ef3c018e9295d416bc74ec9c95" id="tgt220" class="tgtSentence">Información de referencia para las aplicaciones conformes y no conformes</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="643eb214301f31160dfe245a46ac68b3" id="tgt221" class="tgtSentence">Supervisar las aplicaciones conformes y no conformes</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt222" class="tgtSentence">Utilice el <ui>Informe de aplicaciones no conformes</ui> para ver la conformidad de las aplicaciones permitidas y bloqueadas.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="b81da05f29b9e9a642b4aa40d0297e79" id="tgt223" class="tgtSentence">Para ejecutar el informe de aplicaciones no conformes</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt224" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Informes</ui> &gt; <ui>Informe de aplicaciones no conformes</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="4e2d4a2ee109d8e620ca1340105ed9b9" id="tgt225" class="tgtSentence">Seleccione los grupos de dispositivos que quiere comprobar, si quiere comprobar las aplicaciones conformes, las aplicaciones no conformes o ambas y, a continuación, haga clic en <ui>Ver informe</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_URL" expanded="false">
            <title>
              <caps:sentence sentenceid="330c9c0b571a4b62a77c080ece3521dc" id="tgt226" class="tgtSentence">Cómo especificar las direcciones URL de tiendas de aplicaciones</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4620613bebfb4cfeff794dd18f44586a" id="tgt227" class="tgtSentence">Para especificar una dirección URL de aplicación en la lista de aplicaciones conformes y no conformes o en la opción <ui>Seleccione una aplicación administrada que se podrá ejecutar cuando el dispositivo esté en modo de pantalla completa</ui> (solo iOS), use el siguiente formato:</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt228" class="tgtSentence">En la <externalLink><linkText>sección Aplicaciones de Google Play</linkText><linkUri>https://play.google.com/store/apps</linkUri></externalLink>, busque la aplicación que desea utilizar.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a36bfd3404dffe2bd02291e0a765b1f6" id="tgt229" class="tgtSentence">Abra la página de instalación de la aplicación y copie la dirección URL en el Portapapeles.</caps:sentence>
                <caps:sentence sentenceid="1bd3ec773068356fadace92225487e6a" id="tgt230" class="tgtSentence"> Ya puede utilizarla como dirección URL en una la lista de aplicaciones conformes o no conformes.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="43bbd838330ed5d10cf3615521a8428e" id="tgt231" class="tgtSentence">
                  <ui>Ejemplo:</ui> busque Microsoft Office Mobile en Google Play.</caps:sentence>
                <caps:sentence sentenceid="e2b41b597d335f9c843c126deb06ca4e" id="tgt232" class="tgtSentence"> La dirección URL que utilice será <ui>https://play.google.com/store/apps/details?id=com.microsoft.office.officehub</ui>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <nextSteps>
        <content>
          <para></para>
        </content>
      </nextSteps>
      <relatedTopics>
        <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the <token>wit_firstref</token> <ui>Android general configuration policy</ui> to configure settings for:</caps:sentence>
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
                <ui>Kiosk mode</ui> (for Samsung KNOX devices only) - Lock a device to only allow certain features to work.</caps:sentence>
              <caps:sentence id="src4" class="srcSentence"> For example, you can allow a device to only run one managed app that you specify, or you can disable the volume buttons on a device.</caps:sentence>
              <caps:sentence id="src5" class="srcSentence"> These settings might be used for a demonstration model of a device, or a device that is dedicated to performing only one function, such as a point of sale device.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">
                <ui>Compliant and noncompliant apps</ui> - Specify a list of apps that are compliant, or not compliant in your company.</caps:sentence>
              <caps:sentence id="src7" class="srcSentence"> On Android and iOS devices, the <ui>Noncompliant Apps Report</ui> can be used to view the compliance of apps you specified in the list against the apps that users have installed (but cannot actually block the installation of the app).</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="tip">
          <para>
            <caps:sentence id="src8" class="srcSentence">You can configure terms and conditions for users to ensure that they acknowledge that apps on their device, including personal apps will be evaluated, and noncompliant apps will either be blocked, or reported as noncompliant.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Users must accept these terms and conditions before they can enroll their device and use the company portal to get apps.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> For more information about using terms and conditions, see <legacyLink xlink:href="ce59fb93-01fd-4822-a57d-45ca7d89843d">Working with terms and conditions policies in Microsoft Intune</legacyLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Create an Android configuration policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence id="src12" class="srcSentence">To provide basic settings for the configuration policy</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Overview</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Click <ui>Android</ui> &gt; <ui>General Configuration</ui> and then click <ui>Create Policy</ui>.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src15" class="srcSentence">You cannot create a configuration policy using recommended settings.</caps:sentence>
                      <caps:sentence id="src16" class="srcSentence"> You must create a custom policy.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">In the <ui>General</ui> section of the <ui>Create Policy</ui> page, specify a name and a description for the new policy.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Use the information in the following sections to help you supply settings for the policy.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">When you are finished, click <ui>Save Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src20" class="srcSentence">The new policy displays in the <ui>Configuration Policies</ui> node of the <ui>Policy</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Settings" expanded="true">
        <title>
          <caps:sentence id="src21" class="srcSentence">Mobile device security policy settings for Android devices</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src22" class="srcSentence">If the setting you are looking for does not appear in this list, you might be able to create it using an Android custom policy that lets you use OMA-URI settings to control the device.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> For more information, see <link xlink:href="15904440-5a05-47c9-818e-48073b4090e7">Use Android custom policies to manage device settings with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_sec" expanded="false">
            <title>
              <caps:sentence id="src24" class="srcSentence">Password settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src25" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src26" class="srcSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src27" class="srcSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src28" class="srcSentence">Require a password to unlock mobile devices</caps:sentence>
                        </ui>
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
                          <caps:sentence id="src31" class="srcSentence">Minimum password length</caps:sentence>
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
                          <caps:sentence id="src34" class="srcSentence">Number of repeated sign-in failures to allow before the device is wiped</caps:sentence>
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
                          <caps:sentence id="src37" class="srcSentence">Minutes of inactivity before screen turns off</caps:sentence>
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
                          <caps:sentence id="src40" class="srcSentence">Password expiration (days)</caps:sentence>
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
                        <ui>
                          <caps:sentence id="src43" class="srcSentence">Remember password history</caps:sentence>
                        </ui>
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
                        <caps:sentence id="src46" class="srcSentence">
                          <ui>Remember password history</ui> – <ui>Prevent reuse of previous passwords</ui></caps:sentence>
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
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src49" class="srcSentence">Password quality</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src52" class="srcSentence">Allow fingerprint unlock</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src55" class="srcSentence">Encryption settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src57" class="srcSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src59" class="srcSentence">Require encryption on mobile device</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src60" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src61" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src62" class="srcSentence">
                          <ui>Require encryption on storage cards</ui> </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src65" class="srcSentence">System settings</caps:sentence>
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
                        <caps:sentence id="src67" class="srcSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src69" class="srcSentence">Allow screen capture</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src70" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src72" class="srcSentence">Allow diagnostic data submission</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src73" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src75" class="srcSentence">Allow factory reset</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src76" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src77" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_cloud" expanded="false">
            <title>
              <caps:sentence id="src78" class="srcSentence">Cloud settings – documents and data</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src79" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src82" class="srcSentence">Allow Google backup</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src83" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src84" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src85" class="srcSentence">Cloud settings – accounts and synchronization</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src89" class="srcSentence">Allow Google account auto sync</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src91" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_browser" expanded="false">
            <title>
              <caps:sentence id="src92" class="srcSentence">Application settings - browser</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src93" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src94" class="srcSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src96" class="srcSentence">Allow web browser</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src97" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src98" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src99" class="srcSentence">Allow autofill</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src100" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src102" class="srcSentence">Allow pop-up blocker</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src103" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src104" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src105" class="srcSentence">Allow cookies</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src108" class="srcSentence">Allow active scripting</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src109" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src110" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_apps" expanded="false">
            <title>
              <caps:sentence id="src111" class="srcSentence">Application settings - apps</caps:sentence>
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
                        <caps:sentence id="src113" class="srcSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src114" class="srcSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src115" class="srcSentence">Allow Google Play store</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src116" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src117" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_hard" expanded="false">
            <title>
              <caps:sentence id="src118" class="srcSentence">Device capabilities settings - hardware</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src121" class="srcSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src122" class="srcSentence">Allow camera</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src123" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src124" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src125" class="srcSentence">Allow removable storage</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src126" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src127" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src128" class="srcSentence">Allow Wi-Fi</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src129" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src130" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src131" class="srcSentence">Allow Wi-Fi tethering</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src132" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src133" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src134" class="srcSentence">Allow geolocation</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src135" class="srcSentence">(allows the device to utilize location information)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src136" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src137" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src138" class="srcSentence">Allow NFC</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src139" class="srcSentence">(allows operations that use near field communication)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src140" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src141" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src142" class="srcSentence">Allow Bluetooth</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src143" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src144" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src145" class="srcSentence">Allow power off</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src146" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src147" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src148" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src149" class="srcSentence">
                  <superscript>1</superscript> If this setting is disabled, the setting <ui>Number of repeated sign in failures to allow before the device is wiped</ui> for Samsung KNOX devices does not function.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src150" class="srcSentence">Device capabilities settings - cellular</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src151" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src152" class="srcSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src153" class="srcSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src154" class="srcSentence">Allow voice roaming</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src155" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src156" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src157" class="srcSentence">Allow data roaming</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src158" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src159" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src160" class="srcSentence">Allow SMS/MMS messaging</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src161" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src162" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src163" class="srcSentence">Device capabilities settings - features</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src164" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src165" class="srcSentence">Android 4.0+</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src166" class="srcSentence">Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src167" class="srcSentence">Allow voice assistant</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src168" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src169" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src170" class="srcSentence">Allow voice dialing</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src171" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src172" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src173" class="srcSentence">Allow copy and paste</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src174" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src175" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src176" class="srcSentence">Allow clipboard share between applications</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src177" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src178" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src179" class="srcSentence">Allow YouTube</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src180" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src181" class="srcSentence">Yes</caps:sentence>
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
          <caps:sentence id="src182" class="srcSentence">Settings for compliant and noncompliant apps</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src183" class="srcSentence">In the <ui>Compliant &amp; Noncompliant Apps</ui> list, specify a list of compliant or noncompliant apps using the following information:</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src184" class="srcSentence">A single policy can only contain a list of compliant, or a list of noncompliant apps.</caps:sentence>
              <caps:sentence id="src185" class="srcSentence"> You cannot specify both in the same policy.</caps:sentence>
            </para>
          </alert>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">Setting name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">More information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src188" class="srcSentence">Report noncompliance when users install the listed apps</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src189" class="srcSentence">Lists the apps that are not managed by Intune which users are not allowed to install and run.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src190" class="srcSentence">Do not report noncompliance when users install the listed apps</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">Lists the apps that users are allowed to install.</caps:sentence>
                    <caps:sentence id="src192" class="srcSentence"> Users cannot install any other apps.</caps:sentence>
                    <caps:sentence id="src193" class="srcSentence"> Apps that are managed by Intune are automatically allowed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src194" class="srcSentence">Add</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">Adds an app to the selected list.</caps:sentence>
                    <caps:sentence id="src196" class="srcSentence"> Specify a name of your choice, optionally the app publisher, and the URL to the app in the app store.</caps:sentence>
                  </para>
                  <para>
                    <link xlink:href="ab46be6c-ab73-4c99-8492-66d1dd418293#BKMK_URL">How to specify URLs to app stores</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src197" class="srcSentence">Import Apps</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src198" class="srcSentence">Imports a list of apps you have specified in a comma-separated values file.</caps:sentence>
                    <caps:sentence id="src199" class="srcSentence"> Use the format, application name, publisher, app URL in the file.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src200" class="srcSentence">Edit</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src201" class="srcSentence">Let’s you edit the name, publisher and URL of the selected app.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src202" class="srcSentence">Delete</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src203" class="srcSentence">Deletes the selected app from the list.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src204" class="srcSentence">Kiosk mode settings</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src205" class="srcSentence">Specify the following settings for <ui>Samsung KNOX devices</ui>:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src206" class="srcSentence">Setting name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src207" class="srcSentence">More information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src208" class="srcSentence">Select a managed app that will be allowed to run when the device is in kiosk mode</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src209" class="srcSentence">Click <ui>Browse</ui>, then select the managed app, or app from a store that will be allowed to run when the device is in kiosk mode.</caps:sentence>
                    <caps:sentence id="src210" class="srcSentence"> No other apps will be allowed to run on the device.</caps:sentence>
                  </para>
                  <para>
                    <link xlink:href="ab46be6c-ab73-4c99-8492-66d1dd418293#BKMK_URL">How to specify URLs to app stores</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src211" class="srcSentence">Allow volume buttons</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">Enables or disables the use of the volume buttons on the device.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src213" class="srcSentence">Allow screen sleep wake button</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src214" class="srcSentence">Enables or disables the screen sleep wake button on the device.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src215" class="srcSentence">Deploy the Configuration Policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src216" class="srcSentence">Deploy the configuration policy to one or more groups of users or devices in your organization.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src217" class="srcSentence">For more information about how to deploy policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src218" class="srcSentence">A status summary and alerts In the <ui>Policy</ui> workspace identify issues with the policy that require your attention.</caps:sentence>
                  <caps:sentence id="src219" class="srcSentence"> Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src220" class="srcSentence">Reference information for compliant and noncompliant apps</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section expanded="false">
            <title>
              <caps:sentence id="src221" class="srcSentence">Monitor compliant and noncompliant apps</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src222" class="srcSentence">Use the <ui>Noncompliant Apps Report</ui> to view the compliance of allowed and blocked apps.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src223" class="srcSentence">To run the Noncompliant Apps Report</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src224" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Reports</ui> &gt; <ui>Noncompliant Apps Report</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src225" class="srcSentence">Select the device groups that you would like to check, whether you want to check for compliant apps, noncompliant apps, or both, then click <ui>View Report</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_URL" expanded="false">
            <title>
              <caps:sentence id="src226" class="srcSentence">How to specify URLs to app stores</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src227" class="srcSentence">To specify an app URL in the compliant and noncompliant apps list, or in the <ui>Select a managed app that will be allowed to run when the device is in kiosk mode</ui> option (iOS only), use the following format:</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src228" class="srcSentence">In the <externalLink><linkText>Apps section of Google Play</linkText><linkUri>https://play.google.com/store/apps</linkUri></externalLink>, search for the app you want to use.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src229" class="srcSentence">Open the installation page for the app, and copy the URL to the clipboard.</caps:sentence>
                <caps:sentence id="src230" class="srcSentence"> You can now use this as the URL in either the compliant or noncompliant apps list.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src231" class="srcSentence">
                  <ui>Example:</ui> Search Google Play for Microsoft Office Mobile.</caps:sentence>
                <caps:sentence id="src232" class="srcSentence"> The URL you use will be <ui>https://play.google.com/store/apps/details?id=com.microsoft.office.officehub</ui>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <nextSteps>
        <content>
          <para></para>
        </content>
      </nextSteps>
      <relatedTopics>
        <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>