---
title: Administraci&#243;n de dispositivos m&#243;viles con Exchange ActiveSync e Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb9618d2-dc90-48be-b921-8044b7e693ac
---
# Administraci&#243;n de dispositivos m&#243;viles con Exchange ActiveSync e Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="62fd3f87581663e4371e40eb51d66e76" id="tgt1" class="tgtSentence">Para que <token>wit_nextref</token> administre dispositivos móviles directamente, los usuarios deben inscribir los dispositivos en <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence sentenceid="614c518172ac9be49927339bb3cacc0d" id="tgt2" class="tgtSentence"> Para los dispositivos móviles que los usuarios no inscriban se puede habilitar la administración de Exchange ActiveSync mediante Exchange Connector.</caps:sentence>
          <caps:sentence sentenceid="65ead2bcc60b39635c5b775a774909d9" id="tgt3" class="tgtSentence"> Los dispositivos de Exchange se pueden administrar tanto en servidores locales como, en el caso de Exchange hospedado en Microsoft Office 365, en la nube.</caps:sentence>
          <caps:sentence sentenceid="964fe0246f1af7cf97c7ab1d1b2b6dc6" id="tgt4" class="tgtSentence"> Exchange Connector le conecta con su implementación de Exchange y le permite administrar los dispositivos móviles a través de la consola de <token>wit_nextref</token>, en la que dispone de las siguientes capacidades:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="9f1227500444a0159dff42db13634c4a" id="tgt5" class="tgtSentence">Implementar directivas en grupos de usuarios para ayudar a proteger los datos corporativos que se almacenan en los dispositivos móviles (como contraseñas, cifrado y datos adjuntos).</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8b7a04d9e2d3d6805f5dc0478d9256f4" id="tgt6" class="tgtSentence">Definir reglas de acceso de los dispositivos móviles por familia y modelo de dispositivo para establecer qué dispositivos móviles pueden tener acceso a Exchange Active Sync.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8f8b0e078299d04e605740613e653b69" id="tgt7" class="tgtSentence">Inscribir, cambiar el nombre y anular la inscripción de dispositivos.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="90c31d426bb4388c826c4aeccf752c7e" id="tgt8" class="tgtSentence">Eliminar datos de dispositivos móviles con la opción de eliminar datos del dispositivo móvil, por ejemplo, para dispositivos perdidos o robados.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="31777712e92f9ad09ace2af63077c305" id="tgt9" class="tgtSentence">Este tema contiene las siguientes secciones:</caps:sentence>
        </para>
        <list class="nobullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="db1e9622e82f31fa0d3d209ad0b8af58" id="tgt10" class="tgtSentence">
                <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_EX_OP">Configure Microsoft Intune on-premises connector for on-premises or hosted Exchange</link>: utilice esta sección para configurar su infraestructura local con Exchange local o Hosted Exchange.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_S_S">Configure Microsoft Intune service to service connector for hosted Exchange</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_val_ex">Validate your Exchange connection</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_EXCap">Wipe for Exchange-managed mobile devices</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_pol">Policy for Exchange-managed mobile devices</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_acc">Exchange Access rules for mobile devices</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section expanded="false" address="bkmk_EX_OP">
        <title>
          <caps:sentence sentenceid="e065955a29a369a367754a5212397e8b" id="tgt11" class="tgtSentence">Configurar Microsoft Intune On-Premises Connector para Exchange local o Hosted Exchange</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="66e221727333295885533d018cb4a311" id="tgt12" class="tgtSentence">Utilice esta sección para configurar su infraestructura local con Exchange local o Hosted Exchange.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="b4851e92b19af0c5c82447fc0937709d" id="tgt13" class="tgtSentence">Requisitos</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="becd62270d66f170c745d70055de7a16" id="tgt14" class="tgtSentence">Para prepararse para conectar <token>wit_nextref</token> a su servidor de Exchange Server, en primer lugar debe cumplir los siguientes requisitos.</caps:sentence>
                <caps:sentence sentenceid="ffd3b3841b2e751c1e26aef7cf5fa4c4" id="tgt15" class="tgtSentence"> Es posible que ya cumpliera estos requisitos al configurar <token>wit_nextref</token>.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ba12fb48e2d23bb2bd2819f64d02ec7e" id="tgt16" class="tgtSentence">Requisito</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt17" class="tgtSentence">Más información</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="811196e6b810797b3f6b7eb28e84af94" id="tgt18" class="tgtSentence">Establecer la entidad de administración de dispositivos móviles en <token>wit_nextref</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <link xlink:href="668d6460-9d34-47a7-8a85-bbe1ed89f8e1">Set mobile device management authority as Microsoft Intune</link>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f0a61d203dc2ff0e69931b520657b908" id="tgt19" class="tgtSentence">Comprobar que cumple los requisitos de hardware para On-Premises Connector</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <link xlink:href="074de65b-84a5-4a01-a824-18ffd838eab0#BKMK_ExchanceConnectorReqs">Requirements for the On-Premises Exchange Connector</link>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="237b36562f71ee607c680e6d53fa1582" id="tgt20" class="tgtSentence">Configurar una cuenta de usuario con permiso para ejecutar la lista designada de cmdlets de Windows PowerShell</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="08236923117e937a9486d871bb765a76" id="tgt21" class="tgtSentence">Cmdlets de PowerShell para On-Premises Exchange Connector (consultar más abajo)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="bkmk_PS_onprem" expanded="true">
            <title>
              <caps:sentence sentenceid="161801d97c2f1f06c323e9effa8f0d02" id="tgt22" class="tgtSentence">Cmdlets de PowerShell para On-Premises Exchange Connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="bd0a4159871cfb1c604ccff699d68f8a" id="tgt23" class="tgtSentence">Debe crear una cuenta de usuario de Active Directory que sea utilizada por <token>wit_nextref</token> Exchange Connector.</caps:sentence>
                <caps:sentence sentenceid="512763f8f586eda020b9a27fde64e5e7" id="tgt24" class="tgtSentence"> La cuenta debe tener permiso para ejecutar los siguientes cmdlets de Windows PowerShell Exchange necesarios:</caps:sentence>
              </para>
              <procedure>
                <title></title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="d903f49185cfe545fc327302d85b7596" id="tgt25" class="tgtSentence">Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="b685c8c5d6bea4e497a10072b32c773b" id="tgt26" class="tgtSentence">Get-CasMailbox, Set-CasMailbox</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="e90c996159cceab0bd9ab2a12336fe0c" id="tgt27" class="tgtSentence">Get-ActiveSyncMailboxPolicy, Set-ActiveSyncMailboxPolicy, New-ActiveSyncMailboxPolicy, Remove-ActiveSyncMailboxPolicy</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="f8873d7fea4349a37a8d7cc3230aea9e" id="tgt28" class="tgtSentence">Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-ActiveSyncDeviceAccessRule</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="aee5b8a248224719f4c9a9f4ac21a28e" id="tgt29" class="tgtSentence">Get-ActiveSyncDeviceStatistics</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="60e70f53f9f84538efbe219d2e494535" id="tgt30" class="tgtSentence">Get-ActiveSyncDevice</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="567ad329a9dd62ecfee35eac378934e1" id="tgt31" class="tgtSentence">Get-ExchangeServer</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="899659c68289356d382ceb47844729b1" id="tgt32" class="tgtSentence">Get-ActiveSyncDeviceClass</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="fc4d5a5fe667a30145bcda8c943c0c7a" id="tgt33" class="tgtSentence">Get-Recipient</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9449dd693c890f90fd37432f42cf47f5" id="tgt34" class="tgtSentence">Clear-ActiveSyncDevice, Remove-ActiveSyncDevice</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="c5e16a90c5bdd44a226502f7b733e5e0" id="tgt35" class="tgtSentence">Set-ADServerSettings</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="c1580b7dc5002eb7279e114fafa861b8" id="tgt36" class="tgtSentence">Get-Command</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="69126629ae1da3e69f6d98c2447aedaf" id="tgt37" class="tgtSentence">Descargar, instalar y configurar Microsoft Intune Exchange Connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="f90fe76bd133fe951a955579f2f4def1" id="tgt38" class="tgtSentence">Para configurar una conexión que permita que <token>wit_nextref</token> se comunique con el servidor Exchange que hospeda los buzones de los dispositivos móviles, se debe descargar y configurar la herramienta On-Premises Connector desde la consola de administrador de <token>wit_nextref</token>.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="5ff471f7eff3bde06687bc6bb068d005" id="tgt39" class="tgtSentence">Para descargar el paquete de instalación de software de On-Premises Connector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt40" class="tgtSentence">Abra la <token>wit_adminconsole</token>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3fac61e32b1a462cded1a306cd511d35" id="tgt41" class="tgtSentence">En el panel de accesos directos del área de trabajo, haga clic en <ui>Administración</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="af21363a820758cfe92c046e865491b3" id="tgt42" class="tgtSentence">En el panel de navegación, en <ui>Administración de dispositivos móviles</ui>, expanda <ui>Microsoft Exchange</ui> y, a continuación, haga clic en <ui>Configurar conexión de Exchange</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt43" class="tgtSentence">En la página <ui>Configurar conexión de Exchange</ui>, haga clic en <ui>Descargar On-Premises Connector</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="aea319f4c74f55becd009defee00bf02" id="tgt44" class="tgtSentence">El software de On-Premises Connector se encuentra en una carpeta comprimida (.zip) que se puede abrir o guardar.</caps:sentence>
                        <caps:sentence sentenceid="4f4f145aafdf6ea8a38164ebe7706661" id="tgt45" class="tgtSentence"> En el cuadro de diálogo <ui>Descarga de archivos</ui>, haga clic en <ui>Guardar</ui> para almacenar la carpeta comprimida en una ubicación segura.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <alert class="important">
                      <para>
                        <caps:sentence sentenceid="9a9e18c79f9b9248f69a081c86d5a5b2" id="tgt46" class="tgtSentence">No cambie de nombre ni mueva los archivos extraídos; de lo contrario la instalación del software de On-Premises Connector resultará errónea.</caps:sentence>
                      </para>
                    </alert>
                  </content>
                </conclusion>
              </procedure>
              <para>
                <caps:sentence sentenceid="942e918b0f177bc0bcd0d4de2dceed5d" id="tgt47" class="tgtSentence">Siga estos pasos para instalar <token>wit_nextref</token> On-Premises Connector.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="a30b5b2cb6e7513c1e9b942140bbeb99" id="tgt48" class="tgtSentence">On-Premises Connector solo puede instalarse una vez por cada suscripción de <token>wit_nextref</token> y solo en un equipo.</caps:sentence>
                  <caps:sentence sentenceid="e52fcbb04fba85cc32348ccdfff37aac" id="tgt49" class="tgtSentence"> Si intenta instalar el conector local una segunda vez, se reemplazará la conexión inicial de Exchange.</caps:sentence>
                </para>
              </alert>
              <procedure>
                <title>
                  <caps:sentence sentenceid="e07d1d7d9e6f55706875d7529b66e39f" id="tgt50" class="tgtSentence">Para instalar On-Premises Connector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="8ad82c0e51408a6cf294130db0af7c47" id="tgt51" class="tgtSentence">Extraiga los archivos de <ui>Exchange_Connector_Setup.zip</ui> a una ubicación segura.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="116dd7acf4a9fdf7685dbbfbc4ccb561" id="tgt52" class="tgtSentence">Una vez extraídos los archivos, haga doble clic en <ui>Exchange_Connector_Setup.exe</ui> para instalar On-Premises Connector.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence sentenceid="71b83c2086663e9924e53044234a95f6" id="tgt53" class="tgtSentence">Si la carpeta de destino no es una ubicación segura, debe eliminar el archivo de certificado <ui>WindowsIntune.accountcert</ui> después de instalar On-Premises Connector.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <alert class="note">
                      <para>
                        <caps:sentence sentenceid="4b279455e58f5d62716c42bdec870742" id="tgt54" class="tgtSentence">Solo puede configurar una conexión de Exchange por cada cuenta de <token>wit_nextref</token>.</caps:sentence>
                        <caps:sentence sentenceid="71d8aedd1d150d2b2446d1ec27eb9cae" id="tgt55" class="tgtSentence"> Si intenta configurar una conexión adicional, se reemplazará la conexión original con la nueva.</caps:sentence>
                      </para>
                    </alert>
                  </content>
                </conclusion>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence sentenceid="54fdc6599ecb3dd7b87d97eefe36ed0c" id="tgt56" class="tgtSentence">Configurar On-Premises Exchange Connector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt57" class="tgtSentence">En el campo <ui>Servidor Exchange</ui>, seleccione su tipo de entorno de servidor Exchange, <ui>Exchange Server local</ui> o seleccione <ui>Hosted Exchange Server</ui> para Exchange en Microsoft Office 365.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="4d73641da185b18af0ae1d2f31e8f31c" id="tgt58" class="tgtSentence">Para un servidor Exchange local, proporcione el nombre del servidor o el nombre de dominio completo del servidor Exchange que hospeda el rol de servidor de acceso de cliente.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="7eb2949d9618769af5b277810cf8643d" id="tgt59" class="tgtSentence">Para un servidor de Exchange hospedado en Microsoft Office 365, proporcione la dirección del servidor Exchange.</caps:sentence>
                        <caps:sentence sentenceid="d7aae3964f3b4f699d069d8c71642987" id="tgt60" class="tgtSentence">  Para buscar la dirección URL del servidor Exchange hospedado:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="53a644f737c267196f8d47f2d012a256" id="tgt61" class="tgtSentence">Abra Outlook Web App para Office 365.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="01fba21e77a95aa0ad1bd53971ba723e" id="tgt62" class="tgtSentence">Haga clic en el icono “?”</caps:sentence>
                            <caps:sentence sentenceid="cfc51dc7da7803aacb00aa65ffdc4343" id="tgt63" class="tgtSentence"> en la parte superior izquierda y seleccione <ui>Acerca de</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="83a24f3faeb427b427d683b00bc3dc17" id="tgt64" class="tgtSentence">Busque el valor <ui>Servidor externo POP</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="a4a28832075aacafe81fa4c07455a370" id="tgt65" class="tgtSentence">En el caso de un servidor Exchange dedicado y hospedado, proporcione el nombre del servidor o el nombre de dominio completo del servidor Exchange que hospeda el rol de servidor Acceso de clientes.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt66" class="tgtSentence">Haga clic en <ui>Servidor proxy</ui> para especificar la configuración del servidor proxy para el servidor Exchange hospedado.</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt67" class="tgtSentence">Seleccione <ui>Usar un servidor proxy al sincronizar información de dispositivos móviles</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="eb2d3f6b2893bd777f6281d9aadf569f" id="tgt68" class="tgtSentence">Escriba el <ui>nombre del servidor proxy</ui> y el <ui>número de puerto</ui> que se utilizará para tener acceso al servidor.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="a632e05e00ea199278146cba5f0a2aae" id="tgt69" class="tgtSentence">Si es necesario proporcionar las credenciales de usuario para acceder al servidor proxy, seleccione Usar credenciales para conectarse al servidor prox<ui></ui>y, escriba el <ui>dominio\usuario</ui> y la <ui>contraseña</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt70" class="tgtSentence">Haga clic en <ui>Aceptar</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="1a069a318d757d58f6bc7cb6f87b51ed" id="tgt71" class="tgtSentence">Proporcione las credenciales necesarias para conectarse al servidor Exchange.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="6e342e9e502763a9c8c1fdb86718a430" id="tgt72" class="tgtSentence">Proporcione las credenciales administrativas necesarias para enviar notificaciones al buzón de Exchange de un usuario.</caps:sentence>
                        <caps:sentence sentenceid="760fbdcdfadbb07857c3e965bce93564" id="tgt73" class="tgtSentence"> Estas notificaciones se pueden configurar a través de directivas de acceso condicional mediante Intune.</caps:sentence>
                        <caps:sentence sentenceid="26a21e2510b9b5af5371b70794aa09a8" id="tgt74" class="tgtSentence"> Para obtener más información sobre estas directivas, consulte <link xlink:href="5b090c5a-6f12-4e60-ace0-c9929afaa9a3">Enable access to company resources with Microsoft Intune</link>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="3423eb1fbc2a58071262b7207683cb1b" id="tgt75" class="tgtSentence">Asegúrese de que el servicio de detección automática y servicios Web Exchange están configurados en el servidor de acceso de cliente de Exchange.</caps:sentence>
                        <caps:sentence sentenceid="bcca3c8c4c45cb2b8da2787fc61f72c6" id="tgt76" class="tgtSentence"> Para obtener más información al respecto, consulte <externalLink><linkText>Servidor de acceso de cliente</linkText><linkUri>https://technet.microsoft.com/library/dd298114.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt77" class="tgtSentence">En el campo <ui>Contraseña</ui>, indique la contraseña de la cuenta para permitir que <token>wit_nextref</token> acceda al servidor Exchange.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt78" class="tgtSentence">Haga clic en <ui>Conectar</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="9cc2facd794fd48ec7d7b6c88f241654" id="tgt79" class="tgtSentence">La configuración de la conexión puede tardar unos minutos.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="7db4971d7efb2f619229e9380d2c9f94" id="tgt80" class="tgtSentence">Durante la configuración, <token>wit_exch_2</token> guarda la configuración de proxy para permitir el acceso a Internet.</caps:sentence>
                        <caps:sentence sentenceid="5f4b85129a6de02745bd03fb6ab38024" id="tgt81" class="tgtSentence"> Si cambia la configuración de proxy, tendrá que volver a configurar <token>wit_exch_2</token> para aplicar la configuración de proxy actualizada a <token>wit_exch_2</token>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence sentenceid="d8c4f6665cce2b9f145a3c851886c18c" id="tgt82" class="tgtSentence">Después de que <token>wit_exch_2</token> configure la conexión, los dispositivos móviles asociados a los usuarios administrados en <token>wit_nextref</token> se sincronizan automáticamente y se agregan a la <token>wit_adminconsole</token>.</caps:sentence>
                      <caps:sentence sentenceid="d355a31661dcc56d5bf59946baa84e82" id="tgt83" class="tgtSentence"> Esta sincronización puede tardar algún tiempo en completarse.</caps:sentence>
                    </para>
                    <para>
                      <caps:sentence sentenceid="b411619e8bfa11699db4a557dc77a08c" id="tgt84" class="tgtSentence">Para ver el estado de la conexión y el último intento de sincronización correcto, en la <token>wit_adminconsole</token> haga clic en el área de trabajo <ui>Administración</ui> y en <ui>Administración de dispositivos móviles</ui>, haga clic en <ui>Exchange</ui>.</caps:sentence>
                    </para>
                    <alert class="note">
                      <para>
                        <caps:sentence sentenceid="8adb881de612beec2b1a8e06e2af7240" id="tgt85" class="tgtSentence">Si ha instalado On-Premises Connector y en algún punto elimina la conexión de Exchange, debe desinstalar On-Premises Connector del equipo en el que se instaló.</caps:sentence>
                      </para>
                    </alert>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section expanded="false" address="bkmk_S_S">
        <title>
          <caps:sentence sentenceid="1bffc7979685a587c3d33d47f170b70d" id="tgt86" class="tgtSentence">Configurar el servicio de Intune al conector de servicios para Hosted Exchange</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7096a899b6a70a92bfcae153bceed3ea" id="tgt87" class="tgtSentence">Utilice esta sección para conectar <token>wit_firstref</token> y Exchange hospedado sin una infraestructura local.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="b4851e92b19af0c5c82447fc0937709d" id="tgt88" class="tgtSentence">Requisitos</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="becd62270d66f170c745d70055de7a16" id="tgt89" class="tgtSentence">Para prepararse para conectar <token>wit_nextref</token> a su servidor de Exchange Server, asegúrese de haber completado lo siguiente:</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ba12fb48e2d23bb2bd2819f64d02ec7e" id="tgt90" class="tgtSentence">Requisito</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt91" class="tgtSentence">Más información</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="811196e6b810797b3f6b7eb28e84af94" id="tgt92" class="tgtSentence">Establecer la entidad de administración de dispositivos móviles en <token>wit_nextref</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage mobile devices with Microsoft Intune</link>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f0a61d203dc2ff0e69931b520657b908" id="tgt93" class="tgtSentence">Comprobar que cumple los requisitos de hardware para On-Premises Connector</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <link xlink:href="074de65b-84a5-4a01-a824-18ffd838eab0#BKMK_ServiceConnectorReqs">Requirements for the Service to Service Connector</link>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="237b36562f71ee607c680e6d53fa1582" id="tgt94" class="tgtSentence">Configurar una cuenta de usuario con permiso para ejecutar la lista designada de cmdlets de Windows PowerShell</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a7278233622321398d0680577b6203ff" id="tgt95" class="tgtSentence">Cmdlets de PowerShell para Service to Service Connector (consultar más abajo)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="Bkmk_PS_STS">
            <title>
              <caps:sentence sentenceid="35a9196b3ac1e2927081acb83f1e6cb2" id="tgt96" class="tgtSentence">Cmdlets de PowerShell para Service to Service Connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a0d52ca925456214dfd41011715af250" id="tgt97" class="tgtSentence">Debe crear una cuenta de usuario de Exchange Online que sea utilizada por <token>wit_nextref</token> Exchange Connector.</caps:sentence>
                <caps:sentence sentenceid="5069315496033028f3eb1537cd2e3164" id="tgt98" class="tgtSentence"> La cuenta debe tener permiso para ejecutar los cmdlets de Exchange de Windows PowerShell necesarios que se enumeran a continuación.</caps:sentence>
              </para>
              <procedure>
                <title></title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="d903f49185cfe545fc327302d85b7596" id="tgt99" class="tgtSentence">Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="f0453cde2f0e3fb489034a6d4615ab1d" id="tgt100" class="tgtSentence">Get-MobileDeviceMailboxPolicy, Set-MobileDeviceMailboxPolicy, New-MobileDeviceMailboxPolicy, Remove-MobileDeviceMailboxPolicy</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="f8873d7fea4349a37a8d7cc3230aea9e" id="tgt101" class="tgtSentence">Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-ActiveSyncDeviceAccessRule</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="b1a2ba35e2ebaeaf5ba34651b556e57e" id="tgt102" class="tgtSentence">Get-MobileDeviceStatistics</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ed82ace404b78bc6360196f383e930f4" id="tgt103" class="tgtSentence">Get-MobileDevice</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="899659c68289356d382ceb47844729b1" id="tgt104" class="tgtSentence">Get-ActiveSyncDeviceClass</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="fc4d5a5fe667a30145bcda8c943c0c7a" id="tgt105" class="tgtSentence">Get-Recipient</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="c866e0e3dd9ef0fddbaa5ebeecad9836" id="tgt106" class="tgtSentence">Clear-MobileDevice, Remove-MobileDevice</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="eb6ab89a5780977f39273c23739b1577" id="tgt107" class="tgtSentence">Configurar Service to Service Connector</caps:sentence>
            </title>
            <content>
              <procedure>
                <title></title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt108" class="tgtSentence">Abra la <token>wit_adminconsole</token>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3fac61e32b1a462cded1a306cd511d35" id="tgt109" class="tgtSentence">En el panel de accesos directos del área de trabajo, haga clic en <ui>Administración</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="af21363a820758cfe92c046e865491b3" id="tgt110" class="tgtSentence">En el panel de navegación, en <ui>Administración de dispositivos móviles</ui>, expanda <ui>Microsoft Exchange</ui> y, a continuación, haga clic en <ui>Configurar conexión de Exchange</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt111" class="tgtSentence">En la página <ui>Configurar conexión de Exchange</ui>, haga clic en <ui>Configurar Service to Service Connector</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence sentenceid="47b70163dca92b92e11f2796d9fb6117" id="tgt112" class="tgtSentence">Service to Service Connector se configurará automáticamente y se sincronizará con su entorno de Hosted Exchange.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section expanded="false" address="bkmk_val_ex">
        <title>
          <caps:sentence sentenceid="efc0d57d3563ed1ea99f7466883f1f4f" id="tgt113" class="tgtSentence">Validar la conexión de Exchange</caps:sentence>
        </title>
        <content>
          <para></para>
          <procedure>
            <title></title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1c348a84e6587ebf24d7e4578f5a8953" id="tgt114" class="tgtSentence">Después de configurar correctamente <token>wit_exch_2</token>, en la <token>wit_adminconsole</token> haga clic en el área de trabajo <ui>Administración</ui>, y en <ui>Administración de dispositivos móviles</ui>, haga clic en <ui>Microsoft Exchange</ui> y compruebe que los detalles que ha facilitado aparecen en <ui>Información de conexión de Exchange</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="f41ff147e78c2f1f07222cd197526f2b" id="tgt115" class="tgtSentence">También puede comprobar la fecha y la hora del último intento de sincronización correcto.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="bkmk_EXCap">
        <title address="bkmk_wipe">
          <caps:sentence sentenceid="78085b6498c9fdd27e3bc6e800364bfc" id="tgt116" class="tgtSentence">Eliminación de datos de dispositivos móviles administrados por Exchange</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="45a572d6571f514bcd25d89cc68d66e7" id="tgt117" class="tgtSentence">En la tabla siguiente se describen las capacidades de retirada y eliminación de datos mediante Exchange ActiveSync.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c676021e23998e74df5a004897e2537b" id="tgt118" class="tgtSentence">Tipo de eliminación de datos</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4dcbbb702b4aa870ffd94e0a2b8dc759" id="tgt119" class="tgtSentence">Windows 8.1 y Windows RT 8.1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="60c8058ac5e0a595887900b76f729aa1" id="tgt120" class="tgtSentence">Windows RT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e8d2fb426803ec5ca779721a20e31ea4" id="tgt121" class="tgtSentence">Windows Phone 8</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt122" class="tgtSentence">iOS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c31b32364ce19ca8fcd150a417ecce58" id="tgt123" class="tgtSentence">Android</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="253a1a2a076b6868b42edd4ce4c26f86" id="tgt124" class="tgtSentence">Eliminación completa</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7e2a9dbc5b5bf34c92de742e38d9ebae" id="tgt125" class="tgtSentence">Permite quitar cuentas de correo y correo almacenado en caché.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7e2a9dbc5b5bf34c92de742e38d9ebae" id="tgt126" class="tgtSentence">Permite quitar cuentas de correo y correo almacenado en caché.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c5e0e9566fd48f1674f107c0fc77b762" id="tgt127" class="tgtSentence">Restablecimiento de la configuración de fábrica</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c5e0e9566fd48f1674f107c0fc77b762" id="tgt128" class="tgtSentence">Restablecimiento de la configuración de fábrica</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c5e0e9566fd48f1674f107c0fc77b762" id="tgt129" class="tgtSentence">Restablecimiento de la configuración de fábrica</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="eaa09a005cae77527063a1785e04a985" id="tgt130" class="tgtSentence">Eliminación selectiva/correo electrónico</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="671433da588254fb257baa4784df95d7" id="tgt131" class="tgtSentence">Permite quitar cuentas de correo electrónico </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6fbf912174e839b8c622b5e3cd0d4b0" id="tgt132" class="tgtSentence">Permite quitar cuentas de correo electrónico</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aa9af52486028100a63f660bae781021" id="tgt133" class="tgtSentence">No compatible.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aa9af52486028100a63f660bae781021" id="tgt134" class="tgtSentence">No compatible.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="aa9af52486028100a63f660bae781021" id="tgt135" class="tgtSentence">No compatible.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1e500a0268f307732df0740d1e73d0c9" id="tgt136" class="tgtSentence">Eliminación selectiva/directivas</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ae13144336f56d4c42279c6b7c298219" id="tgt137" class="tgtSentence">Se quita el cumplimiento de directivas, pero no se cambia la configuración</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ae13144336f56d4c42279c6b7c298219" id="tgt138" class="tgtSentence">Se quita el cumplimiento de directivas, pero no se cambia la configuración</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ae13144336f56d4c42279c6b7c298219" id="tgt139" class="tgtSentence">Se quita el cumplimiento de directivas, pero no se cambia la configuración</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fa9ac3bc3ca8b19c3132a486c4bfda11" id="tgt140" class="tgtSentence">Se quitó el cumplimiento de directivas, pero no cambia la configuración</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ae13144336f56d4c42279c6b7c298219" id="tgt141" class="tgtSentence">Se quita el cumplimiento de directivas, pero no se cambia la configuración</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="bkmk_pol">
        <title>
          <caps:sentence sentenceid="d78e6cd552d4fb5f977eaaa937c60995" id="tgt142" class="tgtSentence">Directiva para dispositivos móviles administrados por Exchange</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="24ded44b33f63b9d3175fb25a1fac6b4" id="tgt143" class="tgtSentence">La configuración de directivas se puede aplicar mediante la consola de <token>wit_nextref</token>; consulte <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Configure policy for mobile devices in Microsoft Intune</link>.</caps:sentence>
            <caps:sentence sentenceid="7ea42627156eac10dca6a52a8d91c716" id="tgt144" class="tgtSentence"> Para obtener una lista detallada de las configuraciones de directivas y las características de Exchange ActiveSync admitidas por dispositivos móviles específicos, vea <externalLink><linkText>Exchange ActiveSync Client Comparison Table (Tabla de comparación de clientes de Exchange ActiveSync)</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=247270</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="87a69be26a8aef5ca48f24142c4c0480" id="tgt145" class="tgtSentence">Al conectar <token>wit_nextref</token> a un entorno de Microsoft Exchange, la directiva de EAS de todos los usuarios administrados con <token>wit_nextref</token> se restablecerá a la directiva predeterminada actual en el servidor de Microsoft Exchange, a menos que haya una directiva más específica definida en <token>wit_nextref</token>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section address="bkmk_acc">
        <title>
          <caps:sentence sentenceid="d0a680c584e3520de19efd90a8988e7b" id="tgt146" class="tgtSentence">Reglas de acceso a Exchange para dispositivos móviles</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="ff195db05d00f854be8f291ffbdecc67" id="tgt147" class="tgtSentence">Las reglas de acceso a Exchange para dispositivos móviles determinan el nivel de acceso a Exchange que se otorga a estos dispositivos.</caps:sentence>
            <caps:sentence sentenceid="bb267f60fab9e31bffc959d327a6e2ad" id="tgt148" class="tgtSentence"> Esta configuración afectará a todos los dispositivos móviles, incluidos los dispositivos móviles no inscritos en <token>wit_nextref</token>.</caps:sentence>
            <caps:sentence sentenceid="ad70b2379e64e6362a40847e70e13883" id="tgt149" class="tgtSentence"> Puede empezar por definir una <ui>Regla predeterminada</ui> que se aplicará a cualquier dispositivo móvil al que no se le aplique una regla personalizada.</caps:sentence>
            <caps:sentence sentenceid="386abb4bdfff5391cb0c24e03e08556c" id="tgt150" class="tgtSentence"> La tabla siguiente contiene los niveles de acceso administrados por Exchange ActiveSync:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0bcba23bbce54e01823ca5e854698716" id="tgt151" class="tgtSentence">Nivel de acceso</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt152" class="tgtSentence">Descripción</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="b343f48765e36aa21c278de94ff25bb6" id="tgt153" class="tgtSentence">Permitir a todos los dispositivos móviles el acceso a Exchange, a menos que una regla personalizada indique lo contrario</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c8f44b1846a2dc036de60a9db4387897" id="tgt154" class="tgtSentence">En el estado de acceso Permitir, un dispositivo móvil puede sincronizarse a través de Exchange ActiveSync y conectarse con el servidor Exchange para recuperar el correo electrónico y manipular información del calendario, contactos, tareas y notas.</caps:sentence>
                    <caps:sentence sentenceid="67a86f289684440ed29247a5c5fdaa33" id="tgt155" class="tgtSentence"> Esto permanecerá así siempre que el dispositivo móvil cumpla con la <ui>Directiva de seguridad de dispositivos móviles</ui> de <token>wit_nextref</token> que se haya configurado, a menos que el administrador de Exchange bloquee al usuario o el dispositivo móvil.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="f1cf8b2589cacd271eda1478e3b6d697" id="tgt156" class="tgtSentence">Bloquear a todos los dispositivos móviles el acceso a Exchange, a menos que una regla personalizada indique lo contrario</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1feef9baf4b6f57c228e1f545faba0c0" id="tgt157" class="tgtSentence">Si establece una configuración de acceso de dispositivo para bloquear un dispositivo móvil, este no podrá conectarse al servidor Exchange y recibirá errores de tipo HTTP 403 (prohibido).</caps:sentence>
                    <caps:sentence sentenceid="0a1dcb69b13ccbc763b8e09c5ab3a9d4" id="tgt158" class="tgtSentence"> El usuario recibirá un mensaje de correo electrónico desde el servidor Exchange indicando que se bloqueó el acceso al buzón desde el dispositivo móvil.</caps:sentence>
                    <caps:sentence sentenceid="73789cc6d141f57ae18f10c052900fe4" id="tgt159" class="tgtSentence"> El usuario no podrá leer el mensaje de correo electrónico en el dispositivo móvil bloqueado.</caps:sentence>
                    <caps:sentence sentenceid="83aa526a3e1ee7546cf521bc922a5801" id="tgt160" class="tgtSentence"> Puede agregar texto personalizado a este mensaje con instrucciones para los usuarios cuyos dispositivos estén bloqueados a través de la tarea <ui>Establecer notificación de usuario</ui>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="8a5e953d5a0d1e471262d3cce8529163" id="tgt161" class="tgtSentence">Poner en cuarentena todos los dispositivos móviles para poder tomar más tarde una decisión sobre cada dispositivo móvil, a menos que una regla personalizada indique lo contrario</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="88f51a0e729f2cd9722d41787725acfd" id="tgt162" class="tgtSentence">Cuando se pone en cuarentena un dispositivo móvil, este puede conectarse al servidor Exchange.</caps:sentence>
                    <caps:sentence sentenceid="8244230a1632316773925f1b43cfe136" id="tgt163" class="tgtSentence"> Sin embargo, se le concede únicamente acceso limitado a los datos.</caps:sentence>
                    <caps:sentence sentenceid="1a849f89c21327cbbcd399b4cf193596" id="tgt164" class="tgtSentence"> El usuario puede agregar contenido a sus propias carpetas de calendario, contactos, tareas y notas, pero el servidor no permitirá al dispositivo que recupere contenido del buzón del usuario.</caps:sentence>
                    <caps:sentence sentenceid="d2f3a35f7edea308a6b3cb49c39379fd" id="tgt165" class="tgtSentence"> El usuario recibirá un solo mensaje de correo electrónico donde se le notifica que el dispositivo móvil se pone en cuarentena.</caps:sentence>
                    <caps:sentence sentenceid="7a211b777413b7b33899548235cebe72" id="tgt166" class="tgtSentence"> El dispositivo recibirá este mensaje, que también estará disponible en el buzón del usuario.</caps:sentence>
                    <caps:sentence sentenceid="338224abe06fa97f80af8850ce3680fb" id="tgt167" class="tgtSentence"> Puede agregar texto personalizado a este mensaje con instrucciones para los usuarios cuyos dispositivos estén en cuarentena a través de la tarea <ui>Establecer notificación de usuario</ui>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="28b2b52130f698deec95a5d7518dd909" id="tgt168" class="tgtSentence">Una estrategia de acceso es una combinación de una <ui>Regla predeterminada</ui> y de <ui>Reglas personalizadas</ui> que se aplican a todos los dispositivos móviles conectados a Exchange.</caps:sentence>
            <caps:sentence sentenceid="a048c66fd2bcfecadbba7c43bdae6008" id="tgt169" class="tgtSentence"> La tabla siguiente contiene algunos ejemplos de estrategias de acceso.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f92301b5cdd7844d335e82b16b998be2" id="tgt170" class="tgtSentence">Estrategia de acceso</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt171" class="tgtSentence">Descripción</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4993e4f72f01ff1c9e81f4ea5c6d145e" id="tgt172" class="tgtSentence">Lista de admisión</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="974fe33e524e58c996dc2c4760fa6485" id="tgt173" class="tgtSentence">Puede utilizar una lista de admisión para conceder acceso a una lista de dispositivos conocidos y restringir el acceso al resto.</caps:sentence>
                    <caps:sentence sentenceid="ef6f4a0bd869c55120f7a2bef56eb8da" id="tgt174" class="tgtSentence"> Para ello, debe crear reglas personalizadas para permitir a los dispositivos específicos que desee que tengan acceso a los buzones de los usuarios.</caps:sentence>
                    <caps:sentence sentenceid="9d7b00d7d68871b382efa518a401179a" id="tgt175" class="tgtSentence"> Tan pronto como cree dicha regla, debe establecer la regla de acceso predeterminada para bloquear o poner en cuarentena el resto de dispositivos.</caps:sentence>
                    <caps:sentence sentenceid="9da3170d5c0ee739f8f5b47a31210ad6" id="tgt176" class="tgtSentence"> Para agregar un nuevo dispositivo a la lista de admisión, cree una nueva regla personalizada</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0d2690b2ab019be74cbd2d5331bebf36" id="tgt177" class="tgtSentence">Lista de bloqueo</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c9a86bd6463c6009fe2022ac0d1202e4" id="tgt178" class="tgtSentence">Puede usar una lista de bloqueo para conceder acceso de forma predeterminada a todos los dispositivos y bloquear un conjunto de dispositivos que no desea que accedan a su organización.</caps:sentence>
                    <caps:sentence sentenceid="e74b64c70d43c1b413b8d8d52d5a7f93" id="tgt179" class="tgtSentence"> Para crear una lista de bloqueo, debe crear reglas personalizadas para bloquear los dispositivos que no desea sincronizar con los buzones de la organización.</caps:sentence>
                    <caps:sentence sentenceid="188d5d58e6e22e670a526ca0b47cb212" id="tgt180" class="tgtSentence"> La regla predeterminada debe establecerse para permitir el acceso a todos los dispositivos que no estén explícitamente bloqueados por las reglas existentes.</caps:sentence>
                    <caps:sentence sentenceid="7274104b7b7fc4e1fb12f0d38239a6dd" id="tgt181" class="tgtSentence"> Para agregar un nuevo dispositivo o un conjunto de dispositivos a la lista de bloqueo, cree una nueva regla personalizada.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9f07066a213722b1c147ec79a33a957d" id="tgt182" class="tgtSentence">Admisión y bloqueo mixto</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="350622d4454e4cdb29f2604dbb362b84" id="tgt183" class="tgtSentence">Además de crear listas de admisión y bloqueo, puede poner en cuarentena nuevos dispositivos móviles a medida que se introducen en la organización en el momento de la evaluación.</caps:sentence>
                    <caps:sentence sentenceid="3e9b9ee51dae3a90c25c9bb02ba97941" id="tgt184" class="tgtSentence"> Por ejemplo, si tiene una lista de bloqueo de dispositivos móviles no permitidos en su organización y una lista de admisión de dispositivos móviles permitidos en su organización, puede establecer la regla predeterminada en cuarentena.</caps:sentence>
                    <caps:sentence sentenceid="5b9b90b1346227cc18d75067af35341c" id="tgt185" class="tgtSentence"> El resto de dispositivos se pondrá en cuarentena, lo que le permitirá examinar los nuevos dispositivos a medida que se introducen en la organización y decidir si los agrega a la lista de admisión o a la lista de bloqueo.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para></para>
          <para>
            <caps:sentence sentenceid="ca5e36edd960e6e5084c5b77207fc9af" id="tgt186" class="tgtSentence">El siguiente procedimiento describe cómo crear una regla personalizada.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="45a58c0ae5129d132cc196ab50add90e" id="tgt187" class="tgtSentence">Crear una regla de acceso predeterminada</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt188" class="tgtSentence">Abra la <token>wit_adminconsole</token>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="752aa017ea4de5217e5d5fd8b7024304" id="tgt189" class="tgtSentence">En el panel de accesos directos del área de trabajo, haga clic en el icono <ui>Directiva</ui> y en <ui>Acceso a Exchange para dispositivos móviles</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt190" class="tgtSentence">En la lista <ui>Regla predeterminada</ui>, seleccione la regla de acceso que desea aplicar a todos los dispositivos móviles no cubiertos por una regla o exención personal.</caps:sentence>
                    <caps:sentence sentenceid="9c246454e1fc1fdab04143e527678570" id="tgt191" class="tgtSentence"> Haga clic en <ui>Guardar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence sentenceid="ca5e36edd960e6e5084c5b77207fc9af" id="tgt192" class="tgtSentence">El siguiente procedimiento describe cómo crear una regla personalizada.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="6542ce156b499191de464278e0c93e92" id="tgt193" class="tgtSentence">Crear una regla de acceso personalizada</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt194" class="tgtSentence">Abra la <token>wit_adminconsole</token>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="752aa017ea4de5217e5d5fd8b7024304" id="tgt195" class="tgtSentence">En el panel de accesos directos del área de trabajo, haga clic en el icono <ui>Directiva</ui> y en <ui>Acceso a Exchange para dispositivos móviles</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt196" class="tgtSentence">En la lista <ui>Reglas personalizadas</ui>, haga clic en <ui>Agregar regla</ui> y cree una regla personalizada.</caps:sentence>
                    <caps:sentence sentenceid="9c246454e1fc1fdab04143e527678570" id="tgt197" class="tgtSentence"> Haga clic en <ui>Guardar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">For <token>wit_nextref</token> to directly manage mobile devices, users need to enroll devices into <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For mobile devices that users have not enrolled you can enable Exchange ActiveSync management using the Exchange connector.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Exchange devices can be managed in both on premises servers and for hosted Exchange on Microsoft Office 365 in the cloud.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The Exchange connector connects you with your Exchange deployment and lets you manage mobile devices through the <token>wit_nextref</token> console, where you have the following capabilities:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Deploy policies to user groups to help secure corporate data that is stored on mobile devices such as password, encryption, and attachments.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Define mobile device access rules by device family and device model to set which mobile devices can access Exchange ActiveSync.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Enroll, rename, and un-enroll devices.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Wipe mobile devices with the option to wipe the mobile device, such as for lost or stolen devices.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src9" class="srcSentence">This topic contains the following sections:</caps:sentence>
        </para>
        <list class="nobullet">
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">
                <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_EX_OP">Configure Microsoft Intune on-premises connector for on-premises or hosted Exchange</link>: Use this section to configure your on-premises infrastructure with on-premises Exchange or hosted Exchange.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_S_S">Configure Microsoft Intune service to service connector for hosted Exchange</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_val_ex">Validate your Exchange connection</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_EXCap">Wipe for Exchange-managed mobile devices</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_pol">Policy for Exchange-managed mobile devices</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_acc">Exchange Access rules for mobile devices</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section expanded="false" address="bkmk_EX_OP">
        <title>
          <caps:sentence id="src11" class="srcSentence">Configure Microsoft Intune on-premises connector for on-premises or hosted Exchange</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src12" class="srcSentence">Use this section to configure your on-premises infrastructure with on-premises Exchange or hosted Exchange.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src13" class="srcSentence">Requirements</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src14" class="srcSentence">To prepare to connect <token>wit_nextref</token> to your Exchange Server, you must first fulfill the following requirements.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> You may have already fulfilled these requirements when you set up <token>wit_nextref</token>.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src16" class="srcSentence">Requirement</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src17" class="srcSentence">More information</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src18" class="srcSentence">Set the Mobile Device Management Authority to <token>wit_nextref</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <link xlink:href="668d6460-9d34-47a7-8a85-bbe1ed89f8e1">Set mobile device management authority as Microsoft Intune</link>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src19" class="srcSentence">Verify you have hardware requirements for the on-premises connector</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <link xlink:href="074de65b-84a5-4a01-a824-18ffd838eab0#BKMK_ExchanceConnectorReqs">Requirements for the On-Premises Exchange Connector</link>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">Configure a user account with permission to run the designated list of Windows PowerShell cmdlets</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src21" class="srcSentence">Powershell Cmdlets for On-Premises Exchange Connector (see below)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="bkmk_PS_onprem" expanded="true">
            <title>
              <caps:sentence id="src22" class="srcSentence">Powershell Cmdlets for On-Premises Exchange Connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src23" class="srcSentence">You must create an Active Directory user account that is used by the <token>wit_nextref</token> Exchange Connector.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> The account must have permission to run the following required Windows PowerShell Exchange cmdlets:</caps:sentence>
              </para>
              <procedure>
                <title></title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src25" class="srcSentence">Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src26" class="srcSentence">Get-CasMailbox, Set-CasMailbox</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src27" class="srcSentence">Get-ActiveSyncMailboxPolicy, Set-ActiveSyncMailboxPolicy, New-ActiveSyncMailboxPolicy, Remove-ActiveSyncMailboxPolicy</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src28" class="srcSentence">Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-ActiveSyncDeviceAccessRule</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src29" class="srcSentence">Get-ActiveSyncDeviceStatistics</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src30" class="srcSentence">Get-ActiveSyncDevice</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src31" class="srcSentence">Get-ExchangeServer</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src32" class="srcSentence">Get-ActiveSyncDeviceClass</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src33" class="srcSentence">Get-Recipient</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">Clear-ActiveSyncDevice, Remove-ActiveSyncDevice</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">Set-ADServerSettings</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">Get-Command</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src37" class="srcSentence">Download, Install and Configure the Microsoft Intune Exchange Connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src38" class="srcSentence">To set up a connection that enables <token>wit_nextref</token> to communicate with the Exchange Server that hosts the mobile devices’ mailboxes, you must download and configure the On-Premises Connector tool from the <token>wit_nextref</token> administrator console.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src39" class="srcSentence">To download the On-Premises Connector software installation package</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">Open the <token>wit_adminconsole</token>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src41" class="srcSentence">In the workspace shortcuts pane, click <ui>Administration</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">In the navigation pane, under <ui>Mobile Device Management</ui>, expand <ui>Microsoft Exchange</ui> and then click <ui>Setup Exchange Connection</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">On the <ui>Setup Exchange Connection</ui> page, click <ui>Download On-Premises Connector</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">The On-Premises Connector software is contained in a compressed (.zip) folder that can be opened or saved.</caps:sentence>
                        <caps:sentence id="src45" class="srcSentence"> In the <ui>File Download</ui> dialog box, click <ui>Save</ui> to store the compressed folder to a secure location.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <alert class="important">
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Do not rename or move the extracted files or the On-Premises Connector software installation will not succeed.</caps:sentence>
                      </para>
                    </alert>
                  </content>
                </conclusion>
              </procedure>
              <para>
                <caps:sentence id="src47" class="srcSentence">Perform the following steps to install the <token>wit_nextref</token> On-Premises Connector.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src48" class="srcSentence">The On-Premises Connector can only be installed once per <token>wit_nextref</token> subscription, and only on one computer.</caps:sentence>
                  <caps:sentence id="src49" class="srcSentence"> If you attempt to install the On-Premises Connector a second time, you will replace the initial Exchange connection.</caps:sentence>
                </para>
              </alert>
              <procedure>
                <title>
                  <caps:sentence id="src50" class="srcSentence">To install the On-Premises Connector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">Extract the files in <ui>Exchange_Connector_Setup.zip</ui> into a secure location.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">After the files are extracted, double-click <ui>Exchange_Connector_Setup.exe</ui> to install the On-Premises Connector.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence id="src53" class="srcSentence">If the destination folder is not a secure location, you should delete the certificate file <ui>WindowsIntune.accountcert</ui> after you install the On-Premises Connector.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <alert class="note">
                      <para>
                        <caps:sentence id="src54" class="srcSentence">You can only set up one Exchange connection per <token>wit_nextref</token> account.</caps:sentence>
                        <caps:sentence id="src55" class="srcSentence"> If you try to configure an additional connection, it will replace the original connection with the new one.</caps:sentence>
                      </para>
                    </alert>
                  </content>
                </conclusion>
              </procedure>
              <procedure>
                <title>
                  <caps:sentence id="src56" class="srcSentence">Configure the On-Premises Exchange Connector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src57" class="srcSentence">In the <ui>Exchange server</ui> field, select your Exchange server environment type, either <ui>On-premises Exchange Server</ui> or select <ui>Hosted Exchange Server</ui> for Exchange on Microsoft Office 365.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">For an on-premises Exchange server, provide either the server name or fully qualified domain name of the Exchange server that hosts the Client Access server role.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src59" class="srcSentence">For a hosted Exchange server in Microsoft Office 365, provide the Exchange server address.</caps:sentence>
                        <caps:sentence id="src60" class="srcSentence">  To find the hosted Exchange server URL:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src61" class="srcSentence">Open the Outlook Web App for Office 365.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src62" class="srcSentence">Click the “?”</caps:sentence>
                            <caps:sentence id="src63" class="srcSentence"> icon at the top left, and select <ui>About</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src64" class="srcSentence">Locate the <ui>POP External Server</ui> value.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src65" class="srcSentence">For a dedicated, hosted Exchange server, provide either the server name or the fully qualified domain name of the dedicated Exchange server that hosts the Client Access server role.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">Click <ui>Proxy Server</ui> to specify proxy server settings for your hosted Exchange server.</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src67" class="srcSentence">Select <ui>Use a proxy server when synchronizing mobile device information</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src68" class="srcSentence">Enter the <ui>proxy server name</ui> and the <ui>port number</ui> to be used to access the server.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src69" class="srcSentence">If it is necessary to provide user credentials to access the proxy server, select Use credentials to connect to the proxy serve<ui></ui>r and enter the <ui>domain\user</ui> and the <ui>password</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src70" class="srcSentence">Click <ui>OK</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">Provide the credentials necessary to connect to your Exchange server.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src72" class="srcSentence">Provide administrative credentials necessary to send notifications to a user’s Exchange mailbox.</caps:sentence>
                        <caps:sentence id="src73" class="srcSentence"> These notifications are configurable via Conditional Access policies using Intune.</caps:sentence>
                        <caps:sentence id="src74" class="srcSentence"> For more information on these policies see <link xlink:href="5b090c5a-6f12-4e60-ace0-c9929afaa9a3">Enable access to company resources with Microsoft Intune</link>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src75" class="srcSentence">Ensure that the Autodiscover service and Exchange Web Services are configured on the Exchange Client Access Server.</caps:sentence>
                        <caps:sentence id="src76" class="srcSentence"> For more information on that see <externalLink><linkText>Client Access server</linkText><linkUri>https://technet.microsoft.com/library/dd298114.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src77" class="srcSentence">In the <ui>Password</ui> field, provide the password for this account to enable <token>wit_nextref</token> to access the Exchange Server.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src78" class="srcSentence">Click <ui>Connect</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src79" class="srcSentence">It may take a few minutes while the connection is set up.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">During configuration, the <token>wit_exch_2</token> stores your proxy settings to enable access to the Internet.</caps:sentence>
                        <caps:sentence id="src81" class="srcSentence"> If your proxy settings change, you will have to reconfigure the <token>wit_exch_2</token> in order to apply the updated proxy settings to the <token>wit_exch_2</token>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence id="src82" class="srcSentence">After the <token>wit_exch_2</token> sets up the connection, mobile devices associated with users that are managed in <token>wit_nextref</token> are automatically synchronized and added to the <token>wit_adminconsole</token>.</caps:sentence>
                      <caps:sentence id="src83" class="srcSentence"> This synchronization may take some time to complete.</caps:sentence>
                    </para>
                    <para>
                      <caps:sentence id="src84" class="srcSentence">To view the status of the connection and the last successful synchronization attempt, in the <token>wit_adminconsole</token> click the <ui>Administration</ui> workspace, and under <ui>Mobile Device Management</ui>, click <ui>Exchange</ui>.</caps:sentence>
                    </para>
                    <alert class="note">
                      <para>
                        <caps:sentence id="src85" class="srcSentence">If you have installed the On-Premises Connector, and if at some point you delete the Exchange connection, you must uninstall the On-Premises Connector from the computer onto which it was installed.</caps:sentence>
                      </para>
                    </alert>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section expanded="false" address="bkmk_S_S">
        <title>
          <caps:sentence id="src86" class="srcSentence">Configure Intune service to service connector for hosted Exchange</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src87" class="srcSentence">Use this section to connect <token>wit_firstref</token> and hosted Exchange without an on-premises infrastructure.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src88" class="srcSentence">Requirements</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src89" class="srcSentence">To prepare to connect <token>wit_nextref</token> to your Exchange Server, make sure you have completed the following:</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">Requirement</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src91" class="srcSentence">More information</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">Set the Mobile Device Management Authority to <token>wit_nextref</token></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage mobile devices with Microsoft Intune</link>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src93" class="srcSentence">Verify you have hardware requirements for the on-premises connector</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <link xlink:href="074de65b-84a5-4a01-a824-18ffd838eab0#BKMK_ServiceConnectorReqs">Requirements for the Service to Service Connector</link>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src94" class="srcSentence">Configure a user account with permission to run the designated list of Windows PowerShell cmdlets</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">PowerShell Cmdlets for Service to Service Connector (See below)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="Bkmk_PS_STS">
            <title>
              <caps:sentence id="src96" class="srcSentence">PowerShell Cmdlets for Service to Service Connector</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src97" class="srcSentence">You must create an Exchange Online user account that is used by the <token>wit_nextref</token> Exchange Connector.</caps:sentence>
                <caps:sentence id="src98" class="srcSentence"> The account must have permission to run the required Windows PowerShell Exchange cmdlets that are listed below.</caps:sentence>
              </para>
              <procedure>
                <title></title>
                <steps class="bullet">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src99" class="srcSentence">Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src100" class="srcSentence">Get-MobileDeviceMailboxPolicy, Set-MobileDeviceMailboxPolicy, New-MobileDeviceMailboxPolicy, Remove-MobileDeviceMailboxPolicy</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-ActiveSyncDeviceAccessRule</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">Get-MobileDeviceStatistics</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src103" class="srcSentence">Get-MobileDevice</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src104" class="srcSentence">Get-ActiveSyncDeviceClass</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src105" class="srcSentence">Get-Recipient</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">Clear-MobileDevice, Remove-MobileDevice</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src107" class="srcSentence">Set up the Service to Service Connector</caps:sentence>
            </title>
            <content>
              <procedure>
                <title></title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src108" class="srcSentence">Open the <token>wit_adminconsole</token>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src109" class="srcSentence">In the workspace shortcuts pane, click <ui>Administration</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src110" class="srcSentence">In the navigation pane, under <ui>Mobile Device Management</ui>, expand <ui>Microsoft Exchange</ui> and then click <ui>Set Up Exchange Connection</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src111" class="srcSentence">On the <ui>Set Up Exchange Connection</ui> page, click <ui>Set Up Service to Service Connector</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para>
                <caps:sentence id="src112" class="srcSentence">The Service to Service Connector will automatically configure and synchronize with your Hosted Exchange environment.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section expanded="false" address="bkmk_val_ex">
        <title>
          <caps:sentence id="src113" class="srcSentence">Validate your Exchange connection</caps:sentence>
        </title>
        <content>
          <para></para>
          <procedure>
            <title></title>
            <steps class="bullet">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">After you have successfully configured the <token>wit_exch_2</token>, in the <token>wit_adminconsole</token> click the <ui>Administration</ui> workspace, and under <ui>Mobile Device Management</ui>, click <ui>Microsoft Exchange</ui> and validate that the details you provided appear under <ui>Exchange Connection Information</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">You can also check the time and date of the last successful synchronization attempt.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="bkmk_EXCap">
        <title address="bkmk_wipe">
          <caps:sentence id="src116" class="srcSentence">Wipe for Exchange-managed Mobile Devices</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src117" class="srcSentence">The following table describes the retire/wipe capabilities through Exchange ActiveSync.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src118" class="srcSentence">Type of Wipe</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src119" class="srcSentence">Windows 8.1 and Windows RT 8.1</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">Windows RT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src121" class="srcSentence">Windows Phone 8</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src122" class="srcSentence">iOS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src123" class="srcSentence">Android</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src124" class="srcSentence">Full Wipe</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src125" class="srcSentence">Removes mail account and cached mail.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src126" class="srcSentence">Removes mail account and cached mail.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src127" class="srcSentence">Factory Reset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src128" class="srcSentence">Factory Reset</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src129" class="srcSentence">Factory Reset</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src130" class="srcSentence">Selective Wipe/Email</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src131" class="srcSentence">Removes email account </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src132" class="srcSentence">Removes email account</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src133" class="srcSentence">Not supported.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src134" class="srcSentence">Not supported.</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src135" class="srcSentence">Not supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">Selective Wipe/policies</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src137" class="srcSentence">Policy enforcement removed, but settings are not changed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src138" class="srcSentence">Policy enforcement removed, but settings are not changed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src139" class="srcSentence">Policy enforcement removed, but settings are not changed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src140" class="srcSentence">Policy enforcement removed, but  settings are not changed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">Policy enforcement removed, but settings are not changed</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="bkmk_pol">
        <title>
          <caps:sentence id="src142" class="srcSentence">Policy for Exchange-managed mobile devices</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src143" class="srcSentence">Policy settings can be applied through the <token>wit_nextref</token> console, see <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Configure policy for mobile devices in Microsoft Intune</link>.</caps:sentence>
            <caps:sentence id="src144" class="srcSentence"> For a detailed list of Exchange ActiveSync policy settings and features that are supported by specific mobile devices, see <externalLink><linkText>Exchange ActiveSync Client Comparison Table</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=247270</linkUri></externalLink>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src145" class="srcSentence">Upon connecting <token>wit_nextref</token> to a Microsoft Exchange environment, all users managed through <token>wit_nextref</token> will have their EAS policy reset to the current default policy on the Microsoft Exchange server, unless there is a more specific policy defined within <token>wit_nextref</token>.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section address="bkmk_acc">
        <title>
          <caps:sentence id="src146" class="srcSentence">Exchange Access rules for mobile devices</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src147" class="srcSentence">Exchange access rules for mobile devices determine the level of access to Exchange that is granted to mobile devices.</caps:sentence>
            <caps:sentence id="src148" class="srcSentence"> These setting will affect all mobile devices, even the mobile devices not enrolled in <token>wit_nextref</token>.</caps:sentence>
            <caps:sentence id="src149" class="srcSentence"> You can start off by defining a <ui>Default Rule</ui> which will apply to any mobile device that does not have a custom rule applied to it.</caps:sentence>
            <caps:sentence id="src150" class="srcSentence"> The following table contains the access levels managed by Exchange ActiveSync:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">Access level</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src152" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src153" class="srcSentence">Allow all mobile devices to access Exchange, unless a custom rule states otherwise</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src154" class="srcSentence">In the allow access state, a mobile device can synchronize through Exchange ActiveSync and connect to the Exchange server to retrieve email and manipulate calendar information, contacts, tasks, and notes.</caps:sentence>
                    <caps:sentence id="src155" class="srcSentence"> This will continue as long as the device complies with the <token>wit_nextref</token> <ui>Mobile Device Security Policy</ui> that you have configured, unless the user or the specific mobile device has been blocked by the Exchange administrator.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src156" class="srcSentence">Block all mobile devices from accessing Exchange, unless a custom rule states otherwise</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">A mobile device that is blocked because of a device access setting you configured will not be allowed to connect to the Exchange server and will receive HTTP 403 Forbidden errors.</caps:sentence>
                    <caps:sentence id="src158" class="srcSentence"> The user will receive an email message from the Exchange server telling them that the mobile device was blocked from accessing their mailbox.</caps:sentence>
                    <caps:sentence id="src159" class="srcSentence"> The user will not be able to read the email message on the blocked mobile device.</caps:sentence>
                    <caps:sentence id="src160" class="srcSentence"> You can add customized text to this message to provide instructions for users whose devices are blocked through the <ui>Set User Notification</ui> task.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src161" class="srcSentence">Quarantine all mobile devices so I can decide later for each individual mobile device, unless a custom rule states otherwise</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src162" class="srcSentence">When a mobile device is quarantined, the mobile device is allowed to connect to the Exchange server.</caps:sentence>
                    <caps:sentence id="src163" class="srcSentence"> However, it is given only limited access to data.</caps:sentence>
                    <caps:sentence id="src164" class="srcSentence"> The user can add content to their own Calendar, Contacts, Tasks, and Notes folders but the server will not allow the device to retrieve any content from the user's mailbox.</caps:sentence>
                    <caps:sentence id="src165" class="srcSentence"> The user will receive a single email message that tells them that the mobile device is quarantined.</caps:sentence>
                    <caps:sentence id="src166" class="srcSentence"> This message will be received by the device and will also be available in the user's mailbox.</caps:sentence>
                    <caps:sentence id="src167" class="srcSentence"> You can add customized text to this message to provide instructions for users whose devices are quarantined through the <ui>Set User Notification</ui> task.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src168" class="srcSentence">An access strategy is a combination of a <ui>Default Rule</ui> and <ui>Custom Rules</ui>  that apply to all mobile devices connected to exchange.</caps:sentence>
            <caps:sentence id="src169" class="srcSentence"> The table below lists some example access strategies.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src170" class="srcSentence">Access Strategy</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">Allow list</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src173" class="srcSentence">You can use an allow list to grant access to a list of known devices and restrict access for everything else.</caps:sentence>
                    <caps:sentence id="src174" class="srcSentence"> To do this, you must create custom rules so that the specific devices you want are allowed to access users' mailboxes.</caps:sentence>
                    <caps:sentence id="src175" class="srcSentence"> As soon as you create such a rule, you must set the default access rule to block or quarantine all other devices.</caps:sentence>
                    <caps:sentence id="src176" class="srcSentence"> To add a new device to the allow list, create a new custom rule</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">Block list</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">You can use a block list to grant access to all devices by default, but to block access for a set of devices that you do not want to access your organization.</caps:sentence>
                    <caps:sentence id="src179" class="srcSentence"> You create a block list by creating custom rules to block the devices that you do not want to synchronize with the organization’s mailboxes.</caps:sentence>
                    <caps:sentence id="src180" class="srcSentence"> The default rule should be set to allow access to all devices that are not explicitly blocked by the existing rules.</caps:sentence>
                    <caps:sentence id="src181" class="srcSentence"> To add a new device or set of devices to the block list, create a new custom rule.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">Mixed allow and block</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">In addition to creating allow and block lists, you can quarantine new mobile devices as they are introduced into the organization while you evaluate them.</caps:sentence>
                    <caps:sentence id="src184" class="srcSentence"> For example, if you have a block list for mobile devices that are not allowed within your organization, and an allow list for mobile devices that are allowed within the organization, you can set the default rule to quarantine.</caps:sentence>
                    <caps:sentence id="src185" class="srcSentence"> All other devices will automatically be quarantined, which lets you discover new devices as they are introduced to the organization and decide whether to add them to the allow list or the block list.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para></para>
          <para>
            <caps:sentence id="src186" class="srcSentence">The following procedure describes how to create a custom rule.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src187" class="srcSentence">Create a Default Access Rule</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src188" class="srcSentence">Open the <token>wit_adminconsole</token>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src189" class="srcSentence">In the workspace shortcuts pane, click the <ui>Policy</ui> icon and click <ui>Exchange Access for Mobile Devices</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src190" class="srcSentence">In the <ui>Default Rule</ui> list, select the Access Rule that you wish to apply to all mobile devices not covered by a rule or personal exemption.</caps:sentence>
                    <caps:sentence id="src191" class="srcSentence"> Click <ui>Save</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence id="src192" class="srcSentence">The following procedure describes how to create a custom rule.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src193" class="srcSentence">Create a Custom Access Rule</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src194" class="srcSentence">Open the <token>wit_adminconsole</token>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">In the workspace shortcuts pane, click the <ui>Policy</ui> icon and click <ui>Exchange Access for Mobile Devices</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src196" class="srcSentence">In the <ui>Custom Rules</ui> list, Click <ui>Add Rule</ui> and create a custom rule.</caps:sentence>
                    <caps:sentence id="src197" class="srcSentence"> Click <ui>Save</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>