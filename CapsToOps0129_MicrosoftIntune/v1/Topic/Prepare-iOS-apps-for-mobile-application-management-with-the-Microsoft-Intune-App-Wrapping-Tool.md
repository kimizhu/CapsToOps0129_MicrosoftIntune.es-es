---
title: Preparar aplicaciones iOS para la administraci&#243;n de aplicaciones m&#243;viles con la herramienta de ajuste de aplicaciones de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 99ab0369-5115-4dc8-83ea-db7239b0de97
---
# Preparar aplicaciones iOS para la administraci&#243;n de aplicaciones m&#243;viles con la herramienta de ajuste de aplicaciones de Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt1" class="tgtSentence">Use la <ui>herramienta de ajuste de aplicaciones de Microsoft Intune para iOS</ui> para modificar el comportamiento de las aplicaciones iOS internas; para ello, debe restringir las características de la aplicación sin modificar el código de la propia aplicación.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="dc633f2e865a01a976901fc6d4971c68" id="tgt2" class="tgtSentence">La herramienta es una aplicación de línea de comandos de Mac OS que crea un "contenedor" alrededor de una aplicación.</caps:sentence>
          <caps:sentence sentenceid="ba9c1c59ff656bd7c1dd8ced5ef99daf" id="tgt3" class="tgtSentence"> Una vez que se procesa una aplicación, puede cambiar la funcionalidad de aplicaciones con una directiva de administración de aplicaciones móviles <token>wit_nextref</token> que configure (consulte <link xlink:href="b4fb33a8-a2fa-4353-bd89-5bda48b68e83">Help secure apps using mobile application management policies with Windows Intune</link>).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="de282e954762c9ce6db405fbb4361a62" id="tgt4" class="tgtSentence">Para descargar la herramienta, consulte <externalLink><linkText>Herramienta de ajuste de aplicaciones de Microsoft Intune para iOS</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=45218</linkUri></externalLink>.</caps:sentence>
        </para>
      </introduction>
      <section address="BKMK_Prereq" expanded="true">
        <title>
          <caps:sentence sentenceid="20b5a1df0a4cc8104c2c22808ae4acb7" id="tgt5" class="tgtSentence">Paso 1: cumplir los requisitos previos para usar la herramienta de ajuste de aplicaciones</caps:sentence>
        </title>
        <content>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ba12fb48e2d23bb2bd2819f64d02ec7e" id="tgt6" class="tgtSentence">Requisito</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b1980bff27a9e4538350c98c81f0ce9c" id="tgt7" class="tgtSentence">Detalles y más información</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6ef98978f9f07925d9c609699e1847cf" id="tgt8" class="tgtSentence">Sistema operativo y conjunto de herramientas admitidos</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a43db0183898022e707a477c1406968" id="tgt9" class="tgtSentence">Debe ejecutar la herramienta de ajuste de aplicaciones en un equipo Mac que ejecute OS X 10.8.5 o posterior que tenga instalada la versión 5 o posterior del conjunto de herramientas XCode.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para></para>
                  <para>
                    <caps:sentence sentenceid="7eaf1d9127a37255507c942bb20af7a6" id="tgt10" class="tgtSentence">Certificado de firma y perfil de aprovisionamiento</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1979232272f74570419bfd45e7cc0f7d" id="tgt11" class="tgtSentence">Debe poseer un perfil de aprovisionamiento y un certificado de firma de Apple.</caps:sentence>
                    <caps:sentence sentenceid="ea2b567f5829abdf92a86da3ebf1a2c6" id="tgt12" class="tgtSentence"> Para obtener más información, consulte la <externalLink><linkText>documentación para desarrolladores de Apple</linkText><linkUri>https://developer.apple.com/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e7076904ecb6a5598fbfcef68ce0f68b" id="tgt13" class="tgtSentence">Procesamiento de una aplicación con la herramienta de ajuste de aplicaciones</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="73fa29024c5e5d9e6e82e299e1e10b19" id="tgt14" class="tgtSentence">Para procesar una aplicación con la herramienta de ajuste de aplicaciones:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="6cb62d6b9f8240aefa0adaf77068fd7b" id="tgt15" class="tgtSentence">Las aplicaciones deben estar desarrolladas y firmadas por la compañía o por un fabricante de software independientes (ISV).</caps:sentence>
                        <caps:sentence sentenceid="8c45a4ec71b98b35db5c903b534b1938" id="tgt16" class="tgtSentence"> No se puede usar esta herramienta para procesar aplicaciones de la tienda de Apple.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="df90f52984b5e8e86cb8c7770f9c5aef" id="tgt17" class="tgtSentence">La aplicación debe escribirse para iOS 7.0 o una versión posterior.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f931b41541a2688dee3b0e3dc87e4e7c" id="tgt18" class="tgtSentence">Las aplicaciones deben tener el formato ejecutable independiente de la posición (PIE).</caps:sentence>
                        <caps:sentence sentenceid="04b3856d195851de362aa649c44eb4e4" id="tgt19" class="tgtSentence"> Para obtener más información acerca del formato PIE, consulte la documentación para desarrolladores de Apple.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="398fa4356a8ecb24067c2f00a518b10c" id="tgt20" class="tgtSentence">La aplicación debe tener el formato de extensión <ui>.app</ui> o <ui>.ipa</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="515e13c532339d6b8f75023c2b1efb47" id="tgt21" class="tgtSentence">Aplicaciones que no pueden procesar con la herramienta de ajuste de aplicaciones</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="286b025c3ce0e33c590a3bfcc6bd95a5" id="tgt22" class="tgtSentence">Aplicaciones cifradas</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="def51c509546375269797a32359d9e9d" id="tgt23" class="tgtSentence">Aplicaciones sin firmar</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9002143676725d3a0680247492cbf2ab" id="tgt24" class="tgtSentence">Aplicaciones con atributos de archivo extendidos</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="024004829337a8542dfc0fe9a7896b4b" id="tgt25" class="tgtSentence">Aplicaciones que usan la biblioteca de Azure Active Directory (ADAL)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="43eff5249ef5ba694d987e53fa7f9410" id="tgt26" class="tgtSentence">Si su aplicación usa ADAL:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="7a34f85c51a2fb788117832082e04c2b" id="tgt27" class="tgtSentence">La aplicación debe incorporar una versión de ADAL igual o posterior a la versión 1.0.2.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="7f15eadc80a022de58ed0ddd247ea92c" id="tgt28" class="tgtSentence">El desarrollador debe permitir que su aplicación acceda a los recursos de administración de aplicaciones móviles de Intune.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="4462659de4d522ffbc363a78e3f7fd9f" id="tgt29" class="tgtSentence">Consulte <link xlink:href="99ab0369-5115-4dc8-83ea-db7239b0de97#BKMK_ADAL">Information for apps that use the Azure Active Directory Library (ADAL)</link> en este artículo para obtener más información sobre cómo usar ADAL.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bc276c9a688a2f09197da017cbd6efa5" id="tgt30" class="tgtSentence">Derechos de configuración de la aplicación</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ab7518eaec6008b19b74210d7d9144bb" id="tgt31" class="tgtSentence">Debe establecer los derechos antes de ajustar la aplicación. Estos derechos conceden permisos de aplicación adicionales y capacidades que van más allá de aquellas que se conceden en general.</caps:sentence>
                    <caps:sentence sentenceid="78876cede6e051df998fab51465986f4" id="tgt32" class="tgtSentence"> Para ver más instrucciones, consulte <link xlink:href="#BKMK_ios_entitlements">Setting app entitlements</link>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="acfdf3c87206282ea521092bf8f81408" id="tgt33" class="tgtSentence">Paso 2: instalar la herramienta de ajuste de aplicaciones</caps:sentence>
        </title>
        <content>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="34de99fd778bb21e24d240ab71296290" id="tgt34" class="tgtSentence">
                Desde la página <ui>Microsoft Intune App Wrapping Tool para iOS</ui> del <externalLink><linkText>Centro de descarga de Microsoft</linkText><linkUri>http://www.microsoft.com/en-us/download/default.aspx</linkUri></externalLink>, descargue el archivo de instalación de la herramienta de ajuste de aplicaciones en un equipo Mac.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="901cc58bfd7dd771273bce08f83a34af" id="tgt35" class="tgtSentence">En el equipo Mac, haga doble clic en el archivo de instalación <ui>Microsoft Intune App Wrapping Tool for iOS.dmg</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt36" class="tgtSentence">Haga clic en <ui>Acepto</ui> para aceptar el Contrato de licencia para el usuario final (CLUF).</caps:sentence>
                <caps:sentence sentenceid="32fdeef792eaf5a70b3eeef64d89d1e2" id="tgt37" class="tgtSentence"> El instalador se monta y se muestra en el equipo Mac.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="695acb94ea0db61ead338c35bc81878e" id="tgt38" class="tgtSentence">Abra el programa de instalación y copie los archivos que se muestran en una nueva carpeta en el equipo Mac.</caps:sentence>
                <caps:sentence sentenceid="28a0ec3da75131657653ae7c1ba358fe" id="tgt39" class="tgtSentence"> Una vez hecho esto, ya puede desconectar la unidad del instalador montada.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="30311596450d0634dd6eb3230308245b" id="tgt40" class="tgtSentence">Ahora está preparado para ejecutar la herramienta de ajuste de aplicaciones.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="6e5cf4a90e9572a480973787810b4f9f" id="tgt41" class="tgtSentence">Paso 3: ejecutar la herramienta de ajuste de aplicaciones</caps:sentence>
        </title>
        <content>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="ba2570e46b45d5f9e2c88fed979eed5b" id="tgt42" class="tgtSentence">En el equipo Mac, abra una ventana de Terminal y navegue hasta la carpeta donde guardó los archivos.</caps:sentence>
                <caps:sentence sentenceid="e17dfd59608bb81d26d4cfd827cc8830" id="tgt43" class="tgtSentence"> Dado que el archivo ejecutable reside dentro del paquete, deberá ejecutar el comando siguiente:</caps:sentence>
              </para>
              <code>./IntuneMAMPackager.app/Contents/MacOS/IntuneMAMPackager –i /&lt;path of input app&gt;/&lt;app filename&gt; -o /&lt;path to output folder&gt;/&lt;app filename&gt; –p /&lt;path to provisioning profile&gt; –c &lt;SHA1 hash of the certificate&gt; -a &lt;client ID of input app&gt; -r &lt;reply URI of input app&gt; -v true</code>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="d6e641f8706519b72252c138deabd90a" id="tgt44" class="tgtSentence">Algunos parámetros son opcionales, tal como se muestra en la tabla siguiente.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="01e8074753ed2c9a4a40fee3657adc8d" id="tgt45" class="tgtSentence">
                  <ui>Ejemplo:</ui> el comando del ejemplo siguiente ejecuta la herramienta de ajuste de aplicaciones en una aplicación denominada <ui>MyApp.ipa</ui>.</caps:sentence>
                <caps:sentence sentenceid="2c586607fb188b011d4f50370283ebb1" id="tgt46" class="tgtSentence"> Se especifican un perfil de aprovisionamiento y el hash SHA-1.</caps:sentence>
                <caps:sentence sentenceid="785f9b44848480cc16ed80950f5368f3" id="tgt47" class="tgtSentence"> La aplicación procesada se crea y almacena en <ui>/users/myadmin/Documents</ui> en el equipo Mac.</caps:sentence>
              </para>
              <code>/users/myadmin/Downloads/IntuneMAMPackager.app/Contents/MacOS/IntuneMAMPackager -i /users/myadmin/Downloads/MyApp.ipa -o /users/myadmin/Documents/MyApp_Wrapped.ipa -p /users/myadmin/Downloads/My_Provisioning_Profile_.mobileprovision -c 12A3BC45D67EF8901A2B3CDEF4ABC5D6E7890FAB –a 20e1cd0d-268e-4308-9583-02ae97dd353e –r https://contoso/ -v true</code>
              <para>
                <caps:sentence sentenceid="7d53bbb145ba51831f9b621cd658c9e8" id="tgt48" class="tgtSentence">Puede usar las siguientes propiedades de línea de comandos con la herramienta de ajuste de aplicaciones:</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1a8db4c996d8ed8289da5f957879ab94" id="tgt49" class="tgtSentence">Propiedad</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt50" class="tgtSentence">Más información</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="914071b8934b1d6035495f1ed02aa5fd" id="tgt51" class="tgtSentence">-h</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="38707662ca47dbfe31531ae1b9cfce82" id="tgt52" class="tgtSentence">Muestra las propiedades de línea de comandos disponibles para la herramienta de ajuste de aplicaciones.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="20f011826070657b0f0092278d65ec74" id="tgt53" class="tgtSentence">-i</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8771774b052502ba5ccbe7437897b90f" id="tgt54" class="tgtSentence">Especifica la ruta de acceso y el nombre de archivo de la aplicación de entrada.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b2ed43620b7fff2689035f1e99c24ded" id="tgt55" class="tgtSentence">-o</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="066bc3ba8aac1c80796cf34f76806279" id="tgt56" class="tgtSentence">Especifica la ruta de acceso en la que se va a guardar la aplicación procesada.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b3868ba70a8f4cf55464dd9926381db1" id="tgt57" class="tgtSentence">-p</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4fd371b3656717214343914193a7729b" id="tgt58" class="tgtSentence">Especifica la ruta de acceso al perfil de aprovisionamiento para las aplicaciones iOS.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="21d45631e3f4d3499ba78b73deaad0f1" id="tgt59" class="tgtSentence">-c</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="10147af17051f2da679ba88acece0466" id="tgt60" class="tgtSentence">Especifica el hash SHA1 del certificado de firma.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="37caf0ee262229a9ddc60877eec6883f" id="tgt61" class="tgtSentence">-a</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2e7dd22e0a01bd7ad8103286c5897a09" id="tgt62" class="tgtSentence">Identificador de cliente de la aplicación de entrada (en formato GUID) si la aplicación usa bibliotecas de Azure Active Directory (opcional).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="dca90348d03e2bdb52ad4cc669a23ebd" id="tgt63" class="tgtSentence">-r</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="36257efbdb2d30f439eb79ef0b98280c" id="tgt64" class="tgtSentence">URI de redireccionamiento de la aplicación de entrada si la aplicación usa bibliotecas de Azure Active Directory (opcional).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="47fa03ef5536c5573b137cec5adc2d39" id="tgt65" class="tgtSentence">-v</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="196d282409eb29e3913f58b1e1aa5d53" id="tgt66" class="tgtSentence">Salida de mensajes detallados en la consola (opcional).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4cfcce07af6f3b1c474ed2d11a52164e" id="tgt67" class="tgtSentence">Una vez que complete el proceso, se mostrará el mensaje <ui>La aplicación se ajustó correctamente</ui>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5c113c7fb2011f2d8a63cf6b9c1450c0" id="tgt68" class="tgtSentence">Si se produce un error, consulte <link xlink:href="99ab0369-5115-4dc8-83ea-db7239b0de97#BKMK_Error">error messages</link> para obtener ayuda.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4d13d98887e2b90bbcb8f8f37afccf70" id="tgt69" class="tgtSentence">La aplicación ajustada se guarda en la carpeta de salida que especificó anteriormente.</caps:sentence>
                <caps:sentence sentenceid="3e60cf63c91ab083c7cf35141afa8a92" id="tgt70" class="tgtSentence"> Ahora puede cargar la aplicación en <token>wit_nextref</token> y asociarla a una directiva de administración de aplicaciones móviles.</caps:sentence>
                <caps:sentence sentenceid="3469bdbb614ecd5d39b11849d3bf1551" id="tgt71" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy software to mobile devices in Microsoft Intune</link>.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="13fe93f7fbe521641fbb5b8538091c93" id="tgt72" class="tgtSentence">Debe cargar la aplicación como una nueva aplicación.</caps:sentence>
                  <caps:sentence sentenceid="cdc635d2cd28003ea73aeaa478f39437" id="tgt73" class="tgtSentence"> No se puede actualizar una versión anterior y sin ajustar de la aplicación.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence sentenceid="553490780f776593254526210f95b97f" id="tgt74" class="tgtSentence">A continuación, podrá implementar la aplicación en sus grupos de <token>wit_nextref</token> y esta se ejecutará en el dispositivo con las restricciones de aplicación especificadas.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="55a90c609d011365932506e8573b2d3d" id="tgt75" class="tgtSentence">Archivos de registro y mensajes de error</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ed03784389b7694f3218ea32ead09b84" id="tgt76" class="tgtSentence">Use la siguiente información para solucionar los problemas que tenga con la herramienta de ajuste de aplicaciones.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_Error">
            <title>
              <caps:sentence sentenceid="99ef0f507788ea70d9732ac28a98ff89" id="tgt77" class="tgtSentence">Mensajes de error</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="b59920842739652b5f9859a506d5c865" id="tgt78" class="tgtSentence">Si la herramienta de ajuste de aplicaciones no se completa correctamente, se mostrará uno de los siguientes mensajes de error:</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c5bbc13af6039ac4cf215911e482b5d4" id="tgt79" class="tgtSentence">Mensaje de error</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt80" class="tgtSentence">Más información</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cc5f5be876048e1fb1b099270933bc6f" id="tgt81" class="tgtSentence">Debe especificar un perfil de aprovisionamiento de iOS válido.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ebb6c4cba627c1c53b360297f5222211" id="tgt82" class="tgtSentence">Su perfil de aprovisionamiento podría no ser válido.</caps:sentence>
                        <caps:sentence sentenceid="fef7cd80dc96b9f34677aaf73b452d9c" id="tgt83" class="tgtSentence"> Asegúrese de que tenga los permisos correctos para dispositivos y que su perfil se destine correctamente a desarrollo o a distribución.</caps:sentence>
                        <caps:sentence sentenceid="f80cbe94131df948bf99d034f58f44c6" id="tgt84" class="tgtSentence"> El perfil de aprovisionamiento también podría haber expirado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5226a2a46eff4a1d667f452c0a596430" id="tgt85" class="tgtSentence">Especifique un nombre de aplicación de entrada válido.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="72fa5722fac3dd4391a8e20fe9bc59fd" id="tgt86" class="tgtSentence">Asegúrese de que el nombre de la aplicación de entrada especificado sea correcto.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="68088c89a82445b6a8a472c05c435014" id="tgt87" class="tgtSentence">Especifique una ruta válida a la aplicación de salida.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="baf2ca2b06226f398200c66e598455b7" id="tgt88" class="tgtSentence">Asegúrese de que la ruta de acceso a la aplicación de salida especificada exista y sea correcta.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cafa0fb15072a2802f9468eaef6a49bc" id="tgt89" class="tgtSentence">Especifique un perfil de aprovisionamiento de entrada válido.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c0a9fd1e9e0b42c95a1dfb6de8950e75" id="tgt90" class="tgtSentence">Asegúrese de que proporcionó un nombre y una extensión de perfil de aprovisionamiento válidos.</caps:sentence>
                        <caps:sentence sentenceid="b59966e599ae1aae8677aa0d008a91bd" id="tgt91" class="tgtSentence"> Puede que el perfil de aprovisionamiento no disponga de derechos o que no se haya incluido la opción de línea de comandos <ui>– p</ui>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b01b224e679d4be90cb7fe03cf6d4d20" id="tgt92" class="tgtSentence">No se encontró la aplicación de entrada especificada.</caps:sentence>
                        <caps:sentence sentenceid="f8e379528c2f6ebc4e02ce44cb3b81bd" id="tgt93" class="tgtSentence"> Especifique un nombre de aplicación de entrada y una ruta de acceso válidos.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d52543fd2ec2d8f048a3bc9cb272cdc2" id="tgt94" class="tgtSentence">Asegúrese de que la ruta de acceso de la aplicación de entrada sea válida y exista.</caps:sentence>
                        <caps:sentence sentenceid="41699b19a0000ca3f29070dc02d2ed05" id="tgt95" class="tgtSentence"> Asegúrese de que la aplicación de entrada exista en esa ubicación.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0254e69d4173436f965852d10f383c8f" id="tgt96" class="tgtSentence">No se encontró el archivo de perfil de aprovisionamiento entrada especificado.</caps:sentence>
                        <caps:sentence sentenceid="87e7d7a1413baf3d31c606f4b3b59100" id="tgt97" class="tgtSentence"> Especifique un archivo de perfil de aprovisionamiento de entrada válido.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="153c47f31f3f378bda7aed9d18ade3d5" id="tgt98" class="tgtSentence">Asegúrese de que la ruta de acceso al archivo de aprovisionamiento de entrada sea válida y de que el archivo especificado exista.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6b9ef6698d15a07643ea4d8b6fa09269" id="tgt99" class="tgtSentence">No se encontró la carpeta de aplicación de salida especificada.</caps:sentence>
                        <caps:sentence sentenceid="7c414bda3c776ffe54fa0870cbadb339" id="tgt100" class="tgtSentence"> Especifique una ruta válida a la aplicación de salida.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c6df7c2940dd6df31fa92d74ce5f1b20" id="tgt101" class="tgtSentence">Asegúrese de que la ruta de acceso de salida especificada sea válida y exista.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="599fc06e7ba315371d20e9f51af3d3ef" id="tgt102" class="tgtSentence">La aplicación de salida no tiene extensión .ipa.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="305e29e9734b3db4c694b2f77fbdea4e" id="tgt103" class="tgtSentence">La herramienta de ajuste de aplicaciones solo acepta aplicaciones con las extensiones <ui>.app</ui> e <ui>.ipa</ui>.</caps:sentence>
                        <caps:sentence sentenceid="724731c79e7610a1cfbfaf67b8caca61" id="tgt104" class="tgtSentence"> Asegúrese de que el archivo de salida tenga una extensión válida.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a818bb4e27049fe50850856b4e64d034" id="tgt105" class="tgtSentence">Se especificó un certificado de firma no válido.</caps:sentence>
                        <caps:sentence sentenceid="32b0818f472532daef5c308a3b280ac4" id="tgt106" class="tgtSentence"> Especifique un certificado de firma de Apple válido.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8d8a880564a98e11c4dbdaab661ba98f" id="tgt107" class="tgtSentence">Asegúrese de haber descargado el certificado de firma correcto desde el portal para desarrolladores de Apple.</caps:sentence>
                        <caps:sentence sentenceid="73538ee90a38ab85eefa6d125496420c" id="tgt108" class="tgtSentence"> También es posible que el certificado haya expirado.</caps:sentence>
                        <caps:sentence sentenceid="6061cd17f461897b854ab6b9b41d924e" id="tgt109" class="tgtSentence"> Si el perfil de aprovisionamiento y el certificado de Apple se pueden usar para firmar correctamente una aplicación en Xcode, son válidos para la herramienta de ajuste de aplicaciones.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d394953c66ef17abcfc6d02f3eb6a3d5" id="tgt110" class="tgtSentence">La aplicación de entrada especificada no es válida.</caps:sentence>
                        <caps:sentence sentenceid="9944cdf572db10ca739edac7985ffab0" id="tgt111" class="tgtSentence"> Especifique una aplicación válida.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="49d829d67e1e908535bbf13d7cec17ef" id="tgt112" class="tgtSentence">Asegúrese de que tenga una aplicación iOS válida que se haya compilado como archivo .app o .ipa.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a22e643456d0e523f0b1c6b2da5de1ee" id="tgt113" class="tgtSentence">La aplicación de entrada especificada está cifrada.</caps:sentence>
                        <caps:sentence sentenceid="811af494b9f881c73547a5cc27e7fedf" id="tgt114" class="tgtSentence"> Especifique una aplicación sin cifrar válida.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f0f63c435e079a14892c2a382b6b3504" id="tgt115" class="tgtSentence">La herramienta de ajuste de aplicaciones no es compatible con aplicaciones cifradas.</caps:sentence>
                        <caps:sentence sentenceid="b62db6524275be270eb1a2cd9748785f" id="tgt116" class="tgtSentence"> Especifique una aplicación sin cifrar.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c949e8a8c8346114aa831200ed8ef061" id="tgt117" class="tgtSentence">La aplicación de entrada especificada no está en un formato ejecutable independiente de la posición (PIE).</caps:sentence>
                        <caps:sentence sentenceid="adbd06de6404dd9ec9f8c6165f622af3" id="tgt118" class="tgtSentence"> Especifique una aplicación válida en formato PIE.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9c9bd764c24f95a5af82176ac150835c" id="tgt119" class="tgtSentence">Las aplicaciones de archivo ejecutable independiente de la posición (PIE) se pueden cargar en una dirección de memoria aleatoria al ejecutarse, lo que puede tener ventajas de seguridad.</caps:sentence>
                        <caps:sentence sentenceid="2cb5c2ef58acfd544151956153bd1f57" id="tgt120" class="tgtSentence"> Para obtener más información, consulte la documentación para desarrolladores de Apple.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e429dbbbc3f87ee1c19f94af124ebab" id="tgt121" class="tgtSentence">La aplicación de entrada especificada ya se ajustó.</caps:sentence>
                        <caps:sentence sentenceid="91d9972b8c4a8198d6721422d4d0326f" id="tgt122" class="tgtSentence"> Especifique una aplicación sin ajustar válida.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d318523e6b912ed96c40339efc19396f" id="tgt123" class="tgtSentence">No puede procesar una aplicación que la herramienta ya procesó.</caps:sentence>
                        <caps:sentence sentenceid="1004d1bc7f35a3b09a354a2f752980c4" id="tgt124" class="tgtSentence"> Si desea volver a procesar una aplicación, ejecute la herramienta con la versión original de la aplicación.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2f522832eff5595b6583909d8a5a2216" id="tgt125" class="tgtSentence">La aplicación de entrada especificada no está firmada.</caps:sentence>
                        <caps:sentence sentenceid="8ff17c828e1d0ebe806df7b5d9f9aa74" id="tgt126" class="tgtSentence"> Especifique una aplicación firmada válida.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cc90ccce6eaa1aba4797b949f4730945" id="tgt127" class="tgtSentence">La herramienta de ajuste de aplicaciones requiere que las aplicaciones estén firmadas.</caps:sentence>
                        <caps:sentence sentenceid="d55abc9c4c2a5dd1e668dab3b8918e25" id="tgt128" class="tgtSentence"> Consulte la documentación para desarrolladores para aprender a firmar una aplicación ajustada.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b16ca6976594993a5ec4306ef909aaa4" id="tgt129" class="tgtSentence">La aplicación de entrada especificada debe tener formato .ipa o .app.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e3cecf11ec0e34b6b5a02cac1cdc782c" id="tgt130" class="tgtSentence">La herramienta de ajuste de aplicaciones solo acepta aplicaciones con las extensiones .app e .ipa.</caps:sentence>
                        <caps:sentence sentenceid="8fe4972962f7247ae7b33439d68e6615" id="tgt131" class="tgtSentence"> Asegúrese de que el archivo de entrada tenga una extensión válida y se haya compilado como archivo .app o .ipa.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="acfdb58b64aae83aa06aec76579a4dae" id="tgt132" class="tgtSentence">La aplicación de entrada especificada ya se ajustó y se encuentra en la última versión de la plantilla de directiva.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4f8d61fab05001bcd2148d53efcc5e2f" id="tgt133" class="tgtSentence">La herramienta de ajuste de aplicaciones no ajustará una aplicación ajustada existente con la última versión de la plantilla de directiva.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="39d77504817fb639b5af7fafb3518be5" id="tgt134" class="tgtSentence">El identificador de cliente de Azure Active Directory especificado no es un GUID con formato correcto.</caps:sentence>
                        <caps:sentence sentenceid="e727b50a55ff7b510bb8df4c7c8e4601" id="tgt135" class="tgtSentence"> Especifique un identificador de cliente válido.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="67917c93e63ce2075e06c2e0cea42919" id="tgt136" class="tgtSentence">Cuando use el parámetro de identificador de cliente, asegúrese de que haya proporcionado un identificador de cliente válido en formato GUID.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9fc36306e0eff0b4a9016a0b81d2e751" id="tgt137" class="tgtSentence">El URI de respuesta de Azure Active Directory especificado no es un URI con formato correcto.</caps:sentence>
                        <caps:sentence sentenceid="c3b9bce5b176e7c19c89e7596c73e67f" id="tgt138" class="tgtSentence"> Especifique un URI de respuesta válido.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fd4c1d5305405cd5892aed77fca896bd" id="tgt139" class="tgtSentence">Cuando use la propiedad de línea de comandos de URI de respuesta, asegúrese de que haya proporcionado un URI de respuesta válido.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0dd5566cb7a7bc2528307347657cb853" id="tgt140" class="tgtSentence">ADVERTENCIA: no ha especificado un hash de certificado SHA1.</caps:sentence>
                        <caps:sentence sentenceid="9779c3d7da9d74793eeb066208d7ad9b" id="tgt141" class="tgtSentence"> Asegúrese de que la aplicación ajustada se firme antes de implementarla.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a6669e0a640201b0126fd3ef72318f90" id="tgt142" class="tgtSentence">Asegúrese de especificar un valor de hash SHA válido (mediante la propiedad de línea de comandos <ui>–c</ui>).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="ace64f945d902d31b4d48a6ae4f558a6" id="tgt143" class="tgtSentence">Archivos de registro de la herramienta de ajuste de aplicaciones</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="ee91932b484e1b3705f164a029b287c8" id="tgt144" class="tgtSentence">Las aplicaciones que se ajustaron mediante la herramienta de ajuste de aplicaciones generan los registros que se escriben en la consola del dispositivo cliente de iOS.</caps:sentence>
                <caps:sentence sentenceid="06c5709248073eecdae11a8aa07d631c" id="tgt145" class="tgtSentence"> Esta información resulta útil en situaciones en las que tiene problemas con la aplicación y necesita diagnosticar si el problema está relacionado con la herramienta de ajuste de aplicaciones.</caps:sentence>
                <caps:sentence sentenceid="85410dfefc4bffd3db2b72799f3dbda8" id="tgt146" class="tgtSentence"> Para resolver este problema, use los siguientes pasos:</caps:sentence>
              </para>
              <procedure>
                <title></title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="bf03de324ac6c0483fb11a2bf301a39d" id="tgt147" class="tgtSentence">Reproduzca el problema ejecutando la aplicación.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="181fa755801c7d552db89dea214bc84a" id="tgt148" class="tgtSentence">Recopile la salida de consola siguiendo las instrucciones de <externalLink><linkText>Depuración de aplicaciones iOS implementadas</linkText><linkUri>https://developer.apple.com/library/ios/qa/qa1747/_index.html</linkUri></externalLink> de Apple.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="03b58a0c5731d1fff3d7e9b35fb31043" id="tgt149" class="tgtSentence">Filtre los registros guardados para la salida de restricciones de la aplicación especificando el siguiente script en la consola:</caps:sentence>
                      </para>
                      <code>grep “IntuneAppRestrictions” &lt;text file containing console output&gt; &gt; &lt;required filtered log file name&gt; </code>
                      <para>
                        <caps:sentence sentenceid="514402f99717527a1e985d6e3cedf1f6" id="tgt150" class="tgtSentence">Puede enviar los registros filtrados a Microsoft.</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="f9808dd42433a57f74934fb553b0c9be" id="tgt151" class="tgtSentence">En el archivo de registro, el elemento "versión" representa la versión de compilación de Xcode.</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence sentenceid="afbf11ba1080851475d476f9b13b76bc" id="tgt152" class="tgtSentence">Las aplicaciones ajustadas también ofrecen a los usuarios la opción de enviar registros directamente desde el dispositivo a través de correo electrónico después de que la aplicación se bloquea.</caps:sentence>
                        <caps:sentence sentenceid="2b4b09de0fbd76859f41f780eba993b4" id="tgt153" class="tgtSentence"> Los usuarios pueden enviarle el registro para que lo examine y reenviarlo a Microsoft si es necesario.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_ADAL" expanded="true">
            <title>
              <caps:sentence sentenceid="776bfd6a32de5685fe9873eb2047f6b5" id="tgt154" class="tgtSentence">
          Información para las aplicaciones que usen la biblioteca de Azure Active Directory (ADAL)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="d795991bba5a3c9210add374e0a1a5b0" id="tgt155" class="tgtSentence">La información de esta sección solo se aplica a aplicaciones que usan la biblioteca de Azure Active Directory (ADAL).</caps:sentence>
                <caps:sentence sentenceid="6d6753df9c4764c087ebba5d091e0a7e" id="tgt156" class="tgtSentence"> Si no está seguro de si su aplicación usa esta biblioteca, póngase en contacto con el desarrollador de la aplicación.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="7a34f85c51a2fb788117832082e04c2b" id="tgt157" class="tgtSentence">La aplicación debe incorporar una versión de ADAL igual o posterior a la versión 1.0.2.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="66f2af5b99dde2088913e4a2cfb6b52a" id="tgt158" class="tgtSentence">Para las aplicaciones que usen ADAL, deben cumplirse las siguientes condiciones:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="95cd3a9b6d47cabff2c2440098704260" id="tgt159" class="tgtSentence">La aplicación debe incorporar una versión de ADAL posterior o igual a la versión 1.0.2</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c05c66b36bea9dc64857a5ab06136cdb" id="tgt160" class="tgtSentence">Los desarrolladores deben permitir que sus aplicaciones accedan a los recursos de administración de aplicaciones móviles de Intune, tal como se describe en <link xlink:href="#BKMK_step_use_adal">Steps to follow for apps that use ADAL</link>.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section address="BKMK_adal_overview">
                <title>
                  <caps:sentence sentenceid="bfed8cc455e33b76bdcc20518eb2dc62" id="tgt161" class="tgtSentence">Información general acerca de los identificadores que debe obtener</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="e7c1ccdde011660deff8db65df92cc57" id="tgt162" class="tgtSentence">Las aplicaciones que usen ADAL deben registrarse a través del portal de administración de Azure para obtener dos identificadores únicos para la aplicación:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="f393f3f5e496869a15bc72cbfd56f541" id="tgt163" class="tgtSentence">Identificador</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt164" class="tgtSentence">Más información</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="313af772d92d01300d5e89512cd93bd0" id="tgt165" class="tgtSentence">Valor predeterminado</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="796b5045502934ad2f1885a22f5b76ef" id="tgt166" class="tgtSentence">Identificador de cliente</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="1492d9dcec5116626780d4b6e6648798" id="tgt167" class="tgtSentence">Una vez que se registra con Azure Active Directory, se genera un identificador GUID único para cada aplicación.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="49c0b4f4372e0e062b8a73d24dcb88f3" id="tgt168" class="tgtSentence">Si conoce el identificador de cliente específico de las aplicaciones, puede especificar este valor.</caps:sentence>
                            <caps:sentence sentenceid="419e8d1453908ecc4ab45bfb5420ddb4" id="tgt169" class="tgtSentence"> De lo contrario, debe usarse el valor predeterminado.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dd51c3eb9be0fff84f7f746c2906e9b" id="tgt170" class="tgtSentence">6c7e8096-f593-4d72-807f-a5f86dcc9c77</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="7b4e15adb1f75dab81a9c42356e12477" id="tgt171" class="tgtSentence">URI de redireccionamiento</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d98de059484be2fbda59c998197a4364" id="tgt172" class="tgtSentence">Valor de URI que los desarrolladores pueden proporcionar al registrar la aplicación con Azure Active Directory para asegurarse de que los tokens de autenticación se devuelvan específicamente a ese extremo.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="aea965dbba961c7a886b702f9e0f6da9" id="tgt173" class="tgtSentence">La especificación de un URI de redireccionamiento es un parámetro opcional para la herramienta de ajuste de aplicaciones.</caps:sentence>
                            <caps:sentence sentenceid="5eeeca0eba5c99a1cd5860645c81d4ce" id="tgt174" class="tgtSentence"> Si no se especifica, se usará un identificador URI predeterminado.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="55d1dba84eb7de3ff1618d4f0aaa34fc" id="tgt175" class="tgtSentence">urn:ietf:wg:oauth:2.0:oob</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <para>
                    <caps:sentence sentenceid="1ee5ebd329c5299bddbd852e5a2ac7b1" id="tgt176" class="tgtSentence">Cuando no se proporcionan los valores anteriores a la herramienta, se usan automáticamente los siguientes valores adicionales:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f96237d30971f84489b1c98d909f6aea" id="tgt177" class="tgtSentence">
                          <ui>URI de la entidad emisora</ui>: https://login.windows.net/common/oauth2/authorize</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="17f24eccae423619968f623cafc9725c" id="tgt178" class="tgtSentence">
                          <ui>Identificador de recurso</ui>: https://intunemam.microsoft.com</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </section>
              <section address="BKMK_step_use_adal">
                <title>
                  <caps:sentence sentenceid="e091fbec2a45110a192867379cb1beee" id="tgt179" class="tgtSentence">Pasos que debe seguir en cuanto a las aplicaciones que usan ADAL</caps:sentence>
                </title>
                <content>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="446c7ec59abfb83834bb96ce5efdad86" id="tgt180" class="tgtSentence">Revise <link xlink:href="#BKMK_adal_overview">Overview of identifiers you need to get</link> para identificar los valores que debe obtener.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b06be992fb8a0771a5076a3d8efc24d7" id="tgt181" class="tgtSentence">Configure el acceso a la administración de aplicaciones móviles en Azure Active Directory mediante los siguientes pasos:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ccc8bdeea96f8df1cd08f3fdbd8339bc" id="tgt182" class="tgtSentence">Inicie sesión en una cuenta de Azure Active Directory existente en el portal de administración de Azure.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt183" class="tgtSentence">Haga clic en <ui>registro existente de la aplicación LOB</ui> en Azure Active Directory.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="799378bd7c32004eda7053298d6905cf" id="tgt184" class="tgtSentence">En la sección de configuración, elija <ui>Configurar acceso a las API web en otras aplicaciones</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt185" class="tgtSentence">En la sección <ui>Permiso en otras aplicaciones</ui> de la primera lista desplegable, elija <ui>Administración de aplicaciones móviles de Intune</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="c715ea7cfcb45b006a468d487cc719b7" id="tgt186" class="tgtSentence">Ahora puede usar el identificador de cliente de la aplicación en la herramienta de ajuste de aplicaciones.</caps:sentence>
                            <caps:sentence sentenceid="d2076ce1693e2e2cb09f6d3abc63f955" id="tgt187" class="tgtSentence"> Puede encontrar el identificador de cliente de la aplicación en el portal de administración de Azure Active Directory, tal como se describe en la sección <link xlink:href="#BKMK_adal_overview">Overview of identifiers you need to get</link>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt188" class="tgtSentence">Use los valores <ui>Client-ID</ui> (mediante la propiedad <ui>–a</ui>) y <ui>Redirect-URI</ui> como propiedades de línea de comandos en la herramienta de ajuste de aplicaciones.</caps:sentence>
                        <caps:sentence sentenceid="69c36fb128e8315b166c6a5efc18b5ef" id="tgt189" class="tgtSentence"> Si no tiene estos valores, se usarán los predeterminados.</caps:sentence>
                        <caps:sentence sentenceid="06c43226ea668d70ec9768e0b01b52c5" id="tgt190" class="tgtSentence"> Recuerde que debe especificar ambos valores o el usuario final no podrá autenticar correctamente la aplicación procesada.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence sentenceid="3dc66a0546140a18bbf9d53aee23affd" id="tgt191" class="tgtSentence">Requisitos de autenticación, perfil de aprovisionamiento y certificados</caps:sentence>
                </title>
                <content>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="ba12fb48e2d23bb2bd2819f64d02ec7e" id="tgt192" class="tgtSentence">Requisito</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt193" class="tgtSentence">Detalles</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2f7a0a581b791ebfc979bb576eefdbc3" id="tgt194" class="tgtSentence">Perfil de aprovisionamiento</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3617e5f8ca4eb9396169aa6d14cc580e" id="tgt195" class="tgtSentence">
                              <ui>Asegúrese de que el perfil de aprovisionamiento sea válido antes de incluirlo</ui>: la herramienta de ajuste de aplicaciones no comprueba si el perfil de aprovisionamiento expiró al procesar una aplicación iOS.</caps:sentence>
                            <caps:sentence sentenceid="69cdaac1796ea312ce281ffa7e6dbbaa" id="tgt196" class="tgtSentence"> Si se especifica un perfil de aprovisionamiento expirado, la herramienta de ajuste de aplicaciones incluirá el perfil de aprovisionamiento caducado y no sabrá que hay un problema hasta que la aplicación no se pueda instalar en un dispositivo iOS.</caps:sentence> </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e0d30cef5c6139275b58b525001b413c" id="tgt197" class="tgtSentence">Certificado</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ed45fdf86671c9921fc60a0ecc16c37d" id="tgt198" class="tgtSentence">
                                  <ui>Asegúrese de que el certificado sea válido antes de especificarlo</ui>: la herramienta no comprueba si un certificado expiró al procesar aplicaciones iOS.</caps:sentence>
                                <caps:sentence sentenceid="e506c0e2a15caae30508e8375626d23a" id="tgt199" class="tgtSentence"> Si se proporciona el valor hash de un certificado expirado, la herramienta procesará y firmará la aplicación, pero no se podrá instalar en dispositivos.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ff0765010366e9018b756fb39d26411c" id="tgt200" class="tgtSentence">
                                  <ui>Asegúrese de que el certificado proporcionado para firmar la aplicación en paquete tenga una coincidencia en el perfil de aprovisionamiento</ui>: la herramienta no valida si el perfil de aprovisionamiento tiene una coincidencia para el certificado proporcionado para firmar la aplicación ajustada.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="6fa691d2c07bea6ae78b7022c80e9d20" id="tgt201" class="tgtSentence">Autenticación</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="d1ef44673cb049a3f88d83488d036392" id="tgt202" class="tgtSentence">En dispositivos en los que haya implementado una aplicación ajustada, si se toca la barra de estado en el dispositivo será necesario que el usuario vuelva a autenticarse con <token>wit_nextref</token>.</caps:sentence>
                                <caps:sentence sentenceid="e89fb79af36023cbe8fca3b54d4eb1d4" id="tgt203" class="tgtSentence"> La directiva predeterminada de una aplicación ajustada es <legacyItalic>autenticación al volver a iniciar</legacyItalic>.</caps:sentence>
                                <caps:sentence sentenceid="a6f605e63af1d2de54ac96c25c3c2ac6" id="tgt204" class="tgtSentence"> iOS controla cualquier notificación externa (por ejemplo, una llamada telefónica) como salir de la aplicación y, a continuación, volver a iniciarla.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="a42e4a43011e68ce854d7f93bdf6ecb0" id="tgt205" class="tgtSentence">Un dispositivo debe tener establecido un PIN para que el cifrado funcione.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="c3659473410fbbea8c2104c89e6077fc" id="tgt206" class="tgtSentence">En el caso de aplicaciones ajustadas, el primer usuario que inicia sesión en cualquier aplicación ajustada del mismo editor se almacena en la memoria caché.</caps:sentence>
                                <caps:sentence sentenceid="3050b866577920b1236559b992e0f0e5" id="tgt207" class="tgtSentence"> A partir de entonces, solo ese usuario puede tener acceso a la aplicación.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="a9bc1e2dbd139381677c7fcf1b323655" id="tgt208" class="tgtSentence">Para restablecer el usuario, tiene que anularse la inscripción del dispositivo y volver a inscribirlo.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence sentenceid="8874dc8870798acf1ba1c059ac600385" id="tgt209" class="tgtSentence">Notas técnicas sobre ADAP y solución de problemas</caps:sentence>
                </title>
                <content>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d116509dc1a26a19874a1be1c632f349" id="tgt210" class="tgtSentence">Si no se encuentra ningún recurso ADAL, la herramienta incluirá la biblioteca dinámica ADAL.</caps:sentence>
                        <caps:sentence sentenceid="7b789e6018526e6941dc03fd315ae5d8" id="tgt211" class="tgtSentence"> La herramienta buscará la biblioteca ADAL de nombre <ui>ADALiOS.bundle</ui> en la carpeta raíz.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="38a00d7457d6ca8ad165c0b8ce0646d4" id="tgt212" class="tgtSentence">La herramienta no buscará archivos binarios ADAL (si existen) en la aplicación.</caps:sentence>
                        <caps:sentence sentenceid="4be5d5f522178ca9997b0fc7f8cd9285" id="tgt213" class="tgtSentence"> Si la aplicación se vincula a una versión no actualizada, puede haber errores en tiempo de ejecución durante el inicio de sesión cuando se habilitan directivas de autenticación.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="0d7d4223d2aaad75162ffb2e664ab936" id="tgt214" class="tgtSentence">
                          <token>wit_nextref</token> obtiene el token de AAD para el identificador del recurso de administración de aplicaciones móviles (MAM) de <token>wit_nextref</token> para autenticación.</caps:sentence>
                        <caps:sentence sentenceid="d1bee6335ebe5329a3b1f0f571f5550d" id="tgt215" class="tgtSentence"> Sin embargo, no se utiliza en cualquier llamada que, a su vez, compruebe la validez del token.</caps:sentence>
                        <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt216" class="tgtSentence">
                          <token>wit_nextref</token> solo lee el UPN del usuario con sesión iniciada para determinar el acceso de la aplicación.</caps:sentence>
                        <caps:sentence sentenceid="2b8553864b335a64fbf9e6c219c95911" id="tgt217" class="tgtSentence"> El token de AAD no se usa para las demás llamadas de servicio.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2880caf659110456bfb33b1ee0a129d1" id="tgt218" class="tgtSentence">Los tokens de autenticación se comparten entre las aplicaciones del mismo editor ya que se almacenan en las llaves compartidas.</caps:sentence>
                        <caps:sentence sentenceid="307b6e09250ca6aec4eda353503376a0" id="tgt219" class="tgtSentence"> Si desea aislar una aplicación concreta, debe usar un certificado de firma y un perfil de aprovisionamiento distintos para esa aplicación.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="318456facfc6d997cc896daf840d6086" id="tgt220" class="tgtSentence">Las peticiones de inicio de sesión dobles se impiden si proporciona el identificador de cliente y el URI de redireccionamiento de la aplicación cliente.</caps:sentence>
                        <caps:sentence sentenceid="abaca04340f1f0146a3c7ebf3e4e4914" id="tgt221" class="tgtSentence"> Este identificador de cliente debe registrarse para obtener acceso al identificador del recurso de MAM de <token>wit_nextref</token> MAM en el panel de AAD.</caps:sentence>
                        <caps:sentence sentenceid="72763e5d0a30f184ae49b2ab9149c46a" id="tgt222" class="tgtSentence"> Si no lo hace, provocará un error de inicio de sesión cuando se ejecute la aplicación.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <section address="BKMK_ios_entitlements">
        <title>
          <caps:sentence sentenceid="e51f11ff1e8e44eef2c77cf055ad964b" id="tgt223" class="tgtSentence">Configurar los derechos de la aplicación</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="181807851369ad48113d439e18b8b57a" id="tgt224" class="tgtSentence">Antes de ajustar la aplicación, puede concederle <ui>derechos</ui> para que tenga permisos y capacidades adicionales que normalmente no podría usar.</caps:sentence>
            <caps:sentence sentenceid="83a6d1fd4325bf13c7387f279a72f3c2" id="tgt225" class="tgtSentence">   Un <ui>archivo de derechos</ui> se usa durante la firma de código para especificar permisos especiales dentro de la aplicación (por ejemplo, el acceso a las cadenas de claves compartidas).</caps:sentence>
            <caps:sentence sentenceid="259c1c4b5cb0caf27af346c32d2ab30e" id="tgt226" class="tgtSentence"> Los servicios de aplicaciones específicos, denominados <ui>capacidades</ui>, se habilitan en Xcode durante el desarrollo de las aplicaciones.</caps:sentence>
            <caps:sentence sentenceid="53921b9032e9b820e542b1d99dce6940" id="tgt227" class="tgtSentence"> Una vez habilitadas, las capacidades se reflejan en el archivo de derechos.</caps:sentence>
            <caps:sentence sentenceid="7b732880c1ac039a416976509f5f8500" id="tgt228" class="tgtSentence"> Para obtener más información acerca de los derechos y las capacidades, consulte <externalLink><linkText>Agregar capacidades</linkText><linkUri>https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AddingCapabilities/AddingCapabilities.html</linkUri></externalLink> en la biblioteca para desarrolladores de iOS.</caps:sentence>
            <caps:sentence sentenceid="e28234f748bf019919924b63d127ddde" id="tgt229" class="tgtSentence"> Para obtener una lista completa de las capacidades admitidas, consulte <externalLink><linkText>Capacidades admitidas</linkText><linkUri>https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/SupportedCapabilities/SupportedCapabilities.html</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="22064518b8bda32c726e2d6b4235be9d" id="tgt230" class="tgtSentence">Capacidades admitidas por la herramienta de ajuste de aplicaciones para iOS</caps:sentence>
            </title>
            <content>
              <table border="1">
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9a06cb435cd72d31b714e9dbb5c3d168" id="tgt231" class="tgtSentence">Capacidad</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt232" class="tgtSentence">Descripción</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4c7a06a3c511faa29a86e7961273b30c" id="tgt233" class="tgtSentence">Uso recomendado</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b48c5010a1fb5606b3341fbb7ffc6967" id="tgt234" class="tgtSentence">Grupos de aplicaciones</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d3cc39d24d0906f98077f05223a3e6b4" id="tgt235" class="tgtSentence">Use los grupos de aplicaciones para permitir que varias aplicaciones tengan acceso a contenedores compartidos y que la comunicación entre procesos adicionales entre las aplicaciones sea posible.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="01c1e8138f68214ed45759137494a404" id="tgt236" class="tgtSentence">Para habilitar los grupos de aplicaciones, abra el panel <ui>Capacidades</ui> y haga clic en el interruptor <ui>ACTIVAR</ui> que se encuentra en la sección <ui>Grupos de aplicaciones </ui>.</caps:sentence>
                        <caps:sentence sentenceid="6f01d0b5b6a53b6ac71ab47ef93488f3" id="tgt237" class="tgtSentence"> Puede agregar grupos de aplicaciones o seleccionar los ya existentes.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1510a70206df3636bbeb144de2d1b916" id="tgt238" class="tgtSentence">Al usar grupos de aplicaciones, use la notación DNS inversa:</caps:sentence>
                      </para>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="d7b9f4c92347b19aace6f0e88c2032b9" id="tgt239" class="tgtSentence">group.com.companyName.AppGroup</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="083da50194f2c5416a40666a5ee8c2d1" id="tgt240" class="tgtSentence">Modos en segundo plano</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt241" class="tgtSentence"> <para>Si habilita los modos en segundo plano, la aplicación de iOS podrá seguir ejecutándose en segundo plano.</para></caps:sentence>
                    </TD>
                    <TD></TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="073395e7b5fc53b602884ac0aaf757fb" id="tgt242" class="tgtSentence">Protección de datos</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt243" class="tgtSentence"> <para>La opción Protección de datos agrega un nivel de seguridad a los archivos almacenados en el disco mediante la aplicación de iOS. Asimismo, la protección de datos usa el hardware de cifrado integrado en ciertos dispositivos para almacenar archivos en el disco con un formato cifrado. Debe aprovisionar la aplicación para usar la protección de datos.</para></caps:sentence>
                    </TD>
                    <TD></TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0acb2bd1e7828ed5d5e80a29ad57086f" id="tgt244" class="tgtSentence">Compras desde la aplicación</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="34cf1ef460cce0ae7ea25239101f9da1" id="tgt245" class="tgtSentence">La opción de Compras desde la aplicación inserta una opción para acceder a la tienda directamente desde su aplicación, lo que le permitirá conectarse a la misma y procesar los pagos del usuario de forma segura.</caps:sentence>
                        <caps:sentence sentenceid="35f2555b00c346cf54a08d7bb9dfdded" id="tgt246" class="tgtSentence"> Puede usar la opción Compras desde la aplicación para pagar por mejorar las funcionalidades o para conseguir contenidos adicionales que pueda usar la aplicación.</caps:sentence>
                      </para>
                    </TD>
                    <TD></TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="060f5544df3460705e305ee72545a57a" id="tgt247" class="tgtSentence">Uso compartido de cadenas de claves</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="89c8d4b2eee73c0341434f6f62ea7f2f" id="tgt248" class="tgtSentence">Si habilita el uso compartido de las cadenas de claves, la aplicación podrá compartir contraseñas en la cadena de claves con otras aplicaciones desarrolladas por el equipo.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bf77cd668878bb6241df0a949950c46b" id="tgt249" class="tgtSentence">Cuando use de forma compartida las cadenas de claves, use la notación DNS inversa:</caps:sentence>
                      </para>
                      <para>
                        <legacyItalic>
                          <caps:sentence sentenceid="8cff363494267f7f2bbcabe53d6936f0" id="tgt250" class="tgtSentence">com.companyName.KeychainGroup</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="13cadc434c25bd3de4b1f90d2c39c56d" id="tgt251" class="tgtSentence">VPN personal</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="641ca9b1162c98f3e1547c66309d3f47" id="tgt252" class="tgtSentence">Habilite la VPN personal para permitir a su aplicación crear y controlar un sistema personalizado de la configuración de VPN mediante el marco de la extensión de la red.</caps:sentence>
                      </para>
                    </TD>
                    <TD></TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8a74e940a7352c49cd4944e3f2a3dd2a" id="tgt253" class="tgtSentence">Notificaciones de inserción</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="aef75050eee5a4da64fa702471347488" id="tgt254" class="tgtSentence">El servicio de notificaciones push de Apple (APN) permite que una aplicación que no se está ejecutando en primer plano notifique al usuario que tiene información para el mismo.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="be7de151dd5b1c732220dc79e01adf98" id="tgt255" class="tgtSentence">Para que funcionen las notificaciones push, debe usar un perfil de aprovisionamiento específico de la aplicación.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1ce48bdd76c7b3edd2f11eb0283fe381" id="tgt256" class="tgtSentence">Siga los pasos de la <externalLink><linkText>documentación para desarrolladores de Apple</linkText><linkUri>https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AddingCapabilities/AddingCapabilities.html</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b19002e5b1813f252a4f2a00dd48ff6e" id="tgt257" class="tgtSentence">Configuración de accesorios inalámbricos</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="90138921580f59ce7fc2aa9361885759" id="tgt258" class="tgtSentence">Si habilita la configuración de accesorios inalámbricos, se agrega al proyecto el marco de accesorios externos y permite a la aplicación configurar accesorios MFi Wi-Fi.</caps:sentence>
                      </para>
                    </TD>
                    <TD></TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="32487dedb8cc91fd14da75b918ee5e6c" id="tgt259" class="tgtSentence">Pasos para habilitar derechos</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2c595786e1124c7740ef022291e7ae63" id="tgt260" class="tgtSentence">Habilite las capacidades de la aplicación:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5fa34fd383034b6057d5948e64bc016c" id="tgt261" class="tgtSentence">En Xcode, desplácese hasta el destino de la aplicación y haga clic en el panel <ui>Capacidades</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a68ab2c72225cfaf759f998f1c8dec25" id="tgt262" class="tgtSentence">Active las capacidades adecuadas.</caps:sentence>
                        <caps:sentence sentenceid="f70c241c1c3da6e95bd17e4fd272b737" id="tgt263" class="tgtSentence"> Para obtener información detallada acerca de cada capacidad y cómo determinar los valores correctos, consulte <externalLink><linkText>Agregar capacidades</linkText><linkUri>https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AddingCapabilities/AddingCapabilities.html</linkUri></externalLink> en la biblioteca para desarrolladores de iOS.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="fc7722956697fb34bd290714d92dc400" id="tgt264" class="tgtSentence">Tenga en cuenta los identificadores que haya creado durante el proceso.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="54a67fc1fa7daa81af3d43d38b8ae11b" id="tgt265" class="tgtSentence">Compile y firme la aplicación para que se realicen los ajustes oportunos.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f57c135cad9eb872c4b0d4976491625a" id="tgt266" class="tgtSentence">Habilite los derechos en el perfil de aprovisionamiento:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ae2b87edfb74f24bb40d3e3b59df067c" id="tgt267" class="tgtSentence">Inicie sesión en el Centro de usuarios registrados para desarrolladores de Apple.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="1e86203ea516f5246e67da80ee644f8f" id="tgt268" class="tgtSentence">Cree un perfil de aprovisionamiento para la aplicación.</caps:sentence>
                        <caps:sentence sentenceid="dba73f72c649c5a7c9a7b7f3cb9b69ff" id="tgt269" class="tgtSentence"> Para obtener más instrucciones, consulte <externalLink><linkText>Cómo obtener los requisitos previos para la herramienta de ajuste de aplicaciones de Intune para iOS</linkText><linkUri>http://blogs.technet.com/b/microsoftintune/archive/2015/02/25/how-to-obtain-the-prerequisites-for-the-intune-app-wrapping-tool-for-ios.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="651c5db428654e85ff4a86a287a4303e" id="tgt270" class="tgtSentence">En el perfil de aprovisionamiento, habilite los mismos derechos que tiene en su aplicación.</caps:sentence>
                        <caps:sentence sentenceid="3f37eaad031fb7f7930b952743fe7f08" id="tgt271" class="tgtSentence"> Debe proporcionar los mismos identificadores que especificó durante el desarrollo de la aplicación.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d28c824ffe8feee10a4ccce337c3ab93" id="tgt272" class="tgtSentence">Complete el Asistente para perfiles de aprovisionamiento y descargue el archivo.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="021d2b1efc61d555586bf9061564174e" id="tgt273" class="tgtSentence"> Asegúrese de que se hayan cumplido todos los requisitos previos y, a continuación, ajuste la aplicación.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="db8a565b7d306eb3247c0b37d1e9b3eb" id="tgt274" class="tgtSentence">Solucionar errores comunes con derechos</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="8e45eb914dce846691e01fd5446ca0fb" id="tgt275" class="tgtSentence"> Si la herramienta de ajuste de aplicaciones para iOS muestra un error de derecho, intente los siguientes pasos de solución de problemas.</caps:sentence>
              </para>
              <table border="1">
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0aae4c8f3cc35693d0cbbe631f2e8b52" id="tgt276" class="tgtSentence">Problema</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="560220fc3242a805f094edce47f35702" id="tgt277" class="tgtSentence">Causa</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b7e164b34ff76b1cda93a058604190da" id="tgt278" class="tgtSentence">Solución</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e2a77bd4efbfd4ba030376bbea3ebe34" id="tgt279" class="tgtSentence">Error al analizar los derechos creados a partir de la aplicación de entrada.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="74aba3543a80c70cad423bae579de095" id="tgt280" class="tgtSentence">La herramienta de ajuste de aplicaciones no puede leer el archivo de derechos que se ha extraído de la aplicación.</caps:sentence>
                        <caps:sentence sentenceid="2616591cc1451123125f8f8102212759" id="tgt281" class="tgtSentence"> Es posible que el archivo de derechos sea incorrecto.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fd09c3d575a7945367a4b13ed1aed4d9" id="tgt282" class="tgtSentence">Compruebe el archivo de derechos de la aplicación.</caps:sentence>
                        <caps:sentence sentenceid="9a95c42a4617b82a429d1360af64718b" id="tgt283" class="tgtSentence"> Para ello, siga las instrucciones que se detallan a continuación.</caps:sentence>
                        <caps:sentence sentenceid="c6ade15886ef9a0a35c2a5fcbb3e04ef" id="tgt284" class="tgtSentence"> Al inspeccionar el archivo de derechos, busque cualquier sintaxis incorrecta.</caps:sentence>
                        <caps:sentence sentenceid="1e64f43946ca6f8ebf6dd7331f20e8f5" id="tgt285" class="tgtSentence"> Recuerde que el archivo debe estar en formato XML.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="125a413de3caa6bb6b3522a05e9355d4" id="tgt286" class="tgtSentence">Faltan los derechos en el perfil de aprovisionamiento (se enumeran los derechos que faltan).</caps:sentence>
                        <caps:sentence sentenceid="e2e71d365b88780cadbc26035a037d68" id="tgt287" class="tgtSentence"> Vuelva a empaquetar la aplicación con un perfil de aprovisionamiento que tenga estos derechos.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a0c0ea8be54a2ddb4bebb8a21a9cb861" id="tgt288" class="tgtSentence">Existe una incoherencia entre los derechos habilitados en el perfil de aprovisionamiento y las capacidades habilitadas en la aplicación.</caps:sentence>
                        <caps:sentence sentenceid="5aa9ac2fec8ac91b28af08071f4d9afc" id="tgt289" class="tgtSentence"> Esta disparidad también se aplica a los identificadores de capacidades concretas (por ejemplo, grupos de aplicaciones, acceso a cadenas de claves, etc.).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f76d6d2e5d6d9d0dfd3e477508760e6e" id="tgt290" class="tgtSentence">Por lo general, puede crear un nuevo perfil de aprovisionamiento que tenga las mismas capacidades que la aplicación.</caps:sentence>
                        <caps:sentence sentenceid="75cc3a94fd5202b374723df8521bd0c3" id="tgt291" class="tgtSentence"> Cuando no coinciden los identificadores entre el perfil y la aplicación, la herramienta de ajuste de aplicaciones reemplazará los identificadores si le es posible.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="ce48106f1369258cbc96f0f14a55991c" id="tgt292" class="tgtSentence">Buscar los derechos existentes de una aplicación firmada</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="9e98cf5f815e0ec0581ef090a8cf580b" id="tgt293" class="tgtSentence">Para revisar los derechos existentes de una aplicación firmada y de un perfil de aprovisionamiento:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="bef139fa5e182a530530a0b9a0e5384d" id="tgt294" class="tgtSentence">Busque el archivo .ipa y cambie la extensión a .zip.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="108679fc99c28ba7babd522efb471ee7" id="tgt295" class="tgtSentence">Expanda el archivo .zip.</caps:sentence>
                        <caps:sentence sentenceid="d5f11d39675e8ec5eebe8665e87fb67d" id="tgt296" class="tgtSentence"> Esto creará una carpeta de carga que contiene el lote .app.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="57548cf2594ecee43c723248cc57aa10" id="tgt297" class="tgtSentence">Use la herramienta codesign para comprobar los derechos del lote .app de la siguiente manera:</caps:sentence>
                      </para>
                      <code>$ codesign -d --entitlements :- "Payload/YourApp.app"</code>
                      <para>
                        <caps:sentence sentenceid="6b9cf579910e539767e730fe9e4e9211" id="tgt298" class="tgtSentence">donde <codeInline>YourApp.app</codeInline> es el nombre del lote .app.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3b0d06cff5fc1ba5d34baf8246521dae" id="tgt299" class="tgtSentence">Use la herramienta de seguridad para comprobar los derechos del perfil de aprovisionamiento incrustado de la aplicación:</caps:sentence>
                      </para>
                      <code>$ security -D -i "Payload/YourApp.app/embedded.mobileprovision"</code>
                      <para>
                        <caps:sentence sentenceid="6b9cf579910e539767e730fe9e4e9211" id="tgt300" class="tgtSentence">donde <codeInline>YourApp.app</codeInline> es el nombre del lote .app.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="b397754eb8d845abf8bd7306799de5f5" id="tgt301" class="tgtSentence">Seguridad y privacidad de la herramienta de ajuste de aplicaciones</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="d8e81d8c53c768ce08bad19218f75a6f" id="tgt302" class="tgtSentence">Use los procedimientos recomendados de seguridad y privacidad siguientes al usar la herramienta de ajuste de aplicaciones.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="664091f503173957f36fc188eee2a118" id="tgt303" class="tgtSentence">El certificado de firma, el perfil de aprovisionamiento y la aplicación de línea de negocio que especifique deben estar en el mismo equipo Mac que use para ejecutar la herramienta de ajuste de aplicaciones.</caps:sentence>
                <caps:sentence sentenceid="ecb51848dd39bc44d9a704e9a1618931" id="tgt304" class="tgtSentence"> Si los archivos están en una ruta de acceso UNC, asegúrese de que se pueda acceder a ellos desde el equipo Mac.</caps:sentence>
                <caps:sentence sentenceid="858baf7ce71bc8409bb78eef7d84482b" id="tgt305" class="tgtSentence"> La ruta de acceso debe estar protegida mediante la firma SMB o IPsec.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="cd4b375fbb92bc1d72e59f56b4245c10" id="tgt306" class="tgtSentence">La aplicación ajustada que se importa a la consola de <token>wit_nextref</token> debe estar en el mismo equipo en el que se ejecuta la herramienta.</caps:sentence>
                <caps:sentence sentenceid="0d808b939f0baf9072dbad647e17d67c" id="tgt307" class="tgtSentence"> Si el archivo está en una ruta de acceso UNC, asegúrese de que se pueda acceder a ella desde el equipo en el que se ejecuta la consola de <token>wit_nextref</token>.</caps:sentence>
                <caps:sentence sentenceid="858baf7ce71bc8409bb78eef7d84482b" id="tgt308" class="tgtSentence"> La ruta de acceso debe estar protegida mediante la firma SMB o IPsec.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="48c07fb64c30e37ca8407a46094a9ab8" id="tgt309" class="tgtSentence">El entorno en donde se descarga la herramienta de ajuste de aplicaciones desde el sitio Centro de descarga de Microsoft debe protegerse mediante la firma SMB o IPsec.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="01015074642e0e9210326dd38208684f" id="tgt310" class="tgtSentence">La aplicación que procese debe proceder de un origen de confianza para garantizar la protección frente a ataques.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="49bd19177aee99302b8ee84c791824a9" id="tgt311" class="tgtSentence">Asegúrese de que la carpeta de salida especificada en la herramienta de ajuste de aplicaciones esté protegida, especialmente si se trata de una carpeta remota.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c4a292152809cb7793f6720a906d5f78" id="tgt312" class="tgtSentence">
            Las aplicaciones iOS que incluyen un cuadro de diálogo de carga de archivos pueden permitir a los usuarios sortear, cortar, copiar y pegar restricciones aplicadas a la aplicación.</caps:sentence>
                <caps:sentence sentenceid="e19f4eecf1e1f18cc33ceb19091f6d74" id="tgt313" class="tgtSentence"> Por ejemplo, un usuario podría usar el cuadro de diálogo de carga de archivos para cargar una captura de pantalla de los datos de aplicación.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="984d4c0c998391cabf9da32a5234a228" id="tgt314" class="tgtSentence">Cuando los usuarios supervisan la carpeta de documentos en su dispositivo desde dentro de una aplicación ajustada, puede que vean una carpeta de nombre <ui>.msftintuneapplauncher</ui>.</caps:sentence>
                <caps:sentence sentenceid="40b0d86c7cadc37200393b3932efb719" id="tgt315" class="tgtSentence"> Si esta carpeta se cambia o elimina, esto podría afectar al funcionamiento correcto de las aplicaciones restringidas.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b4fb33a8-a2fa-4353-bd89-5bda48b68e83">Protect data using mobile application management policies with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the <ui>Microsoft Intune App Wrapping Tool for iOS</ui> to modify the behavior of in-house iOS apps by restricting features of the app without changing the code of the app itself.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">The tool is a Mac OS command line application that creates a ‘wrapper’ around an app.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Once an app is processed, you can then change the apps functionality using an  <token>wit_nextref</token> mobile application management policy that you configure (see <link xlink:href="b4fb33a8-a2fa-4353-bd89-5bda48b68e83">Help secure apps using mobile application management policies with Windows Intune</link>).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">To download the tool, see <externalLink><linkText>Microsoft Intune App Wrapping Tool for iOS</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=45218</linkUri></externalLink>.</caps:sentence>
        </para>
      </introduction>
      <section address="BKMK_Prereq" expanded="true">
        <title>
          <caps:sentence id="src5" class="srcSentence">Step 1: Fulfill the prerequisites for using the app wrapping tool</caps:sentence>
        </title>
        <content>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">Requirement</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">Details and more information</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Supported operating system and toolset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">You must run the app wrapping tool on a Mac computer that runs OS X 10.8.5 or later, which has the XCode toolset version 5 or later installed.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para></para>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Signing certificate and provisioning profile</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">You must have an Apple signing certificate and provisioning profile.</caps:sentence>
                    <caps:sentence id="src12" class="srcSentence"> See your <externalLink><linkText>Apple developer documentation</linkText><linkUri>https://developer.apple.com/</linkUri></externalLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Processing an app with the App Wrapping Tool</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">To process an app with the app wrapping tool:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src15" class="srcSentence">Apps must be developed and signed by your company, or an independent software vendor (ISV).</caps:sentence>
                        <caps:sentence id="src16" class="srcSentence"> You cannot use this tool to process apps from the Apple Store.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src17" class="srcSentence">The app must be written for iOS 7.0 or later.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src18" class="srcSentence">Apps must be in the Position Independent Executable (PIE) format.</caps:sentence>
                        <caps:sentence id="src19" class="srcSentence"> For more information about the PIE format, see your Apple developer documentation.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">The app must have the extension <ui>.app</ui>, or <ui>.ipa</ui> format.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">Apps that the app wrapping tool cannot process</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">Encrypted apps</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src23" class="srcSentence">Unsigned apps</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src24" class="srcSentence">Apps with extended file attributes</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">Apps that use the Azure Active Directory Library (ADAL)</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">If your app uses ADAL:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src27" class="srcSentence">The app must incorporate an ADAL version greater than or equal to 1.0.2.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src28" class="srcSentence">The developer must grant their app access to the Intune Mobile Application Management resource.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">See <link xlink:href="99ab0369-5115-4dc8-83ea-db7239b0de97#BKMK_ADAL">Information for apps that use the Azure Active Directory Library (ADAL)</link> in this article for details about how to use ADAL.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src30" class="srcSentence">Setting entitlements for your app</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">You must set entitlements, which give the app additional permissions and capabilities beyond those typically granted, before you wrap the app.</caps:sentence>
                    <caps:sentence id="src32" class="srcSentence"> See <link xlink:href="#BKMK_ios_entitlements">Setting app entitlements</link> for instructions.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src33" class="srcSentence">Step 2: Install the app wrapping tool</caps:sentence>
        </title>
        <content>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src34" class="srcSentence">
                From the <ui>Microsoft Intune App Wrapping Tool for iOS</ui> page on the <externalLink><linkText>Microsoft Download Center</linkText><linkUri>http://www.microsoft.com/en-us/download/default.aspx</linkUri></externalLink>, download the installation file for the app wrapping tool to a Mac computer.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src35" class="srcSentence">On the Mac computer, double-click the installation file <ui>Microsoft Intune App Wrapping Tool for iOS.dmg</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src36" class="srcSentence">Click <ui>Agree</ui> to accept the End User License Agreement (EULA).</caps:sentence>
                <caps:sentence id="src37" class="srcSentence"> The installer is mounted and displayed on the Mac computer.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src38" class="srcSentence">Open the installer and  copy the displayed files to a new folder on the Mac computer.</caps:sentence>
                <caps:sentence id="src39" class="srcSentence"> You can now disconnect the mounted installer drive.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src40" class="srcSentence">You are now ready to run the app wrapping tool.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src41" class="srcSentence">Step 3: Run the app wrapping tool</caps:sentence>
        </title>
        <content>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src42" class="srcSentence">On the Mac computer, open a Terminal window and navigate to the folder where you saved the files.</caps:sentence>
                <caps:sentence id="src43" class="srcSentence"> Because the executable resides inside the package, you’ll need to run the command as follows:</caps:sentence>
              </para>
              <code>./IntuneMAMPackager.app/Contents/MacOS/IntuneMAMPackager –i /&lt;path of input app&gt;/&lt;app filename&gt; -o /&lt;path to output folder&gt;/&lt;app filename&gt; –p /&lt;path to provisioning profile&gt; –c &lt;SHA1 hash of the certificate&gt; -a &lt;client ID of input app&gt; -r &lt;reply URI of input app&gt; -v true</code>
              <alert class="note">
                <para>
                  <caps:sentence id="src44" class="srcSentence">Some parameters are optional as shown in the table below.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence id="src45" class="srcSentence">
                  <ui>Example:</ui> The following example command runs the app wrapping tool on an app named <ui>MyApp.ipa</ui>.</caps:sentence>
                <caps:sentence id="src46" class="srcSentence"> A provisioning profile and SHA-1 hash are specified.</caps:sentence>
                <caps:sentence id="src47" class="srcSentence"> The processed app is created and stored in the <ui>/users/myadmin/Documents</ui> on the Mac computer.</caps:sentence>
              </para>
              <code>/users/myadmin/Downloads/IntuneMAMPackager.app/Contents/MacOS/IntuneMAMPackager -i /users/myadmin/Downloads/MyApp.ipa -o /users/myadmin/Documents/MyApp_Wrapped.ipa -p /users/myadmin/Downloads/My_Provisioning_Profile_.mobileprovision -c 12A3BC45D67EF8901A2B3CDEF4ABC5D6E7890FAB –a 20e1cd0d-268e-4308-9583-02ae97dd353e –r https://contoso/ -v true</code>
              <para>
                <caps:sentence id="src48" class="srcSentence">You can use the following command line properties with the app wrapping tool:</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">Property</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">More information</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src51" class="srcSentence">-h</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">Displays the available command-line properties for the app wrapping tool.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src53" class="srcSentence">-i</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">Specifies the path and file name of the input app.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src55" class="srcSentence">-o</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">Specifies the path in which to save the processed app.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src57" class="srcSentence">-p</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">Specifies the path to your provisioning profile for iOS apps.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src59" class="srcSentence">-c</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src60" class="srcSentence">Specifies the SHA1 hash of the signing certificate.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src61" class="srcSentence">-a</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src62" class="srcSentence">Client ID of the input app (in GUID format) if the app uses Azure Active Directory Libraries (Optional).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src63" class="srcSentence">-r</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">Redirect URI of the input app if the app uses Azure Active Directory Libraries (Optional).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src65" class="srcSentence">-v</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">Output verbose messages to the console (Optional).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src67" class="srcSentence">After processing completes, the message <ui>The application was successfully wrapped</ui> will be displayed.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src68" class="srcSentence">If an error occurs, see <link xlink:href="99ab0369-5115-4dc8-83ea-db7239b0de97#BKMK_Error">error messages</link> for help.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src69" class="srcSentence">The wrapped app is saved in the output folder you specified previously.</caps:sentence>
                <caps:sentence id="src70" class="srcSentence"> You can now upload the app into <token>wit_nextref</token> and associate it with a mobile application management policy.</caps:sentence>
                <caps:sentence id="src71" class="srcSentence"> To learn more, see <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy software to mobile devices in Microsoft Intune</link>.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src72" class="srcSentence">You must upload the app as a new app.</caps:sentence>
                  <caps:sentence id="src73" class="srcSentence"> You cannot update an older, unwrapped version of the app.</caps:sentence>
                </para>
              </alert>
              <para>
                <caps:sentence id="src74" class="srcSentence">You can now deploy the app to your <token>wit_nextref</token> groups, and the app will now run on the device using the app restrictions you specify.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src75" class="srcSentence">Error messages and log files</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src76" class="srcSentence">Use the following information to troubleshoot issues you have with the app wrapping tool.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_Error">
            <title>
              <caps:sentence id="src77" class="srcSentence">Error messages</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src78" class="srcSentence">If the app wrapping tool fails to complete successfully, one of the following error messages will be displayed:</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src79" class="srcSentence">Error message</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">More information</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">You must specify a valid iOS provisioning profile.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src82" class="srcSentence">Your provisioning profile might not be valid.</caps:sentence>
                        <caps:sentence id="src83" class="srcSentence"> Check to make sure you have the correct permissions for devices and that your profile is correctly targeting either development or distribution.</caps:sentence>
                        <caps:sentence id="src84" class="srcSentence"> Your provisioning profile might also be expired.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src85" class="srcSentence">Specify a valid input application name.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">Make sure that the input application name you specified is correct.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">Specify a valid path to the output application.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">Make sure that the path to the output application you specified exists, and is correct.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">Specify a valid input provisioning profile.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">Make sure you supplied a valid provisioning profile name and extension.</caps:sentence>
                        <caps:sentence id="src91" class="srcSentence"> Your provisioning profile might be missing entitlements or you might not have included the <ui>–p</ui> command-line option.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">The input application you specified was not found.</caps:sentence>
                        <caps:sentence id="src93" class="srcSentence"> Specify a valid input application name and path.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src94" class="srcSentence">Make sure your input app path is valid and exists.</caps:sentence>
                        <caps:sentence id="src95" class="srcSentence"> Make sure the input app exists at that location.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src96" class="srcSentence">The input provisioning profile file you specified was not found.</caps:sentence>
                        <caps:sentence id="src97" class="srcSentence"> Specify a valid input provisioning profile file.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src98" class="srcSentence">Make sure that the path to the input provisioning file is valid and that the file you specified exists.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src99" class="srcSentence">The output application folder you specified was not found.</caps:sentence>
                        <caps:sentence id="src100" class="srcSentence"> Specify a valid path to the output application.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">Make sure that the output path you specified is valid and exists.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">Output app does not have .ipa extension.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src103" class="srcSentence">Only apps with the <ui>.app</ui> and <ui>.ipa</ui> extensions are accepted by the app wrapping tool.</caps:sentence>
                        <caps:sentence id="src104" class="srcSentence"> Make sure your output file has a valid extension.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src105" class="srcSentence">An invalid signing certificate was specified.</caps:sentence>
                        <caps:sentence id="src106" class="srcSentence"> Specify a valid Apple signing certificate.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">Make sure you’ve downloaded the correct signing certificate from the Apple developer portal.</caps:sentence>
                        <caps:sentence id="src108" class="srcSentence"> Your certificate might also be expired.</caps:sentence>
                        <caps:sentence id="src109" class="srcSentence"> If your Apple certificate and provisioning profile can be used to correctly sign an app within Xcode, then they are valid for the app wrapping tool.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src110" class="srcSentence">The input application you specified is invalid.</caps:sentence>
                        <caps:sentence id="src111" class="srcSentence"> Specify a valid application.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src112" class="srcSentence">Make sure you have a valid iOS application that has been compiled as an .app or .ipa file.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src113" class="srcSentence">The input application you specified is encrypted.</caps:sentence>
                        <caps:sentence id="src114" class="srcSentence"> Specify a valid unencrypted application.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src115" class="srcSentence">The app wrapping tool does not support encrypted apps.</caps:sentence>
                        <caps:sentence id="src116" class="srcSentence"> Specify an unencrypted app.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src117" class="srcSentence">The input application you specified is not in a Position Independent Executable (PIE) format.</caps:sentence>
                        <caps:sentence id="src118" class="srcSentence"> Specify a valid application in PIE format.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">Position Independent Executable (PIE) apps can be loaded at a random memory address when run which can have security benefits.</caps:sentence>
                        <caps:sentence id="src120" class="srcSentence"> For more information, see your Apple Developer documentation.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src121" class="srcSentence">The input app you specified has already been wrapped.</caps:sentence>
                        <caps:sentence id="src122" class="srcSentence"> Specify a valid unwrapped application.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src123" class="srcSentence">You cannot process an app that has already been processed by the tool.</caps:sentence>
                        <caps:sentence id="src124" class="srcSentence"> If you want to process an app again, run the tool using the original version of the app.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src125" class="srcSentence">The input application you specified is not signed.</caps:sentence>
                        <caps:sentence id="src126" class="srcSentence"> Specify a valid signed application.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src127" class="srcSentence">The app wrapping tool requires apps to be signed.</caps:sentence>
                        <caps:sentence id="src128" class="srcSentence"> Consult your developer documentation to learn how to sign a wrapped app.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src129" class="srcSentence">The input application you specified must be in the .ipa or .app format.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src130" class="srcSentence">Only .app and .ipa extensions are accepted by the app wrapping tool.</caps:sentence>
                        <caps:sentence id="src131" class="srcSentence"> Make sure your input file has a valid extension and has been compiled as a .app or .ipa file.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src132" class="srcSentence">The input app you specified has already been wrapped and is on the latest policy template version.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src133" class="srcSentence">The app wrapping tool will not rewrap an existing wrapped app with the latest policy template version.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src134" class="srcSentence">The given Azure Active Directory Client ID not a well-formed GUID.</caps:sentence>
                        <caps:sentence id="src135" class="srcSentence"> Please specify a valid Client ID.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src136" class="srcSentence">When using the Client ID parameter, make sure you’ve provided a valid Client ID in GUID format.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src137" class="srcSentence">The given Azure Active Directory reply URI is not a well-formed URI.</caps:sentence>
                        <caps:sentence id="src138" class="srcSentence"> Please specify a valid reply URI.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src139" class="srcSentence">When using the reply URI command line property, make sure you’ve provided a valid reply URI.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src140" class="srcSentence">WARNING: You did not specify a SHA1 certificate hash.</caps:sentence>
                        <caps:sentence id="src141" class="srcSentence"> Make sure that your wrapped application is signed before deploying.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src142" class="srcSentence">Ensure that you specify a valid SHA hash (using the <ui>–c</ui> command line property).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src143" class="srcSentence">Log files for the app wrapping tool</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src144" class="srcSentence">Apps that have been wrapped by using the app wrapping tool generate logs which are written to the iOS client device console.</caps:sentence>
                <caps:sentence id="src145" class="srcSentence"> This information is useful in situations where you are having problems with the application and need to diagnose if the issue is related to the app wrapping tool.</caps:sentence>
                <caps:sentence id="src146" class="srcSentence"> To retrieve this information, use the following steps:</caps:sentence>
              </para>
              <procedure>
                <title></title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src147" class="srcSentence">Reproduce the issue by running the app.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src148" class="srcSentence">Collect the console output by following Apple's instructions for <externalLink><linkText>Debugging Deployed iOS Apps</linkText><linkUri>https://developer.apple.com/library/ios/qa/qa1747/_index.html</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src149" class="srcSentence">Filter the saved logs for App Restrictions output by entering the following script into the console:</caps:sentence>
                      </para>
                      <code>grep “IntuneAppRestrictions” &lt;text file containing console output&gt; &gt; &lt;required filtered log file name&gt; </code>
                      <para>
                        <caps:sentence id="src150" class="srcSentence">You can submit the filtered logs to Microsoft.</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src151" class="srcSentence">In the log file, the item ‘build version’ represents the build version of Xcode.</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence id="src152" class="srcSentence">Wrapped apps will also present users the option to send logs directly from the device via email after the app crashes.</caps:sentence>
                        <caps:sentence id="src153" class="srcSentence"> Users can send the log to you to examine and forward to Microsoft if required.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_ADAL" expanded="true">
            <title>
              <caps:sentence id="src154" class="srcSentence">
          Information for apps that use the Azure Active Directory Library (ADAL)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src155" class="srcSentence">The information in this section applies only to apps that use the Azure Active Directory Library (ADAL).</caps:sentence>
                <caps:sentence id="src156" class="srcSentence"> If you are unsure if your app uses this library, contact the developer of the app.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src157" class="srcSentence">The app must incorporate an ADAL version greater than or equal to 1.0.2.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src158" class="srcSentence">For apps that use ADAL, the following must be true:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src159" class="srcSentence">The app must incorporate an ADAL version greater than or equal to 1.0.2</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">Developers must grant their app access to the Intune Mobile Application Management resource, as described in <link xlink:href="#BKMK_step_use_adal">Steps to follow for apps that use ADAL</link>.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
            <sections>
              <section address="BKMK_adal_overview">
                <title>
                  <caps:sentence id="src161" class="srcSentence">Overview of identifiers you need to get</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">Apps that use ADAL must register via the Azure management portal to obtain two unique identifiers for their app:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src163" class="srcSentence">Identifier</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src164" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src165" class="srcSentence">Default value</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src166" class="srcSentence">Client ID</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src167" class="srcSentence">A unique GUID identifier is generated for each app after it registers with Azure Active Directory.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src168" class="srcSentence">If you know the app's specific client ID, you can specify this value.</caps:sentence>
                            <caps:sentence id="src169" class="srcSentence"> Otherwise, the default value must be used.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src170" class="srcSentence">6c7e8096-f593-4d72-807f-a5f86dcc9c77</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src171" class="srcSentence">Redirect URI</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src172" class="srcSentence">A URI value that developers can provide when registering their app with Azure Active Directory to ensure that authentication tokens are returned specifically to that endpoint.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src173" class="srcSentence">Supplying a redirect URI is an optional parameter for the app wrapping tool.</caps:sentence>
                            <caps:sentence id="src174" class="srcSentence"> If it is not specified, a default URI will be used.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src175" class="srcSentence">urn:ietf:wg:oauth:2.0:oob</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">When you do not supply the above values to the tool; the following additional values are automatically used:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src177" class="srcSentence">
                          <ui>Authority URI</ui> - https://login.windows.net/common/oauth2/authorize</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src178" class="srcSentence">
                          <ui>Resource ID</ui> - https://intunemam.microsoft.com</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </section>
              <section address="BKMK_step_use_adal">
                <title>
                  <caps:sentence id="src179" class="srcSentence">Steps to follow for apps that use ADAL</caps:sentence>
                </title>
                <content>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src180" class="srcSentence">Review <link xlink:href="#BKMK_adal_overview">Overview of identifiers you need to get</link> to identify the values that you need to get.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src181" class="srcSentence">Configure access to mobile application management in Azure Active Directory by doing the following:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src182" class="srcSentence">Log into an existing Azure Active Directory account in the Azure management portal.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src183" class="srcSentence">Click <ui>existing LOB application registration</ui> in Azure Active Directory.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src184" class="srcSentence">In the configure section, choose <ui>Configure Access to Web APIs in other applications</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src185" class="srcSentence">In the <ui>Permission to other applications</ui> section, from the first drop-down list, choose <ui>Intune Mobile Application Management</ui>.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src186" class="srcSentence">You can now use the app's Client ID in the app wrapping tool.</caps:sentence>
                            <caps:sentence id="src187" class="srcSentence"> You can find the app's Client ID in the Azure Active Directory management portal as described in the <link xlink:href="#BKMK_adal_overview">Overview of identifiers you need to get</link> section.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src188" class="srcSentence">Use the <ui>Client-ID</ui> (using the property <ui>–a</ui>) and <ui>Redirect-URI</ui> values as command-line properties in the app wrapping tool.</caps:sentence>
                        <caps:sentence id="src189" class="srcSentence"> If you do not have these values, the default values are used.</caps:sentence>
                        <caps:sentence id="src190" class="srcSentence"> You must specify both values, or the end user will not be able to successfully authenticate the processed app.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence id="src191" class="srcSentence">Certificate, provisioning profile, and authentication requirements</caps:sentence>
                </title>
                <content>
                  <table border="1">
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src192" class="srcSentence">Requirement</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src193" class="srcSentence">Details</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src194" class="srcSentence">Provisioning profile</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src195" class="srcSentence">
                              <ui>Make sure that the provisioning profile is valid before you include it</ui> - The app wrapping tool does not check whether the provisioning profile is expired when processing an iOS app.</caps:sentence>
                            <caps:sentence id="src196" class="srcSentence"> If an expired provisioning profile is specified, the app wrapping tool will include the expired provisioning profile, and you will not know there is a problem until the app fails to install on an iOS device.</caps:sentence> </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src197" class="srcSentence">Certificate</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src198" class="srcSentence">
                                  <ui>Make sure that the certificate is valid before you specify it</ui> - The tool does not check whether a certificate is expired when processing iOS apps.</caps:sentence>
                                <caps:sentence id="src199" class="srcSentence"> If the hash for an expired certificate is provided, the tool will process and sign the app, but it will fail to install on devices.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src200" class="srcSentence">
                                  <ui>Make sure that the certificate provided for signing the packaged application has a match in the provisioning profile</ui> - The tool does not validate if the provisioning profile has a match for the certificate provided for signing the wrapped application.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src201" class="srcSentence">Authentication</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src202" class="srcSentence">On devices to which you have deployed a wrapped application, touching the status bar on the device will require the user to re-authenticate with <token>wit_nextref</token>.</caps:sentence>
                                <caps:sentence id="src203" class="srcSentence"> The default policy in a wrapped application is <legacyItalic>authentication on re-launch</legacyItalic>.</caps:sentence>
                                <caps:sentence id="src204" class="srcSentence"> iOS handles any external notification (for example a phone call) as exiting the app and then re-launching it.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src205" class="srcSentence">A device must have a pin set for encryption to work.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src206" class="srcSentence">For wrapped apps, the first user who signs into any wrapped app from the same publisher is cached.</caps:sentence>
                                <caps:sentence id="src207" class="srcSentence"> After this point, only that user is allowed to access the app.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src208" class="srcSentence">To reset the user, the device has to be unenrolled and then re-enrolled.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence id="src209" class="srcSentence">Troubleshooting and technical notes about ADAP</caps:sentence>
                </title>
                <content>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src210" class="srcSentence">If no ADAL resources are found, the tool will include the ADAL dynamic library.</caps:sentence>
                        <caps:sentence id="src211" class="srcSentence"> The tool will search for the ADAL library with a name of <ui>ADALiOS.bundle</ui> in the root folder.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src212" class="srcSentence">The tool does not search for ADAL binaries (if any) within the app.</caps:sentence>
                        <caps:sentence id="src213" class="srcSentence"> If the app links to an outdated version, there may be runtime errors during login if authentication policies are enabled.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src214" class="srcSentence">
                          <token>wit_nextref</token> fetches the AAD token to the <token>wit_nextref</token> MAM resource-id for authentication.</caps:sentence>
                        <caps:sentence id="src215" class="srcSentence"> However, it is not used in any call that would in-turn verify the validity of the token.</caps:sentence>
                        <caps:sentence id="src216" class="srcSentence">
                          <token>wit_nextref</token> only reads the UPN of the signed-in user to determine app access.</caps:sentence>
                        <caps:sentence id="src217" class="srcSentence"> The AAD token is not used for any further service calls.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src218" class="srcSentence">Authentication tokens are shared between apps from the same publisher since they are stored in shared keychain.</caps:sentence>
                        <caps:sentence id="src219" class="srcSentence"> If you want to isolate a specific app, then you must use a different signing certificate and provisioning profile for that app.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src220" class="srcSentence">Double login prompts are prevented if you provide your client application’s Client ID and Redirect URI.</caps:sentence>
                        <caps:sentence id="src221" class="srcSentence"> This Client ID needs to be registered to access the published <token>wit_nextref</token> MAM resource ID in the AAD Dashboard.</caps:sentence>
                        <caps:sentence id="src222" class="srcSentence"> Failure to do so will result in a login failure when the app runs.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <section address="BKMK_ios_entitlements">
        <title>
          <caps:sentence id="src223" class="srcSentence">Setting app entitlements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src224" class="srcSentence">Before wrapping your app, you can grant <ui>entitlements</ui> to give the app  additional permissions and capabilities that exceed what an app typically can do.</caps:sentence>
            <caps:sentence id="src225" class="srcSentence">   An <ui>entitlement file</ui> is used during code signing to specify special permissions within your app (for example, access to a shared keychain).</caps:sentence>
            <caps:sentence id="src226" class="srcSentence"> Specific app services, called <ui>capabilities</ui>, are enabled within Xcode during app development.</caps:sentence>
            <caps:sentence id="src227" class="srcSentence"> Once enabled, the capabilities are reflected in your entitlements file.</caps:sentence>
            <caps:sentence id="src228" class="srcSentence"> For more information about entitlements and capabilities, see <externalLink><linkText>Adding Capabilities</linkText><linkUri>https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AddingCapabilities/AddingCapabilities.html</linkUri></externalLink> in the iOS Developer Library.</caps:sentence>
            <caps:sentence id="src229" class="srcSentence"> For a complete list of supported capabilities, see <externalLink><linkText>Supported capabilities</linkText><linkUri>https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/SupportedCapabilities/SupportedCapabilities.html</linkUri></externalLink>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src230" class="srcSentence">Supported capabilities for the App Wrapping Tool for iOS</caps:sentence>
            </title>
            <content>
              <table border="1">
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src231" class="srcSentence">Capability</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src232" class="srcSentence">Description</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src233" class="srcSentence">Recommended guidance</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src234" class="srcSentence">App Groups</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src235" class="srcSentence">Use app groups to allow multiple apps to access shared containers and allow additional inter-process communication between apps.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src236" class="srcSentence">To enable app groups, open the <ui>Capabilities</ui> pane and click the <ui>ON</ui> switch in the <ui>App Groups </ui>section.</caps:sentence>
                        <caps:sentence id="src237" class="srcSentence"> You can add app groups or select existing ones.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src238" class="srcSentence">When using App Groups, use reverse DNS notation:</caps:sentence>
                      </para>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src239" class="srcSentence">group.com.companyName.AppGroup</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src240" class="srcSentence">Background Modes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <caps:sentence id="src241" class="srcSentence"> <para>Enabling background modes allows your iOS app to continue running in the background.</para></caps:sentence>
                    </TD>
                    <TD></TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src242" class="srcSentence">Data Protection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <caps:sentence id="src243" class="srcSentence"> <para>Data protection adds a level of security to files stored on disk by your iOS app. Data protection uses the built-in encryption hardware present on specific devices to store files in an encrypted format on disk. Your app needs to be provisioned to use data protection.</para></caps:sentence>
                    </TD>
                    <TD></TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src244" class="srcSentence">In-App Purchase</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src245" class="srcSentence">In-App purchase embeds a store directly into your app by enabling you to connect to the store and securely process payments from the user.</caps:sentence>
                        <caps:sentence id="src246" class="srcSentence"> You can use In-App Purchase to collect payment for enhanced functionality or for additional content usable by your app.</caps:sentence>
                      </para>
                    </TD>
                    <TD></TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src247" class="srcSentence">Keychain Sharing</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src248" class="srcSentence">Enabling keychain sharing allows your app to share passwords in the keychain with other apps developed by your team.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src249" class="srcSentence">When using Keychain Sharing, use reverse DNS notation:</caps:sentence>
                      </para>
                      <para>
                        <legacyItalic>
                          <caps:sentence id="src250" class="srcSentence">com.companyName.KeychainGroup</caps:sentence>
                        </legacyItalic>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src251" class="srcSentence">Personal VPN</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src252" class="srcSentence">Enable personal VPN to allow your app to create and control a custom system VPN configuration using the Network Extension framework.</caps:sentence>
                      </para>
                    </TD>
                    <TD></TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src253" class="srcSentence">Push Notifications</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src254" class="srcSentence">Apple Push Notification service (APNs) allows an app that isn’t running in the foreground to notify the user that it has information for the user.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src255" class="srcSentence">For push notifications to work, you need to use an app-specific provisioning profile.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src256" class="srcSentence">Follow the steps in the <externalLink><linkText>Apple developer documentation</linkText><linkUri>https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AddingCapabilities/AddingCapabilities.html</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src257" class="srcSentence">Wireless Accessory Configuration</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src258" class="srcSentence">Enabling wireless accessory configuration adds the External Accessory framework to your project and allows your app to configure MFi Wi-Fi accessories.</caps:sentence>
                      </para>
                    </TD>
                    <TD></TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src259" class="srcSentence">Steps to enable entitlements</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src260" class="srcSentence">Enable capabilities in your app:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src261" class="srcSentence">In Xcode, navigate to your app’s target, and click the <ui>Capabilities</ui> pane.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src262" class="srcSentence">Turn on the appropriate capabilities.</caps:sentence>
                        <caps:sentence id="src263" class="srcSentence"> For detailed information about each capability and how to determine the correct values, see <externalLink><linkText>Adding Capabilities</linkText><linkUri>https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AddingCapabilities/AddingCapabilities.html</linkUri></externalLink> in the iOS Developer Library.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src264" class="srcSentence">Note any IDs that you created during the process.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src265" class="srcSentence">Build and sign your app to be wrapped.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src266" class="srcSentence">Enable entitlements in your provisioning profile:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src267" class="srcSentence">Log in to the Apple Developer Member Center.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src268" class="srcSentence">Create a provisioning profile for your app.</caps:sentence>
                        <caps:sentence id="src269" class="srcSentence"> For instructions, see <externalLink><linkText>How to Obtain the Prerequisites for the Intune App Wrapping Tool for iOS</linkText><linkUri>http://blogs.technet.com/b/microsoftintune/archive/2015/02/25/how-to-obtain-the-prerequisites-for-the-intune-app-wrapping-tool-for-ios.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src270" class="srcSentence">In your provisioning profile, enable the same entitlements that you have in your app.</caps:sentence>
                        <caps:sentence id="src271" class="srcSentence"> You will need to supply the same IDs that you specified during the development of your app.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src272" class="srcSentence">Complete the provisioning profile wizard and download your file.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src273" class="srcSentence"> Ensure that you have satisfied all the prerequisites, and then wrap the app.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src274" class="srcSentence">Troubleshooting common errors with entitlements</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src275" class="srcSentence"> If the App Wrapping Tool for iOS displays an entitlement error, try the following troubleshooting steps.</caps:sentence>
              </para>
              <table border="1">
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src276" class="srcSentence">Issue</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src277" class="srcSentence">Cause</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src278" class="srcSentence">Resolution</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src279" class="srcSentence">Failed to parse entitlements generated from the input application.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src280" class="srcSentence">The App Wrapping Tool cannot read the entitlements file that was extracted from the app.</caps:sentence>
                        <caps:sentence id="src281" class="srcSentence"> The entitlements file might be malformed.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src282" class="srcSentence">Inspect the entitlements file for your app.</caps:sentence>
                        <caps:sentence id="src283" class="srcSentence"> To do so, follow the instructions detailed below.</caps:sentence>
                        <caps:sentence id="src284" class="srcSentence"> When inspecting the entitlements file, check for any malformed syntax.</caps:sentence>
                        <caps:sentence id="src285" class="srcSentence"> The file should be in XML format.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src286" class="srcSentence">Entitlements are missing in the provisioning profile (missing entitlements are listed).</caps:sentence>
                        <caps:sentence id="src287" class="srcSentence"> Repackage the app with a provisioning profile that has these entitlements.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src288" class="srcSentence">There is a mismatch between the entitlements enabled in the provisioning profile and the capabilities enabled in the app.</caps:sentence>
                        <caps:sentence id="src289" class="srcSentence"> This mismatch also applies to the IDs associated with particular capabilities (i.e., App Groups, Keychain Access etc).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src290" class="srcSentence">Generally, you can create a new provisioning profile that enables the same capabilities as the app.</caps:sentence>
                        <caps:sentence id="src291" class="srcSentence"> When IDs between the profile and app don't match, the App Wrapping Tool will replace the IDs if it is able to.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src292" class="srcSentence">Finding the existing entitlements of a signed app</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src293" class="srcSentence">To review the existing entitlements of a signed app and provisioning profile:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src294" class="srcSentence">Find the .ipa file and change its the extension to .zip.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src295" class="srcSentence">Expand the .zip file.</caps:sentence>
                        <caps:sentence id="src296" class="srcSentence"> This will produce a Payload folder containing your .app bundle.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src297" class="srcSentence">Use the codesign tool to check the entitlements on the .app bundle like this:</caps:sentence>
                      </para>
                      <code>$ codesign -d --entitlements :- "Payload/YourApp.app"</code>
                      <para>
                        <caps:sentence id="src298" class="srcSentence">where <codeInline>YourApp.app</codeInline> is the actual name of your .app bundle.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src299" class="srcSentence">Use the security tool to check the entitlements of the app's embedded provisioning profile:</caps:sentence>
                      </para>
                      <code>$ security -D -i "Payload/YourApp.app/embedded.mobileprovision"</code>
                      <para>
                        <caps:sentence id="src300" class="srcSentence">where <codeInline>YourApp.app</codeInline> is the actual name of your .app bundle.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src301" class="srcSentence">Security and privacy for the app wrapping tool</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src302" class="srcSentence">Use the following security and privacy best practices when you use the app wrapping tool.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src303" class="srcSentence">The signing certificate, provisioning profile and the line-of-business app you specify must be on the same Mac computer that you use to run the app wrapping tool.</caps:sentence>
                <caps:sentence id="src304" class="srcSentence"> If the files are on a UNC path, ensure that these are accessible from the Mac computer.</caps:sentence>
                <caps:sentence id="src305" class="srcSentence"> The path must be secured via IPsec or SMB signing.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src306" class="srcSentence">The wrapped application imported into the <token>wit_nextref</token> console should be on the same computer that you run the tool on.</caps:sentence>
                <caps:sentence id="src307" class="srcSentence"> If the file is on a UNC path, ensure that it is accessible on the computer running the <token>wit_nextref</token> console.</caps:sentence>
                <caps:sentence id="src308" class="srcSentence"> The path must be secured via IPsec or SMB signing.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src309" class="srcSentence">The environment where the app wrapping tool is downloaded from the Microsoft Download Center site needs to be secured via IPsec or SMB signing.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src310" class="srcSentence">The app you process must come from a trust-worthy source to ensure protection against attacks.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src311" class="srcSentence">Ensure that the output folder you specify in the app wrapping tool is secured, particularly if it is a remote folder.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src312" class="srcSentence">
            iOS apps that include a file upload dialog box can allow users to circumvent cut, copy and paste restrictions applied to the app.</caps:sentence>
                <caps:sentence id="src313" class="srcSentence"> For example, a user could use the file upload dialog box to upload a screenshot of the app data.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src314" class="srcSentence">When users monitor the documents folder on their device from within a wrapped app, they might see a folder named <ui>.msftintuneapplauncher</ui>.</caps:sentence>
                <caps:sentence id="src315" class="srcSentence"> If this folder is changed or deleted, this might affect the correct functioning of restricted apps.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="b4fb33a8-a2fa-4353-bd89-5bda48b68e83">Protect data using mobile application management policies with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>