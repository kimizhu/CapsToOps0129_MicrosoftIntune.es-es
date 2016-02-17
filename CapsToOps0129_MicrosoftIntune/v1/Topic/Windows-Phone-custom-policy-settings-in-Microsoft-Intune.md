---
title: Configuraci&#243;n de directivas personalizadas de Windows Phone en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f64674ff-f2a6-471c-82a5-bcff23c7514d
---
# Configuraci&#243;n de directivas personalizadas de Windows Phone en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt1" class="tgtSentence">Use la <ui>Directiva de configuración personalizada de Windows Phone</ui> de <token>wit_firstref</token> para implementar la configuración de OMA-URI (identificador uniforme de recursos de Open Mobile Alliance), que puede usarse para controlar las características de los <ui>dispositivos de Windows Phone 8.1</ui>.</caps:sentence>
          <caps:sentence sentenceid="8d40fac4ac37509f820ec2d303c38d24" id="tgt2" class="tgtSentence"> Se trata de una configuración estándar que muchos fabricantes de dispositivos móviles usan para controlar las características del dispositivo.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="740e1cccdf53ee0dabd853b8b086bcf1" id="tgt3" class="tgtSentence">Esta capacidad está destinada a permitirle implementar la configuración de Windows Phone que no se puede configurar con una directiva de <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence sentenceid="4c4623cc4a431eaa78a301d7856090ea" id="tgt4" class="tgtSentence"> Para obtener información acerca de las opciones que se pueden configurar con estas directivas, consulte <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Configure security policy for mobile devices in Microsoft Intune</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ca46ecafdc32d32a12198405fe486d1d" id="tgt5" class="tgtSentence">Para obtener ayuda acerca de cómo crear la configuración de OMA-URI para dispositivos Windows Phone, consulte <externalLink><linkText>Windows Phone 8.1 MDM protocol documentation</linkText><linkUri>http://technet.microsoft.com/library/dn499787.aspx</linkUri></externalLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="02974e48cd252545f6e50c0ad5e5cfcf" id="tgt6" class="tgtSentence">Cómo crear una directiva personalizada de Windows Phone</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt7" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Agregar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt8" class="tgtSentence">En <ui>Windows</ui>, configure una directiva de <ui>configuración personalizada (Windows Phone 8.1 y versiones posteriores)</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="3a9e7333b5e01181a60ae01e405e944d" id="tgt9" class="tgtSentence">Para crear e implementar directivas fácilmente, consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="b8552549ca9d61b8cbd3fd8fdc23942a" id="tgt10" class="tgtSentence">Solo puede crear e implementar una directiva personalizada.</caps:sentence>
                    <caps:sentence sentenceid="e3b2888d8f4d059bda2997d26638a507" id="tgt11" class="tgtSentence"> La configuración recomendada no está disponible.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="606f1d2158988f6e69e06586b9f24c1d" id="tgt12" class="tgtSentence">La tabla siguiente le facilitará la configuración de directivas generales:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt13" class="tgtSentence">Nombre de la configuración</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt14" class="tgtSentence">Más información</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt15" class="tgtSentence">Nombre</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="582a4cb91381a72640e40bab04a45d3b" id="tgt16" class="tgtSentence">Escriba un nombre único para la directiva que le ayude a identificarla en la consola de <token>wit_nextref</token>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt17" class="tgtSentence">Descripción</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="784a907294c7a707bbb92bf99416cf0b" id="tgt18" class="tgtSentence">Proporcione una descripción general de la directiva y otra información relevante que le ayude a encontrarla.</caps:sentence>
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
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt19" class="tgtSentence">En la sección <ui>Configuración OMA-URI</ui>, haga clic en <ui>Agregar</ui> para agregar un valor.</caps:sentence>
                    <caps:sentence sentenceid="d02e9eef2acac6cb33d9b16639243048" id="tgt20" class="tgtSentence"> También puede editar o eliminar un valor existente.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt21" class="tgtSentence">En el cuadro de diálogo <ui>Agregar o editar configuración OMA-URI</ui>, especifique la siguiente información:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="447b7147e84be512208dcc0995d67ebc" id="tgt22" class="tgtSentence">Elemento</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt23" class="tgtSentence">Más información</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt24" class="tgtSentence">Nombre de la configuración</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b25be43287736dc29249283789580234" id="tgt25" class="tgtSentence">Escriba un nombre único para el valor OMA-URI que le ayude a identificarlo en la lista de valores de configuración.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="6754b3fdad38016213d4b9d46256de42" id="tgt26" class="tgtSentence">Descripción del valor</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="62493ef9a08271cdd406c1864a42de5f" id="tgt27" class="tgtSentence">Proporcione una descripción que ofrezca una visión general del valor y otra información relevante que le ayude a encontrarlo.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="1443a7220ce58bf7476b59728760e6f7" id="tgt28" class="tgtSentence">Tipo de datos</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="68c572e87552f9ec55886c4212f96685" id="tgt29" class="tgtSentence">Seleccione el tipo de fecha en que especificará este valor OMA-URI.</caps:sentence>
                            <caps:sentence sentenceid="a286929ca0f740e14eb1d567ac54d6cb" id="tgt30" class="tgtSentence"> Elija de entre las siguientes opciones:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="b45cffe084dd3d20d928bee85e7b0f21" id="tgt31" class="tgtSentence">String</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="573bb660411b4996a98b98028247498b" id="tgt32" class="tgtSentence">Cadena (XML)</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="88412b82a0b294501c4de9d554a6494e" id="tgt33" class="tgtSentence">Fecha y hora</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="157db7df530023575515d366c9b672e8" id="tgt34" class="tgtSentence">Integer</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="1403c9489f9bb53f4e3a25339d22eebb" id="tgt35" class="tgtSentence">Punto flotante</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="84e2c64f38f78ba3ea5c905ab5a2da27" id="tgt36" class="tgtSentence">Boolean</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="45ba21357c2a6fc435ad3d9b494a7071" id="tgt37" class="tgtSentence">OMA-URI (distingue mayúsculas de minúsculas)</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9415acd2602a372a442381707563fcc8" id="tgt38" class="tgtSentence">Especifique el OMA-URI para el que desee suministrar un valor.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt39" class="tgtSentence">Valor</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="7217f3564ec322de578b94b7c66f7cb7" id="tgt40" class="tgtSentence">Especifique el valor asociado con el OMA-URI especificado anteriormente.</caps:sentence>
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
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt41" class="tgtSentence">Haga clic en <ui>Aceptar</ui> para guardar el valor y volver a la página <ui>Crear directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="27112a11f9261caf4068fbcbe965797f" id="tgt42" class="tgtSentence">Continúe agregando tantos valores como sea necesario.</caps:sentence>
                    <caps:sentence sentenceid="118fb1a3f502368b3803f2a34a6170ec" id="tgt43" class="tgtSentence"> Cuando haya terminado, haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt44" class="tgtSentence">La nueva directiva se muestra en el nodo <ui>Directivas de configuración</ui> del área de trabajo <ui>Directiva</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="13104cbd3fc767ee4b1b96b2abf63645" id="tgt45" class="tgtSentence">Implementar una directiva personalizada de Windows Phone</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1745f7882002f41f4d1346b36d0cf8fc" id="tgt46" class="tgtSentence">Implemente la directiva en uno o más grupos de usuarios o dispositivos de su organización.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="ad5c1bcb5291ef46b20f2e8f623f5ca4" id="tgt47" class="tgtSentence">Para obtener más información sobre cómo implementar directivas, consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="01d86b2114262db694dc64c0bb564e2d" id="tgt48" class="tgtSentence">En el área de trabajo <ui>Directiva</ui> de la página <ui>General</ui>, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención.</caps:sentence>
                  <caps:sentence sentenceid="f38e8d4a29f6e64f69b2faa73bb44771" id="tgt49" class="tgtSentence"> Además, aparece un resumen de estado en el área de trabajo <ui>Panel</ui>.</caps:sentence>
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
          <caps:sentence id="src1" class="srcSentence">Use the <token>wit_firstref</token> <ui>Windows Phone custom configuration policy</ui> to deploy OMA-URI (Open Mobile Alliance Uniform Resource Identifier) settings that can be used to control features on <ui>Windows Phone 8.1 devices</ui>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> These are standard settings that many mobile device manufacturers use to control device features.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">This capability is intended to allow you to deploy Windows Phone settings that are not configurable with an <token>wit_nextref</token> policy.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For information about the settings you can configure with these policies, see <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Configure security policy for mobile devices in Microsoft Intune</link>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">For help creating OMA-URI settings for Windows Phone devices, see <externalLink><linkText>Windows Phone 8.1 MDM protocol documentation</linkText><linkUri>http://technet.microsoft.com/library/dn499787.aspx</linkUri></externalLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">How to create a Windows Phone custom policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Under <ui>Windows</ui>, configure a <ui>Custom Configuration (Windows Phone 8.1 and later)</ui> policy.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">For help creating and deploying policies, see the <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices in Windows Intune</link>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">You can only create and deploy a custom policy.</caps:sentence>
                    <caps:sentence id="src11" class="srcSentence"> Recommended settings are not available.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Use the following table to help you configure the general policy settings:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src13" class="srcSentence">Setting name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src14" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src15" class="srcSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src16" class="srcSentence">Enter a unique name for the policy to help you identify it in the <token>wit_nextref</token> console.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src17" class="srcSentence">Description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src18" class="srcSentence">Provide a description that gives an overview of the policy and other relevant information that helps you to locate it.</caps:sentence>
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
                    <caps:sentence id="src19" class="srcSentence">In the <ui>OMA-URI Settings</ui> section, click <ui>Add</ui> to add a setting.</caps:sentence>
                    <caps:sentence id="src20" class="srcSentence"> You can also edit or delete an existing setting.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">In the <ui>Add or Edit OMA-URI</ui> Setting dialog box, specify the following information:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src22" class="srcSentence">Item</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src23" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src24" class="srcSentence">Setting name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src25" class="srcSentence">Enter a unique name for the OMA-URI setting to help you identify it in the list of settings.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src26" class="srcSentence">Setting description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src27" class="srcSentence">Provide a description that gives an overview of the setting and other relevant information to help you locate it.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src28" class="srcSentence">Data type</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src29" class="srcSentence">Select the date type in which you will specify this OMA-URI setting.</caps:sentence>
                            <caps:sentence id="src30" class="srcSentence"> Choose from:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src31" class="srcSentence">String</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src32" class="srcSentence">String (XML)</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src33" class="srcSentence">Date and time</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src34" class="srcSentence">Integer</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src35" class="srcSentence">Floating point</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src36" class="srcSentence">Boolean</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src37" class="srcSentence">OMA-URI (Case Sensitive)</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src38" class="srcSentence">Specify the OMA-URI you want to supply a setting for.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src39" class="srcSentence">Value</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src40" class="srcSentence">Specify the value to associate with the OMA-URI you specified previously.</caps:sentence>
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
                    <caps:sentence id="src41" class="srcSentence">Click <ui>OK</ui> to save the setting and return to the <ui>Create Policy</ui> page.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Continue to add as many settings as you require.</caps:sentence>
                    <caps:sentence id="src43" class="srcSentence"> When you are done, click <ui>Save Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src44" class="srcSentence">The new policy displays in the <ui>Configuration Policies</ui> node of the <ui>Policy</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src45" class="srcSentence">Deploy a Windows Phone Custom policy</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">Deploy the policy to one or more groups of users or devices in your organization.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src47" class="srcSentence">For more information about how to deploy policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src48" class="srcSentence">A status summary and alerts on the <ui>Overview</ui> page of the <ui>Policy</ui> workspace identify issues with the policy that require your attention.</caps:sentence>
                  <caps:sentence id="src49" class="srcSentence"> Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</caps:sentence>
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