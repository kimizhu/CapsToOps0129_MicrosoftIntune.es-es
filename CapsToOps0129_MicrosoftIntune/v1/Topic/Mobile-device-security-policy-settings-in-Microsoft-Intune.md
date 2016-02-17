---
title: Configuraci&#243;n de directivas de seguridad de dispositivos m&#243;viles en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e5ab3b76-08af-4893-b294-fb6627fdc4c6
---
# Configuraci&#243;n de directivas de seguridad de dispositivos m&#243;viles en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="78d6cde0f35a9fdfb2db11b6a320ad4a" id="tgt1" class="tgtSentence">
              <token>wit_firstref</token> ahora ofrece directivas de configuración independientes para cada plataforma de dispositivo, y estas directivas contienen la configuración más actualizada que se puede usar.</caps:sentence>
            <caps:sentence sentenceid="75553b67be5bc87bdbffd8e0448f1452" id="tgt2" class="tgtSentence"> Se puede seguir usando la directiva de seguridad de dispositivo móvil, pues las implementaciones existentes seguirán funcionando.</caps:sentence>
            <caps:sentence sentenceid="d601229054343e3347a8dc5a98334101" id="tgt3" class="tgtSentence"> Sin embargo, debe planear la migración a las nuevas directivas de configuración tan pronto como sea posible, ya que la directiva de seguridad de dispositivos móviles se eliminará en el futuro.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="01f8cf1e5ff5e37b41cca78526df1e76" id="tgt4" class="tgtSentence">Utilice las directivas de seguridad de dispositivos móviles de <token>wit_firstref</token> para configurar una amplia variedad de opciones que puede implementar para los dispositivos administrados de su organización.</caps:sentence>
          <caps:sentence sentenceid="b8a9ea974ae9f0e78671f6ddd8ea94c0" id="tgt5" class="tgtSentence"> Estas opciones de configuración se pueden usar para controlar la funcionalidad y la seguridad de los dispositivos.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="783ac6d76428cf74cb92c50c6a88c5ce" id="tgt6" class="tgtSentence">Puede crear e implementar directivas de seguridad de dispositivos móviles para los siguientes tipos de dispositivo:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="fc8f0165495c50b06190a092284fc5de" id="tgt7" class="tgtSentence">Dispositivos Windows RT 8.1 y dispositivos Windows 8.1 inscritos</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt8" class="tgtSentence">Windows RT</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt9" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt10" class="tgtSentence">iOS</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt11" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence sentenceid="536b4c09c272d7a1bd2fd3ed44964799" id="tgt12" class="tgtSentence">Algunas opciones no son aplicables a algunos dispositivos.</caps:sentence>
            <caps:sentence sentenceid="0248fb2c0b346f58d13f57e42ca50883" id="tgt13" class="tgtSentence"> Consulte la tabla siguiente para obtener una lista completa de opciones que se pueden configurar.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="95b272b6e0a7cccdc1af3b36e7458a7b" id="tgt14" class="tgtSentence">Crear una directiva de seguridad de dispositivos móviles</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt15" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Agregar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt16" class="tgtSentence">Haga clic en <ui>Configuración de dispositivo móvil común</ui> &gt; <ui>Seguridad de dispositivos móviles</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9d2552da95fcbfb44084d280981f48e4" id="tgt17" class="tgtSentence">Elija si desea crear una directiva que contiene la configuración recomendada o si desea crear una directiva personalizada y, después, haga clic en <ui>Crear directiva</ui>.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="ccf9d684a76af8a6305c398f908d31f1" id="tgt18" class="tgtSentence">Haga clic en el icono de información junto a cada valor para ver el valor recomendado para la opción.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence sentenceid="e19316ff66f05bdcf357a1e5cf0dfea1" id="tgt19" class="tgtSentence">Si necesita más información acerca de cómo crear e implementar directivas, consulte el tema <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="abda7877548e2693387fce7b54bf4008" id="tgt20" class="tgtSentence">Consulte la sección <link xlink:href="e5ab3b76-08af-4893-b294-fb6627fdc4c6#BKMK_Settings">Policy settings for mobile devices</link> de este tema para obtener información acerca de las opciones que puede configurar.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt21" class="tgtSentence">Cuando haya terminado haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt22" class="tgtSentence">La nueva directiva se muestra en el nodo <ui>Directivas de configuración</ui> del área de trabajo <ui>Directiva</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="b5d01c8595ab1a703cfb232c37a620d5" id="tgt23" class="tgtSentence">Implementar una directiva de seguridad de dispositivos móviles</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="55c6b8eb4d9b754e8c9ff0f6d1894b2a" id="tgt24" class="tgtSentence">Implemente la directiva de seguridad de dispositivos móviles en uno o más grupos de usuarios o dispositivos de su organización.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="ad5c1bcb5291ef46b20f2e8f623f5ca4" id="tgt25" class="tgtSentence">Para obtener más información sobre cómo implementar directivas, consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="01d86b2114262db694dc64c0bb564e2d" id="tgt26" class="tgtSentence">En el área de trabajo <ui>Directiva</ui> de la página <ui>General</ui>, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención.</caps:sentence>
                  <caps:sentence sentenceid="f38e8d4a29f6e64f69b2faa73bb44771" id="tgt27" class="tgtSentence"> Además, aparece un resumen de estado en el área de trabajo <ui>Panel</ui>.</caps:sentence>
                </para>
                <alert class="important">
                  <para>
                    <caps:sentence sentenceid="a339d83d70ee476186202597f6fed1f7" id="tgt28" class="tgtSentence">La información sobre el estado puede tardar hasta 24 horas en aparecer en la consola de administración de <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </alert>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Settings" expanded="true">
        <title>
          <caps:sentence sentenceid="a9b41065620050dcc9f0a74c866f70c8" id="tgt29" class="tgtSentence">Configuración de directivas para dispositivos móviles</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section address="BKMK_sec" expanded="true">
            <title>
              <caps:sentence sentenceid="4dfc8238219173ac50d6f602bd6f59cd" id="tgt30" class="tgtSentence">Configuración de seguridad</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt31" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt32" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt33" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt34" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt35" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt36" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="00e48d1f688610a2c1bc595a2aaad4db" id="tgt37" class="tgtSentence">Requerir una contraseña para desbloquear dispositivos móviles</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt38" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt39" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt40" class="tgtSentence">Sí</caps:sentence>
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
                          <caps:sentence sentenceid="dca92e82330f06a43bed4c39a9ae8a45" id="tgt43" class="tgtSentence">Tipo de contraseña obligatoria</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="673ec97b13a814ace1bdb7efea92d383" id="tgt44" class="tgtSentence">(especifica el tipo de contraseña que será necesario, como solo numérica o alfanumérica).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt45" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt46" class="tgtSentence">Sí</caps:sentence>
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
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt49" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="484685f502a8f416bcf92e78a2b673ec" id="tgt50" class="tgtSentence">Tipo de contraseña requerida: número mínimo de conjuntos de caracteres</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="f436d05af8cc158ec3146b927d809dd9" id="tgt51" class="tgtSentence">Hay cuatro conjuntos de caracteres: letras minúsculas, letras mayúsculas, símbolos y números.</caps:sentence>
                        <caps:sentence sentenceid="256ecca469c924c14a7ad824a453e019" id="tgt52" class="tgtSentence"> Esta configuración especifica cuántos conjuntos de caracteres diferentes deben incluirse en la contraseña.</caps:sentence>
                        <caps:sentence sentenceid="50aad4a3d8ba306bf04418b5e31363f3" id="tgt53" class="tgtSentence"> Sin embargo, para dispositivos iOS, especifica el número de caracteres de símbolos que deben incluirse en la contraseña.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt54" class="tgtSentence">Sí<superscript>2</superscript></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt55" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt56" class="tgtSentence">Sí</caps:sentence>
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
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2f276c6158fbb9b45297b2600181d32d" id="tgt59" class="tgtSentence">Longitud mínima de contraseña</caps:sentence>
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
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt62" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt63" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt64" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9903f598b57a7f39747ca848a1376d18" id="tgt65" class="tgtSentence">Permitir contraseñas sencillas</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="4f1e869c0cf4719448849db8258003df" id="tgt66" class="tgtSentence">Contraseñas sencillas serían, por ejemplo, "0000" y "1234".</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt67" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt68" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt69" class="tgtSentence">Sí</caps:sentence>
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
                          <caps:sentence sentenceid="aad4971834ff738bf7c82b31d2513c23" id="tgt72" class="tgtSentence">Número de errores de inicio de sesión repetidos que se permiten antes de que se borre el dispositivo</caps:sentence>
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
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt74" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt75" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt76" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt77" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9c77c0d298b482fc19eba178ba592b67" id="tgt78" class="tgtSentence">Minutos de inactividad antes de que se apague la pantalla</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt79" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt80" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt81" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt82" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt83" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt84" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2fb470a15f63e1990f7635ac30db44d7" id="tgt85" class="tgtSentence">Expiración de contraseña (días)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt86" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt87" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt88" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt89" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt90" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="bd7e3f529ae9c075d09f3b7116bbe632" id="tgt91" class="tgtSentence">Recordar el historial de contraseñas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt92" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt93" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt94" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt95" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt96" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0e592e13acb6618a4ca5a3126b0bfa63" id="tgt97" class="tgtSentence">
                          <ui>Recordar historial de la contraseña</ui>: <ui>Impedir la reutilización de contraseñas anteriores</ui></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt98" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt99" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt100" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt101" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt102" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9e9b99fa7ec9aee1de52865489683bc6" id="tgt103" class="tgtSentence">Calidad de contraseña</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt104" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt105" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt106" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt107" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt108" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="599a1558c182afbc03db5b8265350ffe" id="tgt109" class="tgtSentence">Permitir contraseña de imagen y PIN</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt110" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt111" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt112" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt113" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt114" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c6f50988cb876f83b08878649ee5446b" id="tgt115" class="tgtSentence">Minutos de inactividad antes de que se pida la contraseña</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt116" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt117" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt118" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt119" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt120" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt121" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d0569abb86c04c16833d42071ed293ff" id="tgt122" class="tgtSentence">Permitir desbloqueo mediante huellas digitales</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt123" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt124" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt125" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25fbb9e01328ad82abeac6034a48a5b3" id="tgt126" class="tgtSentence">iOS 7 y versiones posteriores</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt127" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="d307d16a85b290e2b9acae7e13becc02" id="tgt128" class="tgtSentence">
                  <superscript>1</superscript> En los dispositivos iOS, cuando configura las opciones <ui>Minutos de inactividad antes de que se apague la pantalla</ui> y <ui>Minutos de inactividad antes de que sea necesaria la contraseña</ui>, estas se aplican en secuencia.</caps:sentence>
                <caps:sentence sentenceid="0e41fab1af7302bd345c5eec2d7cc3c6" id="tgt129" class="tgtSentence"> Por ejemplo, si establece el valor para ambas opciones en <ui>5</ui> minutos, la pantalla se apagará automáticamente transcurridos 5 minutos y el dispositivo se bloqueará pasados 5 minutos más.</caps:sentence>
                <caps:sentence sentenceid="7266ad0d4a29f557acb9106b66c50ce4" id="tgt130" class="tgtSentence"> Sin embargo, si el usuario apaga la pantalla manualmente, la segunda opción se aplica inmediatamente.</caps:sentence>
                <caps:sentence sentenceid="bee2d95aa2d53fae8531c5360fc269d9" id="tgt131" class="tgtSentence"> En el mismo ejemplo, una vez que el usuario apague la pantalla, el dispositivo se bloqueará 5 minutos más tarde.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="68e4641564f690bdbe6df84b5e166781" id="tgt132" class="tgtSentence">
                  <superscript>2</superscript> Cuando se implementa una directiva de longitud de contraseña para dispositivos que ejecutan Windows RT, los usuarios se verán obligados a restablecer su contraseña, aunque la contraseña actual cumpla los requisitos de la directiva.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="ddd65d7d92420afaf23beb9ab9cd3be7" id="tgt133" class="tgtSentence">Configuración de cifrado</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt134" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt135" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt136" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt137" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt138" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt139" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6ee61936fa4604c18cfc32efd91b93d5" id="tgt140" class="tgtSentence">Requerir cifrado en dispositivo móvil</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt141" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                      <para>
                        <caps:sentence sentenceid="564ef91f4823aa9f094932a962d6f442" id="tgt142" class="tgtSentence">Para dispositivos de Windows Phone 8, debe establecerse en <ui>Sí</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1c6a02e9c0537efec3523bc6efa08377" id="tgt143" class="tgtSentence">Para habilitar el cifrado en dispositivos iOS, habilite la opción <ui>Requerir una contraseña para desbloquear dispositivos móviles</ui>.</caps:sentence>
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
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt146" class="tgtSentence">Sí</caps:sentence>
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
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt149" class="tgtSentence">
                          <ui>Requerir cifrado en tarjetas de almacenamiento</ui> <superscript>2</superscript></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt150" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt151" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a8f9193f812f8fa9fa1f33d9d17af1c1" id="tgt152" class="tgtSentence">n/d (las aplicaciones y los datos asociados se cifran automáticamente)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt153" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt154" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="13255e2083914b35540684da63ec3fac" id="tgt155" class="tgtSentence">
                  <superscript>1</superscript> Información adicional para los dispositivos que ejecutan Windows 8.1</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="04aa2a349c54b727768bc4f5c9a2af37" id="tgt156" class="tgtSentence">Para forzar el cifrado en los dispositivos que ejecutan Windows 8.1, debe instalar la <externalLink><linkText>Actualización de cliente de diciembre de 2014 MDM en Windows </linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> en cada dispositivo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0e1479825d5ecb3b7572092ad74979a7" id="tgt157" class="tgtSentence">Si habilita este valor para dispositivos de Windows 8.1, todos los usuarios del dispositivo deben tener una cuenta de Microsoft.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1f6cf6b88c6face55c624e6b0e0d530" id="tgt158" class="tgtSentence">Para que el cifrado funcione, el dispositivo debe cumplir los requisitos de certificación de hardware de Microsoft <externalLink><linkText>InstantGo</linkText><linkUri>http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1a43fc77f8aeb73b1f10a0d0ac884235" id="tgt159" class="tgtSentence">Al exigir el cifrado en un dispositivo, solo se puede acceder a la clave de recuperación desde la cuenta de Microsoft de los usuarios, a la que se accede desde su cuenta de OneDrive.</caps:sentence>
                    <caps:sentence sentenceid="28e69dac0d8510fdc2168d3f84e4282a" id="tgt160" class="tgtSentence"> No se puede recuperar esta clave en nombre de un usuario.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="6def4f3d3fafe24045bf0615af4a8f25" id="tgt161" class="tgtSentence">
                  <superscript>2</superscript> Se aplica también a dispositivos administrados por Exchange ActiveSync.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="8e00380a370cea8bf75a0c532842e34f" id="tgt162" class="tgtSentence">Configuración de malware</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt163" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt164" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt165" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt166" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt167" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt168" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="bde056659cf8d8d00c90cf82f2fd8739" id="tgt169" class="tgtSentence">Requerir firewall de red</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt170" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt171" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt172" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt173" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt174" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e193432d344954d2ff1ed1f9e7ae2aa2" id="tgt175" class="tgtSentence">Habilitar SmartScreen</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt176" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt177" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt178" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt179" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt180" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="621e3306e54a1464a3b513c46e371145" id="tgt181" class="tgtSentence">Configuración del sistema</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt182" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt183" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt184" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt185" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt186" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt187" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3b6305eb7e96c55a1375646e0e48a023" id="tgt188" class="tgtSentence">Requerir actualizaciones automáticas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt189" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt190" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt191" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt192" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt193" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f88e0a610ae00360d5981961a873a90c" id="tgt194" class="tgtSentence">Requerir actualizaciones automáticas: clasificación mínima de actualizaciones para instalar automáticamente </caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt195" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                      <para>
                        <caps:sentence sentenceid="208ad7a1e1ad18e9901df8bd6050904e" id="tgt196" class="tgtSentence">Seleccione la clasificación de actualizaciones que se instalarán automáticamente:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="8631d949e5d4532385c465e03ab33254" id="tgt197" class="tgtSentence">
                              <ui>Importante</ui>: instala todas las actualizaciones que se clasifican como importantes.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ddde09bf2eeb57f460d6b83247833078" id="tgt198" class="tgtSentence">
                              <ui>Recomendada</ui>: instala todas las actualizaciones que se clasifican como importantes o recomendadas.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt199" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt200" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt201" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt202" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt203" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0404a8a7a4917a78c040cfb0df59a1df" id="tgt204" class="tgtSentence">Permitir captura de pantalla</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt205" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt206" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt207" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt208" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt209" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a5588daba5a86c481df38445e7bc0e8c" id="tgt210" class="tgtSentence">Permitir centro de control en la pantalla de bloqueo</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt211" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt212" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt213" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25fbb9e01328ad82abeac6034a48a5b3" id="tgt214" class="tgtSentence">iOS 7 y versiones posteriores</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt215" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="deef7e36d2734321fda87cdc044ab642" id="tgt216" class="tgtSentence">Permitir vista de notificaciones en la pantalla de bloqueo</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt217" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt218" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt219" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25fbb9e01328ad82abeac6034a48a5b3" id="tgt220" class="tgtSentence">iOS 7 y versiones posteriores</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt221" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="74c8a3158b4a12629a3580a4e34c80db" id="tgt222" class="tgtSentence">Permitir vista de hoy en la pantalla de bloqueo</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt223" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt224" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt225" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25fbb9e01328ad82abeac6034a48a5b3" id="tgt226" class="tgtSentence">iOS 7 y versiones posteriores</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt227" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a33b7f65aa61e08d39296d64a265d815" id="tgt228" class="tgtSentence">Control de cuentas de usuario</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt229" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt230" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt231" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt232" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt233" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8105846d4b7150b1c6849bc3e7994889" id="tgt234" class="tgtSentence">Permitir el envío de datos de diagnóstico</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt235" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt236" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt237" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt238" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt239" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="126a842bd18c92d62723308ad2f021ac" id="tgt240" class="tgtSentence">Permitir certificados TLS que no son de confianza</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt241" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt242" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt243" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt244" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt245" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="552b9b0340a459c1263382d94cb7aea8" id="tgt246" class="tgtSentence">Permitir el software de cartera personal durante un bloqueo</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt247" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt248" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt249" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt250" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt251" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="608181c0e21051993fa84c1754b29b65" id="tgt252" class="tgtSentence">Permitir el restablecimiento de la configuración de fábrica</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt253" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt254" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt255" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt256" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt257" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="9dbefa36f3fb44490f39123ff8a41561" id="tgt258" class="tgtSentence">
                  <superscript>1</superscript> Para forzar el cifrado en los dispositivos que ejecutan Windows 1, debe instalar la <externalLink><linkText>Actualización de cliente de diciembre de 8.1 MDM en Windows</linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> en cada dispositivo.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_cloud" expanded="true">
            <title>
              <caps:sentence sentenceid="5ac5d7b85913db1a420f267dcaa4b286" id="tgt259" class="tgtSentence">Configuración de nube: documentos y datos</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt260" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt261" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt262" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt263" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt264" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt265" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3e75813582c6d1c29e582c0df341503f" id="tgt266" class="tgtSentence">Permitir copias de seguridad en iCloud</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt267" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt268" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt269" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt270" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt271" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="388f4819e3a67636f905c3598ac3ca01" id="tgt272" class="tgtSentence">Permitir sincronización de documentos en iCloud</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt273" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt274" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt275" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt276" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt277" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="799717449231aea76c42b1fe7f68a627" id="tgt278" class="tgtSentence">Permitir sincronización de Photo Stream en iCloud</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt279" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt280" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt281" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt282" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt283" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="69bc5863cde2172abb6af47c6f550b92" id="tgt284" class="tgtSentence">Requerir copia de seguridad cifrada</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt285" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt286" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt287" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt288" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt289" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="735bff1b7ea46e575f38d35c8075f761" id="tgt290" class="tgtSentence">Dirección URL de carpetas de trabajo</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="03ad9effd4c60820b30ddc0e4a299de8" id="tgt291" class="tgtSentence">(establece la dirección URL de la carpeta de trabajo para permitir que los documentos se sincronicen en todos los dispositivos)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt292" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt293" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt294" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt295" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt296" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d4ee6da051209c3d059005435cf4410a" id="tgt297" class="tgtSentence">Permitir copia de seguridad de Google</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt298" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt299" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt300" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt301" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt302" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="cb3b851ef85207fa479d6e0aec32b937" id="tgt303" class="tgtSentence">Configuración de nube: cuentas y sincronización</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt304" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt305" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt306" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt307" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt308" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt309" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="34d59c1187653c22ca1945abd1e99469" id="tgt310" class="tgtSentence">Permitir cuenta de Microsoft</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt311" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt312" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt313" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt314" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt315" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4e6ab245815ee0f96be82e5c04ec4629" id="tgt316" class="tgtSentence">Permitir la sincronización automática de la cuenta de Google</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt317" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt318" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt319" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt320" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt321" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_email" expanded="true">
            <title>
              <caps:sentence sentenceid="b70b51c3cbc157e714fc4f486985d666" id="tgt322" class="tgtSentence">Configuración de correo electrónico</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt323" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt324" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt325" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt326" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt327" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt328" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="17836474810ec136a53ef50ae13b53ae" id="tgt329" class="tgtSentence">Permitir a los usuarios descargar datos adjuntos de correo electrónico</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt330" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt331" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt332" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt333" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt334" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt335" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1d04bab799f80dd2c6becf1583d443e9" id="tgt336" class="tgtSentence">Periodo de sincronización del correo electrónico</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt337" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt338" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt339" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt340" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt341" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt342" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt343" class="tgtSentence">
                          <ui>‎Permitir que los dispositivos móviles que no son totalmente compatibles con esta configuración se sincronicen con Exchange (Exchange ActiveSync)</ui>
                          <superscript>1</superscript>
                        </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt344" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt345" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt346" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt347" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt348" class="tgtSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="eeafdcc3ddf2a74a877fb9a274423661" id="tgt349" class="tgtSentence">Hacer que la cuenta Microsoft sea opcional en la aplicación Windows Mail</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt350" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt351" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt352" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt353" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt354" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="bb8e3c8fd2e7c158822256e459ec0edc" id="tgt355" class="tgtSentence">Permitir cuentas de correo electrónico personalizadas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt356" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt357" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt358" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt359" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt360" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="6def4f3d3fafe24045bf0615af4a8f25" id="tgt361" class="tgtSentence">
                  <superscript>1</superscript> Se aplica también a dispositivos administrados por Exchange ActiveSync.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_browser" expanded="true">
            <title>
              <caps:sentence sentenceid="06746f3d881795846a0870dc6d355fd7" id="tgt362" class="tgtSentence">Configuración de la aplicación: explorador</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt363" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt364" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt365" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt366" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt367" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt368" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a0c48d4afe3535baaeabfa7149c6ef7a" id="tgt369" class="tgtSentence">Permitir explorador web</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt370" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt371" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt372" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt373" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt374" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e047ee944ff7459a4014e5e126e5e963" id="tgt375" class="tgtSentence">Permitir el autorrelleno</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt376" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt377" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt378" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt379" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt380" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1b2a6b1dd6c8827b383f55ca82da08c8" id="tgt381" class="tgtSentence">Permitir bloqueador de elementos emergentes</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt382" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt383" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt384" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt385" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt386" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2c3b0c032374c0766b908511ca23da8c" id="tgt387" class="tgtSentence">Permitir cookies</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt388" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt389" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt390" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt391" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt392" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6ff864914a0d00af70203ffdaab9015e" id="tgt393" class="tgtSentence">Permitir complementos</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt394" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt395" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt396" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt397" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt398" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e1c3ff920a64a9bd299d2d0f8b43d0fa" id="tgt399" class="tgtSentence">Permitir Active scripting</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt400" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt401" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt402" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt403" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt404" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="dcc733e492fd957f1d798d9c0050f31e" id="tgt405" class="tgtSentence">Permitir advertencias de fraude</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt406" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt407" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt408" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt409" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt410" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b95f6e0fbf9465ba046084e9c23da640" id="tgt411" class="tgtSentence">Permitir el acceso a sitios de intranet por la entrada de una sola palabra</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="a4018b221eb67660c98822d4feae0bbf" id="tgt412" class="tgtSentence">(permite el uso de una sola palabra para dirigir Internet Explorer a un sitio web como, por ejemplo, "Bing")</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt413" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt414" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt415" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt416" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt417" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="beb88125affa16172ecab8ead56124c3" id="tgt418" class="tgtSentence">Permitir la detección automática de redes de intranet</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt419" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt420" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt421" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt422" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt423" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4b9d9dc6621cf87b4c15ae9dff57114a" id="tgt424" class="tgtSentence">Nivel de seguridad de Internet</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt425" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt426" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt427" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt428" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt429" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e89cd4dd97c7f886785b6ffbab06e79e" id="tgt430" class="tgtSentence">Nivel de seguridad de intranet</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt431" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt432" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt433" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt434" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt435" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="55dc66e16dbee875acc2f3fcb9afb0ed" id="tgt436" class="tgtSentence">Nivel de seguridad de sitios de confianza</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt437" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt438" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt439" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt440" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt441" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="27af881ca31cfcd20f86a5256a215cf5" id="tgt442" class="tgtSentence">Nivel de seguridad de sitios restringidos</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt443" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt444" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt445" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt446" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt447" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2396b23f36a57f25d78bc6029de6fd63" id="tgt448" class="tgtSentence">Enviar encabezado Do Not Track</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt449" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt450" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt451" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt452" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt453" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="90695fab9db4ed43a3e3a73ed6a0b3b4" id="tgt454" class="tgtSentence">Permitir el acceso al menú Modo de empresa</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt455" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt456" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt457" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt458" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt459" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9d283a482cbd56c47e4fbee8fe755804" id="tgt460" class="tgtSentence">Ubicación de la lista de sitios de Modo de empresa</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt461" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt462" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt463" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt464" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt465" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_apps" expanded="true">
            <title>
              <caps:sentence sentenceid="1fc255764272758aa0421dbfe0ddf895" id="tgt466" class="tgtSentence">Configuración de la aplicación: aplicaciones</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt467" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt468" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt469" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt470" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt471" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt472" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f956e1c595e427cc2f06ff42da87a73f" id="tgt473" class="tgtSentence">Permitir almacén de aplicaciones</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt474" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt475" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt476" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt477" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt478" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d0d37a9e950cd9b67c447a724a0a10ff" id="tgt479" class="tgtSentence">Requerir una contraseña para tener acceso al almacén de aplicaciones</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt480" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt481" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt482" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt483" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt484" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="15bbbd631e65a3eaea9ba110f5379651" id="tgt485" class="tgtSentence">Permitir compras dentro de la aplicación</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt486" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt487" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt488" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt489" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt490" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="cca28dc78879d7456286b10f239585c4" id="tgt491" class="tgtSentence">Permitir documentos administrados en otras aplicaciones no administradas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt492" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt493" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt494" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25fbb9e01328ad82abeac6034a48a5b3" id="tgt495" class="tgtSentence">iOS 7 y versiones posteriores</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt496" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="89b7c130f4a6a761f835def592db27ec" id="tgt497" class="tgtSentence">Permitir documentos no administrados en otras aplicaciones administradas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt498" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt499" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt500" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25fbb9e01328ad82abeac6034a48a5b3" id="tgt501" class="tgtSentence">iOS 7 y versiones posteriores</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt502" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5ff7ade21b54d5c5a2ed50d69bc4ca50" id="tgt503" class="tgtSentence">Permitir videoconferencias</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt504" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt505" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt506" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt507" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt508" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="824ac3d0d9c9b0f8a457c0c7cae6ef26" id="tgt509" class="tgtSentence">Permitir contenido para adultos en el almacén multimedia</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt510" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt511" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt512" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt513" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt514" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="978a2b4d0dd07d1dc40b6304f88117f7" id="tgt515" class="tgtSentence">Permitir la instalación de aplicaciones</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt516" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt517" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt518" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt519" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt520" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="3a2a434c2e11cedc218c3d03fe57e840" id="tgt521" class="tgtSentence">Configuración de la aplicación: juegos</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt522" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt523" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt524" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt525" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt526" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt527" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c29f353a504a0ff8b66b2ba94a80cc0a" id="tgt528" class="tgtSentence">Permitir amigos del Game Center</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt529" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt530" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt531" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt532" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt533" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="87e39875bf498d0817176fa1cbb4ee9e" id="tgt534" class="tgtSentence">Permitir juegos multijugador</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt535" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt536" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt537" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt538" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt539" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_hard" expanded="true">
            <title>
              <caps:sentence sentenceid="8868ff8ede3d8e50302ccfd0fbe08fa2" id="tgt540" class="tgtSentence">Configuración de funcionalidades del dispositivo: hardware</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt541" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt542" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt543" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt544" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt545" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt546" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="05dd919b3a7292227de28546f39f4928" id="tgt547" class="tgtSentence">Permitir cámara</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt548" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt549" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt550" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt551" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt552" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ce113c55d1b3a3b1616bd8d58f2d6fdb" id="tgt553" class="tgtSentence">Permitir almacenamiento extraíble</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt554" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt555" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt556" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt557" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt558" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8dc8bec3c22373dd8447523e6202a5d4" id="tgt559" class="tgtSentence">Permitir Wi-Fi</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt560" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt561" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt562" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt563" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt564" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5e2d5cfbfc5736a9055a62acc9465520" id="tgt565" class="tgtSentence">Permitir Wi-Fi Tethering</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt566" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt567" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt568" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt569" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt570" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6da9e7b6cf656a40f0f3079fe763e272" id="tgt571" class="tgtSentence">Permitir la conexión automática a zonas Wi-Fi gratuitas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt572" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt573" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt574" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt575" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt576" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="051640f64cfb604b6ba0ea831cb32db8" id="tgt577" class="tgtSentence">Permitir informar de zonas Wi-Fi</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="27d14c21167377dfb78d30d1e745302e" id="tgt578" class="tgtSentence">(enviar información acerca de las conexiones Wi-Fi para ayudar a detectar conexiones cercanas)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt579" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt580" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt581" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt582" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt583" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2c41b4c56056968e9f89851a7650f6ed" id="tgt584" class="tgtSentence">Permitir geolocalización</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="54d1d9dc079a0e71d46173926b7bdac9" id="tgt585" class="tgtSentence">(permite que el dispositivo use la información de ubicación)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt586" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt587" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt588" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt589" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt590" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1773b705c6c985b2c179ff71b1d8a9eb" id="tgt591" class="tgtSentence">Permitir NFC</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="61d63d3ebe635c14c40732c4174c93f3" id="tgt592" class="tgtSentence">(permite las operaciones que usan la transmisión de datos en proximidad)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt593" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt594" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt595" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt596" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt597" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f5b02fb1ac756124bdb8eaa270d0c1b2" id="tgt598" class="tgtSentence">Permitir Bluetooth</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt599" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt600" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt601" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt602" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt603" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0036c994fc54780c3fe33b48bbb6ad2b" id="tgt604" class="tgtSentence">Permitir desconectar</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt605" class="tgtSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt606" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt607" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt608" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt609" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt610" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="b08c860e8631d03c9bd34d33411dffda" id="tgt611" class="tgtSentence">
                  <superscript>1</superscript> Si se deshabilita esta opción, la opción <ui>Número de errores de inicio de sesión repetidos que se permiten antes de que se eliminen los datos del dispositivo</ui> de los dispositivos Samsung KNOX no funciona.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="52e183edd25a42305b595b80551ab7a9" id="tgt612" class="tgtSentence">Configuración de funcionalidades del dispositivo: datos móviles</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt613" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt614" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt615" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt616" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt617" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt618" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7b57e74c6890ff3c771ae41ec0178dcd" id="tgt619" class="tgtSentence">Permitir itinerancia de voz</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt620" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt621" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt622" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt623" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt624" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c2d252651547ad4dfa328dcf51811431" id="tgt625" class="tgtSentence">Permitir itinerancia de datos</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt626" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt627" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt628" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt629" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt630" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ecf2e3dcd5bc239b53446105c1d607ad" id="tgt631" class="tgtSentence">Permitir la sincronización automática en itinerancia</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt632" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt633" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt634" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt635" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt636" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7a4807d26f0a57c865542194b3a896f4" id="tgt637" class="tgtSentence">Permitir mensajería SMS y MMS</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt638" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt639" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt640" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt641" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt642" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="ac27b430b679e95693410b0ae55eafde" id="tgt643" class="tgtSentence">Configuración de funcionalidades del dispositivo: características</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt644" class="tgtSentence">Nombre de la configuración</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt645" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt646" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b35778ff0b935400feebbe60eb0446" id="tgt647" class="tgtSentence">Windows Phone 8 y Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt648" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f113c591704b11229a0eec6ec5a90233" id="tgt649" class="tgtSentence">Android y Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="de8cad2852e0f20cb63cfb0a37fda788" id="tgt650" class="tgtSentence">Permitir asistente de voz</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt651" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt652" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt653" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt654" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt655" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9d91c16314828972a73e4592e873c7d5" id="tgt656" class="tgtSentence">Permitir asistente de voz con el dispositivo bloqueado</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt657" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt658" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt659" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt660" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt661" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0e9d7a3a8a5a48009347229ab6b471a1" id="tgt662" class="tgtSentence">Permitir la marcación por voz</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt663" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt664" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt665" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt666" class="tgtSentence">Sí</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt667" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f98807ee3f4cbb43e555d032ecbbcb5c" id="tgt668" class="tgtSentence">Permitir copiar y pegar</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt669" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt670" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93c158c2e30faf7ef9a30d7f379e2720" id="tgt671" class="tgtSentence">Windows Phone 8.1 solo</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt672" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt673" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="86346db0261d443bbddafdcb103c6d61" id="tgt674" class="tgtSentence">Permitir el uso compartido del Portapapeles entre aplicaciones</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt675" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt676" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt677" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt678" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt679" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f3848a5ba1d65031d70a43ab92edfddf" id="tgt680" class="tgtSentence">Permitir YouTube</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt681" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt682" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt683" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt684" class="tgtSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a737f8e9d4497e5132dc7d743ecf5b0f" id="tgt685" class="tgtSentence">Sí (solo Samsung KNOX)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
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
        <alert class="important">
          <para>
            <caps:sentence id="src1" class="srcSentence">
              <token>wit_firstref</token> now features separate configuration policies for each device platform, and these policies contain the most up-to-date settings you can use.</caps:sentence>
            <caps:sentence id="src2" class="srcSentence"> You can continue to use the mobile device security policy and any existing deployments will still work.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> However, you should plan to migrate to the new configuration policies as soon as possible as the mobile device security policy will be removed in the future.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src4" class="srcSentence">Use <token>wit_firstref</token> mobile device security policies to configure a wide range of settings that you can deploy to managed devices in your organization.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> These settings can be used to control the functionality and security of your devices.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">You can create and deploy mobile device security policies for the following device types:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Windows RT 8.1 and enrolled Windows 8.1 devices</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Windows RT</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">iOS</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">Android and Samsung KNOX</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="note">
          <para>
            <caps:sentence id="src12" class="srcSentence">Some settings are not applicable to some devices.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> See the table below for a full list of settings you can configure.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Create a mobile device security policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Click <ui>Common Mobile Device Settings</ui> &gt; <ui>Mobile Device Security</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">Choose whether you want to create a policy that contains recommended settings, or whether you want to create a custom policy, and then click <ui>Create Policy</ui>.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src18" class="srcSentence">Click the information icon next to each setting to view the recommended value for the setting.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">For more information about how to create and deploy policies, see the <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link> topic.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">See the <link xlink:href="e5ab3b76-08af-4893-b294-fb6627fdc4c6#BKMK_Settings">Policy settings for mobile devices</link> section in this topic for information about the settings you can configure.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">When you are finished, click <ui>Save Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src22" class="srcSentence">The new policy displays in the <ui>Configuration Policies</ui> node of the <ui>Policy</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src23" class="srcSentence">Deploy a mobile device security policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">Deploy the mobile device security policy to one or more groups of users or devices in your organization.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src25" class="srcSentence">For more information about how to deploy policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src26" class="srcSentence">A status summary and alerts on the <ui>Overview</ui> page of the <ui>Policy</ui> workspace identify issues with the policy that require your attention.</caps:sentence>
                  <caps:sentence id="src27" class="srcSentence"> Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</caps:sentence>
                </para>
                <alert class="important">
                  <para>
                    <caps:sentence id="src28" class="srcSentence">It might take up to 24 hours for status information to appear in the <token>wit_nextref</token> admin console.</caps:sentence>
                  </para>
                </alert>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Settings" expanded="true">
        <title>
          <caps:sentence id="src29" class="srcSentence">Policy settings for mobile devices</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section address="BKMK_sec" expanded="true">
            <title>
              <caps:sentence id="src30" class="srcSentence">Security settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src31" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src32" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src33" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src37" class="srcSentence">Require a password to unlock mobile devices</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src39" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">Yes</caps:sentence>
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
                          <caps:sentence id="src43" class="srcSentence">Required password type</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">(specifies the type of password that will be required, such as numeric only, or alphanumeric)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Yes</caps:sentence>
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
                    <TD>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src50" class="srcSentence">Required password type – Minimum number of character sets</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">There are four character sets, lowercase letters, uppercase letters, numbers, and symbols.</caps:sentence>
                        <caps:sentence id="src52" class="srcSentence"> This setting specifies how many different character sets must be included in the password).</caps:sentence>
                        <caps:sentence id="src53" class="srcSentence"> However, for iOS devices, this specifies the number of symbol characters must be included in the password)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">Yes<superscript>2</superscript></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src55" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">Yes</caps:sentence>
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
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src59" class="srcSentence">Minimum password length</caps:sentence>
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
                    <TD>
                      <para>
                        <caps:sentence id="src62" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src65" class="srcSentence">Allow simple passwords</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">Simple passwords include ‘0000’ and ‘1234’</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src67" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">Yes</caps:sentence>
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
                          <caps:sentence id="src72" class="srcSentence">Number of repeated sign-in failures to allow before the device is wiped</caps:sentence>
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
                        <caps:sentence id="src74" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src75" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src76" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src77" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src78" class="srcSentence">Minutes of inactivity before screen turns off</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src79" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src82" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src83" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src84" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src85" class="srcSentence">Password expiration (days)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src91" class="srcSentence">Remember password history</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src93" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src94" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src96" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src97" class="srcSentence">
                          <ui>Remember password history</ui> – <ui>Prevent reuse of previous passwords</ui></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src98" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src99" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src100" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src103" class="srcSentence">Password quality</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src104" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src105" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src108" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src109" class="srcSentence">Allow picture password and PIN</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src110" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src111" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src112" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src113" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src114" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src115" class="srcSentence">Minutes of inactivity before password is required</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src116" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src117" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src118" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src121" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src122" class="srcSentence">Allow fingerprint unlock</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src123" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src124" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src125" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src126" class="srcSentence">iOS 7 and later</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src127" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src128" class="srcSentence">
                  <superscript>1</superscript> For iOS devices, when you configure the settings <ui>Minutes of inactivity before screen turns off</ui> and <ui>Minutes of inactivity before password is required</ui>, they are applied in sequence.</caps:sentence>
                <caps:sentence id="src129" class="srcSentence"> For example, if you set the value for both settings to <ui>5</ui> minutes, the screen will turn off automatically after 5 minutes, and the device will be locked after an additional 5 minutes.</caps:sentence>
                <caps:sentence id="src130" class="srcSentence"> However, if the user turns off the screen manually, the second setting is immediately applied.</caps:sentence>
                <caps:sentence id="src131" class="srcSentence"> In the same example, after the user turns off the screen, the device will lock 5 minutes later.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src132" class="srcSentence">
                  <superscript>2</superscript> When you set deploy a password length policy to devices that run Windows RT, users will be forced to reset their password, even if their current password complies with the policy requirements.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src133" class="srcSentence">Encryption settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src134" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src135" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src136" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src137" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src138" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src139" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src140" class="srcSentence">Require encryption on mobile device</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src141" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                      <para>
                        <caps:sentence id="src142" class="srcSentence">For Windows Phone 8 devices, you must set this to <ui>Yes</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src143" class="srcSentence">To enable encryption on iOS devices, enable the setting <ui>Require a password to unlock mobile devices</ui>.</caps:sentence>
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
                    <TD>
                      <para>
                        <caps:sentence id="src146" class="srcSentence">Yes</caps:sentence>
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
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src149" class="srcSentence">
                          <ui>Require encryption on storage cards</ui> <superscript>2</superscript></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src150" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src151" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src152" class="srcSentence">n/a (apps and associated data are automatically encrypted)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src153" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src154" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src155" class="srcSentence">
                  <superscript>1</superscript> Additional information for devices that run Windows 8.1</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">To enforce encryption on devices that run Windows 8.1, you must install the <externalLink><linkText>December 2014 MDM client update for Windows</linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> on each device.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">If you enable this setting for Windows 8.1 devices, all users of the device must have a Microsoft Account.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src158" class="srcSentence">For encryption to work, the device must meet the Microsoft <externalLink><linkText>InstantGo</linkText><linkUri>http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/</linkUri></externalLink> hardware certification requirements.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">When you enforce encryption on a device, the recovery key is only accessible from the users Microsoft Account, accessed from their OneDrive account.</caps:sentence>
                    <caps:sentence id="src160" class="srcSentence"> You cannot recover this key on behalf of a user.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src161" class="srcSentence">
                  <superscript>2</superscript> Applies to devices that are managed by Exchange ActiveSync also.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src162" class="srcSentence">Malware settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src163" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src164" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src165" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src166" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src167" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src168" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src169" class="srcSentence">Require network firewall</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src170" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src171" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src172" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src173" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src174" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src175" class="srcSentence">Enable SmartScreen</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src176" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src177" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src178" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src179" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src180" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src181" class="srcSentence">System settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src182" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src183" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src184" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src185" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src186" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src187" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src188" class="srcSentence">Require automatic updates</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src189" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src190" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src191" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src192" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src193" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src194" class="srcSentence">Require automatic updates – Minimum classification of updates to install automatically </caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src195" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                      <para>
                        <caps:sentence id="src196" class="srcSentence">Choose the classification of updates that will be installed automatically:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src197" class="srcSentence">
                              <ui>Important</ui> – Installs all updates classified as important.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src198" class="srcSentence">
                              <ui>Recommended</ui> – Installs all updates classified as important or recommended.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src199" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src200" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src201" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src202" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src203" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src204" class="srcSentence">Allow screen capture</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src205" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src206" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src207" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src208" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src209" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src210" class="srcSentence">Allow control center in lock screen</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src211" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src212" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src213" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src214" class="srcSentence">iOS 7 and later</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src215" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src216" class="srcSentence">Allow notification view in lock screen</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src217" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src218" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src219" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src220" class="srcSentence">iOS 7 and later</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src221" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src222" class="srcSentence">Allow today view in lock screen</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src223" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src224" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src225" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src226" class="srcSentence">iOS 7 and later</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src227" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src228" class="srcSentence">User Account Control</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src229" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src230" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src231" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src232" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src233" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src234" class="srcSentence">Allow diagnostic data submission</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src235" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src236" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src237" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src238" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src239" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src240" class="srcSentence">Allow untrusted TLS certificates</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src241" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src242" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src243" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src244" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src245" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src246" class="srcSentence">Allow personal wallet software while locked</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src247" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src248" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src249" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src250" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src251" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src252" class="srcSentence">Allow factory reset</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src253" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src254" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src255" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src256" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src257" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src258" class="srcSentence">
                  <superscript>1</superscript> To enforce encryption on devices that run Windows 8.1, you must install the <externalLink><linkText>December 2014 MDM client update for Windows</linkText><linkUri>http://support.microsoft.com/kb/3013816</linkUri></externalLink> on each device.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_cloud" expanded="true">
            <title>
              <caps:sentence id="src259" class="srcSentence">Cloud settings – documents and data</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src260" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src261" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src262" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src263" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src264" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src265" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src266" class="srcSentence">Allow backup to iCloud</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src267" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src268" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src269" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src270" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src271" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src272" class="srcSentence">Allow document sync to iCloud</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src273" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src274" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src275" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src276" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src277" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src278" class="srcSentence">Allow Photo Stream sync to iCloud</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src279" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src280" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src281" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src282" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src283" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src284" class="srcSentence">Require encrypted backup</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src285" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src286" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src287" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src288" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src289" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src290" class="srcSentence">Work Folders URL</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src291" class="srcSentence">(sets the URL of the work folder to allow documents to be synchronized across devices)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src292" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src293" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src294" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src295" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src296" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src297" class="srcSentence">Allow Google backup</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src298" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src299" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src300" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src301" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src302" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src303" class="srcSentence">Cloud settings – accounts and synchronization</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src304" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src305" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src306" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src307" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src308" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src309" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src310" class="srcSentence">Allow Microsoft account</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src311" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src312" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src313" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src314" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src315" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src316" class="srcSentence">Allow Google account auto sync</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src317" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src318" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src319" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src320" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src321" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_email" expanded="true">
            <title>
              <caps:sentence id="src322" class="srcSentence">Email settings</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src323" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src324" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src325" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src326" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src327" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src328" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src329" class="srcSentence">Allow users to download email attachments</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src330" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src331" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src332" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src333" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src334" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src335" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src336" class="srcSentence">Email synchronization period</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src337" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src338" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src339" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src340" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src341" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src342" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src343" class="srcSentence">
                          <ui>Allow mobile devices that don’t fully support these settings to synchronize with Exchange (Exchange ActiveSync)</ui> <superscript>1</superscript></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src344" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src345" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src346" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src347" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src348" class="srcSentence">n/a</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src349" class="srcSentence">Make Microsoft account optional in Windows Mail application</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src350" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src351" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src352" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src353" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src354" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src355" class="srcSentence">Allow custom email accounts</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src356" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src357" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src358" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src359" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src360" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src361" class="srcSentence">
                  <superscript>1</superscript> Applies to devices that are managed by Exchange ActiveSync also.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_browser" expanded="true">
            <title>
              <caps:sentence id="src362" class="srcSentence">Application settings - browser</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src363" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src364" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src365" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src366" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src367" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src368" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src369" class="srcSentence">Allow web browser</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src370" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src371" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src372" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src373" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src374" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src375" class="srcSentence">Allow autofill</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src376" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src377" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src378" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src379" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src380" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src381" class="srcSentence">Allow pop-up blocker</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src382" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src383" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src384" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src385" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src386" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src387" class="srcSentence">Allow cookies</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src388" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src389" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src390" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src391" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src392" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src393" class="srcSentence">Allow plug-ins</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src394" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src395" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src396" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src397" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src398" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src399" class="srcSentence">Allow active scripting</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src400" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src401" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src402" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src403" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src404" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src405" class="srcSentence">Allow fraud warning</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src406" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src407" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src408" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src409" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src410" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src411" class="srcSentence">Allow intranet site for single word entry</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src412" class="srcSentence">(allows use of a single word to direct Internet Explorer to a web site, such as ‘Bing’)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src413" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src414" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src415" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src416" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src417" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src418" class="srcSentence">Allow automatic detection of intranet network</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src419" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src420" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src421" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src422" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src423" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src424" class="srcSentence">Security level for Internet</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src425" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src426" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src427" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src428" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src429" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src430" class="srcSentence">Security level for intranet</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src431" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src432" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src433" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src434" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src435" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src436" class="srcSentence">Security level for trusted sites</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src437" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src438" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src439" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src440" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src441" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src442" class="srcSentence">Security level for restricted sites</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src443" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src444" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src445" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src446" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src447" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src448" class="srcSentence">Send Do Not Track header</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src449" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src450" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src451" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src452" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src453" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src454" class="srcSentence">Allow Enterprise Mode menu access</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src455" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src456" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src457" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src458" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src459" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src460" class="srcSentence">Enterprise Mode site list location</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src461" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src462" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src463" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src464" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src465" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_apps" expanded="true">
            <title>
              <caps:sentence id="src466" class="srcSentence">Application settings - apps</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src467" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src468" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src469" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src470" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src471" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src472" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src473" class="srcSentence">Allow application store</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src474" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src475" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src476" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src477" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src478" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src479" class="srcSentence">Require a password to access application store</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src480" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src481" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src482" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src483" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src484" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src485" class="srcSentence">Allow in-app purchases</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src486" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src487" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src488" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src489" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src490" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src491" class="srcSentence">Allow managed documents in other unmanaged apps</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src492" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src493" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src494" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src495" class="srcSentence">iOS 7 and later</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src496" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src497" class="srcSentence">Allow unmanaged documents in other managed apps</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src498" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src499" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src500" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src501" class="srcSentence">iOS 7 and later</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src502" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src503" class="srcSentence">Allow video conferencing</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src504" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src505" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src506" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src507" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src508" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src509" class="srcSentence">Allow adult content in media store</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src510" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src511" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src512" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src513" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src514" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src515" class="srcSentence">Allow app installation</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src516" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src517" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src518" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src519" class="srcSentence">iOS 6 and later</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src520" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src521" class="srcSentence">Application settings - gaming</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src522" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src523" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src524" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src525" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src526" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src527" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src528" class="srcSentence">Allow Game Center friends</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src529" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src530" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src531" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src532" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src533" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src534" class="srcSentence">Allow multiplayer gaming</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src535" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src536" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src537" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src538" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src539" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_hard" expanded="true">
            <title>
              <caps:sentence id="src540" class="srcSentence">Device capabilities settings - hardware</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src541" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src542" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src543" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src544" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src545" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src546" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src547" class="srcSentence">Allow camera</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src548" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src549" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src550" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src551" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src552" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src553" class="srcSentence">Allow removable storage</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src554" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src555" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src556" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src557" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src558" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src559" class="srcSentence">Allow Wi-Fi</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src560" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src561" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src562" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src563" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src564" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src565" class="srcSentence">Allow Wi-Fi tethering</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src566" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src567" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src568" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src569" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src570" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src571" class="srcSentence">Allow automatic connection to free Wi-Fi hotspots</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src572" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src573" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src574" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src575" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src576" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src577" class="srcSentence">Allow Wi-Fi hotspot reporting</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src578" class="srcSentence">(send information about Wi-Fi connections to help discover nearby connections)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src579" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src580" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src581" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src582" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src583" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src584" class="srcSentence">Allow geolocation</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src585" class="srcSentence">(allows the device to utilize location information)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src586" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src587" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src588" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src589" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src590" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src591" class="srcSentence">Allow NFC</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src592" class="srcSentence">(allows operations that use near field communication)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src593" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src594" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src595" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src596" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src597" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src598" class="srcSentence">Allow Bluetooth</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src599" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src600" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src601" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src602" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src603" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src604" class="srcSentence">Allow power off</caps:sentence>
                        </ui>
                        <superscript>
                          <caps:sentence id="src605" class="srcSentence">1</caps:sentence>
                        </superscript>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src606" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src607" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src608" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src609" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src610" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src611" class="srcSentence">
                  <superscript>1</superscript> If this setting is disabled, the setting <ui>Number of repeated sign in failures to allow before the device is wiped</ui> for Samsung KNOX devices does not function.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src612" class="srcSentence">Device capabilities settings - cellular</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src613" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src614" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src615" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src616" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src617" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src618" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src619" class="srcSentence">Allow voice roaming</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src620" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src621" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src622" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src623" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src624" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src625" class="srcSentence">Allow data roaming</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src626" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src627" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src628" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src629" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src630" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src631" class="srcSentence">Allow automatic synchronization while roaming</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src632" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src633" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src634" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src635" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src636" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src637" class="srcSentence">Allow SMS/MMS messaging</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src638" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src639" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src640" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src641" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src642" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src643" class="srcSentence">Device capabilities settings - features</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src644" class="srcSentence">Setting name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src645" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src646" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src647" class="srcSentence">Windows Phone 8 and Windows Phone 8.1</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src648" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src649" class="srcSentence">Android and Samsung KNOX</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src650" class="srcSentence">Allow voice assistant</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src651" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src652" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src653" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src654" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src655" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src656" class="srcSentence">Allow voice assistant while device is locked</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src657" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src658" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src659" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src660" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src661" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src662" class="srcSentence">Allow voice dialing</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src663" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src664" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src665" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src666" class="srcSentence">Yes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src667" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src668" class="srcSentence">Allow copy and paste</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src669" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src670" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src671" class="srcSentence">Windows Phone 8.1 only</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src672" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src673" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src674" class="srcSentence">Allow clipboard share between applications</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src675" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src676" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src677" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src678" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src679" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src680" class="srcSentence">Allow YouTube</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src681" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src682" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src683" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src684" class="srcSentence">No</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src685" class="srcSentence">Yes (Samsung KNOX only)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
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