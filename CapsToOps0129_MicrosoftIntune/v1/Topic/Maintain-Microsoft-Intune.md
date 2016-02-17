---
title: Mantener Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 041e4c61-ceb9-4c6f-a853-d0444d682af8
---
# Mantener Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="f5805e437dee7a089001ec916a323623" id="tgt1" class="tgtSentence">Como servicio en nube hospedado por Microsoft, el servicio wit_nextref<token>wit_firstref</token> se mantiene automáticamente con poca intervención por parte del usuario.</caps:sentence>
          <caps:sentence sentenceid="f83e5fde75ee65d978ee8d0060cd6fb2" id="tgt2" class="tgtSentence"> No obstante, debe estar familiarizado con las tareas de mantenimiento siguientes, que podrían ser necesarias para el mantenimiento del servicio:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="041e4c61-ceb9-4c6f-a853-d0444d682af8#BKMK_Maintenance">Common maintenance tasks</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="041e4c61-ceb9-4c6f-a853-d0444d682af8#BKMK_ManagePreferences">Change your contact preferences</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="041e4c61-ceb9-4c6f-a853-d0444d682af8#BKMK_ManagePartners">Manage partner relationships</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="041e4c61-ceb9-4c6f-a853-d0444d682af8#BKMK_DecommissionIntune">Decommission your subscription</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_Maintenance">
        <title>
          <caps:sentence sentenceid="9634d9f42b11b4cdd379e025749b67bc" id="tgt3" class="tgtSentence">Tareas de mantenimiento comunes</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="478f3a4c51824ad23cb50c1c60670c0f" id="tgt4" class="tgtSentence">Tarea</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt5" class="tgtSentence">Detalles</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="a7b7b82733b2b42e9b52668890bd6825" id="tgt6" class="tgtSentence">Actualizar el servicio de <token>wit_firstref</token></caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9c5023e02a027bd32675c18ab9e97a68" id="tgt7" class="tgtSentence">
                      <token>wit_firstref</token> es un servicio en la nube y Microsoft administra actualizaciones del servicio en su nombre.</caps:sentence>
                    <caps:sentence sentenceid="b24bf1ed8beb8358d2c9baab17f4c50b" id="tgt8" class="tgtSentence"> Cada vez que usted se conecta a un portal web administrativo, se conecta a la versión más reciente disponible.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="ddf18a5b8dbabb4d9a305324795b96f0" id="tgt9" class="tgtSentence">Normalmente, las actualizaciones del servicio no causan un cambio visible.</caps:sentence>
                    <caps:sentence sentenceid="3a5bacaccd8d33ef195ff507e3bf26d6" id="tgt10" class="tgtSentence"> Sin embargo, las actualizaciones importantes se detallan en el <ui>Tablón de anuncios</ui>, que aparece al conectarse a la <token>wit_adminconsole</token> después de una actualización del servicio.</caps:sentence>
                    <caps:sentence sentenceid="c4d0a50461c6b27b06f562d0b132510c" id="tgt11" class="tgtSentence"> También puede ver los avisos en la página <ui>Aviso</ui> del área de trabajo <ui>Alertas</ui> de la <token>wit_adminconsole</token>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="37afc2413209a94828134c285f1bdb96" id="tgt12" class="tgtSentence">Cuando hay actualizaciones del software cliente, puede que se le solicite que descargue e implemente el cliente actualizado.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="4462659de4d522ffbc363a78e3f7fd9f" id="tgt13" class="tgtSentence">Consulte <externalLink><linkText>Actualizaciones del servicio de Microsoft Intune</linkText><linkUri>http://technet.microsoft.com/library/dn292747.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="596f956ec675f06cef4c7c07e69ef5db" id="tgt14" class="tgtSentence">Copia de seguridad y recuperación de los datos de <token>wit_firstref</token> en la nube</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="896d9fe03d5089a9b1dec0efdb575042" id="tgt15" class="tgtSentence">Como parte del servicio de <token>wit_nextref</token>, la infraestructura y los datos que se administran en su nombre incluyen:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d4503dec3944fe993af0fe720943ac01" id="tgt16" class="tgtSentence">Las configuraciones que realice para su instancia de <token>wit_nextref</token></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="40d4266a170230135202bb3a0535f06c" id="tgt17" class="tgtSentence">Los datos y el estado de los dispositivos que administra</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="26829411d870da73388c1ba345f15cf1" id="tgt18" class="tgtSentence">Los datos que cargue en el almacenamiento en nube, como el software que implemente y la información de licencias</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8dac2d4f88449549fb9fc8914c63f83b" id="tgt19" class="tgtSentence">Las cuentas de usuario que agregue a su instancia de Microsoft Azure AD</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="e075ef23208cb75b4d7096cd5ed65b48" id="tgt20" class="tgtSentence">Los datos que cargue para su uso con <token>wit_nextref</token> se mantienen en la nube, pero esto no elimina la necesidad de mantener una copia de seguridad local del origen de dicha información.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence sentenceid="de1364a2b677a5e84189d08529432376" id="tgt21" class="tgtSentence">Para obtener información acerca de cómo administra sus datos Microsoft, descargue el documento <externalLink><linkText>Microsoft Intune Privacy and Data Protection Overview (Información general sobre privacidad y protección de datos de Microsoft Intune)</linkText><linkUri>http://download.microsoft.com/download/C/C/8/CC8065C4-829F-4635-B731-1D39287444C0/Windows_Intune_Privacy_and_Data_Protection_Overview.pdf</linkUri></externalLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="9c7d55396f89397ea032ca961aff1fa4" id="tgt22" class="tgtSentence">Reinstalar On-Premises Exchange Connector</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a43346e381aca17cb16f808be0014903" id="tgt23" class="tgtSentence">No hay opciones de copia de seguridad o restauración de este conector.</caps:sentence>
                    <caps:sentence sentenceid="938d47a14ecc3c7563009e2c9c5265aa" id="tgt24" class="tgtSentence"> Al instalar o reinstalar este conector, la nueva instancia reemplaza cualquier conector configurado previamente.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="a282601d475e838040dcc4da21fae279" id="tgt25" class="tgtSentence">Reinstalar Service to Service Connector</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c572843eaaa125aabb2fe37b9f4f586f" id="tgt26" class="tgtSentence">La configuración de este conector se mantiene en el almacenamiento en nube y no requiere copia de seguridad ni restauración.</caps:sentence>
                    <caps:sentence sentenceid="f37fad60a4dc1f1770e149853eaf4514" id="tgt27" class="tgtSentence"> Al configurar este conector, la nueva instancia reemplaza cualquier conector configurado previamente.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="797e662016f13c75b8848fc548af01cc" id="tgt28" class="tgtSentence">Copia de seguridad de equipos y dispositivos individuales</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a9b9a1d964c280e8027fa7e04a3d9a06" id="tgt29" class="tgtSentence">
                      <token>wit_nextref</token> no administra la copia de seguridad ni la recuperación de los datos, las configuraciones o las aplicaciones de los dispositivos móviles o los equipos que usted administra con el servicio.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_ManagePreferences">
        <title>
          <caps:sentence sentenceid="ddfff1018d2b8a3f72cb13f8a649ec86" id="tgt30" class="tgtSentence">Cambiar las preferencias de contacto</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="478f3a4c51824ad23cb50c1c60670c0f" id="tgt31" class="tgtSentence">Tarea</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt32" class="tgtSentence">Detalles</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="ddfff1018d2b8a3f72cb13f8a649ec86" id="tgt33" class="tgtSentence">Cambiar las preferencias de contacto</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b3190addc5f3e3674d5991d678c9aa72" id="tgt34" class="tgtSentence">Los administradores de <token>wit_firstref</token> tienen la opción de recibir comunicaciones relacionadas con el producto de Microsoft: </caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="853ae90f0351324bd73ea615e6487517" id="tgt35" class="tgtSentence">
                      <embeddedLabel>Para administrar las comunicaciones que recibe</embeddedLabel>:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt36" class="tgtSentence">En el <externalLink><linkText>portal de cuentas de Microsoft Intune</linkText><linkUri>https://account.manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Mi perfil</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="0ac19500cb6276ca1424e20f30b4be41" id="tgt37" class="tgtSentence">Edite la sección <ui>Preferencias de contacto</ui> para proporcionar sus detalles de contacto y para seleccionar las comunicaciones que desea recibir.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt38" class="tgtSentence">Haga clic en <ui>Guardar</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="ae9de1c7a82df8e22d59014391a395c8" id="tgt39" class="tgtSentence">Seguirá recibiendo mensajes de correo electrónico relacionados con sus cuentas de servicio y facturación incluso si elige no recibir información adicional del producto.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_ManagePartners">
        <title>
          <caps:sentence sentenceid="b0c38f9b1ac30cea8ad7729079bf40fe" id="tgt40" class="tgtSentence">Administrar las relaciones con los partners</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5e901ba35003cac66481c0513f1c8028" id="tgt41" class="tgtSentence">Si actualmente no trabaja con ningún partner, puede buscar uno en el sitio web de <externalLink><linkText>Microsoft Pinpoint</linkText><linkUri>http://go.microsoft.com/fwlink/?linkid=235605</linkUri></externalLink>.</caps:sentence>
            <caps:sentence sentenceid="be385899d64dcbc893f42c45673303d2" id="tgt42" class="tgtSentence"> La disponibilidad del partner dependerá de los servicios que utilice y del país o la región donde use dichos servicios.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="478f3a4c51824ad23cb50c1c60670c0f" id="tgt43" class="tgtSentence">Tarea</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt44" class="tgtSentence">Detalles</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="75fa06d06675725075a07af1f72c1424" id="tgt45" class="tgtSentence">Administrar un partner para su suscripción</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="65140cab49b40c0ba8eb27cf27e79f85" id="tgt46" class="tgtSentence">Los partners son asesores que pueden proporcionar experiencia técnica, de soporte y ventas para ayudarle a configurar y mantener su suscripción.</caps:sentence>
                    <caps:sentence sentenceid="a3f145cd7eacdb9ec36e8a82c24739c8" id="tgt47" class="tgtSentence"> Puede agregar, cambiar o quitar un partner de Microsoft de su suscripción en cualquier momento.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="1a3c6b0ea77ff6285b98e908da13bec1" id="tgt48" class="tgtSentence">Antes de agregar o cambiar un partner para su suscripción, debe tener el id. de partner de Microsoft del partner.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="853ae90f0351324bd73ea615e6487517" id="tgt49" class="tgtSentence">
                      <embeddedLabel>Para administrar un partner para una suscripción</embeddedLabel>:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt50" class="tgtSentence">En el <externalLink><linkText>portal de cuentas de Microsoft Intune</linkText><linkUri>https://account.manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Administrar</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt51" class="tgtSentence">Haga clic en <token>wit_firstref</token>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt52" class="tgtSentence">En el panel derecho de la página <ui>Detalles de la suscripción</ui>, en <ui>Información de partner</ui>, haga clic en:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="909e0178d4f5f6ce20afb8fc7b5bbd04" id="tgt53" class="tgtSentence">
                              <ui>Agregar</ui> si está agregando un partner a su suscripción.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d3c2323db3b531d79af4ff623b3bdc73" id="tgt54" class="tgtSentence">
                              <ui>Editar</ui> si está cambiando o quitando un partner.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c54eb42f791fef08d7d7ea1d60d2adf5" id="tgt55" class="tgtSentence">Actualizar la información para el <ui>id. de partner de Microsoft</ui>:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0d82fde330a7771df01531b44a4a217b" id="tgt56" class="tgtSentence">Para agregar o cambiar un partner, escriba el id. de partner del partner con el cual quiere trabajar.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="21d3e7641f7f0b8c9b15fb4f80214f0d" id="tgt57" class="tgtSentence">Para quitar un partner, borre el id. de partner</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt58" class="tgtSentence">Haga clic en <ui>Aceptar</ui> para guardar el cambio.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="04f5215ecceb82a20cdf8e137150c2f1" id="tgt59" class="tgtSentence">Gestionar un administrador delegado</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="16e240cc8d12ce76793a86532e6e12ab" id="tgt60" class="tgtSentence">Al suscribirse a <token>wit_nextref</token>, está dando permisos de administrador y puede asignar permisos de administrador a otros usuarios de su empresa.</caps:sentence>
                    <caps:sentence sentenceid="f18c6e23ff107cbb6da13ff6be66c851" id="tgt61" class="tgtSentence"> Sin embargo, si desea que otra persona administre el servicio, puede delegar este rol en un partner de Microsoft.</caps:sentence>
                    <caps:sentence sentenceid="9aac644de60d05ea06128fc5348c53f0" id="tgt62" class="tgtSentence"> Cuando autoriza a un partner a asumir esta función, se le denomina <legacyItalic>administrador delegado</legacyItalic>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="8c499fa96d5cd924c908eafc018b9bb1" id="tgt63" class="tgtSentence">
                      <embeddedLabel>Agregar un administrador delegado</embeddedLabel>: este proceso se debe iniciar por su partner de Microsoft.</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="92ad2600bd1395711d878500877d76da" id="tgt64" class="tgtSentence">El partner envía un mensaje de correo electrónico preguntándole si desea otorgarles permisos para que actúen como un administrador delegado.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="e4058d29f48618ab9da6019adbda39c3" id="tgt65" class="tgtSentence">Lea las condiciones del partner en el mensaje de correo electrónico.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="9400e493b23d21c62a7b4cdedcf824e3" id="tgt66" class="tgtSentence">Para autorizar el acuerdo, haga clic en el vínculo proporcionado con el mensaje, que le llevará a una página de autorización.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="853ae90f0351324bd73ea615e6487517" id="tgt67" class="tgtSentence">
                      <embeddedLabel>Ver sus administradores delegados</embeddedLabel>:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt68" class="tgtSentence">En el <externalLink><linkText>portal de cuentas de Microsoft Intune</linkText><linkUri>https://account.manage.microsoft.com/</linkUri></externalLink>, en <ui>Soporte</ui>, haga clic en <ui>Información general</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt69" class="tgtSentence">En la página <ui>Introducción al soporte técnico</ui>, en <ui>Administradores delegados</ui>, haga clic en <ui>Administrar administradores delegados</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="853ae90f0351324bd73ea615e6487517" id="tgt70" class="tgtSentence">
                      <embeddedLabel>Quitar un administrador delegado</embeddedLabel>:</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="3127149d96007355c0d9f58460fbb218" id="tgt71" class="tgtSentence">Al quitar un administrador delegado, quita los permisos del partner para tener acceso a su servicio y modificarlo.</caps:sentence>
                    <caps:sentence sentenceid="ac0b4ebb454102b26f8c2e1ce6cb9a8c" id="tgt72" class="tgtSentence"> Puede quitar el administrador delegado en cualquier momento.</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt73" class="tgtSentence">En el <externalLink><linkText>portal de cuentas de Microsoft Intune</linkText><linkUri>https://account.manage.microsoft.com/</linkUri></externalLink>, en <ui>Soporte</ui>, haga clic en <ui>Información general</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt74" class="tgtSentence">En la página <ui>Introducción al soporte técnico</ui>, en <ui>Administradores delegados</ui>, haga clic en <ui>Administrar administradores delegados</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt75" class="tgtSentence">En la página <ui>Administradores delegados</ui>, seleccione el partner que desea quitar y haga clic en <ui>Quitar administrador delegado</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_DecommissionIntune">
        <title>
          <caps:sentence sentenceid="c523f59e18e1c9a44d5b2637e5518bde" id="tgt76" class="tgtSentence">Cancelar la suscripción</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6bc786c444da504f240ed482e2ad05c8" id="tgt77" class="tgtSentence">Utilice la siguiente información para quitar los datos de los dispositivos y la infraestructura cuando planee dejar de utilizar <token>wit_firstref</token>.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="478f3a4c51824ad23cb50c1c60670c0f" id="tgt78" class="tgtSentence">Tarea</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt79" class="tgtSentence">Detalles</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="0eca7a954f97f3a922b592da79438faa" id="tgt80" class="tgtSentence">Cancelar la suscripción</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="591896b5ccbd34160719b17f189636f3" id="tgt81" class="tgtSentence">Para cancelar su suscripción, debe contactar con la <externalLink><linkText>Asistencia telefónica para Microsoft Intune</linkText><linkUri>http://technet.microsoft.com/library/jj839713.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="36aa87ec707637148ba311dee09de8e8" id="tgt82" class="tgtSentence">Para ayudar a proteger su privacidad, le pedimos que proporcione la siguiente información relacionada con su cuenta:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3c2d62170b7f974b2e28646aa8fb492b" id="tgt83" class="tgtSentence">La cuenta profesional o educativa que utiliza para iniciar sesión en el servicio en la nube</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="02cd0a5299a170b98aeded4ebfda68c0" id="tgt84" class="tgtSentence">El nombre y apellido del contacto principal para la organización</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4b02a9d9ad4f6feb358fcaa6e7ce7d58" id="tgt85" class="tgtSentence">El nombre de la organización tal como se muestra en su cuenta</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3956eb86b861dccfffa578891e78952b" id="tgt86" class="tgtSentence">La dirección completa de la organización</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="bc241cee38f2d03915e899ca57ddd3e9" id="tgt87" class="tgtSentence">Antes de cancelar su suscripción:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="5405a52f27d736b72a6ef23249e0791a" id="tgt88" class="tgtSentence">
                          <embeddedLabel>Quitar dominios de su servicio en la nube</embeddedLabel>:si ha agregado sus propios nombres de dominio a su organización para usarlos con <token>wit_nextref</token> debe <externalLink><linkText>quitar un dominio</linkText><linkUri>http://msdn.microsoft.com/library/azure/jj151817.aspx#bkmk_remove</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="48aca9e14cbd7f1e0db537936e17aedd" id="tgt89" class="tgtSentence">
                          <embeddedLabel>Guarde sus datos</embeddedLabel>: los datos asociados con su servicio en línea se eliminan transcurridos 90 días tras la cancelación de su suscripción.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="1ff9681ee6d17df782a0e0e8f9426396" id="tgt90" class="tgtSentence">Después de cancelar su suscripción, si cambia de opinión, puede restablecer su suscripción durante los siguientes 90 días a través de soporte técnico por teléfono.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="5966fc94c524150ea284150e0a2d9424" id="tgt91" class="tgtSentence">Quitar datos de equipos y dispositivos</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6e96051333211a596c8d55134160ef92" id="tgt92" class="tgtSentence">Cuando planee deje de utilizar el servicio para administrar un dispositivo, puede que le interese desinstalar las aplicaciones que administra con <token>wit_nextref</token>, quitar la aplicación del <token>wit_iwportal_1</token> y desinstalar el software cliente <token>wit_nextref</token> de los equipos.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="2fb6e4f5d5abfcd3efcf92d580c850d6" id="tgt93" class="tgtSentence">Normalmente, las aplicaciones y las configuraciones que introduce <token>wit_nextref</token> permanecen tras detenerse con <token>wit_nextref</token>.</caps:sentence>
                    <caps:sentence sentenceid="84a4afe01db3ea14f5bb38cd13855397" id="tgt94" class="tgtSentence"> Por lo tanto:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="f00963222ccf44fbc60c461b00d7dd85" id="tgt95" class="tgtSentence">Planee utilizar las opciones integradas para borrar los dispositivos para quitar información confidencial.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="41643783f30dc5b2ed9be177f927bbc7" id="tgt96" class="tgtSentence">Planee desinstalar las aplicaciones antes de finalizar la administración activa.</caps:sentence>
                        <caps:sentence sentenceid="84e10bb6d503ff90fe8a48059e37bc90" id="tgt97" class="tgtSentence"> El proceso de desinstalación de aplicaciones depende de cada aplicación.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="6e62b828d295da471a4a385ba49d39c0" id="tgt98" class="tgtSentence">Tenga en cuenta que la configuración guardada o aplicada anteriormente permanece en el dispositivo.</caps:sentence>
                        <caps:sentence sentenceid="b4499c759778d582d217155f543a934b" id="tgt99" class="tgtSentence"> Cuando ya no se aplican las configuraciones, el propietario del dispositivo puede cambiarlas.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="cb01f32e34c5a7f1d35f3aae2c8b7786" id="tgt100" class="tgtSentence">Para obtener información acerca de la retirada de los dispositivos de <token>wit_nextref</token>, consulte los siguientes temas:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="80219166c3d3f038c1a3799845545f82" id="tgt101" class="tgtSentence">
                          <embeddedLabel>Dispositivos móviles</embeddedLabel>: consulte <link xlink:href="8519e411-3d48-44eb-9b41-3e4fd6a93112">Help protect your data with Remote Wipe, Remote Lock, or Passcode Reset Using Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="6a215c983cfc74c80039faacdefc4f59" id="tgt102" class="tgtSentence">
                          <embeddedLabel>Equipos</embeddedLabel>: consulte la sección "Retirar un equipo", en <link xlink:href="eb912c73-54d2-4d78-ac34-3cbe825804c7">Manage Computers with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="79eabea7de6d1fcc8c1af864c7b1dc73" id="tgt103" class="tgtSentence">Quitar la infraestructura</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="09c7645416adbefd7b226e26c7880ede" id="tgt104" class="tgtSentence">
                      <token>wit_nextref</token>no tiene software o infraestructura común que usted desinstala de sus servidores.</caps:sentence>
                    <caps:sentence sentenceid="34d4b3cfc1c4c56fad5ef24f5f6ea12a" id="tgt105" class="tgtSentence"> Sin embargo, a continuación se facilitan ejemplos de herramientas opcionales que puede que utilice con <token>wit_nextref</token> que es posible desinstalar cuando ya no se utilicen en su entorno:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="1be68a16f9a3a10ccd5c5f57847e26d4" id="tgt106" class="tgtSentence">On-Premises Exchange Connector</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="da536c495b9565638f878e8046675ea0" id="tgt107" class="tgtSentence">Herramientas de sincronización de Active Directory, incluidas:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ecd37fd6e8e14532b559d7f367e2224c" id="tgt108" class="tgtSentence">Herramienta de sincronización de Active Directory</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="91b34df7340d7151c2e9e906934c5e5c" id="tgt109" class="tgtSentence">Servicios de federación de Microsoft Active Directory 2.0 (AD FS)</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="89e21e892356cf3a6b1c6d23e798c53d" id="tgt110" class="tgtSentence">Proxy de AD FS 2.0</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="5f5073aed67c5e39d2f10355e20a698b" id="tgt111" class="tgtSentence">Proveedor de identidades de terceros</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="9c1102b38fac717a85da1a13ccf8acdb" id="tgt112" class="tgtSentence">Antes de desinstalar una herramienta o una solución, asegúrese de que ya no se utilice.</caps:sentence>
                    <caps:sentence sentenceid="8012867358cf0bb5473fce8278557a58" id="tgt113" class="tgtSentence"> Por ejemplo, podría utilizar una solución como la Herramienta de sincronización de Active Directory para la sincronización de los usuarios locales con Azure AD.</caps:sentence>
                    <caps:sentence sentenceid="b071486355ab9e795a586bde481da01c" id="tgt114" class="tgtSentence"> Si sigue suscrito a otros servicios en la nube como Office 365, puede que sea necesario conservar la herramienta para que la utilice ese servicio.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence sentenceid="082691d4537fba656ff68cc228881727" id="tgt115" class="tgtSentence">Quitar datos de la nube</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7521fa7b885e813f2055a17749dd3929" id="tgt116" class="tgtSentence">Si decide cancelar la suscripción a <token>wit_nextref</token>, puede utilizar el <token>wit_icp_2</token> y la <token>wit_adminconsole</token> para quitar de forma activa la información y los datos que almacena en la nube.</caps:sentence>
                    <caps:sentence sentenceid="5045ab49244d724bd9a0073514babc67" id="tgt117" class="tgtSentence"> Estos datos pueden incluir su información de dispositivo y usuario, el software que cargó para implementar en los dispositivos y las configuraciones personalizadas como los grupos y los informes.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="e35664e82dc54e471f8092c76379ad06" id="tgt118" class="tgtSentence">Si no quita sus datos de la nube antes de que finalice su suscripción, se abre un período de gracia de 90 días para los datos durante el cual puede seguir accediendo a los mismos, así como seguir administrándolos, en <token>wit_nextref</token>.</caps:sentence>
                    <caps:sentence sentenceid="29754e751609e2ea8823d5524e73d55a" id="tgt119" class="tgtSentence"> Sin embargo, durante este período de gracia no puede administrar los dispositivos utilizando el servicio.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="2d5d986485983bb86709703f2aee5952" id="tgt120" class="tgtSentence">Una vez que expira el período de gracia, Microsoft elimina todas las instancias de sus datos automáticamente, y esa información deja de estar disponible.</caps:sentence>
                    <caps:sentence sentenceid="a62668f43e58cb8637c83df86304766d" id="tgt121" class="tgtSentence"> Para obtener más información, consulte Data disposition (Disposición de los datos) en el documento <externalLink><linkText>Microsoft Intune Privacy and Data Protection Overview (Información general sobre privacidad y protección de datos de Microsoft Intune)</linkText><linkUri>http://download.microsoft.com/download/C/C/8/CC8065C4-829F-4635-B731-1D39287444C0/Windows_Intune_Privacy_and_Data_Protection_Overview.pdf</linkUri></externalLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
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
          <caps:sentence id="src1" class="srcSentence">As a cloud service hosted by Microsoft, the <token>wit_firstref</token> service is maintained automatically with little maintenance required by you.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> However, you should be familiar with the following maintenance tasks that might be required to maintain your service:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="041e4c61-ceb9-4c6f-a853-d0444d682af8#BKMK_Maintenance">Common maintenance tasks</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="041e4c61-ceb9-4c6f-a853-d0444d682af8#BKMK_ManagePreferences">Change your contact preferences</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="041e4c61-ceb9-4c6f-a853-d0444d682af8#BKMK_ManagePartners">Manage partner relationships</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="041e4c61-ceb9-4c6f-a853-d0444d682af8#BKMK_DecommissionIntune">Decommission your subscription</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_Maintenance">
        <title>
          <caps:sentence id="src3" class="srcSentence">Common maintenance tasks</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src4" class="srcSentence">Task</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">Details</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src6" class="srcSentence">Update the <token>wit_firstref</token> service</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">
                      <token>wit_firstref</token> is a cloud service, and Microsoft manages service updates for you.</caps:sentence>
                    <caps:sentence id="src8" class="srcSentence"> Each time you connect to an administrative web portal, you connect to the most current version available.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">Typically, service updates do not cause a visible change.</caps:sentence>
                    <caps:sentence id="src10" class="srcSentence"> However, important updates are detailed in the <ui>Notice</ui> board, which is displayed when you connect to the <token>wit_adminconsole</token> after a service update.</caps:sentence>
                    <caps:sentence id="src11" class="srcSentence"> You can also view notices on the <ui>Notice</ui> page of the <ui>Alerts</ui> workspace of the <token>wit_adminconsole</token>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">When there are updates to the client software, you might be prompted to download and deploy the updated client.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">See <externalLink><linkText>Microsoft Intune Service Updates</linkText><linkUri>http://technet.microsoft.com/library/dn292747.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src14" class="srcSentence">Back up and recover <token>wit_firstref</token> data in the cloud</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">As part of the <token>wit_nextref</token> service, the infrastructure and data that is managed for you includes:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src16" class="srcSentence">Configurations you make for your instance of <token>wit_nextref</token></caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src17" class="srcSentence">Data and status from the devices you manage</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src18" class="srcSentence">Data you upload to the cloud storage, such as software you deploy and license information</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src19" class="srcSentence">User accounts that you add to your instance of Microsoft Azure AD</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src20" class="srcSentence">Data you upload for use with <token>wit_nextref</token> is maintained in the cloud but does not replace the need to maintain an on-premises backup for the source of that information.</caps:sentence>
                    </para>
                  </alert>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">For information about how Microsoft manages your data, download the <externalLink><linkText>Microsoft Intune Privacy and Data Protection Overview</linkText><linkUri>http://download.microsoft.com/download/C/C/8/CC8065C4-829F-4635-B731-1D39287444C0/Windows_Intune_Privacy_and_Data_Protection_Overview.pdf</linkUri></externalLink> white paper.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src22" class="srcSentence">Reinstall the On-Premises Exchange Connector</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">There are no options to back up or restore this connector.</caps:sentence>
                    <caps:sentence id="src24" class="srcSentence"> When you install or reinstall this connector, the new instance replaces any previously configured connector.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src25" class="srcSentence">Reinstall the Service to Service Connector</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">The configuration of this connector is maintained in your cloud storage and does not require backup or restoration.</caps:sentence>
                    <caps:sentence id="src27" class="srcSentence"> When you configure this connector, the new instance replaces any previously configured connector.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src28" class="srcSentence">Back up individual devices and computers</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">
                      <token>wit_nextref</token> does not manage the backup or recovery for data, settings, or applications on mobile devices or computers that you manage with the service.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_ManagePreferences">
        <title>
          <caps:sentence id="src30" class="srcSentence">Change your contact preferences</caps:sentence>
        </title>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">Task</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">Details</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src33" class="srcSentence">Change your contact preferences</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Administrators for <token>wit_firstref</token> have the option to receive product-related communications from Microsoft: </caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">
                      <embeddedLabel>To manage the communications you receive</embeddedLabel>:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">In the <externalLink><linkText>Microsoft Intune account portal</linkText><linkUri>https://account.manage.microsoft.com/</linkUri></externalLink>, click <ui>My profile</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">Edit the <ui>Contact preferences</ui> section to provide your contact details and to select the communications you want to receive.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">Click <ui>Save</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">You will continue to receive email messages related to your billing and service accounts even if you choose not to receive additional product information.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_ManagePartners">
        <title>
          <caps:sentence id="src40" class="srcSentence">Manage partner relationships</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src41" class="srcSentence">If you do not currently work with a partner, you can find one on the <externalLink><linkText>Microsoft Pinpoint</linkText><linkUri>http://go.microsoft.com/fwlink/?linkid=235605</linkUri></externalLink> website.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> Partner availability depends on the services you use and the country or region where you will use those services.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Task</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Details</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src45" class="srcSentence">Manage a Partner for your subscription</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">Partners are advisors who can provide sales, support, and technical expertise to help you set up and maintain your subscription.</caps:sentence>
                    <caps:sentence id="src47" class="srcSentence"> You can add, change, or remove a Microsoft partner from your subscription at any time.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Before you add or change a partner for your subscription, you must have the partner’s Microsoft Partner ID.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">
                      <embeddedLabel>To manage a partner for a subscription</embeddedLabel>:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">In the <externalLink><linkText>Microsoft Intune account portal</linkText><linkUri>https://account.manage.microsoft.com/</linkUri></externalLink>, click <ui>Manage</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">Click <token>wit_firstref</token>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">On the <ui>Subscription details</ui> page, in the right pane under <ui>Partner information</ui>, click:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src53" class="srcSentence">
                              <ui>Add</ui> if you are adding a partner to your subscription.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src54" class="srcSentence">
                              <ui>Edit</ui> if you are changing or removing a partner.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src55" class="srcSentence">Update the information for <ui>Microsoft partner ID</ui>:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src56" class="srcSentence">To add or change a partner, enter the Partner ID of the partner you want to work with.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src57" class="srcSentence">To remove a partner, clear the Partner ID</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">Click <ui>OK</ui> to save the change.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src59" class="srcSentence">Manage a delegated administrator</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src60" class="srcSentence">When you subscribe to <token>wit_nextref</token>, you are given administrator permissions and can assign administrator permissions to other users in your company.</caps:sentence>
                    <caps:sentence id="src61" class="srcSentence"> However, when you want someone else to administer the service, you can delegate this role to a Microsoft partner.</caps:sentence>
                    <caps:sentence id="src62" class="srcSentence"> When you authorize a partner to take on this role, the partner is referred to as a <legacyItalic>delegated administrator</legacyItalic>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">
                      <embeddedLabel>Add a delegated administrator</embeddedLabel>: This process must be initiated by your Microsoft partner.</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">The partner sends you an email message asking you if you want to give them permissions to act as a delegated administrator.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src65" class="srcSentence">Read the partner's terms in the email message.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">To authorize the agreement, click the link provided in the message, which will take you to an authorization page.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">
                      <embeddedLabel>View your delegated administrators</embeddedLabel>:</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">In the <externalLink><linkText>Microsoft Intune account portal</linkText><linkUri>https://account.manage.microsoft.com/</linkUri></externalLink>, under <ui>Support</ui>, click <ui>Overview</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">On the <ui>Support overview</ui> page, under <ui>Delegated administrators</ui>, click <ui>Manage your delegated administrators</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src70" class="srcSentence">
                      <embeddedLabel>Remove a delegated administrator</embeddedLabel>:</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">When you remove a delegated administrator, you remove the partner’s permissions to access and modify your service.</caps:sentence>
                    <caps:sentence id="src72" class="srcSentence"> You can remove the delegated partner at any time.</caps:sentence>
                  </para>
                  <list class="ordered">
                    <listItem>
                      <para>
                        <caps:sentence id="src73" class="srcSentence">In the <externalLink><linkText>Microsoft Intune account portal</linkText><linkUri>https://account.manage.microsoft.com/</linkUri></externalLink>, under <ui>Support</ui>, click <ui>Overview</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">On the <ui>Support overview</ui> page, under <ui>Delegated administrators</ui>, click <ui>Manage your delegated administrators</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src75" class="srcSentence">On the <ui>Delegated administrators</ui> page, select the partner that you want to remove and click <ui>Remove delegated administrator</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <section address="BKMK_DecommissionIntune">
        <title>
          <caps:sentence id="src76" class="srcSentence">Decommission your subscription</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src77" class="srcSentence">Use the following information to remove data from devices and your infrastructure when you plan to no longer use <token>wit_firstref</token>.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">Task</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">Details</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src80" class="srcSentence">Cancel your subscription</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src81" class="srcSentence">To cancel your subscription, you must <externalLink><linkText>Contact Assisted Phone Support for Microsoft Intune</linkText><linkUri>http://technet.microsoft.com/library/jj839713.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">To help protect your privacy, we ask you to provide the following information regarding your account:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src83" class="srcSentence">The work or school account you use to sign in to the cloud service</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src84" class="srcSentence">The first and last name of the primary contact for your organization</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src85" class="srcSentence">The name of your organization as it shows on your account</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">The complete street address of your organization</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">Before you cancel your subscription:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">
                          <embeddedLabel>Remove domains from your cloud service</embeddedLabel>: If you added your own domain names for your organization to use with <token>wit_nextref</token>, you need to <externalLink><linkText>Remove a domain</linkText><linkUri>http://msdn.microsoft.com/library/azure/jj151817.aspx#bkmk_remove</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">
                          <embeddedLabel>Save your data</embeddedLabel>: The data associated with your online service is deleted 90 days after you cancel your subscription.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src90" class="srcSentence">After your subscription is canceled, if you change your mind, you can reinstate your subscription within 90 days by contacting Support by phone.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src91" class="srcSentence">Remove data from devices and computers</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src92" class="srcSentence">When you plan to no longer use the service to manage a device, you might want to uninstall the applications you manage with <token>wit_nextref</token>, remove the <token>wit_iwportal_1</token> app, and uninstall the <token>wit_nextref</token> client software from computers.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">Typically, applications and configurations that are introduced by <token>wit_nextref</token> remain in place after you stop using <token>wit_nextref</token>.</caps:sentence>
                    <caps:sentence id="src94" class="srcSentence"> Therefore:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">Plan to use the built-in options to wipe devices to remove sensitive information.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src96" class="srcSentence">Plan to uninstall applications before ending active management.</caps:sentence>
                        <caps:sentence id="src97" class="srcSentence"> The process to uninstall applications is app-specific.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src98" class="srcSentence">Be aware that settings previously enforced or set by remain in place on the device.</caps:sentence>
                        <caps:sentence id="src99" class="srcSentence"> When the settings are no longer enforced, they can be changed by the owner of the device.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">For information about retiring devices from <token>wit_nextref</token>, see the following topics:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">
                          <embeddedLabel>Mobile devices</embeddedLabel>: See <link xlink:href="8519e411-3d48-44eb-9b41-3e4fd6a93112">Help protect your data with Remote Wipe, Remote Lock, or Passcode Reset Using Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">
                          <embeddedLabel>Computers</embeddedLabel>: See the "To retire a computer" section in <link xlink:href="eb912c73-54d2-4d78-ac34-3cbe825804c7">Manage Computers with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src103" class="srcSentence">Remove infrastructure</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">
                      <token>wit_nextref</token>has no common infrastructure or software that you uninstall from your servers.</caps:sentence>
                    <caps:sentence id="src105" class="srcSentence"> However, the following are examples of optional tools you might use with <token>wit_nextref</token> that you can uninstall when no longer used in your environment:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">On-Premises Exchange Connector</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">Tools for Active Directory synchronization, including:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src108" class="srcSentence">Directory Sync tool</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src109" class="srcSentence">Microsoft Active Directory Federation Services 2.0 (AD FS)</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src110" class="srcSentence">AD FS 2.0 Proxy</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src111" class="srcSentence">Third-party Identity Provider</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">Before uninstalling a tool or solution, ensure it is no longer in use.</caps:sentence>
                    <caps:sentence id="src113" class="srcSentence"> For example, you might use a solution such as the Active Directory Sync Tool to synchronize your local users with Azure AD.</caps:sentence>
                    <caps:sentence id="src114" class="srcSentence"> If you continue to subscribe to other cloud services like Office 365, you might need to retain the tool for use by that service.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <embeddedLabel>
                      <caps:sentence id="src115" class="srcSentence">Remove data from the cloud</caps:sentence>
                    </embeddedLabel>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">When you choose to no longer subscribe to <token>wit_nextref</token>, you can use the <token>wit_icp_2</token> and <token>wit_adminconsole</token> to actively remove information and data you store in the cloud.</caps:sentence>
                    <caps:sentence id="src117" class="srcSentence"> This data can include your user and device information, software you uploaded to deploy to devices, and custom configurations such as groups and reports.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src118" class="srcSentence">If you do not remove your data from the cloud before your subscription ends, it enters a 90-day grace period during which you can continue to access and manage your data in <token>wit_nextref</token>.</caps:sentence>
                    <caps:sentence id="src119" class="srcSentence"> However, during this grace period, you cannot manage devices by using the service.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">After the grace period expires, Microsoft deletes all instances of your data automatically, and that information is no longer available.</caps:sentence>
                    <caps:sentence id="src121" class="srcSentence"> For more information, see “Data disposition” in the <externalLink><linkText>Microsoft Intune Privacy and Data Protection Overview</linkText><linkUri>http://download.microsoft.com/download/C/C/8/CC8065C4-829F-4635-B731-1D39287444C0/Windows_Intune_Privacy_and_Data_Protection_Overview.pdf</linkUri></externalLink> white paper.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="110cbdbf-8f9b-4c1b-9e3e-184113cd711c">Technical reference for Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>