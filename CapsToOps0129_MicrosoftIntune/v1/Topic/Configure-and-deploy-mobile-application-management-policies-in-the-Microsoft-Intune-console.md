---
title: Proteger datos mediante las directivas de administraci&#243;n de aplicaciones m&#243;viles con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b4fb33a8-a2fa-4353-bd89-5bda48b68e83
---
# Proteger datos mediante las directivas de administraci&#243;n de aplicaciones m&#243;viles con Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ae80f6bc3509dccdabe407c025da7303" id="tgt1" class="tgtSentence">Las directivas de administración de aplicaciones móviles de <token>wit_firstref</token> le permiten modificar la funcionalidad de las aplicaciones que se implementan para ayudar a armonizarlas con las directivas de cumplimiento y seguridad de su compañía.</caps:sentence>
          <caps:sentence sentenceid="6b75e3f4a5d256d1ac65b93a9bb8dce6" id="tgt2" class="tgtSentence"> Por ejemplo, puede limitar las operaciones de cortar, copiar y pegar dentro de una aplicación administrada, o configurar una aplicación para abrir todos los vínculos web dentro de un explorador administrado.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="13c42332fd6fb9d81bade6827396b001" id="tgt3" class="tgtSentence">Compatibilidad con las directivas de administración de aplicaciones móviles:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="531e11f157d84cb139461224a3d6b078" id="tgt4" class="tgtSentence">Dispositivos que ejecutan Android 4 y versiones posteriores.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="1a9266baf4f89938b1fd411b4f029db6" id="tgt5" class="tgtSentence">Dispositivos que ejecutan iOS 7 y versiones posteriores.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="78b6af95727755f530d909b9083031bd" id="tgt6" class="tgtSentence">A diferencia de otras directivas de <token>wit_nextref</token>, no se implementa directamente una directiva de administración de aplicaciones móviles.</caps:sentence>
          <caps:sentence sentenceid="50e07b73d871a4bbb61156c0e9037fb8" id="tgt7" class="tgtSentence"> En su lugar, se asocia la directiva con la aplicación que desea restringir.</caps:sentence>
          <caps:sentence sentenceid="2dd71f5c984052e7075b5427dad95b70" id="tgt8" class="tgtSentence"> Cuando la aplicación se implementa e instala en dispositivos, se aplicará la configuración especificada.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1b9c911b423415300e783126467f121d" id="tgt9" class="tgtSentence">Para aplicar restricciones a una aplicación, esta debe incorporar el Kit de desarrollo de software (SDK) para aplicaciones de <token>wit_firstref</token>.</caps:sentence>
          <caps:sentence sentenceid="3d2b8c371ac4488b58e444948a26bc34" id="tgt10" class="tgtSentence"> Existen dos métodos de obtención de este tipo de aplicación:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="49ef5acca5c4f38d7e6cf35052f70a86" id="tgt11" class="tgtSentence">
                <ui>Utilizar una aplicación administrada por directiva</ui>: tiene integrado el SDK de la aplicación.</caps:sentence>
              <caps:sentence sentenceid="80ee6f2f2d7eac6629cfc2c28a3973ba" id="tgt12" class="tgtSentence"> Para agregar este tipo de aplicación, especifique un vínculo a la aplicación desde una tienda de aplicaciones como, por ejemplo, iTunes Store o Google Play.</caps:sentence>
              <caps:sentence sentenceid="fa586ca9c79c8671782d7ec708b7208a" id="tgt13" class="tgtSentence"> No es necesario ningún procesamiento adicional para este tipo de aplicación.</caps:sentence>
              <caps:sentence sentenceid="c55a66f6f539d89512910f02fbe88ca7" id="tgt14" class="tgtSentence"> Ver una lista de <link xlink:href="49023822-0aa7-4508-8119-3be8976d21d1">Managed apps for Microsoft Intune mobile application management policies</link>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="463fbc9fae7a4cd38a4e6a6a5a960317" id="tgt15" class="tgtSentence">
                <ui>Usar una aplicación "ajustada"</ui>: las aplicaciones se empaquetan a fin de incluir el SDK de la aplicación con la <ui>herramienta de ajuste de aplicaciones de Microsoft Intune</ui>.</caps:sentence>
              <caps:sentence sentenceid="1e1482c29fe18477f43e2e49ec503aff" id="tgt16" class="tgtSentence"> Esta herramienta se usa normalmente para procesar aplicaciones de empresa que se hayan creado internamente.</caps:sentence>
              <caps:sentence sentenceid="1ca1d4b8adfe5717162316d6a6ab85f1" id="tgt17" class="tgtSentence"> No se puede usar para procesar aplicaciones que se hayan descargado desde la tienda de aplicaciones.</caps:sentence>
              <caps:sentence sentenceid="78876cede6e051df998fab51465986f4" id="tgt18" class="tgtSentence"> Consulte <link xlink:href="99ab0369-5115-4dc8-83ea-db7239b0de97">Prepare iOS apps for mobile application management with the Microsoft Intune App Wrapping Tool</link> y <link xlink:href="e9c349c8-51ae-4d73-b74a-6173728a520b">Prepare Android apps for mobile application management with the Microsoft Intune App Wrapping Tool</link>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="f0d18e31b99999350b6a84e2db67bd1d" id="tgt19" class="tgtSentence">Algunas aplicaciones administradas, como la aplicación Outlook para iOS y Android admiten <ui>identidades múltiples</ui>.</caps:sentence>
          <caps:sentence sentenceid="afab1c1301608870656bd0399c7e5c92" id="tgt20" class="tgtSentence"> Esto significa que <token>wit_nextref</token> solo aplica la configuración de administración a las cuentas corporativas o los datos de la aplicación.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4dc260386d206a637a8fe6211b8d5006" id="tgt21" class="tgtSentence">Por ejemplo, mediante la aplicación de Outlook:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="8442f8736914be7493bee79fac9150ca" id="tgt22" class="tgtSentence">	Si el usuario configura una cuenta de correo electrónico de trabajo y otra personal, <token>wit_nextref</token> solo aplica la configuración de administración a la cuenta de trabajo y no administra la cuenta personal.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="42e75839c87c74503991a0356816fbf0" id="tgt23" class="tgtSentence">	Si el dispositivo se retira o se cancela la inscripción, solo los datos corporativos de Outlook se quitan del dispositivo.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="c006591f95282908997d303717af47a3" id="tgt24" class="tgtSentence">La cuenta de trabajo utilizada debe ser la misma cuenta que se usó para inscribir el dispositivo con <token>wit_nextref</token>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="tip">
          <para>
            <caps:sentence sentenceid="63332401048a73fcfc9fee6524330896" id="tgt25" class="tgtSentence">Si usa <token>wit_nextref</token> con <token>cmshort</token>, consulte <externalLink><linkText>Cómo controlar aplicaciones mediante directivas de administración de aplicaciones móviles en Configuration Manager</linkText><linkUri>https://technet.microsoft.com/library/mt131414.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="01dd78a5ea96df651626f9a399fcc9a4" id="tgt26" class="tgtSentence">Crear e implementar una aplicación con una directiva de administración de aplicaciones móviles</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="8b83817f381a751a0c05435773d79d41" id="tgt27" class="tgtSentence">
                  <embeddedLabel>Paso 1:</embeddedLabel> obtenga el vínculo a una aplicación administrada por directivas o cree una aplicación ajustada.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="71a8f01ac5a7bc5372da0602c59b4eeb" id="tgt28" class="tgtSentence">
                  <embeddedLabel>Paso 2:</embeddedLabel> publique la aplicación en su espacio de almacenamiento en la nube.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c684d19680c912c0e0c07ffb8fa077b1" id="tgt29" class="tgtSentence">
                  <embeddedLabel>Paso 3:</embeddedLabel> cree una directiva de administración de aplicaciones móviles.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ad6254b87eda7f0a8656f7aa45910cc3" id="tgt30" class="tgtSentence">
                  <embeddedLabel>Paso 4:</embeddedLabel> implemente la aplicación seleccionando la opción para asociar la aplicación a una directiva de administración de aplicaciones móviles.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7d94ce06300f3f4650d52344b3498d67" id="tgt31" class="tgtSentence">
                  <embeddedLabel>Paso 5:</embeddedLabel> supervise la implementación de la aplicación.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="256ba1a9e9d8d062dc723fc8c317ef53" id="tgt32" class="tgtSentence">
            <embeddedLabel>Paso 1:</embeddedLabel> obtenga el vínculo a una aplicación administrada por directivas o cree una aplicación ajustada</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="118d154a2a3a37dece48f55314b52d30" id="tgt33" class="tgtSentence">
                  <ui>Para obtener un vínculo a una aplicación administrada por directiva</ui>: desde la tienda de aplicaciones, busque y anote la dirección URL de la aplicación administrada por directiva que desea implementar.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b77dceb3cdc668613ef005a89aafb9d4" id="tgt34" class="tgtSentence">Por ejemplo, la dirección URL de Microsoft Word para la aplicación de iPad es <userInput>https://itunes.apple.com/us/app/microsoft-word-for-ipad/id586447913?mt=8</userInput></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2c3420042d3e5eefbf7a7372487f9372" id="tgt35" class="tgtSentence">
                  <ui>Para crear una aplicación ajustada</ui>: use la información de los temas <link xlink:href="99ab0369-5115-4dc8-83ea-db7239b0de97">Prepare iOS apps for mobile application management with the Microsoft Intune App Wrapping Tool</link> y <link xlink:href="e9c349c8-51ae-4d73-b74a-6173728a520b">Prepare Android apps for mobile application management with the Microsoft Intune App Wrapping Tool</link> para crear una aplicación ajustada.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="39b4937cfb9ecb55e93e878fa20ee16c" id="tgt36" class="tgtSentence">La herramienta crea una aplicación procesada que se usará al publicar la aplicación en su espacio de almacenamiento en nube.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="8bdda4283aafab26ec0ce4595089732e" id="tgt37" class="tgtSentence">
            <embeddedLabel>Paso 2:</embeddedLabel> publique la aplicación en su espacio de almacenamiento en la nube</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="383a8ff798129aa5704ec11e97ca591c" id="tgt38" class="tgtSentence">Cuando se publica una aplicación administrada, los procedimientos difieren en función de si se publica una aplicación administrada por directiva o una aplicación que se procesó mediante la Microsoft Intune App Wrapping Tool para iOS.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="d2aec74263987077fa41a29299cc8d24" id="tgt39" class="tgtSentence">Para publicar una aplicación administrada por directiva</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="0fb99a7d8b3347d9997d6cdb8c04d289" id="tgt40" class="tgtSentence">Cuando esté listo para cargar la aplicación en su espacio de almacenamiento en nube, siga las instrucciones de <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a#BKMK_PublishSoftware">Publish mobile device software to Microsoft Intune cloud storage</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ac8b349f34a74f1bc04d3dc88cd02abc" id="tgt41" class="tgtSentence">En el caso de aplicaciones iOS, seleccione <ui>Aplicación iOS administrada de la tienda de aplicaciones</ui> en <ui>Seleccione cómo debe ponerse a disposición de los dispositivos este software</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="7c9bff9cd45936ce7944e0d68652e177" id="tgt42" class="tgtSentence">En el caso de aplicaciones Android, seleccione <ui>Vínculo externo</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt43" class="tgtSentence">En <ui>Especificar la dirección URL</ui>, escriba la dirección URL a la aplicación administrada por directiva que anotó anteriormente.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="2a004991b9fc096d461e86f49a7117db" id="tgt44" class="tgtSentence">Una vez finalizada la carga, verá <ui>Sí</ui> en <ui>Directivas de administración de aplicaciones</ui> en la página <ui>Propiedades del software</ui> de la aplicación cargada.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="da4b004a83f15f8aaaaa2c92480639de" id="tgt45" class="tgtSentence">Una vez que haya comprobado que la aplicación se carga correctamente, continúe con el paso 3.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="c0943ca0db71b5d93a41813c5a922a78" id="tgt46" class="tgtSentence">Para publicar una aplicación procesada con la herramienta de ajuste de aplicaciones de Microsoft Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="0fb99a7d8b3347d9997d6cdb8c04d289" id="tgt47" class="tgtSentence">Cuando esté listo para cargar la aplicación en su espacio de almacenamiento en nube, siga las instrucciones de <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a#BKMK_PublishSoftware">Publish mobile device software to Microsoft Intune cloud storage</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt48" class="tgtSentence">Seleccione <ui>Software Installer</ui> en <ui>Seleccione cómo debe ponerse a disposición de los dispositivos este software</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt49" class="tgtSentence">Seleccione <ui>Paquete de aplicación de iOS (archivo *.ipa)</ui> en <ui>Tipo de archivo instalador de software</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="2a004991b9fc096d461e86f49a7117db" id="tgt50" class="tgtSentence">Una vez finalizada la carga, verá <ui>Sí</ui> en <ui>Directivas de administración de aplicaciones</ui> en la página <ui>Propiedades del software</ui> de la aplicación cargada.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="da4b004a83f15f8aaaaa2c92480639de" id="tgt51" class="tgtSentence">Una vez que haya comprobado que la aplicación se carga correctamente, continúe con el paso 3.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="bkmk_step3">
        <title>
          <caps:sentence sentenceid="8ed07845e994f2dd439d3a0ab5bfc0fa" id="tgt52" class="tgtSentence">
            <embeddedLabel>Paso 3:</embeddedLabel> cree una directiva de administración de aplicaciones móviles</caps:sentence>
        </title>
        <content>
          <procedure expanded="true">
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt53" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Información general</ui> &gt; <ui>Agregar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="8eaf71f1ef02bb38cf0cab39f6526555" id="tgt54" class="tgtSentence">Configure e implemente uno de las siguientes directivas de <ui>Software</ui> en función del tipo de dispositivo para el que desea configurar aplicaciones:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4bdca24c3d5cc6725c747803ab1bfafd" id="tgt55" class="tgtSentence">Directiva de administración de aplicaciones móviles (Android 4 y posterior)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="29d1eede8b13830fbbd64655c4666e73" id="tgt56" class="tgtSentence">Directiva de administración de aplicaciones móviles (iOS 7 y posterior)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="3c869780bc51137bac60f02d372c756a" id="tgt57" class="tgtSentence">Puede usar la configuración recomendada o personalizar la configuración.</caps:sentence>
                    <caps:sentence sentenceid="363ddf43df695c296401df2564573a36" id="tgt58" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="c0d0cbbd73b2b5491c34a53d2b509e5f" id="tgt59" class="tgtSentence">Configure los siguientes valores según sea necesario.</caps:sentence>
                    <caps:sentence sentenceid="82075b9391a52f968a402fb9c968ebdf" id="tgt60" class="tgtSentence"> Las opciones pueden diferir en función del tipo de dispositivo para el que va a configurar la directiva.</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt61" class="tgtSentence">Valor</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt62" class="tgtSentence">Más información</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt63" class="tgtSentence">Nombre</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4a5cb5174e3496c8fc4a0138e6f19137" id="tgt64" class="tgtSentence">Especifique un nombre para esta directiva.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt65" class="tgtSentence">Descripción</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e6d5e1f85c07fcfee99e5c6b971f1f50" id="tgt66" class="tgtSentence">Si lo desea, especifique una descripción para esta directiva.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="e1cc9c0bafb9b6cc967379e7b33a7078" id="tgt67" class="tgtSentence">Restringir contenido web para mostrar en un explorador administrado corporativo</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="932fb3117a2c0f8e1018a9d64d7c3eeb" id="tgt68" class="tgtSentence">Cuando se habilita esta configuración, los vínculos en la aplicación se abrirán en el explorador administrado.</caps:sentence>
                            <caps:sentence sentenceid="2268536abba7d48508d53ad2937053e7" id="tgt69" class="tgtSentence"> Debe haber implementado esta aplicación en dispositivos para que esta opción funcione.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8e0c4e984dbb4b30a86c232b15df8490" id="tgt70" class="tgtSentence">
                              <ui>Impedir copias de seguridad de Android</ui> o <ui>Impedir copias de seguridad de iTunes e iCloud</ui></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="1d4cbe99e1ce2eb94c4cae0a5efec52b" id="tgt71" class="tgtSentence">Deshabilita la copia de seguridad de cualquier información procedente de la aplicación.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="a8ae1f1bd61e5f48fc9441fd79973926" id="tgt72" class="tgtSentence">Permitir que la aplicación transfiera datos a otras aplicaciones</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8cce1e95e8dee823386c1ac1793ccc5c" id="tgt73" class="tgtSentence">Especifica las aplicaciones a las que esta aplicación puede enviar datos.</caps:sentence>
                            <caps:sentence sentenceid="6964201e69fd925200079fef787f5eb1" id="tgt74" class="tgtSentence"> Puede elegir no permitir la transferencia de datos a ninguna aplicación, permitir solo la transferencia a otras aplicaciones administradas o permitir la transferencia a cualquier aplicación.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="65ab00437851b55ca87ddc27d4e58c78" id="tgt75" class="tgtSentence">Por ejemplo, cuando no se permite la transferencia de datos, restringir la transferencia de datos a servicios, como mensajería SMS, asignar imágenes a los contactos y exponer en Facebook o Twitter.</caps:sentence>
                          </para>
                          <alert class="important">
                            <para>
                              <caps:sentence sentenceid="56a03d0745e780caf58f99b06f8dc6a8" id="tgt76" class="tgtSentence">Esta configuración no controla el uso de la característica <ui>Abrir en</ui> en dispositivos móviles.</caps:sentence>
                            </para>
                          </alert>
                          <para>
                            <caps:sentence sentenceid="fb77d96cc530e283baf49e328d58a55d" id="tgt77" class="tgtSentence">Para dispositivos iOS, para evitar la transferencia de documentos entre aplicaciones administradas y no administradas, debe también configurar e implementar una directiva de seguridad de dispositivos móviles que deshabilite la configuración <ui>Permitir documentos administrados en otras aplicaciones no administradas</ui>.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="b2699cfa6a1f91460593193ef6605faa" id="tgt78" class="tgtSentence">Si selecciona permitir solo la transferencia a otras aplicaciones administradas, se usarán los visores Image Viewer y PDF Viewer de Intune (si se implementaron) para abrir el contenido de los tipos respectivos.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="86ada3673da1a7d159622f63fb395346" id="tgt79" class="tgtSentence">Permitir que la aplicación reciba datos de otras aplicaciones</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5923ab78e0f1a7e67e1aeb4e119e2982" id="tgt80" class="tgtSentence">Especifica las aplicaciones de las que esta aplicación puede recibir datos.</caps:sentence>
                            <caps:sentence sentenceid="1b9dc4fc8fa80a28adcb544f0cd796a2" id="tgt81" class="tgtSentence"> Puede:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="23337f164e580e96bd4b3b406bd0ac1a" id="tgt82" class="tgtSentence">no permitir la transferencia de datos desde ninguna aplicación</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="5455260a4e41f085880f05b652673c5f" id="tgt83" class="tgtSentence">permitir solo la transferencia desde otras aplicaciones administradas</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="939bf10f28b65eea13366f78058d494a" id="tgt84" class="tgtSentence">permitir la transferencia desde cualquier aplicación</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="4803abebb29d0edf2dbbcd8190951d21" id="tgt85" class="tgtSentence">Impedir "Guardar como..."</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="cfb16dc9469292b1d199ef32f3a7ff32" id="tgt86" class="tgtSentence">Deshabilita el uso de la opción <ui>Guardar como</ui> para guardar los datos en ubicaciones de almacenamiento personales en la nube (por ejemplo, el OneDrive Personal o Dropbox) en cualquier aplicación que use esta directiva.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="8c59cf3d5b55b1e23747261d128338db" id="tgt87" class="tgtSentence">Restringir cortar, copiar y pegar con otras aplicaciones</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="11fd0dfe65241e42e62329c9370a4fe7" id="tgt88" class="tgtSentence">Especifica cómo pueden usarse las operaciones de cortar, copiar y pegar con la aplicación.</caps:sentence>
                            <caps:sentence sentenceid="a286929ca0f740e14eb1d567ac54d6cb" id="tgt89" class="tgtSentence"> Elija de entre las siguientes opciones:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f00af2216501a42246dd2da6db59ade0" id="tgt90" class="tgtSentence">
                                  <ui>Bloqueada</ui> : no permitir operaciones de cortar, copiar y pegar entre esta aplicación y otras aplicaciones.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="8a16a83785e80f4538accc98bd870d53" id="tgt91" class="tgtSentence">
                                  <ui>Aplicaciones administradas por directiva</ui>: permitir solo operaciones de cortar, copiar y pegar entre esta aplicación y otras aplicaciones administradas.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="2dea3a1e00753f3dc69c37db8df610be" id="tgt92" class="tgtSentence">
                                  <ui>Aplicaciones administradas por directiva con Pegar en</ui>: permitir que los datos cortados o copiados desde esta aplicación solo se peguen en otras aplicaciones administradas.</caps:sentence>
                                <caps:sentence sentenceid="cfb6e3a7515b6f3393a8f5c55e8a8cd4" id="tgt93" class="tgtSentence"> Permitir que los datos cortados o copiados desde cualquier aplicación se peguen en esta aplicación.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="fbcd2fc58488e44f5ee010e4e6c4ca5c" id="tgt94" class="tgtSentence">
                                  <ui>Cualquier aplicación</ui>: sin restricciones para las operaciones de cortar, copiar y pegar en esta aplicación o desde ella.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="ba784ec1f4c3eb8e78a874ddae16c8bd" id="tgt95" class="tgtSentence">Para copiar y pegar datos entre las aplicaciones administradas, ambas aplicaciones deben tener las opciones <ui>Aplicaciones administradas por directiva</ui> o <ui>Aplicaciones administradas por directiva con Pegar en</ui> configuradas.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="97223c666a42b440fbdde94f734607bc" id="tgt96" class="tgtSentence">Requerir PIN simple en acceso</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5085d4a6ecf8e8d05f1dc62202a68038" id="tgt97" class="tgtSentence">Requiere que el usuario escriba un número PIN que especifica al usar esta aplicación.</caps:sentence>
                            <caps:sentence sentenceid="35fa889be7a7d7c3f8ba1d7af678479b" id="tgt98" class="tgtSentence"> Se pedirá al usuario que lo configure la primera vez que ejecuta la aplicación.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="030e626c46b34f7e438dced595189d26" id="tgt99" class="tgtSentence">Número de intentos antes de restablecimiento del PIN</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8e7077d5a48ccc1a69423d33c9bd9008" id="tgt100" class="tgtSentence">Especifique el número de intentos de entrada de PIN que pueden realizarse antes de que el usuario deba restablecer el PIN.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="c9408bb8c88b117b1853eec0e4d66483" id="tgt101" class="tgtSentence">Requerir credenciales corporativas en acceso</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="818f1a0ce61274bb2271da7a03cf4f3d" id="tgt102" class="tgtSentence">Requiere que el usuario deba introducir su información de inicio de sesión corporativa para tener acceso a la aplicación.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="1c0faa87b71665da0126f6d6fe3c4105" id="tgt103" class="tgtSentence">Requerir cumplimiento de dispositivos con la directiva corporativa en acceso</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7ae3dd3de4072da042612952a8ae3854" id="tgt104" class="tgtSentence">Solo permite que se use la aplicación cuando el dispositivo no está liberado ni modificado.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="68a914c6d98b1a095cf97b94ba241940" id="tgt105" class="tgtSentence">Volver a comprobar los requisitos de acceso después de (minutos)</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt106" class="tgtSentence">En el campo <ui>Tiempo de espera</ui>, especifique el período de tiempo que debe transcurrir antes de que se vuelvan a comprobar los requisitos de acceso de la aplicación una vez iniciada la aplicación.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="c4825a0f34039ec334b098361d07cea8" id="tgt107" class="tgtSentence">Período de gracia sin conexión</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b93b129da32fffec3d14fb594a0c1324" id="tgt108" class="tgtSentence">Si el dispositivo está desconectado, especifique el período de tiempo que debe transcurrir antes de que se vuelvan a comprobar los requisitos de acceso de la aplicación.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="f5e139f8cfe1079ec7c87ed1b44c4b94" id="tgt109" class="tgtSentence">Cifrar datos de aplicación</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c8555c9122fde42c2f073065b3a0a788" id="tgt110" class="tgtSentence">Especifica que se cifren todos los datos asociados a esta aplicación, incluidos los datos almacenados externamente como, por ejemplo, tarjetas SD.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <embeddedLabel>
                                <caps:sentence sentenceid="45539cc2e2d0a567722ba54a2dee1b9f" id="tgt111" class="tgtSentence">Cifrado para iOS</caps:sentence>
                              </embeddedLabel>
                            </para>
                            <para>
                              <caps:sentence sentenceid="de0cb4d5b8f91bf32d39c330bf20cbc3" id="tgt112" class="tgtSentence">En el caso de aplicaciones que están asociadas a una directiva de administración de aplicaciones móviles de <token>wit_nextref</token>, los datos se cifran en reposo con el cifrado de nivel de dispositivo proporcionado por el sistema operativo.</caps:sentence>
                              <caps:sentence sentenceid="e8efe3c8ecd4d81f44ba3134f41a2019" id="tgt113" class="tgtSentence"> Esta opción se habilita a través de la directiva de PIN del dispositivo que debe establecer el administrador de TI.</caps:sentence>
                              <caps:sentence sentenceid="44a07f10798dd73b138b8f18bdb4a235" id="tgt114" class="tgtSentence"> Cuando se requiere un PIN, los datos se cifrarán según la configuración de la directiva de administración de aplicaciones móviles.</caps:sentence>
                              <caps:sentence sentenceid="416089df8cbbc6ca579368f9c4a4c782" id="tgt115" class="tgtSentence"> Como se indica en la documentación de Apple, <externalLink><linkText>los módulos usados por iOS 7 están certificados mediante FIPS 140-2</linkText><linkUri>http://support.apple.com/en-us/HT202739</linkUri></externalLink>.</caps:sentence>   </para>
                            <para>
                              <embeddedLabel>
                                <caps:sentence sentenceid="c976167b93bc1fae8825834392acf475" id="tgt116" class="tgtSentence">Cifrado para Android</caps:sentence>
                              </embeddedLabel>
                            </para>
                            <para>
                              <caps:sentence sentenceid="de0cb4d5b8f91bf32d39c330bf20cbc3" id="tgt117" class="tgtSentence">En el caso de aplicaciones que están asociadas a una directiva de administración de aplicaciones móviles de <token>wit_nextref</token>, Microsoft proporciona el cifrado.</caps:sentence>
                              <caps:sentence sentenceid="5c6559d28ab56dc55367ab8371495b0d" id="tgt118" class="tgtSentence"> Los datos se cifran de forma sincrónica durante las operaciones de E/S de archivos según la configuración de la directiva de administración de aplicaciones móviles.</caps:sentence>
                              <caps:sentence sentenceid="29df971fe087694402e5c5d4225d3e8b" id="tgt119" class="tgtSentence"> Las aplicaciones administradas en Android usan el cifrado AES-128 en modo CBC mediante las bibliotecas de criptografía de la plataforma.</caps:sentence>
                              <caps:sentence sentenceid="0531d2181826136e20f1181ff5ce22dd" id="tgt120" class="tgtSentence"> El método de cifrado no está certificado mediante FIPS 140-2.</caps:sentence>
                              <caps:sentence sentenceid="ad3f047b337803f913e4cf712a30facc" id="tgt121" class="tgtSentence"> Siempre se cifrará el contenido del almacenamiento del dispositivo.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4ca64536087ea6beae272c65ad3161e8" id="tgt122" class="tgtSentence">
                              <ui>Bloquear captura de pantalla</ui> (solo en dispositivos Android)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2492f38569f9d5c456eaad980dc84c1c" id="tgt123" class="tgtSentence">Especifica que las funciones de captura de pantalla del dispositivo se bloquean cuando se usa esta aplicación.</caps:sentence>
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
                    <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt124" class="tgtSentence">Cuando haya terminado haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt125" class="tgtSentence">La nueva directiva se muestra en el nodo <ui>Directivas de configuración</ui> del área de trabajo <ui>Directiva</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="535a3a5afb1dffeac6df53599203a4e9" id="tgt126" class="tgtSentence">
            <embeddedLabel>Paso 4:</embeddedLabel> asocie la aplicación a una directiva de administración de aplicaciones móviles e implemente la aplicación.</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="72d7c0450a46596eeae4cf1ac7cd7fe4" id="tgt127" class="tgtSentence">Implemente la aplicación, asegurándose de seleccionar la directiva de administración de aplicaciones móviles de la página <ui>Administración de aplicaciones móviles</ui> para asociar la directiva a la aplicación.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3d7d30605a309123a172bc57a6d96f71" id="tgt128" class="tgtSentence">Para obtener más información, consulte <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy software to mobile devices in Windows Intune</link>.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="bbbb994a6ac01feff806f646938d1b7f" id="tgt129" class="tgtSentence">En el caso de dispositivos que ejecutan sistemas operativos anteriores a iOS 7.1, las directivas asociadas no se quitarán al desinstalar la aplicación.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="42164345301d1549f9395e6112e5db61" id="tgt130" class="tgtSentence">Si se anula la inscripción del dispositivo en <token>wit_nextref</token>, no se eliminan las directivas de las aplicaciones; las aplicaciones que tenían aplicadas directivas conservarán la configuración de las directivas aunque la aplicación se desinstale y se vuelva a instalar.</caps:sentence>
            </para>
          </alert>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="13d95cc79df018c62db18d13cd558b45" id="tgt131" class="tgtSentence">Qué hacer cuando ya se ha implementado una aplicación en dispositivos</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="8f7cfe99fbf829b9a5b4f896b54f4952" id="tgt132" class="tgtSentence">Puede haber situaciones en que implemente una aplicación y uno de los usuarios o dispositivos de destino ya tenga una versión no administrada de la aplicación instalada, por ejemplo, si el usuario ha instalado Microsoft Word desde la tienda de aplicaciones.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="f4c90effb0428cce17f66601102b2f24" id="tgt133" class="tgtSentence">En este caso, debe pedir al usuario que desinstale manualmente la versión no administrada para que se pueda instalar la versión administrada que se ha configurado.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e536d54304665510ef8b284a70a140f7" id="tgt134" class="tgtSentence">Sin embargo, para los dispositivos que ejecutan iOS 9 y versiones posteriores, <token>wit_nextref</token> pedirá automáticamente al usuario permiso para ocuparse de la administración de la aplicación existente.</caps:sentence>
                <caps:sentence sentenceid="3528bfc10c1d1b48a8fe1720a3272d3a" id="tgt135" class="tgtSentence"> Si acepta, <token>wit_nextref</token> administrará la aplicación y también se aplicarán las directivas de administración de aplicaciones móviles asociadas con la aplicación.</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence sentenceid="4943bd01da173db15ef49acff1cce576" id="tgt136" class="tgtSentence">Si el dispositivo está en modo de supervisión, <token>wit_nextref</token> se ocupará de la administración de la aplicación existente sin pedir permiso a los usuarios.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="7d94ce06300f3f4650d52344b3498d67" id="tgt137" class="tgtSentence">
            <embeddedLabel>Paso 5:</embeddedLabel> supervise la implementación de la aplicación.</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9ec1d2dd2cb41f40ceb9917fd14627f5" id="tgt138" class="tgtSentence">Cuando haya creado e implementado una aplicación asociada a una directiva de administración de aplicaciones móviles, use los procedimientos siguientes para supervisar la aplicación y resuelva los conflictos de directivas.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="6c36038bf1f6ed420e06bc9bbcb625ee" id="tgt139" class="tgtSentence">Para ver el estado de la implementación</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt140" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Grupos</ui> &gt; <ui>Información general</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="074e341bb965d9786b85b2fda05c0f8f" id="tgt141" class="tgtSentence">Realice uno de los siguientes pasos:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt142" class="tgtSentence">Haga clic en <ui>Todos los usuarios</ui> y luego haga doble clic en el usuario cuyos dispositivos desea examinar.</caps:sentence>
                        <caps:sentence sentenceid="a0d64bf59fd2765c4ef3aaf9a36c078b" id="tgt143" class="tgtSentence"> En la página <ui>Propiedades del usuario</ui>, haga clic en <ui>Dispositivos</ui> y luego haga doble clic en el dispositivo que desea examinar.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt144" class="tgtSentence">Haga clic en <ui>Todos los dispositivos</ui> &gt; <ui>Todos los dispositivos móviles</ui>.</caps:sentence>
                        <caps:sentence sentenceid="94898649863bca08a3420d208bbe0015" id="tgt145" class="tgtSentence"> En la página <ui>Propiedades del grupo de dispositivos</ui>, haga clic en <ui>Dispositivos</ui> y luego haga doble clic en el dispositivo que desea examinar.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1d78457e80b3c77f152c8c399312bb34" id="tgt146" class="tgtSentence">En la página <ui>Propiedades del dispositivo móvil</ui>, haga clic en <ui>Directiva</ui> para ver una lista de las directivas de administración de aplicaciones móviles que se hayan implementado en el dispositivo.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="720e8e2741d6dd62537ba2df46c1d5a0" id="tgt147" class="tgtSentence">Seleccione la directiva de administración de aplicaciones móviles cuyo estado desea ver.</caps:sentence>
                    <caps:sentence sentenceid="649e2a567bc706763f35a4d0a7a82cca" id="tgt148" class="tgtSentence"> Puede ver los detalles de la directiva en el panel inferior y expandir el nodo para mostrar su configuración.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="2c6631d2c4c7f36c474591432c5fdad0" id="tgt149" class="tgtSentence">En la columna <ui>Estado</ui> de cada una de las directivas de administración de aplicaciones móviles, se mostrará <ui>Cumple</ui>, <ui>Cumplimiento (pendiente)</ui> o <ui>Error</ui>.</caps:sentence>
                    <caps:sentence sentenceid="70292eb7772465b924271ff892654834" id="tgt150" class="tgtSentence"> Si la directiva seleccionada tiene una o más configuraciones en conflicto, se mostrará <ui>Error</ui> en este campo.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="894b30c8cf01b5579c5e331ad53c15e8" id="tgt151" class="tgtSentence">Cuando haya identificado un conflicto, puede modificar las configuraciones de directivas en conflicto para que usen la misma configuración o implementar una sola directiva para la aplicación y el usuario.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section expanded="false" address="BKMK_Conf">
            <title>
              <caps:sentence sentenceid="b401d82e008ad25352e9fdd1d7bc847a" id="tgt152" class="tgtSentence">Cómo se resuelven los conflictos de directivas</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="6830d5fcdd032531ad98dc24f0d82444" id="tgt153" class="tgtSentence">Cuando hay un conflicto de directivas de administración de aplicaciones móviles en la primera implementación para el usuario o el dispositivo, el valor específico de la configuración en conflicto se quitará de la directiva implementada en la aplicación y la aplicación usará un valor de conflicto integrado.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="ff113ea52ad2b586f1d2ee13f1831ae8" id="tgt154" class="tgtSentence">Cuando hay un conflicto de directivas de administración de aplicaciones móviles en implementaciones posteriores para la aplicación o el usuario, el valor específico de la configuración en conflicto no se actualizará en la directiva de administración de aplicaciones móviles implementada para la aplicación y la aplicación usará el valor existente para dicha configuración.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="2956fcfb8fe47c9ee28637b98c948dd4" id="tgt155" class="tgtSentence">En casos en los que el dispositivo o el usuario recibe dos directivas en conflicto, se aplica el comportamiento siguiente:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3b12ca255a9dc04997bfd4e0517af640" id="tgt156" class="tgtSentence">Si ya se implementó una directiva para el dispositivo, la configuración de directiva existente no se sobrescribe.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="37af9c684bb5a2948342377324e0b837" id="tgt157" class="tgtSentence">Si todavía no se implementó ninguna directiva para el dispositivo y se implementan dos configuraciones en conflicto, se usa la configuración predeterminada integrada en el dispositivo.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="71e0cbf3-2bfb-412e-8a12-8503df08b4cf">Protect company resources with Microsoft Intune</link>
        <link xlink:href="5b49d81d-8a28-4d78-a21b-6614920a7b82">Provision and configure apps with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Mobile application management policies in <token>wit_firstref</token> let you modify the functionality of apps that you deploy to help bring them into line with your company compliance and security policies.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For example, you can restrict cut, copy and paste operations within a managed app, or configure an app to open all web links inside a managed browser.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">Mobile application management policies support:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">Devices that run Android 4 and later.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Devices that run iOS 7 and later.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src6" class="srcSentence">Unlike other <token>wit_nextref</token> policies, you do not deploy a mobile application management policy directly.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> Instead, you associate the policy with the app that you want to restrict.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> When the app is deployed and installed on devices, the settings you specify will take effect.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">To apply restrictions to an app, the app must incorporate the <token>wit_firstref</token> App Software Development Kit (SDK).</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> There are two methods of obtaining this type of app:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">
                <ui>Use a policy managed app</ui> – Has the App SDK built-in.</caps:sentence>
              <caps:sentence id="src12" class="srcSentence"> To add this type of app, you specify a link to the app from an app store such as the iTunes store or Google Play.</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> No further processing is required for this type of app.</caps:sentence>
              <caps:sentence id="src14" class="srcSentence"> See a list of <link xlink:href="49023822-0aa7-4508-8119-3be8976d21d1">Managed apps for Microsoft Intune mobile application management policies</link>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">
                <ui>Use a ‘wrapped’ app</ui> - Apps that are repackaged to include the App SDK by using the <ui>Microsoft Intune App Wrapping Tool</ui>.</caps:sentence>
              <caps:sentence id="src16" class="srcSentence"> This tool is typically used to process company apps that were created in-house.</caps:sentence>
              <caps:sentence id="src17" class="srcSentence"> It cannot be used to process apps that were downloaded from the app store.</caps:sentence>
              <caps:sentence id="src18" class="srcSentence"> See <link xlink:href="99ab0369-5115-4dc8-83ea-db7239b0de97">Prepare iOS apps for mobile application management with the Microsoft Intune App Wrapping Tool</link> and <link xlink:href="e9c349c8-51ae-4d73-b74a-6173728a520b">Prepare Android apps for mobile application management with the Microsoft Intune App Wrapping Tool</link>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src19" class="srcSentence">Some managed apps, like the Outlook app for iOS and Android support <ui>multi-identity</ui>.</caps:sentence>
          <caps:sentence id="src20" class="srcSentence"> This means that <token>wit_nextref</token> only applies management settings to corporate accounts or data in the app.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src21" class="srcSentence">For example, using the Outlook app:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src22" class="srcSentence">	If the user configures a corporate, and a personal email account, <token>wit_nextref</token> only applies management settings to the corporate account and does not manage the personal account.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src23" class="srcSentence">	If the device is retired, or unenrolled, only the corporate Outlook data is removed from the device.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src24" class="srcSentence">The corporate account used must be the same account that was used to enroll the device with <token>wit_nextref</token>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <alert class="tip">
          <para>
            <caps:sentence id="src25" class="srcSentence">If you are using <token>wit_nextref</token> with <token>cmshort</token>, see <externalLink><linkText>How to Control Apps Using Mobile Application Management Policies in Configuration Manager</linkText><linkUri>https://technet.microsoft.com/library/mt131414.aspx</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src26" class="srcSentence">Create and deploy an app with a mobile application management policy</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src27" class="srcSentence">
                  <embeddedLabel>Step 1:</embeddedLabel> Get the link to a policy managed app, or create a wrapped app.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src28" class="srcSentence">
                  <embeddedLabel>Step 2:</embeddedLabel> Publish the app to your cloud storage space.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src29" class="srcSentence">
                  <embeddedLabel>Step 3:</embeddedLabel> Create a mobile application management policy.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src30" class="srcSentence">
                  <embeddedLabel>Step 4:</embeddedLabel> Deploy the app, selecting the option to associate the app with a mobile application management policy.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src31" class="srcSentence">
                  <embeddedLabel>Step 5:</embeddedLabel> Monitor the app deployment.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src32" class="srcSentence">
            <embeddedLabel>Step 1:</embeddedLabel> Obtain the link to a policy managed app, or create a wrapped app</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src33" class="srcSentence">
                  <ui>To obtain a link to a policy managed app</ui> - From the app store, find, and note the URL of the policy managed app you want to deploy.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src34" class="srcSentence">For example, the URL of the Microsoft Word for iPad app is <userInput>https://itunes.apple.com/us/app/microsoft-word-for-ipad/id586447913?mt=8</userInput></caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src35" class="srcSentence">
                  <ui>To create a wrapped app</ui> - Use the information in the topics <link xlink:href="99ab0369-5115-4dc8-83ea-db7239b0de97">Prepare iOS apps for mobile application management with the Microsoft Intune App Wrapping Tool</link> and <link xlink:href="e9c349c8-51ae-4d73-b74a-6173728a520b">Prepare Android apps for mobile application management with the Microsoft Intune App Wrapping Tool</link> to create a wrapped app.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src36" class="srcSentence">The tool creates a processed app that you will use when you publish the app to your cloud storage space.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src37" class="srcSentence">
            <embeddedLabel>Step 2:</embeddedLabel> Publish the app to your cloud storage space</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src38" class="srcSentence">When you publish a managed app, the procedures differ depending on whether you are publishing a policy managed app, or an app that was processed using the Microsoft Intune App Wrapping Tool for iOS.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src39" class="srcSentence">To publish a policy managed app</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">When you are ready to upload the app to your cloud storage space, follow the instructions in <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a#BKMK_PublishSoftware">Publish mobile device software to Microsoft Intune cloud storage</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">For iOS apps, select <ui>Managed iOS App from the App Store</ui>, under <ui>Select how this software is made available to devices</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">For Android apps, select <ui>External link</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Under <ui>Specify the URL</ui>, enter the URL to the policy managed app that you noted earlier.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src44" class="srcSentence">After the upload completes, you will see <ui>Yes</ui> for <ui>App Management Policies</ui> on the <ui>Software Properties</ui> page for the uploaded app.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src45" class="srcSentence">Once you have verified that the app is uploaded successfully, continue to Step 3.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src46" class="srcSentence">To publish an app that was processed using the Microsoft Intune App Wrapping Tool</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">When you are ready to upload the app to your cloud storage space, follow the instructions in <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a#BKMK_PublishSoftware">Publish mobile device software to Microsoft Intune cloud storage</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Select <ui>Software Installer</ui>, under <ui>Select how this software is made available to devices</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">Select <ui>App package for iOS (*.ipa file)</ui> under <ui>Software installer file type</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src50" class="srcSentence">After the upload completes, you will see <ui>Yes</ui> for <ui>App Management Policies</ui> on the <ui>Software Properties</ui> page for the uploaded app.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src51" class="srcSentence">Once you have verified that the app is uploaded successfully, continue to Step 3.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="bkmk_step3">
        <title>
          <caps:sentence id="src52" class="srcSentence">
            <embeddedLabel>Step 3:</embeddedLabel> Create a mobile application management policy</caps:sentence>
        </title>
        <content>
          <procedure expanded="true">
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Overview</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Configure and deploy one of the following <ui>Software</ui> policies, depending on the device type you want to configure apps for:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src55" class="srcSentence">Mobile Application Management Policy (Android 4 and later)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src56" class="srcSentence">Mobile Application Management Policy (iOS 7 and later)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">You can use recommended settings or customize the settings.</caps:sentence>
                    <caps:sentence id="src58" class="srcSentence"> For details, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Configure the following values as required.</caps:sentence>
                    <caps:sentence id="src60" class="srcSentence"> The options might differ depending on the device type for which you are configuring the policy.</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src61" class="srcSentence">Value</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src62" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src63" class="srcSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src64" class="srcSentence">Specify a name for this policy.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src65" class="srcSentence">Description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src66" class="srcSentence">Optionally, specify a description for this policy.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src67" class="srcSentence">Restrict web content to display in a corporate managed browser</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src68" class="srcSentence">When this setting is enabled, any links in the app will be opened in the Managed Browser.</caps:sentence>
                            <caps:sentence id="src69" class="srcSentence"> You must have deployed this app to devices in order for this option to work.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src70" class="srcSentence">
                              <ui>Prevent Android backups</ui> or <ui>Prevent iTunes and iCloud backups</ui></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src71" class="srcSentence">Disables the backup of any information from the app.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src72" class="srcSentence">Allow app to transfer data to other apps</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src73" class="srcSentence">Specifies the apps that this app can send data to.</caps:sentence>
                            <caps:sentence id="src74" class="srcSentence"> You can choose to not allow data transfer to any app, only allow transfer to other managed apps, or to allow transfer to any app.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src75" class="srcSentence">For example, when you do not allow data transfer, you restrict data transfer to services like SMS messaging, assigning images to contacts, and posting to Facebook or Twitter.</caps:sentence>
                          </para>
                          <alert class="important">
                            <para>
                              <caps:sentence id="src76" class="srcSentence">This setting does not control use of the <ui>Open In</ui> feature on mobile devices.</caps:sentence>
                            </para>
                          </alert>
                          <para>
                            <caps:sentence id="src77" class="srcSentence">For iOS devices, to prevent document transfer between managed and unmanaged apps, you must also configure and deploy a mobile device security policy that disables the setting <ui>Allow managed documents in other unmanaged apps</ui>.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src78" class="srcSentence">If you select to only allow transfer to other managed apps, the Intune PDF and image viewers (if deployed) will be used to open content of the respective types.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src79" class="srcSentence">Allow app to receive data from other apps</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src80" class="srcSentence">Specifies the apps that this app can receive data from.</caps:sentence>
                            <caps:sentence id="src81" class="srcSentence"> You can choose to:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src82" class="srcSentence">not allow data transfer from any app</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src83" class="srcSentence">only allow transfer from other managed apps</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src84" class="srcSentence">allow transfer from any app</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src85" class="srcSentence">Prevent “Save As”</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src86" class="srcSentence">Disables use of the <ui>Save As</ui> option to save data to personal cloud storage locations (such as OneDrive Personal or Dropbox) in any app that uses this policy.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src87" class="srcSentence">Restrict cut, copy and paste with other apps</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src88" class="srcSentence">Specifies how cut, copy, and paste operations can be used with the app.</caps:sentence>
                            <caps:sentence id="src89" class="srcSentence"> Choose from:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src90" class="srcSentence">
                                  <ui>Blocked</ui> – Do not allow cut, copy, and paste operations between this app and other apps.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src91" class="srcSentence">
                                  <ui>Policy Managed Apps</ui> – Only allow cut, copy, and paste operations between this app and other managed apps.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src92" class="srcSentence">
                                  <ui>Policy Managed Apps with Paste In</ui> – Allow data cut or copied from this app only to be pasted into other managed apps.</caps:sentence>
                                <caps:sentence id="src93" class="srcSentence"> Allow data cut or copied from any app to be pasted into this app.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src94" class="srcSentence">
                                  <ui>Any App</ui> – No restrictions to cut, copy, and paste operations to, or from this app.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src95" class="srcSentence">To copy and paste data between managed apps, both apps must have either the <ui>Policy Managed Apps</ui> or <ui>Policy Managed Apps with Paste In</ui> settings configured.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src96" class="srcSentence">Require simple PIN for access</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src97" class="srcSentence">Requires the user to enter a PIN number which they specify to use this app.</caps:sentence>
                            <caps:sentence id="src98" class="srcSentence"> The user will be asked to set this up the first time they run the app.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src99" class="srcSentence">Number of attempts before PIN reset</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src100" class="srcSentence">Specify the number of PIN entry attempts which can be made before the user must reset the PIN.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src101" class="srcSentence">Require corporate credentials for access</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src102" class="srcSentence">Requires that the user must enter their corporate logon information before they can access the app.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src103" class="srcSentence">Require device compliance with corporate policy for access</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src104" class="srcSentence">Only allows the app to be used when the device is not jailbroken or rooted.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src105" class="srcSentence">Recheck the access requirements after (minutes)</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src106" class="srcSentence">In the <ui>Timeout</ui> field, specify the time period before the access requirements for the app are rechecked after the app is launched.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src107" class="srcSentence">Offline grace period</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src108" class="srcSentence">If the device is offline, specify the time period before the access requirements for the app are rechecked.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src109" class="srcSentence">Encrypt app data</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src110" class="srcSentence">Specifies that all data associated with this app will be encrypted, including data stored externally, such as SD cards.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <embeddedLabel>
                                <caps:sentence id="src111" class="srcSentence">Encryption for iOS</caps:sentence>
                              </embeddedLabel>
                            </para>
                            <para>
                              <caps:sentence id="src112" class="srcSentence">For apps that are associated with an <token>wit_nextref</token> mobile application management policy, data is encrypted at rest using device level encryption provided by the OS.</caps:sentence>
                              <caps:sentence id="src113" class="srcSentence"> This is enabled through device PIN policy that must be set by the IT admin.</caps:sentence>
                              <caps:sentence id="src114" class="srcSentence"> When a PIN is required, the data will be encrypted per the settings in the mobile application management policy.</caps:sentence>
                              <caps:sentence id="src115" class="srcSentence"> As stated in Apple documentation, <externalLink><linkText>the modules used by iOS 7 are FIPS 140-2 certified</linkText><linkUri>http://support.apple.com/en-us/HT202739</linkUri></externalLink>.</caps:sentence>   </para>
                            <para>
                              <embeddedLabel>
                                <caps:sentence id="src116" class="srcSentence">Encryption for Android</caps:sentence>
                              </embeddedLabel>
                            </para>
                            <para>
                              <caps:sentence id="src117" class="srcSentence">For apps that are associated with an <token>wit_nextref</token> mobile application management policy, encryption is provided by Microsoft.</caps:sentence>
                              <caps:sentence id="src118" class="srcSentence"> Data is encrypted synchronously during file I/O operations according to the setting in the mobile application management policy.</caps:sentence>
                              <caps:sentence id="src119" class="srcSentence"> Managed apps on Android use AES-128 encryption in CBC mode utilizing the platform cryptography libraries.</caps:sentence>
                              <caps:sentence id="src120" class="srcSentence"> The encryption method is not FIPS 140-2 certified.</caps:sentence>
                              <caps:sentence id="src121" class="srcSentence"> Content on the device storage will always be encrypted.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src122" class="srcSentence">
                              <ui>Block screen capture</ui> (Android devices only)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src123" class="srcSentence">Specifies that the screen capture capabilities of the device are blocked when using this app.</caps:sentence>
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
                    <caps:sentence id="src124" class="srcSentence">When you are finished, click <ui>Save Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src125" class="srcSentence">The new policy displays in the <ui>Configuration Policies</ui> node of the <ui>Policy</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src126" class="srcSentence">
            <embeddedLabel>Step 4:</embeddedLabel> Associate the app with a mobile application management policy, then deploy the app.</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src127" class="srcSentence">Deploy the app, ensuring that you select the mobile application management policy on the <ui>Mobile App Management</ui> page to associate the policy with the app.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src128" class="srcSentence">For details, see <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy software to mobile devices in Windows Intune</link>.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src129" class="srcSentence">For devices that run operating systems earlier than iOS 7.1, associated policies will not be removed when the app is uninstalled.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src130" class="srcSentence">If the device is unenrolled from <token>wit_nextref</token>, polices are not removed from the apps; any apps that had policies applied will retain the policy settings even after the app is uninstalled and reinstalled.</caps:sentence>
            </para>
          </alert>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src131" class="srcSentence">What to do when an app is already deployed on devices</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src132" class="srcSentence">There might be situations where you deploy an app and one of the targeted users or devices already has an unmanaged version of the app installed, for example, the user installed Microsoft Word from the app store.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src133" class="srcSentence">In this case, you must ask the user to manually uninstall the unmanaged version so that the managed version you configured can be installed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src134" class="srcSentence">However, for devices that run iOS 9 and later, <token>wit_nextref</token> will automatically ask the user for permission to take over management of the existing app.</caps:sentence>
                <caps:sentence id="src135" class="srcSentence"> If they agree, then the app will become managed by <token>wit_nextref</token> and any mobile application management policies you associated with the app will also be applied .</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence id="src136" class="srcSentence">If the device is in supervised mode, <token>wit_nextref</token> will take over management of the existing app without asking the users permission.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src137" class="srcSentence">
            <embeddedLabel>Step 5:</embeddedLabel> Monitor the app deployment.</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src138" class="srcSentence">Once you have created and deployed an app associated with a mobile application management policy, use the following procedures to monitor the app and resolve any policy conflicts.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src139" class="srcSentence">To view the status of the deployment</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src140" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>Overview</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">Perform one of the following steps:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src142" class="srcSentence">Click <ui>All Users</ui>, then double-click on the user whose devices you want to examine.</caps:sentence>
                        <caps:sentence id="src143" class="srcSentence"> One the <ui>User Properties</ui> page, click <ui>Devices</ui>, then double-click the device you want to examine.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src144" class="srcSentence">Click <ui>All Devices</ui> &gt; <ui>All Mobile Devices</ui>.</caps:sentence>
                        <caps:sentence id="src145" class="srcSentence"> On the <ui>Device Group Properties</ui> page, click <ui>Devices</ui>, then double-click the device you want to examine.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src146" class="srcSentence">From the <ui>Mobile Device Properties</ui> page, click <ui>Policy</ui> to see a list of the mobile application management policies that have been deployed to the device.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src147" class="srcSentence">Select the mobile application management policy whose status you want to view.</caps:sentence>
                    <caps:sentence id="src148" class="srcSentence"> You can view details of the policy in the bottom pane and expand its node to display its settings.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src149" class="srcSentence">Under the <ui>Status</ui> column of each of the mobile application management policies, <ui>Conforms</ui>, <ui>Conforms (Pending)</ui>, or <ui>Error</ui> will be displayed.</caps:sentence>
                    <caps:sentence id="src150" class="srcSentence"> If the selected policy has one or more settings in conflict, <ui>Error</ui> will be displayed in this field.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">Once you have identified a conflict, you can revise conflicting policy settings to use the same setting, or deploy only one policy to the app and user.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section expanded="false" address="BKMK_Conf">
            <title>
              <caps:sentence id="src152" class="srcSentence">How policy conflicts are resolved</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src153" class="srcSentence">When there is a mobile application management policy conflict on the first deployment to the user or device, the specific setting value in conflict will be removed from the policy deployed to the app, and the app will use a built-in conflict value.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src154" class="srcSentence">When there is a mobile app management policy conflict on later deployments to the app or user, the specific setting value in conflict will not be updated on the mobile app management policy deployed to the app, and the app will use the existing value for that setting.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src155" class="srcSentence">In cases where the device or user receives two conflicting policies, the following behavior applies:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">If a policy has already been deployed to the device, the existing policy settings are not overwritten.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">If no policy has already been deployed to the device, and two conflicting settings are deployed, the default setting built into the device is used.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="71e0cbf3-2bfb-412e-8a12-8503df08b4cf">Protect company resources with Microsoft Intune</link>
        <link xlink:href="5b49d81d-8a28-4d78-a21b-6614920a7b82">Provision and configure apps with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>