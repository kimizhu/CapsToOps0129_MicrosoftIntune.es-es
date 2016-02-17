---
title: Usar directivas para administrar equipos y dispositivos m&#243;viles con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec
---
# Usar directivas para administrar equipos y dispositivos m&#243;viles con Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt1" class="tgtSentence">
            <token>wit_firstref</token> <embeddedLabel>Directivas</embeddedLabel> son grupos de configuraciones que controlan características en equipos y dispositivos móviles.</caps:sentence>
          <caps:sentence sentenceid="73b0f5acd77b9fc6c361f56df93b8c02" id="tgt2" class="tgtSentence"> Las directivas se crean con plantillas que contienen configuraciones recomendadas o personalizadas, y se implementan en grupos de dispositivos o usuarios.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="99caea1e3aaffe8627a0f763a3c6a4d3" id="tgt3" class="tgtSentence">Cómo crear directivas de configuración</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="39a8bf3a5cd074058ef9f3f019e0004d" id="tgt4" class="tgtSentence">La manera de crear directivas difiere según el tipo de directiva que se va a crear.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="157b9b47f399c8d8675245b65b3b24f2" id="tgt5" class="tgtSentence">Estos procedimientos tratan la creación de directivas de configuración.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f6374a237343a5f050e4bf789ca4f6d9" id="tgt6" class="tgtSentence">Para obtener ayuda para elegir la directiva adecuada, consulte <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Manage settings and features on your devices with Microsoft Intune policies</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3f76a86972abad4037b64c7d8d76cc31" id="tgt7" class="tgtSentence">Para obtener información acerca de la creación de directivas de cumplimiento, vea <link xlink:href="0775107a-6662-41c8-9404-be14bbb599f3">Manage device compliance policies for Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ac5fa09cdd8b09fa66e88bb78c383081" id="tgt8" class="tgtSentence">Para obtener información acerca de la creación de directivas de acceso condicional, vea <link xlink:href="c564d292-b83b-440d-bf08-3f5b299b7a5e">Manage access to email and SharePoint with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b2740e2446147a4d7aded323ec89acd8" id="tgt9" class="tgtSentence">Para obtener información acerca de las directivas de inscripción de dispositivos de empresa, vea <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Set up iOS management with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <procedure>
            <title>
              <caps:sentence sentenceid="f099f23f532d29541ade70cd4e662ecc" id="tgt10" class="tgtSentence">Para crear una directiva</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt11" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Directivas de configuración</ui> &gt; <ui>Agregar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="66a7eb17b789331ddbca2f838b959d05" id="tgt12" class="tgtSentence">Seleccione la directiva que quiera, elija usar la configuración recomendada para la directiva (si está disponible; puede cambiar esta configuración en otro momento), o crear una directiva personalizada con su propia configuración.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence sentenceid="8ffc7af7506530ce488b9657ced59118" id="tgt13" class="tgtSentence">Para obtener ayuda para elegir la directiva correcta, consulte <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Manage settings and features on your devices with Microsoft Intune policies</link>.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="e553f407d23271631b6e3f8a87a9726a" id="tgt14" class="tgtSentence">Cuando esté listo, haga clic en <ui>Crear directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt15" class="tgtSentence">En la pantalla <ui>Crear directiva</ui>, configure un nombre y una descripción opcional para la directiva.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="39e15588516e10b2b88f028ac3ea7d26" id="tgt16" class="tgtSentence">Configure la directiva necesaria y, a continuación, haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="c4a1b155a1db4949719852532bf84e77" id="tgt17" class="tgtSentence">En el cuadro de diálogo de confirmación, haga clic en <ui>Sí</ui> para implementar la directiva ahora o haga clic en <ui>No</ui> para crear la directiva sin implementarla.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="ef9bcbbc5894950617cac846a2646f33" id="tgt18" class="tgtSentence">Puede ver y editar la nueva directiva examinando las secciones de cada tipo de directiva en el área de trabajo <ui>Directiva</ui>.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="cc352689c1906adcae40490e36a280d3" id="tgt19" class="tgtSentence">Cuando se crea una directiva que usa la configuración recomendada, el nombre de la nueva directiva es una combinación del nombre de la plantilla, la fecha y la hora.</caps:sentence>
                  <caps:sentence sentenceid="8cd9c304e7f78e89a11aeedd4e21cf27" id="tgt20" class="tgtSentence"> Al modificar la directiva, el nombre se actualiza con la fecha y la hora de la edición.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <para>
            <caps:sentence sentenceid="b884e9d66de533db74b89051a38a2fbc" id="tgt21" class="tgtSentence">Ahora que ha creado una directiva, probablemente querrá implementarla en uno o varios grupos de usuarios o dispositivos.</caps:sentence>
          </para>
          <alert class="tip">
            <para>
              <caps:sentence sentenceid="9f0e5f4c789690ce96c1d5adc40ea67b" id="tgt22" class="tgtSentence">No implemente todos los tipos de directiva.</caps:sentence>
              <caps:sentence sentenceid="dd2ab25c57d977645c29c2b39fd9755e" id="tgt23" class="tgtSentence"> Por ejemplo, no se implementa la directiva de administración de aplicaciones móviles.</caps:sentence>
              <caps:sentence sentenceid="9bb3e937c70f9a4cdbea89c9068562a9" id="tgt24" class="tgtSentence"> Este tipo de directiva se asocia con una aplicación, que, a continuación, se implementa.</caps:sentence>
            </para>
          </alert>
          <procedure>
            <title>
              <caps:sentence sentenceid="97dee020e092d2bf2296218f4900b194" id="tgt25" class="tgtSentence">Para implementar una directiva</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt26" class="tgtSentence">En el área de trabajo <ui>Directiva</ui>, seleccione la directiva que quiera implementar y, a continuación, haga clic en <ui>Administrar implementación</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt27" class="tgtSentence">En el cuadro de diálogo <ui>Administrar la implementación</ui>:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="7aa0cc4adc5bb4707828e5c81d46776d" id="tgt28" class="tgtSentence">
                          <embeddedLabel>Para implementar la directiva</embeddedLabel>: seleccione uno o más grupos en los que quiera implementar la directiva y haga clic en <ui>Agregar</ui> &gt; <ui>Aceptar</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="51ba8b693db25ae97d6ba110b0b7b149" id="tgt29" class="tgtSentence">
                          <embeddedLabel>Para cerrar el cuadro de diálogo sin implementarla</embeddedLabel>: haga clic en <ui>Cancelar</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="fede0d0322be6f27289fe0d8eaad6d9d" id="tgt30" class="tgtSentence">Cuando se selecciona una directiva implementada, puede ver más información acerca de la implementación en la parte inferior de la lista de directivas.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="9e3614be456ddc521350b0c48ad7d4a8" id="tgt31" class="tgtSentence">Para administrar directivas que ya ha creado</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt32" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Directiva</ui> y, a continuación, busque y seleccione la directiva que desee administrar.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="784f979c0ad6d8c132cd7f1b11d501c7" id="tgt33" class="tgtSentence">Seleccione una de las acciones de la tabla siguiente:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="418c5509e2171d55b0aee5c2ea4442b5" id="tgt34" class="tgtSentence">Acción</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt35" class="tgtSentence">Más información</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="de95b43bceeb4b998aed4aed5cef1ae7" id="tgt36" class="tgtSentence">Editar</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="6bb4ca7848a195549e6b2b1898fe5a03" id="tgt37" class="tgtSentence">Abre las propiedades de la directiva seleccionada para que pueda realizar cambios.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="099af53f601532dbd31e0ea99ffdeb64" id="tgt38" class="tgtSentence">Eliminar</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e29beb8ea32857be387d0310543fe836" id="tgt39" class="tgtSentence">Elimina la directiva seleccionada.</caps:sentence>
                          </para>
                          <para address="BKMK_delete_policy">
                            <caps:sentence sentenceid="f8e81ccee21d9168e9c929b7d9a3bb35" id="tgt40" class="tgtSentence">Al eliminar una directiva, se quita de todos los grupos en los que se ha implementado.</caps:sentence>
                          </para>
                          <para>
                            <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec#BKMK_What">What happens when a policy is deleted, or no longer applicable</link>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="82dad1a62119270e878f904ee48f1bce" id="tgt41" class="tgtSentence">Administrar la implementación</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt42" class="tgtSentence">En el cuadro de diálogo <ui>Administrar la implementación</ui>, seleccione el grupo donde desea implementar la directiva y haga clic en <ui>Agregar</ui>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="78ee39268985bfe7a31ab4a19d21e499" id="tgt43" class="tgtSentence">Tareas para las directivas de Intune</caps:sentence>
        </title>
        <content>
          <procedure expanded="false" address="BKMK_Refresh">
            <title>
              <caps:sentence sentenceid="0b155d0935236cf98bf5c7f2074d7b64" id="tgt44" class="tgtSentence">las directivas en un dispositivo a fin de asegurarse de que están actualizadas (solo se aplica a equipos)</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt45" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Grupos</ui> y seleccione un grupo de dispositivos.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1aef72622694d0bed703a5df3b7beb0d" id="tgt46" class="tgtSentence">Seleccione los dispositivos en los que desea actualizar las directivas y haga clic en <ui>Tareas remotas</ui> &gt; <ui>Actualizar directivas</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt47" class="tgtSentence">Haga clic en <ui>Tareas remotas</ui> en la esquina inferior derecha de la ventana de la <token>wit_adminconsole</token> para comprobar el estado de la tarea.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="cccdcdb003c732cc54eeabbb1ccd1221" id="tgt48" class="tgtSentence">Para obtener más información acerca de las directivas de Intune</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="ba737498fc194a450cd9e5a954b9eb6e" id="tgt49" class="tgtSentence">¿Cuánto tiempo tardan los dispositivos móviles en obtener directivas o aplicaciones una vez implementados?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="3334020091784458de4ec8fc2f82b970" id="tgt50" class="tgtSentence">Cuando se implementa una directiva o aplicación, <ui><token>wit_nextref</token> empieza inmediatamente a intentar notificar al dispositivo que debe conectar con el servicio <token>wit_nextref</token>.  </ui>Este proceso suele tardar menos de 5 minutos.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="bb3f6be158248dc59d791b3200b357af" id="tgt51" class="tgtSentence">Si un dispositivo no se conecta para recibir la directiva una vez enviada la primera notificación, se realizan 3 intentos más.</caps:sentence>
                <caps:sentence sentenceid="018132669825424513ac3df2b0ab839c" id="tgt52" class="tgtSentence">  Si el dispositivo está desconectado (por ejemplo, está desactivado o no está conectado a una red), puede que no reciba las notificaciones.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="31a8f73b15264a5edcab21906457405c" id="tgt53" class="tgtSentence">En ese caso, el dispositivo obtendrá la directiva en la próxima conexión programada con el servicio <token>wit_nextref</token>, como se indica a continuación:</caps:sentence>
              </para>
              <table border="1">
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="34a6e5d64ade17ef4e51612c50dd72f5" id="tgt54" class="tgtSentence">Plataforma</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3350c1ea661060ea54f71e0945f95232" id="tgt55" class="tgtSentence">Frecuencia de conexión después de la notificación inicial</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt56" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fbe99f5276ea6a42166975f65e3ecd53" id="tgt57" class="tgtSentence">Cada 6 horas</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c31b32364ce19ca8fcd150a417ecce58" id="tgt58" class="tgtSentence">Android</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f6875ce0bc65b85ba7561cfa0180124a" id="tgt59" class="tgtSentence">Cada 8 horas</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="701fa4ddba17ba8634b10dea6ae686c5" id="tgt60" class="tgtSentence">Windows Phone</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f6875ce0bc65b85ba7561cfa0180124a" id="tgt61" class="tgtSentence">Cada 8 horas</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="80875a3b1d3a8fdf3bd69e1e5d1478fa" id="tgt62" class="tgtSentence">Equipos con Windows inscritos como dispositivos</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e4f79b5ee48feb7ffed429dcd45c7e55" id="tgt63" class="tgtSentence">Cada 24 horas</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="0040843909a9cdd19c132623732e4dde" id="tgt64" class="tgtSentence">Si el dispositivo se acaba de inscribir, la frecuencia de conexión será más frecuente, como se indica a continuación:</caps:sentence>
              </para>
              <table border="1">
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="34a6e5d64ade17ef4e51612c50dd72f5" id="tgt65" class="tgtSentence">Plataforma</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fad6c43b628858e0b472d0c164557fcf" id="tgt66" class="tgtSentence">Frecuencia</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt67" class="tgtSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="65998a253aae6b306258f871ad732986" id="tgt68" class="tgtSentence">Cada 15 minutos durante 6 horas y, después, cada 6 horas</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c31b32364ce19ca8fcd150a417ecce58" id="tgt69" class="tgtSentence">Android</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt70" class="tgtSentence"> <para>Cada 3 minutos durante 15 minutos y, después, cada 15 minutos durante 2 horas y, después cada 8 horas</para></caps:sentence>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="701fa4ddba17ba8634b10dea6ae686c5" id="tgt71" class="tgtSentence">Windows Phone</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="383c37388e83657812774b62a43c3c01" id="tgt72" class="tgtSentence">Cada 5 minutos durante 15 minutos y, después, cada 15 minutos durante 2 horas y, después cada 8 horas</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="80875a3b1d3a8fdf3bd69e1e5d1478fa" id="tgt73" class="tgtSentence">Equipos Windows inscritos como dispositivos</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4aeec7485dd22232a69b45ce03741404" id="tgt74" class="tgtSentence">Cada 3 minutos durante 30 minutos y, a continuación, cada 24 horas</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="1c0715e0c2d6e85291e46ea0eca0a951" id="tgt75" class="tgtSentence">Los usuarios también pueden iniciar la aplicación del Portal de empresa y sincronizar el dispositivo para buscar la directiva inmediatamente en cualquier momento.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="acb2bce81741d501a410b40ca15d5b07" id="tgt76" class="tgtSentence">¿Qué acciones provocan que Intune envíe inmediatamente una notificación a un dispositivo?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="1610ebb155c513d8580fcbe46ec00554" id="tgt77" class="tgtSentence">Los dispositivos conectan con <token>wit_nextref</token> cuando reciben una notificación que se lo indica o durante la conexión programada periódicamente que se muestra en las tablas superiores.</caps:sentence>
                <caps:sentence sentenceid="9d2f8cbb7e68151035c21910351d1bbe" id="tgt78" class="tgtSentence">  Cuando el destino es un dispositivo o usuario concreto con una acción como un borrado, bloqueo, restablecimiento de contraseña, implementación de aplicaciones, implementación de perfiles (Wi-Fi, VPN, correo electrónico, etc.) o implementación de directivas, <token>wit_nextref</token> comenzará inmediatamente a intentar notificar al dispositivo que debe conectarse al servicio Intune para recibir estas actualizaciones.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="676c6838f5b183e97b5b2421b98c6dc0" id="tgt79" class="tgtSentence">Otros cambios, como la revisión de la información de contacto del portal de empresa, no provocan una notificación inmediata a los dispositivos.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="9d754f0442723fabd600a3f4fa214973" id="tgt80" class="tgtSentence">Si varias directivas se implementan en el mismo usuario o dispositivo, ¿cómo puedo saber qué configuración se aplicará?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="0975a3a74a1016d5a6b33d630347c6ea" id="tgt81" class="tgtSentence">Es importante saber que, cuando se aplican dos o más directivas al mismo usuario o dispositivo, la evaluación de la configuración aplicada se hace a nivel de parámetro individual.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c34457877e99c72f26604225350cd216" id="tgt82" class="tgtSentence">La configuración de directivas de cumplimiento siempre tiene prioridad respecto a la configuración de directivas de configuración</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="dab2049f8e82de99a49284bdc78b0478" id="tgt83" class="tgtSentence">La configuración de directivas de cumplimiento más restrictiva se aplica si se evalúa con la misma configuración en otra directiva de cumplimiento</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="014af35dd5a87811a35d3bbf525692d3" id="tgt84" class="tgtSentence">La configuración de directivas de configuración más restrictiva se aplica si se evalúa con la misma configuración en otra directiva de configuración</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="aeaf8cd5638f42221d067ce65b534a9d" id="tgt85" class="tgtSentence">¿Qué sucede cuando las directivas de administración de aplicaciones móviles (MAM) entran en conflicto entre sí?</caps:sentence>
              <caps:sentence sentenceid="db2f6cd16952217a1be36c8635e1a5b9" id="tgt86" class="tgtSentence"> ¿Cuál se aplicará a la aplicación?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="e4842df0d657dfcb4312cc7c4b0da438" id="tgt87" class="tgtSentence">Los valores en conflicto son la configuración más restrictiva disponible en una directiva de administración de aplicaciones móviles, excepto para los campos de entrada de números (como intentos de PIN antes del restablecimiento).</caps:sentence>
                <caps:sentence sentenceid="2c499d9c0f943d5b8eab4bdf03fdc640" id="tgt88" class="tgtSentence">  Los campos de entrada de números se definirán con los mismos valores que si crea una directiva MAM en la consola con la opción de configuración recomendada.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="6503b539b37b21607c41341af77af765" id="tgt89" class="tgtSentence">Se producen conflictos cuando dos configuraciones de directiva son iguales.</caps:sentence>
                <caps:sentence sentenceid="8e7171f716d243b1950f0d6b5060ee45" id="tgt90" class="tgtSentence">  Por ejemplo, si configura dos directivas MAM que son idénticas, salvo por la configuración de copiar y pegar.</caps:sentence>
                <caps:sentence sentenceid="f6e00d501ba647d9a93b5c8c4e3b6a04" id="tgt91" class="tgtSentence">  En este escenario, la configuración de copiar y pegar se definirá con el valor más restrictivo, pero el resto de parámetros se aplicará según la configuración.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="69385f5b2026fa4b57fd5993953a0f82" id="tgt92" class="tgtSentence">Si una directiva se implementa en la aplicación y se aplica y, a continuación, se implementa una segunda, la primera tendrá precedencia y se aplicará, mientras que la segunda presentará un conflicto.</caps:sentence>
                <caps:sentence sentenceid="4da77473ba389277b16ca8bcbba3e7b5" id="tgt93" class="tgtSentence"> Sin embargo, si se aplican al mismo tiempo, lo que significa que no hay ninguna directiva anterior, ambas estarán en conflicto y los parámetros en conflicto se definirán con los valores más restrictivos.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="a6595e988886a7bb5b24e660b1cc63f0" id="tgt94" class="tgtSentence">¿Qué sucede cuando hay un conflicto de directivas personalizadas de iOS?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="05519602988e99e5179cc1f579ab2ce9" id="tgt95" class="tgtSentence">Intune no evalúa la carga de archivos de configuración de Apple ni directivas personalizadas de OMA-URI; sencillamente, se usa como mecanismo de entrega.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="f7e220b2b214a6212301e85d6aaa1f04" id="tgt96" class="tgtSentence">Por lo tanto, al implementar una directiva personalizada, asegúrese de que los valores configurados no entran en conflicto con las directivas de cumplimiento, configuración o de otro tipo.</caps:sentence>
                <caps:sentence sentenceid="72c4b9d6e442cfdcdda8318fab7ddcb8" id="tgt97" class="tgtSentence"> En el caso de una directiva personalizada con conflictos de parámetros, el orden en que se aplican los conflictos es aleatorio.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_What" expanded="false">
            <title>
              <caps:sentence sentenceid="d4083d88740905113903e8d56b8eae3a" id="tgt98" class="tgtSentence">¿Qué ocurre cuando se elimina una directiva o deja de ser aplicable?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="2e23a9271901f562046c199183ad8714" id="tgt99" class="tgtSentence">Al eliminar una directiva o quitar un dispositivo de un grupo al que se le aplica una directiva, se quitará la directiva y la configuración del dispositivo según las siguientes tablas:</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="09156eaf9ed2f5e3235fae84f05a0fad" id="tgt100" class="tgtSentence">Dispositivos móviles</caps:sentence>
                </title>
                <content>
                  <para></para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8c2447b0d283a8352470924c80fc57ad" id="tgt101" class="tgtSentence">Tipo de directiva</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="0f4137ed1502b5045d6083aa258b5c42" id="tgt102" class="tgtSentence">Windows</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c31b32364ce19ca8fcd150a417ecce58" id="tgt103" class="tgtSentence">Android</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a6694986ec6a7d79fbead54b33a47074" id="tgt104" class="tgtSentence">Windows Phone (solo 8.1)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt105" class="tgtSentence">iOS</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d0afe8f12ec4db66502cfc145ac5bbe5" id="tgt106" class="tgtSentence">Perfiles de correo electrónico, certificado, VPN y Wi-Fi</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b07286ebbb5bc7aa91cc3eaa8bc19711" id="tgt107" class="tgtSentence">Quitado</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b07286ebbb5bc7aa91cc3eaa8bc19711" id="tgt108" class="tgtSentence">Quitado</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b07286ebbb5bc7aa91cc3eaa8bc19711" id="tgt109" class="tgtSentence">Quitado</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b07286ebbb5bc7aa91cc3eaa8bc19711" id="tgt110" class="tgtSentence">Quitado</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e0f8d72e1c1b0372f15dcbd03b3ecc15" id="tgt111" class="tgtSentence">Todos los demás tipos de directivas</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c4062e5e79f046720fb9c64bc9ab3e24" id="tgt112" class="tgtSentence">No se ha quitado</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c4062e5e79f046720fb9c64bc9ab3e24" id="tgt113" class="tgtSentence">No se ha quitado</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="65fde986647c83ebc725f77b5dc67ef3" id="tgt114" class="tgtSentence">Se han eliminado las siguientes configuraciones:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="00e48d1f688610a2c1bc595a2aaad4db" id="tgt115" class="tgtSentence">Requerir una contraseña para desbloquear dispositivos móviles</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="9903f598b57a7f39747ca848a1376d18" id="tgt116" class="tgtSentence">Permitir contraseñas sencillas</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="2f276c6158fbb9b45297b2600181d32d" id="tgt117" class="tgtSentence">Longitud mínima de contraseña</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="dca92e82330f06a43bed4c39a9ae8a45" id="tgt118" class="tgtSentence">Tipo de contraseña obligatoria</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="2fb470a15f63e1990f7635ac30db44d7" id="tgt119" class="tgtSentence">Expiración de contraseña (días)</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="bd7e3f529ae9c075d09f3b7116bbe632" id="tgt120" class="tgtSentence">Recordar el historial de contraseñas</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="aad4971834ff738bf7c82b31d2513c23" id="tgt121" class="tgtSentence">Número de errores de inicio de sesión repetidos que se permiten antes de que se borre el dispositivo</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="c6f50988cb876f83b08878649ee5446b" id="tgt122" class="tgtSentence">Minutos de inactividad antes de que se pida la contraseña</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="484685f502a8f416bcf92e78a2b673ec" id="tgt123" class="tgtSentence">Tipo de contraseña requerida: número mínimo de conjuntos de caracteres</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="05dd919b3a7292227de28546f39f4928" id="tgt124" class="tgtSentence">Permitir cámara</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="6ee61936fa4604c18cfc32efd91b93d5" id="tgt125" class="tgtSentence">Requerir cifrado en dispositivo móvil</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ce113c55d1b3a3b1616bd8d58f2d6fdb" id="tgt126" class="tgtSentence">Permitir almacenamiento extraíble</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="a0c48d4afe3535baaeabfa7149c6ef7a" id="tgt127" class="tgtSentence">Permitir explorador web</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f956e1c595e427cc2f06ff42da87a73f" id="tgt128" class="tgtSentence">Permitir almacén de aplicaciones</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="0404a8a7a4917a78c040cfb0df59a1df" id="tgt129" class="tgtSentence">Permitir captura de pantalla</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="2c41b4c56056968e9f89851a7650f6ed" id="tgt130" class="tgtSentence">Permitir geolocalización</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="34d59c1187653c22ca1945abd1e99469" id="tgt131" class="tgtSentence">Permitir cuenta de Microsoft</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f98807ee3f4cbb43e555d032ecbbcb5c" id="tgt132" class="tgtSentence">Permitir copiar y pegar</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="5e2d5cfbfc5736a9055a62acc9465520" id="tgt133" class="tgtSentence">Permitir Wi-Fi Tethering</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="6da9e7b6cf656a40f0f3079fe763e272" id="tgt134" class="tgtSentence">Permitir la conexión automática a zonas Wi-Fi gratuitas</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="051640f64cfb604b6ba0ea831cb32db8" id="tgt135" class="tgtSentence">Permitir informar de zonas Wi-Fi</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="608181c0e21051993fa84c1754b29b65" id="tgt136" class="tgtSentence">Permitir el restablecimiento de la configuración de fábrica</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="f5b02fb1ac756124bdb8eaa270d0c1b2" id="tgt137" class="tgtSentence">Permitir Bluetooth</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="1773b705c6c985b2c179ff71b1d8a9eb" id="tgt138" class="tgtSentence">Permitir NFC</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="8dc8bec3c22373dd8447523e6202a5d4" id="tgt139" class="tgtSentence">Permitir Wi-Fi</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3b6bdce28b89d91c6312cefb5f23fe75" id="tgt140" class="tgtSentence">Eliminado, <ui>excepto</ui> para:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="7b57e74c6890ff3c771ae41ec0178dcd" id="tgt141" class="tgtSentence">Permitir itinerancia de voz</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="c2d252651547ad4dfa328dcf51811431" id="tgt142" class="tgtSentence">Permitir itinerancia de datos</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ecf2e3dcd5bc239b53446105c1d607ad" id="tgt143" class="tgtSentence">Permitir la sincronización automática en itinerancia</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence sentenceid="524164822d03894ee68052e183e7ea36" id="tgt144" class="tgtSentence">Equipos</caps:sentence>
                </title>
                <content>
                  <para></para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8c2447b0d283a8352470924c80fc57ad" id="tgt145" class="tgtSentence">Tipo de directiva</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="418c5509e2171d55b0aee5c2ea4442b5" id="tgt146" class="tgtSentence">Acción</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <embeddedLabel>
                              <caps:sentence sentenceid="e1f95fda4bceb4c3bd367f566b9660b0" id="tgt147" class="tgtSentence">Configuración de Endpoint Protection</caps:sentence>
                            </embeddedLabel>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9134d123c760a940d529deec3b3c7868" id="tgt148" class="tgtSentence">La configuración se restaura a los valores recomendados.</caps:sentence>
                            <caps:sentence sentenceid="f26e6049a24343d636036ea9448ded4c" id="tgt149" class="tgtSentence"> La única excepción es la opción de configuración <ui>Unirse a Microsoft Active Protection Service</ui>, para la que el valor predeterminado es <ui>No</ui>.</caps:sentence>
                            <caps:sentence sentenceid="363ddf43df695c296401df2564573a36" id="tgt150" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Microsoft Intune</link>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <embeddedLabel>
                              <caps:sentence sentenceid="96b46a6ead63ea8de88c6b3ca0f870f1" id="tgt151" class="tgtSentence">Configuración de las actualizaciones de software</caps:sentence>
                            </embeddedLabel>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="b457d4f42ae0e3e29580b5bd1e54fdc6" id="tgt152" class="tgtSentence">La configuración se restablece al estado predeterminado del sistema operativo.</caps:sentence>
                            <caps:sentence sentenceid="363ddf43df695c296401df2564573a36" id="tgt153" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="64ba8e58-fab1-4480-a440-164268810138">Keep Your Computers Up To Date with Software Updates in Microsoft Intune</link>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <embeddedLabel>
                              <caps:sentence sentenceid="ff53d3dbeaaa20ccbaa51397b12dfbfb" id="tgt154" class="tgtSentence">Configuración de <token>wit_tools</token></caps:sentence>
                            </embeddedLabel>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="d996a6d77eff52eb9fae58eceb347386" id="tgt155" class="tgtSentence">Cualquier información de contacto de soporte configurada por la directiva se elimina de los equipos.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <embeddedLabel>
                              <caps:sentence sentenceid="9f18be92243ea7a57e92cfaa67ad3e78" id="tgt156" class="tgtSentence">Configuración de Windows Firewall</caps:sentence>
                            </embeddedLabel>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="030a4a1c5539e029ccc2b05c34113abb" id="tgt157" class="tgtSentence">La configuración se restablece al estado predeterminado del sistema operativo del equipo.</caps:sentence>
                            <caps:sentence sentenceid="363ddf43df695c296401df2564573a36" id="tgt158" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Microsoft Intune</link>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="110cbdbf-8f9b-4c1b-9e3e-184113cd711c">Technical reference for Microsoft Intune</link>
        <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Manage settings and features on your devices with Microsoft Intune policies</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">
            <token>wit_firstref</token> <embeddedLabel>Policies</embeddedLabel> are groups of settings that control features on mobile devices and computers.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You create policies using templates that contain recommended or customized settings, and then deploy them to device or user groups.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">How to create configuration policies</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">The way you create policies differs depending on the policy type you are creating.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">These procedures cover creating configuration policies.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src6" class="srcSentence">To help choose the right policy for your needs, see <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Manage settings and features on your devices with Microsoft Intune policies</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src7" class="srcSentence">For information about creating compliance policies, see <link xlink:href="0775107a-6662-41c8-9404-be14bbb599f3">Manage device compliance policies for Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src8" class="srcSentence">For information about creating conditional access policies, see <link xlink:href="c564d292-b83b-440d-bf08-3f5b299b7a5e">Manage access to email and SharePoint with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">For information about corporate device enrollment policies, see <link xlink:href="dc451224-1372-4b84-b641-cfa67cb3849b">Set up iOS management with Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <procedure>
            <title>
              <caps:sentence id="src10" class="srcSentence">To create a policy</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Configuration Policies</ui> &gt; <ui>Add</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Choose the policy you want, choose to use the recommended settings for the policy (when available; you can change these settings later), or to create a custom policy with your own settings.</caps:sentence>
                  </para>
                  <alert class="tip">
                    <para>
                      <caps:sentence id="src13" class="srcSentence">For help choosing the right policy, see <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Manage settings and features on your devices with Microsoft Intune policies</link>.</caps:sentence>
                    </para>
                  </alert>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">When you are ready, click <ui>Create Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">On the <ui>Create Policy</ui> screen, configure a name and optional description for the policy.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">Configure the required policy settings, then click <ui>Save Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">In the confirmation dialog box, click <ui>Yes</ui> to deploy the policy now, or click <ui>No</ui> to create the policy without deploying it.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src18" class="srcSentence">You can view and edit the new policy by browsing the sections for each policy type in <ui>Policy</ui> workspace.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src19" class="srcSentence">When you create a policy that uses the recommended settings, the name of the new policy is a combination of the template name, date, and time.</caps:sentence>
                  <caps:sentence id="src20" class="srcSentence"> When you edit the policy, the name updates with the time and date of the edit.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <para>
            <caps:sentence id="src21" class="srcSentence">Now that you have created a policy, you will typically want to deploy it to one or more groups of users or devices.</caps:sentence>
          </para>
          <alert class="tip">
            <para>
              <caps:sentence id="src22" class="srcSentence">You don't deploy all policy types.</caps:sentence>
              <caps:sentence id="src23" class="srcSentence"> For example, the mobile application management policy is not deployed.</caps:sentence>
              <caps:sentence id="src24" class="srcSentence"> This policy type is instead associated with an app, which you then deploy.</caps:sentence>
            </para>
          </alert>
          <procedure>
            <title>
              <caps:sentence id="src25" class="srcSentence">To deploy a policy</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">In the <ui>Policy</ui> workspace, select the policy you want to deploy, then click <ui>Manage Deployment</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">In the <ui>Manage Deployment</ui> dialog box:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src28" class="srcSentence">
                          <embeddedLabel>To deploy the policy</embeddedLabel> - Select one or more groups to which you want to deploy the policy, then click <ui>Add</ui> &gt; <ui>OK</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src29" class="srcSentence">
                          <embeddedLabel>To close the dialog box without deploying it</embeddedLabel> - Click <ui>Cancel</ui>.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src30" class="srcSentence">When you select a deployed policy, you can view further information about the deployment in the lower part of the policies list.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src31" class="srcSentence">To manage policies you have already created</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Policy</ui>, then browse to and select the policy you want to manage.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Select one of the actions in the following table:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src34" class="srcSentence">Action</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src35" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src36" class="srcSentence">Edit</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src37" class="srcSentence">Opens the properties for the selected policy to allow you to make changes.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src38" class="srcSentence">Delete</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src39" class="srcSentence">Deletes the selected policy.</caps:sentence>
                          </para>
                          <para address="BKMK_delete_policy">
                            <caps:sentence id="src40" class="srcSentence">When you delete a policy, it is removed from all groups to which it was deployed.</caps:sentence>
                          </para>
                          <para>
                            <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec#BKMK_What">What happens when a policy is deleted, or no longer applicable</link>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src41" class="srcSentence">Manage Deployment</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src42" class="srcSentence">In the <ui>Manage Deployment</ui> dialog box, select the group you want to deploy the policy to and click <ui>Add</ui>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src43" class="srcSentence">Tasks for Intune policies</caps:sentence>
        </title>
        <content>
          <procedure expanded="false" address="BKMK_Refresh">
            <title>
              <caps:sentence id="src44" class="srcSentence">To refresh the policies on a device to ensure they are current (applies to computers only)</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Groups</ui>, and then select a device group.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">Select the devices on which you want to refresh the policies, and then click <ui>Remote Tasks</ui> &gt; <ui>Refresh Policies</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">Click <ui>Remote Tasks</ui> in the bottom-right corner of the <token>wit_adminconsole</token> window to check the task status.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src48" class="srcSentence">More information about Intune policies</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src49" class="srcSentence">How long does it take for mobile devices to get policy or apps after they have been deployed?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src50" class="srcSentence">When a policy or app is deployed, <ui><token>wit_nextref</token> immediately begins attempting to notify the device that it should check-in with the <token>wit_nextref</token> service.  </ui>This typically takes less than 5 minutes.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src51" class="srcSentence">If a device doesn't check in to get policy after the first notification is sent, 3 more attempts are made.</caps:sentence>
                <caps:sentence id="src52" class="srcSentence">  If the device is offline (for example, it is turned off, or not connected to a network) then it might not receive the notifications.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src53" class="srcSentence">In this case, the device will get policy on its next scheduled check-in with the <token>wit_nextref</token> service as follows:</caps:sentence>
              </para>
              <table border="1">
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">Platform</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src55" class="srcSentence">Check-in frequency after initial notification</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src56" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src57" class="srcSentence">Every 6 hours</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">Android</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src59" class="srcSentence">Every 8 hours</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src60" class="srcSentence">Windows Phone</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src61" class="srcSentence">Every 8 hours</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src62" class="srcSentence">Windows PCs enrolled as devices</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">Every 24 hours</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src64" class="srcSentence">If the device has just enrolled the check-in frequency will be more frequent as follows:</caps:sentence>
              </para>
              <table border="1">
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src65" class="srcSentence">Platform</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">Frequency</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src67" class="srcSentence">iOS</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">Every 15 minutes for 6 hours and then every 6 hours</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">Android</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <caps:sentence id="src70" class="srcSentence"> <para>Every 3 minutes for 15 minutes then every 15 minutes for 2 hours, and then every 8 hours</para></caps:sentence>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">Windows Phone</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src72" class="srcSentence">Every 5 minutes for 15 minutes then every 15 minutes for 2 hours, and then every 8 hours</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src73" class="srcSentence">Windows PCs enrolled as devices</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">Every 3 minutes for 30 minutes, and then every 24 hours</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src75" class="srcSentence">Users can also launch the Company Portal app and sync the device to immediately check for policy anytime.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src76" class="srcSentence">What actions cause Intune to immediately send notification  to a device?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src77" class="srcSentence">Devices check in with <token>wit_nextref</token> either when they receive a notification telling them to check-in, or during their regularly scheduled check-in as shown in the tables above.</caps:sentence>
                <caps:sentence id="src78" class="srcSentence">  When you target a device or user specifically with an action such as a wipe, lock, passcode reset, app deployment, profile deployment (WiFi, VPN, e-mail, etc.), or policy deployment, <token>wit_nextref</token> will immediately begin trying to notify the device that it should check-in with the Intune service to receive these updates.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src79" class="srcSentence">Other changes such as revising the contact information in the company portal do not cause an immediate notification to devices.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src80" class="srcSentence">If multiple policies are deployed to the same user or device how do I know which settings will get applied?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src81" class="srcSentence">It’s important to know that when two or more policies are deployed to the same user or device the evaluation for which setting is applied is done at the individual setting level.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">Compliance policy settings always have precedence over configuration policy settings</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src83" class="srcSentence">The most restrictive compliance policy setting is applied if evaluated against the same setting in a different compliance policy</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">The most restrictive configuration policy setting is applied if evaluated against the same setting in a different configuration policy</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src85" class="srcSentence">What happens when mobile application management (MAM) policies conflict with each other?</caps:sentence>
              <caps:sentence id="src86" class="srcSentence"> Which one will be applied to the app?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src87" class="srcSentence">Conflict values are the most restrictive settings available in a mobile application management policy, except for the number entry fields (like PIN attempts before reset).</caps:sentence>
                <caps:sentence id="src88" class="srcSentence">  The number entry fields will be set to the same as the values as if you create a MAM policy in the console using the recommended settings option.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src89" class="srcSentence">Conflicts occur when two policy settings are the same.</caps:sentence>
                <caps:sentence id="src90" class="srcSentence">  For example, you configured two MAM policies that are identical except for the copy/paste setting.</caps:sentence>
                <caps:sentence id="src91" class="srcSentence">  In this scenario, the copy/paste setting will be set to the most restrictive value, but the rest of the settings will be applied as configured.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src92" class="srcSentence">If one policy is deployed to the app and takes effect, and then a second one is deployed, the first one deployed will take precedence and stay applied, while the second shows in conflict.</caps:sentence>
                <caps:sentence id="src93" class="srcSentence"> However, if they are both applied at the same time, meaning that there is no preceding policy, then they will both be in conflict, and any conflicting settings will be set to the most restrictive values.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src94" class="srcSentence">What happens when iOS custom policies conflict?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src95" class="srcSentence">Intune does not evaluate the payload of Apple Configuration files or custom OMA-URI policy, it merely serves as the delivery mechanism.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src96" class="srcSentence">Therefore, when you deploy a custom policy, ensure the settings configured do not conflict with compliance, configuration or other custom policies.</caps:sentence>
                <caps:sentence id="src97" class="srcSentence"> In the case of a custom policy with settings conflicts, the order in which are settings are applied is random.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_What" expanded="false">
            <title>
              <caps:sentence id="src98" class="srcSentence">What happens when a policy is deleted, or no longer applicable</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src99" class="srcSentence">When you delete a policy, or remove a device from a group to which a policy was deployed, the policy and settings will be removed from the device according to the following tables:</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src100" class="srcSentence">Mobile devices</caps:sentence>
                </title>
                <content>
                  <para></para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src101" class="srcSentence">Policy type</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src102" class="srcSentence">Windows</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src103" class="srcSentence">Android</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src104" class="srcSentence">Windows Phone (8.1 only)</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src105" class="srcSentence">iOS</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src106" class="srcSentence">Wi-Fi, VPN, certificate and email profiles</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src107" class="srcSentence">Removed</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src108" class="srcSentence">Removed</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src109" class="srcSentence">Removed</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src110" class="srcSentence">Removed</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src111" class="srcSentence">All other policy types</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src112" class="srcSentence">Not removed</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src113" class="srcSentence">Not removed</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src114" class="srcSentence">The following settings are removed:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src115" class="srcSentence">Require a password to unlock mobile devices</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src116" class="srcSentence">Allow simple passwords</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src117" class="srcSentence">Minimum password length</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src118" class="srcSentence">Required password type</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src119" class="srcSentence">Password expiration (days)</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src120" class="srcSentence">Remember password history</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src121" class="srcSentence">Number of repeated sign-in failures to allow before the device is wiped</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src122" class="srcSentence">Minutes of inactivity before password is required</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src123" class="srcSentence">Required password type – minimum number of character sets</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src124" class="srcSentence">Allow camera</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src125" class="srcSentence">Require encryption on mobile device</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src126" class="srcSentence">Allow removable storage</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src127" class="srcSentence">Allow web browser</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src128" class="srcSentence">Allow application store</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src129" class="srcSentence">Allow screen capture</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src130" class="srcSentence">Allow geolocation</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src131" class="srcSentence">Allow Microsoft Account</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src132" class="srcSentence">Allow copy and paste</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src133" class="srcSentence">Allow Wi-Fi tethering</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src134" class="srcSentence">Allow automatic connection to free Wi-Fi hotspots</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src135" class="srcSentence">Allow Wi-Fi hotspot reporting</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src136" class="srcSentence">Allow factory reset</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src137" class="srcSentence">Allow Bluetooth</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src138" class="srcSentence">Allow NFC</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src139" class="srcSentence">Allow Wi-Fi</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src140" class="srcSentence">Removed, <ui>except</ui> for:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src141" class="srcSentence">Allow voice roaming</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src142" class="srcSentence">Allow data roaming</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src143" class="srcSentence">Allow automatic synchronization while roaming</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
              <section>
                <title>
                  <caps:sentence id="src144" class="srcSentence">Computers</caps:sentence>
                </title>
                <content>
                  <para></para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src145" class="srcSentence">Policy type</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src146" class="srcSentence">Action</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <embeddedLabel>
                              <caps:sentence id="src147" class="srcSentence">Endpoint Protection settings</caps:sentence>
                            </embeddedLabel>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src148" class="srcSentence">Settings are restored to their recommended values.</caps:sentence>
                            <caps:sentence id="src149" class="srcSentence"> The only exception is the setting <ui>Join Microsoft Active Protection Service</ui> for which the default value is <ui>No</ui>.</caps:sentence>
                            <caps:sentence id="src150" class="srcSentence"> For details, see <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Microsoft Intune</link>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <embeddedLabel>
                              <caps:sentence id="src151" class="srcSentence">Software updates settings</caps:sentence>
                            </embeddedLabel>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src152" class="srcSentence">Settings are reset to the default state for the operating system.</caps:sentence>
                            <caps:sentence id="src153" class="srcSentence"> For details, see <link xlink:href="64ba8e58-fab1-4480-a440-164268810138">Keep Your Computers Up To Date with Software Updates in Microsoft Intune</link>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <embeddedLabel>
                              <caps:sentence id="src154" class="srcSentence">
                                <token>wit_tools</token> settings</caps:sentence>
                            </embeddedLabel>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src155" class="srcSentence">Any support contact information that was configured by the policy is deleted from computers.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <embeddedLabel>
                              <caps:sentence id="src156" class="srcSentence">Windows Firewall settings</caps:sentence>
                            </embeddedLabel>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src157" class="srcSentence">Settings are reset to the default for the computer operating system.</caps:sentence>
                            <caps:sentence id="src158" class="srcSentence"> For details, see <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Microsoft Intune</link>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                </content>
              </section>
            </sections>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="110cbdbf-8f9b-4c1b-9e3e-184113cd711c">Technical reference for Microsoft Intune</link>
        <link xlink:href="d27f2739-9791-4aae-a9db-01a4e59ccfe5">Manage settings and features on your devices with Microsoft Intune policies</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>