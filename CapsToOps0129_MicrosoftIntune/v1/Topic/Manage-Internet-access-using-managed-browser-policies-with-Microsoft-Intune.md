---
title: Administrar el acceso a Internet mediante directivas de explorador administrado con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dc946303-e09b-4d73-8bf4-87742299bc54
---
# Administrar el acceso a Internet mediante directivas de explorador administrado con Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c201df6eb20874d0ebd4078c1563cc76" id="tgt1" class="tgtSentence">El explorador administrado es una aplicación de exploración web que se puede implementar en su organización mediante <token>wit_firstref</token>.</caps:sentence>
          <caps:sentence sentenceid="040172472ad80800b937c809caa22870" id="tgt2" class="tgtSentence"> Una directiva de explorador administrado configura una lista de permitidos o una lista de bloqueados que restringe los sitios web que pueden visitar los usuarios del explorador administrado.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4269a35958a04a8eed7aab963a1fc882" id="tgt3" class="tgtSentence">Dado que esta aplicación es una aplicación administrada, también puede aplicar las directivas de administración de aplicaciones móviles a la aplicación, tales como controlar el uso de cortar, copiar y pegar, impedir las capturas de pantalla y garantizar que los vínculos a contenido donde los usuarios pueden hacer clic solo se abran en aplicaciones administradas.</caps:sentence>
          <caps:sentence sentenceid="363ddf43df695c296401df2564573a36" id="tgt4" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="b4fb33a8-a2fa-4353-bd89-5bda48b68e83">Control apps using mobile application management policies with Microsoft Intune</link>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="d3640768dfcca36ff8813d9341804e7d" id="tgt5" class="tgtSentence">Si los usuarios instalan el explorador administrado ellos mismos, las directivas especificadas no lo administrarán.</caps:sentence>
            <caps:sentence sentenceid="0fc26a531dcdb33aa9a8bf51b3df9e85" id="tgt6" class="tgtSentence"> Para asegurarse de que el explorador se administra mediante Intune, estos deben desinstalar la aplicación para que se la pueda implementar como una aplicación administrada.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="9fe37bd0093917a7e2a895adfa384b3a" id="tgt7" class="tgtSentence">Puede crear directivas de explorador administrado para los siguientes tipos de dispositivo:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="7c4ad09da3590127d1fc36d19c68aa69" id="tgt8" class="tgtSentence">Dispositivos que ejecutan Android 4 y versiones posteriores</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="02d22031a7e394b2e03012b073970107" id="tgt9" class="tgtSentence">Dispositivos que ejecutan iOS 7 y versiones posteriores</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="3291cf0cc27507f18ea3990fcd481d51" id="tgt10" class="tgtSentence">Crear una directiva de explorador administrado</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt11" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Agregar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="0044212430dcd3451abe98376d5f68b9" id="tgt12" class="tgtSentence">Configure uno de los siguientes tipos de directivas de <ui>software</ui>:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6f8271dba7333c557acc01b3c694a968" id="tgt13" class="tgtSentence">Directiva de explorador administrado (Android 4 y posterior)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e29363275fb8a787b6f67582ec619eb6" id="tgt14" class="tgtSentence">Directiva de explorador administrado (iOS 7 y posterior)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="e19316ff66f05bdcf357a1e5cf0dfea1" id="tgt15" class="tgtSentence">Si necesita más información acerca de cómo crear e implementar directivas, consulte el tema <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="f7004f3c84376a9dddecdcda275f5e3e" id="tgt16" class="tgtSentence">La tabla siguiente le facilitará la configuración de directivas de explorador administrado:</caps:sentence>
                  </para>
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
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt18" class="tgtSentence">Más información</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt19" class="tgtSentence">Nombre</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4067d2582cc56c6070e54387a3dffe59" id="tgt20" class="tgtSentence">Escriba un nombre único para la directiva de explorador administrado que le ayude a identificarla en la consola de <token>wit_nextref</token>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt21" class="tgtSentence">Descripción</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c2601aeb987ceea160f690a47ba5b76b" id="tgt22" class="tgtSentence">Proporcione una descripción que le ofrezca una visión general de la directiva y otra información relevante que le ayude a encontrarla.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="68c5b239986d294329004c5b0de63d13" id="tgt23" class="tgtSentence">Habilitar una lista de permitidos o bloqueados para restringir las direcciones URL que el explorador administrado puede abrir</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f43dd4a21cdcb4d7a93a309c9318d45f" id="tgt24" class="tgtSentence">Seleccione una de las siguientes opciones:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="6b9c353319aeaaae536fe44a0e64ee33" id="tgt25" class="tgtSentence">
                                  <ui>Permitir al explorador administrado abrir únicamente las direcciones URL de la lista siguiente</ui>: especifique una lista de direcciones URL que el explorador administrado podrá abrir.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="20428ba6e706bb8c44cdf8caf402617c" id="tgt26" class="tgtSentence">
                                  <ui>Bloquear el explorador administrado para que no pueda abrir las direcciones URL de la lista siguiente</ui>: especifique una lista de direcciones URL que el explorador administrado no podrá abrir.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="ab3f2a1286fbcbf65c99f8b1e4cc2e67" id="tgt27" class="tgtSentence">No puede incluir direcciones URL permitidas y bloqueadas en la misma directiva de explorador administrado.</caps:sentence>
                            </para>
                          </alert>
                          <para>
                            <caps:sentence sentenceid="86e87163eb0a7a3371d61dcac26aa8d7" id="tgt28" class="tgtSentence">Para obtener más información acerca de los formatos de dirección URL que puede especificar, vea <link xlink:href="dc946303-e09b-4d73-8bf4-87742299bc54#BKMK_URLs">URL Format for allowed and blocked URLs</link> en este tema.</caps:sentence>
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
                    <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt29" class="tgtSentence">Cuando haya terminado haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt30" class="tgtSentence">La nueva directiva se muestra en el nodo <ui>Directivas de configuración</ui> del área de trabajo <ui>Directiva</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="b048cb42fb088d0f0a24259cef8eeca5" id="tgt31" class="tgtSentence">Crear una implementación de software para la aplicación de explorador administrado</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5879848019369246786fe0df02d1a0da" id="tgt32" class="tgtSentence">Después de crear la directiva de explorador administrado, puede crear una implementación de software para la aplicación de explorador administrado y asociarla a la directiva de explorador administrado que ha creado.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="9bb8564ab48db1310f5054ede1c901f8" id="tgt33" class="tgtSentence">Las directivas de explorador administrado no se implementan de la misma manera que otras directivas de <token>wit_nextref</token>.</caps:sentence>
              <caps:sentence sentenceid="ee8acab473fa9adc430a4844a31cf670" id="tgt34" class="tgtSentence"> Este tipo de directiva debe asociarse con el paquete de software de explorador administrado.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="025d1e3eade9a4fbd45dfbcb92e5aa4f" id="tgt35" class="tgtSentence">Implemente la aplicación y asegúrese de seleccionar la directiva de explorador administrado en la página <ui>Administración de aplicaciones móviles</ui> para asociar la directiva a la aplicación.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="18bef32c9c6f057d58d12adc93eaa5f4" id="tgt36" class="tgtSentence">Para obtener más información sobre cómo implementar directivas, consulte <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy software to mobile devices in Windows Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="66409ed88975741fbf1e7ed44954ed56" id="tgt37" class="tgtSentence">Seguridad y privacidad del explorador administrado</caps:sentence>
        </title>
        <content>
          <para></para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="fdfe0a6c4ccb5818f53e6fb3d60743b1" id="tgt38" class="tgtSentence">En dispositivos iOS, no se pueden abrir los sitios web que visitan los usuarios y que tienen un certificado expirado o que no es de confianza.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="515e0952c554f7abd7b72688d52a5e83" id="tgt39" class="tgtSentence">El explorador administrado no usa la configuración que realizan los usuarios para el explorador integrado en sus dispositivos.</caps:sentence>
                <caps:sentence sentenceid="9f4df5c4a26ae209a94c2816d181acb9" id="tgt40" class="tgtSentence"> Esto se debe a que el explorador administrado no tiene acceso a esta configuración.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e95a85cfd9bb07c0d5db1f6fd6d5af9b" id="tgt41" class="tgtSentence">Si configura las opciones <ui>Requerir PIN sencillo para el acceso</ui> o <ui>   Requerir credenciales corporativas para el acceso </ui> en una directiva de administración de aplicaciones móviles asociada con el explorador administrado, cuando un usuario haga clic en el vínculo de ayuda en la página autenticación, podrá examinar los sitios de Internet independientemente de si se agregaron a una lista de bloqueados en la directiva de explorador administrado.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="808872de1b8a17d97f0bd6759100e7e8" id="tgt42" class="tgtSentence">El explorador administrado solo puede bloquear el acceso a sitios cuando se accede a estos directamente.</caps:sentence>
                <caps:sentence sentenceid="609670c87e0905a6411191f522863e36" id="tgt43" class="tgtSentence"> No puede bloquear el acceso cuando se usan servicios intermedios (por ejemplo, un servicio de traducción) para acceder al sitio.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e8a448a3c90a61edf36edda6cd725415" id="tgt44" class="tgtSentence">Para permitir la autenticación, <ui>*.microsoft.com</ui> está exento de la configuración de permitidos o bloqueados: siempre se permite.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="d3d297c4ec3eb120f4d37f0a160f9af0" id="tgt45" class="tgtSentence">Información de referencia</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section address="BKMK_URLs" expanded="false">
            <title>
              <caps:sentence sentenceid="2b2f3a74dfade3c37f1a625e0b6a8920" id="tgt46" class="tgtSentence">Formato de dirección URL para las direcciones URL permitidas y bloqueadas</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="02947663304488a1b8357b47e297f669" id="tgt47" class="tgtSentence">Utilice la siguiente información para conocer los formatos permitidos y los caracteres comodín que puede usar al especificar direcciones URL en las listas de permitidos y bloqueados.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5a16e8631c5ab0ccdea54a460c9e1d9a" id="tgt48" class="tgtSentence">Puede utilizar el carácter comodín '<ui>*</ui>' según las reglas de la siguiente lista de patrones permitidos.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b2ff55d8cfa63fb66ca3cd67cf587925" id="tgt49" class="tgtSentence">Asegúrese de anteponer <ui>http</ui> o <ui>https</ui> a todas las direcciones URL al introducirlas en la lista.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3bdc49f988eb568ba1f205f21ba8da4b" id="tgt50" class="tgtSentence">Puede especificar números de puerto en la dirección.</caps:sentence>
                    <caps:sentence sentenceid="4fbef20a562900e7652c274538bd9dce" id="tgt51" class="tgtSentence"> Si no especifica un número de puerto, los valores usados serán:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d6fc4e37ee93ef77cea8019be84abcd6" id="tgt52" class="tgtSentence">Puerto 80 para http</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="0381a453cfbac15ab6d36f5476b7f228" id="tgt53" class="tgtSentence">Puerto 443 para https</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="2ab265559cd6a059e9649bae632ac863" id="tgt54" class="tgtSentence">No se admite el uso de caracteres comodín para el número de puerto como, por ejemplo, <ui>http://www.contoso.com:*</ui> y <ui>http://www.contoso.com: /*</ui></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e77fdb3273272c516b7c16157152c8a5" id="tgt55" class="tgtSentence">Utilice la siguiente tabla para obtener información acerca de los patrones permitidos que puede usar al especificar direcciones URL:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="572d4e421e5e6b9bc11d815e8a027112" id="tgt56" class="tgtSentence">Dirección URL</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt57" class="tgtSentence">Descripción</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9c28d32df234037773be184dbdafc274" id="tgt58" class="tgtSentence">Coincide</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="42945a1174cbb526d960490fb94c9a79" id="tgt59" class="tgtSentence">No coincide</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="247191ba871b71178994e143d5ef4a19" id="tgt60" class="tgtSentence">http://www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2a67c413d4756f0231eea52a33401d22" id="tgt61" class="tgtSentence">Coincide con una sola página</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="965fc798118a5fff23691778f73ed877" id="tgt62" class="tgtSentence">www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="38b9311789bc6edae05c70ba38518477" id="tgt63" class="tgtSentence">host.contoso.com</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="06587f132df1b6cd78b0c403c505514e" id="tgt64" class="tgtSentence">www.contoso.com/images</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="08729065c2417dd9ab67527a0b7207bc" id="tgt65" class="tgtSentence">contoso.com/</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d0c12db4e81b7512ffde9c763257dc69" id="tgt66" class="tgtSentence">http://contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2a67c413d4756f0231eea52a33401d22" id="tgt67" class="tgtSentence">Coincide con una sola página</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="08729065c2417dd9ab67527a0b7207bc" id="tgt68" class="tgtSentence">contoso.com/</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="38b9311789bc6edae05c70ba38518477" id="tgt69" class="tgtSentence">host.contoso.com</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="06587f132df1b6cd78b0c403c505514e" id="tgt70" class="tgtSentence">www.contoso.com/images</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="965fc798118a5fff23691778f73ed877" id="tgt71" class="tgtSentence">www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8cea7c0f748958fe05348c66caf02617" id="tgt72" class="tgtSentence">http://www.contoso.com/*</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d04f6513238e8eb348bed5ee4f5269c8" id="tgt73" class="tgtSentence">Coincide con todas las direcciones URL que comienzan con www.contoso.com </caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="965fc798118a5fff23691778f73ed877" id="tgt74" class="tgtSentence">www.contoso.com</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="06587f132df1b6cd78b0c403c505514e" id="tgt75" class="tgtSentence">www.contoso.com/images</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="a2273af6d818c473934699a6ce994414" id="tgt76" class="tgtSentence">www.contoso.com/videos/tvshows</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="38b9311789bc6edae05c70ba38518477" id="tgt77" class="tgtSentence">host.contoso.com</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="518e32170773cc931ae11f930120db9f" id="tgt78" class="tgtSentence">host.contoso.com/images</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3332bd37e29a05de27fbbc76520068ac" id="tgt79" class="tgtSentence">http://*.contoso.com/*</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="0ac14b4c8128ba7c40d02225736e5c1a" id="tgt80" class="tgtSentence">Coincide con todos los subdominios en contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3ce12dd8816cb7ad51b67236794d993d" id="tgt81" class="tgtSentence">developer.contoso.com/resources</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="3373403137dba506a46688ad2d8fabfa" id="tgt82" class="tgtSentence">news.contoso.com/images</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="09fa8f3624ae4ac94b447d40226d3aab" id="tgt83" class="tgtSentence">news.contoso.com/images</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="076bc7e72ce6f915d0fee6cfb8fcce54" id="tgt84" class="tgtSentence">contoso.host.com</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="43c317173e5ff0a4990eb7a5e4df58a9" id="tgt85" class="tgtSentence">http://www.contoso.com/images</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9700986901fc01e7941bc419655e6612" id="tgt86" class="tgtSentence">Coincide con una sola carpeta</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="06587f132df1b6cd78b0c403c505514e" id="tgt87" class="tgtSentence">www.contoso.com/images</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7cfa15ca93864be7b1b5ed692d2baa3c" id="tgt88" class="tgtSentence">www.contoso.com/images/dogs</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a352bd416597b9e26f9a6cd3653bb6b3" id="tgt89" class="tgtSentence">http://www.contoso.com:80</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7382fa055c423a008379ceaecb48cb44" id="tgt90" class="tgtSentence">Coincide con una sola página, con un número de puerto</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a352bd416597b9e26f9a6cd3653bb6b3" id="tgt91" class="tgtSentence">http://www.contoso.com:80</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para></para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="38449cd377fd859ef1c34101446400f2" id="tgt92" class="tgtSentence">https://www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="503a17e57eb57c51e38ad60b37c59ee0" id="tgt93" class="tgtSentence">Coincide con una sola página segura</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="38449cd377fd859ef1c34101446400f2" id="tgt94" class="tgtSentence">https://www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="247191ba871b71178994e143d5ef4a19" id="tgt95" class="tgtSentence">http://www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4fece20f4532cb6ada2ad2a7b98fa7b4" id="tgt96" class="tgtSentence">http://www.contoso.com/images/*</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f59732eb2f7ea4f71364fffeab3581f5" id="tgt97" class="tgtSentence">Coincide con una sola carpeta y todas sus subcarpetas</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7cfa15ca93864be7b1b5ed692d2baa3c" id="tgt98" class="tgtSentence">www.contoso.com/images/dogs</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="b97afedf0831b4f863aa51a8903cc12b" id="tgt99" class="tgtSentence">www.contoso.com/images/cats</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="052dae1d6a11ad6a983ff4c37360b443" id="tgt100" class="tgtSentence">www.contoso.com/videos</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f0f0badf1b8eb1c106a120938b50431d" id="tgt101" class="tgtSentence">Los siguientes son ejemplos de algunas de las entradas que no se pueden especificar:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5f8f90389cbf5085efab6030ed861c09" id="tgt102" class="tgtSentence">*.com</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="afaa67a72765f4cf67b8ed935f8ce9f7" id="tgt103" class="tgtSentence">*.contoso/*</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="7f666796a41fbd2af4a39f3eca37b421" id="tgt104" class="tgtSentence">www.contoso.com/*images</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="23f1e75b183de1db9c00152351e47eda" id="tgt105" class="tgtSentence">www.contoso.com/*images*pigs</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4b561469459ed17e940b92d2afb0e3e2" id="tgt106" class="tgtSentence">www.contoso.com/page*</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="59f9536b0aa21a81c28d128d9f5095fc" id="tgt107" class="tgtSentence">Direcciones IP</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="15b848490e5722142b1db3d2a004d884" id="tgt108" class="tgtSentence">https://*</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3e8bc715182c5b7d4e57db7468bdd06e" id="tgt109" class="tgtSentence">http://*</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="0d7d1b7c11b3ae3ced5addfe324491d1" id="tgt110" class="tgtSentence">http://www.contoso.com:*</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b64c15dceb168bba2ab16e3a243ed581" id="tgt111" class="tgtSentence">http://www.contoso.com: /*</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="e8ed89b13a8761edc1ab0550bb665e56" id="tgt112" class="tgtSentence">Cómo se resuelven los conflictos entre las listas de permitidos y bloqueados</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="21dfa5f57fb6d29bfff4f294edffe700" id="tgt113" class="tgtSentence">Si se implementan varias directivas de explorador administrado en un dispositivo y la configuración presenta conflictos, tanto el modo (permitir o bloquear) como las listas de direcciones URL se evalúan para detectar conflictos.</caps:sentence>
                <caps:sentence sentenceid="ccc596f58b922213181c5ca73e7dabe9" id="tgt114" class="tgtSentence"> En caso de conflicto, se aplica el comportamiento siguiente:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0d714b2bfa9eaa62553446bafa27326e" id="tgt115" class="tgtSentence">Si los modos de cada directiva son iguales, pero las listas de direcciones URL son diferentes, las direcciones URL no se aplicarán en el dispositivo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="7128efc54919513616099f57ae9fda16" id="tgt116" class="tgtSentence">Si los modos de cada directiva son diferentes, pero las listas de direcciones URL son iguales, las direcciones URL no se aplicarán en el dispositivo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="7eeb69d82bae6d13c5c64747e7a90409" id="tgt117" class="tgtSentence">Si un dispositivo está recibiendo las directivas de explorador administrado por primera vez y dos directivas están en conflicto, las direcciones URL no se aplicarán en el dispositivo.</caps:sentence>
                    <caps:sentence sentenceid="7008d361da948c4f95a6d66d8fad3f5d" id="tgt118" class="tgtSentence"> Utilice el nodo <ui>Conflictos de directivas</ui> del área de trabajo <ui>Directiva</ui> para ver los conflictos.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0a27352a502a3e193c76f610f59f122b" id="tgt119" class="tgtSentence">Si un dispositivo ya ha recibido una directiva de explorador administrado y se implementa una segunda directiva con la configuración en conflicto, la configuración original permanece en el dispositivo.</caps:sentence>
                    <caps:sentence sentenceid="7008d361da948c4f95a6d66d8fad3f5d" id="tgt120" class="tgtSentence"> Utilice el nodo <ui>Conflictos de directivas</ui> del área de trabajo <ui>Directiva</ui> para ver los conflictos.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="5b090c5a-6f12-4e60-ace0-c9929afaa9a3">Enable access to company resources with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The managed browser is a web browsing application that you can deploy in your organization using <token>wit_firstref</token>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> A managed browser policy configures an allow list or a block list that restricts the web sites that users of the managed browser can visit.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">Because this app is a managed app, you can also apply mobile application management policies to the app, such as controlling the use of cut, copy and paste, preventing screen captures, and also ensuring that links to content that users click only open in other managed apps.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For details, see <link xlink:href="b4fb33a8-a2fa-4353-bd89-5bda48b68e83">Control apps using mobile application management policies with Microsoft Intune</link>.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src5" class="srcSentence">If users install the managed browser themselves, it will not be managed by any policies you specify.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> To ensure that the browser is managed by Intune, they must uninstall the app before you can deploy it to them as a managed app.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src7" class="srcSentence">You can create managed browser policies for the following device types:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Devices that run Android 4 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Devices that run iOS 7 and later</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Create a managed browser policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Configure one of the following <ui>Software</ui> policy types:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src13" class="srcSentence">Managed Browser Policy (Android 4 and later)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src14" class="srcSentence">Managed Browser Policy (iOS 7 and later)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">For more information about how to create and deploy policies, see the <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link> topic.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Use the following table to help you configure the managed browser policy settings:</caps:sentence>
                  </para>
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
                            <caps:sentence id="src18" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src19" class="srcSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src20" class="srcSentence">Enter a unique name for the managed browser policy to help you identify it in the <token>wit_nextref</token> console.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src21" class="srcSentence">Description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src22" class="srcSentence">Provide a description that gives an overview of the managed browser policy and other relevant information that helps you to locate it.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src23" class="srcSentence">Enable an allow list or block list to restrict the URLs the Managed Browser can open</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src24" class="srcSentence">Select one of the following options:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src25" class="srcSentence">
                                  <ui>Allow the managed browser to open only the URLs listed below</ui> – Specify a list of URLs that the managed browser can open.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src26" class="srcSentence">
                                  <ui>Block the managed browser from opening the URLs listed below</ui> – Specify a list of URLs that the managed browser will be blocked from opening.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src27" class="srcSentence">You cannot include both allowed and blocked URLs in the same managed browser policy.</caps:sentence>
                            </para>
                          </alert>
                          <para>
                            <caps:sentence id="src28" class="srcSentence">For more information about the URL formats you can specify, see <link xlink:href="dc946303-e09b-4d73-8bf4-87742299bc54#BKMK_URLs">URL Format for allowed and blocked URLs</link> in this topic.</caps:sentence>
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
                    <caps:sentence id="src29" class="srcSentence">When you are finished, click <ui>Save Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src30" class="srcSentence">The new policy displays in the <ui>Configuration Policies</ui> node of the <ui>Policy</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src31" class="srcSentence">Create a software deployment for the managed browser app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src32" class="srcSentence">After you have created the managed browser policy, you can then create a software deployment for the managed browser app, and associate it with the managed browser policy you created.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src33" class="srcSentence">Managed browser policies are not deployed in the same way as other <token>wit_nextref</token> polices.</caps:sentence>
              <caps:sentence id="src34" class="srcSentence"> This type of policy must be associated with the managed browser software package.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src35" class="srcSentence">Deploy the app, ensuring that you select the managed browser policy on the <ui>Mobile App Management</ui> page to associate the policy with the app.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src36" class="srcSentence">For more information about how to deploy apps, see <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy software to mobile devices in Windows Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src37" class="srcSentence">Security and privacy for the managed browser</caps:sentence>
        </title>
        <content>
          <para></para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src38" class="srcSentence">On iOS devices, web sites that users visit that have an expired or untrusted certificate cannot be opened.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src39" class="srcSentence">Settings that users make for the built-in browser on their devices are not used by the managed browser.</caps:sentence>
                <caps:sentence id="src40" class="srcSentence"> This is because the managed browser does not have access to these settings.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src41" class="srcSentence">If you configure the options <ui>Require simple PIN for access</ui> or <ui>Require corporate credentials for access</ui> in a mobile application management policy associated with the managed browser and a user clicks the help link on the authentication page, they can then browse any Internet sites regardless of whether they were added to a block list in the managed browser policy.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src42" class="srcSentence">The managed browser can only block access to sites when they are accessed directly.</caps:sentence>
                <caps:sentence id="src43" class="srcSentence"> It cannot block access when intermediate services (such as a translation service) are used to access the site.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src44" class="srcSentence">To allow authentication, <ui>*.microsoft.com</ui> is exempt from the allow or block list settings – it is always allowed.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src45" class="srcSentence">Reference information</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section address="BKMK_URLs" expanded="false">
            <title>
              <caps:sentence id="src46" class="srcSentence">URL format for allowed and blocked URLs</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src47" class="srcSentence">Use the following information to learn about the allowed formats and wildcards you can use when specifying URLs in the allowed and blocked lists.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">You can use the wildcard symbol ‘<ui>*</ui>’ according to the rules in the permitted patterns list below.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">Ensure that you prefix all URLs with <ui>http</ui> or <ui>https</ui> when entering them into the list.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">You can specify port numbers in the address.</caps:sentence>
                    <caps:sentence id="src51" class="srcSentence"> If you do not specify a port number, the values used will be:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">Port 80 for http</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">Port 443 for https</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Using wildcards for the port number is not supported, for example, <ui>http://www.contoso.com:*</ui> and <ui>http://www.contoso.com: /*</ui></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">Use the following table to learn about the permitted patterns you can use when you specify URLs:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src56" class="srcSentence">URL</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src57" class="srcSentence">Description</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src58" class="srcSentence">Matches</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src59" class="srcSentence">Does not match</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src60" class="srcSentence">http://www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src61" class="srcSentence">Matches a single page</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src62" class="srcSentence">www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src63" class="srcSentence">host.contoso.com</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src64" class="srcSentence">www.contoso.com/images</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src65" class="srcSentence">contoso.com/</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src66" class="srcSentence">http://contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src67" class="srcSentence">Matches a single page</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src68" class="srcSentence">contoso.com/</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src69" class="srcSentence">host.contoso.com</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src70" class="srcSentence">www.contoso.com/images</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src71" class="srcSentence">www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src72" class="srcSentence">http://www.contoso.com/*</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src73" class="srcSentence">Matches all URLs beginning with www.contoso.com </caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src74" class="srcSentence">www.contoso.com</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src75" class="srcSentence">www.contoso.com/images</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src76" class="srcSentence">www.contoso.com/videos/tvshows</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src77" class="srcSentence">host.contoso.com</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src78" class="srcSentence">host.contoso.com/images</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src79" class="srcSentence">http://*.contoso.com/*</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src80" class="srcSentence">Matches all sub-domains under contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src81" class="srcSentence">developer.contoso.com/resources</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src82" class="srcSentence">news.contoso.com/images</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src83" class="srcSentence">news.contoso.com/videos</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src84" class="srcSentence">contoso.host.com</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src85" class="srcSentence">http://www.contoso.com/images</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src86" class="srcSentence">Matches a single folder</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src87" class="srcSentence">www.contoso.com/images</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src88" class="srcSentence">www.contoso.com/images/dogs</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src89" class="srcSentence">http://www.contoso.com:80</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src90" class="srcSentence">Matches a single page, using a port number</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src91" class="srcSentence">http://www.contoso.com:80</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para></para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src92" class="srcSentence">https://www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src93" class="srcSentence">Matches a single, secure page</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src94" class="srcSentence">https://www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src95" class="srcSentence">http://www.contoso.com</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src96" class="srcSentence">http://www.contoso.com/images/*</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src97" class="srcSentence">Matches a single folder and all subfolders</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src98" class="srcSentence">www.contoso.com/images/dogs</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src99" class="srcSentence">www.contoso.com/images/cats</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src100" class="srcSentence">www.contoso.com/videos</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">The following are examples of some of the inputs you cannot specify:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">*.com</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src103" class="srcSentence">*.contoso/*</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src104" class="srcSentence">www.contoso.com/*images</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src105" class="srcSentence">www.contoso.com/*images*pigs</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">www.contoso.com/page*</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">IP addresses</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src108" class="srcSentence">https://*</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src109" class="srcSentence">http://*</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src110" class="srcSentence">http://www.contoso.com:*</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src111" class="srcSentence">http://www.contoso.com: /*</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src112" class="srcSentence">How conflicts between the allow and block list are resolved</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src113" class="srcSentence">If multiple managed browser policies are deployed to a device and the settings conflict, both the mode (allow or block) and the URL lists are evaluated for conflicts.</caps:sentence>
                <caps:sentence id="src114" class="srcSentence"> In case of a conflict, the following behavior applies:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">If the modes in each policy are the same, but the URL lists are different, the URLs will not be enforced on the device.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">If the modes in each policy are different, but the URL lists are the same, the URLs will not be enforced on the device.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">If a device is receiving managed browser policies for the first time and two policies conflict, the URLs will not be enforced on the device.</caps:sentence>
                    <caps:sentence id="src118" class="srcSentence"> Use the <ui>Policy Conflicts</ui> node of the <ui>Policy</ui> workspace to view the conflicts.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src119" class="srcSentence">If a device has already received a managed browser policy and a second policy is deployed with conflicting settings, the original settings remain on the device.</caps:sentence>
                    <caps:sentence id="src120" class="srcSentence"> Use the <ui>Policy Conflicts</ui> node of the <ui>Policy</ui> workspace to view the conflicts.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="5b090c5a-6f12-4e60-ace0-c9929afaa9a3">Enable access to company resources with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>