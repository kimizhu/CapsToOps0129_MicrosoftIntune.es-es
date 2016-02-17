---
title: Configurar la entidad de administraci&#243;n de dispositivos m&#243;viles como Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 668d6460-9d34-47a7-8a85-bbe1ed89f8e1
---
# Configurar la entidad de administraci&#243;n de dispositivos m&#243;viles como Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence sentenceid="dd74f59aee9f782f7490a01b3785e003" id="tgt1" class="tgtSentence">Antes de que los usuarios puedan inscribir dispositivos móviles con <token>wit_nextref</token>, el administrador de TI debe declarar a <token>wit_nextref</token> como <newTerm>entidad de administración de dispositivos móviles</newTerm>.</caps:sentence>
          <caps:sentence sentenceid="a726b3bbf6639a325810a9f76659ac12" id="tgt2" class="tgtSentence"> Una <newTerm>autoridad de administración de dispositivos móviles</newTerm> define el único servicio de administración que tiene permiso para administrar un conjunto de dispositivos.</caps:sentence>
          <caps:sentence sentenceid="3064c987726b179b37f439dc1303fe9e" id="tgt3" class="tgtSentence">  Las soluciones para la entidad de administración de dispositivos móviles incluyen <token>wit_nextref</token>, Administrador de configuración con <token>wit_nextref</token> o las soluciones MDM de Office 365.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4e9ab10c1c20b0db2ab970c19cb19afc" id="tgt4" class="tgtSentence">En esta guía se da por hecho que Intune se utiliza sin la integración de System Center Configuration Manager por lo que la configuración debe establecerse en Microsoft Intune.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4798060b304b4372ef20791fc8028737" id="tgt5" class="tgtSentence">Entidad de MDM</caps:sentence>
        </title>
        <content>
          <para>
            <embeddedLabel>
              <caps:sentence sentenceid="2368ea3e0e1c4c17aa13ef7352a13457" id="tgt6" class="tgtSentence">Establecer la entidad de administración de dispositivos móviles</caps:sentence>
            </embeddedLabel>
            <br />
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="6fc81d6d528adf6203e8fcc52e55f1c0" id="tgt7" class="tgtSentence">Considere detenidamente si quiere administrar los dispositivos móviles solo mediante Intune, mediante la integración de System Center Configuration Manager con Intune o mediante Office 365.</caps:sentence>
              <caps:sentence sentenceid="74e62f841ac3d36b6839a1e04dde3065" id="tgt8" class="tgtSentence"> Una vez establecida alguna de estas opciones como entidad de administración de dispositivos móviles, no se podrá cambiar.</caps:sentence>
              <caps:sentence sentenceid="ea7a585d4a0cc7fd1ce12c6dcb4f9bad" id="tgt9" class="tgtSentence"> Si no está seguro de las opciones, vea <link xlink:href="2d91b8b5-bf44-4562-ab4a-6611584f9674">Different ways to manage your devices with Microsoft Intune</link>.</caps:sentence>
            </para>
          </alert>
          <procedure address="BKMK_Set_MDM_Authority">
            <title>
              <caps:sentence sentenceid="2368ea3e0e1c4c17aa13ef7352a13457" id="tgt10" class="tgtSentence">Establecer la entidad de administración de dispositivos móviles</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt11" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt12" class="tgtSentence">En la lista <ui>Tareas</ui>, haga clic en <ui>Configurar entidad de administración de dispositivos móviles</ui>.</caps:sentence>
                    <caps:sentence sentenceid="90adbbe7112a5ab0269194573e650cc6" id="tgt13" class="tgtSentence"> Se abre el cuadro de diálogo <ui>Establecer entidad de administración de dispositivos móviles</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="ac87b0ae-d498-456d-9f49-bbd6147e030a"></image>
                  </mediaLink>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="10283baadf2ea84205b10159f99d98ff" id="tgt14" class="tgtSentence">Intune solicita confirmación de que desea que Intune sea su entidad de MDM.</caps:sentence>
                    <caps:sentence sentenceid="c09e2ebec8853984449cf155a73bd423" id="tgt15" class="tgtSentence"> Active la casilla y haga clic en <ui>Sí</ui> si desea utilizar Microsoft Intune para administrar dispositivos móviles.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="0911002e9d7693038dbc102b3ad42268" id="tgt16" class="tgtSentence">Ahora que Intune es la entidad de MDM, puede habilitar la inscripción para dispositivos:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence sentenceid="60e15fe129757b9fbfd84a4e54a86b90" id="tgt17" class="tgtSentence">Habilitar la administración de iOS</caps:sentence>
                          </linkText>
                          <linkUri>https://technet.microsoft.com/library/dn408185.aspx</linkUri>
                        </externalLink>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence sentenceid="969edea7a3030a8f3454abb302ec8237" id="tgt18" class="tgtSentence">Habilitar la administración de Android</caps:sentence>
                          </linkText>
                          <linkUri>https://technet.microsoft.com/library/dn764960.aspx</linkUri>
                        </externalLink>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence sentenceid="896604df2a17073ca5f599ab4f1da7ff" id="tgt19" class="tgtSentence">Configurar la administración de Windows Phone</caps:sentence>
                          </linkText>
                          <linkUri>https://technet.microsoft.com/library/dn764959.aspx</linkUri>
                        </externalLink>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence sentenceid="9ff0e21677ea34392c434c273731d6da" id="tgt20" class="tgtSentence">Habilitar la administración de Windows</caps:sentence>
                          </linkText>
                          <linkUri>https://technet.microsoft.com/library/mt346003.aspx</linkUri>
                        </externalLink>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Set up device enrollment in Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Before users  can enroll mobile devices with <token>wit_nextref</token>, the IT administrator must declare <token>wit_nextref</token> as the <newTerm>mobile device management authority</newTerm>.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> A  <newTerm>mobile device management authority</newTerm> defines the single management service with permission to manage a set of devices.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence">  Solutions for the mobile device management authority include <token>wit_nextref</token>, Configuration Manager with <token>wit_nextref</token>, or Office 365 MDM solutions.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">This guidance assumes Intune is used without System Center Configuration Manager integration so the setting should be set to Microsoft Intune.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">MDM authority</caps:sentence>
        </title>
        <content>
          <para>
            <embeddedLabel>
              <caps:sentence id="src6" class="srcSentence">Set mobile device management authority</caps:sentence>
            </embeddedLabel>
            <br />
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src7" class="srcSentence">Consider carefully whether you want to manage mobile devices using Intune only, System Center Configuration Manager with Intune integration, or using Office 365.</caps:sentence>
              <caps:sentence id="src8" class="srcSentence"> After you set the mobile device management authority to either of these options, it cannot be changed again.</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> If you're unsure of your options, see <link xlink:href="2d91b8b5-bf44-4562-ab4a-6611584f9674">Different ways to manage your devices with Microsoft Intune</link>.</caps:sentence>
            </para>
          </alert>
          <procedure address="BKMK_Set_MDM_Authority">
            <title>
              <caps:sentence id="src10" class="srcSentence">Set mobile device management authority</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">In the <ui>Tasks</ui> list, click <ui>Set Mobile Device Management Authority</ui>.</caps:sentence>
                    <caps:sentence id="src13" class="srcSentence"> The <ui>Set MDM Authority</ui> dialog box opens.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="ac87b0ae-d498-456d-9f49-bbd6147e030a"></image>
                  </mediaLink>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">Intune requests confirmation that you want Intune as your MDM authority.</caps:sentence>
                    <caps:sentence id="src15" class="srcSentence"> Check the box and then click <ui>Yes</ui> to use Microsoft Intune to manage mobile devices.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Now that Intune is the MDM authority, you can enable device enrollment for devices:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence id="src17" class="srcSentence">Enable iOS management</caps:sentence>
                          </linkText>
                          <linkUri>https://technet.microsoft.com/library/dn408185.aspx</linkUri>
                        </externalLink>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence id="src18" class="srcSentence">Enable Android management</caps:sentence>
                          </linkText>
                          <linkUri>https://technet.microsoft.com/library/dn764960.aspx</linkUri>
                        </externalLink>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence id="src19" class="srcSentence">Enable Windows Phone management</caps:sentence>
                          </linkText>
                          <linkUri>https://technet.microsoft.com/library/dn764959.aspx</linkUri>
                        </externalLink>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <externalLink>
                          <linkText>
                            <caps:sentence id="src20" class="srcSentence">Enable Windows management</caps:sentence>
                          </linkText>
                          <linkUri>https://technet.microsoft.com/library/mt346003.aspx</linkUri>
                        </externalLink>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Set up device enrollment in Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>