---
title: Introducci&#243;n a la implementaci&#243;n de aplicaciones en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2b770f4f-6d36-41e4-b535-514b46e29aaa
---
# Introducci&#243;n a la implementaci&#243;n de aplicaciones en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="e8de541da7c036b17cc11621923e7a79" id="tgt1" class="tgtSentence">Antes de administrar e implementar aplicaciones en <token>wit_firstref</token>, use la información de esta sección para obtener información acerca de:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_SoftwareWorkspace">The App workspace</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_SoftwarePublisher">Microsoft Intune Software Publisher</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_OSRequirements">Operating system requirements</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_Types">Software installation types</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_SoftwareDistProcess">General app distribution process</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_Depl">Understand app distribution actions</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section DoNotNumber="false" address="BKMK_SoftwareWorkspace">
        <title>
          <caps:sentence sentenceid="d534fd3ee25145f520ecdc9c320ae41b" id="tgt2" class="tgtSentence">Área de trabajo de aplicaciones</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt3" class="tgtSentence">El área de trabajo de <ui>aplicaciones</ui> de la <token>wit_adminconsole</token> proporciona información sobre aplicaciones detectadas y administradas.</caps:sentence>
            <caps:sentence sentenceid="53dad362bd481cd9384e73af8f6023cc" id="tgt4" class="tgtSentence"> Están disponibles las páginas siguientes:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1c7a3bf58a2404dcc92a2301a3c8e428" id="tgt5" class="tgtSentence">Página del área de trabajo de aplicaciones</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt6" class="tgtSentence">Detalles</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="bce059749d61c1c247c303d0118d0d53" id="tgt7" class="tgtSentence">Información general</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b71e34cebb8ce945f7426bc15a59af1d" id="tgt8" class="tgtSentence">Enumera las alertas de implementación de aplicaciones y el estado actual del almacenamiento en nube.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="d22e228a9d678667efba5f1626bcaa9a" id="tgt9" class="tgtSentence">Software detectado</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="056c39b0a4a8f31b573b5b966f39d7e4" id="tgt10" class="tgtSentence">Muestra los datos de inventario de software que <token>wit_firstref</token> detecta en los equipos administrados.</caps:sentence>
                    <caps:sentence sentenceid="5ba02170630f770b1119f8eb61a958ea" id="tgt11" class="tgtSentence"> El inventario de software solo está disponible para los equipos.</caps:sentence>
                    <caps:sentence sentenceid="a475378bd828303e872a2f5759459521" id="tgt12" class="tgtSentence"> Por tanto, <token>wit_nextref</token> no detecta ni enumera aplicaciones para dispositivos móviles administrados.</caps:sentence>
                    <caps:sentence sentenceid="737a0c28d2767800588e714e3195d5c9" id="tgt13" class="tgtSentence"> Puede realizar las siguientes tareas desde el área de trabajo <ui>Software detectado</ui>:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="994aec93e587691cbae7fbb66d65fda2" id="tgt14" class="tgtSentence">Ver propiedades de aplicaciones</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="dbc93b9c2ac6012dcf42c8ed40191ff0" id="tgt15" class="tgtSentence">Agregar contratos de licencia para el software detectado</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="9a6dd283c3de653fbca500f9721f634f" id="tgt16" class="tgtSentence">Aplicaciones</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt17" class="tgtSentence">En la página <ui>Aplicaciones</ui> se cargan, implementan y administran de manera continua las aplicaciones que quiere implementar en equipos y dispositivos móviles administrados.</caps:sentence>
                    <caps:sentence sentenceid="712ef70f3f0846ff718404f0f568f68e" id="tgt18" class="tgtSentence"> Puede realizar las siguientes tareas:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="494d9c85b754c9212fc1af64886823a7" id="tgt19" class="tgtSentence">Ver y modificar propiedades de aplicaciones</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ee68cf31cb7c4dcc643736d693dd486f" id="tgt20" class="tgtSentence">Agregar contratos de licencia para las aplicaciones administradas</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5835646a26b9a51332e07406adc656de" id="tgt21" class="tgtSentence">Administrar implementaciones de aplicaciones</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f9743fe66fe679e0d30f091eb111bb11" id="tgt22" class="tgtSentence">Agregar nuevas aplicaciones</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f3262c68bcb547853833edf2759749e4" id="tgt23" class="tgtSentence">Editar las propiedades de las aplicaciones administradas</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="07bf975491998ebce01dd870e281db84" id="tgt24" class="tgtSentence">Eliminar aplicaciones</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section DoNotNumber="false" address="BKMK_SoftwarePublisher">
        <title>
          <caps:sentence sentenceid="a5de0000af72cecb37fd8fbea94d5137" id="tgt25" class="tgtSentence">Microsoft Intune Software Publisher</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt26" class="tgtSentence">El <ui>Editor de software de Microsoft Intune</ui> se inicia al agregar o modificar aplicaciones desde la <token>wit_adminconsole</token>.</caps:sentence>
            <caps:sentence sentenceid="bbb6243f1b376044f055564720ad19c2" id="tgt27" class="tgtSentence"> En el editor, se selecciona un tipo de instalador de software que permitirá cargar aplicaciones (programas para equipos o aplicaciones para dispositivos móviles) para almacenarlo en el almacenamiento en nube de <token>wit_nextref</token> o vincularlo a una tienda en línea o una aplicación web.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_PublisherRequirements">
            <title>
              <caps:sentence sentenceid="11e13d19e22de00daa252d28d312be17" id="tgt28" class="tgtSentence">Requisitos del editor de software de Microsoft Intune</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="aa0a31238729749d5d58eb3f2656d7a6" id="tgt29" class="tgtSentence">Antes de empezar a utilizar el editor de software de <token>wit_firstref</token>, necesita instalar la versión completa de Microsoft .NET Framework 4.0.</caps:sentence>
                <caps:sentence sentenceid="0a9d81226f8a4ada3b1ffc8d6fc24046" id="tgt30" class="tgtSentence"> Después de instalar .NET Framework, podría ser necesario reiniciar el equipo para que el editor de software de <token>wit_firstref</token> se abra correctamente.</caps:sentence>
                <caps:sentence sentenceid="363ddf43df695c296401df2564573a36" id="tgt31" class="tgtSentence"> Para obtener más información, consulte <externalLink><linkText>Microsoft .NET Framework 4 (instalador web)</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=17851</linkUri></externalLink>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_CloudStorage">
            <title>
              <caps:sentence sentenceid="f7b83bdd918fc48cf3bada6487869519" id="tgt32" class="tgtSentence">Requisitos de almacenamiento en nube</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="94a05257b0d9be1c1414dd8cd6f09290" id="tgt33" class="tgtSentence">Todas las aplicaciones que se implementen deben empaquetarse y cargarse al almacenamiento en nube de <token>wit_firstref</token>.</caps:sentence>
                <caps:sentence sentenceid="d175291785be26dfdbcd9865f0fbd133" id="tgt34" class="tgtSentence"> Antes de implementar aplicaciones, asegúrese de que haya suficiente espacio de almacenamiento disponible para cargarlas.</caps:sentence>
                <caps:sentence sentenceid="6cce4932a12692d0a4aa77fdf194351e" id="tgt35" class="tgtSentence"> Una suscripción de prueba de <token>wit_nextref</token> incluye 2 gigabytes (GB) de almacenamiento en nube que sirve para almacenar actualizaciones y aplicaciones administradas.</caps:sentence>
                <caps:sentence sentenceid="2acc5b7f1c7e5aed54492fa398448c7c" id="tgt36" class="tgtSentence"> Una suscripción de pago incluye 20 GB, con la opción de adquirir más espacio de almacenamiento en incrementos de 1 GB mediante el Complemento de almacenamiento adicional de <token>wit_firstref</token>.</caps:sentence>
                <caps:sentence sentenceid="6685204956cc52acaff92b1d153ee0e6" id="tgt37" class="tgtSentence"> Las siguientes reglas se aplican a la compra de más almacenamiento en la nube para <token>wit_nextref</token>:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3f1a40ddd0b131b39ce6950f5ee6ca80" id="tgt38" class="tgtSentence">No puede adquirir almacenamiento adicional durante el período de prueba o de versión preliminar de <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0e22f73e280ba5b204ac8587fa94f0cf" id="tgt39" class="tgtSentence">Debe tener una suscripción de pago activa para poder adquirir almacenamiento adicional.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="351a8185ac026b97ade59a39dc8f0c7b" id="tgt40" class="tgtSentence">Únicamente los administradores de facturación o los administradores globales de su servicio de Microsoft Online pueden adquirir almacenamiento adicional a través del portal de cuentas de <token>wit_nextref</token>.</caps:sentence>
                    <caps:sentence sentenceid="43e04df45e301dc06c6cb1655f743c27" id="tgt41" class="tgtSentence"> Para administrar, agregar o eliminar estos administradores, usted debe ser administrador global e iniciar sesión en el portal de cuentas de <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e5568d48ea1aee8e7b076a3d3ccc37bb" id="tgt42" class="tgtSentence">Si es un cliente de licencias por volumen que adquirió <token>wit_nextref</token> o el complemento <token>wit_firstref</token> a través de un contrato Enterprise, póngase en contacto con su gestor de cuentas de Microsoft o su partner de Microsoft para obtener información relativa a los precios y para adquirir almacenamiento adicional.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="090bc52c3035e737cc94f39f8ea82c74" id="tgt43" class="tgtSentence">Para comprar almacenamiento adicional</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt44" class="tgtSentence">En el <externalLink><linkText>portal de cuentas de Microsoft Intune</linkText><linkUri>https://account.manage.microsoft.com</linkUri></externalLink>, en el panel izquierdo en <ui>Suscripciones</ui>, haga clic en <ui>Administrar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt45" class="tgtSentence">En la página <ui>Administración de suscripciones y facturación</ui>, haga clic en la suscripción de <token>wit_nextref</token> para la que desea comprar almacenamiento adicional.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt46" class="tgtSentence">En la página <ui>Detalles de la suscripción</ui>, en <ui>Complementos opcionales</ui>, haga clic en <ui>Agregar más</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt47" class="tgtSentence">En la página <ui>Seleccionar número de licencias</ui>, en <ui>Complementos opcionales</ui>, escriba el número de GB de almacenamiento adicional que desea comprar para el complemento de almacenamiento adicional de Microsoft Intune.</caps:sentence>
                        <caps:sentence sentenceid="e1f156ae74c21136d3de3959f51c51ec" id="tgt48" class="tgtSentence"> Por ejemplo, si actualmente tiene 20 GB y desea agregar 10 GB, escriba 10.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt49" class="tgtSentence">En la página <ui>Revisar información importante</ui>, revise la información de resumen de pedido y, si es correcta, haga clic en <ui>Realizar pedido</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt50" class="tgtSentence">La página <ui>Confirmación de pedido</ui> se abre para mostrar los detalles del pedido.</caps:sentence>
                        <caps:sentence sentenceid="9c246454e1fc1fdab04143e527678570" id="tgt51" class="tgtSentence"> Haga clic en <ui>Finalizar</ui> para completar el proceso.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section DoNotNumber="false" address="BKMK_OSRequirements">
        <title>
          <caps:sentence sentenceid="280f13faf59f75c6315dcea4839d9262" id="tgt52" class="tgtSentence">Requisitos del sistema operativo</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="326ace8e395baf65da41e93b3e733959" id="tgt53" class="tgtSentence">Los dispositivos móviles y los equipos deben ejecutar un sistema operativo compatible para instalar las aplicaciones que se implementan con <token>wit_nextref</token>.</caps:sentence>
          </para>
          <para>
            <embeddedLabel>
              <caps:sentence sentenceid="09156eaf9ed2f5e3235fae84f05a0fad" id="tgt54" class="tgtSentence">Dispositivos móviles</caps:sentence>
            </embeddedLabel>
          </para>
          <para>
            <caps:sentence sentenceid="abc16928024fa2d5ff0b3c415bf06a49" id="tgt55" class="tgtSentence">Para obtener la lista completa de sistemas operativos compatibles con dispositivos móviles, consulte <link xlink:href="f23b3ee7-78da-4e53-9fc2-78e58401bcf9">Mobile device management capabilities in Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <embeddedLabel>
              <caps:sentence sentenceid="524164822d03894ee68052e183e7ea36" id="tgt56" class="tgtSentence">Equipos</caps:sentence>
            </embeddedLabel>
          </para>
          <para>
            <caps:sentence sentenceid="6dfde1d4eff29145bb4927608440807f" id="tgt57" class="tgtSentence">Para obtener la lista completa de sistemas operativos compatibles para los equipos administrados, consulte <link xlink:href="77fa5c66-a87c-47df-964c-800eea509b33">Computer management capabilities in Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_Types">
        <title>
          <caps:sentence sentenceid="9be8fe26b78b86faa8689aa3a4da8b99" id="tgt58" class="tgtSentence">Tipos de instalación de software</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="64ef014eb7bae3a6512c6cdbb6098fde" id="tgt59" class="tgtSentence">
              <token>wit_nextref</token> permite implementar los siguientes tipos de instalación de software:</caps:sentence>
          </para>
        </content>
        <sections>
          <section DoNotNumber="false" address="BKMK_SoftwareInstallers">
            <title>
              <caps:sentence sentenceid="6ac8576a66f05b034829359342f04293" id="tgt60" class="tgtSentence">Instalador de software</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt61" class="tgtSentence">Utilice el tipo de instalación <ui>Instalador de Software</ui> para:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3c69e64ab31cc520986582e240c47d4b" id="tgt62" class="tgtSentence">Cargar un paquete de la aplicación firmado al almacenamiento en nube de Microsoft Intune y poner la aplicación a disposición de los usuarios a través del <token>wit_iwportal_1</token>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="eb5eaed4e442c21339c0fae443698a18" id="tgt63" class="tgtSentence">Cargar aplicaciones que se implementarán en equipos que ejecutan el cliente de equipo de <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8ddcf20ee2b0ac8795251993f18b2d8d" id="tgt64" class="tgtSentence">Instalar aplicaciones en dispositivos móviles administrados desde un archivo de instalación, pasando por alto la tienda de aplicaciones (lo que se conoce como instalación de prueba).</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="2c5c12fbab15f067b699d7acae161d15" id="tgt65" class="tgtSentence">Utilice la tabla siguiente para ayudarle a entender los diferentes tipos de archivo de instalador de software:</caps:sentence>
              </para>
              <table>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <legacyBold>
                          <caps:sentence sentenceid="ca60d03de958402998a3dcdc3c53bef0" id="tgt66" class="tgtSentence">Tipo de instalador de software</caps:sentence>
                        </legacyBold>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <legacyBold>
                          <caps:sentence sentenceid="b4851e92b19af0c5c82447fc0937709d" id="tgt67" class="tgtSentence">Requisitos</caps:sentence>
                        </legacyBold>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="13753637c76e16592ff40c38458eb307" id="tgt68" class="tgtSentence">Windows Installer (*.msi, *.exe)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0e5916674075a1dd67824b004d47d7da" id="tgt69" class="tgtSentence">Los archivos de Windows Installer deben ser compatibles con una instalación silenciosa, es decir, sin que sea necesaria la intervención del usuario.</caps:sentence>
                            <caps:sentence sentenceid="f30ed67e66e0b6fb41ea68e09d5cc2a8" id="tgt70" class="tgtSentence"> Si la aplicación usa otro tipo de archivo de instalación o requiere la intervención del usuario durante la instalación, no podrá instalarse mediante <token>wit_nextref</token>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="5d40223430e38980d54aea711bf2090a" id="tgt71" class="tgtSentence">Consulte la documentación de la aplicación para ver las opciones de la línea de comandos pertinentes (como /q) para forzar la instalación silenciosa de la aplicación en los equipos administrados.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="44ef3795f548cae87d4893eb302bf4f4" id="tgt72" class="tgtSentence">Los archivos y las carpetas adicionales que requiera el programa de instalación de la aplicación deben estar disponibles en la ubicación que se especifique para los archivos de instalación de la aplicación.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="cc2194daec0f4b880f9e33dc9642842c" id="tgt73" class="tgtSentence">En la mayoría de los casos, los archivos de Windows Installer (.msi) y de revisión de Windows Installer (.msp) no requieren que <token>wit_nextref</token> instale argumentos de línea de comandos.</caps:sentence>
                            <caps:sentence sentenceid="c55d0ba801164697c9cd60525990cf0c" id="tgt74" class="tgtSentence"> Consulte la documentación de la aplicación.</caps:sentence>
                            <caps:sentence sentenceid="5885d8d42cda9d0630b72b97382a93be" id="tgt75" class="tgtSentence"> Si es necesario especificar argumentos de línea de comandos, deben escribirse como pares nombre=valor (como, por ejemplo, TRANSFORMS=custom_transform.mst).</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="31e4eedb52d0b2870d34c912e2a7d9a5" id="tgt76" class="tgtSentence">Paquete de aplicación de Android (archivo *.apk)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1c707d07c984f57d7eac66639c2039ee" id="tgt77" class="tgtSentence">El paquete de aplicación de Android no está disponible como un tipo de instalador de software hasta que la entidad de administración de dispositivos móviles se establezca en <token>wit_firstref</token>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="3d7d30605a309123a172bc57a6d96f71" id="tgt78" class="tgtSentence">Para obtener más información, consulte <link xlink:href="dbe5cad1-3e0d-41a9-966b-738156089700">Start managing Android devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3458fce4273ca3aede37a7667e3db60c" id="tgt79" class="tgtSentence">Paquete de aplicación iOS (archivo *.ipa)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="b7d91fb6aa3a2b2c7825ba2a11db6d8a" id="tgt80" class="tgtSentence">Para implementar aplicaciones de iOS, deberá disponer de un paquete .ipa válido.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="278ff20eef3b4e99fff1d546e922376b" id="tgt81" class="tgtSentence">El paquete .ipa debe estar firmado por Apple y la fecha de expiración indicada en el perfil de aprovisionamiento sigue siendo válida.</caps:sentence>
                            <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt82" class="tgtSentence">
                              <token>wit_nextref</token> puede distribuir aplicaciones iOS de certificado de empresa.</caps:sentence>
                            <caps:sentence sentenceid="bea3ad18c496624e697e060a87a06256" id="tgt83" class="tgtSentence"> No todas las aplicaciones con certificación de desarrollador de Apple son compatibles.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="6447ec1c571f477fde3a5cfb41f18719" id="tgt84" class="tgtSentence">La empresa debe estar registrada para el programa iOS Developer Enterprise Program.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="cea3034b75389d92d154e42fe41f203f" id="tgt85" class="tgtSentence">Asegúrese de que el servidor de seguridad de la organización permite el acceso a los sitios web de certificación y aprovisionamiento de iOS.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="3d7d30605a309123a172bc57a6d96f71" id="tgt86" class="tgtSentence">Para obtener más información, consulte <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Start managing iOS devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt87" class="tgtSentence">
                          <ui>Paquete de aplicación de Windows Phone (*.xap, .appx, .appxbundle)</ui> </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="32adb8339969d80e176266acf635b1df" id="tgt88" class="tgtSentence">Antes de distribuir un paquete de aplicación de Windows Phone 8 o Windows Phone 8.1, debe configurar <token>wit_firstref</token> como la entidad de administración de dispositivos móviles, configurar los usuarios y obtener un certificado de firma de código móvil empresarial.</caps:sentence>
                        <caps:sentence sentenceid="363ddf43df695c296401df2564573a36" id="tgt89" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Start managing Windows devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2e75600070866fa34fbab2972bd06658" id="tgt90" class="tgtSentence">Paquete de aplicación de Windows (.appx, .appxbundle)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e480126fad1968028c3faac689eb729d" id="tgt91" class="tgtSentence">El paquete appx de Windows para los dispositivos Windows RT y Windows 8.1 inscritos no estará disponible hasta que configure <token>wit_firstref</token> como la entidad de administración de dispositivos móviles y obtenga un certificado de firma de código y las claves de activación de producto de instalación de prueba.</caps:sentence>
                        <caps:sentence sentenceid="363ddf43df695c296401df2564573a36" id="tgt92" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Start managing Windows devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="a15717937e8a885da138c16082b514ee" id="tgt93" class="tgtSentence">A continuación, consulte la siguiente información para obtener detalles acerca de la instalación de aplicaciones de línea de negocio de la Plataforma universal de Windows (UWP) con <token>wit_nextref</token>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2e21651a0d8ef7ae690a63d66525e748" id="tgt94" class="tgtSentence">Windows Installer a través de MDM (*.msi)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="106b2d9f6d94f60ba20593bfb6f555ed" id="tgt95" class="tgtSentence">Este tipo de instalador le permite crear e implementar aplicaciones basadas en Windows Installer para dispositivos inscritos que ejecutan Windows 10.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="817f5127a8770a53b040d345393b3e8f" id="tgt96" class="tgtSentence">Las consideraciones siguientes se aplican cuando se utiliza este tipo de instalador:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="33163536af153e2a63fda53f34fa4b71" id="tgt97" class="tgtSentence">Solo puede cargar un único archivo con la extensión <ui>.msi</ui></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ba5993f53c1819f879ebd720b5556f7c" id="tgt98" class="tgtSentence">El código de producto y la versión del producto del archivo se usan para la detección de la aplicación</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="91e723f076e9d301ca4c41419dd0cbd3" id="tgt99" class="tgtSentence">Se utilizará el comportamiento de reinicio predeterminado de la aplicación.</caps:sentence>
                            <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt100" class="tgtSentence">
                              <token>wit_nextref</token> no controla esto</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="17813f5e979dd66a174c5383a934504e" id="tgt101" class="tgtSentence">Los paquetes MSI por usuario se instalarán para un solo usuario</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="06e5366e529dce40494d4fe632084a39" id="tgt102" class="tgtSentence">Los paquetes MSI por máquina se instalarán para todos los usuarios del dispositivo</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="f1a1b962c55514978e5a3622cea17604" id="tgt103" class="tgtSentence">Actualmente, los paquetes MSI de modo dual solo se instalan para todos los usuarios del dispositivo</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="bce1f39fe955bdd660932213090ffcbb" id="tgt104" class="tgtSentence">Se admiten actualizaciones de aplicaciones cuando el código de producto MSI de cada versión es el mismo</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="e7e6cdaf235b0807da280b2c636df8aa" id="tgt105" class="tgtSentence">Compatibilidad de las aplicaciones de la Plataforma universal de Windows (UWP)</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="37c5a89af08d0eac8a9682637850228d" id="tgt106" class="tgtSentence">Los dispositivos de Windows 10 no necesitan una clave de instalación de prueba para instalar las aplicaciones de línea de negocio.</caps:sentence>
                    <caps:sentence sentenceid="e87d7a6afbb1922cde1ab0004ca3527d" id="tgt107" class="tgtSentence"> Sin embargo, la clave del Registro <ui>HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\Appx\AllowAllTrustedApps</ui> debe tener un valor de <ui>1</ui> para habilitar la instalación de prueba.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="16e412f781e1e49ef3c21cd22161e30c" id="tgt108" class="tgtSentence">Si esta clave del Registro no está configurada, <token>wit_nextref</token> establecerá automáticamente este valor en <ui>1</ui> la primera vez que implemente una aplicación en el dispositivo.</caps:sentence>
                    <caps:sentence sentenceid="9155e5c5f5e7d08e314bd2564b47d939" id="tgt109" class="tgtSentence"> Si estableció este valor en <ui>0</ui>, <token>wit_nextref</token> no podrá cambiar automáticamente el valor y se producirá un error en la implementación de las aplicaciones de línea de negocio.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="6cc02c4590138836a420ad48b6a353fa" id="tgt110" class="tgtSentence">Debe firmar las aplicaciones de línea de negocio de la Plataforma universal de Windows con un certificado de firma de código de confianza en cada dispositivo en el que implemente la aplicación.</caps:sentence>
                    <caps:sentence sentenceid="8c5a521169a9e7f4e4a59c1ba9c1ebc3" id="tgt111" class="tgtSentence"> Puede usar certificados de una infraestructura PKI interna o un certificado procedente de un certificado raíz público de terceros instalado en el dispositivo.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="051af9985b2b8e3e8c526087cf2dea5a" id="tgt112" class="tgtSentence">En los dispositivos de Windows 10 Mobile, puede usar un certificado de firma de código que no sea Symantec para firmar aplicaciones universales con extensión <ui>.appx</ui>.</caps:sentence>
                    <caps:sentence sentenceid="dbbd05c1a8c9f3f04c246c67d767f49c" id="tgt113" class="tgtSentence"> En cuanto a aplicaciones <ui>.xap</ui> y paquetes <ui>.appx</ui> compilados para Windows Phone 8.1 que desee instalar en dispositivos de Windows 10 Mobile, debe usar un certificado de firma de código de Symantec.</caps:sentence>
                  </para>
                </content>
              </section>
            </sections>
          </section>
          <section DoNotNumber="false" address="BKMK_ExternalLinks">
            <title>
              <caps:sentence sentenceid="82436e593a1946d9fbc85921c230ad07" id="tgt114" class="tgtSentence">Vínculo externo</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt115" class="tgtSentence">Utilice el tipo de instalación <ui>Vínculo externo</ui> cuando tenga: </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ba0efeaaebac5c9fb9255157e58ef299" id="tgt116" class="tgtSentence">
                      <embeddedLabel>Dirección URL</embeddedLabel> que permite a los usuarios descargar una aplicación de la tienda en línea.</caps:sentence>
                    <caps:sentence sentenceid="532694675a27b6929e773a783acc3899" id="tgt117" class="tgtSentence"> Este tipo de instalación es compatible con las siguientes plataformas de dispositivos:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8812037b6ece7fcb9c7da9f16f9485c5" id="tgt118" class="tgtSentence">Windows 8 y versiones posteriores</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt119" class="tgtSentence">Windows RT</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="edf26a253b14faa8f27aa839c9119b62" id="tgt120" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt121" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b39f32f5a7eb4d500a97c874db57f363" id="tgt122" class="tgtSentence">Dispositivos Android</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="51b6206c358c82b7e934c2cfcbedd666" id="tgt123" class="tgtSentence">
                      <embeddedLabel>Vínculo</embeddedLabel> a una aplicación basada en web que se ejecuta desde el explorador web.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="d8e6a17aa159e25da46f8b70fd6bc7cc" id="tgt124" class="tgtSentence">Este tipo de instalación está disponible para todos los dispositivos compatibles con <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="f4d68728f8c1a94a269a3633637edad9" id="tgt125" class="tgtSentence">Los vínculos externos se ponen a disposición de los usuarios a través del <token>wit_iwportal_1</token>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="f84d42f82b605aba4cbf6bdfb85184e3" id="tgt126" class="tgtSentence">Aplicación iOS administrada desde la tienda de aplicaciones</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt127" class="tgtSentence">Use el tipo de instalación <ui>Aplicación iOS administrada desde la tienda de aplicaciones</ui> para administrar e implementar aplicaciones iOS gratuitas desde la tienda de aplicaciones iOS.</caps:sentence>
                <caps:sentence sentenceid="59528d8e4efec6421b2e0db817418db3" id="tgt128" class="tgtSentence"> Puede implementar este tipo de instalador como una instalación necesaria de modo que sea obligatorio en los dispositivos administrados (esto también hace que esté disponible para instalarlo desde el portal web móvil) o implementarlo como disponible para que los usuarios puedan descargarlo desde el portal web móvil.</caps:sentence>
                <caps:sentence sentenceid="21dd8341494488c724047bd359991467" id="tgt129" class="tgtSentence"> También puede asociar directivas de administración de aplicaciones móviles a aplicaciones compatibles y revisar su estado en la consola del administrador.</caps:sentence>
                <caps:sentence sentenceid="40e372de3bc25a6905bff64c94e46c3c" id="tgt130" class="tgtSentence"> Las aplicaciones iOS administradas no se almacenan en su espacio de almacenamiento en la nube de <token>wit_nextref</token>.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_SoftwareDistProcess">
        <title>
          <caps:sentence sentenceid="e7536b14c450b31fbdc53467941e3388" id="tgt131" class="tgtSentence">Proceso general de implementación de aplicaciones</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="12e63e5f0530294b949957387f4db078" id="tgt132" class="tgtSentence">En esta sección se resume el proceso de implementación de aplicaciones en <token>wit_nextref</token>.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2764ca9d34e90313978d044f27ae433b" id="tgt133" class="tgtSentence">Paso</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt134" class="tgtSentence">Más información</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c7e1b43906c3ed0eff3c8ace8fb54ee3" id="tgt135" class="tgtSentence">Asegúrese de que la aplicación que quiere implementar sea compatible con <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa">Prepare for app deployment with Microsoft Intune</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f6dc9e35aa2d43f423d9831797e891a8" id="tgt136" class="tgtSentence">Cree grupos de usuarios o dispositivos en los que pueda implementar la aplicación.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b5d7e1d957e7b9fdc8ad3e07775a9202" id="tgt137" class="tgtSentence">Publique la aplicación en el almacenamiento en nube de <token>wit_firstref</token>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a#BKMK_PublishSoftware">Publish mobile device apps to Microsoft Intune cloud storage</link>
                  </para>
                  <para>
                    <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb#BKMK_PublishSoftware">Publish computer apps to Microsoft Intune cloud storage</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0e081e2e9f7aa73387c39a03bb311bbb" id="tgt138" class="tgtSentence">Implemente la aplicación en los dispositivos móviles o equipos mediante la acción de implementación que necesite.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy apps to mobile devices in Microsoft Intune</link>
                  </para>
                  <para>
                    <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb">Deploy apps to computers in Microsoft Intune</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="99a5e5124cca296d1e07e3d885e4334e" id="tgt139" class="tgtSentence">Supervise la implementación de la aplicación.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a#BKMK_MonitorSoftware">Monitor mobile device apps</link>
                  </para>
                  <para>
                    <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb#BKMK_MonitorSoftware">Monitor computer apps</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_Depl">
        <title>
          <caps:sentence sentenceid="f85b04da86bdaecd1458211122248894" id="tgt140" class="tgtSentence">Comprender las acciones de implementación de aplicaciones</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a431db78448faa12912845ff45e82055" id="tgt141" class="tgtSentence">Al implementar aplicaciones, puede elegir una de las siguientes acciones de implementación:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="92e3a11f0acf2d4778bf57a321047d95" id="tgt142" class="tgtSentence">
                  <ui>Instalación requerida</ui>: la aplicación se instala en el dispositivo sin necesitar la intervención del usuario final.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="2abf0f9d684bcd12ac6ac1b55c3778d7" id="tgt143" class="tgtSentence">En el caso de dispositivos iOS que no están en modo supervisado, el usuario debe aceptar la oferta de la aplicación antes de instalarla.</caps:sentence>
                  <caps:sentence sentenceid="1fbea3ac2605eda68966299db13d8b97" id="tgt144" class="tgtSentence">  Para obtener información acerca del uso del <externalLink><linkText>modo supervisado</linkText><linkUri>http://support.apple.com/en-is/HT202837</linkUri></externalLink> en Microsoft Intune, consulte <link xlink:href="ab46be6c-ab73-4c99-8492-66d1dd418293">Manage devices using configuration policies with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="568e36c126a2c0c1e62142b882c48ad4" id="tgt145" class="tgtSentence">Ya no podrá crear nuevas implementaciones de aplicaciones para dispositivos que ejecuten sistemas operativos anteriores a iOS 7.1.</caps:sentence>
                  <caps:sentence sentenceid="07bf3fb7c558107d75b4c18c76fef1f1" id="tgt146" class="tgtSentence"> Cualquier implementación de aplicaciones que se realicen en dispositivos que ejecuten un sistema operativo anterior a iOS 7.1, seguirán funcionando y <token>wit_nextref</token> se encargará de administrarlas.</caps:sentence>
                </para>
              </alert>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="bca8334f5305478f1d7c836304deb7ac" id="tgt147" class="tgtSentence">Para dispositivos Android, el usuario debe aceptar la oferta de la aplicación antes de instalarla.</caps:sentence>
                </para>
              </alert>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7095c6ddf7d2583ea242351e9cdc4900" id="tgt148" class="tgtSentence">
                  <ui>Instalación disponible</ui>: la aplicación aparece en el portal de empresa y los usuarios finales pueden solicitar instalarla.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="fba975997c04ddcc3fc1f06c34790586" id="tgt149" class="tgtSentence">
                  <ui>Desinstalar</ui>: la aplicación se desinstala del dispositivo.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9742f73403bea008a89a959341ead031" id="tgt150" class="tgtSentence">
                  <ui>No aplicable</ui> : la aplicación no aparece en el portal de empresa y no está instalada en los dispositivos.</caps:sentence>
              </para>
            </listItem>
          </list>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="34a6e5d64ade17ef4e51612c50dd72f5" id="tgt151" class="tgtSentence">Plataforma</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b00818793fbc05a7dc67248ad038e3f9" id="tgt152" class="tgtSentence">Instalación requerida</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e6548c0b4c88797fe8d9644ab63190c5" id="tgt153" class="tgtSentence">Instalación disponible</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fe98497efedbe156ecc4b953aea77e07" id="tgt154" class="tgtSentence">Desinstalar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4b99c13013f59eb4aa6fc87d531d9c24" id="tgt155" class="tgtSentence">No aplicable</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ceafbd0831b407d74e2be4d8d6640d16" id="tgt156" class="tgtSentence">Paquete de aplicación de Windows (implementado para un grupo de usuarios)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt157" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt158" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt159" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt160" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ed39e48495d189c8983cc235a7bc83fb" id="tgt161" class="tgtSentence">Paquete de aplicación de Windows (se implementa para un grupo de dispositivos)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt162" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt163" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt164" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt165" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3b15b94854e4f0b4a00cff6741118e70" id="tgt166" class="tgtSentence">Paquete de aplicación para dispositivos móviles (se implementa para un grupo de usuarios)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt167" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt168" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt169" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt170" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5f9a2d2b935d3f9d5012303f28e0e378" id="tgt171" class="tgtSentence">Paquete de aplicación para dispositivos móviles (se implementa para un grupo de dispositivos)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt172" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt173" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt174" class="tgtSentence">Sí</caps:sentence>
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
                    <caps:sentence sentenceid="d0fec2ae17bb59dc1c8be4a6cbc25080" id="tgt176" class="tgtSentence">Windows Installer (se implementa para un grupo de usuarios)</caps:sentence>
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
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt179" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt180" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ca0f5345b71e0f383cf114f5a2c6e97f" id="tgt181" class="tgtSentence">Windows Installer (se implementa para un grupo de dispositivos)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt182" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt183" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt184" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt185" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ec63a18217df9fd63a00f8697fbff788" id="tgt186" class="tgtSentence">Vínculo externo (se implementa para un grupo de usuarios)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt187" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt188" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt189" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt190" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7157546357da3dad8869e188f7040e5a" id="tgt191" class="tgtSentence">Vínculo externo (se implementa para un grupo de dispositivos)</caps:sentence>
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
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt194" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt195" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="18196fa0d00693627f1d0ed4434a5789" id="tgt196" class="tgtSentence">Aplicación iOS administrada desde la tienda de aplicaciones (se implementa para un grupo de usuarios)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt197" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt198" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt199" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt200" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="dfbd4ad3018f684d5dfc5fa097526071" id="tgt201" class="tgtSentence">Aplicación iOS administrada desde la tienda de aplicaciones (se implementa para un grupo de dispositivos)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt202" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt203" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt204" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt205" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="22078e907d4db2f51e9f54df6e3440db" id="tgt206" class="tgtSentence">Cuando un dispositivo recibe dos implementaciones, con la misma acción de implementación, se aplican las siguientes reglas:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="6b7401e3290bc8036fbc56f993072e6c" id="tgt207" class="tgtSentence">Las implementaciones para un grupo de dispositivos tienen prioridad sobre las implementaciones para un grupo de usuarios.</caps:sentence>
                <caps:sentence sentenceid="450e09e0efb99f0f418e5ed33ed02b16" id="tgt208" class="tgtSentence"> Sin embargo, si una aplicación se implementa para un grupo de usuarios con la acción de implementación <ui>Disponible</ui> y la misma aplicación se implementa también para un grupo de dispositivos con la acción de implementación <ui>No aplicable</ui>, la aplicación estará disponible en el portal de la compañía para que los usuarios la instalen.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9608d9d77d70e0921fcaed2d0d111198" id="tgt209" class="tgtSentence">El intento de la administración de TI tiene prioridad sobre el usuario final.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="730f667633059ed243d1d03dc1dc5a2e" id="tgt210" class="tgtSentence">Las acciones de instalación tienen prioridad sobre las acciones de desinstalación.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b4759ba3c3a55bb3ceaa5a1b0e24b065" id="tgt211" class="tgtSentence">Si un dispositivo recibe una instalación requerida y una instalación disponible, ambas acciones se combinan (la aplicación es necesaria y está disponible).</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5b49d81d-8a28-4d78-a21b-6614920a7b82">Provision and configure apps with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Before you manage and deploy apps in <token>wit_firstref</token>, use the information in this section to learn about:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_SoftwareWorkspace">The App workspace</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_SoftwarePublisher">Microsoft Intune Software Publisher</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_OSRequirements">Operating system requirements</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_Types">Software installation types</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_SoftwareDistProcess">General app distribution process</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa#BKMK_Depl">Understand app distribution actions</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section DoNotNumber="false" address="BKMK_SoftwareWorkspace">
        <title>
          <caps:sentence id="src2" class="srcSentence">The Apps workspace</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">The <ui>Apps</ui> workspace in the <token>wit_adminconsole</token> provides information about detected and managed apps.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The following pages are available:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">Apps workspace page</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">Details</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src7" class="srcSentence">Overview</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Lists app deployment alerts and the current status of your cloud storage.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src9" class="srcSentence">Detected Software</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Shows the software inventory data that <token>wit_firstref</token> detects on managed computers.</caps:sentence>
                    <caps:sentence id="src11" class="srcSentence"> Software inventory is only available for computers.</caps:sentence>
                    <caps:sentence id="src12" class="srcSentence"> Therefore, <token>wit_nextref</token> does not detect or list apps for managed mobile devices.</caps:sentence>
                    <caps:sentence id="src13" class="srcSentence"> You can perform the following tasks from the <ui>Detected Software</ui> workspace:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">View app properties</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src15" class="srcSentence">Add license agreements for detected software</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src16" class="srcSentence">Apps</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">The <ui>Apps</ui> page is where the apps that you want to deploy to your managed computers and mobile devices is uploaded, deployed, and managed on an ongoing basis.</caps:sentence>
                    <caps:sentence id="src18" class="srcSentence"> You can perform the following tasks:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src19" class="srcSentence">View and modify app properties</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">Add license agreements to managed apps</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src21" class="srcSentence">Manage app deployments</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">Add new apps</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src23" class="srcSentence">Edit the properties of managed apps</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src24" class="srcSentence">Delete apps</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section DoNotNumber="false" address="BKMK_SoftwarePublisher">
        <title>
          <caps:sentence id="src25" class="srcSentence">Microsoft Intune Software Publisher</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src26" class="srcSentence">The <ui>Microsoft Intune Software Publisher</ui> starts when you add or modify apps from the <token>wit_adminconsole</token>.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> From the publisher, you select a software installer type that will either upload apps (programs for computers or apps for mobile devices) to be stored in <token>wit_nextref</token> cloud storage, or link to an online store or web application.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_PublisherRequirements">
            <title>
              <caps:sentence id="src28" class="srcSentence">Microsoft Intune Software Publisher requirements</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src29" class="srcSentence">Before you begin to use the <token>wit_firstref</token> Software Publisher, you must install the full version of Microsoft .NET Framework 4.0.</caps:sentence>
                <caps:sentence id="src30" class="srcSentence"> After you install the .NET Framework, you might have to restart your computer before the <token>wit_firstref</token> Software Publisher will open correctly.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence"> For details, see <externalLink><linkText>Microsoft .NET Framework 4 (Web Installer)</linkText><linkUri>http://www.microsoft.com/download/details.aspx?id=17851</linkUri></externalLink>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_CloudStorage">
            <title>
              <caps:sentence id="src32" class="srcSentence">Cloud storage requirements</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src33" class="srcSentence">All apps that you deploy must be packaged and uploaded to <token>wit_firstref</token> cloud storage.</caps:sentence>
                <caps:sentence id="src34" class="srcSentence"> Before you deploy apps, make sure there is enough storage space available to upload the app.</caps:sentence>
                <caps:sentence id="src35" class="srcSentence"> A trial subscription of <token>wit_nextref</token> includes 2 gigabytes (GB) of cloud-based storage that is used to store managed apps and updates.</caps:sentence>
                <caps:sentence id="src36" class="srcSentence"> A paid subscription includes 20GB, with the option to purchase additional storage space at 1GB increments by using the <token>wit_firstref</token> Extra Storage Add-on.</caps:sentence>
                <caps:sentence id="src37" class="srcSentence"> The following rules apply to purchasing additional cloud-based storage for <token>wit_nextref</token>:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">You cannot purchase additional storage during any <token>wit_nextref</token> pre-release or trial period.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">You must have an active paid subscription in order to purchase additional storage.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Only billing administrators or global administrators for your Microsoft Online Service can purchase additional storage through the <token>wit_nextref</token> account portal.</caps:sentence>
                    <caps:sentence id="src41" class="srcSentence"> To add, delete, or manage these administrators, you must be a global administrator and sign in to the <token>wit_nextref</token> account portal.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">If you are a volume licensing customer who has purchased <token>wit_nextref</token> or the <token>wit_firstref</token> Add-on through the enterprise agreement, contact your Microsoft Account Manager or Microsoft Partner for pricing information and to purchase additional storage.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src43" class="srcSentence">To purchase additional storage</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">In the <externalLink><linkText>Microsoft Intune account portal</linkText><linkUri>https://account.manage.microsoft.com</linkUri></externalLink>, in the left pane under <ui>Subscriptions</ui>, click <ui>Manage</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">On the <ui>Billing and subscription management</ui> page, click the <token>wit_nextref</token> subscription for which you want to purchase additional storage.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">On the <ui>Subscription details</ui> page, by <ui>Optional add-ons</ui>, click <ui>Add more</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src47" class="srcSentence">On the <ui>Select number of licenses</ui> page, under <ui>Optional add-ons</ui>, enter the additional number of GB of storage that you want to buy for the Microsoft Intune Extra Storage add-on.</caps:sentence>
                        <caps:sentence id="src48" class="srcSentence"> For example, if you currently have 20 GB, and you want to add another 10 GB, enter 10.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">On the <ui>Review important information</ui> page, review the order summary information, and if it is correct, click <ui>Place order</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">The <ui>Order confirmation page</ui> opens to display the order details.</caps:sentence>
                        <caps:sentence id="src51" class="srcSentence"> Click <ui>Finish</ui> to complete the process.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section DoNotNumber="false" address="BKMK_OSRequirements">
        <title>
          <caps:sentence id="src52" class="srcSentence">Operating system requirements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src53" class="srcSentence">Mobile devices and computers must run a supported operating system to install apps that you deploy by using <token>wit_nextref</token>.</caps:sentence>
          </para>
          <para>
            <embeddedLabel>
              <caps:sentence id="src54" class="srcSentence">Mobile devices</caps:sentence>
            </embeddedLabel>
          </para>
          <para>
            <caps:sentence id="src55" class="srcSentence">For the complete list of supported operating systems for mobile devices, see <link xlink:href="f23b3ee7-78da-4e53-9fc2-78e58401bcf9">Mobile device management capabilities in Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <embeddedLabel>
              <caps:sentence id="src56" class="srcSentence">Computers</caps:sentence>
            </embeddedLabel>
          </para>
          <para>
            <caps:sentence id="src57" class="srcSentence">For the complete list of supported operating systems for managed computers, see <link xlink:href="77fa5c66-a87c-47df-964c-800eea509b33">Computer management capabilities in Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section address="BKMK_Types">
        <title>
          <caps:sentence id="src58" class="srcSentence">Software installation types</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src59" class="srcSentence">
              <token>wit_nextref</token> lets you deploy the following software installation types:</caps:sentence>
          </para>
        </content>
        <sections>
          <section DoNotNumber="false" address="BKMK_SoftwareInstallers">
            <title>
              <caps:sentence id="src60" class="srcSentence">Software Installer</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src61" class="srcSentence">Use the <ui>Software Installer</ui> installation type to:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">Upload a signed app package to Microsoft Intune cloud storage and make the app available to users through the <token>wit_iwportal_1</token>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">Upload apps that will be deployed to computers that run the <token>wit_nextref</token> computer client.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">Install apps on managed mobile devices from an installation file, bypassing the app store (known as side loading).</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src65" class="srcSentence">Use the following table to help you understand the different software installer file types:</caps:sentence>
              </para>
              <table>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <legacyBold>
                          <caps:sentence id="src66" class="srcSentence">Software installer type</caps:sentence>
                        </legacyBold>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <legacyBold>
                          <caps:sentence id="src67" class="srcSentence">Requirements</caps:sentence>
                        </legacyBold>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src68" class="srcSentence">Windows Installer (*.exe, *.msi)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src69" class="srcSentence">The Windows Installer files must support silent installation, that is, without requiring user intervention.</caps:sentence>
                            <caps:sentence id="src70" class="srcSentence"> If your app uses any other type of Setup file, or requires user interaction during setup, that app cannot be installed by using <token>wit_nextref</token>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src71" class="srcSentence">Refer to your app documentation to find the relevant command-line options, such as /q, to force the app to install silently on the managed computers.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src72" class="srcSentence">Any additional files and folders that are required by the app’s setup program must be available from the location that you specify for the app setup files.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src73" class="srcSentence">In most cases, Windows Installer (.msi) and Windows Installer Patch (.msp) files do not require any command-line arguments to be installed by <token>wit_nextref</token>.</caps:sentence>
                            <caps:sentence id="src74" class="srcSentence"> Check your app documentation.</caps:sentence>
                            <caps:sentence id="src75" class="srcSentence"> If command-line arguments are required, they must be entered as Name=Value pairs (such as TRANSFORMS=custom_transform.mst).</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src76" class="srcSentence">App Package for Android (*.apk file)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src77" class="srcSentence">The App Package for Android is not available as a software installer type until you set the Mobile Device Management Authority to <token>wit_firstref</token>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src78" class="srcSentence">For details, see <link xlink:href="dbe5cad1-3e0d-41a9-966b-738156089700">Start managing Android devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src79" class="srcSentence">App Package for iOS (*.ipa file)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src80" class="srcSentence">To deploy iOS apps, you must have a valid .ipa package</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src81" class="srcSentence">The .ipa package must be signed by Apple and the expiration date indicated in the provisioning profile is still valid.</caps:sentence>
                            <caps:sentence id="src82" class="srcSentence">
                              <token>wit_nextref</token> can distribute enterprise certificate iOS applications.</caps:sentence>
                            <caps:sentence id="src83" class="srcSentence"> Not all Apple developer certificate apps are supported.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src84" class="srcSentence">Your enterprise must be registered for the iOS Developer Enterprise Program.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src85" class="srcSentence">Make sure that your organization’s firewall allows access to the iOS provisioning and certification web sites.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">For details, see <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Start managing iOS devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">
                          <ui>Windows Phone app package (*.xap, .appx, .appxbundle)</ui> </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">Before you distribute a Windows Phone 8 or Windows Phone 8.1 app package, you must set the mobile device management authority to <token>wit_firstref</token>, set up users, and obtain an enterprise mobile code-signing certificate.</caps:sentence>
                        <caps:sentence id="src89" class="srcSentence"> For details, see <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Start managing Windows devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src90" class="srcSentence">Windows app package (.appx, .appxbundle)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src91" class="srcSentence">The Windows appx package for Windows RT and enrolled Windows 8.1 devices is not available until you set the mobile device management authority to <token>wit_firstref</token>, provision users, obtain a code-signing certificate, and sideloading product activation keys.</caps:sentence>
                        <caps:sentence id="src92" class="srcSentence"> For details, see <link xlink:href="61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f">Start managing Windows devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src93" class="srcSentence">See below for information about installing line of business Universal Windows Platform (UWP) apps with <token>wit_nextref</token>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src94" class="srcSentence">Windows Installer through MDM (*.msi)</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">This installer type lets you create and deploy Windows Installer based apps to enrolled devices that run Windows 10.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src96" class="srcSentence">The following considerations apply when you use this installer type:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src97" class="srcSentence">You can only upload a single file with the extension <ui>.msi</ui></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src98" class="srcSentence">The file's product code and product version are used for app detection</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src99" class="srcSentence">The default restart behavior of the app will be used.</caps:sentence>
                            <caps:sentence id="src100" class="srcSentence">
                              <token>wit_nextref</token> does not control this</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src101" class="srcSentence">Per user MSI packages will be installed for a single user</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src102" class="srcSentence">Per machine MSI packages will be installed for all users on the device</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src103" class="srcSentence">Dual mode MSI packages currently only install for all users on the device</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src104" class="srcSentence">App updates are supported when the MSI product code of each version is the same</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src105" class="srcSentence">Support for Universal Windows Platform (UWP) apps</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">Windows 10 devices do not require a sideloading key to install line of business apps.</caps:sentence>
                    <caps:sentence id="src107" class="srcSentence"> However, the registry key <ui>HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\Appx\AllowAllTrustedApps</ui> must have a value of to <ui>1</ui> to enable sideloading.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src108" class="srcSentence">If this registry key is not configured, <token>wit_nextref</token> will automatically set this value to <ui>1</ui> the first time you deploy an app to the device.</caps:sentence>
                    <caps:sentence id="src109" class="srcSentence"> If you have set this value to <ui>0</ui>, then <token>wit_nextref</token> cannot automatically change the value, and the deployment of line of business apps will fail.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">Universal Windows Platform line of business apps must be signed with a code-signing certificate that is trusted on each device to which the app is deployed.</caps:sentence>
                    <caps:sentence id="src111" class="srcSentence"> You can use certificates from an in-house PKI infrastructure, or a certificate from a third-party public root certificate installed on the device.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">On Windows 10 Mobile devices, you can use a non-Symantec code signing certificate to sign universal <ui>.appx</ui> apps.</caps:sentence>
                    <caps:sentence id="src113" class="srcSentence"> For <ui>.xap</ui> apps, and also <ui>.appx</ui> packages built for Windows Phone 8.1 that you want to install on Windows 10 Mobile devices, you must use a Symantec code-signing certificate.</caps:sentence>
                  </para>
                </content>
              </section>
            </sections>
          </section>
          <section DoNotNumber="false" address="BKMK_ExternalLinks">
            <title>
              <caps:sentence id="src114" class="srcSentence">External Link</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src115" class="srcSentence">Use the <ui>External Link</ui> installation type when you have a: </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">
                      <embeddedLabel>URL</embeddedLabel> that lets users download an app from the online store.</caps:sentence>
                    <caps:sentence id="src117" class="srcSentence"> This installation type is supported by the following device platforms:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src118" class="srcSentence">Windows 8 and later</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">Windows RT</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src121" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src122" class="srcSentence">Android devices</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src123" class="srcSentence">
                      <embeddedLabel>Link</embeddedLabel> to a web-based app that runs from the web browser.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src124" class="srcSentence">This installation type is available to all devices supported by <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src125" class="srcSentence">External links are made available to users through the <token>wit_iwportal_1</token>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src126" class="srcSentence">Managed iOS app from the app store</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src127" class="srcSentence">Use the <ui>Managed iOS app from the app store</ui> installation type to manage and deploy iOS apps that are free of charge from the iOS app store.</caps:sentence>
                <caps:sentence id="src128" class="srcSentence"> You can deploy this installer type as a required install to make it mandatory on managed devices (which also makes it available to install from the mobile web portal), or deploy it as available to let users download it from the mobile web portal.</caps:sentence>
                <caps:sentence id="src129" class="srcSentence"> You can also associate mobile application management policies with compatible apps and review their status in the administrator console.</caps:sentence>
                <caps:sentence id="src130" class="srcSentence"> Managed iOS apps are not stored in your <token>wit_nextref</token> cloud storage space.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_SoftwareDistProcess">
        <title>
          <caps:sentence id="src131" class="srcSentence">General app deployment process</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src132" class="srcSentence">This section provides an overview of the app deployment process in <token>wit_nextref</token>.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src133" class="srcSentence">Step</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src134" class="srcSentence">More information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src135" class="srcSentence">Ensure that the app you want to deploy is supported by <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="2b770f4f-6d36-41e4-b535-514b46e29aaa">Prepare for app deployment with Microsoft Intune</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">Create groups of users or devices to which you can deploy the app.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src137" class="srcSentence">Publish the app to <token>wit_firstref</token> cloud storage.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a#BKMK_PublishSoftware">Publish mobile device apps to Microsoft Intune cloud storage</link>
                  </para>
                  <para>
                    <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb#BKMK_PublishSoftware">Publish computer apps to Microsoft Intune cloud storage</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src138" class="srcSentence">Deploy the app to mobile devices or computers using the deployment action you require.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy apps to mobile devices in Microsoft Intune</link>
                  </para>
                  <para>
                    <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb">Deploy apps to computers in Microsoft Intune</link>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src139" class="srcSentence">Monitor the app deployment.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a#BKMK_MonitorSoftware">Monitor mobile device apps</link>
                  </para>
                  <para>
                    <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb#BKMK_MonitorSoftware">Monitor computer apps</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_Depl">
        <title>
          <caps:sentence id="src140" class="srcSentence">Understand app deployment actions</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src141" class="srcSentence">When you deploy apps, you can choose from one of the following deployment actions:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src142" class="srcSentence">
                  <ui>Required install</ui> – The app is installed onto the device, with no end-user intervention required.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src143" class="srcSentence">For iOS devices that are not in supervised mode, the user must accept the app offer before it is installed.</caps:sentence>
                  <caps:sentence id="src144" class="srcSentence">  For information about using <externalLink><linkText>supervised mode</linkText><linkUri>http://support.apple.com/en-is/HT202837</linkUri></externalLink> in Microsoft Intune, see <link xlink:href="ab46be6c-ab73-4c99-8492-66d1dd418293">Manage devices using configuration policies with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src145" class="srcSentence">You can no longer create new app deployments to iOS devices running an operating system earlier than iOS 7.1.</caps:sentence>
                  <caps:sentence id="src146" class="srcSentence"> Any existing app deployments to devices running an earlier operating system than iOS 7.1 will continue to work and be managed by <token>wit_nextref</token>.</caps:sentence>
                </para>
              </alert>
              <alert class="note">
                <para>
                  <caps:sentence id="src147" class="srcSentence">For Android devices, the user must accept the app offer before it is installed.</caps:sentence>
                </para>
              </alert>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src148" class="srcSentence">
                  <ui>Available install</ui> – The app is displayed in the company portal, and end-users can install it on-demand.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src149" class="srcSentence">
                  <ui>Uninstall</ui> – The app is uninstalled from the device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src150" class="srcSentence">
                  <ui>Not applicable</ui> – The app is not displayed in the company portal, and is not installed to any devices.</caps:sentence>
              </para>
            </listItem>
          </list>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">Platform</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">Required install</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">Available install</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">Uninstall</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src155" class="srcSentence">Not applicable</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">Windows app package (deployed to a user group)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src158" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src161" class="srcSentence">Windows app package (deployed to a device group</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src164" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src165" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src166" class="srcSentence">App package for mobile devices (deployed to a user group)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src168" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src170" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">App package for mobile devices (deployed to a device group)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src173" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src174" class="srcSentence">Yes</caps:sentence>
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
                    <caps:sentence id="src176" class="srcSentence">Windows Installer (deployed to a user group)</caps:sentence>
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
                <TD>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src181" class="srcSentence">Windows Installer (deployed to a device group)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src185" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">External link (deployed to a user group)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src188" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src189" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src190" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">External link (deployed to a device group)</caps:sentence>
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
                <TD>
                  <para>
                    <caps:sentence id="src194" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src196" class="srcSentence">Managed iOS app from the app store (deployed to a user group)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src197" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src198" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src199" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src201" class="srcSentence">Managed iOS app from the app store (deployed to a device group)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src202" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src203" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src204" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src205" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src206" class="srcSentence">When two deployments, with the same deployment action are received by a device, the following rules apply:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src207" class="srcSentence">Deployments to a device group take precedence over deployments to a user group.</caps:sentence>
                <caps:sentence id="src208" class="srcSentence"> However, if an app is deployed to a user group with a deployment action of <ui>Available</ui> and the same app is also deployed to a device group with a deployment action of <ui>Not Applicable</ui>, the app will be made available in the company portal for users to install.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src209" class="srcSentence">The intent of the IT admin takes precedence over the end-user.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src210" class="srcSentence">An install actions takes precedence over an uninstall action.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src211" class="srcSentence">If both a required install and an available install are received by a device, the actions are combined (the app is both required and available).</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5b49d81d-8a28-4d78-a21b-6614920a7b82">Provision and configure apps with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>