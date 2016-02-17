---
title: Utilizar grupos para administrar usuarios y dispositivos en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5
---
# Utilizar grupos para administrar usuarios y dispositivos en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="2865b0e8d472ad50643cf057958b8356" id="tgt1" class="tgtSentence">Los <ui>grupos</ui> de <token>wit_firstref</token> ofrecen una gran flexibilidad para administrar los dispositivos y usuarios.</caps:sentence>
          <caps:sentence sentenceid="a2941fecdb88c9d4a15d46760b987c69" id="tgt2" class="tgtSentence"> Puede configurar los grupos según sus necesidades de organización (por ejemplo, por ubicación geográfica, departamento o características de hardware).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="c66ed83d559ae7e09a9da3cb392c2cbf" id="tgt3" class="tgtSentence">Además, puede filtrar grupos para permitir que los administradores de TI solo tengan permiso para realizar operaciones en los grupos que especifique.</caps:sentence>
          <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt4" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5#BKMK_Filter">Use filtered group views to help secure and manage users and devices</link> en este tema.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="60af7c40d909bad6a3b2c4901b8bd63d" id="tgt5" class="tgtSentence">Para crear y administrar grupos, se utiliza el área de trabajo <ui>Grupos</ui> de la <token>wit_adminconsole</token>.</caps:sentence>
          <caps:sentence sentenceid="90adbbe7112a5ab0269194573e650cc6" id="tgt6" class="tgtSentence"> La página <ui>Información general de grupos</ui> contiene resúmenes de estado que le ayudan a identificar y clasificar por orden de prioridad los asuntos que requieren su atención en relación con:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="abca7cba75e5a9ff86b1490f32891f82" id="tgt7" class="tgtSentence">Alertas</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4a9f9e77a2dbe1ee49e693c3b4cc0e98" id="tgt8" class="tgtSentence">Actualizaciones de software</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <token>epshort</token>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f4af8b5789576c000ce9105b25609bd6" id="tgt9" class="tgtSentence">Directiva</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="1386b728116df9b8782d89fe3a6a37e1" id="tgt10" class="tgtSentence">Administración de software</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="61c2881c52bd9b5819b4c62d5fd4fdac" id="tgt11" class="tgtSentence">Además, se muestra una vista jerárquica de los grupos que le permite ver los resúmenes de estado, así como identificar y resolver problemas de los miembros de un grupo seleccionado.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="488523b34732d5e69070f219d736d6da" id="tgt12" class="tgtSentence">
            <token>wit_nextref</token> proporciona nueve grupos integrados que no se pueden editar ni eliminar:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <ui>
                <caps:sentence sentenceid="6c018b0fe727e93f53c7a15bb4ae203e" id="tgt13" class="tgtSentence">Todos los usuarios</caps:sentence>
              </ui>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <ui>
                    <caps:sentence sentenceid="e296d1fa154fed1e8d0f2a7c3bb732bb" id="tgt14" class="tgtSentence">Usuarios no agrupados</caps:sentence>
                  </ui>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <ui>
                <caps:sentence sentenceid="57985c764d775128b5ac85f37d6336c2" id="tgt15" class="tgtSentence">Todos los dispositivos</caps:sentence>
              </ui>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <ui>
                    <caps:sentence sentenceid="2f4b743a3e49c321151e6a560b8a0292" id="tgt16" class="tgtSentence">Todos los equipos</caps:sentence>
                  </ui>
                </para>
              </listItem>
              <listItem>
                <para>
                  <ui>
                    <caps:sentence sentenceid="567d16323fbaf5d69e31830da46f463d" id="tgt17" class="tgtSentence">Todos los dispositivos móviles</caps:sentence>
                  </ui>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <ui>
                        <caps:sentence sentenceid="c647763b61af30a25160ab8d543545eb" id="tgt18" class="tgtSentence">Todos los dispositivos administrados directamente</caps:sentence>
                      </ui>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <ui>
                        <caps:sentence sentenceid="7e3c3cf850960e35ef410e708fa873c9" id="tgt19" class="tgtSentence">Todos los dispositivos administrados por Exchange ActiveSync</caps:sentence>
                      </ui>
                    </para>
                  </listItem>
                </list>
              </listItem>
              <listItem>
                <para>
                  <ui>
                    <caps:sentence sentenceid="5a89ac5181ddf937d9accc277057ff9b" id="tgt20" class="tgtSentence">Todos los dispositivos propiedad de la empresa</caps:sentence>
                  </ui>
                </para>
              </listItem>
              <listItem>
                <para>
                  <ui>
                    <caps:sentence sentenceid="1ce8072a573d267e887cf5cfe66a473e" id="tgt21" class="tgtSentence">Dispositivos no agrupados</caps:sentence>
                  </ui>
                </para>
              </listItem>
            </list>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="f6dbc1ec0ed4d6c96e20cbf2714aa9cc" id="tgt22" class="tgtSentence">Pertenencias a grupos</caps:sentence>
        </title>
        <content>
          <para></para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="548c91d121d0c636df24a1cff130ea97" id="tgt23" class="tgtSentence">Un grupo puede contener o bien usuarios o bien dispositivos, pero no ambos.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="90c04273a2a86b6e0c0e8a8b0334fc55" id="tgt24" class="tgtSentence">
                      <embeddedLabel>Grupos de dispositivos:</embeddedLabel> aquí se incluyen equipos y dispositivos móviles.</caps:sentence>
                    <caps:sentence sentenceid="3d6b76cfdc5ac6db60f3a9d9b1fee984" id="tgt25" class="tgtSentence"> Para poder agregar un equipo a un grupo, debe inscribirse.</caps:sentence>
                    <caps:sentence sentenceid="d55203021b27af6b5f10a766d1dc8b91" id="tgt26" class="tgtSentence"> Para poder agregar un dispositivo móvil a un grupo, su entorno debe configurarse para admitir dispositivos móviles, y los dispositivos deben inscribirse, o detectarse desde Exchange ActiveSync.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c6d79c2a88c082485bd56cb8572a3e3b" id="tgt27" class="tgtSentence">
                      <embeddedLabel>Grupos de usuarios:</embeddedLabel> un grupo puede contener usuarios de grupos de seguridad, que son grupos que se sincronizan desde Active Directory.</caps:sentence>
                    <caps:sentence sentenceid="2970e60a4a565f16c424837724e8de2f" id="tgt28" class="tgtSentence"> Si no utiliza la sincronización de Active Directory, puede crear estos grupos manualmente.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="58ca5c8eda6dd96572845e5a169fc608" id="tgt29" class="tgtSentence">Un dispositivo o un usuario pueden pertenecer a más de un grupo.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5354987d9c48a0b8ea80bef7e13faad8" id="tgt30" class="tgtSentence">Un grupo puede incluir y excluir miembros según las siguientes reglas de pertenencia:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="303961bb97270aca1685731e7d9dfb30" id="tgt31" class="tgtSentence">
                      <embeddedLabel>Criterios de pertenencia:</embeddedLabel> son reglas dinámicas que <token>wit_nextref</token> ejecuta para incluir o excluir miembros.</caps:sentence>
                    <caps:sentence sentenceid="a08d9f4e0cfce35446da81fa1d86f29f" id="tgt32" class="tgtSentence">  Estos criterios utilizan grupos de seguridad y otra información sincronizada desde su instancia local de Active Directory.</caps:sentence>
                    <caps:sentence sentenceid="fd9a8bf9c53285dceeb45b876e7c3591" id="tgt33" class="tgtSentence"> Cuando el grupo de seguridad o los datos que se sincronizan cambian, puede cambiar la pertenencia al grupo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="27fc556bd1f7c52aaab1cc014efee88f" id="tgt34" class="tgtSentence">
                      <embeddedLabel>Pertenencia directa:</embeddedLabel> son reglas estáticas que agregan o excluyen miembros explícitamente.</caps:sentence>
                    <caps:sentence sentenceid="1af4c9e9127c52c94e7077148ed9c35f" id="tgt35" class="tgtSentence"> La lista de pertenencia es estática.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="db2a3ddea3df2e4300306a537be21c32" id="tgt36" class="tgtSentence">No se necesitan los Servicios de dominio de Active Directory (AD DS) para crear grupos de usuarios o grupos de dispositivos que incluyan usuarios o equipos, pero para que los grupos de dispositivos incluyan dispositivos móviles, su entorno debe configurarse para admitir dispositivos móviles.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="95b8f9ea237fce4ec8f09e5149109348" id="tgt37" class="tgtSentence">Además, los dispositivos deben detectarse y agregarse a <token>wit_nextref</token>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="16d9d5eb5264b77b3a273ce9a05f060d" id="tgt38" class="tgtSentence">Relaciones de grupo</caps:sentence>
        </title>
        <content>
          <para></para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="7be256e8cd25038082edb1804980bfa3" id="tgt39" class="tgtSentence">Cada grupo que se cree debe tener un grupo primario y no se puede cambiar el grupo primario de un grupo una vez creado el grupo.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6fc695f41d331ed0d89acd9cdd2b687e" id="tgt40" class="tgtSentence">Cuando se agregan usuarios o dispositivos a un grupo secundario:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="51ae28a571bb4059e80acf8dfa564bff" id="tgt41" class="tgtSentence">Los grupos secundarios siempre son subconjuntos del grupo primario.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="154b484f86eb00578cbb0b9c41909270" id="tgt42" class="tgtSentence">Los nuevos miembros que se agreguen a un grupo secundario se agregan automáticamente al grupo primario del grupo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ad367ddabd0733d72b596c293a7c0bb6" id="tgt43" class="tgtSentence">No se puede agregar un miembro a un grupo secundario si ese miembro está excluido del grupo primario.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2251cb4bdee5e0402a071f1712618b3b" id="tgt44" class="tgtSentence">La pertenencia a un grupo primario define la disponibilidad de la pertenencia al grupo secundario.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="683a4e58688ec39537ad6c929cc9a70c" id="tgt45" class="tgtSentence">Cuando se elimina un grupo primario, se eliminan todos los grupos secundarios.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="77fd5ee4e84dd95fa325817a3350e577" id="tgt46" class="tgtSentence">Es posible implementar contenido y directivas en un grupo primario a la vez que se excluye la implementación en los grupos secundarios.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="6fab15e051a23c9b7d2836e01ea7a73a" id="tgt47" class="tgtSentence">Puede agregar un usuario o un dispositivo específico a un grupo secundario que no sea miembro del grupo primario.</caps:sentence>
                <caps:sentence sentenceid="95f7606e7afaad2d69090e34cb11a189" id="tgt48" class="tgtSentence"> Si lo hace, el nuevo miembro del grupo se agregará al grupo primario.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="88f3d83c58d4656de1ad35ccfecd3043" id="tgt49" class="tgtSentence">Sin embargo, no puede agregar un miembro a un grupo secundario que está excluido del grupo primario.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8df792bba2530106fc215ac723000d16" id="tgt50" class="tgtSentence">La pertenencia a grupos es recursiva.</caps:sentence>
                <caps:sentence sentenceid="4be0bb25039056347740ae85bcda324d" id="tgt51" class="tgtSentence"> Por ejemplo:</caps:sentence>
              </para>
              <list class="nobullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="340590fa48236d0164abb324fab814ad" id="tgt52" class="tgtSentence">
                      <embeddedLabel>Nuria</embeddedLabel> es miembro de un único grupo, el grupo de seguridad <ui>Usuarios de portátil</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt53" class="tgtSentence">El grupo <ui>Usuarios de portátil</ui> es miembro del grupo de seguridad <ui>Usuarios aprobados</ui>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0aafa4df0fbac9bcff8fdddc091a2858" id="tgt54" class="tgtSentence">Usted crea un grupo en <token>wit_nextref</token> que utiliza una consulta de pertenencia dinámica que incluye a los miembros del grupo <ui>Usuarios aprobados</ui>.</caps:sentence>
                    <caps:sentence sentenceid="a58474a93d0956ea33f67765648293a3" id="tgt55" class="tgtSentence"> El resultado es que su grupo de usuarios de <token>wit_nextref</token> incluye a <embeddedLabel>Nuria</embeddedLabel>.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
          <alert class="tip">
            <para>
              <caps:sentence sentenceid="c7647b48c1187d155de43cc80bdb62b8" id="tgt56" class="tgtSentence">Al crear los grupos, tenga en cuenta cómo se aplicará la directiva.</caps:sentence>
              <caps:sentence sentenceid="db68f6011d5500ce95db7ea1d101c100" id="tgt57" class="tgtSentence"> Por ejemplo, puede tener directivas específicas para sistemas operativos de dispositivos y directivas específicas para diferentes roles de la organización o para las unidades organizativas que ha definido en Active Directory.</caps:sentence>
              <caps:sentence sentenceid="6381e2b3c9cc150945962560d2b484ca" id="tgt58" class="tgtSentence"> Algunos usuarios consideran útil disponer de grupos de dispositivos específicos de iOS, Android y Windows, así como de grupos de usuarios para cada rol organizativo.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="374d1508a33a340b5c1d34476aae5659" id="tgt59" class="tgtSentence">Probablemente deseará crear una directiva predeterminada que se aplique a todos los grupos y dispositivos, para establecer los requisitos de cumplimiento básicos de la compañía.</caps:sentence>
              <caps:sentence sentenceid="8bdb11ccf0d71f30bd2e4e4137de1842" id="tgt60" class="tgtSentence"> A continuación, cree directivas más específicas para las categorías más amplias de usuarios y dispositivos como, por ejemplo, directivas de correo electrónico para el sistema operativo de cada dispositivo.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="403d37305d265277e1e57f8ff7d0c7b0" id="tgt61" class="tgtSentence">Preste atención al asignar nombres a las directivas a fin de poder identificarlas fácilmente en el futuro.</caps:sentence>
              <caps:sentence sentenceid="960a115d45e1070900621fe2bd68a6a2" id="tgt62" class="tgtSentence"> Por ejemplo, un nombre de directiva descriptivo ideal sería <ui>Directiva de correo electrónico de WP para toda la compañía</ui>.</caps:sentence>
            </para>
            <para>
              <caps:sentence sentenceid="80d0daff6c842d5a3ec4d3dd3ee11aee" id="tgt63" class="tgtSentence">Cada vez que cree una directiva restrictiva deseará comunicarla a los usuarios. Por lo tanto, después de crear directivas y grupos más generales, preste atención a la creación de grupos más pequeños para poder reducir las comunicaciones innecesarias.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5f2fd34a3f20e56b83ffbcf57a080578" id="tgt64" class="tgtSentence">Creación de grupos de Microsoft Intune</caps:sentence>
        </title>
        <content>
          <procedure address="BKMK_CreateDevGroup">
            <title>
              <caps:sentence sentenceid="a0a1e3b7748051f7cf8a0cf579ef8170" id="tgt65" class="tgtSentence">Para crear un grupo de dispositivos</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt66" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Grupos</ui> &gt; <ui>Información general</ui> &gt; <ui>Crear grupo</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="7bdedc52d3982313603ed67954cd5627" id="tgt67" class="tgtSentence">Especifique un nombre y una descripción opcional para el grupo, seleccione un grupo de dispositivos como grupo primario y, a continuación, haga clic en <ui>Siguiente</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt68" class="tgtSentence">En la página <ui>Definir criterios de pertenencia</ui>, seleccione el tipo de dispositivos que va a incluir el grupo.</caps:sentence>
                    <caps:sentence sentenceid="980eab58bb5381884f7ad6538ae1dae9" id="tgt69" class="tgtSentence"> Las opciones adicionales de configuración del grupo dependen del tipo de dispositivos que seleccione:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="6c1c4a30b9c6098978c81efe6373a4b0" id="tgt70" class="tgtSentence">
                          <embeddedLabel>Equipo:</embeddedLabel> especifique si se deben incluir todos los miembros del grupo principal, las unidades organizativas que desee incluir o excluir y los dominios que desee incluir o excluir.</caps:sentence>
                        <caps:sentence sentenceid="2126f76f50d22c7d5401bd5c6b6c4d37" id="tgt71" class="tgtSentence"> La información sobre unidades organizativas y dominios de los equipos se obtiene del inventario.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="4fc66025b4db8cef7a35ffb000484903" id="tgt72" class="tgtSentence">
                          <embeddedLabel>Móvil:</embeddedLabel> especifique si se deben incluir solo los dispositivos móviles administrados por <token>wit_nextref</token>, los administrados por Exchange ActiveSync o ambos.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="450204310bc7ccf6c7ab6c59a2847f20" id="tgt73" class="tgtSentence">
                          <embeddedLabel>Todos los dispositivos: </embeddedLabel>esta opción incluye todos los dispositivos sin exclusiones en función de criterios.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt74" class="tgtSentence">En la página <ui>Definir pertenencia directa</ui>, puede incluir o excluir los dispositivos individuales que especifique si pulsa <ui>Examinar</ui>.</caps:sentence>
                    <caps:sentence sentenceid="4654557955fa3ce9e29d0805aa3bf572" id="tgt75" class="tgtSentence"> Si utiliza esta opción para seleccionar dispositivos que no están en el grupo primario especificado, estos dispositivos se agregan automáticamente al grupo primario.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt76" class="tgtSentence">En la página <ui>Resumen</ui>, revise las acciones que se van a realizar y, a continuación, haga clic en <ui>Finalizar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="c231681212ce72647fdf71d58ea628c5" id="tgt77" class="tgtSentence">El grupo que se acaba de crear se encuentra en la lista <ui>Grupos</ui>, en el área de trabajo <ui>Grupos</ui>, en el grupo primario.</caps:sentence>
                  <caps:sentence sentenceid="9fbfdf7aa4c5de6ec931d6f9764a4c8f" id="tgt78" class="tgtSentence"> Aquí también puede editar o eliminar el grupo.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence sentenceid="eb63011b3d05731f80ab08eaab7c6bd4" id="tgt79" class="tgtSentence">Para crear un grupo de usuarios</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt80" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Grupos</ui> &gt; <ui>Información general</ui> &gt; <ui>Crear grupo</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="b916e318c8391f426f62a59b76935893" id="tgt81" class="tgtSentence">Especifique un nombre y una descripción opcional para el grupo, seleccione un grupo de usuarios como grupo primario y, a continuación, haga clic en <ui>Siguiente</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt82" class="tgtSentence">En la página <ui>Definir criterios de pertenencia</ui>, especifique si desea incluir todos los miembros del grupo primario o empezar con un grupo vacío.</caps:sentence>
                    <caps:sentence sentenceid="1a009103c51db5bf7a83a4f52d84f3b2" id="tgt83" class="tgtSentence">  Una vez hecho esto, incluya o excluya los miembros en función de los <maml:embeddedLabel xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">grupos de seguridad</maml:embeddedLabel> que configure manualmente en el portal de cuentas o que se sincronicen desde su servicio local de Active Directory.</caps:sentence>
                    <caps:sentence sentenceid="c7c8ee0a07eda8ce31290f735452f83d" id="tgt84" class="tgtSentence"> Si cambia la pertenencia de un grupo de seguridad, también puede cambiar la pertenencia de los grupos de usuarios basados en ese grupo de seguridad.</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence sentenceid="6909d6fda87bb18882774dac792d4d55" id="tgt85" class="tgtSentence">Tenga en cuenta que si el grupo incluye miembros de grupos de seguridad o administrador específicos y que si usted excluye a miembros de grupos específicos, se quitarán los miembros que incluyó en un principio.</caps:sentence>
                      <caps:sentence sentenceid="a37e577b816df6f2e5bb843892e39dc5" id="tgt86" class="tgtSentence"> Para crear un grupo que tenga tanto los miembros incluidos como los excluidos, le recomendamos que cree un grupo principal con los miembros incluidos y que, a continuación, cree un grupo secundario en el principal para enumerar ahí los miembros excluidos.</caps:sentence>
                      <caps:sentence sentenceid="24e7129337dde9d4015e60c5f01618ae" id="tgt87" class="tgtSentence"> A continuación, puede usar ese grupo secundario como le sea conveniente para distribuir directivas, perfiles y aplicaciones de Intune.</caps:sentence>
                    </para>
                  </alert>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="d5498b5beb53c5da6b899f319104c7c3" id="tgt88" class="tgtSentence">En el Portal de administración de Azure puede crear un grupo en función del administrador al cual los usuarios envían sus notificaciones.</caps:sentence>
                      <caps:sentence sentenceid="f7c764bc97a699c0f7eed68771e0212e" id="tgt89" class="tgtSentence"> El grupo será dinámico y cambiará a medida que se agreguen o se quiten empleados del equipo del administrador en Azure Active Directory.</caps:sentence>
                      <caps:sentence sentenceid="0ac8969fb2e537e529d605fcb2291439" id="tgt90" class="tgtSentence"> El procedimiento para crear un grupo de Azure basado en un administrador se describe en <externalLink><linkText>Uso de atributos para crear reglas avanzadas</linkText><linkUri>https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/</linkUri></externalLink> en la sección denominada <legacyBold>Configurar un grupo como "Administrador"</legacyBold>.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt91" class="tgtSentence">En la página <ui>Definir pertenencia directa</ui>, puede incluir o excluir los usuarios individuales que especifique si pulsa <ui>Examinar</ui>.</caps:sentence>
                    <caps:sentence sentenceid="f0e6585394e65b40b2db6b65857d1623" id="tgt92" class="tgtSentence"> Si utiliza esta opción para seleccionar usuarios que no están en el grupo primario especificado, estos dispositivos se agregan automáticamente al grupo primario.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt93" class="tgtSentence">En la página <ui>Resumen</ui>, revise las acciones que se van a realizar y, a continuación, haga clic en <ui>Finalizar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="c231681212ce72647fdf71d58ea628c5" id="tgt94" class="tgtSentence">El grupo que se acaba de crear se encuentra en la lista <ui>Grupos</ui>, en el área de trabajo <ui>Grupos</ui>, en el grupo primario.</caps:sentence>
                  <caps:sentence sentenceid="9fbfdf7aa4c5de6ec931d6f9764a4c8f" id="tgt95" class="tgtSentence"> Aquí también puede editar o eliminar el grupo.</caps:sentence>
                </para>
                <alert class="tip">
                  <para>
                    <caps:sentence sentenceid="68088e4be3db6efbefced0f4887ec79e" id="tgt96" class="tgtSentence">Los grupos de seguridad son un excelente recurso para rellenar los grupos de usuarios.</caps:sentence>
                    <caps:sentence sentenceid="33bca38788331dd5c4fea945f16777e2" id="tgt97" class="tgtSentence"> Puesto que los grupos de seguridad definen quién tiene acceso a qué recursos, se pueden convertir perfectamente en  grupos de usuarios de <token>wit_nextref</token>.</caps:sentence>
                    <caps:sentence sentenceid="533768f94e18f31428ba1ab7b9eaea71" id="tgt98" class="tgtSentence"> Los grupos de seguridad que se sincronizan desde Active Directory a Azure Active Directory, o que se crean directamente en Azure Active Directory a través del Portal de cuentas de <token>wit_nextref</token>, el Portal de administración de O365 o el portal de administración de Azure, estarán a su disposición para crear grupos de usuarios en <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </alert>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="581323a74d43182aab33df9d5af92077" id="tgt99" class="tgtSentence">Administración de los grupos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="43d3c7feaa59323d6fcae68a70961d0d" id="tgt100" class="tgtSentence">Después de crear los grupos seguirá administrándolos según las necesidades de su organización.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_Filter">
            <title>
              <caps:sentence sentenceid="95d7948818e6687fa800ac447f7c28e0" id="tgt101" class="tgtSentence">Usar vistas de grupo filtrado para ayudar a proteger y administrar usuarios y dispositivos</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="f26d996c0e9e42d4f488a941136cf3f1" id="tgt102" class="tgtSentence">Las vistas de grupos filtradas permiten restringir los grupos que cada administrador de TI puede administrar.</caps:sentence>
                <caps:sentence sentenceid="e2bc177b86e47aad6d8e29e160344295" id="tgt103" class="tgtSentence"> Esto puede resultar útil cuando:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="668c123802c824420a8d71173b5e3c8f" id="tgt104" class="tgtSentence">Los administradores de TI solo deben poder implementar elementos para dispositivos y usuarios específicos.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="da5690c5771bfdf80292e58e9f343136" id="tgt105" class="tgtSentence">Quiere mostrar solo los grupos relevantes a cada administrador de TI.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="69240bf68ba0c2c3c6e9b3484cf63d27" id="tgt106" class="tgtSentence">Puede configurar vistas de grupo filtradas para los administradores de servicios en la consola de administrador de <token>wit_nextref</token>.</caps:sentence>
                <caps:sentence sentenceid="363ddf43df695c296401df2564573a36" id="tgt107" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268">What to know before setting up Windows Intune</link>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="d133247b4febb62fd51c000f7a89a705" id="tgt108" class="tgtSentence">Después de configurar vistas de grupo filtradas para un administrador de servicios, el administrador:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3c65b72799d37eddf1d808aea6131d51" id="tgt109" class="tgtSentence">Solo puede ver y seleccionar los grupos especificados al implementar directivas o software, o al usar informes</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4a8256c817a6c96a89797e909d6125bd" id="tgt110" class="tgtSentence">No recibe información del estado de las siguientes páginas de la consola de administración:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="69770a4d9f3959e501cfe5317d57080f" id="tgt111" class="tgtSentence">Información general del sistema</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="f996bb9c459e95480a526fa7c26093a7" id="tgt112" class="tgtSentence">Información general de grupos</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="1f23187f826d95d56841711c4dd4c84e" id="tgt113" class="tgtSentence">Información general de Endpoint Protection</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ad8222cfef1bd1c86add36040acba532" id="tgt114" class="tgtSentence">Información general de alertas</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="59a7ca5b55972d7c457b92535861a83f" id="tgt115" class="tgtSentence">Información general de software</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7c1c2b1f7d4c5be333416473a7dd4272" id="tgt116" class="tgtSentence">Información general de directivas</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="3aa22b9fb080e763fa658c4473d59c64" id="tgt117" class="tgtSentence">Para configurar las vistas de grupo filtradas</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt118" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Administración de administradores</ui> &gt; <ui>Administradores de servicios</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="7b52ae8245f434321cab86ae3b91f391" id="tgt119" class="tgtSentence">Seleccione el administrador de servicios para el que desea filtrar los grupos y haga clic en <ui>Administrar grupos</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt120" class="tgtSentence">En el cuadro de diálogo <ui>Seleccione los grupos que serán visibles para este administrador de servicios</ui>, agregue los grupos a los que el administrador de servicios seleccionado podrán tener acceso y, después, haga clic en <ui>Aceptar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence sentenceid="3b6c3f39f205bdb1417b7551b19c6a95" id="tgt121" class="tgtSentence">Después de configurar las vistas de grupo filtradas, los administradores de TI podrán ver y seleccionar solo los grupos especificados.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="d60494a19592749e007a06d9999f1cd3" id="tgt122" class="tgtSentence">Otras tareas de administración para grupos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="271c5075778fd3e61dd167d3a0f37e8b" id="tgt123" class="tgtSentence">Puede editar el grupo para cambiar su nombre y descripción, así como los miembros que pertenecen al grupo.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="60d7aa1240803df4804e4bd63b27d87e" id="tgt124" class="tgtSentence">Puede eliminar un grupo que ya no satisfaga las necesidades de la organización.</caps:sentence>
            <caps:sentence sentenceid="cf3dfcafd25ccdf7b2d70e8637a11383" id="tgt125" class="tgtSentence"> Al eliminar un grupo no se eliminan los usuarios que pertenecen a este.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="c25c37dbb7186299499a1b1f7037f4d8" id="tgt126" class="tgtSentence">Grupos y directivas</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="aa1a64505a7d6d1d4043d58a37e2ad92" id="tgt127" class="tgtSentence">Una vez haya configurado los grupos y las directivas, deseará comprobar las implicaciones prácticas del diseño.</caps:sentence>
            <caps:sentence sentenceid="861611543ebc31ed4aba0cfe1836dd75" id="tgt128" class="tgtSentence"> Aquí tiene algunos consejos útiles e información sobre los grupos y las directivas.</caps:sentence>
          </para>
        </content>
        <content>
          <para>
            <caps:sentence sentenceid="9e1ee2aab4ea8857e81733eba1266523" id="tgt129" class="tgtSentence">Puede recuperar una gran cantidad de información sobre cada dispositivo administrado por <token>wit_nextref</token>.</caps:sentence>
            <caps:sentence sentenceid="85d87b25aa591f4e1e4ae57648c64c30" id="tgt130" class="tgtSentence"> Seleccione cualquier dispositivo de un grupo de dispositivos y examine las categorías de información en la parte superior de la pantalla.</caps:sentence>
            <caps:sentence sentenceid="abd9f85a722666a8f3246c8cf4258c1b" id="tgt131" class="tgtSentence"> Seleccione <ui>Directiva</ui>.</caps:sentence>
            <caps:sentence sentenceid="75cdd50b954bf0405e15daffb629c4ca" id="tgt132" class="tgtSentence"> Verá algo parecido a esta captura de pantalla de configuración de directiva de un dispositivo Android.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="3032fd32-6c3b-4e4e-bf1f-8de6e9b8bf3c"></image>
          </mediaLink>
        </content>
        <content>
          <para>
            <caps:sentence sentenceid="f1378526e6b00673a41e1a16a4c6092d" id="tgt133" class="tgtSentence">Cada directiva tiene un <ui>Valor previsto</ui> y un <ui>Estado</ui>.</caps:sentence>
            <caps:sentence sentenceid="ddf95e418805c9a659b2672aa8afef92" id="tgt134" class="tgtSentence"> El valor previsto es lo que tenía pensado lograr al asignar la directiva.</caps:sentence>
            <caps:sentence sentenceid="e44829a0b1075417d938ead5cb5adb3d" id="tgt135" class="tgtSentence"> El estado es lo que se logra realmente cuando todas las directivas aplicables al dispositivo, así como las restricciones y los requisitos del hardware y el sistema operativo, se consideran conjuntamente.</caps:sentence>
            <caps:sentence sentenceid="1a529b78f50cfe3456838b8d7dd8334f" id="tgt136" class="tgtSentence">  En la captura de pantalla se pueden ver dos ejemplos claros:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="9dc1b719ac29691cc56383ec80e5c4ec" id="tgt137" class="tgtSentence">
                  <ui>Permitir contraseñas sencillas</ui> está establecido en <ui>Sí</ui>, como se muestra en la columna <ui>Valor previsto</ui>, pero su <ui>Estado</ui> es <ui>No aplicable</ui>.</caps:sentence>
                <caps:sentence sentenceid="7b4fb4b11c4714e0a01bbce5ee86d947" id="tgt138" class="tgtSentence"> Esto es porque no se admiten contraseñas sencillas para dispositivos Android.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f8c309ae581905cb913686891e477f38" id="tgt139" class="tgtSentence">De forma similar, el elemento de directiva expandido <ui>Configuración de correo electrónico para dispositivos iOS</ui> no se aplica a este dispositivo, ya que es un dispositivo Android.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
        <content>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="604b61a544029446272926985783e200" id="tgt140" class="tgtSentence">Recuerde que cuando dos directivas con distintos niveles de restricción se aplican al mismo dispositivo o usuario, la directiva más restrictiva se aplica en la práctica.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d158503c-1276-422b-ab81-5f66c1cd7e7a">Start using Microsoft Intune</link>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="bd854e819a9550dafe0c9b715e019a4d" id="tgt141" class="tgtSentence">Cómo comprar Intune</caps:sentence>
          </linkText>
          <linkUri>http://technet.microsoft.com/en-us/library/dn646949.aspx</linkUri>
        </externalLink>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">
            <ui>Groups</ui> in <token>wit_firstref</token> give you great flexibility for managing your devices and users.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You can set up groups to suit your organizational needs (for example, by geographic location, department, or hardware characteristics).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">Additionally, you can filter groups to allow your IT admins permissions to only perform operations on the groups you specify.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> For more information, see <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5#BKMK_Filter">Use filtered group views to help secure and manage users and devices</link> in this topic.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">To create and manage groups, you use the <ui>Groups</ui> workspace in the <token>wit_adminconsole</token>.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> The <ui>Groups Overview</ui> page contains status summaries that help you identify and prioritize issues that require your attention for:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Alerts</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Software updates</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <token>epshort</token>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Policy</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">Software management</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src11" class="srcSentence">Additionally, a hierarchical view of your groups is shown that lets you view status summaries and identify and resolve problems for members of a selected group.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src12" class="srcSentence">
            <token>wit_nextref</token> provides nine built-in groups that you cannot edit or delete:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <ui>
                <caps:sentence id="src13" class="srcSentence">All Users</caps:sentence>
              </ui>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <ui>
                    <caps:sentence id="src14" class="srcSentence">Ungrouped Users</caps:sentence>
                  </ui>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <ui>
                <caps:sentence id="src15" class="srcSentence">All Devices</caps:sentence>
              </ui>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <ui>
                    <caps:sentence id="src16" class="srcSentence">All Computers</caps:sentence>
                  </ui>
                </para>
              </listItem>
              <listItem>
                <para>
                  <ui>
                    <caps:sentence id="src17" class="srcSentence">All Mobile Devices</caps:sentence>
                  </ui>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <ui>
                        <caps:sentence id="src18" class="srcSentence">All Direct Managed Devices</caps:sentence>
                      </ui>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <ui>
                        <caps:sentence id="src19" class="srcSentence">All Exchange ActiveSync Managed Devices</caps:sentence>
                      </ui>
                    </para>
                  </listItem>
                </list>
              </listItem>
              <listItem>
                <para>
                  <ui>
                    <caps:sentence id="src20" class="srcSentence">All Corporate-owned Devices</caps:sentence>
                  </ui>
                </para>
              </listItem>
              <listItem>
                <para>
                  <ui>
                    <caps:sentence id="src21" class="srcSentence">Ungrouped Devices</caps:sentence>
                  </ui>
                </para>
              </listItem>
            </list>
          </listItem>
        </list>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src22" class="srcSentence">Group memberships</caps:sentence>
        </title>
        <content>
          <para></para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">A group can contain either users or devices, but not both.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">
                      <embeddedLabel>Device groups:</embeddedLabel> This includes both computers and mobile devices.</caps:sentence>
                    <caps:sentence id="src25" class="srcSentence"> Before you can add a computer to a group, it must be enrolled.</caps:sentence>
                    <caps:sentence id="src26" class="srcSentence"> Before you can add a mobile device to a group, your environment must be configured to support mobile devices, and the devices must be enrolled, or discovered from Exchange ActiveSync.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">
                      <embeddedLabel>User groups:</embeddedLabel> A group can contain users from security groups, which are groups that synchronize from your Active Directory.</caps:sentence>
                    <caps:sentence id="src28" class="srcSentence"> If you do not use Active Directory synchronization, you can manually create these groups.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src29" class="srcSentence">A device or a user can belong to more than one group.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src30" class="srcSentence">A group can include and exclude members based on the following membership rules:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">
                      <embeddedLabel>Criteria Membership:</embeddedLabel> These are dynamic rules that <token>wit_nextref</token> runs to include or exclude members.</caps:sentence>
                    <caps:sentence id="src32" class="srcSentence">  These criteria use security groups and other information synchronized from your local Active Directory.</caps:sentence>
                    <caps:sentence id="src33" class="srcSentence"> When the security group or data that is synchronized changes, the group membership can change.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">
                      <embeddedLabel>Direct Membership:</embeddedLabel> These are static rules that explicitly add or exclude members.</caps:sentence>
                    <caps:sentence id="src35" class="srcSentence"> The membership list is static.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src36" class="srcSentence">Active Directory Domain Services (AD DS) is not required to create user groups or device groups that include users or computers, but for device groups to include mobile devices, your environment must be configured to support mobile devices.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src37" class="srcSentence">Additionally, the devices must be discovered and added to <token>wit_nextref</token>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src38" class="srcSentence">Group relationships</caps:sentence>
        </title>
        <content>
          <para></para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src39" class="srcSentence">Every group you create must have a parent group and you cannot change a group’s parent group once the group is created.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src40" class="srcSentence">When adding users or devices to a child group:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">Child groups are always subsets of the parent group.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">New members you add to a child group are automatically added to that group’s parent group.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">You cannot add a member to a child group when that member is excluded from the parent group.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src44" class="srcSentence">The membership of a parent group defines the available membership for the child group.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src45" class="srcSentence">When you delete a parent group, all child groups are deleted.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src46" class="srcSentence">You can deploy content and policies to a parent group while excluding deployment to child groups.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src47" class="srcSentence">You can add a specific user or device to a child group that is not a member of the parent group.</caps:sentence>
                <caps:sentence id="src48" class="srcSentence"> If you do so, the new group member will be added to the parent group.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src49" class="srcSentence">However, you cannot add a member to a child group that is excluded from the parent group.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src50" class="srcSentence">Group membership is recursive.</caps:sentence>
                <caps:sentence id="src51" class="srcSentence"> For example:</caps:sentence>
              </para>
              <list class="nobullet">
                <listItem>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">
                      <embeddedLabel>Pat</embeddedLabel> is a member of only one group, the <ui>Laptop Users</ui> security group.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">The <ui>Laptop Users</ui> group is a member of the <ui>Approved Users</ui> security group.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">You create a group in <token>wit_nextref</token> that uses a dynamic membership query that includes the members of the <ui>Approved Users</ui> group.</caps:sentence>
                    <caps:sentence id="src55" class="srcSentence"> The result is that your <token>wit_nextref</token> user group includes <embeddedLabel>Pat</embeddedLabel>.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
          <alert class="tip">
            <para>
              <caps:sentence id="src56" class="srcSentence">When you're creating your groups consider how you will apply policy.</caps:sentence>
              <caps:sentence id="src57" class="srcSentence"> For example, you may have policies specific to device operating systems, and policies specific to different roles in your organization, or to Organizational Units you've already defined in Active Directory.</caps:sentence>
              <caps:sentence id="src58" class="srcSentence"> Some consider it useful to have device groups specific to iOS, Android, and Windows, as well as user groups for each organizational role.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src59" class="srcSentence">You'll probably want to create a default policy that applies to all groups and devices, to establish the basic compliance requirements of your company.</caps:sentence>
              <caps:sentence id="src60" class="srcSentence"> Then create more specific policies for the broadest categories of users and devices, for example, email policies for each of the device operating systems.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src61" class="srcSentence">Be careful naming your policies so that you can easily identify them later.</caps:sentence>
              <caps:sentence id="src62" class="srcSentence"> For example, a good, descriptive policy name is <ui>WP Email Policy for Entire Company</ui>.</caps:sentence>
            </para>
            <para>
              <caps:sentence id="src63" class="srcSentence">Each time you create a restrictive policy you'll want to communicate it to your users, so after you create the more general groups and policies pay attention to how you create smaller groups so that you can reduce unnecessary communication.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src64" class="srcSentence">How to create Microsoft Intune groups</caps:sentence>
        </title>
        <content>
          <procedure address="BKMK_CreateDevGroup">
            <title>
              <caps:sentence id="src65" class="srcSentence">To create a device group</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>Overview</ui> &gt; <ui>Create Group</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">Specify a name and optional description for the group, select a device group as the parent group, then click <ui>Next</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">On the <ui>Define Membership Criteria</ui> page, select the type of devices the group will include.</caps:sentence>
                    <caps:sentence id="src69" class="srcSentence"> Additional options to configure the group depend on the type of devices you select:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src70" class="srcSentence">
                          <embeddedLabel>Computer:</embeddedLabel> Specify whether to include all members of the parent group, the Organizational Units you want to include or exclude and the domains you want to include or exclude.</caps:sentence>
                        <caps:sentence id="src71" class="srcSentence"> The OU and domain information for a computer is obtained from inventory.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src72" class="srcSentence">
                          <embeddedLabel>Mobile:</embeddedLabel> Specify to include only mobile devices that are managed by <token>wit_nextref</token>, those managed by Exchange ActiveSync, or both.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src73" class="srcSentence">
                          <embeddedLabel>All devices:</embeddedLabel> This option includes all devices with no exclusions based on criteria.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">On the <ui>Define Direct Membership</ui> page, include or exclude individual devices you specify by clicking <ui>Browse</ui>.</caps:sentence>
                    <caps:sentence id="src75" class="srcSentence"> If you use the option to select devices that are not in the parent group you specified, those devices are automatically added to the parent group.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src76" class="srcSentence">On the <ui>Summary</ui> page, review the actions that will be taken, and then click <ui>Finish</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src77" class="srcSentence">The newly created group can be found in the <ui>Groups</ui> list, in the <ui>Groups</ui> workspace, under the parent group.</caps:sentence>
                  <caps:sentence id="src78" class="srcSentence"> From here, you can also edit or delete the group.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure>
            <title>
              <caps:sentence id="src79" class="srcSentence">To create a user group</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui> &gt; <ui>Overview</ui> &gt; <ui>Create Group</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src81" class="srcSentence">Specify a name and optional description for the group, select a user group as the parent group, then click <ui>Next</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">On the <ui>Define Membership Criteria</ui> page, specify whether to include all members of the parent group or to start with an empty group.</caps:sentence>
                    <caps:sentence id="src83" class="srcSentence">  You can then  include or exclude members based on the <maml:embeddedLabel xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">Security groups</maml:embeddedLabel>  of users that you manually configure in the account portal or that synchronize from your local Active Directory.</caps:sentence>
                    <caps:sentence id="src84" class="srcSentence"> If the membership of a security group changes, membership of user groups based on that security group can also change.</caps:sentence>
                  </para>
                  <alert class="important">
                    <para>
                      <caps:sentence id="src85" class="srcSentence">Currently, if your group includes members from specific security or manager groups, and you also exclude members from specific groups, the members you initially included will be removed.</caps:sentence>
                      <caps:sentence id="src86" class="srcSentence"> To create a group that has both included members and excluded members, we recommend that you first create a parent group with the included members, and then create a child to that group in which you list the excluded members.</caps:sentence>
                      <caps:sentence id="src87" class="srcSentence"> You can then use that child group as appropriate for Intune policies, profiles, and app distribution.</caps:sentence>
                    </para>
                  </alert>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src88" class="srcSentence">In the Azure Management Portal you can create a group based on the manager that the users report to.</caps:sentence>
                      <caps:sentence id="src89" class="srcSentence"> The group will be dynamic, changing as employees are added to or removed from that manager's team in Azure Active Directory.</caps:sentence>
                      <caps:sentence id="src90" class="srcSentence"> The procedure for creating an Azure group based on a manager is described in <externalLink><linkText>Using attributes to create advanced rules</linkText><linkUri>https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/</linkUri></externalLink> in the section called <legacyBold>To configure a group as a “Manager” group</legacyBold>.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">On the <ui>Define Direct Membership</ui> page, include or exclude individual users you specify by clicking <ui>Browse</ui>.</caps:sentence>
                    <caps:sentence id="src92" class="srcSentence"> If you use the option to select users that are not in the parent group you specified, those devices are automatically added to the parent group.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">On the <ui>Summary</ui> page, review the actions that will be taken, and then click <ui>Finish</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src94" class="srcSentence">The newly created group can be found in the <ui>Groups</ui> list, in the <ui>Groups</ui> workspace, under the parent group.</caps:sentence>
                  <caps:sentence id="src95" class="srcSentence"> From here, you can also edit or delete the group.</caps:sentence>
                </para>
                <alert class="tip">
                  <para>
                    <caps:sentence id="src96" class="srcSentence">Security groups are a great resource for populating user groups.</caps:sentence>
                    <caps:sentence id="src97" class="srcSentence"> Since your security groups define who has access to which resources, that can translate well into  <token>wit_nextref</token> user groups.</caps:sentence>
                    <caps:sentence id="src98" class="srcSentence"> Security groups that are synced from Active Directory to Azure Active Directory, or that are created directly in Azure Active Directory through the <token>wit_nextref</token> Account Portal, the O365 Administration Portal or the Azure Administration portal, are all available to you for creating user groups in <token>wit_nextref</token>.</caps:sentence>
                  </para>
                </alert>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src99" class="srcSentence">Managing your groups</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src100" class="srcSentence">Once you’ve created your groups you will continue to manage them according to the needs of your organization.</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_Filter">
            <title>
              <caps:sentence id="src101" class="srcSentence">Use filtered group views to help secure and manage users and devices</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src102" class="srcSentence">Filtered group views let you restrict which groups each IT admin can manage.</caps:sentence>
                <caps:sentence id="src103" class="srcSentence"> This can be useful when:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">Your IT admins should only be able to deploy items to specific users and devices.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src105" class="srcSentence">You want to display only relevant groups to each IT admin.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src106" class="srcSentence">You can configure filtered group views for service administrators in the <token>wit_nextref</token> administrator console.</caps:sentence>
                <caps:sentence id="src107" class="srcSentence"> For details, see <link xlink:href="5d1ac59c-a885-4276-8576-f3cf81c2d268">What to know before setting up Windows Intune</link>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src108" class="srcSentence">After configuring filtered group views for a service administrator, that administrator:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src109" class="srcSentence">Can view and select only the groups you specified when deploying software or policies, or when using reports</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">Does not receive status information on the following pages of the administration console:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src111" class="srcSentence">System Overview</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src112" class="srcSentence">Groups Overview</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src113" class="srcSentence">Endpoint Protection Overview</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src114" class="srcSentence">Alerts Overview</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src115" class="srcSentence">Software Overview</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src116" class="srcSentence">Policy Overview</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src117" class="srcSentence">To configure filtered group views</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src118" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Administrator Management</ui> &gt; <ui>Service Administrators</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">Select the service administrator for whom you want to filter groups, and then click <ui>Manage Groups</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">In the <ui>Select the groups that will be visible to this service administrator</ui> dialog box, add the groups that the selected service administrator will be able to access, and then click <ui>OK</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence id="src121" class="srcSentence">After you configure the filtered group views, the IT admin will be able to view and select only the groups you selected.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src122" class="srcSentence">Other management tasks for groups</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src123" class="srcSentence">You can edit your group to change its name and description and who belongs to the group.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src124" class="srcSentence">You can delete a group that no longer serves the needs of your organization.</caps:sentence>
            <caps:sentence id="src125" class="srcSentence"> Deleting a group does not delete the users that belong to that group.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src126" class="srcSentence">Groups and policy</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src127" class="srcSentence">Once you've set up your groups and policies, you'll want to check the practical implications of your design.</caps:sentence>
            <caps:sentence id="src128" class="srcSentence"> Here are some helpful tips and information about groups and policy.</caps:sentence>
          </para>
        </content>
        <content>
          <para>
            <caps:sentence id="src129" class="srcSentence">You can retrieve a lot of information regarding each device managed by <token>wit_nextref</token>.</caps:sentence>
            <caps:sentence id="src130" class="srcSentence"> Select any device from a device group and browse through the categories of information at the top of the screen.</caps:sentence>
            <caps:sentence id="src131" class="srcSentence"> Select <ui>Policy </ui>.</caps:sentence>
            <caps:sentence id="src132" class="srcSentence"> You'll see something like this screenshot of an Android device's policy settings.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="3032fd32-6c3b-4e4e-bf1f-8de6e9b8bf3c"></image>
          </mediaLink>
        </content>
        <content>
          <para>
            <caps:sentence id="src133" class="srcSentence">Each policy has an <ui>Intended Value</ui> and a <ui>Status</ui>.</caps:sentence>
            <caps:sentence id="src134" class="srcSentence"> The intended value is what you meant to achieve when assigning the policy.</caps:sentence>
            <caps:sentence id="src135" class="srcSentence"> The status is what is actually achieved when all of the policies that apply to the device, as well as the restrictions and requirements of the hardware and the operating system, are considered together.</caps:sentence>
            <caps:sentence id="src136" class="srcSentence">  In the screenshot you can see two clear examples:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src137" class="srcSentence">
                  <ui>Allow simple passwords</ui> is set to <ui>Yes</ui>, as shown in the <ui>Intended Value</ui> column, but its <ui>Status</ui> is <ui>Not applicable</ui>.</caps:sentence>
                <caps:sentence id="src138" class="srcSentence"> This is because simple passwords are not supported for Android devices.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src139" class="srcSentence">Similarly, the expanded policy item<ui>Email settings for iOS devices</ui> is not applied to this device, as it is an Android device.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
        <content>
          <alert class="note">
            <para>
              <caps:sentence id="src140" class="srcSentence">Remember that when two policies with different levels of restriction apply to the same device or user, the more restrictive policy applies in practice.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d158503c-1276-422b-ab81-5f66c1cd7e7a">Start using Microsoft Intune</link>
        <externalLink>
          <linkText>
            <caps:sentence id="src141" class="srcSentence">How to buy Intune</caps:sentence>
          </linkText>
          <linkUri>http://technet.microsoft.com/en-us/library/dn646949.aspx</linkUri>
        </externalLink>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>