---
title: Solucionar problemas de actualizaciones de software en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d17b70f4-17b4-4d89-88fd-70fa4f34fbea
---
# Solucionar problemas de actualizaciones de software en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para></para>
      </introduction>
      <section address="BKMK_Updates" expanded="true">
        <title>
          <caps:sentence sentenceid="3e38dc0612a365332bdf4e84e4164710" id="tgt1" class="tgtSentence">Solucionar problemas con las actualizaciones de software</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6ddd11119bdb704c5d14caa38b7d6072" id="tgt2" class="tgtSentence">Use la información de esta sección para resolver problemas con las actualizaciones de software en <token>wit_firstref</token>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="2216aa10a4af093c21caebf234b74932" id="tgt3" class="tgtSentence">Códigos de error de actualización de software</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="2fa437cd5a379cd438dbb2db6109b6d8" id="tgt4" class="tgtSentence">En la tabla siguiente se muestran los códigos de error del Agente de <token>wit_firstref</token> Update.</caps:sentence>
                <caps:sentence sentenceid="5b0b240a3eac7d0e4ffed4a39c16b2c2" id="tgt5" class="tgtSentence"> Si no encuentra un código de error específico en esta tabla, vea <externalLink><linkText>Windows Update Agent Result Codes (Códigos de resultado del Agente de Windows Update)</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=221542</linkUri></externalLink>.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d22fbcfa8424b1e6c55b784be952198b" id="tgt6" class="tgtSentence">Código de error</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5c468f1abb510e3d7468a681ce4c976d" id="tgt7" class="tgtSentence">Nombre simbólico</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt8" class="tgtSentence">Más información</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2edaf6bb3942dd321d3e0b2e87701b53" id="tgt9" class="tgtSentence">0x00cf0001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8400f0a29b5b29bcd5d66e13ce83cbc3" id="tgt10" class="tgtSentence">OM_S_SERVICE_STOP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e93be8d4f50a280b859b0de963dbd89a" id="tgt11" class="tgtSentence">El agente se detuvo correctamente.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e3f503677517d2a5e81947c95a59fe8c" id="tgt12" class="tgtSentence">0x00cf0003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1424d2fb39683c6b0a4e40d84728751f" id="tgt13" class="tgtSentence">OM_S_UPDATE_ERROR</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bf0631fa4a8db095d3d04d9845d1bf82" id="tgt14" class="tgtSentence">La operación se completó correctamente, pero se produjeron errores al aplicar las actualizaciones.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f40d578758b6bd2952b188b3125f8fc6" id="tgt15" class="tgtSentence">0x00cf0004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6379c35a2cb0da9e8c0461f482b6c492" id="tgt16" class="tgtSentence">OM_S_MARKED_FOR_DISCONNECT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="81791c5986a6a9c52d8f965a102831bb" id="tgt17" class="tgtSentence">Se ha marcado una devolución de llamada para desconectarse más tarde porque la solicitud de desconectar la operación se produjo mientras se estaba ejecutando una devolución de llamada.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="fe60f8062c1f93b18f1d2c9b86b43b27" id="tgt18" class="tgtSentence">0x00cf0005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ca6a2e9276f87eab941b9578707d4f27" id="tgt19" class="tgtSentence">OM_S_REBOOT_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b2bc052edbe4d23bf2f13759845e21c3" id="tgt20" class="tgtSentence">El sistema debe reiniciarse para completar la instalación de la actualización.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8ed373f34fd18a3ccccb27445c324058" id="tgt21" class="tgtSentence">0x00cf0006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5761bb670e65ecc96b32b42c70541e45" id="tgt22" class="tgtSentence">OM_S_ALREADY_INSTALLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1091837d67b5bd708a9e6aa26ec44c16" id="tgt23" class="tgtSentence">La actualización que se va a instalar ya está instalada en el sistema.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="cb7f44d7c201d7cf21f2473372c52448" id="tgt24" class="tgtSentence">0x00cf0007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ce4564971bb736f94f41e768ec917b92" id="tgt25" class="tgtSentence">OM_S_ALREADY_UNINSTALLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b02803be1452ffcf5c4dd05425e90e64" id="tgt26" class="tgtSentence">La actualización que se va a quitar no está instalada en el sistema.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="17284cffb6238ebda9c187be02ca4515" id="tgt27" class="tgtSentence">0x00cf2015</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ee39260061611d0101896fa6b79125b6" id="tgt28" class="tgtSentence">OM_S_UH_INSTALLSTILLPENDING</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3cd6fcbfbca06fb9b40efdda04ff1d0b" id="tgt29" class="tgtSentence">La instalación de la actualización está en curso.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b9469ac2785f7738523e74fb2efc3202" id="tgt30" class="tgtSentence">0x80cf0001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="16752ba9575d889c838f4ade589218aa" id="tgt31" class="tgtSentence">OM_E_NO_SERVICE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="39847fe29c0baa1ad4a8588a60c9ba63" id="tgt32" class="tgtSentence">El agente no pudo proporcionar el servicio.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="65590b5adb76b74110b80607a9c6e3c4" id="tgt33" class="tgtSentence">0x80cf0002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3842cba4aab8b76331612ac354ba015a" id="tgt34" class="tgtSentence">OM_E_MAX_CAPACITY_REACHED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="834e635b55d66e05a7ebd9d0fbc115ee" id="tgt35" class="tgtSentence">Se superó la capacidad máxima del servicio.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6887efc736696f4f99974ff0701c7c61" id="tgt36" class="tgtSentence">0x80cf0003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fd3eeaef66f87cfdd0e4db04c15da0da" id="tgt37" class="tgtSentence">OM_E_UNKNOWN_ID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bd4db87c1ad2a5f48b6b4b2f6f7fd601" id="tgt38" class="tgtSentence">No se encuentra un identificador.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ddae0858ab766ad6dd2fcc5148c1971c" id="tgt39" class="tgtSentence">0x80cf0004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4bcaa47a194f754da47da67f5533d78f" id="tgt40" class="tgtSentence">OM_E_NOT_INITIALIZED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade9fcd9cff2404ad356b7f3ec805cca" id="tgt41" class="tgtSentence">No se pudo inicializar el objeto.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0992e17bf2320221c6c25adb01fdd61b" id="tgt42" class="tgtSentence">0x80cf0007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6c4aee954ca528fb5effa1025bdb92cb" id="tgt43" class="tgtSentence">OM_E_INVALIDINDEX</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bc31966992f1bb9daaa4ab87eeda8986" id="tgt44" class="tgtSentence">El índice de una colección no es válido.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b257565ab77142e94631bbc847569dfe" id="tgt45" class="tgtSentence">0x80cf0008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f6961575b7776d1073328ecd376119c8" id="tgt46" class="tgtSentence">OM_E_ITEMNOTFOUND</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="edebd2f9eae1553530908423923f17de" id="tgt47" class="tgtSentence">No se encontró la clave del elemento consultado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="39fe64c1cae60be8a32160166a266eca" id="tgt48" class="tgtSentence">0x80cf0009</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="12ba78da03f2dd23beb89f1c204a2cd2" id="tgt49" class="tgtSentence">OM_E_OPERATIONINPROGRESS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ad5005bcbd7de971a957bf3e965a9485" id="tgt50" class="tgtSentence">Había un conflicto con una operación en curso.</caps:sentence>
                        <caps:sentence sentenceid="58c001ef8bca8996ca8960d3b8733310" id="tgt51" class="tgtSentence"> Algunas operaciones (como, por ejemplo, varias instalaciones) no se pueden realizar simultáneamente.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="19009e3466ea80c77c5b9e0387fe2c41" id="tgt52" class="tgtSentence">0x80cf000B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c5df7daf5d221115fa2e34c2cd085950" id="tgt53" class="tgtSentence">OM_E_CALL_CANCELLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="98af44f5295adf50cf59ab666a968721" id="tgt54" class="tgtSentence">Se canceló la operación.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d45987a2e6db8bdf274c88fcb5eff991" id="tgt55" class="tgtSentence">0x80cf000C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="39ff2b0108ac01a77f2d2da21d3ed6d6" id="tgt56" class="tgtSentence">OM_E_NOOP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d9fa1277096be6dca0d84ddcd11c53d5" id="tgt57" class="tgtSentence">No era necesaria ninguna operación.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f8d204be299d2ab06e2d430860b8d3c2" id="tgt58" class="tgtSentence">0x80cf000D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0a342088d4680834a816a271a1502c88" id="tgt59" class="tgtSentence">OM_E_XML_MISSINGDATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="91ba02c03d5fb1a4b8c2f6165c513035" id="tgt60" class="tgtSentence">El agente no encontró la información necesaria en los datos XML de la actualización.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="141ebb6649d80cbdeed990c6c2e92b47" id="tgt61" class="tgtSentence">0x80cf000E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4be8cfc4a49e2639e86d598ed13f17b0" id="tgt62" class="tgtSentence">OM_E_XML_INVALID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="99df5d655481c9d49733235c8d568ff6" id="tgt63" class="tgtSentence">El agente encontró información no válida en los datos XML de la actualización.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="edab935aa650fac5a31eedbf057d1f8e" id="tgt64" class="tgtSentence">0x80cf000F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2e4aeed1354f466ed2a99ac49ef776eb" id="tgt65" class="tgtSentence">OM_E_CYCLE_DETECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5557ae4c10b6c20ae6b15e40e9ac310a" id="tgt66" class="tgtSentence">Se detectaron relaciones circulares de actualización en los metadatos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="64d47d41919545a78469c4a640cd44e1" id="tgt67" class="tgtSentence">0x80cf0010</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c1bd243b3e97a077472a55896d1ba0a8" id="tgt68" class="tgtSentence">OM_E_TOO_DEEP_RELATION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="64f79861000c6bcd23da08e43bcef94c" id="tgt69" class="tgtSentence">No se pudieron evaluar las relaciones de actualización porque estaban anidadas en un nivel demasiado profundo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f7c9071b6a572d422d6d8cb4f07b368b" id="tgt70" class="tgtSentence">0x80cf0011</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="855626a6d50d79a1be110bf01691b5d7" id="tgt71" class="tgtSentence">OM_E_INVALID_RELATIONSHIP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7092dcfd217793f050b6f67349a6d314" id="tgt72" class="tgtSentence">Se encontró una relación de actualización que no es válida.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="41e3fc2783906e4bf7aad3caa0c9d1ab" id="tgt73" class="tgtSentence">0x80cf0012</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b8597a3c06a932d9dcc086d081cb4e1f" id="tgt74" class="tgtSentence">OM_E_REG_VALUE_INVALID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="afae6f8fe45824370eb33d4d27fef755" id="tgt75" class="tgtSentence">Se leyó un valor del Registro que no es válido.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="96f61d2becbc7779be38471726d161ea" id="tgt76" class="tgtSentence">0x80cf0013</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e399421b92abd394f0981b4915669221" id="tgt77" class="tgtSentence">OM_E_DUPLICATE_ITEM</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="92a3e189369b4cc98c885baefcafa012" id="tgt78" class="tgtSentence">La operación intentó agregar un elemento duplicado a una lista.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="086799881948de2803fa984e625d05a1" id="tgt79" class="tgtSentence">0x80cf0014</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e5e94ad848d46e706e6f42c1b84b01da" id="tgt80" class="tgtSentence">OM_E_INVALID_INSTALL_REQUESTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cf18f437b274b18f491ccf6c0c1c63e3" id="tgt81" class="tgtSentence">El autor de la llamada no puede instalar las actualizaciones solicitadas.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2e1a6507f619c9dbcb6ec66c33fd4ae3" id="tgt82" class="tgtSentence">0x80cf0016</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4e3f02895cade252cdc4fb2175f3f712" id="tgt83" class="tgtSentence">OM_E_INSTALL_NOT_ALLOWED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="af2af0602f5a2c421cfbef5bb90c7224" id="tgt84" class="tgtSentence">La operación intentó instalar mientras se estaba realizando otra instalación o el sistema estaba pendiente de un reinicio obligatorio.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="10c1c1e4c14d55f4096f4153b7b706bd" id="tgt85" class="tgtSentence">0x80cf0017</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a229a21ba622bd09a7aaea27a25020bd" id="tgt86" class="tgtSentence">OM_E_NOT_APPLICABLE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="47219b06019dd3b8eb5627fa01c3d091" id="tgt87" class="tgtSentence">No se realizó la operación porque no hay ninguna actualización aplicable.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2d1fe75c2cd862c9f9bf56fa5130f1d6" id="tgt88" class="tgtSentence">0x80cf0018</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="932ffe814aabbb0771c10ef88fc5118d" id="tgt89" class="tgtSentence">OM_E_NO_USERTOKEN</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="69ea2ab22fad279c7a7452fcdf8601cd" id="tgt90" class="tgtSentence">Se produjo un error en la operación porque falta un token de usuario necesario.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ec20c045ec18244e9d8e59fcc1032e48" id="tgt91" class="tgtSentence">0x80cf0019</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="57e2231be1bfcb3d37ade67d95a3a1e5" id="tgt92" class="tgtSentence">OM_E_EXCLUSIVE_INSTALL_CONFLICT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a78b13f3a161374964d938be14ac934a" id="tgt93" class="tgtSentence">Una actualización exclusiva no se puede instalar simultáneamente con otras actualizaciones.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d061108530ffea16a200104c567fe188" id="tgt94" class="tgtSentence">0x80cf001A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c2449c9f43fd5651935f203b49293012" id="tgt95" class="tgtSentence">OM_E_POLICY_NOT_SET</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4fb24a777635c880d450666b2df7e860" id="tgt96" class="tgtSentence">No se estableció un valor de directiva.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="122fb860d4102cba59b3686642c6a589" id="tgt97" class="tgtSentence">0x80cf001D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5a8f83fd236e06aab1227ad6b53eaa9f" id="tgt98" class="tgtSentence">OM_E_INVALID_UPDATE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5b4108827d34e689ca1e62db3f5bdf06" id="tgt99" class="tgtSentence">Una actualización contiene metadatos que no son válidos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="cd3936c1dce0908fb0adaacabf007f0c" id="tgt100" class="tgtSentence">0x80cf001E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f334c2217ded5c39b2a8ffc3f69ee00a" id="tgt101" class="tgtSentence">OM_E_SERVICE_STOP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3df7b3a6a8c265d26af325f8ca54efe4" id="tgt102" class="tgtSentence">No se pudo completar la operación porque se estaba cerrando el servicio o el sistema.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2d421533e234fcfba312e9dfcfefe91e" id="tgt103" class="tgtSentence">0x80cf001F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="107a680e4ae415ccb6c50462a9ebf489" id="tgt104" class="tgtSentence">OM_E_NO_CONNECTION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e22a55706c16a67f40b64f0edfa16f4e" id="tgt105" class="tgtSentence">No se pudo completar la operación porque la conexión de red no estaba disponible.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="19eeaa3725d2728aefa187cab2cb598b" id="tgt106" class="tgtSentence">0x80cf0020</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8b55381890bdb4fde45f99e2423aa236" id="tgt107" class="tgtSentence">OM_E_NO_INTERACTIVE_USER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5e7d16ca0931bac95a4fed56b55bf296" id="tgt108" class="tgtSentence">No se puede completar la operación porque no hay ningún usuario interactivo conectado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4094fb8aed6789839ab9b917e2de644a" id="tgt109" class="tgtSentence">0x80cf0021</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f6ef4bb1e574e5361336726ca31fe804" id="tgt110" class="tgtSentence">OM_E_TIME_OUT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ae48bec3a648f9c9f0b42af24bf8f9f8" id="tgt111" class="tgtSentence">No se pudo completar la operación porque se agotó el tiempo de espera.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="31961f839dbdab9e246833fba43914eb" id="tgt112" class="tgtSentence">0x80cf0022</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d2fd9d8396c689ad0e8d14745a4fe583" id="tgt113" class="tgtSentence">OM_E_ALL_UPDATES_FAILED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9bdff714d06f0e5a8cad68aa1ebd3252" id="tgt114" class="tgtSentence">Error en la operación para todas las actualizaciones.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="07da727a98d39b49a7be83882fbf3fee" id="tgt115" class="tgtSentence">0x80cf0024</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="07087fa21c8c73011bb65a8c85ba12a5" id="tgt116" class="tgtSentence">OM_E_NO_UPDATE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ac73336ccba93cd11e03085d6a36a4e3" id="tgt117" class="tgtSentence">No hay actualizaciones.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="833fe93eed1ae5056f2e9012cfa0ea8b" id="tgt118" class="tgtSentence">0x80cf0025</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6c145da31693fea8ab26eb52d295c3e6" id="tgt119" class="tgtSentence">OM_E_USER_ACCESS_DISABLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="34a81f1081f6560f85adbd782b54ef17" id="tgt120" class="tgtSentence">La configuración de la directiva de grupo impidió el acceso a Windows Update.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="cd13eb5fd090cb7df722aa0e3379075c" id="tgt121" class="tgtSentence">0x80cf0026</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8f9b83f5d0fd56180d2e2ee1d6906635" id="tgt122" class="tgtSentence">OM_E_INVALID_UPDATE_TYPE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="86a9364be95b81ec06cc254fda96ff8f" id="tgt123" class="tgtSentence">El tipo de actualización no es válido.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1dddce007c8b4af949a0732d9bdaeadd" id="tgt124" class="tgtSentence">0x80cf0028</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1d966e4c9215d693604267c5a935a696" id="tgt125" class="tgtSentence">OM_E_UNINSTALL_NOT_ALLOWED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="172a39b7c3b086a0ede307581be7a51c" id="tgt126" class="tgtSentence">No se pudo desinstalar la actualización porque la solicitud no se originó en un servidor WSUS.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f45c7149f7c2a9e4ae33447cddd8e17e" id="tgt127" class="tgtSentence">0x80cf0029</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8de773e6c4651cde087c0324a4373f9f" id="tgt128" class="tgtSentence">OM_E_INVALID_PRODUCT_LICENSE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8f7bbecd1a66255ae233d4ac986411ad" id="tgt129" class="tgtSentence">Es posible que la búsqueda no haya encontrado algunas actualizaciones o puede haber una aplicación sin licencia en el sistema.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="fdb4f836fbde28af53941d0b09b0400a" id="tgt130" class="tgtSentence">0x80cf002C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="faf43d74c063134e82f6021831dcad4b" id="tgt131" class="tgtSentence">OM_E_BIN_SOURCE_ABSENT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5122d131852556c1a2431ac54451b9cb" id="tgt132" class="tgtSentence">No se puede instalar una actualización diferencial comprimida porque requería el origen.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7ddbf04ac37d86fe4997b3f1a3bff169" id="tgt133" class="tgtSentence">0x80cf002D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e0cda9bbff20a8e2098b23d835ce6861" id="tgt134" class="tgtSentence">OM_E_SOURCE_ABSENT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a93e0ea3e63614125482a04f22de6f3d" id="tgt135" class="tgtSentence">No se puede instalar una actualización de archivos completos porque requería el origen.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8fc35d6ff3c8f50aaa5dd55839629a83" id="tgt136" class="tgtSentence">0x80cf002E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="de2aed04ceb8e8c42d6904181ba605b0" id="tgt137" class="tgtSentence">OM_E_WU_DISABLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f196c8da0e628119d851547e442a77cc" id="tgt138" class="tgtSentence">No se permite el acceso a un servidor no administrado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ce590d785fbb32b55674e2acc8637c9f" id="tgt139" class="tgtSentence">0x80cf002F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="31f3c59fa5cd41e5f14b4dfc2d6a4e99" id="tgt140" class="tgtSentence">OM_E_CALL_CANCELLED_BY_POLICY</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="034235211b83dd86e87873ef321cf743" id="tgt141" class="tgtSentence">No se puede completar la operación porque estaba establecida la directiva <system>DisableWindowsUpdateAccess</system>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f5accc58cd5313d40327bb319caa3ab7" id="tgt142" class="tgtSentence">0x80cf0030</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cec98a413802868fb1b4f9baaf9b38d1" id="tgt143" class="tgtSentence">OM_E_INVALID_PROXY_SERVER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="da406d29c0a27e57247d2bf1f9cbfe8f" id="tgt144" class="tgtSentence">El formato de la lista de servidores proxy no es válido.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6cc57defdb468ee39c55af3c81a012da" id="tgt145" class="tgtSentence">0x80cf0031</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="27ebf7622c129b98515b42292d68e544" id="tgt146" class="tgtSentence">OM_E_INVALID_FILE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5d2c085a12f4c8fdb6710bcf4b9f8afc" id="tgt147" class="tgtSentence">El formato del archivo es incorrecto.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e57de7c5b684b516d8afaa4d63c13bad" id="tgt148" class="tgtSentence">0x80cf0032</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="dc3a014bfd7e89e5914d4dadc1324afc" id="tgt149" class="tgtSentence">OM_E_INVALID_CRITERIA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d68b4984ce555ce3293f5b6e780fb39e" id="tgt150" class="tgtSentence">La cadena de criterios de búsqueda no es válida.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7af3a78556b309bb1aaccd2f10ea362b" id="tgt151" class="tgtSentence">0x80cf0034</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a7548149c97f6ba70f285041ddf26bbf" id="tgt152" class="tgtSentence">OM_E_DOWNLOAD_FAILED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="642a18c5b00e680bce743b21efb77a6b" id="tgt153" class="tgtSentence">No se pudo descargar la actualización.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5ab36e3530686e4e460b0b21ee485550" id="tgt154" class="tgtSentence">0x80cf0035</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="04976bca0b5fb3d19a056ac34c5db7a5" id="tgt155" class="tgtSentence">OM_E_UPDATE_NOT_PROCESSED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cd7e2c34011087ac72cfc54412eec4a1" id="tgt156" class="tgtSentence">No se procesó la actualización.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9ffd0f158e587c45f44b8f08e0f23e9e" id="tgt157" class="tgtSentence">0x80cf0036</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bf8f3fae302aa9fce21102db4207ffc3" id="tgt158" class="tgtSentence">OM_E_INVALID_OPERATION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="acb2fbe411d1c9cc7f437a2e691c67ee" id="tgt159" class="tgtSentence">El estado actual del objeto no permitió la operación.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="efe7ddedb896ac6ee71a308d9f565a3c" id="tgt160" class="tgtSentence">0x80cf0037</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="519f3a016e953926ddc806469861abbd" id="tgt161" class="tgtSentence">OM_E_NOT_SUPPORTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3090f7b37677dd6090e980b1fd56b84b" id="tgt162" class="tgtSentence">No se admite la operación.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b03e1da73f2b24e02515d0453288aff3" id="tgt163" class="tgtSentence">0x80cf0038</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c91ac44045211b7369aa3b0a08868537" id="tgt164" class="tgtSentence">OM_E_WINHTTP_INVALID_FILE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2940c3400924e8a407829d6965a054f5" id="tgt165" class="tgtSentence">El archivo descargado tiene un tipo de contenido inesperado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b34db6b3c7ae1a363bfddd3ca277b757" id="tgt166" class="tgtSentence">0x80cf0039</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b28914aa4fbea45ac75d471365c245e4" id="tgt167" class="tgtSentence">OM_E_TOO_MANY_RESYNC</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3634203e750cc7aa8d4ae626f2bccfe3" id="tgt168" class="tgtSentence">El servidor envió al agente demasiadas solicitudes de resincronización.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5e21aa5b1618048c3ce8e6d21b160e77" id="tgt169" class="tgtSentence">0x80cf0043</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a3826680d01d8253433426c00e198327" id="tgt170" class="tgtSentence">OM_E_NO_UI_SUPPORT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="113f5a9a78691dbe1231df2543489182" id="tgt171" class="tgtSentence">No se admite la interfaz de usuario de WUA.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b8788ca56ff614b05cdba3b1872b2f60" id="tgt172" class="tgtSentence">0x80cf0044</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4a7ff75b109be0ca4a63b282c245eeb2" id="tgt173" class="tgtSentence">OM_E_PER_MACHINE_UPDATE_ACCESS_DENIED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ec2426ea32e7176bc2a8b87ec27671b6" id="tgt174" class="tgtSentence">Solo los administradores pueden realizar esta operación en actualizaciones por equipo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d2d533557d43fc02193b311890f5f894" id="tgt175" class="tgtSentence">0x80cf0045</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="703b00d20ae43e9ead91bdd477b7c19b" id="tgt176" class="tgtSentence">OM_E_UNSUPPORTED_SEARCHSCOPE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5be98e8dfefb996b9bb71f06ca82be5f" id="tgt177" class="tgtSentence">Se intentó realizar una búsqueda con un alcance no admitido.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f1794e2f6e61adef4e199d62dba06230" id="tgt178" class="tgtSentence">0x80cf0046</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a06aa510602924b5bbc86cc69287ef5e" id="tgt179" class="tgtSentence">OM_E_BAD_FILE_URL</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="33875e1b40c5af437c080d85b90e8c7f" id="tgt180" class="tgtSentence">La dirección URL no apunta a un archivo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a2c8e6f63ed234f6d9d77b5bb402602e" id="tgt181" class="tgtSentence">0x80cf0047</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="53e06bee4404d1fb1b96f793fb984ff1" id="tgt182" class="tgtSentence">OM_E_NOTSUPPORTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1231ba69c9cfa107331dd489fa02fc4b" id="tgt183" class="tgtSentence">No se admite la operación solicitada.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="715cc5c6dc7ca7b7bc8cd1a02630f43a" id="tgt184" class="tgtSentence">0x80cf0049</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="56f4fe1399a01c1e30d3fce75b326249" id="tgt185" class="tgtSentence">OM_E_OUTOFRANGE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="029eb31c4640e4386cc238b1532fa828" id="tgt186" class="tgtSentence">Los datos están fuera del intervalo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6978837eb0fdc286d0b2b45f790cc19b" id="tgt187" class="tgtSentence">0x80cf004A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b4e603cacbdd4cc79935c1dc9a33c86f" id="tgt188" class="tgtSentence">OM_E_INVALIDWUAVERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8fb9daa26d3e676fd13eeca453390d25" id="tgt189" class="tgtSentence">Los datos contienen una versión que no es válida.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="40ec66f2530e123b19c9d7d3eb96baec" id="tgt190" class="tgtSentence">0x80cf004B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="97a089d65fb08900d43ed1e93280228c" id="tgt191" class="tgtSentence">OM_E_SEARCH_COMPLETED_WITH_SOME_FAILURES</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2d19c03d74b28ab93829e00602ad06c6" id="tgt192" class="tgtSentence">Se completó la llamada de búsqueda, pero no se detectaron algunas de las actualizaciones.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="865d3bc50dd2d03b9731cbdcebed0703" id="tgt193" class="tgtSentence">0x80cf004C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6be5b9bbf80542f1ed7be6ef4a8267ad" id="tgt194" class="tgtSentence">OM_E_DOWNLOAD_COMPLETED_WITH_SOME_FAILURES</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7fb49b4fe5c595f7b9c13503b5aa011e" id="tgt195" class="tgtSentence">Se completó la llamada de descarga, pero no se descargaron algunas de las actualizaciones.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="da1c83ed80a295b5ac4298f5985c31a8" id="tgt196" class="tgtSentence">0x80cf004D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="eea61894a7de21ecf56d92e56754f4a4" id="tgt197" class="tgtSentence">OM_E_INSTALL_COMPLETED_WITH_SOME_FAILURES</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d0bfddbf4b3b9da43e73074228a86aa1" id="tgt198" class="tgtSentence">Se completó la llamada de instalación, pero no se instalaron algunas de las actualizaciones.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b365d955f9e741bbab8966369e466395" id="tgt199" class="tgtSentence">0x80cf004E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c020f5f7f0c55fd35aaac41ea16e6fb3" id="tgt200" class="tgtSentence">OM_E_WINUPDATE_CACHE_UNINITIALIZED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bbbde1f196a90806768207f1fa6ae656" id="tgt201" class="tgtSentence">La caché de Windows Update está vacía porque no se ha inicializado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c6d76dc338f2cf65149315cf61ee30ab" id="tgt202" class="tgtSentence">0x80cf0436</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6d8d344eafdfef467f8bd6474c843ef6" id="tgt203" class="tgtSentence">OM_E_PT_CATALOG_SYNC_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="660a689edf6bbb5d81e144533c6f0e6c" id="tgt204" class="tgtSentence">El servidor no admite búsquedas específicas de categorías.</caps:sentence>
                        <caps:sentence sentenceid="a3f4894ee0ab659dd20da9ced4a913fe" id="tgt205" class="tgtSentence"> En su lugar deben ejecutarse búsquedas de catálogo completo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5875863939f398559277e442505d8e23" id="tgt206" class="tgtSentence">0x80cf0437</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e062aaea5a2e78139876fad129774200" id="tgt207" class="tgtSentence">OM_E_PT_SECURITY_VERIFICATION_FAILURE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="520c2963b0df0fb1431797b04273acc6" id="tgt208" class="tgtSentence">Hubo un problema al autorizar con el servicio.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c5ccb13b3b36623b14bfd8900381990b" id="tgt209" class="tgtSentence">0x80cf0438</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="78bae6db399952f455afce4909ad4a60" id="tgt210" class="tgtSentence">OM_E_PT_ENDPOINT_UNREACHABLE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="dd89332de7190a870f3aa3c8af28439c" id="tgt211" class="tgtSentence">No hay conectividad de red o de ruta al extremo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9c9bb005f76bc98ea587a62654a18250" id="tgt212" class="tgtSentence">0x80cf0439</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="699e0842a19fda03497f85ecb751a353" id="tgt213" class="tgtSentence">OM_E_PT_INVALID_FORMAT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="34d115f611870d2ea4d0ddcc9425739f" id="tgt214" class="tgtSentence">Los datos recibidos no cumplen las expectativas del contrato de datos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e9b69889a93fcbaafeed5527ec74b621" id="tgt215" class="tgtSentence">0x80cf043A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e6403f53e471d50341c71e66b2fc52fe" id="tgt216" class="tgtSentence">OM_E_PT_INVALID_URL</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="caa90963ca8ba1a02e10ac1e9d88c29a" id="tgt217" class="tgtSentence">La dirección URL no es válida.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8b3de6188c460ab6dc34c399506a18b6" id="tgt218" class="tgtSentence">0x80cf043B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ec77d45a3b15a66a5a21bed144f6dd22" id="tgt219" class="tgtSentence">OM_E_PT_NWS_NOT_LOADED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8825bb6abe7a16e4de6f06190837432f" id="tgt220" class="tgtSentence">No se puede cargar el entorno de tiempo de ejecución de NWS.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a1c020c180102f79dd4f81e4a374ab06" id="tgt221" class="tgtSentence">0x80cf043C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="04ce1287b3ea82262a2f8a103699b64d" id="tgt222" class="tgtSentence">OM_E_PT_PROXY_AUTH_SCHEME_NOT_SUPPORTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ca266e42bf522c0cda7aea9004a57473" id="tgt223" class="tgtSentence">No se admite el esquema de autenticación de proxy.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b6687b101f09326a7138bcc940710a72" id="tgt224" class="tgtSentence">0x80cf043D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ae3adfdb576208297d837dcfb4763b03" id="tgt225" class="tgtSentence">OM_E_SERVICEPROP_NOTAVAIL</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cd1f7dba093912803ee13a99b1a409b6" id="tgt226" class="tgtSentence">La propiedad de servicio solicitada no está disponible.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9fd9e04ac4db01c2f2d4d86c639487de" id="tgt227" class="tgtSentence">0x80cf043E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="82f24791bddcbf9273bb0bb8d29285a6" id="tgt228" class="tgtSentence">OM_E_PT_ENDPOINT_REFRESH_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d1bb2f07ee3f54df45293a9b6afc10b1" id="tgt229" class="tgtSentence">El complemento de proveedor de extremo requiere una actualización en línea.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3edfc89867068dc755ffbeca2fb4b571" id="tgt230" class="tgtSentence">0x80cf043F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d3f1a991e2bee39e25a974585978da13" id="tgt231" class="tgtSentence">OM_E_PT_ENDPOINTURL_NOTAVAIL</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="43f3d6b19a988e731928420abf4cc644" id="tgt232" class="tgtSentence">No está disponible una dirección URL para el extremo de servicio solicitado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="de8d16927a7a0582b681b51abc2a20e2" id="tgt233" class="tgtSentence">0x80cf0440</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e74ee047108fc2b698125eb15e2d4b0b" id="tgt234" class="tgtSentence">OM_E_PT_ENDPOINT_DISCONNECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="740ce702edb77f60e62681472acc478c" id="tgt235" class="tgtSentence">Se terminó la conexión al extremo de servicio.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a0dda3bc858f9538ebd5305b2d37ffdf" id="tgt236" class="tgtSentence">0x80cf0441</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8441e3a4008530dd0b5bbfba59ea9043" id="tgt237" class="tgtSentence">OM_E_PT_INVALID_OPERATION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6809e1683ea3fa6d0dab56454b0f42b3" id="tgt238" class="tgtSentence">La operación no es válida porque el autor de llamadas de protocolo está en un estado inadecuado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="24781cb4b37323a65b5b068b4ffba450" id="tgt239" class="tgtSentence">0x80cf0FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fa09b56e479da099238a47b779dafe73" id="tgt240" class="tgtSentence">OM_E_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2938e786ffc5aa4457fcdb1a0c6f5b42" id="tgt241" class="tgtSentence">No se pudo completar la operación por razones que no se explican mediante otro código de error.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="71a37e0e36cb9cc274bf10838856fece" id="tgt242" class="tgtSentence">0x80cf1001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2c577f2de421a6420ca7f2268c322116" id="tgt243" class="tgtSentence">OM_E_MSI_WRONG_VERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1a65924239f13ee65097469948553171" id="tgt244" class="tgtSentence">La búsqueda no encontró algunas actualizaciones porque la versión de Windows Installer es anterior a la versión 3.1.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0ca958f1dfa258f36199799d9e1cf70e" id="tgt245" class="tgtSentence">0x80cf1002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4b017b877b8d0a00b48686d4788d89bf" id="tgt246" class="tgtSentence">OM_E_MSI_NOT_CONFIGURED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bc3149421bcc2f54ade3b1784cefbbbb" id="tgt247" class="tgtSentence">La búsqueda no encontró algunas actualizaciones porque aún no se ha configurado Windows Installer.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="689dcb2d2613c14beff7d13c5be0c242" id="tgt248" class="tgtSentence">0x80cf1003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="48b12bae885e3516857f998d30ff28e9" id="tgt249" class="tgtSentence">OM_E_MSP_DISABLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4bb66ef3f5bd33f4e34821f4b7c68b60" id="tgt250" class="tgtSentence">La búsqueda no encontró algunas actualizaciones porque la directiva deshabilitó la aplicación de revisiones de Windows Installer.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="583dd604272b77792d000cf7ead3594c" id="tgt251" class="tgtSentence">0x80cf1004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ada9046150bb323abf3001dff9408671" id="tgt252" class="tgtSentence">OM_E_MSI_WRONG_APP_CONTEXT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="896c101482fb8d391aad32828d013b67" id="tgt253" class="tgtSentence">No se pudo aplicar una actualización porque la aplicación se instala por usuario.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1b3e0a0a30c1f8fd0f4faffed9fd0801" id="tgt254" class="tgtSentence">0x80cf2000</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="32cff392f7d292bd6a7cda7092ec8fe7" id="tgt255" class="tgtSentence">OM_E_UH_REMOTEUNAVAILABLE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8bf71aee94b9a93468328da337032509" id="tgt256" class="tgtSentence">No se pudo completar una solicitud de controlador de actualización remota porque no hay ningún proceso remoto disponible.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ab3a874d0e55bd0019edc87aa30caf82" id="tgt257" class="tgtSentence">0x80cf2001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="48e49d89f9ce1eabee87dd42b00f063b" id="tgt258" class="tgtSentence">OM_E_UH_LOCALONLY</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e05277d0001aeda9032cfe74cd836708" id="tgt259" class="tgtSentence">No se pudo completar una solicitud de controlador de actualización remota porque el controlador es solo local.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="40770218ce25c13ac3796672bae39b58" id="tgt260" class="tgtSentence">0x80cf2003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="be02d1572e892f623d35108ee110fa82" id="tgt261" class="tgtSentence">OM_E_UH_REMOTEALREADYACTIVE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="738102842f667848ac0fdf2d6fb7c878" id="tgt262" class="tgtSentence">No se pudo crear un controlador de actualización remota porque ya existe uno.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a3e6c229bad129cd973d45eee538adc7" id="tgt263" class="tgtSentence">0x80cf2004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="37af215225f5436e2f8f9bbe381f2296" id="tgt264" class="tgtSentence">OM_E_UH_DOESNOTSUPPORTACTION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="74d20853ebf7eac445c84d61ed9584bd" id="tgt265" class="tgtSentence">No se pudo completar una solicitud al controlador para instalar (desinstalar) una actualización porque la actualización no es compatible con la instalación (desinstalación).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="04bb7d05d48b56dab7ef2406cf33d704" id="tgt266" class="tgtSentence">0x80cf2005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e89f5f7dbf0ce1bcbbd3599fa1bbb72c" id="tgt267" class="tgtSentence">OM_E_UH_WRONGHANDLER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c5ec31b2773df62d012f5575a85c8cf2" id="tgt268" class="tgtSentence">No se pudo completar una operación porque se especificó un controlador incorrecto.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ab9a86863f618236bbef742cb262f882" id="tgt269" class="tgtSentence">0x80cf2006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e53be2d0505368d6a8765dcb4a9880c" id="tgt270" class="tgtSentence">OM_E_UH_INVALIDMETADATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1ea8466f65bebe34d93ca08a8cf71928" id="tgt271" class="tgtSentence">No se pudo completar una operación de controlador porque la actualización contiene metadatos que no son válidos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c8f97c4d43ced91ba7bac5857885b787" id="tgt272" class="tgtSentence">0x80cf2007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a774fccfc77a8b18f11c739531a2d7be" id="tgt273" class="tgtSentence">OM_E_UH_INSTALLERHUNG</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2c728de02b247e52fa32d80843aae117" id="tgt274" class="tgtSentence">No se pudo completar una operación porque el instalador superó el límite de tiempo.</caps:sentence>
                        <caps:sentence sentenceid="357c90dfb9f5ae693d5e4d89c1e22291" id="tgt275" class="tgtSentence"> Compruebe si se aprobó la implementación de una actualización que requiere la interacción con el usuario.</caps:sentence>
                        <caps:sentence sentenceid="3ab656e96dd68ae17e5bd4cc4f990098" id="tgt276" class="tgtSentence"> En este caso deberá revisar los parámetros de instalación de la actualización para poder instalarla de forma silenciosa.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9d5618842333db22ee152fc1a9b82710" id="tgt277" class="tgtSentence">0x80cf2008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="63eb4f2e926b610441b890e5a2946147" id="tgt278" class="tgtSentence">OM_E_UH_OPERATIONCANCELLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9bc285699ad5819013b2969b8d249dcd" id="tgt279" class="tgtSentence">Se canceló una operación que el controlador de actualización estaba realizando.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5a80702d5664973a86ddab4bb28662e8" id="tgt280" class="tgtSentence">0x80cf2009</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="37906af5895eab7a3a55684637973f64" id="tgt281" class="tgtSentence">OM_E_UH_BADHANDLERXML</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="04f311f3b4bb5801d014adde21ac15af" id="tgt282" class="tgtSentence">No se pudo completar una operación porque los metadatos específicos del controlador no son válidos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="aae4f6a47aeeb7ead0571d441ae1599c" id="tgt283" class="tgtSentence">0x80cf200B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f49a9df53389df6bb6fdbc6e01c4eacc" id="tgt284" class="tgtSentence">OM_E_UH_INSTALLERFAILURE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="23f29ae12967ac50fdd323d1f80d8964" id="tgt285" class="tgtSentence">El instalador no pudo instalar (desinstalar) una o varias actualizaciones.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="cfa335964f00f2906f5f9f0f22540979" id="tgt286" class="tgtSentence">0x80cf200D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1904a22dd7dac28cc3e9deb423ba60f8" id="tgt287" class="tgtSentence">OM_E_UH_NEEDANOTHERDOWNLOAD</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fabb624dc4b35dc75cac99444944133b" id="tgt288" class="tgtSentence">El controlador de actualización no instaló la actualización porque debe volver a descargarse.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6f9945499dd02cf07a45acbb323891ea" id="tgt289" class="tgtSentence">0x80cf200E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="163d0f8aae4022841292cbdc273460a9" id="tgt290" class="tgtSentence">OM_E_UH_NOTIFYFAILURE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b745870b48d8b29fa342effa8d7fd3de" id="tgt291" class="tgtSentence">El controlador de actualización no pudo enviar la notificación de estado de la operación de instalación (desinstalación).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="67259fab34c6eb52b6e45b3bab74cf91" id="tgt292" class="tgtSentence">0x80cf2014</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b5fe622eb8a5fbd142e8b53ad2977a71" id="tgt293" class="tgtSentence">OM_E_UH_POSTREBOOTSTILLPENDING</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="329b49a6846bb264096b0bd95e5251bd" id="tgt294" class="tgtSentence">La operación posterior al reinicio para la actualización sigue en curso.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b65ef90004369150f44d84a97170fa62" id="tgt295" class="tgtSentence">0x80cf2015</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d0fb529a805b3f66ae1a8414e5bf71a4" id="tgt296" class="tgtSentence">OM_E_UH_POSTREBOOTRESULTUNKNOWN</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ae09a6546097eaa201ab2bf0cfeb4266" id="tgt297" class="tgtSentence">No se pudo determinar el resultado de la operación posterior al reinicio para la actualización.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b4190837a8a2a74978f1b2fc76f5b3d2" id="tgt298" class="tgtSentence">0x80cf2016</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="120fc1325ea44bd477fe2be4aade0979" id="tgt299" class="tgtSentence">OM_E_UH_POSTREBOOTUNEXPECTEDSTATE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="33b314e49ffb30cc688511caa8d3ba54" id="tgt300" class="tgtSentence">El estado de la actualización tras la operación posterior al reinicio se completó de manera inesperada.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="82654caaf5711e431deb0fb31491eae2" id="tgt301" class="tgtSentence">0x80cf2017</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="32a669800b3d0e8f749a73e7ad41b7f1" id="tgt302" class="tgtSentence">OM_E_UH_NEW_SERVICING_STACK_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fb18a07325b25ec975a30c3e30ba92a8" id="tgt303" class="tgtSentence">Hay que actualizar la pila de servicios del sistema operativo antes de poder descargar o instalar esta actualización.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6926ed4e4c88041d4ab8f87fcf4c5a3b" id="tgt304" class="tgtSentence">0x80cf2018</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ca06af5a55dfbd84c7fbf4a9cf5fb512" id="tgt305" class="tgtSentence">OM_E_UH_CALLED_BACK_FAILURE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="618897e12c7d450ff7ca81be4668549b" id="tgt306" class="tgtSentence">Un instalador de devolución de llamada devolvió una llamada con error.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b42b40751e37d40b8fdf9583f1d4c0d2" id="tgt307" class="tgtSentence">0x80cf2019</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b6fa8f0b9254c5988ed503d70fcede17" id="tgt308" class="tgtSentence">OM_E_UH_CUSTOMINSTALLER_INVALID_SIGNATURE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="57eaa87570e53f3535f26ab4a3281c2e" id="tgt309" class="tgtSentence">La firma de instalador personalizada no coincide con la firma requerida por la actualización.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="71dc368b6b6193bfc20d89e1e42b6aaa" id="tgt310" class="tgtSentence">0x80cf201A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="21371945e217f20ef2f25a41d38a50cc" id="tgt311" class="tgtSentence">OM_E_UH_UNSUPPORTED_INSTALLCONTEXT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1ac020e5058a841e7c002c4daf63301e" id="tgt312" class="tgtSentence">El instalador no admite la configuración de instalación.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="acea489ec32c56f665c474d164ae26dd" id="tgt313" class="tgtSentence">0x80cf201B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ff3521fa36ad24d50022ada05290d0df" id="tgt314" class="tgtSentence">OM_E_UH_INVALID_TARGETSESSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1f1e68b70a7e71e5074d1536bb2d9ae4" id="tgt315" class="tgtSentence">La sesión de destino para la instalación no es válida.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4ba389cfb748889b2a7427627b4124f1" id="tgt316" class="tgtSentence">0x80cf2FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="31379f1238331a184978b7f0a919bc76" id="tgt317" class="tgtSentence">OM_E_UH_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e02daae5a8cdf9be54bcd6001f3d9771" id="tgt318" class="tgtSentence">Un error de actualización de controlador no está cubierto por otro código de OM_E_UH_*.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="cbc19dc843dba805438d0107f3db6774" id="tgt319" class="tgtSentence">0x80cf3FFD</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ba8b475a172cdb3f216a7c25917739a5" id="tgt320" class="tgtSentence">OM_E_NON_UI_MODE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="47169ac746a9ac279ea6d21e94d4fc0b" id="tgt321" class="tgtSentence">No se puede mostrar la interfaz de usuario en modo de funcionamiento sin interfaz de usuario.</caps:sentence>
                        <caps:sentence sentenceid="06061a1b54f8bf209a244e16d99dc771" id="tgt322" class="tgtSentence"> Es posible que no estén instalados los módulos de interfaz de usuario del cliente de Windows Update.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="cfc906ad2ea0d333da60f79d6fd36b43" id="tgt323" class="tgtSentence">0x80cf3FFE</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c84e2b37b8de9c7dec07561b6dfe5564" id="tgt324" class="tgtSentence">OM_E_WUCLTUI_UNSUPPORTED_VERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="585edea0e17f5396357e6908044c548c" id="tgt325" class="tgtSentence">No se admite esta versión de las funciones exportadas de la interfaz de usuario del cliente de WU.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ee3bf1b39fc897a35bdae29b5f8b8ee2" id="tgt326" class="tgtSentence">0x80cf3FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c52566c9d14f62d6a14298d617678026" id="tgt327" class="tgtSentence">OM_E_AUCLIENT_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bdfb90caa53c79e6248843aa85701314" id="tgt328" class="tgtSentence">Se produjo un error de interfaz de usuario que no está cubierto por otro código de error de OM_E_AUCLIENT_*.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b5158480c45507d626473951d946d787" id="tgt329" class="tgtSentence">0x80cf4007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a3d2d6d3f5246721237c12eaec873ca4" id="tgt330" class="tgtSentence">OM_E_PT_SOAPCLIENT_SOAPFAULT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt331" class="tgtSentence">Igual que <system>SOAPCLIENT_SOAPFAULT</system>.</caps:sentence>
                        <caps:sentence sentenceid="57954726789984a106c9f95624ebbc2a" id="tgt332" class="tgtSentence"> Error del cliente SOAP a causa de un error de SOAP con código de error <system>OM_E_PT_SOAP_*</system>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="93b15b3b562f318fecfd06704bda7827" id="tgt333" class="tgtSentence">0x80cf4008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d2aec56d1524fdea2e5df675fa0980f2" id="tgt334" class="tgtSentence">OM_E_PT_SOAPCLIENT_PARSEFAULT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt335" class="tgtSentence">Igual que <system>SOAPCLIENT_PARSEFAULT_ERROR</system>.</caps:sentence>
                        <caps:sentence sentenceid="3eca68ae71ffa333b891e73469d582e1" id="tgt336" class="tgtSentence">  El cliente SOAP no pudo analizar un error de SOAP.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="971e8ec9dcb133f147fd08334259de9e" id="tgt337" class="tgtSentence">0x80cf400A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="368646f87ca814ce7492701310874cdb" id="tgt338" class="tgtSentence">OM_E_PT_SOAPCLIENT_PARSE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt339" class="tgtSentence">Igual que <system>SOAPCLIENT_PARSE_ERROR</system>.</caps:sentence>
                        <caps:sentence sentenceid="ec35e5651f5481eef4f789d816515ea8" id="tgt340" class="tgtSentence">  El cliente SOAP no pudo analizar la respuesta del servidor.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1fbbb9ed29c620331f554e90c97e1b69" id="tgt341" class="tgtSentence">0x80cf400B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a061dc09e1a7f50c01b22e182e57236b" id="tgt342" class="tgtSentence">OM_E_PT_SOAP_VERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt343" class="tgtSentence">Igual que <system>SOAP_E_VERSION_MISMATCH</system>.</caps:sentence>
                        <caps:sentence sentenceid="61858eaceb8f2033d77ba23b33aed344" id="tgt344" class="tgtSentence"> El cliente SOAP detectó un espacio de nombres no reconocible para la envoltura SOAP.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9c34fb201645a1e9592f2cf6cf16ae2a" id="tgt345" class="tgtSentence">0x80cf400C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fbdc32f8ffbb0a73ffec9aab3ae3023a" id="tgt346" class="tgtSentence">OM_E_PT_SOAP_MUST_UNDERSTAND</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt347" class="tgtSentence">Igual que <system>SOAP_E_MUST_UNDERSTAND</system>.</caps:sentence>
                        <caps:sentence sentenceid="cec98c968a94fa11fc021bcc63174530" id="tgt348" class="tgtSentence"> El cliente SOAP no pudo interpretar un encabezado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c434c6112b29626874595ddca420cbb5" id="tgt349" class="tgtSentence">0x80cf400D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b3114da3346472b9bb3794b844739196" id="tgt350" class="tgtSentence">OM_E_PT_SOAP_CLIENT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt351" class="tgtSentence">Igual que <system>SOAP_E_CLIENT</system>.</caps:sentence>
                        <caps:sentence sentenceid="8d970abea8099a5910bc305ab1ab148b" id="tgt352" class="tgtSentence"> El cliente SOAP detectó un formato incorrecto en el mensaje.</caps:sentence>
                        <caps:sentence sentenceid="006e69343f58a2e26e88f595712af085" id="tgt353" class="tgtSentence"> Corríjalo antes de volver a enviarlo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f15e40ac51151e68c6f7cfacaeb6f724" id="tgt354" class="tgtSentence">0x80cf400E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b89a2c92bcad764c52ad965ebde46ea4" id="tgt355" class="tgtSentence">OM_E_PT_SOAP_SERVER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt356" class="tgtSentence">Igual que <system>SOAP_E_SERVER</system>.</caps:sentence>
                        <caps:sentence sentenceid="245b597a79473aa3a9de84e25a0d410b" id="tgt357" class="tgtSentence"> No se pudo procesar el mensaje SOAP a causa de un error de servidor.</caps:sentence>
                        <caps:sentence sentenceid="e8471b91c25a5fab6e1d2e1227f80e4c" id="tgt358" class="tgtSentence"> Vuelva a enviarlo más tarde.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c396029b133a906d7429c45921623873" id="tgt359" class="tgtSentence">0x80cf4010</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3e337ed57b4be9509cadb213d107378b" id="tgt360" class="tgtSentence">OM_E_PT_EXCEEDED_MAX_SERVER_TRIPS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e2153f4df03c36616217009a2fc041e6" id="tgt361" class="tgtSentence">El número de viajes de ida y vuelta al servidor superó el límite máximo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c627f1e79658590e52aac292dc5eda57" id="tgt362" class="tgtSentence">0x80cf4012</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d0d1d1077187bd9ce952a63b73796678" id="tgt363" class="tgtSentence">OM_E_PT_DOUBLE_INITIALIZATION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7ef234ea6d40ae92abadc0629456deef" id="tgt364" class="tgtSentence">No se pudo inicializar porque el objeto ya estaba inicializado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e3b7a190cd8a3abe8f7cdb095140bd69" id="tgt365" class="tgtSentence">0x80cf4013</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="91038a402dae2afac68371eb5fb08a03" id="tgt366" class="tgtSentence">OM_E_PT_INVALID_COMPUTER_NAME</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9dbc7cf93c0da93f29621822439f2abb" id="tgt367" class="tgtSentence">No se puede determinar el nombre del equipo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b30e1aba7bb15d269bdf7c1aa2d92459" id="tgt368" class="tgtSentence">0x80cf4015</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="221f315f20092c2585edd06cde1ec7b5" id="tgt369" class="tgtSentence">OM_E_PT_REFRESH_CACHE_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d46d96572f96a61479fb4228e464ff49" id="tgt370" class="tgtSentence">La respuesta del servidor indica que se ha cambiado el servidor o que la cookie no es válida.</caps:sentence>
                        <caps:sentence sentenceid="afe11c8d6ca4b51e314c54d4f37bc09f" id="tgt371" class="tgtSentence"> Actualice la caché interna y reinténtelo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="79d1a2bb56373e3915b3efcaa9a25753" id="tgt372" class="tgtSentence">0x80cf4016</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8bb151cd36adb54564c6c7049b33cea4" id="tgt373" class="tgtSentence">OM_E_PT_HTTP_STATUS_BAD_REQUEST</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt374" class="tgtSentence">Igual que <system>HTTP status 400</system>.</caps:sentence>
                        <caps:sentence sentenceid="037ee9cb92b64d824d724fc768510617" id="tgt375" class="tgtSentence"> El servidor no pudo procesar la solicitud porque la sintaxis no es válida.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="14f9220495c6ad6c9bae3f3865d9068f" id="tgt376" class="tgtSentence">0x80cf4017</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cb9e864f2886763168d53ed8853bdac9" id="tgt377" class="tgtSentence">OM_E_PT_HTTP_STATUS_DENIED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt378" class="tgtSentence">Igual que <system>HTTP status 401</system>.</caps:sentence>
                        <caps:sentence sentenceid="2a0d8da431502f3de0a5b8503cc6d3a9" id="tgt379" class="tgtSentence"> El recurso solicitado requiere autenticación de usuarios.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1b4a1ccee69b64bfb3a1689d30748393" id="tgt380" class="tgtSentence">0x80cf4018</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5effceec98312577c0d8ba19c775a33e" id="tgt381" class="tgtSentence">OM_E_PT_HTTP_STATUS_FORBIDDEN</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt382" class="tgtSentence">Igual que <system>HTTP status 403</system>.</caps:sentence>
                        <caps:sentence sentenceid="1408a97216692bc170d63ac57dc5181e" id="tgt383" class="tgtSentence"> El servidor comprendió la solicitud pero la rechazó.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="39651a72f26ffbea91e68c0848da4715" id="tgt384" class="tgtSentence">0x80cf4019</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9990d8e36c4a20a0f8d64fdeb6a236ea" id="tgt385" class="tgtSentence">OM_E_PT_HTTP_STATUS_NOT_FOUND</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt386" class="tgtSentence">Igual que <system>HTTP status 404</system>.</caps:sentence>
                        <caps:sentence sentenceid="f0b144a4503194561628fee449a1dbbe" id="tgt387" class="tgtSentence"> El servidor no encuentra el URI (identificador uniforme de recursos) solicitado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="bc1eb8e89e8eb14ec4b288fd716de1a3" id="tgt388" class="tgtSentence">0x80cf401A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8ddcab5fd8f355a871b38c302b28495e" id="tgt389" class="tgtSentence">OM_E_PT_HTTP_STATUS_BAD_METHOD</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt390" class="tgtSentence">Igual que <system>HTTP status 405</system>.</caps:sentence>
                        <caps:sentence sentenceid="bc9405ba30294370988f6f1ff1d409fc" id="tgt391" class="tgtSentence"> El método HTTP no está permitido.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="852d4383d482c7da2d6000e816742040" id="tgt392" class="tgtSentence">0x80cf401B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="34585c001a8e82a1cc636d6070b77f4a" id="tgt393" class="tgtSentence">OM_E_PT_HTTP_STATUS_PROXY_AUTH_REQ</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt394" class="tgtSentence">Igual que <system>HTTP status 407</system>.</caps:sentence>
                        <caps:sentence sentenceid="0265b00eadb38d223d12fffd84c73dd6" id="tgt395" class="tgtSentence"> Se requiere autenticación de proxy.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="33495c225ffd0e2ae5ee76e5cf73ab1f" id="tgt396" class="tgtSentence">0x80cf401C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0f92ec9342f911cea6685f48cb6ac259" id="tgt397" class="tgtSentence">OM_E_PT_HTTP_STATUS_REQUEST_TIMEOUT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt398" class="tgtSentence">Igual que <system>HTTP status 408</system>.</caps:sentence>
                        <caps:sentence sentenceid="21928de2e2a9079c2dac16b58a818491" id="tgt399" class="tgtSentence"> El servidor agotó el tiempo de espera para la solicitud.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5d66f2d54abc41da0e05c0f01851f383" id="tgt400" class="tgtSentence">0x80cf401D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d961215df08354d3de94f85c609c58ed" id="tgt401" class="tgtSentence">OM_E_PT_HTTP_STATUS_CONFLICT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt402" class="tgtSentence">Igual que <system>HTTP status 409</system>.</caps:sentence>
                        <caps:sentence sentenceid="e6beafb88574e05faf81050358cf3108" id="tgt403" class="tgtSentence"> La solicitud no se completó debido a un conflicto con el estado actual del recurso.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="eba5f793173d3d9329ccfa9e45df2734" id="tgt404" class="tgtSentence">0x80cf401E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b7b615e93d6787b639fed7b05abf5b11" id="tgt405" class="tgtSentence">OM_E_PT_HTTP_STATUS_GONE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt406" class="tgtSentence">Igual que <system>HTTP status 410</system>.</caps:sentence>
                        <caps:sentence sentenceid="8be8c25fcda933720fc8e67e1323486d" id="tgt407" class="tgtSentence"> El recurso solicitado ya no está disponible en el servidor.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6ba81b9db41aac0c55bc2e5a7383f9fb" id="tgt408" class="tgtSentence">0x80cf401F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="584766b2952784276486bd9a20e39ba9" id="tgt409" class="tgtSentence">OM_E_PT_HTTP_STATUS_SERVER_ERROR</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt410" class="tgtSentence">Igual que <system>HTTP status 500</system>.</caps:sentence>
                        <caps:sentence sentenceid="2f59d04d618120c8618e90a6b3d90cd6" id="tgt411" class="tgtSentence"> No se pudo completar la solicitud a causa de un error interno en el servidor.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="72ed3486505f8a1079c2c2b476f2dcc2" id="tgt412" class="tgtSentence">0x80cf4020</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a109a516ce58e4c98f3213c75aaab541" id="tgt413" class="tgtSentence">OM_E_PT_HTTP_STATUS_NOT_SUPPORTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt414" class="tgtSentence">Igual que <system>HTTP status 500</system>.</caps:sentence>
                        <caps:sentence sentenceid="db246770d0076d98d863161dd0f4e7e2" id="tgt415" class="tgtSentence"> El servidor no admite la funcionalidad necesaria para completar la solicitud.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="64ad1c0fb744c3ea8c9e42702e064299" id="tgt416" class="tgtSentence">0x80cf4021</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ea9ebe9fd870587e0c533426b55daea5" id="tgt417" class="tgtSentence">OM_E_PT_HTTP_STATUS_BAD_GATEWAY</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt418" class="tgtSentence">Igual que <system>HTTP status 502</system>.</caps:sentence>
                        <caps:sentence sentenceid="e32e058fb046c8c73e88fc77cac4b5e6" id="tgt419" class="tgtSentence"> Mientras actuaba como puerta de enlace o proxy, el servidor recibió una respuesta no válida del servidor precedente al que tenía acceso mientras intentaba completar la solicitud.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d0860638a8dd493e674c175f1a442009" id="tgt420" class="tgtSentence">0x80cf4022</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3a45a1d696ab6c0914f7ed58836e4fdc" id="tgt421" class="tgtSentence">OM_E_PT_HTTP_STATUS_SERVICE_UNAVAIL</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt422" class="tgtSentence">Igual que <system>HTTP status 503</system>.</caps:sentence>
                        <caps:sentence sentenceid="bcf7b573a0624bc8554567cc9a5cbe66" id="tgt423" class="tgtSentence"> El servicio está sobrecargado temporalmente.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f7b4690a4c2d83d0d96e9ef31886d7e5" id="tgt424" class="tgtSentence">0x80cf4023</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="427270d39c0297dca33eddd2f9d93436" id="tgt425" class="tgtSentence">OM_E_PT_HTTP_STATUS_GATEWAY_TIMEOUT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt426" class="tgtSentence">Igual que <system>HTTP status 503</system>.</caps:sentence>
                        <caps:sentence sentenceid="5bf16242332df7582e959fc3c87de72a" id="tgt427" class="tgtSentence"> Se agotó el tiempo de espera de una puerta de enlace para la solicitud.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="fa748325343f81a8eea7b59b81a6a087" id="tgt428" class="tgtSentence">0x80cf4024</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d91837702d83f38dfe69dd5e620829bc" id="tgt429" class="tgtSentence">OM_E_PT_HTTP_STATUS_VERSION_NOT_SUP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt430" class="tgtSentence">Igual que <system>HTTP status 505</system>.</caps:sentence>
                        <caps:sentence sentenceid="858366e66ebe195ebc4e4dbce1c37232" id="tgt431" class="tgtSentence"> El servidor no admite la versión del protocolo HTTP que se usa para la solicitud.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="10470e14e5785f785caa3660b13bfbf8" id="tgt432" class="tgtSentence">0x80cf4025</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ab350ade3205c5e25bf9af4ad4607649" id="tgt433" class="tgtSentence">OM_E_PT_FILE_LOCATIONS_CHANGED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c7e5a0ed2af91a143e9bc1bf59b6d682" id="tgt434" class="tgtSentence">No se pudo completar la operación a causa de un cambio de ubicación de archivo.</caps:sentence>
                        <caps:sentence sentenceid="5f75abcb6be7b22091d6237f9a817b21" id="tgt435" class="tgtSentence"> Actualice el estado interno y repita el envío.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8ed06dc6480d77c48187bab2c2f582ad" id="tgt436" class="tgtSentence">0x80cf4027</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6765520aeed41a217943069c84632f11" id="tgt437" class="tgtSentence">OM_E_PT_NO_AUTH_PLUGINS_REQUESTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ddce7feb75dd96c364f13b4fd4959622" id="tgt438" class="tgtSentence">El servidor devolvió una lista de información de autenticación vacía.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="596c0dd917a702013b97b69271949f8e" id="tgt439" class="tgtSentence">0x80cf4028</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="25b059685849ef81be7f02e59b69e84b" id="tgt440" class="tgtSentence">OM_E_PT_NO_AUTH_COOKIES_CREATED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7d6d9e1a1d583473345703d3b2324ae7" id="tgt441" class="tgtSentence">El agente no pudo crear cookies de autenticación válidas.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="771609049ff20f6343a22edf23703461" id="tgt442" class="tgtSentence">0x80cf4029</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4e2943730d51dda1be9f46b89f2d35f8" id="tgt443" class="tgtSentence">OM_E_PT_INVALID_CONFIG_PROP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9ef4fbbd73af79433ab46ba539cf3cc9" id="tgt444" class="tgtSentence">Un valor de propiedad de configuración no es correcto.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="fec0693ea5d42247ff975c3628240620" id="tgt445" class="tgtSentence">0x80cf402A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2be2cb92178664afbf8b5814f1354918" id="tgt446" class="tgtSentence">OM_E_PT_CONFIG_PROP_MISSING</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c7c365dfa9d569cdb2d252ac96144ed1" id="tgt447" class="tgtSentence">Falta un valor de propiedad de configuración.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="10410602e498437a280de533d43a88b3" id="tgt448" class="tgtSentence">0x80cf402B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="118419b2d98c52f0f2e6e20d78860bd7" id="tgt449" class="tgtSentence">OM_E_PT_HTTP_STATUS_NOT_MAPPED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f1f74b2f3096babf4ee54143e5fbc869" id="tgt450" class="tgtSentence">No se pudo completar la solicitud HTTP y la razón no se corresponde con ninguno de los códigos de error <system>OM_E_PT_HTTP_*</system>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3ac6f7e03926a09f359b60d0da81be2d" id="tgt451" class="tgtSentence">0x80cf402C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f61da683cda3bbed5a7e8b1f763f1138" id="tgt452" class="tgtSentence">OM_E_PT_WINHTTP_NAME_NOT_RESOLVED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ade4f06976568675a2ab059925cd5898" id="tgt453" class="tgtSentence">Igual que <system>ERROR_WINHTTP_NAME_NOT_RESOLVED</system>.</caps:sentence>
                        <caps:sentence sentenceid="b58e26637913f60e625ea868706af923" id="tgt454" class="tgtSentence"> No se puede resolver el nombre del servidor proxy o el servidor de destino.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="42ad4a381a2754378ede46d0e5ffdc94" id="tgt455" class="tgtSentence">0x80cf402F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f0ea8679191945c6ffe627e612e6ee5e" id="tgt456" class="tgtSentence">OM_E_PT_ECP_SUCCEEDED_WITH_ERRORS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cdd162aa4df121126bc95a0c077063d9" id="tgt457" class="tgtSentence">Se completó el procesamiento del archivo .CAB externo con algunos errores.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0a246756b781870b563179c9dab64565" id="tgt458" class="tgtSentence">0x80cf4030</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="058dfb3afd87f8ba63a5b5743f474c0a" id="tgt459" class="tgtSentence">OM_E_PT_ECP_INIT_FAILED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6ff98485274545b4d7126b1c06d45040" id="tgt460" class="tgtSentence">No se completó la inicialización del procesador de archivos .CAB externos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a81cbdab92a2d4d1eb4589d88a487ee7" id="tgt461" class="tgtSentence">0x80cf4031</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e4499a51e97aa5f5a5349233e5ecfa96" id="tgt462" class="tgtSentence">OM_E_PT_ECP_INVALID_FILE_FORMAT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9f3a300503bfa7a1b4bfdbf39d240cb3" id="tgt463" class="tgtSentence">El formato de un archivo de metadatos no es válido.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="696d6e8522be71cb65e5e77e14351aa2" id="tgt464" class="tgtSentence">0x80cf4032</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4c47b619e4a28b2167477b77e717b75c" id="tgt465" class="tgtSentence">OM_E_PT_ECP_INVALID_METADATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d3ff9e6c209ffb8fe307b92bdaa92a75" id="tgt466" class="tgtSentence">El procesador de archivos .CAB externos detectó metadatos no válidos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="08974f6c77ee35c23b2cbe3eebfa36db" id="tgt467" class="tgtSentence">0x80cf4033</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2ae4a007477ef89fef1721588834fe57" id="tgt468" class="tgtSentence">OM_E_PT_ECP_FAILURE_TO_EXTRACT_DIGEST</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="231733cbfcfa7eb9b93e3495cc3fba21" id="tgt469" class="tgtSentence">No se pudo extraer el resumen de archivo de un archivo .CAB externo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="367871c734d4cecf3bb71e7a48a2ca24" id="tgt470" class="tgtSentence">0x80cf4034</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a5479baa917c101f4972ac6e3fcec188" id="tgt471" class="tgtSentence">OM_E_PT_ECP_FAILURE_TO_DECOMPRESS_CAB_FILE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="dcead936095d4f2abe6705785a332df7" id="tgt472" class="tgtSentence">No se pudo descomprimir un archivo .CAB externo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e267907d910a298452cabcc4714c8588" id="tgt473" class="tgtSentence">0x80cf4035</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0cb4258cd10e54785027e8a388b40141" id="tgt474" class="tgtSentence">OM_E_PT_ECP_FILE_LOCATION_ERROR</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3dbf417e6d0ce31e504e2d2fd624602a" id="tgt475" class="tgtSentence">El procesador de archivos. CAB externos no pudo obtener las ubicaciones de los archivos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ab8d8abe3c0a2ad77a97479b910610f8" id="tgt476" class="tgtSentence">0x80cf4FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1a750c0cbef3998931c3744fbb31ff2f" id="tgt477" class="tgtSentence">OM_E_PT_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="51ae79cd6cfd25f93a183db738a8288c" id="tgt478" class="tgtSentence">Se produjo un error de comunicación que no está cubierto por otro código de error <system>OM_E_PT_*</system>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e255b74a53506b1477506f3247cdfd38" id="tgt479" class="tgtSentence">0x80cf6001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="59c96cbd89cb6e1940500b3b508da768" id="tgt480" class="tgtSentence">OM_E_DM_URLNOTAVAILABLE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0adc372405fab28b55a723f8bd4b1a1b" id="tgt481" class="tgtSentence">No se pudo completar una operación del administrador de descargas porque el archivo solicitado no tiene una dirección URL.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="be87f9778bfc11965a5f0f328acf0cce" id="tgt482" class="tgtSentence">0x80cf6002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="164d7cc949e73b5de5d75dd129e3790e" id="tgt483" class="tgtSentence">OM_E_DM_INCORRECTFILEHASH</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="50e6344e878e868ff68b9fdc43284ea6" id="tgt484" class="tgtSentence">No se pudo completar una operación del administrador de descargas porque no se reconoció el resumen de archivo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9a043ae7780b27813a4f86982b57047d" id="tgt485" class="tgtSentence">0x80cf6003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4c8d6c19e55f52d39df826feabbb81c9" id="tgt486" class="tgtSentence">OM_E_DM_UNKNOWNALGORITHM</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cefa07969860969862527bb35f4b41b2" id="tgt487" class="tgtSentence">No se pudo completar una operación del administrador de descargas porque los metadatos del archivo solicitaron un algoritmo hash no reconocido.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="344e7535b1163b38b2e5b4769d88bbd9" id="tgt488" class="tgtSentence">0x80cf6005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fa113af3bcd52bfb992dd1db04c4f3a3" id="tgt489" class="tgtSentence">OM_E_DM_NONETWORK</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="de28413952423ae1138c0c72b7dd51a8" id="tgt490" class="tgtSentence">No se pudo completar la operación del administrador de descargas porque la conexión de red no estaba disponible.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3e7f9d42872acb077b632623b3f71ed3" id="tgt491" class="tgtSentence">0x80cf6007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="df968066d89887bb49091af50f2841b2" id="tgt492" class="tgtSentence">OM_E_DM_NOTDOWNLOADED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="197641aa4df092086dfe46ffdef99515" id="tgt493" class="tgtSentence">No se descargó la actualización.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e05efc0d17f1c843ca0eb43adb04eb05" id="tgt494" class="tgtSentence">0x80cf6008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9cd4d788fc64b8100dc4cd9946a168a8" id="tgt495" class="tgtSentence">OM_E_DM_FAILTOCONNECTTOBITS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cfac2f2b41c79396cc93bc635283e719" id="tgt496" class="tgtSentence">No se pudo completar una operación del administrador de descargas porque el administrador de descargas no se pudo conectar al Servicio de transferencia inteligente en segundo plano (BITS).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="eea75b9251e6c523aa3038558af5e9b6" id="tgt497" class="tgtSentence">0x80cf6009</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d34494d2c3d7dd57989b60620278a7c6" id="tgt498" class="tgtSentence">OM_E_DM_BITSTRANSFERERROR</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d823f51ae36a7493eb888792748432bd" id="tgt499" class="tgtSentence">No se pudo completar una operación del administrador de descargas a causa de un error no especificado de transferencia del Servicio de transferencia inteligente en segundo plano (BITS).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1446f63526556a9f37ee77997c26d080" id="tgt500" class="tgtSentence">0x80cf600a</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="915d786ebb6480138c76cbac5c70bd1f" id="tgt501" class="tgtSentence">OM_E_DM_DOWNLOADLOCATIONCHANGED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b74d1d47e348fad22b42ff5e1cb63432" id="tgt502" class="tgtSentence">Hay que reiniciar una descarga porque la ubicación de origen de la descarga ha cambiado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a6fd0fa1afcb9bcc615902e3757018c0" id="tgt503" class="tgtSentence">0x80cf600B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8723fa6fa8b684a8b436e6807fb0247b" id="tgt504" class="tgtSentence">OM_E_DM_CONTENTCHANGED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4c054fbb599b646121e707e8939f3a93" id="tgt505" class="tgtSentence">Debe reiniciar una descarga porque el contenido de actualización cambió en una nueva revisión.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3da6949083c0fef4786f0248b8ccee2a" id="tgt506" class="tgtSentence">0x80cf6FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="abad9a72ed5f9162307339defc7d5a5b" id="tgt507" class="tgtSentence">OM_E_DM_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a1465048ccaa9fc559daeb3b93fae7ac" id="tgt508" class="tgtSentence">Se produjo un error del administrador de descargas que no está cubierto por otro código de error <system>OM_E_DM_*</system>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ab9e2a73fe6a61a1d344b50dbee6d122" id="tgt509" class="tgtSentence">0x80cf7003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2ddc2c9bb0d0758f952783bca341a9c6" id="tgt510" class="tgtSentence">OM_E_INVALID_EVENT_PAYLOAD</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="702fd58620c064961cf117e00f2980c8" id="tgt511" class="tgtSentence">Se especificó una carga de eventos que no es válida.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d2c02032b046689d55083b90a52cdfc0" id="tgt512" class="tgtSentence">0x80cf7004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3ed5908ed4c5a72d53479fedc98f38c7" id="tgt513" class="tgtSentence">OM_E_INVALID_EVENT_PAYLOADSIZE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a0f14b03b365124268366858aea063f8" id="tgt514" class="tgtSentence">El tamaño de la carga de eventos enviado no es válido.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="54848141d3c3634a09dc0aa6865e1a26" id="tgt515" class="tgtSentence">0x80cf7005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="effeb4533180b08212b7cbaeb36848a5" id="tgt516" class="tgtSentence">OM_E_SERVICE_NOT_REGISTERED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b64cdcf3daec94519c345bdccf8bcda5" id="tgt517" class="tgtSentence">El servicio no está registrado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e96b1f6bd522c552868eabd368cb80eb" id="tgt518" class="tgtSentence">0x80cf8000</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4cc8f4335e0a987b4939d349d4b37fdd" id="tgt519" class="tgtSentence">OM_E_DS_SHUTDOWN</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="34aeb94ac9744b501ff50e85f2afe0fb" id="tgt520" class="tgtSentence">No se pudo completar una operación porque se está cerrando el agente.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8f996f475daded6ac219baf3a5a2ca15" id="tgt521" class="tgtSentence">0x80cf8001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d9cd08417322ae164581593612b5894f" id="tgt522" class="tgtSentence">OM_E_DS_INUSE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="70e8a3b837a0a36c5d03a184813d6681" id="tgt523" class="tgtSentence">No se pudo completar una operación porque se estaba utilizando el almacén de datos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4e85f8959cea35e10b9055b25574f397" id="tgt524" class="tgtSentence">0x80cf8002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="88a1ab6ef4d4be063e2393108770c069" id="tgt525" class="tgtSentence">OM_E_DS_INVALID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="53db3c092fc15d5dd7245674b88ad9b0" id="tgt526" class="tgtSentence">El estado actual y el esperado del almacén de datos no coinciden.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e8c29cbb5e7bf8e618b89989c5a509c4" id="tgt527" class="tgtSentence">0x80cf8003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c424eeb42195d8ddacbc9eb4ce99ba13" id="tgt528" class="tgtSentence">OM_E_DS_TABLEMISSING</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c64ca0ed70ce38c152d77aa282680be5" id="tgt529" class="tgtSentence">Falta una tabla en el almacén de datos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ed0a699e386859fe5dabd526a2e79dda" id="tgt530" class="tgtSentence">0x80cf8004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4ed27670aa16ebc398dca598192afda7" id="tgt531" class="tgtSentence">OM_E_DS_TABLEINCORRECT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3f6410fec06d067e2ba9308911baab06" id="tgt532" class="tgtSentence">El almacén de datos contiene una tabla con columnas inesperadas.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f3b15ae44d4a30c5eeb90b62af43c752" id="tgt533" class="tgtSentence">0x80cf8005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a3d155aa5cf097fb277c5b535ac43b1c" id="tgt534" class="tgtSentence">OM_E_DS_INVALIDTABLENAME</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="768b5d150abd790ff9264da84a01f0a1" id="tgt535" class="tgtSentence">No se puede abrir una tabla porque no está en el almacén de datos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0b22283cba41ecee147938e58e816f87" id="tgt536" class="tgtSentence">0x80cf8006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c811f2cb40ef216c25b3d9492f5d008f" id="tgt537" class="tgtSentence">OM_E_DS_BADVERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="64cff9535cb5fc2180aa3652994b2deb" id="tgt538" class="tgtSentence">La versión actual y la esperada del almacén de datos no coinciden.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="c77265533862e6d8a23d9be970841275" id="tgt539" class="tgtSentence">0x80cf8007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a5fccbf1796a9aa3fa8d8f31d130272c" id="tgt540" class="tgtSentence">OM_E_DS_NODATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f6345bab38dfd412260fdb1d8a23bfb5" id="tgt541" class="tgtSentence">La información solicitada no está en el almacén de datos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="735baff0cd884e823f82aaa8bfe7b11d" id="tgt542" class="tgtSentence">0x80cf8008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8742ee47e3f33c3bfc99396333a9cf0e" id="tgt543" class="tgtSentence">OM_E_DS_MISSINGDATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="753cada8d98743c1e101290c41da3968" id="tgt544" class="tgtSentence">Falta información necesaria en el almacén de datos o tiene un valor nulo en una columna de tabla que requiere un valor no nulo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="99584b91e36204dfe479d6c3936e7fdb" id="tgt545" class="tgtSentence">0x80cf8009</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="183b705c048c2ae103fbf591f6040dc6" id="tgt546" class="tgtSentence">OM_E_DS_MISSINGREF</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1902368bdc1a490b0b87769b73def807" id="tgt547" class="tgtSentence">Falta información necesaria en el almacén de datos o el almacén contiene una referencia a términos de licencia, un archivo, una propiedad localizada o una fila vinculada que faltan.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="42cd5cf61e84f3aeca061fdb249a5305" id="tgt548" class="tgtSentence">0x80cf800A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b425995389baa48b63f6cf241f1713c4" id="tgt549" class="tgtSentence">OM_E_DS_UNKNOWNHANDLER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7f3b69c17c38da5244ed86e450a9c012" id="tgt550" class="tgtSentence">No se procesó la actualización porque no se reconoció su controlador de actualización.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7d01db5d4fd4fc765ae0a66d09478cdd" id="tgt551" class="tgtSentence">0x80cf800B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a87e05190b21415f1a2f2c7898d19a56" id="tgt552" class="tgtSentence">OM_E_DS_CANTDELETE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1077a02bc49e3431ec43289ca435ca49" id="tgt553" class="tgtSentence">No se eliminó la actualización porque uno o más servicios aún hacen referencia a la misma.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="e113080dc5a087f91322679b4b355b7d" id="tgt554" class="tgtSentence">0x80cf800C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="87fc4f11b5c59f9ddf522f464d4c0c57" id="tgt555" class="tgtSentence">OM_E_DS_LOCKTIMEOUTEXPIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e538346aadc684ce6e970ea85c148b62" id="tgt556" class="tgtSentence">No se pudo bloquear la sección del almacén de datos en el tiempo asignado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="0e9dc0c4b117dff3247236fe9aa93c77" id="tgt557" class="tgtSentence">0x80cf800E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7eebaf3644de42718b82d5242ab0f71a" id="tgt558" class="tgtSentence">OM_E_DS_ROWEXISTS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9dea3a7476cd0bbbb767c056b513b5ff" id="tgt559" class="tgtSentence">No se agregó la fila porque una fila existente tiene la misma clave principal.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1f71b57479d5330ca33477e45b9a7c27" id="tgt560" class="tgtSentence">0x80cf800F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c61536df7e7038e1074873a504b238f6" id="tgt561" class="tgtSentence">OM_E_DS_STOREFILELOCKED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ef4bc327cdffc4fc08bfb1c6abe9951a" id="tgt562" class="tgtSentence">No se pudo inicializar el almacén de datos porque estaba bloqueado por otro proceso.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d4bb1478dca5c765928b14741f6686be" id="tgt563" class="tgtSentence">0x80cf8010</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4d606838a0c19655f68317d37a0f7438" id="tgt564" class="tgtSentence">OM_E_DS_CANNOTREGISTER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="09efdd35259509b11182d37c5045cda6" id="tgt565" class="tgtSentence">No se puede registrar el almacén de datos en el proceso actual mediante COM.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="b7c2f5cb7f19bdf482a106c2097975d0" id="tgt566" class="tgtSentence">0x80cf8011</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9f098b221d6587faa46c28590697ed5a" id="tgt567" class="tgtSentence">OM_E_DS_UNABLETOSTART</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f1b71dd51253a33c99c04020363e7e74" id="tgt568" class="tgtSentence">Una operación no pudo crear un objeto de almacén de datos en otro proceso.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="a806b8635e640f22392d34a902cc9e25" id="tgt569" class="tgtSentence">0x80cf8013</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="450b884e5f700f71af0884b09f624d37" id="tgt570" class="tgtSentence">OM_E_DS_DUPLICATEUPDATEID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b70aa4f331859f891b4850536d915489" id="tgt571" class="tgtSentence">El servidor envió la misma actualización al cliente con dos identificadores de revisión distintos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="793a9a127b802ef1e4199f40a47e1c77" id="tgt572" class="tgtSentence">0x80cf8014</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="adb4011d38c018187e849919f2386b79" id="tgt573" class="tgtSentence">OM_E_DS_UNKNOWNSERVICE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b9017cc5ccb336ca755ce5e15676a833" id="tgt574" class="tgtSentence">No se pudo completar una operación porque el servicio no está en el almacén de datos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9f37e205cac62a21f3d0318fef6e7be7" id="tgt575" class="tgtSentence">0x80cf8015</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d82ffedb9c59ccfdbf5a2a1946f5fee1" id="tgt576" class="tgtSentence">OM_E_DS_SERVICEEXPIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2e721b8f017d81913143c00f5387e2be" id="tgt577" class="tgtSentence">No se pudo completar una operación porque el registro del servicio ha expirado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="56b735db56bb0a242d207bbadcf7d6ca" id="tgt578" class="tgtSentence">0x80cf8016</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9238b65684ee499e452d57c45e31e639" id="tgt579" class="tgtSentence">OM_E_DS_DECLINENOTALLOWED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="89f5c28f302cc172af41adabb67d559c" id="tgt580" class="tgtSentence">Se rechazó una solicitud para ocultar una actualización porque es una actualización obligatoria o porque se implementó con una fecha límite.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="733e6ba90f4a082eda7c8764b253b4d1" id="tgt581" class="tgtSentence">0x80cf8017</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8e794c30e2d5950befe569fdb973e92e" id="tgt582" class="tgtSentence">OM_E_DS_TABLESESSIONMISMATCH</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ce7f91b1d413a0bf0ca0287b0b10eba5" id="tgt583" class="tgtSentence">No se cerró una tabla porque no está asociada a la sesión.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="814d8ff2c2b9468217e7c327fb3e09a9" id="tgt584" class="tgtSentence">0x80cf8018</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7aac63cb8ff1f91087b0bf754ddfd543" id="tgt585" class="tgtSentence">OM_E_DS_SESSIONLOCKMISMATCH</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ce7f91b1d413a0bf0ca0287b0b10eba5" id="tgt586" class="tgtSentence">No se cerró una tabla porque no está asociada a la sesión.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="61a92b5c599fd5a45565f81ab0adea98" id="tgt587" class="tgtSentence">0x80cf8019</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4c8194ea7f1f4a503011cddcadbd89ce" id="tgt588" class="tgtSentence">OM_E_DS_NEEDWINDOWSSERVICE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6f407ca9c44ddb30e5be4803eed57208" id="tgt589" class="tgtSentence">Se rechazó la solicitud de eliminar o anular el registro del servicio porque es un servicio integrado o porque Actualizaciones automáticas no puede cambiar a otro servicio.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4358e5d093a5ddd81469ab795e89214e" id="tgt590" class="tgtSentence">0x80cf801A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="22649071335704eb86a29ec510799d67" id="tgt591" class="tgtSentence">OM_E_DS_INVALIDOPERATION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="950d29c93992dc34a9a003cf19a0d06d" id="tgt592" class="tgtSentence">Se rechazó la solicitud porque no se permite la operación.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="259e0070406ec373c0ea08d7e8ab0622" id="tgt593" class="tgtSentence">0x80cf801B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ce463a4c2f505ca23508dea4f62b8131" id="tgt594" class="tgtSentence">OM_E_DS_SCHEMAMISMATCH</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0dcbaf4015fc6d005eea7137a818d8c6" id="tgt595" class="tgtSentence">El esquema del almacén de datos actual y el esquema de una tabla de un documento XML de copia de seguridad no coinciden.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6cec70eeb432ee16ca175c2c67c8dec1" id="tgt596" class="tgtSentence">0x80cf801C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9717343d4006039944335ee4591dbc52" id="tgt597" class="tgtSentence">OM_E_DS_RESETREQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8bf67d8c3f4c6418d565b0e72eb93686" id="tgt598" class="tgtSentence">El almacén de datos requiere un reinicio de sesión.</caps:sentence>
                        <caps:sentence sentenceid="719e92f9b1e22bb9c2c5d0f033cca2a3" id="tgt599" class="tgtSentence"> Libere la sesión y reinténtelo con una nueva sesión.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8de3d4e12a319d26fab35ef8e265050b" id="tgt600" class="tgtSentence">0x80cf801D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b3b41cbb91e340e7c3089271dd6fdfdf" id="tgt601" class="tgtSentence">OM_E_DS_IMPERSONATED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f1715a8a2af313166982f6ad10e7f0ac" id="tgt602" class="tgtSentence">No se pudo completar una operación de almacén de datos porque se solicitó con una identidad suplantada.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5191a73b9c5eb22ec412586024670980" id="tgt603" class="tgtSentence">0x80cf8FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d73bb035b55425a0d50db2004899e11f" id="tgt604" class="tgtSentence">OM_E_DS_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="59c4d8a7b6ef937e31e36e4b8c1f6253" id="tgt605" class="tgtSentence">Se produjo un error de almacén de datos que no está cubierto por otro código <system>OM_E_DS_*</system>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5f2860ce8b5b1c187b65ceb1807cd93e" id="tgt606" class="tgtSentence">0x80cfA000</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2d3e147be417f0f3fff2b1628c5fc61f" id="tgt607" class="tgtSentence">OM_E_AU_NOSERVICE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e06047221dd59f0b3a07cfb49c739cdd" id="tgt608" class="tgtSentence">Actualizaciones automáticas no pudo atender las solicitudes entrantes.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="df47d9cd24ccec1fd83d1883c9646819" id="tgt609" class="tgtSentence">0x80cfA004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e2e30a8f19f91f4069a196fa56d31414" id="tgt610" class="tgtSentence">OM_E_AU_PAUSED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b19043fadc142acb0a74163f984afa35" id="tgt611" class="tgtSentence">Actualizaciones automáticas no pudo procesar las solicitudes entrantes porque estaba en pausa.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="da69de49fb87d09fbbcb586ee7246551" id="tgt612" class="tgtSentence">0x80cfA005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="20c1b5b1452dc5da0051996536e2749a" id="tgt613" class="tgtSentence">OM_E_AU_NO_REGISTERED_SERVICE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="81b04ed7a6c5b268d2b64c689fd0bbea" id="tgt614" class="tgtSentence">No hay ningún servicio no administrado registrado en Actualizaciones automáticas.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="66688e06f061f44d2b5573f0ddc416f2" id="tgt615" class="tgtSentence">0x80cfA006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="182ba361d2d6bb4b19e399fe7f24a0f5" id="tgt616" class="tgtSentence">OM_E_AU_DETECT_SVCID_MISMATCH</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="98e2e1ca2d37e85bf5aa689fd491fb6c" id="tgt617" class="tgtSentence">Se cambió el servicio predeterminado registrado en Actualizaciones automáticas durante la búsqueda.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="6d9c88d57721f04c39ca63e3d5dd26a4" id="tgt618" class="tgtSentence">0x80cfA007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6ef2c8a8f5a38bb0f6ee612f8712386f" id="tgt619" class="tgtSentence">OM_E_AU_ALREADY_PROMPTING_FOR_REBOOT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b80f8625087599f29f593f0e84ca989e" id="tgt620" class="tgtSentence">Actualizaciones automáticas ya está pidiendo al usuario que reinicie el equipo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="047b938ecbf6e82b5d3bbfe1740cf0c5" id="tgt621" class="tgtSentence">0x80cfAFFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="888c4c08d0953cdd147677762399310d" id="tgt622" class="tgtSentence">OM_E_AU_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6e9d717f1ef17217674ba902f471a380" id="tgt623" class="tgtSentence">Se produjo un error de Actualizaciones automáticas que no está cubierto por otro código <system>OM_E_AU *</system>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7b46a04bee525bff6b4d0d5f21f4546c" id="tgt624" class="tgtSentence">0x80cfE001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e680ac7014cc168fad30d40ec6864de" id="tgt625" class="tgtSentence">OM_E_EE_UNKNOWN_EXPRESSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7c2974f547eac414944dc4d05d319777" id="tgt626" class="tgtSentence">No se pudo completar una operación del evaluador de expresiones porque no se reconoció una expresión.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2d5c4b50f44f229750308524603a76c2" id="tgt627" class="tgtSentence">0x80cfE002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f2e8eb96f8594214927b605ef2fa87a8" id="tgt628" class="tgtSentence">OM_E_EE_INVALID_EXPRESSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3645d1816e877e3d267974752b7008b2" id="tgt629" class="tgtSentence">No se pudo completar una operación del evaluador de expresiones porque una expresión no era válida.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4ea6d4116389be6223e533c62be4e1f8" id="tgt630" class="tgtSentence">0x80cfE003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="12cc70640b92e0d243985ff406c6a066" id="tgt631" class="tgtSentence">OM_E_EE_MISSING_METADATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="361fef3f37038ebd27c3fd15bfd0b5b1" id="tgt632" class="tgtSentence">No se pudo completar una operación del evaluador de expresiones porque una expresión contenía un número incorrecto de nodos de metadatos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="985351017589461f13cb6a83fcafa991" id="tgt633" class="tgtSentence">0x80cfE004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d9b60a4e283112aaaa9e45662d4a2ceb" id="tgt634" class="tgtSentence">OM_E_EE_INVALID_VERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="93ebf994af5c68c482d85a4341b4d38d" id="tgt635" class="tgtSentence">No se pudo completar una operación del evaluador de expresiones porque la versión de los datos de expresión serializados no es válida.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="62b880cff3bb7ab97dc6beea37145001" id="tgt636" class="tgtSentence">0x80cfE005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9a628d064cc4a8c79096b993132f938d" id="tgt637" class="tgtSentence">OM_E_EE_NOT_INITIALIZED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="02394a3dee002e1d3d8e85085c48d515" id="tgt638" class="tgtSentence">No se pudo inicializar el evaluador de expresiones.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8ee15c3a801f44de84a1591bee0d761c" id="tgt639" class="tgtSentence">0x80cfE006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="61c769bee16224db0eabd8c8dfda17bd" id="tgt640" class="tgtSentence">OM_E_EE_INVALID_ATTRIBUTEDATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="254f2642b2fb01081d8c3eb727ca1f08" id="tgt641" class="tgtSentence">No se pudo completar una operación del evaluador de expresiones porque un atributo no es válido.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f6e5c681de49b160b61c5a360401e263" id="tgt642" class="tgtSentence">0x80cfE007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b95fa365820d9151194a2764329c276b" id="tgt643" class="tgtSentence">OM_E_EE_CLUSTER_ERROR</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0e2304a2772aab2f3d0852718267985a" id="tgt644" class="tgtSentence">No se pudo completar una operación del evaluador de expresiones porque no se pudo determinar el estado del clúster del equipo.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="347dfe701aa353e497900cfbf359ec46" id="tgt645" class="tgtSentence">0x80cfEFFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="99f49d7040add6dc7754269732ce8ded" id="tgt646" class="tgtSentence">OM_E_EE_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e7e1cf246d8119bc3b4a0455149058a5" id="tgt647" class="tgtSentence">Se produjo un error del evaluador de expresiones que no está cubierto por otro código de error <system>OM_E_EE_*</system>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3650c7b13627a374a3f5d6cbce158421" id="tgt648" class="tgtSentence">0x80cfF001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3bb20ac851a004e3be91399194b89f47" id="tgt649" class="tgtSentence">OM_E_REPORTER_EVENTCACHECORRUPT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e63ef78e3c2e2b6cdaa834b884f9c927" id="tgt650" class="tgtSentence">El archivo de caché de eventos era defectuoso.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f4c7e5a1756db018af05bdb742055d15" id="tgt651" class="tgtSentence">0x80cfF002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8a546e3cd3f67f5318530f6bb31e8520" id="tgt652" class="tgtSentence">OM_E_REPORTER_EVENTNAMESPACEPARSEFAILED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f4efc8efdca77268df8bf6dfff0284e1" id="tgt653" class="tgtSentence">No se pudieron analizar los datos XML del descriptor del espacio de nombres de eventos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8e53923b243d37538b2d4fbb8c9415f9" id="tgt654" class="tgtSentence">0x80cfF003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="06400bd9fc9032111c759d35c3133b22" id="tgt655" class="tgtSentence">OM_E_INVALID_EVENT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="de72bd0246a5590bf3155bc0b82d15c4" id="tgt656" class="tgtSentence">Los datos XML del descriptor del espacio de nombres de eventos no son válidos.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="17dc618f78fe17806342c69a48cd91f0" id="tgt657" class="tgtSentence">0x80cfF004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f89055ae6e090d3b8caf2a537bdf3894" id="tgt658" class="tgtSentence">OM_E_SERVER_BUSY</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ac2fffae5c9e44d02758ae8a598f3ad0" id="tgt659" class="tgtSentence">El servidor rechazó un evento porque estaba demasiado ocupado.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7f963288a9e8bef8e3905cb821a9c8c3" id="tgt660" class="tgtSentence">0x80cfFFFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2f4dddd541cbc282c9aefbe993a2a023" id="tgt661" class="tgtSentence">OM_E_REPORTER_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1fa6f98ee80d31b60b32b600b3c0f254" id="tgt662" class="tgtSentence">Se produjo un error de informador que no está cubierto por otro código de error.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="863a44f564ff90a50603005b4c631714" id="tgt663" class="tgtSentence">0x80af0005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ce415798204e2bbf40d0a4520b7ebb9b" id="tgt664" class="tgtSentence">OMC_E_INSTALL_NOT_ALLOWED_REBOOT_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="368a33393513d1fbdc0d2b57f514bbf5" id="tgt665" class="tgtSentence">Se produjo un error en la instalación porque hay un reinicio obligatorio pendiente.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3fe909188db29d6590a6123effe59f40" id="tgt666" class="tgtSentence">0x80af0006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="78422399b0ceaa6627d58f7da1428d36" id="tgt667" class="tgtSentence">OMC_E_DOWNLOAD_CANCELLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e09d04ee32a4b46f19e5dba9497d034c" id="tgt668" class="tgtSentence">Se canceló la descarga.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para></para>
      </introduction>
      <section address="BKMK_Updates" expanded="true">
        <title>
          <caps:sentence id="src1" class="srcSentence">Troubleshooting software updates</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Use the information in this section to help you solve software update problems in <token>wit_firstref</token>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section expanded="true">
            <title>
              <caps:sentence id="src3" class="srcSentence">Software update error codes</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src4" class="srcSentence">The following table lists the <token>wit_firstref</token> Update Agent error codes.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> If you cannot find a specific error code in this table, see <externalLink><linkText>Windows Update Agent Result Codes</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=221542</linkUri></externalLink>.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src6" class="srcSentence">Error code</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src7" class="srcSentence">Symbolic name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src8" class="srcSentence">More information</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src9" class="srcSentence">0x00cf0001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src10" class="srcSentence">OM_S_SERVICE_STOP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src11" class="srcSentence">The agent was successfully stopped.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src12" class="srcSentence">0x00cf0003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src13" class="srcSentence">OM_S_UPDATE_ERROR</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">The operation was completed successfully, but errors occurred during the application of updates.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src15" class="srcSentence">0x00cf0004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src16" class="srcSentence">OM_S_MARKED_FOR_DISCONNECT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src17" class="srcSentence">A callback was marked to be disconnected later because the request to disconnect the operation occurred while a callback was running.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src18" class="srcSentence">0x00cf0005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src19" class="srcSentence">OM_S_REBOOT_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src20" class="srcSentence">The system must be restarted to complete the update installation.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src21" class="srcSentence">0x00cf0006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">OM_S_ALREADY_INSTALLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src23" class="srcSentence">The update to be installed is already installed on the system.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src24" class="srcSentence">0x00cf0007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src25" class="srcSentence">OM_S_ALREADY_UNINSTALLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src26" class="srcSentence">The update to be removed is not installed on the system.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src27" class="srcSentence">0x00cf2015</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src28" class="srcSentence">OM_S_UH_INSTALLSTILLPENDING</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src29" class="srcSentence">The update installation is in progress.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src30" class="srcSentence">0x80cf0001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src31" class="srcSentence">OM_E_NO_SERVICE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src32" class="srcSentence">The agent could not provide the service.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src33" class="srcSentence">0x80cf0002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">OM_E_MAX_CAPACITY_REACHED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">The maximum capacity of the service was exceeded.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src36" class="srcSentence">0x80cf0003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">OM_E_UNKNOWN_ID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">An ID cannot be found.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src39" class="srcSentence">0x80cf0004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">OM_E_NOT_INITIALIZED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src41" class="srcSentence">The object could not be initialized.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src42" class="srcSentence">0x80cf0007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">OM_E_INVALIDINDEX</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">The index to a collection is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src45" class="srcSentence">0x80cf0008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">OM_E_ITEMNOTFOUND</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src47" class="srcSentence">The key for the queried item could not be found.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src48" class="srcSentence">0x80cf0009</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">OM_E_OPERATIONINPROGRESS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">A conflicting operation was in progress.</caps:sentence>
                        <caps:sentence id="src51" class="srcSentence"> Some operations, like multiple installations cannot be performed simultaneously.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src52" class="srcSentence">0x80cf000B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">OM_E_CALL_CANCELLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">The operation was canceled.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src55" class="srcSentence">0x80cf000C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">OM_E_NOOP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src57" class="srcSentence">No operation was required.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src58" class="srcSentence">0x80cf000D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src59" class="srcSentence">OM_E_XML_MISSINGDATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src60" class="srcSentence">The agent could not find required information in the update's XML data.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src61" class="srcSentence">0x80cf000E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src62" class="srcSentence">OM_E_XML_INVALID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">The agent found information in the update's XML data that is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src64" class="srcSentence">0x80cf000F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src65" class="srcSentence">OM_E_CYCLE_DETECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">Circular update relationships were detected in the metadata.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src67" class="srcSentence">0x80cf0010</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">OM_E_TOO_DEEP_RELATION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">The update relationships were too deeply nested to evaluate.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src70" class="srcSentence">0x80cf0011</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">OM_E_INVALID_RELATIONSHIP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src72" class="srcSentence">An update relationship was found that is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src73" class="srcSentence">0x80cf0012</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">OM_E_REG_VALUE_INVALID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src75" class="srcSentence">A registry value was read that is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src76" class="srcSentence">0x80cf0013</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src77" class="srcSentence">OM_E_DUPLICATE_ITEM</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src78" class="srcSentence">The operation tried to add a duplicate item to a list.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src79" class="srcSentence">0x80cf0014</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">OM_E_INVALID_INSTALL_REQUESTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">The caller cannot install updates that were requested for installation.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src82" class="srcSentence">0x80cf0016</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src83" class="srcSentence">OM_E_INSTALL_NOT_ALLOWED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src84" class="srcSentence">The operation tried to install while another installation was in progress, or the system was pending a mandatory restart.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src85" class="srcSentence">0x80cf0017</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">OM_E_NOT_APPLICABLE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">The operation was not performed because there are no applicable updates.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src88" class="srcSentence">0x80cf0018</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">OM_E_NO_USERTOKEN</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">The operation failed because a required user token is missing.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src91" class="srcSentence">0x80cf0019</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">OM_E_EXCLUSIVE_INSTALL_CONFLICT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src93" class="srcSentence">An exclusive update cannot be simultaneously installed together with other updates.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src94" class="srcSentence">0x80cf001A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">OM_E_POLICY_NOT_SET</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src96" class="srcSentence">A policy value was not set.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src97" class="srcSentence">0x80cf001D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src98" class="srcSentence">OM_E_INVALID_UPDATE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src99" class="srcSentence">An update contains metadata that is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src100" class="srcSentence">0x80cf001E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">OM_E_SERVICE_STOP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">The operation could not be completed because the service or system was being shut down.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src103" class="srcSentence">0x80cf001F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src104" class="srcSentence">OM_E_NO_CONNECTION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src105" class="srcSentence">The operation could not be completed because the network connection was not available.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src106" class="srcSentence">0x80cf0020</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">OM_E_NO_INTERACTIVE_USER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src108" class="srcSentence">The operation could not be completed because there is no logged-on interactive user.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src109" class="srcSentence">0x80cf0021</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src110" class="srcSentence">OM_E_TIME_OUT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src111" class="srcSentence">The operation could not be completed because it timed out.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src112" class="srcSentence">0x80cf0022</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src113" class="srcSentence">OM_E_ALL_UPDATES_FAILED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src114" class="srcSentence">The operation failed for all the updates.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src115" class="srcSentence">0x80cf0024</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src116" class="srcSentence">OM_E_NO_UPDATE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src117" class="srcSentence">There are no updates.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src118" class="srcSentence">0x80cf0025</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">OM_E_USER_ACCESS_DISABLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">Group Policy settings prevented access to Windows Update.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src121" class="srcSentence">0x80cf0026</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src122" class="srcSentence">OM_E_INVALID_UPDATE_TYPE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src123" class="srcSentence">The update type is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src124" class="srcSentence">0x80cf0028</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src125" class="srcSentence">OM_E_UNINSTALL_NOT_ALLOWED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src126" class="srcSentence">The update could not be uninstalled because the request did not originate from a WSUS server.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src127" class="srcSentence">0x80cf0029</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src128" class="srcSentence">OM_E_INVALID_PRODUCT_LICENSE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src129" class="srcSentence">Search might have missed some updates, or there might be an unlicensed application on the system.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src130" class="srcSentence">0x80cf002C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src131" class="srcSentence">OM_E_BIN_SOURCE_ABSENT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src132" class="srcSentence">A delta-compressed update could not be installed because it required the source.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src133" class="srcSentence">0x80cf002D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src134" class="srcSentence">OM_E_SOURCE_ABSENT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src135" class="srcSentence">A full-file update could not be installed because it required the source.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src136" class="srcSentence">0x80cf002E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src137" class="srcSentence">OM_E_WU_DISABLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src138" class="srcSentence">Access to an unmanaged server is not allowed.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src139" class="srcSentence">0x80cf002F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src140" class="srcSentence">OM_E_CALL_CANCELLED_BY_POLICY</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src141" class="srcSentence">The operation could not be completed because the <system>DisableWindowsUpdateAccess</system> policy was set.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src142" class="srcSentence">0x80cf0030</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src143" class="srcSentence">OM_E_INVALID_PROXY_SERVER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src144" class="srcSentence">The proxy list format is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src145" class="srcSentence">0x80cf0031</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src146" class="srcSentence">OM_E_INVALID_FILE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src147" class="srcSentence">The file is in the wrong format.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src148" class="srcSentence">0x80cf0032</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src149" class="srcSentence">OM_E_INVALID_CRITERIA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src150" class="srcSentence">The search criteria string is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src151" class="srcSentence">0x80cf0034</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src152" class="srcSentence">OM_E_DOWNLOAD_FAILED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src153" class="srcSentence">The update failed to download.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src154" class="srcSentence">0x80cf0035</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src155" class="srcSentence">OM_E_UPDATE_NOT_PROCESSED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src156" class="srcSentence">The update was not processed.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src157" class="srcSentence">0x80cf0036</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src158" class="srcSentence">OM_E_INVALID_OPERATION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src159" class="srcSentence">The object's current state did not allow the operation.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src160" class="srcSentence">0x80cf0037</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src161" class="srcSentence">OM_E_NOT_SUPPORTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src162" class="srcSentence">The operation is not supported.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src163" class="srcSentence">0x80cf0038</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src164" class="srcSentence">OM_E_WINHTTP_INVALID_FILE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src165" class="srcSentence">The downloaded file has an unexpected content type.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src166" class="srcSentence">0x80cf0039</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src167" class="srcSentence">OM_E_TOO_MANY_RESYNC</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src168" class="srcSentence">The server asked the agent to resync too many times.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src169" class="srcSentence">0x80cf0043</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src170" class="srcSentence">OM_E_NO_UI_SUPPORT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src171" class="srcSentence">There is no support for WUA UI.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src172" class="srcSentence">0x80cf0044</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src173" class="srcSentence">OM_E_PER_MACHINE_UPDATE_ACCESS_DENIED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src174" class="srcSentence">Only administrators can perform this operation on per-computer updates.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src175" class="srcSentence">0x80cf0045</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src176" class="srcSentence">OM_E_UNSUPPORTED_SEARCHSCOPE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src177" class="srcSentence">A search was attempted with an unsupported scope.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src178" class="srcSentence">0x80cf0046</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src179" class="srcSentence">OM_E_BAD_FILE_URL</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src180" class="srcSentence">The URL does not point to a file.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src181" class="srcSentence">0x80cf0047</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src182" class="srcSentence">OM_E_NOTSUPPORTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src183" class="srcSentence">The requested operation is not supported.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src184" class="srcSentence">0x80cf0049</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src185" class="srcSentence">OM_E_OUTOFRANGE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src186" class="srcSentence">The data is out of range.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src187" class="srcSentence">0x80cf004A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src188" class="srcSentence">OM_E_INVALIDWUAVERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src189" class="srcSentence">The data contains a version that is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src190" class="srcSentence">0x80cf004B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src191" class="srcSentence">OM_E_SEARCH_COMPLETED_WITH_SOME_FAILURES</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src192" class="srcSentence">The search call was completed, but failed to detect some of the updates.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src193" class="srcSentence">0x80cf004C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src194" class="srcSentence">OM_E_DOWNLOAD_COMPLETED_WITH_SOME_FAILURES</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src195" class="srcSentence">The download call was completed, but failed to download some of the updates.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src196" class="srcSentence">0x80cf004D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src197" class="srcSentence">OM_E_INSTALL_COMPLETED_WITH_SOME_FAILURES</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src198" class="srcSentence">The install call was completed, but failed to install some of the updates.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src199" class="srcSentence">0x80cf004E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src200" class="srcSentence">OM_E_WINUPDATE_CACHE_UNINITIALIZED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src201" class="srcSentence">The Windows Update cache is empty because it has not been initialized.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src202" class="srcSentence">0x80cf0436</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src203" class="srcSentence">OM_E_PT_CATALOG_SYNC_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src204" class="srcSentence">The server does not support category-specific search.</caps:sentence>
                        <caps:sentence id="src205" class="srcSentence"> Full catalog search must be issued instead.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src206" class="srcSentence">0x80cf0437</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src207" class="srcSentence">OM_E_PT_SECURITY_VERIFICATION_FAILURE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src208" class="srcSentence">There was a problem authorizing with the service.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src209" class="srcSentence">0x80cf0438</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src210" class="srcSentence">OM_E_PT_ENDPOINT_UNREACHABLE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src211" class="srcSentence">There is no route or network connectivity to the endpoint.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src212" class="srcSentence">0x80cf0439</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src213" class="srcSentence">OM_E_PT_INVALID_FORMAT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src214" class="srcSentence">The data received does not meet the data contract expectations.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src215" class="srcSentence">0x80cf043A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src216" class="srcSentence">OM_E_PT_INVALID_URL</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src217" class="srcSentence">The URL is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src218" class="srcSentence">0x80cf043B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src219" class="srcSentence">OM_E_PT_NWS_NOT_LOADED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src220" class="srcSentence">The NWS runtime cannot be loaded.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src221" class="srcSentence">0x80cf043C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src222" class="srcSentence">OM_E_PT_PROXY_AUTH_SCHEME_NOT_SUPPORTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src223" class="srcSentence">The proxy authentication scheme is not supported.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src224" class="srcSentence">0x80cf043D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src225" class="srcSentence">OM_E_SERVICEPROP_NOTAVAIL</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src226" class="srcSentence">The requested service property is not available.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src227" class="srcSentence">0x80cf043E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src228" class="srcSentence">OM_E_PT_ENDPOINT_REFRESH_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src229" class="srcSentence">The endpoint provider plug-in requires an online refresh.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src230" class="srcSentence">0x80cf043F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src231" class="srcSentence">OM_E_PT_ENDPOINTURL_NOTAVAIL</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src232" class="srcSentence">A URL for the requested service endpoint is not available.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src233" class="srcSentence">0x80cf0440</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src234" class="srcSentence">OM_E_PT_ENDPOINT_DISCONNECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src235" class="srcSentence">The connection to the service endpoint terminated.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src236" class="srcSentence">0x80cf0441</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src237" class="srcSentence">OM_E_PT_INVALID_OPERATION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src238" class="srcSentence">The operation is not valid because protocol talker is in an inappropriate state.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src239" class="srcSentence">0x80cf0FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src240" class="srcSentence">OM_E_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src241" class="srcSentence">An operation failed because of reasons that are not explained by another error code.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src242" class="srcSentence">0x80cf1001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src243" class="srcSentence">OM_E_MSI_WRONG_VERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src244" class="srcSentence">Search might have missed some updates because the Windows Installer is an earlier version than version 3.1.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src245" class="srcSentence">0x80cf1002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src246" class="srcSentence">OM_E_MSI_NOT_CONFIGURED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src247" class="srcSentence">Search might have missed some updates because the Windows Installer is not configured.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src248" class="srcSentence">0x80cf1003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src249" class="srcSentence">OM_E_MSP_DISABLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src250" class="srcSentence">Search might have missed some updates because policy has disabled Windows Installer patching.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src251" class="srcSentence">0x80cf1004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src252" class="srcSentence">OM_E_MSI_WRONG_APP_CONTEXT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src253" class="srcSentence">An update could not be applied because the application is installed per user.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src254" class="srcSentence">0x80cf2000</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src255" class="srcSentence">OM_E_UH_REMOTEUNAVAILABLE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src256" class="srcSentence">A request for a remote update handler could not be completed because no remote process is available.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src257" class="srcSentence">0x80cf2001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src258" class="srcSentence">OM_E_UH_LOCALONLY</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src259" class="srcSentence">A request for a remote update handler could not be completed because the handler is local only.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src260" class="srcSentence">0x80cf2003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src261" class="srcSentence">OM_E_UH_REMOTEALREADYACTIVE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src262" class="srcSentence">A remote update handler could not be created because one already exists.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src263" class="srcSentence">0x80cf2004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src264" class="srcSentence">OM_E_UH_DOESNOTSUPPORTACTION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src265" class="srcSentence">A request for the handler to install (uninstall) an update could not be completed because the update does not support install (uninstall).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src266" class="srcSentence">0x80cf2005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src267" class="srcSentence">OM_E_UH_WRONGHANDLER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src268" class="srcSentence">An operation could not be completed because the wrong handler was specified.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src269" class="srcSentence">0x80cf2006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src270" class="srcSentence">OM_E_UH_INVALIDMETADATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src271" class="srcSentence">A handler operation could not be completed because the update contains metadata that is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src272" class="srcSentence">0x80cf2007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src273" class="srcSentence">OM_E_UH_INSTALLERHUNG</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src274" class="srcSentence">An operation could not be completed because the installer exceeded the time limit.</caps:sentence>
                        <caps:sentence id="src275" class="srcSentence"> Check whether an update that requires user interaction was approved for deployment.</caps:sentence>
                        <caps:sentence id="src276" class="srcSentence"> In this case, you must revise the update installation parameters so that it can install silently.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src277" class="srcSentence">0x80cf2008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src278" class="srcSentence">OM_E_UH_OPERATIONCANCELLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src279" class="srcSentence">An operation that was being performed by the update handler was canceled.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src280" class="srcSentence">0x80cf2009</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src281" class="srcSentence">OM_E_UH_BADHANDLERXML</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src282" class="srcSentence">An operation could not be completed because the handler-specific metadata is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src283" class="srcSentence">0x80cf200B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src284" class="srcSentence">OM_E_UH_INSTALLERFAILURE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src285" class="srcSentence">The installer failed to install (uninstall) one or more updates.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src286" class="srcSentence">0x80cf200D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src287" class="srcSentence">OM_E_UH_NEEDANOTHERDOWNLOAD</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src288" class="srcSentence">The update handler did not install the update because it must be downloaded again.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src289" class="srcSentence">0x80cf200E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src290" class="srcSentence">OM_E_UH_NOTIFYFAILURE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src291" class="srcSentence">The update handler failed to send notification of the status of the install (uninstall) operation.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src292" class="srcSentence">0x80cf2014</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src293" class="srcSentence">OM_E_UH_POSTREBOOTSTILLPENDING</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src294" class="srcSentence">The post-reboot operation for the update is still in progress.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src295" class="srcSentence">0x80cf2015</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src296" class="srcSentence">OM_E_UH_POSTREBOOTRESULTUNKNOWN</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src297" class="srcSentence">The result of the post-reboot operation for the update could not be determined.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src298" class="srcSentence">0x80cf2016</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src299" class="srcSentence">OM_E_UH_POSTREBOOTUNEXPECTEDSTATE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src300" class="srcSentence">The state of the update after its post-reboot operation was completed is unexpected.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src301" class="srcSentence">0x80cf2017</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src302" class="srcSentence">OM_E_UH_NEW_SERVICING_STACK_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src303" class="srcSentence">The operation system servicing stack must be updated before this update is downloaded or installed.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src304" class="srcSentence">0x80cf2018</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src305" class="srcSentence">OM_E_UH_CALLED_BACK_FAILURE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src306" class="srcSentence">A callback installer called back with an error.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src307" class="srcSentence">0x80cf2019</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src308" class="srcSentence">OM_E_UH_CUSTOMINSTALLER_INVALID_SIGNATURE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src309" class="srcSentence">The custom installer signature did not match the signature that the update requires.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src310" class="srcSentence">0x80cf201A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src311" class="srcSentence">OM_E_UH_UNSUPPORTED_INSTALLCONTEXT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src312" class="srcSentence">The installer does not support the installation configuration.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src313" class="srcSentence">0x80cf201B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src314" class="srcSentence">OM_E_UH_INVALID_TARGETSESSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src315" class="srcSentence">The targeted session for the installation is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src316" class="srcSentence">0x80cf2FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src317" class="srcSentence">OM_E_UH_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src318" class="srcSentence">An update handler error is not covered by another OM_E_UH_* code.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src319" class="srcSentence">0x80cf3FFD</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src320" class="srcSentence">OM_E_NON_UI_MODE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src321" class="srcSentence">Cannot show UI when in non-UI mode.</caps:sentence>
                        <caps:sentence id="src322" class="srcSentence"> Windows Update client UI modules might not be installed.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src323" class="srcSentence">0x80cf3FFE</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src324" class="srcSentence">OM_E_WUCLTUI_UNSUPPORTED_VERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src325" class="srcSentence">This version of WU client UI exported functions is not supported.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src326" class="srcSentence">0x80cf3FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src327" class="srcSentence">OM_E_AUCLIENT_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src328" class="srcSentence">A user interface error occurred that is not covered by another OM_E_AUCLIENT_* error code.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src329" class="srcSentence">0x80cf4007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src330" class="srcSentence">OM_E_PT_SOAPCLIENT_SOAPFAULT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src331" class="srcSentence">Same as <system>SOAPCLIENT_SOAPFAULT</system>.</caps:sentence>
                        <caps:sentence id="src332" class="srcSentence"> SOAP client failed because a SOAP fault of <system>OM_E_PT_SOAP_*</system> error code type occurred.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src333" class="srcSentence">0x80cf4008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src334" class="srcSentence">OM_E_PT_SOAPCLIENT_PARSEFAULT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src335" class="srcSentence">Same as <system>SOAPCLIENT_PARSEFAULT_ERROR</system>.</caps:sentence>
                        <caps:sentence id="src336" class="srcSentence">  SOAP client failed to parse a SOAP fault error.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src337" class="srcSentence">0x80cf400A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src338" class="srcSentence">OM_E_PT_SOAPCLIENT_PARSE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src339" class="srcSentence">Same as <system>SOAPCLIENT_PARSE_ERROR</system>.</caps:sentence>
                        <caps:sentence id="src340" class="srcSentence">  SOAP client failed to parse the response from the server.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src341" class="srcSentence">0x80cf400B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src342" class="srcSentence">OM_E_PT_SOAP_VERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src343" class="srcSentence">Same as <system>SOAP_E_VERSION_MISMATCH</system>.</caps:sentence>
                        <caps:sentence id="src344" class="srcSentence"> SOAP client found an unrecognizable namespace for the SOAP envelope.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src345" class="srcSentence">0x80cf400C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src346" class="srcSentence">OM_E_PT_SOAP_MUST_UNDERSTAND</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src347" class="srcSentence">Same as <system>SOAP_E_MUST_UNDERSTAND</system>.</caps:sentence>
                        <caps:sentence id="src348" class="srcSentence"> SOAP client could not interpret a header.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src349" class="srcSentence">0x80cf400D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src350" class="srcSentence">OM_E_PT_SOAP_CLIENT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src351" class="srcSentence">Same as <system>SOAP_E_CLIENT</system>.</caps:sentence>
                        <caps:sentence id="src352" class="srcSentence"> SOAP client found the message was malformed.</caps:sentence>
                        <caps:sentence id="src353" class="srcSentence"> Correct before resending.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src354" class="srcSentence">0x80cf400E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src355" class="srcSentence">OM_E_PT_SOAP_SERVER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src356" class="srcSentence">Same as <system>SOAP_E_SERVER</system>.</caps:sentence>
                        <caps:sentence id="src357" class="srcSentence"> The SOAP message could not be processed because of a server error.</caps:sentence>
                        <caps:sentence id="src358" class="srcSentence"> Resend later.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src359" class="srcSentence">0x80cf4010</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src360" class="srcSentence">OM_E_PT_EXCEEDED_MAX_SERVER_TRIPS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src361" class="srcSentence">The number of round trips to the server exceeded the maximum limit.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src362" class="srcSentence">0x80cf4012</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src363" class="srcSentence">OM_E_PT_DOUBLE_INITIALIZATION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src364" class="srcSentence">The initialization failed because the object was already initialized.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src365" class="srcSentence">0x80cf4013</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src366" class="srcSentence">OM_E_PT_INVALID_COMPUTER_NAME</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src367" class="srcSentence">The computer name could not be determined.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src368" class="srcSentence">0x80cf4015</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src369" class="srcSentence">OM_E_PT_REFRESH_CACHE_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src370" class="srcSentence">The reply from the server indicates that the server was changed or the cookie was invalid.</caps:sentence>
                        <caps:sentence id="src371" class="srcSentence"> Refresh the internal cache and retry.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src372" class="srcSentence">0x80cf4016</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src373" class="srcSentence">OM_E_PT_HTTP_STATUS_BAD_REQUEST</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src374" class="srcSentence">Same as <system>HTTP status 400</system>.</caps:sentence>
                        <caps:sentence id="src375" class="srcSentence"> The server could not process the request because the syntax is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src376" class="srcSentence">0x80cf4017</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src377" class="srcSentence">OM_E_PT_HTTP_STATUS_DENIED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src378" class="srcSentence">Same as <system>HTTP status 401</system>.</caps:sentence>
                        <caps:sentence id="src379" class="srcSentence"> The requested resource requires user authentication.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src380" class="srcSentence">0x80cf4018</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src381" class="srcSentence">OM_E_PT_HTTP_STATUS_FORBIDDEN</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src382" class="srcSentence">Same as <system>HTTP status 403</system>.</caps:sentence>
                        <caps:sentence id="src383" class="srcSentence"> The server understood the request, but declined to fulfill it.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src384" class="srcSentence">0x80cf4019</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src385" class="srcSentence">OM_E_PT_HTTP_STATUS_NOT_FOUND</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src386" class="srcSentence">Same as <system>HTTP status 404</system>.</caps:sentence>
                        <caps:sentence id="src387" class="srcSentence"> The server cannot find the requested URI (Uniform Resource Identifier).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src388" class="srcSentence">0x80cf401A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src389" class="srcSentence">OM_E_PT_HTTP_STATUS_BAD_METHOD</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src390" class="srcSentence">Same as <system>HTTP status 405</system>.</caps:sentence>
                        <caps:sentence id="src391" class="srcSentence"> The HTTP method is not allowed.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src392" class="srcSentence">0x80cf401B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src393" class="srcSentence">OM_E_PT_HTTP_STATUS_PROXY_AUTH_REQ</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src394" class="srcSentence">Same as <system>HTTP status 407</system>.</caps:sentence>
                        <caps:sentence id="src395" class="srcSentence"> Proxy authentication is required.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src396" class="srcSentence">0x80cf401C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src397" class="srcSentence">OM_E_PT_HTTP_STATUS_REQUEST_TIMEOUT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src398" class="srcSentence">Same as <system>HTTP status 408</system>.</caps:sentence>
                        <caps:sentence id="src399" class="srcSentence"> The server timed out waiting for the request.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src400" class="srcSentence">0x80cf401D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src401" class="srcSentence">OM_E_PT_HTTP_STATUS_CONFLICT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src402" class="srcSentence">Same as <system>HTTP status 409</system>.</caps:sentence>
                        <caps:sentence id="src403" class="srcSentence"> The request was not completed because of a conflict with the current state of the resource.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src404" class="srcSentence">0x80cf401E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src405" class="srcSentence">OM_E_PT_HTTP_STATUS_GONE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src406" class="srcSentence">Same as <system>HTTP status 410</system>.</caps:sentence>
                        <caps:sentence id="src407" class="srcSentence"> The requested resource is no longer available at the server.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src408" class="srcSentence">0x80cf401F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src409" class="srcSentence">OM_E_PT_HTTP_STATUS_SERVER_ERROR</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src410" class="srcSentence">Same as <system>HTTP status 500</system>.</caps:sentence>
                        <caps:sentence id="src411" class="srcSentence"> An error internal to the server prevented the request from being fulfilled.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src412" class="srcSentence">0x80cf4020</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src413" class="srcSentence">OM_E_PT_HTTP_STATUS_NOT_SUPPORTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src414" class="srcSentence">Same as <system>HTTP status 500</system>.</caps:sentence>
                        <caps:sentence id="src415" class="srcSentence"> The server does not support the functionality that is required to fulfill the request.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src416" class="srcSentence">0x80cf4021</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src417" class="srcSentence">OM_E_PT_HTTP_STATUS_BAD_GATEWAY</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src418" class="srcSentence">Same as <system>HTTP status 502</system>.</caps:sentence>
                        <caps:sentence id="src419" class="srcSentence"> The server, while acting as a gateway or proxy, received an invalid response from the upstream server that it accessed while trying to fulfill the request.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src420" class="srcSentence">0x80cf4022</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src421" class="srcSentence">OM_E_PT_HTTP_STATUS_SERVICE_UNAVAIL</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src422" class="srcSentence">Same as <system>HTTP status 503</system>.</caps:sentence>
                        <caps:sentence id="src423" class="srcSentence"> The service is temporarily overloaded.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src424" class="srcSentence">0x80cf4023</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src425" class="srcSentence">OM_E_PT_HTTP_STATUS_GATEWAY_TIMEOUT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src426" class="srcSentence">Same as <system>HTTP status 503</system>.</caps:sentence>
                        <caps:sentence id="src427" class="srcSentence"> The request was timed out waiting for a gateway.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src428" class="srcSentence">0x80cf4024</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src429" class="srcSentence">OM_E_PT_HTTP_STATUS_VERSION_NOT_SUP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src430" class="srcSentence">Same as <system>HTTP status 505</system>.</caps:sentence>
                        <caps:sentence id="src431" class="srcSentence"> The server does not support the HTTP protocol version that is used for the request.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src432" class="srcSentence">0x80cf4025</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src433" class="srcSentence">OM_E_PT_FILE_LOCATIONS_CHANGED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src434" class="srcSentence">The operation failed because of a changed file location.</caps:sentence>
                        <caps:sentence id="src435" class="srcSentence"> Refresh the internal state and resend.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src436" class="srcSentence">0x80cf4027</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src437" class="srcSentence">OM_E_PT_NO_AUTH_PLUGINS_REQUESTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src438" class="srcSentence">The server returned an empty authentication information list.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src439" class="srcSentence">0x80cf4028</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src440" class="srcSentence">OM_E_PT_NO_AUTH_COOKIES_CREATED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src441" class="srcSentence">The agent could not create any valid authentication cookies.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src442" class="srcSentence">0x80cf4029</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src443" class="srcSentence">OM_E_PT_INVALID_CONFIG_PROP</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src444" class="srcSentence">A configuration property value was wrong.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src445" class="srcSentence">0x80cf402A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src446" class="srcSentence">OM_E_PT_CONFIG_PROP_MISSING</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src447" class="srcSentence">A configuration property value was missing.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src448" class="srcSentence">0x80cf402B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src449" class="srcSentence">OM_E_PT_HTTP_STATUS_NOT_MAPPED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src450" class="srcSentence">The HTTP request could not be completed, and the reason did not correspond to any of the <system>OM_E_PT_HTTP_*</system> error codes.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src451" class="srcSentence">0x80cf402C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src452" class="srcSentence">OM_E_PT_WINHTTP_NAME_NOT_RESOLVED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src453" class="srcSentence">Same as <system>ERROR_WINHTTP_NAME_NOT_RESOLVED</system>.</caps:sentence>
                        <caps:sentence id="src454" class="srcSentence"> The proxy server or destination server name cannot be resolved.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src455" class="srcSentence">0x80cf402F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src456" class="srcSentence">OM_E_PT_ECP_SUCCEEDED_WITH_ERRORS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src457" class="srcSentence">The external .cab file processing was completed with some errors.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src458" class="srcSentence">0x80cf4030</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src459" class="srcSentence">OM_E_PT_ECP_INIT_FAILED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src460" class="srcSentence">The external .cab processor initialization was not completed.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src461" class="srcSentence">0x80cf4031</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src462" class="srcSentence">OM_E_PT_ECP_INVALID_FILE_FORMAT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src463" class="srcSentence">The format of a metadata file is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src464" class="srcSentence">0x80cf4032</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src465" class="srcSentence">OM_E_PT_ECP_INVALID_METADATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src466" class="srcSentence">The external cab processor found metadata that is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src467" class="srcSentence">0x80cf4033</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src468" class="srcSentence">OM_E_PT_ECP_FAILURE_TO_EXTRACT_DIGEST</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src469" class="srcSentence">The file digest could not be extracted from an external .cab file.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src470" class="srcSentence">0x80cf4034</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src471" class="srcSentence">OM_E_PT_ECP_FAILURE_TO_DECOMPRESS_CAB_FILE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src472" class="srcSentence">An external .cab file could not be decompressed.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src473" class="srcSentence">0x80cf4035</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src474" class="srcSentence">OM_E_PT_ECP_FILE_LOCATION_ERROR</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src475" class="srcSentence">The external cab processor could not get the file locations.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src476" class="srcSentence">0x80cf4FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src477" class="srcSentence">OM_E_PT_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src478" class="srcSentence">A communication error occurred that is not covered by another <system>OM_E_PT_*</system> error code.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src479" class="srcSentence">0x80cf6001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src480" class="srcSentence">OM_E_DM_URLNOTAVAILABLE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src481" class="srcSentence">A download manager operation could not be completed because the requested file does not have a URL.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src482" class="srcSentence">0x80cf6002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src483" class="srcSentence">OM_E_DM_INCORRECTFILEHASH</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src484" class="srcSentence">A download manager operation could not be completed because the file digest was not recognized.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src485" class="srcSentence">0x80cf6003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src486" class="srcSentence">OM_E_DM_UNKNOWNALGORITHM</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src487" class="srcSentence">A download manager operation could not be completed because the file metadata requested an unrecognized hash algorithm.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src488" class="srcSentence">0x80cf6005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src489" class="srcSentence">OM_E_DM_NONETWORK</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src490" class="srcSentence">A download manager operation could not be completed because the network connection was not available.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src491" class="srcSentence">0x80cf6007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src492" class="srcSentence">OM_E_DM_NOTDOWNLOADED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src493" class="srcSentence">The update has not been downloaded.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src494" class="srcSentence">0x80cf6008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src495" class="srcSentence">OM_E_DM_FAILTOCONNECTTOBITS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src496" class="srcSentence">A download manager operation failed because the download manager could not connect the Background Intelligent Transfer Service (BITS).</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src497" class="srcSentence">0x80cf6009</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src498" class="srcSentence">OM_E_DM_BITSTRANSFERERROR</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src499" class="srcSentence">A download manager operation failed because there was an unspecified Background Intelligent Transfer Service (BITS) transfer error.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src500" class="srcSentence">0x80cf600a</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src501" class="srcSentence">OM_E_DM_DOWNLOADLOCATIONCHANGED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src502" class="srcSentence">A download must be restarted because the download source location has changed.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src503" class="srcSentence">0x80cf600B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src504" class="srcSentence">OM_E_DM_CONTENTCHANGED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src505" class="srcSentence">A download must be restarted because the update content changed in a new revision.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src506" class="srcSentence">0x80cf6FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src507" class="srcSentence">OM_E_DM_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src508" class="srcSentence">A download manager error occurred that is not covered by another <system>OM_E_DM_*</system> error code.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src509" class="srcSentence">0x80cf7003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src510" class="srcSentence">OM_E_INVALID_EVENT_PAYLOAD</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src511" class="srcSentence">An event payload was specified that is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src512" class="srcSentence">0x80cf7004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src513" class="srcSentence">OM_E_INVALID_EVENT_PAYLOADSIZE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src514" class="srcSentence">The size of the event payload submitted is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src515" class="srcSentence">0x80cf7005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src516" class="srcSentence">OM_E_SERVICE_NOT_REGISTERED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src517" class="srcSentence">The service is not registered.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src518" class="srcSentence">0x80cf8000</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src519" class="srcSentence">OM_E_DS_SHUTDOWN</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src520" class="srcSentence">An operation failed because the agent is shutting down.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src521" class="srcSentence">0x80cf8001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src522" class="srcSentence">OM_E_DS_INUSE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src523" class="srcSentence">An operation failed because the data store was in use.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src524" class="srcSentence">0x80cf8002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src525" class="srcSentence">OM_E_DS_INVALID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src526" class="srcSentence">The current and expected states of the data store do not match.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src527" class="srcSentence">0x80cf8003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src528" class="srcSentence">OM_E_DS_TABLEMISSING</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src529" class="srcSentence">The data store is missing a table.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src530" class="srcSentence">0x80cf8004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src531" class="srcSentence">OM_E_DS_TABLEINCORRECT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src532" class="srcSentence">The data store contains a table that has unexpected columns.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src533" class="srcSentence">0x80cf8005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src534" class="srcSentence">OM_E_DS_INVALIDTABLENAME</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src535" class="srcSentence">A table could not be opened because the table is not in the data store.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src536" class="srcSentence">0x80cf8006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src537" class="srcSentence">OM_E_DS_BADVERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src538" class="srcSentence">The current and expected versions of the data store do not match.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src539" class="srcSentence">0x80cf8007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src540" class="srcSentence">OM_E_DS_NODATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src541" class="srcSentence">The information that is requested is not in the data store.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src542" class="srcSentence">0x80cf8008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src543" class="srcSentence">OM_E_DS_MISSINGDATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src544" class="srcSentence">The data store is missing required information or has a null in a table column that requires a non-null value.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src545" class="srcSentence">0x80cf8009</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src546" class="srcSentence">OM_E_DS_MISSINGREF</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src547" class="srcSentence">The data store is missing required information or has a reference to missing license terms, file, localized property, or linked row.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src548" class="srcSentence">0x80cf800A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src549" class="srcSentence">OM_E_DS_UNKNOWNHANDLER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src550" class="srcSentence">The update was not processed because its update handler was not recognized.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src551" class="srcSentence">0x80cf800B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src552" class="srcSentence">OM_E_DS_CANTDELETE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src553" class="srcSentence">The update was not deleted because it is still referenced by one or more services.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src554" class="srcSentence">0x80cf800C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src555" class="srcSentence">OM_E_DS_LOCKTIMEOUTEXPIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src556" class="srcSentence">The data store section could not be locked within the allotted time.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src557" class="srcSentence">0x80cf800E</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src558" class="srcSentence">OM_E_DS_ROWEXISTS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src559" class="srcSentence">The row was not added because an existing row has the same primary key.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src560" class="srcSentence">0x80cf800F</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src561" class="srcSentence">OM_E_DS_STOREFILELOCKED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src562" class="srcSentence">The data store could not be initialized because it was locked by another process.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src563" class="srcSentence">0x80cf8010</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src564" class="srcSentence">OM_E_DS_CANNOTREGISTER</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src565" class="srcSentence">The data store is not allowed to be registered with COM in the current process.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src566" class="srcSentence">0x80cf8011</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src567" class="srcSentence">OM_E_DS_UNABLETOSTART</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src568" class="srcSentence">An operation could not create a data store object in another process.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src569" class="srcSentence">0x80cf8013</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src570" class="srcSentence">OM_E_DS_DUPLICATEUPDATEID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src571" class="srcSentence">The server sent the same update to the client with two different revision IDs.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src572" class="srcSentence">0x80cf8014</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src573" class="srcSentence">OM_E_DS_UNKNOWNSERVICE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src574" class="srcSentence">An operation could not be completed because the service is not in the data store.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src575" class="srcSentence">0x80cf8015</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src576" class="srcSentence">OM_E_DS_SERVICEEXPIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src577" class="srcSentence">An operation could not be completed because the registration of the service has expired.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src578" class="srcSentence">0x80cf8016</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src579" class="srcSentence">OM_E_DS_DECLINENOTALLOWED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src580" class="srcSentence">A request to hide an update was declined because it is a mandatory update or because it was deployed with a deadline.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src581" class="srcSentence">0x80cf8017</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src582" class="srcSentence">OM_E_DS_TABLESESSIONMISMATCH</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src583" class="srcSentence">A table was not closed because it is not associated with the session.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src584" class="srcSentence">0x80cf8018</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src585" class="srcSentence">OM_E_DS_SESSIONLOCKMISMATCH</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src586" class="srcSentence">A table was not closed because it is not associated with the session.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src587" class="srcSentence">0x80cf8019</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src588" class="srcSentence">OM_E_DS_NEEDWINDOWSSERVICE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src589" class="srcSentence">The request to remove or unregister the service was declined because it is a built-in service or because Automatic Updates cannot fall back to another service.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src590" class="srcSentence">0x80cf801A</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src591" class="srcSentence">OM_E_DS_INVALIDOPERATION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src592" class="srcSentence">The request was declined because the operation is not allowed.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src593" class="srcSentence">0x80cf801B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src594" class="srcSentence">OM_E_DS_SCHEMAMISMATCH</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src595" class="srcSentence">The schema of the current data store and the schema of a table in a backup XML document do not match.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src596" class="srcSentence">0x80cf801C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src597" class="srcSentence">OM_E_DS_RESETREQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src598" class="srcSentence">The data store requires a session reset.</caps:sentence>
                        <caps:sentence id="src599" class="srcSentence"> Release the session and retry with a new session.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src600" class="srcSentence">0x80cf801D</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src601" class="srcSentence">OM_E_DS_IMPERSONATED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src602" class="srcSentence">A data store operation could not be completed because it was requested with an impersonated identity.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src603" class="srcSentence">0x80cf8FFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src604" class="srcSentence">OM_E_DS_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src605" class="srcSentence">A data store error occurred that is not covered by another <system>OM_E_DS_*</system> code.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src606" class="srcSentence">0x80cfA000</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src607" class="srcSentence">OM_E_AU_NOSERVICE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src608" class="srcSentence">Automatic Updates could not service incoming requests.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src609" class="srcSentence">0x80cfA004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src610" class="srcSentence">OM_E_AU_PAUSED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src611" class="srcSentence">Automatic Updates could not process incoming requests because it was paused.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src612" class="srcSentence">0x80cfA005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src613" class="srcSentence">OM_E_AU_NO_REGISTERED_SERVICE</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src614" class="srcSentence">No unmanaged service is registered with Automatic Updates.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src615" class="srcSentence">0x80cfA006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src616" class="srcSentence">OM_E_AU_DETECT_SVCID_MISMATCH</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src617" class="srcSentence">The default service registered with Automatic Updates changed during the search.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src618" class="srcSentence">0x80cfA007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src619" class="srcSentence">OM_E_AU_ALREADY_PROMPTING_FOR_REBOOT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src620" class="srcSentence">Automatic Updates is already prompting the user to restart.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src621" class="srcSentence">0x80cfAFFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src622" class="srcSentence">OM_E_AU_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src623" class="srcSentence">An Automatic Updates error occurred that is not covered by another <system>OM_E_AU *</system> code.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src624" class="srcSentence">0x80cfE001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src625" class="srcSentence">OM_E_EE_UNKNOWN_EXPRESSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src626" class="srcSentence">An expression evaluator operation could not be completed because an expression was not recognized.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src627" class="srcSentence">0x80cfE002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src628" class="srcSentence">OM_E_EE_INVALID_EXPRESSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src629" class="srcSentence">An expression evaluator operation could not be completed because an expression was not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src630" class="srcSentence">0x80cfE003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src631" class="srcSentence">OM_E_EE_MISSING_METADATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src632" class="srcSentence">An expression evaluator operation could not be completed because an expression contains an incorrect number of metadata nodes.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src633" class="srcSentence">0x80cfE004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src634" class="srcSentence">OM_E_EE_INVALID_VERSION</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src635" class="srcSentence">An expression evaluator operation could not be completed because the version of the serialized expression data is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src636" class="srcSentence">0x80cfE005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src637" class="srcSentence">OM_E_EE_NOT_INITIALIZED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src638" class="srcSentence">The expression evaluator could not be initialized.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src639" class="srcSentence">0x80cfE006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src640" class="srcSentence">OM_E_EE_INVALID_ATTRIBUTEDATA</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src641" class="srcSentence">An expression evaluator operation could not be completed because an attribute is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src642" class="srcSentence">0x80cfE007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src643" class="srcSentence">OM_E_EE_CLUSTER_ERROR</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src644" class="srcSentence">An expression evaluator operation could not be completed because the cluster state of the computer could not be determined.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src645" class="srcSentence">0x80cfEFFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src646" class="srcSentence">OM_E_EE_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src647" class="srcSentence">An expression evaluator error occurred that is not covered by another <system>OM_E_EE_*</system> error code.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src648" class="srcSentence">0x80cfF001</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src649" class="srcSentence">OM_E_REPORTER_EVENTCACHECORRUPT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src650" class="srcSentence">The event cache file was defective.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src651" class="srcSentence">0x80cfF002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src652" class="srcSentence">OM_E_REPORTER_EVENTNAMESPACEPARSEFAILED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src653" class="srcSentence">The XML in the event namespace descriptor could not be parsed.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src654" class="srcSentence">0x80cfF003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src655" class="srcSentence">OM_E_INVALID_EVENT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src656" class="srcSentence">The XML in the event namespace descriptor is not valid.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src657" class="srcSentence">0x80cfF004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src658" class="srcSentence">OM_E_SERVER_BUSY</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src659" class="srcSentence">The server rejected an event because the server was too busy.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src660" class="srcSentence">0x80cfFFFF</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src661" class="srcSentence">OM_E_REPORTER_UNEXPECTED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src662" class="srcSentence">A reporter error occurred that is not covered by another error code.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src663" class="srcSentence">0x80af0005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src664" class="srcSentence">OMC_E_INSTALL_NOT_ALLOWED_REBOOT_REQUIRED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src665" class="srcSentence">Installation failed because there is a pending mandatory reboot.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src666" class="srcSentence">0x80af0006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src667" class="srcSentence">OMC_E_DOWNLOAD_CANCELLED</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src668" class="srcSentence">The download was canceled.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>