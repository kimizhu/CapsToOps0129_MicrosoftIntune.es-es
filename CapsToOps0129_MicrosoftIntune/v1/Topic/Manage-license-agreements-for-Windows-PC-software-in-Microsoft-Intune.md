---
title: Administrar contratos de licencia de software de equipos Windows en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c59d8635-3f66-40f5-824a-a71c738e0341
---
# Administrar contratos de licencia de software de equipos Windows en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="191a92d99a7c524000d8af9724282146" id="tgt1" class="tgtSentence">
            <token>wit_firstref</token> le permite agregar y administrar la información del contrato de licencia para el software que haya adquirido mediante contratos de licencias por volumen de Microsoft y para el software de Microsoft (o de terceros que no sean Microsoft) que se adquirió por otros medios.</caps:sentence>
          <caps:sentence sentenceid="4f1fbebb1df891a17f8749ac160edb51" id="tgt2" class="tgtSentence"> Asimismo, también puede organizar esta información en grupos lógicos.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="bfa5c7b48d0ef22b5a9ed9e13487ac9d" id="tgt3" class="tgtSentence">Esta característica se proporciona solo para fines de comodidad, no se puede garantizar su precisión.</caps:sentence>
            <caps:sentence sentenceid="3de6604faf10db5db7d26c94604701f4" id="tgt4" class="tgtSentence"> No debe basarse en ella para confirmar el cumplimento de los contratos de licencias por volumen de Microsoft.</caps:sentence>
            <caps:sentence sentenceid="36687b7997d061893d14ab0c09a76998" id="tgt5" class="tgtSentence"> Microsoft no usará los datos recopilados para investigar posibles infracciones o el cumplimiento de los contratos de licencia que pudiera haber suscrito con nosotros.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="530bd177512a771a371eb85cc6a6ecef" id="tgt6" class="tgtSentence">Las licencias que agregue a <token>wit_nextref</token> no afectan a los contratos de licencia ni a sus derechos de uso del software.</caps:sentence>
            <caps:sentence sentenceid="804ec6448581c2b2ed7806fee31b40dd" id="tgt7" class="tgtSentence">  Por ejemplo, cuando se elimina un par de contrato y licencia de <token>wit_nextref</token>, no se eliminan ni se anulan los contratos de licencia que existan entre el usuario y Microsoft.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt8" class="tgtSentence">En el área de trabajo <ui>Licencias</ui> de la consola de administrador de <token>wit_nextref</token>, puede:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="4b591b188eb303a2e407896349bd498a" id="tgt9" class="tgtSentence">
          Agregar y editar contratos de licencias por volumen de Microsoft</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5cc89a2a15ea299090218a9d86c52027" id="tgt10" class="tgtSentence">
          Agregar y editar otros contratos de licencias de software
        </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a5807a4167d32a7ee830c2bead46216a" id="tgt11" class="tgtSentence">Administrar licencias y grupos</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e910a955d7b214086e622d2618466d34" id="tgt12" class="tgtSentence">Compare la información de derechos que <token>wit_nextref</token> recupera del Centro de servicios de licencias por volumen (VLSC) con el inventario de software de Microsoft que <token>wit_nextref</token> detecta en los equipos administrados de Windows.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="127cd2514c699db725c0ee92db82d890" id="tgt13" class="tgtSentence">Asimismo, puede generar informes que muestran recuentos de instalaciones y de licencias de títulos de software.</caps:sentence>
          <caps:sentence sentenceid="2265b52c1d2b13065161798050816db3" id="tgt14" class="tgtSentence"> Los informes de licencias pueden ayudarle a evaluar su posición completa respecto a las licencias para los títulos de software con licencia de Microsoft y de otros fabricantes.</caps:sentence>
        </para>
        <alert class="tip">
          <para>
            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt15" class="tgtSentence">El área de trabajo <ui>Licencias</ui> no se muestra en la consola de administrador hasta que administre al menos un equipo Windows con el equipo cliente de <token>wit_nextref</token>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="702e87d5588e8f9b80613c1c8afdac3c" id="tgt16" class="tgtSentence">Agregar contratos de licencias por volumen de Microsoft</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bd9f57384490d0cfd38e90812e20615d" id="tgt17" class="tgtSentence">Los contratos de licencias por volumen de <token>wit_nextref</token> proporcionan información de licencias del software adquirido a través de contratos de licencias por volumen de Microsoft.</caps:sentence>
            <caps:sentence sentenceid="53672871fddf78340f72841b13059369" id="tgt18" class="tgtSentence"> Puede agregar contratos de licencias por volumen de Microsoft a <token>wit_nextref</token> mediante pares coincidentes de números de contrato.</caps:sentence>
            <caps:sentence sentenceid="a9718f427de603101e4316016c811cc7" id="tgt19" class="tgtSentence"> Los números de autorización o contrato deben coincidir con los números de inscripción o licencia correctos.</caps:sentence>
            <caps:sentence sentenceid="a384dd2a4403134ae8e73579b7f8d183" id="tgt20" class="tgtSentence"> Los pares de números de contrato se obtienen al adquirir los contratos de licencia del <externalLink><linkText>Volume Licensing Service Center (VLSC)</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=223842</linkUri></externalLink>.</caps:sentence>
          </para>
          <procedure address="BKMK_AddVLAgreements" expanded="false">
            <title>
              <caps:sentence sentenceid="6a31f0a1c5387630f49feae1a5d3873b" id="tgt21" class="tgtSentence">Agregar un contrato de licencias por volumen de Microsoft</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt22" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://account.manage.microsoft.com/admin/default.aspx</linkUri></externalLink>, haga clic en <ui>Licencias</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt23" class="tgtSentence">En la página <ui>Agregar contratos</ui>, en <ui>Elegir tipo de contrato</ui>, seleccione <ui>Contrato de licencias por volumen</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt24" class="tgtSentence">En la sección <ui>Agregar detalles del contrato</ui>, elija una de las siguientes opciones:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="fbd8ad481d8a7fa924c64113119d1e13" id="tgt25" class="tgtSentence">
                          <ui>Cargar un archivo CSV que contiene detalles del contrato</ui>: haga clic en Buscar y seleccione el archivo CSV que desea cargar.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="1f8d90ccd4fae6ea781185b3effdbf8b" id="tgt26" class="tgtSentence">El archivo puede contener dos o tres columnas: dos para los pares de contratos solos, o tres si desea agregar un nombre descriptivo para cada par de contratos.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="5f6d64de1d730e9d8b6c552d46f4db55" id="tgt27" class="tgtSentence">El número total de caracteres en un par de números de contrato no puede superar los 16 caracteres ASCII.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="a92c05fafaa1ca81ebfff2a43b2616f5" id="tgt28" class="tgtSentence">Únicamente se admiten caracteres ASCII.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="09374d95d4d64898b33c576d78a4fa5e" id="tgt29" class="tgtSentence">No se admiten los siguientes caracteres en el nombre del contrato: <system>~ ! @ # $ ^ &amp; * ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /</system>. Se permiten espacios en el nombre.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="25dec5df4c0c9d10e9ba1e642b92242b" id="tgt30" class="tgtSentence">El nombre de archivo no debe tener más de 128 caracteres.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="8af06ff6266a6f8b891f0f84e04dd6db" id="tgt31" class="tgtSentence">El archivo debe contener al menos un par de contratos y no puede contener más de 5.000 pares de contratos.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1fc9ec1988963baaaace626bf220fb38" id="tgt32" class="tgtSentence">Formato del archivo</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence sentenceid="fe697fe880660d96f1aa7128cc5b9a25" id="tgt33" class="tgtSentence">Para crear este archivo puede agregar los pares de contratos en un documento de texto sin formato con uno de los siguientes formatos, en función del tipo de organización que registrase en el VLSC.</caps:sentence>
                        <caps:sentence sentenceid="1075d8ca7d52c8b50eabacf9eba9848a" id="tgt34" class="tgtSentence"> Especifique un par de números de contrato por línea.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="8e2237c00eca06c96d1d66c5a5b546c7" id="tgt35" class="tgtSentence">
                              <embeddedLabel>Clientes de Open Value:</embeddedLabel>  <placeholder>Número de contrato</placeholder>, <placeholder>repetir número de contrato</placeholder>, <placeholder>nombre del contrato</placeholder></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="8e2237c00eca06c96d1d66c5a5b546c7" id="tgt36" class="tgtSentence">
                              <embeddedLabel>Clientes de Open:</embeddedLabel>  <placeholder>Número de autorización</placeholder>, <placeholder>número de licencia relacionado</placeholder>, <placeholder>nombre del contrato</placeholder></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="8e2237c00eca06c96d1d66c5a5b546c7" id="tgt37" class="tgtSentence">
                              <embeddedLabel>Clientes de Select y Enterprise:</embeddedLabel>  <placeholder>Número de contrato</placeholder>, <placeholder>número de inscripción relacionado</placeholder>, <placeholder>nombre del contrato</placeholder></caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt38" class="tgtSentence">El formulario <ui>Agregar contratos</ui> le solicitará que busque este archivo cuando agregue un nuevo contrato.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="012361f62ff1493b59e5c51a3d96d871" id="tgt39" class="tgtSentence">A continuación se muestra un ejemplo de contenido de un archivo .csv de un cliente de Open Value.</caps:sentence>
                      </para>
                      <para>
                        <codeInline>01-07001, 01-07001, Office agreements</codeInline>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c1b2c42016f33bc1e2b811489816426d" id="tgt40" class="tgtSentence">
                          <ui>Agregar manualmente detalles del contrato</ui>: proporcione la información siguiente y escriba los pares de números de contrato en los cuadros <ui>Número de autorización/contrato</ui> y <ui>Número de licencia/inscripción/cliente</ui>.</caps:sentence>
                        <caps:sentence sentenceid="52dd1ee14db8acb26289e2d97da0ae1e" id="tgt41" class="tgtSentence"> Después de escribir los dos números, haga clic en el icono <ui>Agregar par de números</ui> para guardar los números y, a continuación, agregue un par nuevo si lo desea.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="644783a0944b72218a790c6dc117b40e" id="tgt42" class="tgtSentence">
                              <ui>Nombre del contrato</ui>: especifique un nombre único para el contrato.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="5cb08823d6b6cc0e699b8d75514fe986" id="tgt43" class="tgtSentence">El nombre del contrato puede tener 256 caracteres como máximo y no puede contener los caracteres siguientes: <system>~ ! @ # $ ^ &amp; * ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /</system>. Se permiten espacios en el nombre.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="16017f809ea6972ab982629d42479853" id="tgt44" class="tgtSentence">
                              <ui>Número de autorización/contrato</ui>: especifique el número de autorización/contrato del par de licencia.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="984479d9419865d61f251645aebe9eed" id="tgt45" class="tgtSentence">
                              <ui>Número de licencia/inscripción/cliente</ui>: especifique el número de licencia/inscripción/cliente del par de licencia.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="f2212ca3c5e83208f321542840b6f4ed" id="tgt46" class="tgtSentence">Si agrega varios pares de números de contrato, <token>wit_nextref</token> creará un contrato con el nombre que especifique, y todos los pares que agregó formarán parte de ese contrato.</caps:sentence>
                        </para>
                      </alert>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="43f3b1d1afb199123de5651f4546809f" id="tgt47" class="tgtSentence">Puede hacer clic en <ui>+</ui> para agregar otro par de números de contrato, o en <ui>-</ui> para quitar un par de números de contrato que ya haya escrito.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt48" class="tgtSentence">En el área <ui>Seleccionar grupo de licencias</ui>, realice alguna de las acciones siguientes:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt49" class="tgtSentence">Seleccione <ui>Agregar los contratos a un grupo de contratos sin asignar</ui> si no desea agregar los nuevos contratos a un grupo de licencias.</caps:sentence>
                        <caps:sentence sentenceid="b8861f8fa2ae2311044ea4ed50263d88" id="tgt50" class="tgtSentence"> Puede editar el contrato más adelante si decide agregarlo a un grupo.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt51" class="tgtSentence">Para agregar los nuevos contratos a un nuevo grupo de licencias, seleccione <ui>Agregar los contratos a un nuevo grupo de licencias</ui>.</caps:sentence>
                        <caps:sentence sentenceid="a63d3f637666b8eb97beadb9e494b8f2" id="tgt52" class="tgtSentence"> Se le solicitará que indique un nombre para el nuevo grupo de licencias.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt53" class="tgtSentence">Para agregar los nuevos contratos a un grupo de licencias existente, seleccione <ui>Agregar los contratos a un grupo de licencias existente</ui>.</caps:sentence>
                        <caps:sentence sentenceid="4f4f145aafdf6ea8a38164ebe7706661" id="tgt54" class="tgtSentence"> En la lista <ui>Nombre del grupo</ui>, seleccione el grupo de licencias al que desea agregar los contratos.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt55" class="tgtSentence">Haga clic en <ui>Aceptar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt56" class="tgtSentence">Se muestra la vista <ui>Todos los contratos</ui> y <token>sco_dm_2</token> se conecta al Centro de servicios de licencias por volumen de Microsoft para validar los pares de números de contrato proporcionados.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="ae586489a481b23e082c59a2a37d52c3" id="tgt57" class="tgtSentence">Para actualizar la información de licencias por volumen después de haber agregado contratos de licencias a <token>wit_nextref</token>, en la página <ui>Información general sobre licencias</ui>, haga clic en <ui>Actualizar ahora</ui>.</caps:sentence>
                  <caps:sentence sentenceid="ec18dbbc923ab9152bb3a7fa21f62233" id="tgt58" class="tgtSentence"> Esta acción permite recuperar la información actual de las licencias del <externalLink><linkText>Microsoft Volume Licensing Service Center (VLSC) (Centro de servicios de licencias por volumen (VLSC) de Microsoft)</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=223842</linkUri></externalLink>.</caps:sentence>
                </para>
                <alert class="important">
                  <para>
                    <caps:sentence sentenceid="c48664d23e8fb7056e07a4da9f02f554" id="tgt59" class="tgtSentence">Hasta que actualice la información de licencias por volumen, es posible que vea una información diferente en la lista de contratos y en la información de derechos de la página <ui>Información general sobre contratos</ui>.</caps:sentence>
                  </para>
                </alert>
                <para>
                  <caps:sentence sentenceid="6b67c7ff5a51accb09847a2cad4d5e4f" id="tgt60" class="tgtSentence">Después de actualizar la información de licencias por volumen, puede comparar la información de licencias con el software de Microsoft detectado en el área de trabajo <ui>Aplicaciones</ui>.</caps:sentence>
                  <caps:sentence sentenceid="f1c5f4cada11f30f46f03f1518a0794d" id="tgt61" class="tgtSentence"> Igualmente, también puede ejecutar los siguientes informes de licencia:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="a86ee2e583755d118e0d8f354c532da2" id="tgt62" class="tgtSentence">
                        <ui>Informes de adquisición de licencias</ui>: le permiten ver el software con licencia en los grupos de licencias que seleccione para ayudarle a encontrar deficiencias en la cobertura.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="954924c287822177231f5597ccc5fa4f" id="tgt63" class="tgtSentence">
                        <ui>Informes de instalación de licencias</ui>: le ayudan a determinar si los contratos de licencia proporcionan una cobertura suficiente.</caps:sentence>
                    </para>
                  </listItem>
                </list>
                <alert class="note">
                  <para>
                    <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt64" class="tgtSentence">El <ui>Título del producto</ui> que se muestra para todos los contratos de licencias por volumen de Microsoft es <ui>No disponible</ui>.</caps:sentence>
                  </para>
                </alert>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="df7d2d1c7533f357d85abc9f0d132c80" id="tgt65" class="tgtSentence">Agregar y editar otros contratos de licencias de software
        </caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f939d65393109fbc6725d99ce8eb8a93" id="tgt66" class="tgtSentence">También puede agregar otros tipos de contratos de licencias a <token>wit_firstref</token>, además de los contratos de licencias por volumen de Microsoft.</caps:sentence>
            <caps:sentence sentenceid="830da9d1e23c0a00fa2cf88be32da7bb" id="tgt67" class="tgtSentence"> Estos contratos pueden incluir software que no sea de Microsoft o software de Microsoft adquirido a través de un distribuidor.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="e90c90f43a6833be89aa2e2da44b1e5a" id="tgt68" class="tgtSentence">Debe tener al menos un equipo Windows inscrito en <token>wit_nextref</token> para poder agregar un contrato.</caps:sentence>
              <caps:sentence sentenceid="2ffe1216709e4380ad498131d62898df" id="tgt69" class="tgtSentence">  De igual manera, al menos un equipo inscrito debe tener cargado el paquete de software sujeto a licencia que desee usar para agregar un contrato de licencia.</caps:sentence>
            </para>
          </alert>
          <procedure address="BKMK_AddOtherSoftwareAgreement" expanded="false">
            <title>
              <caps:sentence sentenceid="103792690479ff4c7a36292fae0a90b3" id="tgt70" class="tgtSentence">Para agregar otros contratos de software</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt71" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://account.manage.microsoft.com/admin/default.aspx</linkUri></externalLink>, haga clic en <ui>Licencias</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt72" class="tgtSentence">Haga clic en <ui>Agregar contratos</ui> en la sección <ui>Otros contratos de licencias de software</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt73" class="tgtSentence">Seleccione <ui>Otro contrato de licencias de software</ui> en la sección <ui>Elegir tipo de contrato</ui> de la página <ui>Agregar contratos</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt74" class="tgtSentence">En el área <ui>Agregar detalles del contrato</ui>, especifique lo siguiente:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a870f42bf18e9049fdf2d96660fcee20" id="tgt75" class="tgtSentence">
                          <ui>Nombre del contrato</ui> (obligatorio). El nombre del contrato puede tener 256 caracteres como máximo y no puede contener los caracteres siguientes: <system>~ ! @ # $ ^ &amp; * ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /</system>. Se permiten espacios en el nombre.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="629ec65204120cd9f99b5265c93829ae" id="tgt76" class="tgtSentence">
                          <ui>Publicador</ui> (obligatorio).</caps:sentence>
                        <caps:sentence sentenceid="2f15b6ea78b8f0655cb9297e9790dc7e" id="tgt77" class="tgtSentence"> Cuando empiece a escribir el nombre de un publicador, el servicio recupera todos los nombres de publicador que contienen las letras que escribe.</caps:sentence>
                        <caps:sentence sentenceid="c3044af34387d740ca0cabd1702fdfde" id="tgt78" class="tgtSentence"> Por ejemplo, si escribe "soft", el servicio recupera todos los nombres de editor que contienen "soft" como parte del nombre, tal como "Microsoft" y "Microsoft Research".</caps:sentence>
                        <caps:sentence sentenceid="f91e716028f620665fcfbd567d6de459" id="tgt79" class="tgtSentence"> Los nombres de publicador se recuperan del catálogo de activos de software.</caps:sentence>
                        <caps:sentence sentenceid="2931ef1dd759eed99d6433f49ee4fabe" id="tgt80" class="tgtSentence"> Debe seleccionar el publicador para poder especificar el título del producto.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence sentenceid="734b539866a3eca6f0343b7f025828f8" id="tgt81" class="tgtSentence">La empresa que desea agregar podría no aparecer en esta lista.</caps:sentence>
                          <caps:sentence sentenceid="7a779af6338d67d83f8018db0a6eca67" id="tgt82" class="tgtSentence"> Solo puede agregar contratos de software de empresas que ya están presentes en el catálogo de activos de software.</caps:sentence>
                          <caps:sentence sentenceid="a2108ba51e38ffba5f542d9da3af23b1" id="tgt83" class="tgtSentence"> De todos modos, Microsoft trabaja sin descanso para agregar los títulos de software más populares.</caps:sentence>
                          <caps:sentence sentenceid="e8185dbb7d893943b3c200d02a088ea5" id="tgt84" class="tgtSentence"> Si desea enviar una solicitud para agregar una empresa a esta lista, puede hacerlo en el <externalLink><linkText>sitio de Intune Uservoice</linkText><linkUri>https://microsoftintune.uservoice.com/</linkUri></externalLink>.</caps:sentence>
                        </para>
                      </alert>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="629ec65204120cd9f99b5265c93829ae" id="tgt85" class="tgtSentence">
                          <ui>Título del producto</ui> (obligatorio).</caps:sentence>
                        <caps:sentence sentenceid="69b6c044f4450501d6dd25f47b54d5a4" id="tgt86" class="tgtSentence"> Cuando empiece a escribir el título del producto, el servicio recupera todos los títulos de producto que contienen las letras que escribe.</caps:sentence>
                        <caps:sentence sentenceid="0784bd5efa9cdba061a068771f2a33b6" id="tgt87" class="tgtSentence"> Debe especificar un <ui>Publicador</ui> para poder especificar un <ui>Título del producto</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="629ec65204120cd9f99b5265c93829ae" id="tgt88" class="tgtSentence">
                          <ui>Número de licencias</ui> (obligatorio).</caps:sentence>
                        <caps:sentence sentenceid="90e713d6c836216438f6d97e6ae37789" id="tgt89" class="tgtSentence"> Especifique el número de licencias adquiridas.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5058f1af8388633f609cadb75a75dc9d" id="tgt90" class="tgtSentence">
                          <ui>Fecha de inicio de la licencia</ui>.</caps:sentence>
                        <caps:sentence sentenceid="90d33c536690afad27876291024c1890" id="tgt91" class="tgtSentence"> Especifique la fecha de inicio de la cobertura de la licencia.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5058f1af8388633f609cadb75a75dc9d" id="tgt92" class="tgtSentence">
                          <ui>Fecha final de la licencia</ui>.</caps:sentence>
                        <caps:sentence sentenceid="0dd73fd3cd70b481ac9306925f93464e" id="tgt93" class="tgtSentence"> Especifique la fecha final de la cobertura de la licencia.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5058f1af8388633f609cadb75a75dc9d" id="tgt94" class="tgtSentence">
                          <ui>Detalles del contrato</ui>.</caps:sentence>
                        <caps:sentence sentenceid="5f037b44d9af6662558af9611b53e512" id="tgt95" class="tgtSentence"> Opcionalmente, puede especificar información de contacto, las claves de registro y otros datos.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt96" class="tgtSentence">En el área <ui>Seleccionar grupo de licencias</ui>, realice alguna de las acciones siguientes:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt97" class="tgtSentence">Si no desea agregar los nuevos contratos a un grupo de licencias nuevo o existente, seleccione <ui>Agregar los contratos a un grupo de contratos sin asignar</ui>.</caps:sentence>
                        <caps:sentence sentenceid="9533016f79d657ecd52cf1e39dc147ee" id="tgt98" class="tgtSentence"> Puede agregar los contratos a grupos de licencias definidos por el usuario en cualquier momento.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt99" class="tgtSentence">Para agregar los nuevos contratos a un nuevo grupo de licencias, seleccione <ui>Agregar los contratos a un nuevo grupo de licencias</ui>.</caps:sentence>
                        <caps:sentence sentenceid="a63d3f637666b8eb97beadb9e494b8f2" id="tgt100" class="tgtSentence"> Se le solicitará que indique un nombre para el nuevo grupo de licencias.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt101" class="tgtSentence">Para agregar los nuevos contratos a un grupo de licencias existente, seleccione <ui>Agregar los contratos a un grupo de licencias existente</ui>.</caps:sentence>
                        <caps:sentence sentenceid="4f4f145aafdf6ea8a38164ebe7706661" id="tgt102" class="tgtSentence"> En la lista <ui>Nombre del grupo</ui>, seleccione el grupo de licencias al que desea agregar los contratos.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt103" class="tgtSentence">Haga clic en <ui>Aceptar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt104" class="tgtSentence">Se muestra la vista de lista <ui>Todos los contratos</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_LicenseGroups">
        <title>
          <caps:sentence sentenceid="d3511a79e7f6899366d95b6521eb43ab" id="tgt105" class="tgtSentence">Administrar contratos de licencia</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8e7a5f52669d917ebfc3166b430e6bba" id="tgt106" class="tgtSentence">
        Los contratos de licencias de software pueden agregarse a grupos de licencias.</caps:sentence>
            <caps:sentence sentenceid="c15b134ae857d5741be3464d95ede285" id="tgt107" class="tgtSentence"> Puede utilizar grupos de licencias para organizar los contratos de licencias en unidades lógicas para la organización.</caps:sentence>
            <caps:sentence sentenceid="b8baff856f3a573d8f0572fcee9371bf" id="tgt108" class="tgtSentence"> Igualmente, puede eliminar los contratos de licencia que creó anteriormente.</caps:sentence>
          </para>
          <table border="1">
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="478f3a4c51824ad23cb50c1c60670c0f" id="tgt109" class="tgtSentence">Tarea</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt110" class="tgtSentence">Detalles</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="89e222e5f5a66f20309b9cba895c9d27" id="tgt111" class="tgtSentence">Crear un grupo de licencias</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt112" class="tgtSentence">En la página <ui>Información general</ui>, del área de trabajo <ui>Licencias</ui>, haga clic en <ui>Crear grupo de licencias</ui> en el menú <ui>Tareas</ui>.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="a32db513c8bbacd0b82bdca9657b636d" id="tgt113" class="tgtSentence">Puede crear como máximo 500 grupos de licencias.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="25d342baf210c992c53f393c48dbd2ba" id="tgt114" class="tgtSentence">Cambiar el nombre de un grupo de licencias</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt115" class="tgtSentence">En el área de trabajo <ui>Licencias</ui>, elija un grupo de licencias y haga clic en <ui>Editar grupo de licencias</ui> en el menú <ui>Tareas</ui>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="46108881beafcd5d886a5c69e449c35f" id="tgt116" class="tgtSentence">Eliminar un grupo de licencias</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt117" class="tgtSentence">En el área de trabajo <ui>Licencias</ui>, elija un grupo de licencias y haga clic en <ui>Eliminar grupo de licencias</ui> en el menú <ui>Tareas</ui>.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="7bcbb1a3625a7f570055b9cd4fa51c10" id="tgt118" class="tgtSentence">Una vez hecho esto, todas las licencias que se encontraban en el grupo eliminado se llevan al grupo de licencias <ui>Contratos sin asignar</ui>.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7ce94e9b5b5d725e7e5964a2f9016a00" id="tgt119" class="tgtSentence">Eliminar un contrato de licencia</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt120" class="tgtSentence">En el área de trabajo <ui>Licencias</ui>, elija un contrato y haga clic en <ui>Eliminar</ui>.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="5d6b7060229e245d69b0589703872314" id="tgt121" class="tgtSentence">Después de eliminar los contratos de licencias por volumen, para actualizar la información de licencia, haga clic en <ui>Actualizar ahora</ui> en la página <ui>Información general sobre licencias</ui> o en la ficha <ui>General</ui> para un grupo de licencias determinado.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb">Deploy apps to computers in Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">
            <token>wit_firstref</token> lets you add and manage license agreement information for software that was purchased through Microsoft Volume Licensing agreements, and for Microsoft or non-Microsoft software that was purchased by other means.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You can also organize this information into logical groups.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src3" class="srcSentence">This feature is provided for convenience only and accuracy is not guaranteed.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> You should not rely on it to confirm compliance with Microsoft Volume Licensing agreements.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Microsoft will not use any data gathered to investigate potential violations of, or compliance with license agreements you may have with us.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">Licenses you add to <token>wit_nextref</token> do not affect your license agreements or entitlements to use your software.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence">  For example, deleting a license/agreement pair from <token>wit_nextref</token>, you do not delete or nullify license agreements that exist between you and Microsoft.</caps:sentence>
          </para>
        </alert>
        <para>
          <caps:sentence id="src8" class="srcSentence">In the <ui>Licenses</ui> workspace of the <token>wit_nextref</token> administrator console, you can:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">
          Add and edit Microsoft Volume Licensing agreements</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">
          Add and edit other software licensing agreements
        </caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">Manage licenses and groups</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Compare the entitlement information that <token>wit_nextref</token> retrieves from the Volume Licensing Service Center (VLSC) to the inventory of Microsoft software that <token>wit_nextref</token> detects on your managed Windows PCs.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src13" class="srcSentence">Additionally, you can generate reports that show installation and license counts for software titles.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> License reports can help you assess your complete license position for Microsoft software and non-Microsoft software titles.</caps:sentence>
        </para>
        <alert class="tip">
          <para>
            <caps:sentence id="src15" class="srcSentence">The <ui>Licenses</ui> workspace is not displayed in the administrator console until you are managing at least one Windows PC with the <token>wit_nextref</token> computer client.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Add Microsoft Volume Licensing agreements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">
              <token>wit_nextref</token> Volume Licensing agreements provide license information for software that was purchased through Microsoft Volume Licensing agreements.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> You can add Microsoft Volume Licensing agreements to <token>wit_nextref</token> by providing matched pairs of agreement numbers.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> The agreement or authorization numbers must be matched to the correct license or enrollment numbers.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> Agreement number pairs are obtained when you purchase your license agreements from the <externalLink><linkText>Volume Licensing Service Center (VLSC)</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=223842</linkUri></externalLink>.</caps:sentence>
          </para>
          <procedure address="BKMK_AddVLAgreements" expanded="false">
            <title>
              <caps:sentence id="src21" class="srcSentence">To add a Microsoft Volume Licensing agreement</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administrator console</linkText><linkUri>https://account.manage.microsoft.com/admin/default.aspx</linkUri></externalLink>, click <ui>Licenses</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">On the <ui>Add Agreements</ui> page, under <ui>Choose Agreement Type</ui>, select <ui>Volume Licensing agreement</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">In the <ui>Add Agreement Details</ui> section, choose one of:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src25" class="srcSentence">
                          <ui>Upload a CSV file that contains agreement details</ui> - Click Browse and select the CSV file you want to upload.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src26" class="srcSentence">The file can contain either two or three columns; two for agreement pairs alone, or three if you want to add a friendly name for each agreement pair.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src27" class="srcSentence">The total number of characters in an agreement number pair cannot exceed 16 ASCII characters.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src28" class="srcSentence">Only ASCII characters are supported.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src29" class="srcSentence">The following characters are not allowed in the agreement name: <system>~ ! @ # $ ^ &amp; * ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /</system>. Spaces are allowed in the name.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src30" class="srcSentence">The file name must be no more than 128 characters in length.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src31" class="srcSentence">The file must contain at least one agreement pair and cannot contain more than 5,000 agreement pairs.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <ui>
                          <caps:sentence id="src32" class="srcSentence">Format for the file</caps:sentence>
                        </ui>
                      </para>
                      <para>
                        <caps:sentence id="src33" class="srcSentence">You can create this file by adding your agreement pairs to a plain text document in one of the following formats, depending on the organization type that you have registered with the VLSC.</caps:sentence>
                        <caps:sentence id="src34" class="srcSentence"> Specify one agreement number pair per line.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src35" class="srcSentence">
                              <embeddedLabel>Open Value Customers:</embeddedLabel>  <placeholder>Agreement number</placeholder>, <placeholder>repeat agreement number</placeholder>, <placeholder>agreement name</placeholder></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src36" class="srcSentence">
                              <embeddedLabel>Open Customers:</embeddedLabel>  <placeholder>Authorization number</placeholder>, <placeholder>related license number</placeholder>, <placeholder>agreement name</placeholder></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src37" class="srcSentence">
                              <embeddedLabel>Select and Enterprise Customers:</embeddedLabel>  <placeholder>Agreement number</placeholder>, <placeholder>related enrollment number</placeholder>, <placeholder>agreement name</placeholder></caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">The <ui>Add Agreements</ui> form prompts you to browse for this file when you add a new agreement.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src39" class="srcSentence">The following is an example of .csv file content for an Open Value customer.</caps:sentence>
                      </para>
                      <para>
                        <codeInline>01-07001, 01-07001, Office agreements</codeInline>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">
                          <ui>Manually add agreement details</ui> - Provide the following information, and then type the agreement number pairs in the <ui>Authorization/Agreement number</ui> and <ui>License/Enrollment/Customer number</ui> boxes.</caps:sentence>
                        <caps:sentence id="src41" class="srcSentence"> After you type both numbers, click the <ui>Add pair</ui> icon to save your numbers, and then optionally add a new pair.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src42" class="srcSentence">
                              <ui>Agreement name</ui> - Specify a unique name for the agreement.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src43" class="srcSentence">The agreement name can have a maximum of 256 characters, and cannot contain the following characters: <system>~ ! @ # $ ^ &amp; * ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /</system>. Spaces are allowed in the name.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src44" class="srcSentence">
                              <ui>Authorization/Agreement number</ui> - Enter the authorization/agreement number of the license pair.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src45" class="srcSentence">
                              <ui>License/Enrollment/Customer number</ui> - Enter the license/enrollment/customer number of the license pair.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src46" class="srcSentence">If you add several agreement number pairs, <token>wit_nextref</token> creates one agreement with the name that you specify, and all pairs that you added will be a part of this agreement.</caps:sentence>
                        </para>
                      </alert>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">You can click <ui>+</ui> to add another agreement number pair, or <ui>-</ui> to remove an agreement number pair you have already entered.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">In the <ui>Select License Group</ui> area, do one of the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">Select <ui>Add the agreements to the Unassigned Agreements group</ui> if you do not want to add the new agreements to a license group.</caps:sentence>
                        <caps:sentence id="src50" class="srcSentence"> You can edit the agreement later if you decide to add it to a group.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">Select <ui>Add the agreements to a new license group</ui> to add the new agreements to a new license group.</caps:sentence>
                        <caps:sentence id="src52" class="srcSentence"> You are prompted to provide a name for the new license group.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">Select <ui>Add the agreements to an existing license group</ui> to add the new agreements to an existing license group.</caps:sentence>
                        <caps:sentence id="src54" class="srcSentence"> In the <ui>Group name</ui> list, select the license group to which you want to add the agreements.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">Click <ui>OK</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src56" class="srcSentence">The <ui>All Agreements</ui> view is displayed, and <token>sco_dm_2</token> connects to the Microsoft Volume Licensing Service Center to validate the agreement number pairs that you provided.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src57" class="srcSentence">To update the volume license information after you have added license agreements in <token>wit_nextref</token>, in the <ui>Licenses Overview</ui> page, click <ui>Refresh Now</ui>.</caps:sentence>
                  <caps:sentence id="src58" class="srcSentence"> This action retrieves the current license information from the <externalLink><linkText>Microsoft Volume Licensing Service Center (VLSC)</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=223842</linkUri></externalLink>.</caps:sentence>
                </para>
                <alert class="important">
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Until you refresh the volume licensing information, you may see different information in the agreements list and the entitlement information on the <ui>Agreements Overview</ui> page.</caps:sentence>
                  </para>
                </alert>
                <para>
                  <caps:sentence id="src60" class="srcSentence">After you refresh the volume license information, you can compare the license information to your detected Microsoft software in the <ui>Apps</ui> workspace.</caps:sentence>
                  <caps:sentence id="src61" class="srcSentence"> You can also run the following license reports:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src62" class="srcSentence">
                        <ui>License Purchase Reports</ui> - Lets you view the licensed software in license groups you select to help you find gaps in coverage.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src63" class="srcSentence">
                        <ui>License Installation Reports</ui> - Helps you determine if you have sufficient license agreement coverage.</caps:sentence>
                    </para>
                  </listItem>
                </list>
                <alert class="note">
                  <para>
                    <caps:sentence id="src64" class="srcSentence">The <ui>Product Title</ui> displayed for all Microsoft Volume License agreements is <ui>Not available</ui>.</caps:sentence>
                  </para>
                </alert>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src65" class="srcSentence">Add and edit other software licensing agreements
        </caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src66" class="srcSentence">You can also add other types of license agreements to <token>wit_firstref</token> in addition to Microsoft Volume Licensing agreements.</caps:sentence>
            <caps:sentence id="src67" class="srcSentence"> These agreements can include non-Microsoft software or Microsoft software that was purchased through a retailer.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src68" class="srcSentence">You must have at least one Windows PC enrolled in <token>wit_nextref</token> before you can add an agreement.</caps:sentence>
              <caps:sentence id="src69" class="srcSentence">  In addition, at least one enrolled computer must have uploaded a licensable software package that you want to use to add a license agreement.</caps:sentence>
            </para>
          </alert>
          <procedure address="BKMK_AddOtherSoftwareAgreement" expanded="false">
            <title>
              <caps:sentence id="src70" class="srcSentence">To add other software agreements</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administrator console</linkText><linkUri>https://account.manage.microsoft.com/admin/default.aspx</linkUri></externalLink>, click <ui>Licenses</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">Click <ui>Add Agreements</ui> in the <ui>Other Software Licensing Agreements</ui> section.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">Select <ui>Other software licensing agreement</ui> in the <ui>Choose Agreement Type</ui> section of the <ui>Add Agreements</ui> page.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">In the <ui>Add Agreement Details</ui> area, specify the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src75" class="srcSentence">
                          <ui>Agreement name</ui> (required). The agreement name can have a maximum of 256 characters, and cannot contain the following characters: <system>~ ! @ # $ ^ &amp; * ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /</system>. Spaces are allowed in the name.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src76" class="srcSentence">
                          <ui>Publisher</ui> (required).</caps:sentence>
                        <caps:sentence id="src77" class="srcSentence"> When you start to type a publisher name, the service retrieves all publisher names that contain the letters that you type.</caps:sentence>
                        <caps:sentence id="src78" class="srcSentence"> For example, if you type “soft,” the service retrieves all publisher names that contain “soft” as part of the name, such as “Microsoft” and “Microsoft Research.”</caps:sentence>
                        <caps:sentence id="src79" class="srcSentence"> The publisher names are retrieved from the Software Asset Catalog.</caps:sentence>
                        <caps:sentence id="src80" class="srcSentence"> You must select the publisher before you can enter the product title.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence id="src81" class="srcSentence">The company that you want to add might not appear in this list.</caps:sentence>
                          <caps:sentence id="src82" class="srcSentence"> You can only add software agreements for companies that are already present in the software asset catalog.</caps:sentence>
                          <caps:sentence id="src83" class="srcSentence"> However, Microsoft continuously works to add the most popular software titles.</caps:sentence>
                          <caps:sentence id="src84" class="srcSentence"> If you would like to submit a request to have a company added to this list you can do so at the <externalLink><linkText>Intune Uservoice site</linkText><linkUri>https://microsoftintune.uservoice.com/</linkUri></externalLink>.</caps:sentence>
                        </para>
                      </alert>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src85" class="srcSentence">
                          <ui>Product title</ui> (required).</caps:sentence>
                        <caps:sentence id="src86" class="srcSentence"> When you start to type a product title, the service retrieves all product titles that contain the letters that you type.</caps:sentence>
                        <caps:sentence id="src87" class="srcSentence"> You must specify a <ui>Publisher</ui> before you can specify a <ui>Product title</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">
                          <ui>License count</ui> (required).</caps:sentence>
                        <caps:sentence id="src89" class="srcSentence"> Enter the number of purchased licenses.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">
                          <ui>License start date</ui>.</caps:sentence>
                        <caps:sentence id="src91" class="srcSentence"> Enter the start date of license coverage.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">
                          <ui>License end date</ui>.</caps:sentence>
                        <caps:sentence id="src93" class="srcSentence"> Enter the end date of license coverage.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src94" class="srcSentence">
                          <ui>Agreement details</ui>.</caps:sentence>
                        <caps:sentence id="src95" class="srcSentence"> You can optionally specify contact information, registration keys, and other information.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src96" class="srcSentence">In the <ui>Select License Group</ui> area, do one of the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src97" class="srcSentence">Select <ui>Add the agreements to the Unassigned Agreements group</ui> if you do not want to add the new agreements to a new or existing license group.</caps:sentence>
                        <caps:sentence id="src98" class="srcSentence"> You can add the agreements to user-defined license groups at any time.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src99" class="srcSentence">Select <ui>Add the agreements to a new license group</ui> to add the new agreements to a new license group.</caps:sentence>
                        <caps:sentence id="src100" class="srcSentence"> You are prompted to provide a name for the new license group.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">Select <ui>Add the agreements to an existing license group</ui> to add the new agreements to an existing license group.</caps:sentence>
                        <caps:sentence id="src102" class="srcSentence"> In the <ui>Group name</ui> list, select the license group to which you want to add the agreements.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src103" class="srcSentence">Click <ui>OK</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src104" class="srcSentence">The <ui>All Agreements</ui> list view is displayed.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_LicenseGroups">
        <title>
          <caps:sentence id="src105" class="srcSentence">Manage license agreements</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src106" class="srcSentence">
        Software licensing agreements can be added to license groups.</caps:sentence>
            <caps:sentence id="src107" class="srcSentence"> You can use license groups to organize your license agreements in units that are logical for your organization.</caps:sentence>
            <caps:sentence id="src108" class="srcSentence"> Additionally, you can delete license agreements which you previously created.</caps:sentence>
          </para>
          <table border="1">
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src109" class="srcSentence">Task</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">Details</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">Create a license group</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">On the <ui>Overview</ui> page of the <ui>Licenses</ui> workspace, click <ui>Create License Group</ui> from the <ui>Tasks</ui> menu.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src113" class="srcSentence">You can create a total maximum of 500 license groups.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">Rename a license group</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">In the <ui>Licenses</ui> workspace, choose a license group, and then click <ui>Edit License Group</ui> from the <ui>Tasks</ui> Menu.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">Delete a license group</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">In the <ui>Licenses</ui> workspace, choose a license group, and then click <ui>Delete License Group</ui> from the <ui>Tasks</ui> Menu.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src118" class="srcSentence">Any licenses that were in the deleted group are moved to the <ui>Unassigned agreements</ui> license group.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src119" class="srcSentence">Delete a license agreement</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">In the <ui>Licenses</ui> workspace, choose an agreement, and then click <ui>Delete</ui>.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src121" class="srcSentence">After you delete Volume Licensing agreements, to update the license information, click <ui>Refresh Now</ui> on the <ui>Licenses Overview</ui> page or on the <ui>General</ui> tab for a specific license group.</caps:sentence>
                    </para>
                  </alert>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="4105b676-11f1-4cd2-88a4-b37d186cdbdb">Deploy apps to computers in Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>