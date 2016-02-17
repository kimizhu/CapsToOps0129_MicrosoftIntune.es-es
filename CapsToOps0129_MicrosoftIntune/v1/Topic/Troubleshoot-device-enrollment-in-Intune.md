---
title: Soluci&#243;n de problemas con la inscripci&#243;n de dispositivos en Intune
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6982ba0e-90ff-4fc4-9594-55797e504b62
---
# Soluci&#243;n de problemas con la inscripci&#243;n de dispositivos en Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para></para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="ac8befe0ede0051f6036953c01f1adbc" id="tgt1" class="tgtSentence">Problemas con la inscripción de dispositivos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9c4217a75559bbfaa9f431ccde0e8206" id="tgt2" class="tgtSentence">Aquí se indican algunos problemas con la inscripción de dispositivos y cómo puede solucionarlos.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="83fc1e61531b91ff9e4fd1b4d03df31a" id="tgt3" class="tgtSentence">Los usuarios de dispositivos administrados pueden recopilar registros de inscripción para que usted pueda revisarlos.</caps:sentence>
              <caps:sentence sentenceid="1d2a70d44ddf8e4f95b16509d8457c73" id="tgt4" class="tgtSentence"> Para recopilar estos registros, tiene instrucciones en <link xlink:href="7e5979ab-fc4c-4c7b-a60c-15317496dfa2">Fix issues with mobile device enrollment</link></caps:sentence>
            </para>
          </alert>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="447b29e3f584554903dbaca100537a7f" id="tgt5" class="tgtSentence">Se alcanzó el límite de dispositivos</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="d0126a6c35dfd1073beae37675172e5c" id="tgt6" class="tgtSentence">
                  <legacyBold>Problema: </legacyBold>recibió un error en el dispositivo de iOS durante la inscripción (como por ejemplo, <legacyBold>El Portal de empresa no está disponible temporalmente</legacyBold>) y el registro DMPdownloader.log que se encuentra en Configuration Manager contiene el error <legacyBold>DeviceCapReached</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="999e2d31c99e90a3eefdaaac2ca028f0" id="tgt7" class="tgtSentence">
                  <legacyBold>Solución: </legacyBold>de forma predeterminada, los usuarios no pueden inscribir más de 5 dispositivos.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="6867e4a4b7e2eb0d05b12ed6f83eab06" id="tgt8" class="tgtSentence">Compruebe el número de dispositivos inscritos y permitidos</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="4cd03abbd30e1c7f63ec823b009624b2" id="tgt9" class="tgtSentence">Asegúrese de que el usuario no tiene más de 5 dispositivos asignados en el Portal de administración de Intune</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="367d80e5497257e98f2aad9bf014ddec" id="tgt10" class="tgtSentence">Compruebe en el Portal de administración de Intune, en Administrador\Dispositivo móvil\Reglas de inscripción, que el límite de inscripción de dispositivos está establecido en 5</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence sentenceid="aedc12507da38d421ddeac754ccedea8" id="tgt11" class="tgtSentence">Los usuarios de dispositivos móviles pueden eliminar dispositivos en la siguiente URL: <externalLink><linkText>https://byodtestservice.azurewebsites.net/</linkText><linkUri>https://byodtestservice.azurewebsites.net/</linkUri></externalLink>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="847459c08d19f7b73720699b97512b3d" id="tgt12" class="tgtSentence">Los administradores pueden eliminar dispositivos en el portal de Azure Active Directory:
</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="b6c85aabfedad4bc53580bfb6b16b456" id="tgt13" class="tgtSentence">Eliminar dispositivos en el portal de Azure Active Directory</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3b82379ff743b3095086e895bdddee0e" id="tgt14" class="tgtSentence">Vaya a <externalLink><linkText>http://aka.ms/accessaad</linkText><linkUri>http://aka.ms/accessaad</linkUri></externalLink> o haga clic en <ui>Administrador</ui> &gt; <ui>Azure AD</ui> en <externalLink><linkText>https://portal.office.com</linkText><linkUri>https://portal.office.com</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="6a5391e18294dc5aa8d6da166cd6e9f0" id="tgt15" class="tgtSentence">Inicie sesión con su identificador de organización mediante el vínculo que encontrará en el lado izquierdo de la página.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="a7feb9dfdb4e54ba39fca97a59924279" id="tgt16" class="tgtSentence">Cree una suscripción de Azure si no tiene una.</caps:sentence>
                        <caps:sentence sentenceid="6e4cfb3579b45daa7e1b591b23e314fc" id="tgt17" class="tgtSentence"> Si tiene una cuenta de pago, no necesitará una tarjeta de crédito o realizar ningún pago (haga clic en el vínculo de suscripción <ui>Registre su suscripción gratuita de Azure Active Directory</ui>).</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt18" class="tgtSentence">Seleccione <ui>Active Directory</ui> y, a continuación, seleccione su empresa.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="7486589d03c162162a7c4e75345fcca4" id="tgt19" class="tgtSentence">Seleccione la pestaña <ui>Usuarios</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ac5cff3e7248bafccc5af7b26dc38bd9" id="tgt20" class="tgtSentence">Seleccione el usuario cuyos dispositivos desea eliminar.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt21" class="tgtSentence">Haga clic en <ui>Dispositivos</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="5fa1611dc95ba82e156796e7369d0965" id="tgt22" class="tgtSentence">Quite los dispositivos que crea oportunos, como por ejemplo aquellos que ya no estén en uso o que tienen definiciones inexactas.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="d1532d2177115b150f281467177d70f5" id="tgt23" class="tgtSentence">Puede evitar llegar al límite de inscripción de dispositivos mediante el uso de administradores de inscripción de dispositivos, tal como se describe en <link xlink:href="a23abc61-69ed-44f1-9b71-b86aefc6ba03">Enroll corporate-owned devices with the Device Enrollment Manager in Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="d5162bcd5e11cfa28b6793f2f507ce53" id="tgt24" class="tgtSentence">Si agrega una cuenta de usuario al grupo de administradores de inscripción de dispositivos, esta no podrá realizar la inscripción al aplicarse la directiva de acceso condicional cuando ese usuario en cuestión inicie sesión.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="8af989396e3ef907dd520619dfc54797" id="tgt25" class="tgtSentence">Error de instalación de perfil</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="deae28b9ec827b791bb266d213459ab1" id="tgt26" class="tgtSentence">
                  <legacyBold>Problema: </legacyBold>recibió un <ui>error en la instalación del perfil</ui> en un dispositivo de iOS o Android</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="8e8a6ab21e4b0e8db61c1174d24437ee" id="tgt27" class="tgtSentence">Pasos para solucionar problemas con la instalación del perfil</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9b39e9a61d82994acd05ca69493649e3" id="tgt28" class="tgtSentence">Confirme que el usuario tiene asignada una licencia adecuada para la versión del servicio Intune que usa.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="7c43927112aeceae9eba24f299c4b930" id="tgt29" class="tgtSentence">Confirme que el dispositivo no esté inscrito en otro proveedor MDM o que no tenga ya instalado un perfil de administración.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="1db212f02c0f78fd18eab87a40844647" id="tgt30" class="tgtSentence">Si el dispositivo es iOS, vaya a <externalLink><linkText>https://portal.manage.microsoft.com</linkText><linkUri>https://portal.manage.microsoft.com</linkUri></externalLink> e intente instalar el perfil cuando se le solicite.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="26772cf68ddd31c8a1aa0815bd3fe74c" id="tgt31" class="tgtSentence">Confirme que Safari y Chrome son los exploradores predeterminados de su dispositivo iOS o Android respectivamente, y que las cookies están habilitadas.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="0dc8aba71898b815ca1e06cd98fadf48" id="tgt32" class="tgtSentence">El Portal de empresa no está disponible temporalmente

</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="deae28b9ec827b791bb266d213459ab1" id="tgt33" class="tgtSentence">
                  <legacyBold>Problema: </legacyBold>recibió en su dispositivo el error <ui>El Portal de empresa no está disponible temporalmente</ui>.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="cc2e44faaf5a4d04b4852b1af6b4e205" id="tgt34" class="tgtSentence">Solucionar el error “El Portal de empresa no está disponible temporalmente”</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="198e2f2a16412d725382ef4344ec00ed" id="tgt35" class="tgtSentence">Quite la aplicación Portal de empresa de Intune del dispositivo.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="23c9782a21342319bc82846e33b47822" id="tgt36" class="tgtSentence">	En el dispositivo, abra el explorador, vaya a <externalLink><linkText>https://portal.manage.microsoft.com</linkText><linkUri>https://portal.manage.microsoft.com</linkUri></externalLink>, e intente un inicio de sesión de usuario.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="0e02b889edd97749e04a7d6660842d48" id="tgt37" class="tgtSentence">Si el usuario no puede iniciar sesión, intente usar otra red.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="c94153a5e53547301ec7994b65ed4bcd" id="tgt38" class="tgtSentence">Si ello produce un error, compruebe que las credenciales del usuario se han sincronizado correctamente con Azure Active Directory.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3a449d62f0b48118ab86b5bcb7eedac6" id="tgt39" class="tgtSentence">	Si el usuario inicia sesión correctamente, el dispositivo iOS le pedirá que instale la aplicación Portal de empresa de Intune y que se inscriba.</caps:sentence>
                        <caps:sentence sentenceid="4d38546de9ef58ce0f0b339835d6e613" id="tgt40" class="tgtSentence"> En un dispositivo Android, debe instalar manualmente la aplicación Portal de empresa de Intune y, a continuación, puede volver a intentar inscribirse.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="8cbda176e949fd57649b88433d1de2d4" id="tgt41" class="tgtSentence">Entidad de MDM no definida

</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="2d4735483245db22862afc6278083466" id="tgt42" class="tgtSentence">
                  <legacyBold>Problema: </legacyBold>recibió el error <ui>Entidad de MDM no definida</ui>.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="e8ea0fc1b12ec9ebb8ee3ce1ca7f39c1" id="tgt43" class="tgtSentence">Solucionar el error “Entidad de MDM no definida”</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="2afd753dde0f0de47cfb03561573fe4d" id="tgt44" class="tgtSentence">Compruebe que la entidad de MDM se ha establecido correctamente para la versión del servicio Intune que usa; esto es, para Intune, MDM de Office 365 y System Center Configuration Manager con Intune.</caps:sentence>
                        <caps:sentence sentenceid="dbbd05c1a8c9f3f04c246c67d767f49c" id="tgt45" class="tgtSentence"> Para <token>wit_nextref</token>, se establece la entidad de MDM en <ui>Administrador</ui> &gt; <ui>Administración de dispositivos móviles</ui>.</caps:sentence>
                        <caps:sentence sentenceid="dbbd05c1a8c9f3f04c246c67d767f49c" id="tgt46" class="tgtSentence"> Para <token>cmshort</token> con <token>wit_nextref</token>, deberá establecerla al configurar el conector <token>wit_nextref</token>; asimismo, en Office 365 deberá acceder a una configuración denominada <ui>Dispositivos móviles</ui>.</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="5721af4835203c0a204be163069c3575" id="tgt47" class="tgtSentence">Una vez establecida la entidad de MDM, solo podrá cambiarla si se pone en contacto con el soporte técnico, tal como se describe en <link xlink:href="4682b6b6-c9ef-483e-a6de-b8830cb98b63">How to get support for Microsoft Intune</link>.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="2e465ffc5b9814339903873abd65297a" id="tgt48" class="tgtSentence">	Compruebe que las credenciales del usuario se han sincronizado correctamente con Azure Active Directory; para ello, asegúrese de que sus UPN coinciden con la información de Active Directory en el Portal de cuentas.</caps:sentence>
                        <caps:sentence sentenceid="61ecb2df98ba7560aa280a84bd4054b6" id="tgt49" class="tgtSentence"> Si el UPN no coincide con la información de Active Directory:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="b7a7c61880b7dd7645b1a211c8898490" id="tgt50" class="tgtSentence">	Desactive DirSync del servidor local
</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="24649a415da1a68764b05a9c09bdb7dd" id="tgt51" class="tgtSentence">	Elimine el usuario que no coincida de la lista de usuarios <ui>Portal de cuentas de Intune</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="017430b248947ce2a63afe2aa719801f" id="tgt52" class="tgtSentence">	Espere aproximadamente una hora para permitir que el servicio de Azure pueda quitar los datos incorrectos.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="fa2b3940d86f0cd484f32598d07f53d0" id="tgt53" class="tgtSentence">	Vuelva a activar DirSync y compruebe si el usuario ya se ha sincronizado correctamente</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="25cd559e26c7e7cfa7cea03bef567da2" id="tgt54" class="tgtSentence">Si usa System Center Configuration Manager con Intune, compruebe que el usuario tiene un identificador válido de usuario en la nube:
 
</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="011413d202aa9e249632d4aaeaaec31c" id="tgt55" class="tgtSentence">Abra SQL Management Studio.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d12b0d29e457021f23498403f867bbb2" id="tgt56" class="tgtSentence">	Conéctese a la base de datos adecuada</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="7129c36c4c3ebfaa5da08f7dadf29185" id="tgt57" class="tgtSentence">	Abra la carpeta de bases de datos y busque la carpeta <ui>CM_DBName</ui>, donde DBName es el nombre de la base de datos de cliente.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="12daf0a2a35a00b57bf30602d0e8fea3" id="tgt58" class="tgtSentence">En la parte superior, haga clic en Nueva consulta y ejecute las siguientes consultas:
</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="d37adb79753cb0602cca5ce5435bfd46" id="tgt59" class="tgtSentence">Para ver todos los usuarios: <codeInline>select * from [CM_ DBName].[dbo].[User_DISC]</codeInline></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="992cfa35b0456112166d1cbe35a75348" id="tgt60" class="tgtSentence">Para ver usuarios específicos, use la siguiente consulta, donde %testuser1% representa el elemento username@domain.com referente al usuario que desea buscar: <codeInline>select * from [CM_ DBName].[dbo].[User_DISC] where User_Principal_Name0 like '%testuser1%'</codeInline></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <para>
                            <caps:sentence sentenceid="a056b72cfb1f16ade78f2d7d0dc4ad1f" id="tgt61" class="tgtSentence">Una vez escrita la consulta, haga clic en <ui>!Execute</ui>.</caps:sentence>
                            <caps:sentence sentenceid="0986c8ff9350fbca2e7404c0788cb05a" id="tgt62" class="tgtSentence"> Cuando obtenga los resultados, busque el identificador clouduser.</caps:sentence>
                            <caps:sentence sentenceid="4dcf2e0d950b61ba644c5da8cc007dc7" id="tgt63" class="tgtSentence">  Si no encuentra ningún identificador, esto quiere decir que el usuario no tiene licencia para usar Intune.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="6109f87785b11393169f92812822cc88" id="tgt64" class="tgtSentence">Los dispositivos móviles desaparecen cuando se usa System Center Configuration Manager con Intune</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="841b64a94536a11fe0ba019cd91e1bcf" id="tgt65" class="tgtSentence">
                  <legacyBold>Problema: </legacyBold>después de inscribir correctamente un dispositivo móvil a Configuration Manager, este desaparece de la colección de dispositivos móviles, pero el dispositivo aún tiene el perfil de administración y aparece en la puerta de enlace de CSS.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="ccc62b97a716f59345da7b661571b9b7" id="tgt66" class="tgtSentence">
                  <legacyBold>Solución: </legacyBold>esto puede ocurrir si tiene un proceso personalizado que quita dispositivos que no estén unidos al dominio o porque el usuario ha retirado la suscripción del dispositivo.</caps:sentence>
                <caps:sentence sentenceid="1ade3165f6a88f53e5ff570383eb9bc9" id="tgt67" class="tgtSentence"> Para validar y comprobar qué proceso o cuenta de usuario ha quitado el dispositivo de la consola de Configuration Manager, siga estos pasos:</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="6ad902faf848f7310c19c863309a81f5" id="tgt68" class="tgtSentence">Compruebe cómo se quitó el dispositivo</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9d1808288897073e5424b47639f73a86" id="tgt69" class="tgtSentence">	En la consola de administración de Configuration Manager, seleccione <ui>Supervisión</ui> &gt;<ui> Estado del sistema</ui> &gt; <ui>Consultas de mensaje de estado</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="5fa7333a602467b3b0f5d87bd3dc3e29" id="tgt70" class="tgtSentence">Haga clic con el botón derecho en <ui>Recursos de miembro de la recopilación eliminados manualmente</ui> y seleccione <ui>Mostrar mensajes</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="96e6752ecc5d030a4c24f7036cbdd6c0" id="tgt71" class="tgtSentence">Seleccione la fecha y hora apropiadas o las últimas 12 horas.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87bf4bfb91170489f0c7136a349da32e" id="tgt72" class="tgtSentence">Busque el dispositivo en cuestión y compruebe cómo se quitó el dispositivo.</caps:sentence>
                        <caps:sentence sentenceid="f906e5d7a0e97de8386d223360737f17" id="tgt73" class="tgtSentence"> En el ejemplo siguiente se muestra que la cuenta SCCMInstall eliminó el dispositivo a través de una aplicación desconocida.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="2886daf8-f636-4d2b-99f2-857a8243b236"></image>
                      </mediaLink>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="b659d4951c7d76d7cefd256e76e285b1" id="tgt74" class="tgtSentence">Compruebe que Configuration Manager no tenga ninguna tarea, script u otro proceso programado que pudiera estar purgando de forma automática dispositivos móviles que no pertenezcan al dominio u otros dispositivos relacionados.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para></para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">Device enrollment issues</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Listed here are some device enrollment issues and how to troubleshoot and resolve them.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src3" class="srcSentence">Your managed device users can collect enrollment logs for you to review.</caps:sentence>
              <caps:sentence id="src4" class="srcSentence"> Instructions for collecting the logs are provided in <link xlink:href="7e5979ab-fc4c-4c7b-a60c-15317496dfa2">Fix issues with mobile device enrollment</link></caps:sentence>
            </para>
          </alert>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src5" class="srcSentence">Device Cap reached</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src6" class="srcSentence">
                  <legacyBold>Issue: </legacyBold>You receive an error on your device during enrollment, such as a <legacyBold>Company Portal Temporarily Unavailable </legacyBold>error on an iOS device, and the DMPdownloader.log on Configuration Manager contains the error <legacyBold>DeviceCapReached</legacyBold>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src7" class="srcSentence">
                  <legacyBold>Resolution: </legacyBold>By design, users can enroll no more than 5 devices.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src8" class="srcSentence">Check number of devices enrolled and allowed</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src9" class="srcSentence">Validate in the Intune admin portal that the user has no more than 5 devices assigned</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src10" class="srcSentence">Check in the Intune admin portal under Admin\Mobile Device Management\Enrollment Rules that the Device enrollment limit is set to 5</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence id="src11" class="srcSentence">Mobile device users can delete devices at the following URL: <externalLink><linkText>https://byodtestservice.azurewebsites.net/</linkText><linkUri>https://byodtestservice.azurewebsites.net/</linkUri></externalLink>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src12" class="srcSentence">Administrators can delete devices in the Azure Active Directory portal:
</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src13" class="srcSentence">To delete devices in the Azure Active Directory portal</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">Browse to <externalLink><linkText>http://aka.ms/accessaad</linkText><linkUri>http://aka.ms/accessaad</linkUri></externalLink> or click <ui>Admin</ui> &gt; <ui>Azure AD</ui> from <externalLink><linkText>https://portal.office.com</linkText><linkUri>https://portal.office.com</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src15" class="srcSentence">Login with your Org ID using the link on the left side of the page.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src16" class="srcSentence">Create an Azure Subscription if you don’t have one.</caps:sentence>
                        <caps:sentence id="src17" class="srcSentence"> This should not require a credit card or payment if you have a paid account (click the <ui>Register your free Azure Active Directory</ui> subscription link).</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src18" class="srcSentence">Select <ui>Active Directory</ui> and then select your organization.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src19" class="srcSentence">Select the <ui>Users</ui> tab.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">Select the user whose devices you want to delete.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src21" class="srcSentence">Click <ui>Devices</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">Remove devices as appropriate, such as those that are no longer in use, or those that have inaccurate definitions.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <alert class="note">
                <para>
                  <caps:sentence id="src23" class="srcSentence">You can avoid the device enrollment cap by using Device Enrollment Managers, as described in <link xlink:href="a23abc61-69ed-44f1-9b71-b86aefc6ba03">Enroll corporate-owned devices with the Device Enrollment Manager in Microsoft Intune</link>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src24" class="srcSentence">A user account which is added to Device Enrollment Managers group will not be able to complete enrollment when Conditional Access policy is enforced for that specific user login.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src25" class="srcSentence">Profile installation failed</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src26" class="srcSentence">
                  <legacyBold>Issue: </legacyBold>You receive a <ui>Profile installation failed</ui> error on an iOS or Android device</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src27" class="srcSentence">Troubleshooting steps for failed profile installation</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src28" class="srcSentence">Confirm that the user has been assigned an appropriate license for the version of the Intune service you are using.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src29" class="srcSentence">Confirm that the device is not already enrolled with another MDM provider or that it does not already have a management profile installed.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src30" class="srcSentence">For an iOS device, navigate to <externalLink><linkText>https://portal.manage.microsoft.com</linkText><linkUri>https://portal.manage.microsoft.com</linkUri></externalLink> and try to install the profile when prompted.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src31" class="srcSentence">Confirm that Safari for iOS and Chrome for Android are the default browsers and that cookies are enabled.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src32" class="srcSentence">Company Portal Temporarily Unavailable

</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src33" class="srcSentence">
                  <legacyBold>Issue: </legacyBold>You receive a <ui>Company Portal Temporarily Unavailable</ui> error on the device.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src34" class="srcSentence">Troubleshooting Company Portal Temporarily Unavailable error</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">Remove the Intune Company Portal app from the device.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">	On the device, open the browser, browse to <externalLink><linkText>https://portal.manage.microsoft.com</linkText><linkUri>https://portal.manage.microsoft.com</linkUri></externalLink>, and attempt a user login.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">If the user fails to log in, have them try another network.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">If that fails, validate that the user’s credentials have synced correctly with Azure Active Directory.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src39" class="srcSentence">	If the user successfully logs in, an iOS device will prompt you to install the Intune Company Portal app and enroll.</caps:sentence>
                        <caps:sentence id="src40" class="srcSentence"> On an Android device you will need to manually install the Intune Company Portal app, after which you can retry enrolling.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src41" class="srcSentence">MDM authority not defined

</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src42" class="srcSentence">
                  <legacyBold>Issue: </legacyBold>You receive an <ui>MDM authority not defined</ui> error.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src43" class="srcSentence">Troubleshooting MDM authority not defined error</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">Verify that the MDM Authority has been set appropriately for the version of the Intune service you are using  , that is, for Intune, O365 MDM, or System Center Configuration Manager with Intune.</caps:sentence>
                        <caps:sentence id="src45" class="srcSentence"> For <token>wit_nextref</token>,  the MDM Authority is set in <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui>.</caps:sentence>
                        <caps:sentence id="src46" class="srcSentence"> For <token>cmshort</token> with <token>wit_nextref</token>, you set it when configuring the <token>wit_nextref</token> connector,  and in O365 it's a setting <ui>Mobile Devices</ui>.</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src47" class="srcSentence">One you set the MDM authority, you can only change it by contacting Support, as described in <link xlink:href="4682b6b6-c9ef-483e-a6de-b8830cb98b63">How to get support for Microsoft Intune</link>.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src48" class="srcSentence">	Verify that the user’s credentials have synced correctly with Azure Active Directory, by checking that their UPN matches the Active Directory information in the Account Portal.</caps:sentence>
                        <caps:sentence id="src49" class="srcSentence"> If the UPN does not match the Active Directory information:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src50" class="srcSentence">	Turn off DirSync on the local server
</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src51" class="srcSentence">	Delete the mismatched user from the <ui>Intune Account Portal</ui> user list.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src52" class="srcSentence">	Wait about one hour to allow the Azure service to remove the incorrect data.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src53" class="srcSentence">	Turn on DirSync again and check if the user is now synced properly</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">In a scenario where you are using System Center Configuration Manager with Intune, verify that the user has a valid Cloud User ID:
 
</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src55" class="srcSentence">Open SQL Management Studio.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src56" class="srcSentence">	Connect to the appropriate DB</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src57" class="srcSentence">	Open the databases folder and find and open the <ui>CM_DBName</ui> folder, where DBName is the name of the customer database.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src58" class="srcSentence">At the top, click New Query  and execute the following queries:
</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src59" class="srcSentence">To see all users: <codeInline>select * from [CM_ DBName].[dbo].[User_DISC]</codeInline></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src60" class="srcSentence">To see Specific Users, use the following query, where %testuser1% represents username@domain.com for the user you want to look up: <codeInline>select * from [CM_ DBName].[dbo].[User_DISC] where User_Principal_Name0 like '%testuser1%'</codeInline></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <para>
                            <caps:sentence id="src61" class="srcSentence">After writing the query click <ui>!Execute</ui>.</caps:sentence>
                            <caps:sentence id="src62" class="srcSentence"> Once the results have been returned, look for the clouduser ID.</caps:sentence>
                            <caps:sentence id="src63" class="srcSentence">  If no ID is found, the user isn't licensed to use Intune.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src64" class="srcSentence">Mobile devices disappear when using System Center Configuration Manager with Intune</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src65" class="srcSentence">
                  <legacyBold>Issue: </legacyBold>After successfully enrolling a mobile device to Configuration Manager it disappears from the mobile device collection, but the device still has the Management Profile and is listed in CSS Gateway.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src66" class="srcSentence">
                  <legacyBold>Resolution: </legacyBold>This may occur because you have a custom process removing non-domain-joined devices, or because the  user has retired the device from the subscription.</caps:sentence>
                <caps:sentence id="src67" class="srcSentence"> To validate and check which process or user account removed the device from the Configuration Manager console, perform the following steps:</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src68" class="srcSentence">Check how device was removed</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">	In the Configuration Manager admin console select <ui>Monitoring</ui> &gt;<ui> System Status</ui> &gt; <ui>Status Message Queries</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src70" class="srcSentence">Right-click <ui>Collection Member Resources Manually Deleted</ui> and select <ui>Show Messages</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">Pick an appropriate time/date or the last 12 hours.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src72" class="srcSentence">Find the device in question and review how the device was removed.</caps:sentence>
                        <caps:sentence id="src73" class="srcSentence"> The Example below shows the account SCCMInstall deleted the device via an Unknown Application.</caps:sentence>
                      </para>
                      <mediaLink>
                        <image xlink:href="2886daf8-f636-4d2b-99f2-857a8243b236"></image>
                      </mediaLink>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">Check that Configuration Manager does not have a scheduled task, script, or other process which could be automatically purging non-domain, mobile, or related devices.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>