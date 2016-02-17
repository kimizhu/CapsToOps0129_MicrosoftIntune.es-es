---
title: Administrar acceso al correo electr&#243;nico con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 09c82f5d-531c-474d-add6-784c83f96d93
---
# Administrar acceso al correo electr&#243;nico con Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt1" class="tgtSentence">Utilice las <ui>directivas de acceso condicional</ui> de <token>wit_firstref</token> para Exchange con la finalidad de administrar el acceso al correo electrónico de Exchange según las condiciones que especifique.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e2b471ebfc85793087242cfac12ce285" id="tgt2" class="tgtSentence">Puede administrar el acceso a:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="d34d6a431b44f8a40097dc9dce45b8e0" id="tgt3" class="tgtSentence">Microsoft Exchange local</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="048c4e2207eb069e0567ae88fd17dd68" id="tgt4" class="tgtSentence">Microsoft Exchange Online</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="43df6b136d7172bfc6b4dd4989cc5a6f" id="tgt5" class="tgtSentence">Exchange Online Dedicated</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="affaebbd36ef6522856c3f50fb6c71d4" id="tgt6" class="tgtSentence">Si configura el acceso condicional, el dispositivo que usen los usuarios debe cumplir las condiciones siguientes para que puedan conectarse al correo electrónico:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="eddc7b3b3949ca29d3c6935be941f878" id="tgt7" class="tgtSentence">Estar inscrito con <token>wit_nextref</token> o un equipo PC unido a un dominio.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4af7800e9aaf56ffa87f148da49163db" id="tgt8" class="tgtSentence">Registrar el dispositivo en Azure Active Directory, lo que se lleva a cabo automáticamente cuando el dispositivo está inscrito con <token>wit_nextref</token> (solo para Exchange Online).</caps:sentence>
              <caps:sentence sentenceid="a2b777df080325171348c22c01d2b3b2" id="tgt9" class="tgtSentence"> Además, el id. de Exchange ActiveSync del cliente debe registrarse con Azure Active Directory (no se aplica a dispositivos de Windows y Windows Phone que se conectan a Exchange local).</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="bc630c1a94707ccdc294b7acc58bcab6" id="tgt10" class="tgtSentence">Los equipos PC unidos a un dominio deben configurarse para que se registren automáticamente con Azure Active Directory.</caps:sentence>
              <caps:sentence sentenceid="23b58def11b45727d3351702515f86af" id="tgt11" class="tgtSentence">  En la sección <ui>Acceso condicional para equipos</ui> del tema <link xlink:href="c564d292-b83b-440d-bf08-3f5b299b7a5e">Manage access to email and SharePoint with Microsoft Intune</link> se enumeran todos los requisitos para habilitar el acceso condicional de equipos PC.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="1480ca351e9c6cd719b99a2de3e4d531" id="tgt12" class="tgtSentence">Cumplir todas las directivas de cumplimiento <token>wit_nextref</token> implementadas en el dispositivo</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="aa237268d451a9e117ad525e8a849a92" id="tgt13" class="tgtSentence">Si no se cumple una condición de acceso condicional, el usuario recibirá uno de los dos mensajes siguientes cuando inicie sesión:</caps:sentence>
        </para>
        <para>
          <ui>
            <caps:sentence sentenceid="d02bc33c006806d28914f8866baff9e0" id="tgt14" class="tgtSentence">Para dispositivos móviles:</caps:sentence>
          </ui>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="50e4346c332bdebd22004d6893fc5e4a" id="tgt15" class="tgtSentence">Si el dispositivo no está inscrito con <token>wit_nextref</token> o no está registrado en Azure Active Directory, se muestra un mensaje con instrucciones sobre cómo instalar la aplicación de portal de empresa, inscribir el dispositivo y activar el correo electrónico a fin de asociar el identificador de Exchange ActiveSync del dispositivo con el registro del dispositivo en Azure Active Directory.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="2c2d16f6fc224b9998c0d76a067a964d" id="tgt16" class="tgtSentence">Si el dispositivo no es conforme, se muestra un mensaje que dirige al usuario al portal web de <token>wit_nextref</token> o a la aplicación del portal de empresa, donde puede encontrar información sobre el problema y sobre cómo resolverlo.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <ui>
            <caps:sentence sentenceid="d64e796c5e1fe70311956587e5e173a7" id="tgt17" class="tgtSentence">Para los equipos PC:</caps:sentence>
          </ui>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="79247a8ee270717d730f3e88cafdee60" id="tgt18" class="tgtSentence">Si el requisito de la directiva de acceso condicional es permitir <ui>unido al dominio</ui> o <ui>conforme</ui>, se muestra un mensaje con instrucciones sobre cómo inscribir el dispositivo.</caps:sentence>
              <caps:sentence sentenceid="170324a0b74eb51500fc5833d88477aa" id="tgt19" class="tgtSentence"> Si el equipo no cumple con alguno de estos requisitos, se le solicitará al usuario que inscriba el dispositivo con <token>wit_nextref</token>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="3828f5015c7e0d46b78896fa07d37a36" id="tgt20" class="tgtSentence">Si el requisito de la directiva de acceso condicional se establece para permitir solo los dispositivos de Windows unidos a un dominio, el dispositivo se bloquea y aparece un mensaje para ponerse en contacto con el administrador de TI.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="1f85397911de369339a75d73dd53d53a" id="tgt21" class="tgtSentence">Puede bloquear el acceso al correo electrónico de Exchange desde el cliente de correo electrónico de Exchange ActiveSync integrado en los dispositivos en las siguientes plataformas:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="c022f0fcb0fb75f7b011c1e6f4224d0f" id="tgt22" class="tgtSentence">Android 4.0 y versiones posterior, Samsung Knox Standard 4.0 y versiones posteriores</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a3fd80a6345c43b6f755f910e3578d3d" id="tgt23" class="tgtSentence">iOS 7.1 y versiones posteriores</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0c22af16b4df02e420abe803e8c325e1" id="tgt24" class="tgtSentence">Windows Phone 8.1 y versiones posteriores</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt25" class="tgtSentence">La aplicación <ui>Correo</ui> en Windows 8.1 y versiones posteriores</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="91624a2c7adedb56fec2b4df39bf02b7" id="tgt26" class="tgtSentence">Aplicación de Outlook para iOS y Android</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="8302ac38e5183dd14f026611471f7d71" id="tgt27" class="tgtSentence">Escritorio de Outlook 2013</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="3ea7c70b08e0362cfc54f25228840241" id="tgt28" class="tgtSentence">Paso 1: evaluar el impacto de la directiva de acceso condicional</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="62084cfda3c38c5efd9368791319bad5" id="tgt29" class="tgtSentence">Si ha configurado una conexión entre <token>wit_nextref</token> y Exchange mediante <ui>Microsoft Intune Service to Service Connector</ui> o el <ui>conector de Exchange local</ui>, puede usar los <ui>informes de inventario de dispositivos móviles</ui> para identificar los clientes de correo de EAS que tendrán el acceso bloqueado a Exchange después de configurar la directiva de acceso condicional.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="87220f36738eca981086ee918e06f8d3" id="tgt30" class="tgtSentence">En los parámetros del informe, seleccione el grupo de <token>wit_nextref</token> que desea evaluar y, si es necesario, las plataformas de dispositivos a las que se aplicará la directiva.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="540ccbd153be5636c3e8fee1647183c3" id="tgt31" class="tgtSentence">Para obtener más información sobre cómo crear informes, consulte <link xlink:href="857309c2-61c9-4c22-becf-4839fedeaece">Manage reports in Windows Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="a14a954e01d4ea6879eca2029eb9381f" id="tgt32" class="tgtSentence">Después de ejecutar el informe, examine estas cuatro columnas para determinar si un usuario se bloqueará:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="1b8609087404c5f5d774cc1c1b8fb611" id="tgt33" class="tgtSentence">
                  <ui>Canal de administración</ui> : indica si Intune, Exchange ActiveSync o ambas aplicaciones administran el dispositivo.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d593f40a5e272fd9d53369632089f295" id="tgt34" class="tgtSentence">
                  <ui>Registrado en AAD</ui> : indica si el dispositivo está registrado con Azure Active Directory (lo que se conoce como unión al "área de trabajo").</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="14ef56a975f9cce79408dfde0e27f8db" id="tgt35" class="tgtSentence">
                  <ui>Conforme</ui> : indica si el dispositivo cumple con las directivas de cumplimiento que se han implementado.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1f362030e1dcce2fa7abc42d029edb4e" id="tgt36" class="tgtSentence">
                  <ui>  Id. de Exchange ActiveSync</ui>: los dispositivos iOS y Android deben tener su id. de Exchange ActiveSync asociado al registro de registro del dispositivo en Azure Active Directory.</caps:sentence>
                <caps:sentence sentenceid="90944ef82df69a5376fbebfde29c1863" id="tgt37" class="tgtSentence"> Esto sucede cuando el usuario hace clic en el vínculo Activar correo electrónico en el correo electrónico de cuarentena.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="1704c8167fff1d00b38075a7e4e6184d" id="tgt38" class="tgtSentence">Los dispositivos Windows Phone siempre muestran un valor en esta columna.</caps:sentence>
                </para>
              </alert>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="29168518cd38ba1d79b540db5f1fe86a" id="tgt39" class="tgtSentence">Los dispositivos que forman parte de un grupo de destino tendrán bloqueado el acceso a Exchange, a menos que los valores de la columna coincidan con los de la tabla siguiente:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5bfab5270787b3e0da8cfe474e41753f" id="tgt40" class="tgtSentence">Canal de administración</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fc5d6c79a5e541c725d0e1c4ec98a95b" id="tgt41" class="tgtSentence">Registrado en AAD</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0fbb03c7ab3a9629832bf719cd6d29e1" id="tgt42" class="tgtSentence">Conforme</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f48b5592d54a5d855c7f4197b3bb6402" id="tgt43" class="tgtSentence">Id. de Exchange ActiveSync</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f9541e0b82b81c07ad078c6a032b964a" id="tgt44" class="tgtSentence">Acción resultante</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="4671a7fed8a6f2d5e4e10fac8244d455" id="tgt45" class="tgtSentence">Administrado por Microsoft Intune y Exchange ActiveSync</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt46" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a6105c0a611b41b08f1209506350279e" id="tgt47" class="tgtSentence">Sí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5de9a8c6328e924432ace7188e29dadb" id="tgt48" class="tgtSentence">Se muestra un valor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90a924ed398d71fa6930ae476cc158ac" id="tgt49" class="tgtSentence">Acceso a correo electrónico concedido</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="998c896d56be7418e61681ba572145d2" id="tgt50" class="tgtSentence">Cualquier otro valor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt51" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7fa3b767c460b54a2be4d49030b349c7" id="tgt52" class="tgtSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b332e68dbd8b6ca582909d80c418cd2e" id="tgt53" class="tgtSentence">No se muestra ningún valor</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a4e17e9977b2507b521dc3c4a8a58b2" id="tgt54" class="tgtSentence">Acceso a correo electrónico bloqueado</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="a85a13fb12ef3797b2c8b04c913430f8" id="tgt55" class="tgtSentence">Puede exportar el contenido del informe y utilizar la columna <ui>Dirección de correo electrónico</ui> para informar a los usuarios de que se les va a bloquear.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="4ea06d9609bb570be83dfee5b36e28e9" id="tgt56" class="tgtSentence">Paso 2: configurar grupos de usuarios para la directiva de acceso condicional</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="75cfe20ee682b617ba5448ae64599e91" id="tgt57" class="tgtSentence">El destino de las directivas de acceso condicional se define en distintos grupos de usuarios en función de los tipos de directiva.</caps:sentence>
            <caps:sentence sentenceid="72da99a6f3e1296c1f37c8b940738681" id="tgt58" class="tgtSentence"> Estos grupos contienen los usuarios de destino o exentos de la directiva.</caps:sentence>
            <caps:sentence sentenceid="e5a3ae17baa5bd7e05c7b0fafa280a3c" id="tgt59" class="tgtSentence"> Cuando un usuario es destinatario de una directiva, cada dispositivo que use debe ser conforme con el fin de obtener acceso al correo electrónico.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="4dcd0b75f5aea368433092e50d0cb75b" id="tgt60" class="tgtSentence">
                  <ui>Directiva de Exchange Online</ui>: dirigida a grupos de usuarios de seguridad de Azure Active Directory.</caps:sentence>
                <caps:sentence sentenceid="81742dc3a20b8780a7507dbf2ca0edb9" id="tgt61" class="tgtSentence"> Estos grupos se pueden configurar en el <ui>Centro de administración de Office 365</ui> o el <ui>portal de cuentas de Intune</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6737ffb37c48893703f6fb4f531725e4" id="tgt62" class="tgtSentence">
                  <ui>Directiva de Exchange local</ui>: para grupos de usuarios de <token>wit_nextref</token>.</caps:sentence>
                <caps:sentence sentenceid="053c67e0e759cce819bda9cb10f75311" id="tgt63" class="tgtSentence"> Se pueden configurar en el área de trabajo <ui>Grupos</ui> de la consola de <token>wit_nextref</token>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="7ffb67825221348eb0e440518196be54" id="tgt64" class="tgtSentence">Se pueden especificar dos tipos de grupo en cada directiva:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="585a99b33fbdb21ad987df9fe31c2d39" id="tgt65" class="tgtSentence">
                  <ui>Grupos destinatarios</ui>: grupos de usuarios a los que se aplica la directiva</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9858819e506e59869a99c670b632353a" id="tgt66" class="tgtSentence">
                  <ui>Grupos exentos</ui>: grupos de usuarios que están exentos de la directiva (opcional)</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="4067e3fddd19ca3050d56a462abf4faf" id="tgt67" class="tgtSentence">Si un usuario pertenece a ambos grupos, estará exento de la directiva.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="421906a2e3747b4a1a4e2dde30309457" id="tgt68" class="tgtSentence">Solo los grupos que son destinatarios de la directiva de acceso condicional se evalúan para el acceso a Exchange.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="af4bbcc99ffc853467c72353f03a2aba" id="tgt69" class="tgtSentence">Paso 3: configurar e implementar una directiva de cumplimiento</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="98b47eb3419bf444a2e3e454628c2031" id="tgt70" class="tgtSentence">Asegúrese de que ha creado e implementado una directiva de cumplimiento para todos los dispositivos a los que se destinará la directiva de acceso condicional a Exchange.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d8516360b3ce4d15a69e25d3e05e3aa4" id="tgt71" class="tgtSentence">Para obtener más información sobre cómo configurar la directiva de cumplimiento, consulte <link xlink:href="0775107a-6662-41c8-9404-be14bbb599f3">Manage devices compliance with compliance policies for Microsoft Intune</link>.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence sentenceid="fb45497c836660b8b5b5c6a11cdc6bd1" id="tgt72" class="tgtSentence">Si no ha implementado una directiva de cumplimiento y habilitado la directiva de acceso condicional a Exchange, se permitirá el acceso a todos los dispositivos destinatarios.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="a297ae6c49f5b06f7fc854dc85896e5f" id="tgt73" class="tgtSentence">Cuando esté listo, continúe en el <ui>paso 4</ui>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5c4be61b6d75d52c9f2de640801f1ae8" id="tgt74" class="tgtSentence">Paso 4: configurar la directiva de acceso condicional</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="26d15c35c87a128a71c96f53ed32bb5c" id="tgt75" class="tgtSentence">Para Exchange Online (y los inquilinos del nuevo entorno de Exchange Online dedicado)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="fceaad590e37dc9c6ce3270753c3dcf3" id="tgt76" class="tgtSentence">Las directivas de acceso condicional de Exchange Online utilizan el siguiente flujo para evaluar si se permitirá o bloqueará el acceso a los dispositivos.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="5ffa6626-e7f2-4b11-a8a2-3c69a2510df7"></image>
              </mediaLink>
              <para>
                <caps:sentence sentenceid="85169efc046e28798e4ed31e6862b974" id="tgt77" class="tgtSentence">Para acceder al correo electrónico, el dispositivo debe:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="005a15ffaeabbe6d67807a67c16f78cf" id="tgt78" class="tgtSentence">Inscribirse con <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2c838c23a5e78536bc14791f8f4bd173" id="tgt79" class="tgtSentence">Los equipos deben estar unidos a un dominio o estar inscritos y cumplir con las directivas establecidas en <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4af7800e9aaf56ffa87f148da49163db" id="tgt80" class="tgtSentence">Estar registrado en Azure Active Directory, lo que se lleva a cabo automáticamente si el dispositivo está inscrito con <token>wit_nextref</token>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="07f2a9d1dbb86a2aaefd874fe575d663" id="tgt81" class="tgtSentence">Los equipos unidos a un dominio deben configurarse para que <externalLink><linkText>registren automáticamente el dispositivo</linkText><linkUri>https://msdn.microsoft.com/en-us/library/azure/dn935033.aspx</linkUri></externalLink> con Azure Active Directory.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="007250f7c3633d999f611bf7700f99a5" id="tgt82" class="tgtSentence">Tener activado el correo electrónico, que asocia el id. de Exchange ActiveSync del dispositivo con el registro del dispositivo en Azure Active Directory (aplicable solo a dispositivos iOS y Android).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="081cbd28136cb43de6df4a2b5c7a0c6c" id="tgt83" class="tgtSentence">Cumplir todas las directivas de cumplimiento de <token>wit_nextref</token> implementadas.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="8496c1c1d8d9e562c172596b38c62d6b" id="tgt84" class="tgtSentence">El estado del dispositivo se almacena en Azure Active Directory, que concede o bloquea el acceso al correo electrónico según las condiciones evaluadas.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="d19251108bb1c150e7383ab779ed2be1" id="tgt85" class="tgtSentence">Si no se cumple una condición, el usuario verá uno de los mensajes siguientes cuando inicie sesión:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="48e4c540e7819c702e8c82fc2732470d" id="tgt86" class="tgtSentence">Si el dispositivo no está inscrito o registrado en Azure Active Directory, se muestra un mensaje con instrucciones sobre cómo instalar la aplicación de portal de empresa e inscribirse.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2c2d16f6fc224b9998c0d76a067a964d" id="tgt87" class="tgtSentence">Si el dispositivo no es conforme, se muestra un mensaje que dirige al usuario al portal web de <token>wit_nextref</token>, donde puede encontrar información sobre el problema y sobre cómo resolverlo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="bfdc867bebd9421d57196f39bb1decf5" id="tgt88" class="tgtSentence">Para un equipo PC:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b5585bce3fdf8791f61007b96d9d7fce" id="tgt89" class="tgtSentence"> Si se establece la directiva para requerir unión a un dominio y el equipo no está unido a ningún dominio, se muestra un mensaje para ponerse en contacto con el administrador de TI.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4ab2036461c4199fe2a4ff1725f5fb24" id="tgt90" class="tgtSentence">Si se establece la directiva para requerir unión a un dominio o ser conforme y el equipo no cumple con estos requisitos, se muestra un mensaje con instrucciones sobre cómo instalar la aplicación del portal de empresa e inscribirse.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="da73e54a6bc2c91e11eedc75d5a94a49" id="tgt91" class="tgtSentence">El mensaje se muestra en el dispositivo para los usuarios de Exchange Online y los inquilinos en el nuevo entorno de Exchange Online dedicado, y se envía a la bandeja de entrada de correo electrónico de los usuarios de Exchange local y los dispositivos heredados dedicado de Exchange Online dedicados.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="5746279d02bf26f23d0f05e3cfc99904" id="tgt92" class="tgtSentence">Las reglas de acceso condicional de <token>wit_nextref</token> reemplazan, permiten, bloquean y ponen en cuarentena las reglas que se han definido en la consola de administración de Exchange Online.</caps:sentence>
                </para>
              </alert>
              <procedure expanded="true" address="BKMK_ExoCA">
                <title>
                  <caps:sentence sentenceid="d5e4584125b3b86003b77a7e023dd9ee" id="tgt93" class="tgtSentence">Para habilitar la directiva de Exchange Online</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt94" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Acceso condicional</ui> &gt; <ui>Directiva de Exchange Online</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt95" class="tgtSentence">En la página <ui>Directivas de Exchange Online</ui>, seleccione <ui>Habilitar directiva de acceso condicional para Exchange Online</ui>.</caps:sentence>
                        <caps:sentence sentenceid="a08a5df61c432f445573461a7451baf0" id="tgt96" class="tgtSentence"> Si selecciona esta opción, el dispositivo debe ser conforme.</caps:sentence>
                        <caps:sentence sentenceid="13657ddcbab4e55d1cbea7ee80790950" id="tgt97" class="tgtSentence"> Si no se selecciona esta opción, el acceso condicional no se aplica.</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="6d2f33a239b2ffd4c19dde8eaabfa4e9" id="tgt98" class="tgtSentence">Si no ha implementado una directiva de cumplimiento y habilita la directiva de Exchange Online, todos los dispositivos de destino se considerarán conformes.</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence sentenceid="fab0b5f99ebc04fc6fecb13dddbacc40" id="tgt99" class="tgtSentence">Independientemente del estado de cumplimiento, todos los usuarios a los que se aplique la directiva deberán inscribir sus dispositivos en <token>wit_nextref</token>.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt100" class="tgtSentence">En <ui>Aplicaciones que usan autenticación moderna</ui>, puede optar por restringir el acceso solo a los dispositivos que son conformes para cada plataforma.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence sentenceid="f690ff65bfad49d70aa9b0171ffc8cc1" id="tgt101" class="tgtSentence">
                            <ui>Autenticación moderna</ui> proporciona el inicio de sesión basado en Active Directory Authentication Library (ADAL) a los clientes de Office.</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="075c534b1583fb8e23755300db4276a5" id="tgt102" class="tgtSentence">La autenticación basada en ADAL permite a los clientes de Office realizar la autenticación basada en explorador (también conocida como autenticación pasiva).</caps:sentence>
                              <caps:sentence sentenceid="1fd5c59f431915a1f77fb209e41eb800" id="tgt103" class="tgtSentence">  Para realizar la autenticación, se envía al usuario a una página web de inicio de sesión.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="69721e6401936ef32deedb715b53351f" id="tgt104" class="tgtSentence">Este nuevo método de inicio de sesión permite nuevos escenarios, como el acceso condicional, según el <ui>cumplimiento de los dispositivos</ui> y si se realizó la <ui>autenticación multifactor</ui>.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                        <para>
                          <caps:sentence sentenceid="fb85d1d61b72e6145fd587f2ca7ff48a" id="tgt105" class="tgtSentence">Este <externalLink><linkText>artículo</linkText><linkUri>https://blogs.office.com/2014/11/12/office-2013-updated-authentication-enabling-multi-factor-authentication-saml-identity-providers/</linkUri></externalLink> contiene información más detallada sobre cómo funciona la autenticación moderna.</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence sentenceid="26405a184b0efa7cd8e12fd0de575001" id="tgt106" class="tgtSentence">	Los equipos deben estar unidos a un dominio o estar inscritos en Intune y ser conformes.</caps:sentence>
                        <caps:sentence sentenceid="9ea0aa9e3f0edea285d47ccbcb37c671" id="tgt107" class="tgtSentence"> Puede establecer los requisitos siguientes:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="9f94cb24780c2c87faeaf448185fa03e" id="tgt108" class="tgtSentence">
                              <ui>Los dispositivos deben estar unidos a un dominio o ser conformes.</ui>  Esto significa que los equipos deben estar unidos a un dominio o cumplir con las directivas establecidas en <token>wit_nextref</token>.</caps:sentence>
                            <caps:sentence sentenceid="21775613f60beb3aee0e647293f80637" id="tgt109" class="tgtSentence"> Si el equipo no cumple con alguno de estos requisitos, se le solicita al usuario que inscriba el dispositivo con <token>wit_nextref</token>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="91937e9910e4ca7bbea202474ccb5ddd" id="tgt110" class="tgtSentence">
                              <ui>Los dispositivos deben estar unidos a un dominio.</ui> Esto significa que los equipos deben estar unidos a un dominio para tener acceso a Exchange Online.</caps:sentence>
                            <caps:sentence sentenceid="68e4992abbfeb3c316dc99812e6bdb5c" id="tgt111" class="tgtSentence"> Si el equipo no está unido a un dominio, el acceso al correo electrónico se bloquea y el usuario debe ponerse en contacto con el administrador de TI.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="973696ad386daf5b6cf795220b026381" id="tgt112" class="tgtSentence">
                              <ui>Los dispositivos deben ser conformes.</ui> Esto significa que los equipos deben inscribirse en <token>wit_nextref</token> y ser conformes.</caps:sentence>
                            <caps:sentence sentenceid="dcf5f59147df996519223897e643998c" id="tgt113" class="tgtSentence"> Si el equipo no está inscrito, se muestra un mensaje con instrucciones sobre cómo inscribirse.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt114" class="tgtSentence">En <ui>Aplicaciones de correo de Exchange ActiveSync</ui>, puede bloquear el acceso del correo electrónico a Exchange Online si el dispositivo no es conforme y seleccionar si desea permitir o bloquear el acceso a correo electrónico cuando Microsoft Intune no pueda administrar el dispositivo.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt115" class="tgtSentence">En <ui>Grupos de destino</ui>, seleccione los grupos de seguridad de Active Directory a los que se aplicará la directiva.</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="04a5e4dc9ba11e515c8e43cf411d2590" id="tgt116" class="tgtSentence">Para los usuarios que se encuentren en los grupos de destino, las directivas de Intune reemplazarán las directivas y reglas de Exchange.</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence sentenceid="71a934f87b7e68d74b80b97eb381659c" id="tgt117" class="tgtSentence">Exchange solo aplicará sus directivas y sus reglas de permiso, bloqueo y cuarentena si:</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="f159d5a935bebe5b8bffe966f9681b8d" id="tgt118" class="tgtSentence">
	El usuario no tiene licencia para Intune.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="1bd78fd349502f3ca9fd72625a19cc18" id="tgt119" class="tgtSentence">El usuario tiene licencia para Intune pero no pertenece a ningún grupo de seguridad de destino de la directiva de acceso condicional.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt120" class="tgtSentence">En <ui>Grupos exentos</ui>, seleccione los grupos de seguridad de Active Directory que se van a excluir de la directiva.</caps:sentence>
                        <caps:sentence sentenceid="11fbe1fb98790081ade2bd68b13cdfdc" id="tgt121" class="tgtSentence"> Si un usuario está incluido tanto los grupos de destino como en los grupos exentos, estará exento de la directiva.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt122" class="tgtSentence">En <ui>Plataformas no compatibles</ui>, seleccione si desea permitir o bloquear el acceso al correo electrónico cuando <token>wit_firstref</token> no pueda administrar el dispositivo y se administre mediante Exchange ActiveSync.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="1bce99f66636e1381b9dced6fe461268" id="tgt123" class="tgtSentence">Cuando haya terminado, haga clic en <ui>Guardar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="a124f6fb61b65c82978835b18206da1a" id="tgt124" class="tgtSentence">No es necesario implementar la directiva de acceso condicional, ya que surte efecto inmediatamente.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="9d40e5f27bdcb4d9b10a8bf172398172" id="tgt125" class="tgtSentence">Cuando un usuario crea una cuenta de correo electrónico, el dispositivo se bloquea inmediatamente.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="1583a2f2dc96fe683fe90d9cd5eb8234" id="tgt126" class="tgtSentence">Si un usuario bloqueado inscribe el dispositivo con <token>wit_nextref</token> (o corrige la no conformidad), el acceso al correo electrónico se desbloquea en dos minutos.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="c4b7fb521431ca712c81972462d5a065" id="tgt127" class="tgtSentence">Si el usuario anula la inscripción del dispositivo, el correo electrónico se bloquea transcurridas unas 24 horas.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </content>
                </conclusion>
              </procedure>
            </content>
            <sections></sections>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="f05cfe8af42a44802072f4bea2461211" id="tgt128" class="tgtSentence">Para Exchange local (y los inquilinos del entorno heredado de Exchange Online dedicado)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="7e7f48fb7c16948c8d8c3c1a57690b69" id="tgt129" class="tgtSentence">Las directivas de acceso condicional de Exchange local y los inquilinos del entorno heredado de Exchange Online dedicado utilizan el siguiente flujo para evaluar si se deben permitir o bloquear los dispositivos.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="7977d51d-3541-4666-a3d4-3864e112790b"></image>
              </mediaLink>
              <procedure expanded="true">
                <title>
                  <caps:sentence sentenceid="4a49166bd59412a967da16bf5eaca57c" id="tgt130" class="tgtSentence">Para habilitar la directiva de Exchange local</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt131" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Acceso condicional</ui> &gt; <ui>Directiva local de Exchange</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="cdd0dcc00e323efa2df849e56ba05b4f" id="tgt132" class="tgtSentence">Configure la directiva con la configuración que necesite:</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="7dc22b2c6a992f0232345df41303f5ea" id="tgt133" class="tgtSentence">Configuración</caps:sentence>
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
                                <ui>
                                  <caps:sentence sentenceid="09695c7d03dd121fa1cbd1deeabadece" id="tgt135" class="tgtSentence">Bloquear el acceso de las aplicaciones de correo electrónico a Exchange Online si el dispositivo no es conforme o no está inscrito en Microsoft Intune</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="65c04b348fbca468f2bb121582ff9060" id="tgt136" class="tgtSentence">Si selecciona esta opción, los dispositivos que no se administren mediante <token>wit_nextref</token> o no cumplan una directiva de cumplimiento aplicable, no podrán acceder a los servicios de Exchange a menos que se hayan definido como exentos.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="44b5ca4d696f1a8fe9cdf83d1ad18ee8" id="tgt137" class="tgtSentence">Invalidación de regla predeterminada: permitir que los dispositivos inscritos y que cumplan con las directivas oportunas puedan obtener acceso a Exchange</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="b5d7151db2ccba3bfd5d645da3bf6546" id="tgt138" class="tgtSentence">Cuando se selecciona esta opción, los dispositivos inscritos en Intune y que cumplen con las directivas establecidas pueden tener acceso a Exchange.</caps:sentence>
                                <caps:sentence sentenceid="4baee07b9515cbbbecb6828820c676b3" id="tgt139" class="tgtSentence">  Esta regla invalida la <ui>regla predeterminada</ui>, lo que significa que incluso si configura la <ui>regla predeterminada</ui> y la establece en cuarentena o para bloquear el acceso, aquellos dispositivos inscritos y que cumplen con las directivas aún seguirán teniendo acceso a Exchange.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="4a5155a6ee8bdd7a6ef224e30e0dfe49" id="tgt140" class="tgtSentence">Grupos de destino</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="7486589d03c162162a7c4e75345fcca4" id="tgt141" class="tgtSentence">Seleccione los grupos de usuarios de <token>wit_nextref</token> que deben inscribir su dispositivo con <token>wit_nextref</token> para poder acceder a Exchange.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="db59dbc232f8fa083e5144f95c0275ed" id="tgt142" class="tgtSentence">Grupos exentos</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="7486589d03c162162a7c4e75345fcca4" id="tgt143" class="tgtSentence">Seleccione los grupos de usuarios de <token>wit_nextref</token> exentos de la directiva de acceso condicional.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="f44870320cd761039f4127ae3f5fbffa" id="tgt144" class="tgtSentence">La configuración de esta lista invalida la de la lista <ui>Grupos de destino</ui>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="a1eafdb6ce2eaabe73dc20afe1690d7f" id="tgt145" class="tgtSentence">Excepciones de plataforma</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt146" class="tgtSentence">Haga clic en <ui>Agregar regla</ui> para configurar una regla que defina los niveles de acceso para las familias y modelos de dispositivos móviles especificados.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="67b2a42cc5b982d0072427ea28551a8b" id="tgt147" class="tgtSentence">Dado que estos dispositivos pueden ser de cualquier tipo,puede configurar tipos de dispositivo que no sean compatibles con <token>wit_nextref</token>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="c2ffa6ac1123111c37160cc54f1300a5" id="tgt148" class="tgtSentence">Regla predeterminada</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="cf04733d63d3d91d295a58106a28cd8a" id="tgt149" class="tgtSentence">En el caso de un dispositivo no cubierto por ninguna de las otras reglas, puede permitirle el acceso a Exchange, bloquearlo o ponerlo en cuarentena.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="5a1fccec765b4e6c32cc3125980d8422" id="tgt150" class="tgtSentence">Al establecer la regla para permitir el acceso a los dispositivos que están inscritos y que cumplen con las directivas, se concede acceso automático al correo electrónico a aquellos dispositivos de iOS, Windows y Samsung Knox.</caps:sentence>
                                <caps:sentence sentenceid="c5ed50c2de013de56cb73f4aef71f5b3" id="tgt151" class="tgtSentence"> El usuario final no tiene que realizar ningún proceso para obtener acceso a su correo electrónico.</caps:sentence>
                                <caps:sentence sentenceid="b506a4107fbb088841d5e11ab758683f" id="tgt152" class="tgtSentence">  En dispositivos Android que no estén basados en Knox, los usuarios finales obtendrán un correo electrónico de cuarentena que incluye un tutorial que le ayudará, paso a paso, a comprobar la inscripción y el cumplimiento de normas para así poder tener acceso al correo electrónico.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="f11629286950da608dc254eb18336a6e" id="tgt153" class="tgtSentence">Si establece la regla para bloquear el acceso o establecer una cuarentena, todos los dispositivos se bloquean al obtener acceso a Exchange, independientemente de si están ya inscritos en Intune o no.</caps:sentence>
                                <caps:sentence sentenceid="d50efd185a5ac51c884ce02cd7822a42" id="tgt154" class="tgtSentence"> Para evitar que los dispositivos inscritos y que cumplen las directivas se vean afectados por esta regla, compruebe la <ui>invalidación de la regla predeterminada.</ui></caps:sentence>
                              </para>
                              <alert class="tip">
                                <para>
                                  <caps:sentence sentenceid="431ffda8fb4c6d351d291b8bd8580860" id="tgt155" class="tgtSentence">Si se pretende bloquear primero todos los dispositivos antes de conceder acceso al correo electrónico, puede serle de utilidad comprobar las opciones de bloqueo de acceso o de regla de cuarentena.</caps:sentence>
                                </para>
                              </alert>
                              <para>
                                <caps:sentence sentenceid="b00224633201c962199c17278cd17e0d" id="tgt156" class="tgtSentence">La regla predeterminada se aplicará a todos los tipos de dispositivo, por lo que los tipos de dispositivo que configure como excepciones de la plataforma y que no sean compatibles con <token>wit_nextref</token> también se verán afectados.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="e51c61809f825a254170407129d04fb1" id="tgt157" class="tgtSentence">Notificación de usuario</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="578e27339d3d313a0563381cff1bb253" id="tgt158" class="tgtSentence">Además del correo electrónico de notificación enviado desde Exchange, Intune envía un correo electrónico que puede configurar y que incluye los pasos para desbloquear el dispositivo.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="bb73586a10fdb6c407562c99c123c2a8" id="tgt159" class="tgtSentence">Puede modificar el mensaje predeterminado y usar etiquetas HTML para formatear el aspecto del texto.</caps:sentence>
                              </para>
                              <alert class="note">
                                <para>
                                  <caps:sentence sentenceid="a196ceceb5bc9d75a708af5252460c38" id="tgt160" class="tgtSentence">Dado que el correo electrónico de notificación de Intune que contiene instrucciones de corrección se envía al buzón de Exchange del usuario, en caso de que el dispositivo del usuario se bloquee antes de recibir el mensaje de correo electrónico, puede usar un dispositivo desbloqueado u otro método para acceder a Exchange y ver el mensaje.</caps:sentence>
                                </para>
                                <para>
                                  <caps:sentence sentenceid="231f401846dcae2ff5343c3943c330ac" id="tgt161" class="tgtSentence">Esto se cumple especialmente cuando la <ui>regla predeterminada</ui> está establecida para bloquear o para poner en cuarentena los dispositivos.</caps:sentence>
                                  <caps:sentence sentenceid="e944f5ac06307c43938e33c84b082b6d" id="tgt162" class="tgtSentence">  En este caso, el usuario final tendrá que ir a su tienda de aplicaciones, descargar la aplicación Portal de empresa de Microsoft e inscribir su dispositivo.</caps:sentence>
                                  <caps:sentence sentenceid="694ee1e708924fd55a13001b66955a32" id="tgt163" class="tgtSentence"> Esto es aplicable a los dispositivos de iOS, Windows y Samsung Knox.</caps:sentence>
                                  <caps:sentence sentenceid="7362e682c0f1b34cd582a3a308718396" id="tgt164" class="tgtSentence">  En cuanto a aquellos dispositivos Android que no están basados en Knox, los administradores de TI tendrán que enviar el correo electrónico de cuarentena a una cuenta de correo electrónico alternativa; a continuación, el usuario final debe copiar ese correo de cuarentena en su dispositivo bloqueado para completar el proceso de inscripción y de cumplimiento de directivas.</caps:sentence>
                                </para>
                              </alert>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="161c3e30514df091b1accff593fa4dd4" id="tgt165" class="tgtSentence">Para que Exchange pueda enviar el correo electrónico de notificación, debe configurar la cuenta que se usará para enviarlo.</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence sentenceid="3d7d30605a309123a172bc57a6d96f71" id="tgt166" class="tgtSentence">Para obtener más información, consulte <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_EX_OP">Configure Microsoft Intune on-premises connector for on-premises or hosted Exchange</link>.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="1bce99f66636e1381b9dced6fe461268" id="tgt167" class="tgtSentence">Cuando haya terminado, haga clic en <ui>Guardar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="a124f6fb61b65c82978835b18206da1a" id="tgt168" class="tgtSentence">No es necesario implementar la directiva de acceso condicional, ya que surte efecto inmediatamente.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="99334118cec64c12317e24b18b577f9d" id="tgt169" class="tgtSentence">Después de que un usuario configure un perfil de Exchange ActiveSync, puede tardar de 1 a 3 horas en bloquear el dispositivo (si no está administrado por <token>wit_nextref</token>).</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="247a83b6505300a186273161b2e0a9ef" id="tgt170" class="tgtSentence">Si un usuario bloqueado luego inscribe el dispositivo con <token>wit_nextref</token> (o corrige la no conformidad), el acceso al correo electrónico se desbloqueará en dos minutos.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="a3207af6092c9bef2a5bc071637b4b53" id="tgt171" class="tgtSentence">Si el usuario anula la inscripción de <token>wit_nextref</token>, puede tardar de 1 a 3 horas en desbloquear el dispositivo.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="81b0a2b5aa70f570f579aeeec8c18f3c" id="tgt172" class="tgtSentence">Paso 5: supervisar el cumplimiento y las directivas de acceso condicional</caps:sentence>
        </title>
        <content>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="5c3dc5b9c245922e0aa0e2147841f0e1" id="tgt173" class="tgtSentence">Para ver los dispositivos que tienen bloqueado el acceso a Exchange</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt174" class="tgtSentence">En el panel de <token>wit_nextref</token>, haga clic en el icono <ui>Dispositivos bloqueados de Exchange</ui> para que se muestre el número de dispositivos bloqueados y vínculos para obtener más información.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Scenario">
        <title>
          <caps:sentence sentenceid="54001408eabb561c2bbc05343018ce00" id="tgt175" class="tgtSentence">Escenarios de ejemplo</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="89aad046c4013782591f1e213e5669d0" id="tgt176" class="tgtSentence">Todos los dispositivos iOS que tienen acceso a Exchange local deben administrarse mediante Intune</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="3b1bf2b1d545abb707e936b56dbd017d" id="tgt177" class="tgtSentence">En este ejemplo, la organización utiliza únicamente dispositivos que ejecutan iOS y requieren que todos estos dispositivos estén administrados por <token>wit_nextref</token> para poder acceder a Exchange.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="90582b952e4c8b13220909036e4b35ec" id="tgt178" class="tgtSentence">Para ello, en la directiva de acceso condicional configuran lo siguiente:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1fb1688e436e71ed7ab5e427efe8495c" id="tgt179" class="tgtSentence">Seleccione la opción <ui>Habilitar directiva de acceso condicional para Exchange Online</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="54ae865bf1a10f03a5526d0dc2cdfe0f" id="tgt180" class="tgtSentence">Para las aplicaciones que usan la autenticación moderna, seleccione <ui>iOS</ui> para la plataforma</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0ceb13d3a431f3ddf08ee4e56b48f23b" id="tgt181" class="tgtSentence">Para las aplicaciones de Exchange ActiveSync, seleccione <ui>Requiere que los dispositivos móviles sean compatibles</ui> y bloquee el acceso a correo electrónico en los dispositivos que no son compatibles con <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b77c299b8702b3d232e68bf366b5d3fe" id="tgt182" class="tgtSentence">Una excepción de plataforma que permite que los dispositivos que ejecutan iOS tengan acceso a Exchange.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e71b33375b07150caae49c2d5602ae9a" id="tgt183" class="tgtSentence">Una regla predeterminada que especifica si un dispositivo no está cubierto por otras reglas, por lo que se debe bloquear.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="63b6b6b310c709f2985e3f3d1491ff8c" id="tgt184" class="tgtSentence">El siguiente flujo se utiliza para decidir los dispositivos que pueden tener acceso a Exchange:</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="9306af75-8e89-46a4-a7fa-dc09107a4d0c"></image>
              </mediaLink>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="e7aafac32e95b0e68022ac1d4a1bbe7a" id="tgt185" class="tgtSentence">Ningún dispositivo Android puede acceder a Exchange local.</caps:sentence>
              <caps:sentence sentenceid="4486d5a36ee52faf8e5c27074ff61950" id="tgt186" class="tgtSentence"> El resto de los dispositivos que accedan a Exchange deben administrarse mediante Intune</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="49260368316a902d1555879da9d17cc6" id="tgt187" class="tgtSentence">En este ejemplo, la organización no desea permitir que los dispositivos que ejecuten Android accedan a Exchange.</caps:sentence>
                <caps:sentence sentenceid="2e3c94b39565f85d939c2600115b1fc2" id="tgt188" class="tgtSentence"> Los demás dispositivos compatibles pueden tener acceso a Exchange, siempre que estén administrados por <token>wit_nextref</token>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="90582b952e4c8b13220909036e4b35ec" id="tgt189" class="tgtSentence">Para ello, en la directiva de acceso condicional configuran lo siguiente:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1fb1688e436e71ed7ab5e427efe8495c" id="tgt190" class="tgtSentence">Seleccione la opción <ui>Habilitar directiva de acceso condicional para Exchange Online</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="80c8bdc6093f1e6aceab77f0d67073e7" id="tgt191" class="tgtSentence">Una excepción de plataforma que impide que los dispositivos que ejecutan Android tengan acceso a Exchange.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="99c01db28a6083d1f28d2c03483aca96" id="tgt192" class="tgtSentence">Una regla predeterminada que especifica si un dispositivo no está cubierto por otras reglas, por lo que debe permitirse.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="63b6b6b310c709f2985e3f3d1491ff8c" id="tgt193" class="tgtSentence">El siguiente flujo se utiliza para decidir los dispositivos que pueden tener acceso a Exchange:</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="59d82948-47d5-47f9-90bd-e8380d8cd152"></image>
              </mediaLink>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="5c6c36fa2064bbcf4e3ca828864556e9" id="tgt194" class="tgtSentence">Bloquee a los usuarios de dispositivos no conformes el acceso a Exchange Online en un grupo de seguridad de Active Directory especificado.</caps:sentence>
              <caps:sentence sentenceid="868068d2fec8f3bd78e39a67a0644ba1" id="tgt195" class="tgtSentence"> Dispositivos exentos en otro grupo de seguridad</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="0d43e43ef792b7b9c456216f24a58c15" id="tgt196" class="tgtSentence">En este escenario, todos los usuarios del grupo de seguridad <ui>Contabilidad</ui> de Active Directory deben tener bloqueado el acceso a Exchange Online si su dispositivo no cumple con una directiva de cumplimiento implementada.</caps:sentence>
                <caps:sentence sentenceid="7903ea984c4e5bab1e1eff2fcd3daa3b" id="tgt197" class="tgtSentence"> Además, los dispositivos que se encuentren en el grupo de seguridad <ui>Finanzas</ui> de Active Directory deben estar exentos de la aplicación de la directiva, aunque también estén incluidos en el grupo de seguridad <ui>Contabilidad</ui>.</caps:sentence>
                <caps:sentence sentenceid="eee9afa3cac30105b0709f039e88d950" id="tgt198" class="tgtSentence"> Por último, si existe algún usuario en este grupo cuyos dispositivos no son compatibles con <token>wit_nextref</token>, se deberá bloquear su acceso a Exchange Online en ese dispositivo.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="90582b952e4c8b13220909036e4b35ec" id="tgt199" class="tgtSentence">Para ello, en la directiva de acceso condicional configuran lo siguiente:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1fb1688e436e71ed7ab5e427efe8495c" id="tgt200" class="tgtSentence">Seleccione la opción <ui>Habilitar directiva de acceso condicional para Exchange Online</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt201" class="tgtSentence">Seleccione <ui>Contabilidad</ui> en <ui>Grupos de destino</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt202" class="tgtSentence">Seleccione <ui>Finanzas</ui> en <ui>Grupos exentos</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt203" class="tgtSentence">En <ui>Aplicaciones de correo de Exchange ActiveSync</ui>, seleccione la opción <ui>Requiere que los dispositivos móviles sean compatibles</ui>.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="63b6b6b310c709f2985e3f3d1491ff8c" id="tgt204" class="tgtSentence">El siguiente flujo se utiliza para decidir los dispositivos que pueden tener acceso a Exchange:</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="0d96dec0-377a-4fa7-978d-0ff62e653d8f"></image>
              </mediaLink>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="c564d292-b83b-440d-bf08-3f5b299b7a5e">Manage access to email and SharePoint with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the <token>wit_firstref</token> <ui>conditional access policies</ui> for Exchange to manage access to Exchange email based on conditions you specify.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">You can manage access to:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">Microsoft Exchange On-premises</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">Microsoft Exchange Online</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Exchange Online Dedicated</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src6" class="srcSentence">If you configure conditional access, before a user can connect to their email, the device they use must:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Be enrolled with <token>wit_nextref</token> or a domain joined PC.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Register the device in Azure Active Directory (this happens automatically when the device is enrolled with <token>wit_nextref</token> (for Exchange Online only).</caps:sentence>
              <caps:sentence id="src9" class="srcSentence"> Additionally, the client Exchange ActiveSync ID must be registered with Azure Active Directory (does not apply to Windows and Windows Phone devices connecting to Exchange On-premises).</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src10" class="srcSentence">For a domain joined PC, you must set it to automatically register with Azure Active Directory.</caps:sentence>
              <caps:sentence id="src11" class="srcSentence">
                <ui>Conditional Access for PCs</ui> section in the <link xlink:href="c564d292-b83b-440d-bf08-3f5b299b7a5e">Manage access to email and SharePoint with Microsoft Intune</link> topic lists the full set of requirements to enable conditional access for PCs.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Be compliant with any <token>wit_nextref</token> compliance policies deployed to that device</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src13" class="srcSentence">If a conditional access condition is not met, the user is presented with one of the following messages when they log in.</caps:sentence>
        </para>
        <para>
          <ui>
            <caps:sentence id="src14" class="srcSentence">For mobile devices:</caps:sentence>
          </ui>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src15" class="srcSentence">If the device is not enrolled with <token>wit_nextref</token>, or is not registered in Azure Active Directory, a message is displayed with instructions about how to install the company portal app, enroll the device, activate email, which associates the device’s Exchange ActiveSync ID with the device record in Azure Active Directory.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src16" class="srcSentence">If the device is not compliant, a message is displayed that directs the user to the <token>wit_nextref</token> web portal, or the company portal app where they can find information about the problem and how to remediate it.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <ui>
            <caps:sentence id="src17" class="srcSentence">For PCs:</caps:sentence>
          </ui>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src18" class="srcSentence">If the conditional access policy requirement is to allow <ui>domain joined</ui> or <ui>compliant</ui>, a message with instructions about how to enroll the device is displayed.</caps:sentence>
              <caps:sentence id="src19" class="srcSentence"> If the PC does not meet either of the requirements, the user will be asked to enroll the device with <token>wit_nextref</token>.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src20" class="srcSentence">If the conditional access policy requirement is set to allow only domain joined windows devices, the device is blocked and a message to contact the IT admin is displayed.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src21" class="srcSentence">You can block access to Exchange email from the devices built-in Exchange ActiveSync email client on the following platforms:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src22" class="srcSentence">Android 4.0 and later, Samsung Knox Standard 4.0 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src23" class="srcSentence">iOS 7.1 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src24" class="srcSentence">Windows Phone 8.1 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src25" class="srcSentence">The <ui>Mail</ui> application on Windows 8.1 and later</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src26" class="srcSentence">Outlook app for iOS and Android</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src27" class="srcSentence">Outlook desktop 2013</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src28" class="srcSentence">Step 1: Evaluate the effect of the conditional access policy</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src29" class="srcSentence">If you have configured a connection between <token>wit_nextref</token> and Exchange by using the <ui>Microsoft Intune service to service connector</ui> or the <ui>on-premises Exchange connector</ui>, you can use the <ui>Mobile Device Inventory Reports</ui> to identify EAS mail clients that will be blocked from accessing Exchange after you configure the conditional access policy.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src30" class="srcSentence">In the report parameters, select the <token>wit_nextref</token> group you want to evaluate and, if required, the device platforms to which the policy will apply.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src31" class="srcSentence">For more information about how to run reports, see <link xlink:href="857309c2-61c9-4c22-becf-4839fedeaece">Manage reports in Windows Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src32" class="srcSentence">After you run the report, examine these four columns to determine whether a user will be blocked:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src33" class="srcSentence">
                  <ui>Management Channel</ui> – Indicates whether the device is managed by Intune, Exchange ActiveSync, or both.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src34" class="srcSentence">
                  <ui>AAD Registered</ui> – Indicates whether the device is registered with Azure Active Directory (known as Workplace Join).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src35" class="srcSentence">
                  <ui>Compliant</ui> – Indicates whether the device is compliant with any compliance policies you deployed.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src36" class="srcSentence">
                  <ui>Exchange ActiveSync ID</ui> – iOS and Android devices are required to have their Exchange ActiveSync ID associated with the device registration record in Azure Active Directory.</caps:sentence>
                <caps:sentence id="src37" class="srcSentence"> This happens when the user clicks the Activate Email link in the quarantine email.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src38" class="srcSentence">Windows Phone devices always display a value in this column.</caps:sentence>
                </para>
              </alert>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src39" class="srcSentence">Devices that are part of a targeted group will be blocked from accessing Exchange unless the column values match those listed in the following table:</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Management channel</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">AAD registered</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Compliant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Exchange ActiveSync ID</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Resulting action</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <ui>
                      <caps:sentence id="src45" class="srcSentence">Managed by Microsoft Intune and Exchange ActiveSync</caps:sentence>
                    </ui>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">Yes</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">A value is displayed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">Email access allowed</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">Any other value</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">No</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">No value is displayed</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">Email access blocked</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src55" class="srcSentence">You can export the contents of the report and use the <ui>Email Address</ui> column to help you inform users that they will be blocked.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src56" class="srcSentence">Step 2: Configure user groups for the conditional access policy</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src57" class="srcSentence">You target conditional access policies to different groups of users depending on the policy types.</caps:sentence>
            <caps:sentence id="src58" class="srcSentence"> These groups contain the users that will be targeted, or exempt from the policy.</caps:sentence>
            <caps:sentence id="src59" class="srcSentence"> When a user is targeted by a policy, each device they use must be compliant in order to access email.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src60" class="srcSentence">
                  <ui>For the Exchange Online policy</ui> – to Azure Active Directory security user groups.</caps:sentence>
                <caps:sentence id="src61" class="srcSentence"> You can configure these groups in the <ui>Office 365 admin center</ui>, or the <ui>Intune account portal</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src62" class="srcSentence">
                  <ui>For the Exchange On-premises policy</ui> – to <token>wit_nextref</token> user groups.</caps:sentence>
                <caps:sentence id="src63" class="srcSentence"> You can configure these in the <ui>Groups</ui> workspace of the <token>wit_nextref</token> console.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src64" class="srcSentence">You can specify two group types in each policy:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src65" class="srcSentence">
                  <ui>Targeted groups</ui> – User groups to which the policy is applied</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src66" class="srcSentence">
                  <ui>Exempted groups</ui> – User groups that are exempt from the policy (optional)</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src67" class="srcSentence">If a user is in both groups, they will be exempt from the policy.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src68" class="srcSentence">Only the groups which are targeted by the conditional access policy are evaluated for Exchange access.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src69" class="srcSentence">Step 3: Configure and deploy a compliance policy</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src70" class="srcSentence">Ensure that you have created and deployed a compliance policy to all devices that the Exchange conditional access policy will be targeted to.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src71" class="srcSentence">For details about how to configure the compliance policy, see <link xlink:href="0775107a-6662-41c8-9404-be14bbb599f3">Manage devices compliance with compliance policies for Microsoft Intune</link>.</caps:sentence>
          </para>
          <alert class="important">
            <para>
              <caps:sentence id="src72" class="srcSentence">If you have not deployed a compliance policy and then enable an Exchange conditional access policy, all targeted devices will be allowed access.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src73" class="srcSentence">When you are ready, continue to <ui>Step 4</ui>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src74" class="srcSentence">Step 4: Configure the conditional access policy</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src75" class="srcSentence">For Exchange Online (and tenants in the new Exchange Online Dedicated environment)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src76" class="srcSentence">The following flow is used by conditional access policies for Exchange Online to evaluate whether to allow or block devices.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="5ffa6626-e7f2-4b11-a8a2-3c69a2510df7"></image>
              </mediaLink>
              <para>
                <caps:sentence id="src77" class="srcSentence">To access email, the device must:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">Enroll with <token>wit_nextref</token></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">PCs must either be domain joined or be enrolled and compliant with the policies set in <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">Register the device in Azure Active Directory (this happens automatically when the device is enrolled with <token>wit_nextref</token>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src81" class="srcSentence">For domain joined PCs, you must  set it up to <externalLink><linkText>automatically register the device</linkText><linkUri>https://msdn.microsoft.com/en-us/library/azure/dn935033.aspx</linkUri></externalLink> with Azure Active Directory.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">Have activated email, which associates the device’s Exchange ActiveSync ID with the device record in Azure Active Directory (applies to iOS and Android devices only).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src83" class="srcSentence">Be compliant with any deployed <token>wit_nextref</token> compliance policies</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src84" class="srcSentence">The device state is stored in Azure Active Directory which grants or blocks access to email, based on the evaluated conditions.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src85" class="srcSentence">If a condition is not met, the user will be presented with one of the following messages when they log in:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">If the device is not enrolled, or registered in Azure Active Directory, a message is displayed with instructions about how to install the company portal app and enroll.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">If the device is not compliant, a message is displayed that directs the user to the <token>wit_nextref</token> web portal where they can find information about the problem and how to remediate it.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">For a PC:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src89" class="srcSentence"> If the policy is set to require domain join, and the PC is not domain joined, a message is displayed to contact the IT admin.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">If the policy is set to require domain join or compliant, then the PC does not meet either requirement, a message is displayed with instructions about how to install the company portal app and enroll.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src91" class="srcSentence">The message is displayed on the device for Exchange Online users and tenants in the new Exchange Online Dedicated environment, and is delivered to the users email inbox for Exchange On-premises and legacy Exchange Online Dedicated devices.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src92" class="srcSentence">
                    <token>wit_nextref</token> conditional access rules override, allow, block and quarantine rules that are defined in the Exchange Online admin console.</caps:sentence>
                </para>
              </alert>
              <procedure expanded="true" address="BKMK_ExoCA">
                <title>
                  <caps:sentence id="src93" class="srcSentence">To enable the Exchange Online policy</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src94" class="srcSentence">In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Conditional Access</ui> &gt; <ui>Exchange Online Policy</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">On the <ui>Exchange Online Policy</ui> page, select <ui>Enable conditional access policy for Exchange Online</ui>.</caps:sentence>
                        <caps:sentence id="src96" class="srcSentence"> If you check this, the device must be compliant.</caps:sentence>
                        <caps:sentence id="src97" class="srcSentence"> If this is not checked then conditional access is not applied.</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src98" class="srcSentence">If you have not deployed a compliance policy and then enable the Exchange Online policy, all targeted devices are reported as compliant.</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence id="src99" class="srcSentence">Regardless of the compliance state, all users who are targeted by the policy will be required to enroll their devices with <token>wit_nextref</token>.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src100" class="srcSentence">Under <ui>Apps using modern authentication</ui>, you can choose to restrict access only to devices that are compliant for each platform.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence id="src101" class="srcSentence">
                            <ui>Modern authentication</ui> brings Active Directory Authentication Library (ADAL)-based sign in to Office clients.</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence id="src102" class="srcSentence">The ADAL based authentication enables Office clients to engage in browser-based authentication (also known as passive authentication).</caps:sentence>
                              <caps:sentence id="src103" class="srcSentence">  To authenticate, the user is directed to a sign-in web page.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence id="src104" class="srcSentence">This new sign-in method enables new scenarios such as, conditional access, based on <ui>device compliance</ui> and whether <ui>multi-factor authentication</ui> was performed.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                        <para>
                          <caps:sentence id="src105" class="srcSentence">This <externalLink><linkText>article</linkText><linkUri>https://blogs.office.com/2014/11/12/office-2013-updated-authentication-enabling-multi-factor-authentication-saml-identity-providers/</linkUri></externalLink> has more detailed information on how modern authentication works.</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">	PCs must either be domain joined, or be enrolled in Intune and compliant.</caps:sentence>
                        <caps:sentence id="src107" class="srcSentence"> You can set the following requirements:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src108" class="srcSentence">
                              <ui>Devices must be domain joined or compliant.</ui>  This means that the PCs must either be domain joined or compliant with the policies set in <token>wit_nextref</token>.</caps:sentence>
                            <caps:sentence id="src109" class="srcSentence"> If the PC does not meet either of these requirements, the user is prompted to enroll the device with <token>wit_nextref</token>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src110" class="srcSentence">
                              <ui>Devices must be domain joined.</ui> This means that the PCs must be domain joined to access Exchange Online.</caps:sentence>
                            <caps:sentence id="src111" class="srcSentence"> If the PC is not domain joined access to email is blocked and the user is prompted to contact the IT admin.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src112" class="srcSentence">
                              <ui>Devices must be compliant.</ui> This means that the PCs must be enrolled in <token>wit_nextref</token> and compliant.</caps:sentence>
                            <caps:sentence id="src113" class="srcSentence"> If the PC is not enrolled, a message with instructions on how to enroll is displayed.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src114" class="srcSentence">Under <ui>Exchange ActiveSync mail apps</ui>, you can choose to block email from accessing Exchange Online if the device is noncompliant, and select whether to allow or block access to email when Microsoft Intune cannot manage the device.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src115" class="srcSentence">Under <ui>Targeted Groups</ui>, select the Active Directory security groups of users to which the policy will apply.</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src116" class="srcSentence">For users that are in the Targeted groups, the Intune polices will replace Exchange rules and policies.</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence id="src117" class="srcSentence">Exchange will only enforce Exchange allow, block and quarantine rules, and Exchange policies if:</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence id="src118" class="srcSentence">
	The user is not licensed for Intune.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence id="src119" class="srcSentence">The user is licensed for Intune, but the user does not belong to any security groups targeted in the conditional access policy.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">Under <ui>Exempted Groups</ui>, select the Active Directory security groups of users that are exempt from this policy.</caps:sentence>
                        <caps:sentence id="src121" class="srcSentence"> If a user  is in both the targeted and exempted groups, they will be exempt from the policy.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src122" class="srcSentence">Under <ui>Unsupported Platforms</ui>, select whether to allow or block access to email when  <token>wit_firstref</token> cannot manage the device, and the device is managed by Exchange ActiveSync.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src123" class="srcSentence">When you are done, click <ui>Save</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence id="src124" class="srcSentence">You do not have to deploy the conditional access policy, it takes effect immediately.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src125" class="srcSentence">After a user creates an email account, the device is blocked immediately.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src126" class="srcSentence">If a blocked user enrolls the device with <token>wit_nextref</token> (or remediates noncompliance), email access is unblocked within 2 minutes.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src127" class="srcSentence">If the user un-enrolls their device, email is blocked after around 24 hours.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </content>
                </conclusion>
              </procedure>
            </content>
            <sections></sections>
          </section>
          <section>
            <title>
              <caps:sentence id="src128" class="srcSentence">For Exchange on-premises (and tenants in the legacy Exchange Online Dedicated environment)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src129" class="srcSentence">The following flow is used by conditional access policies for Exchange on-premises and tenants in the legacy Exchange Online Dedicated environment to evaluate whether to allow or block devices.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="7977d51d-3541-4666-a3d4-3864e112790b"></image>
              </mediaLink>
              <procedure expanded="true">
                <title>
                  <caps:sentence id="src130" class="srcSentence">To enable the Exchange On-premises policy</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src131" class="srcSentence">In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Conditional Access</ui> &gt; <ui>Exchange On-premises policy</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src132" class="srcSentence">Configure the policy with the settings you require:</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src133" class="srcSentence">Setting</caps:sentence>
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
                                <ui>
                                  <caps:sentence id="src135" class="srcSentence">Block email apps from accessing Exchange On-premises if the device is noncompliant or not enrolled to Microsoft Intune</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src136" class="srcSentence">When you select this option, devices that are not managed by <token>wit_nextref</token> or are not compliant with a compliance policy that was deployed to them are blocked from accessing Exchange services unless they have been defined as exempt.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src137" class="srcSentence">Default rule override - Always allow  enrolled and compliant devices to access Exchange</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src138" class="srcSentence">When you check this option, devices that are enrolled in Intune and compliant with the compliant policies are allowed to access Exchange.</caps:sentence>
                                <caps:sentence id="src139" class="srcSentence">  This rule overrides the <ui>Default Rule</ui>, which means that even if you set the <ui>Default Rule</ui> to quarantine or block access, enrolled and compliant devices will still be able to access Exchange.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src140" class="srcSentence">Targeted Groups</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src141" class="srcSentence">Select the <token>wit_nextref</token> user groups that must enroll their device with <token>wit_nextref</token> before they can access Exchange.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src142" class="srcSentence">Exempted Groups</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src143" class="srcSentence">Select the <token>wit_nextref</token> user groups that are exempt from the conditional access policy.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src144" class="srcSentence">Settings in this list override those in the <ui>Targeted Groups</ui> list.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src145" class="srcSentence">Platform Exceptions</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src146" class="srcSentence">Click <ui>Add Rule</ui> to configure a rule that defines access levels for specified mobile device families and models.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src147" class="srcSentence">Because these devices can be of any type, you can also configure device types that are unsupported by <token>wit_nextref</token>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src148" class="srcSentence">Default Rule</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src149" class="srcSentence">For a device that is not covered by any of the other rules, you can choose to allow it to access Exchange, block it, or quarantine it.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src150" class="srcSentence">When you set the rule to allow access, for devices that are enrolled and compliant, email access is granted automatically for iOS, Windows, and Samsung Knox devices.</caps:sentence>
                                <caps:sentence id="src151" class="srcSentence"> The end-user does not have to go through any process to get their email.</caps:sentence>
                                <caps:sentence id="src152" class="srcSentence">  On Android devices that are not Knox based, end-users will get a quarantine email which includes a guided walkthrough to verify enrollment and compliance before they can access email.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src153" class="srcSentence">If you set the rule to block access or quarantine it, all devices are blocked from getting access to exchange regardless of whether they are already enrolled in Intune or not.</caps:sentence>
                                <caps:sentence id="src154" class="srcSentence"> To prevent enrolled and compliant devices from being affected by this rule, check the <ui>Default Rule Override.</ui></caps:sentence>
                              </para>
                              <alert class="tip">
                                <para>
                                  <caps:sentence id="src155" class="srcSentence">If you intention is to first block all devices before granting access to email, checking the Block access, or Quarantine rule can be useful.</caps:sentence>
                                </para>
                              </alert>
                              <para>
                                <caps:sentence id="src156" class="srcSentence">The default rule will apply to all device types, so device types you configure as platform exceptions and that are unsupported by <token>wit_nextref</token> are also affected.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src157" class="srcSentence">User Notification</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src158" class="srcSentence">In addition to the notification email sent from Exchange, Intune sends an email that you can configure which contains steps to unblock the device.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src159" class="srcSentence">You can edit the default message and use HTML tags to format how the text appears.</caps:sentence>
                              </para>
                              <alert class="note">
                                <para>
                                  <caps:sentence id="src160" class="srcSentence">Because the Intune notification email containing remediation instructions is delivered to the user’s Exchange mailbox, in the event that the user’s device gets blocked before they receive the email message, they can use an unblocked device or other method to access Exchange and view the message.</caps:sentence>
                                </para>
                                <para>
                                  <caps:sentence id="src161" class="srcSentence">This is especially true when the <ui>Default Rule</ui> is set to block or quarantine.</caps:sentence>
                                  <caps:sentence id="src162" class="srcSentence">  In this case, the end-user will have to go to their app store, download the Microsoft Company Portal app and enroll their device.</caps:sentence>
                                  <caps:sentence id="src163" class="srcSentence"> This is applicable to iOS, Windows, and Samsung Knox devices.</caps:sentence>
                                  <caps:sentence id="src164" class="srcSentence">  For  Android devices that are not Knox-based, the IT admin will need to send the quarantine email to an alternate email account, which then  the end-user has to copy to their blocked device to complete the enrollment and compliance process.</caps:sentence>
                                </para>
                              </alert>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src165" class="srcSentence">In order for Exchange to be able to send the notification email, you must configure the account that will be used to send the notification email.</caps:sentence>
                        </para>
                        <para>
                          <caps:sentence id="src166" class="srcSentence">For details, see <link xlink:href="eb9618d2-dc90-48be-b921-8044b7e693ac#bkmk_EX_OP">Configure Microsoft Intune on-premises connector for on-premises or hosted Exchange</link>.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src167" class="srcSentence">When you are done, click <ui>Save</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence id="src168" class="srcSentence">You do not have to deploy the conditional access policy, it takes effect immediately.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src169" class="srcSentence">After a user sets up an Exchange ActiveSync profile, it might take from 1-3 hours for the device to be blocked (if it is not managed by <token>wit_nextref</token>).</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src170" class="srcSentence">If a blocked user then enrolls the device with <token>wit_nextref</token> (or remediates noncompliance), email access will be unblocked within 2 minutes.</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src171" class="srcSentence">If the user un-enrolls from <token>wit_nextref</token> it might take from 1-3 hours for the device to be blocked.</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src172" class="srcSentence">Step 5: Monitor the compliance and conditional access policies</caps:sentence>
        </title>
        <content>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src173" class="srcSentence">To view devices that are blocked from Exchange</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src174" class="srcSentence">On the <token>wit_nextref</token> dashboard, click the <ui>Blocked Devices from Exchange</ui> tile to show the number of blocked devices and links to more information.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_Scenario">
        <title>
          <caps:sentence id="src175" class="srcSentence">Example Scenarios</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section expanded="false">
            <title>
              <caps:sentence id="src176" class="srcSentence">All iOS devices that access Exchange On-premises must be managed by Intune</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src177" class="srcSentence">In this example, the organization only uses devices that run iOS and they require that all of these devices are managed by <token>wit_nextref</token> before they can access Exchange.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src178" class="srcSentence">To accomplish this, in the conditional access policy, they configure the following:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">Select the option <ui>Enable conditional access policy for Exchange Online</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">For apps using modern authentication, select <ui>iOS</ui> for the platform</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src181" class="srcSentence">For Exchange ActiveSync apps, select <ui>Require mobile devices to be compliant </ui> and block access to email on devices that are not supported by <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">A platform exception that allows devices that run iOS to access Exchange.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">A default rule that specifies when a device is not covered by other rules, then it should be blocked.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src184" class="srcSentence">The following flow is used to decide which devices can access Exchange:</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="9306af75-8e89-46a4-a7fa-dc09107a4d0c"></image>
              </mediaLink>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src185" class="srcSentence">No Android devices can access Exchange On-premises.</caps:sentence>
              <caps:sentence id="src186" class="srcSentence"> All other devices that access Exchange must be managed by Intune</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src187" class="srcSentence">In this example, the organization does not want to allow devices that run Android access to Exchange.</caps:sentence>
                <caps:sentence id="src188" class="srcSentence"> All other supported devices can access Exchange as long as they are managed by <token>wit_nextref</token>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src189" class="srcSentence">To accomplish this, in the conditional access policy, they configure the following:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src190" class="srcSentence">Select the option <ui>Enable conditional access policy for Exchange online</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">A platform exception that blocks devices that run Android from accessing Exchange.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src192" class="srcSentence">A default rule that specifies when a device is not covered by other rules, then it should be allowed.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src193" class="srcSentence">The following flow is used to decide which devices can access Exchange:</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="59d82948-47d5-47f9-90bd-e8380d8cd152"></image>
              </mediaLink>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src194" class="srcSentence">Block users of noncompliant devices from Exchange Online in a specified Active Directory security group.</caps:sentence>
              <caps:sentence id="src195" class="srcSentence"> Exempt devices in another security group</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src196" class="srcSentence">In this scenario, all users in the <ui>Accounting</ui> Active Directory security group must be blocked from accessing Exchange Online if their device is not compliant with a compliance policy you deployed.</caps:sentence>
                <caps:sentence id="src197" class="srcSentence"> Additionally, any users in the <ui>Finance</ui> Active Directory security group must be exempt from the policy, even if they are also in the <ui>Accounting</ui> security group.</caps:sentence>
                <caps:sentence id="src198" class="srcSentence"> Finally, if any users exist in this group whose devices are not supported by <token>wit_nextref</token>, they must be blocked from accessing Exchange Online on that device.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src199" class="srcSentence">To accomplish this, in the conditional access policy, they configure the following:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">Select the option <ui>Enable conditional access for Exchange Online.</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src201" class="srcSentence">Select <ui>Accounting</ui> under <ui>Targeted Groups</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src202" class="srcSentence">Select <ui>Finance</ui> under <ui>Exempted Groups</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src203" class="srcSentence">Under <ui>Exchange ActiveSync mail apps</ui>, select <ui>Require mobile devices to be compliant</ui>option.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src204" class="srcSentence">The following flow is used to decide which devices can access Exchange:</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="0d96dec0-377a-4fa7-978d-0ff62e653d8f"></image>
              </mediaLink>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="c564d292-b83b-440d-bf08-3f5b299b7a5e">Manage access to email and SharePoint with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>