---
title: Controlar los contenidos que los administradores pueden ver en la consola de administraci&#243;n de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e0783eaa-67dc-410e-9e80-4d3aa72f36d8
---
# Controlar los contenidos que los administradores pueden ver en la consola de administraci&#243;n de Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c738828c153d16ac15927ca499cabb62" id="tgt1" class="tgtSentence">
            <token>wit_nextref</token> proporciona la capacidad para filtrar la vista de la consola de administración para permitir que los usuarios accedan solo a los elementos que desee que vean.</caps:sentence>
          <caps:sentence sentenceid="cb218659fb6d52f74e82ab2b3f936d23" id="tgt2" class="tgtSentence"> Por ejemplo, quizás desee que solo los operadores de la consola de administración puedan actualizar definiciones de malware o restablecer la contraseña en los dispositivos.</caps:sentence>
          <caps:sentence sentenceid="42cbd8b3a6a10f3ec1f627a1d72a658e" id="tgt3" class="tgtSentence"> Esto se logra mediante <ui>designaciones</ui> preestablecidas que se asignan a usuarios específicos.</caps:sentence>
          <caps:sentence sentenceid="fe5fbe38d0024c0978d4dd985ae3750d" id="tgt4" class="tgtSentence"> Cuando estos usuarios acceden a la consola de administración, solo ven los elementos específicos de su designación.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fc64a6d3deb8eb93d01992be465828bd" id="tgt5" class="tgtSentence">Utilice esta característica para asignar tareas de administración fácilmente al personal sin comprometer la seguridad de su datos de <token>wit_nextref</token>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="b0468652e3764511281f7402e4c4ae07" id="tgt6" class="tgtSentence">Cómo asignar una designación a un usuario</caps:sentence>
        </title>
        <content>
          <para></para>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt7" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Administradores de servicios</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="8f27fdacab7fa08765f0cf41c4d24daf" id="tgt8" class="tgtSentence">En la lista de administradores de servicios, seleccione el usuario cuya designación desee cambiar y, después, haga clic en <ui>Administrar acceso</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt9" class="tgtSentence">En el cuadro de diálogo <ui>Administrar acceso</ui>, seleccione el nivel de acceso que desea asignar al usuario seleccionado.</caps:sentence>
                    <caps:sentence sentenceid="8d9fe41f11d85343f18538f8f8a42c9a" id="tgt10" class="tgtSentence"> Puede elegir entre:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e9968bf88f36922995c358886e10a1b8" id="tgt11" class="tgtSentence">Acceso completo</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="94767f578644e1b9f0d235549275e8a3" id="tgt12" class="tgtSentence">Acceso de solo lectura</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="14489fd25cb23642f31fb6d2e5626298" id="tgt13" class="tgtSentence">Además, puede elegir una de las siguientes designaciones que proporcionan niveles de acceso personalizados a la consola de administración de <token>wit_nextref</token>:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5527459add32dd78875ed85aefd0f748" id="tgt14" class="tgtSentence">Designación</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3ea6ee160450cf772aa4e64c31e0d7d0" id="tgt15" class="tgtSentence">El usuario puede:</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b5fb12b645fe43e9f53e78d0965cae86" id="tgt16" class="tgtSentence">Departamento de soporte técnico: nodo Grupos</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="72e53665e639894698a982ab106def16" id="tgt17" class="tgtSentence">Vea las listas de usuarios y dispositivos (el usuario no puede utilizar filtros para modificar la vista.</caps:sentence>
                                <caps:sentence sentenceid="a628ed3bb3865779527f8fe4c4928bc0" id="tgt18" class="tgtSentence"> Sin embargo, puede utilizar filtros de grupo para modificar lo que el usuario puede ver).</caps:sentence>
                                <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt19" class="tgtSentence"> Para obtener más información, vea <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="a239cd0dfdb0d95e4f92b3c709bda2fe" id="tgt20" class="tgtSentence">Imprima la lista de usuarios y dispositivos.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="c36f2b84652225f06cba36bb2457ff22" id="tgt21" class="tgtSentence">Exporte la lista de usuarios y dispositivos.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="a4076bb0588907f14a14769d9b42ce22" id="tgt22" class="tgtSentence">Vea las propiedades de un usuario o un dispositivo.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="73d4583fbca9cbc352c4e497793b8991" id="tgt23" class="tgtSentence">Realice las siguientes tareas remotas:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="4e1ba5579c71e7685d09aa43ca8b13a9" id="tgt24" class="tgtSentence">Ejecutar un examen completo de malware</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="79e2cbb66dc49b16d4a1f8194e3e9502" id="tgt25" class="tgtSentence">Ejecutar un examen rápido de malware</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="1ff89cfac8a0b1cd329301163f67b636" id="tgt26" class="tgtSentence">Reiniciar un equipo</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="9381b93948f45674a1721605f546995c" id="tgt27" class="tgtSentence">Actualizar definiciones de malware</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="1677f36f611fc1d5e28bdcf640b396de" id="tgt28" class="tgtSentence">Actualizar directivas</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="9f4e05be951a9ed4c3cbfbbd7dd935ea" id="tgt29" class="tgtSentence">Actualizar el inventario</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="5891d7e53e98a9fb5570f6ae43c11390" id="tgt30" class="tgtSentence">Bloquear de forma remota un dispositivo</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="d003b5fa135070b607f30bd2047fb2f9" id="tgt31" class="tgtSentence">Restablecimiento de la contraseña</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="89543113268409ddbb2f66bd59e86632" id="tgt32" class="tgtSentence">Cuando el usuario que ha configurado abra la consola de administración de <token>wit_nextref</token>, se le dará el nivel de acceso que ha especificado.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="110cbdbf-8f9b-4c1b-9e3e-184113cd711c">Technical reference for Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">
            <token>wit_nextref</token> provides the ability to filter the admin console view to allow users to access only the items you want them to see.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For example, you might want to allow only admin console operators to be able to update malware definitions, or reset the passcode on devices.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This is accomplished by using preset <ui>designations</ui> that you assign to specific users.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> When these users access the admin console, they only see items specific to their designation.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">Use this feature to help you assign administration tasks to staff while still ensuring the security of your <token>wit_nextref</token> data.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">How to assign a designation to a user</caps:sentence>
        </title>
        <content>
          <para></para>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Service Administrators</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">From the list of service administrators, choose the user whose designation you want to change, and then click <ui>Manage Access</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">In the <ui>Manage Access</ui> dialog box, choose the level of access that you want to give the selected user.</caps:sentence>
                    <caps:sentence id="src10" class="srcSentence"> You can choose from:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src11" class="srcSentence">Full access</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src12" class="srcSentence">Read only access</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Additionally, you can choose from one of the following designations that provide custom levels of access to the <token>wit_nextref</token> admin console:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src14" class="srcSentence">Designation</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src15" class="srcSentence">User can:</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src16" class="srcSentence">Helpdesk - Groups Node</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src17" class="srcSentence">See lists of users and devices (the user cannot use filters to modify the view.</caps:sentence>
                                <caps:sentence id="src18" class="srcSentence"> However, you can use group filtering to modify what the user can see).</caps:sentence>
                                <caps:sentence id="src19" class="srcSentence"> For more information, see <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src20" class="srcSentence">Print the list of users and devices.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src21" class="srcSentence">Export the list of users and devices</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src22" class="srcSentence">View the properties of a user or device.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src23" class="srcSentence">Perform the following remote tasks:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src24" class="srcSentence">Run a full malware scan</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src25" class="srcSentence">Run a quick malware scan</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src26" class="srcSentence">Restart a computer</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src27" class="srcSentence">Update malware definitions</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src28" class="srcSentence">Refresh policies</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src29" class="srcSentence">Refresh inventory</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src30" class="srcSentence">Remote lock a device</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src31" class="srcSentence">Passcode reset</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src32" class="srcSentence">When the user you configured next opens the <token>wit_nextref</token> admin console, they will be given the level of access you specified.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="110cbdbf-8f9b-4c1b-9e3e-184113cd711c">Technical reference for Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>