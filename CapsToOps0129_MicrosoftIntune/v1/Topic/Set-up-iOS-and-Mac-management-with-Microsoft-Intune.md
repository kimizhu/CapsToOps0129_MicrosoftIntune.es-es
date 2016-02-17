---
title: Configurar la administraci&#243;n de iOS con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dc451224-1372-4b84-b641-cfa67cb3849b
---
# Configurar la administraci&#243;n de iOS con Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="fbcdf0a327a2ea84d2819abb16a78018" id="tgt1" class="tgtSentence">Con <token>wit_nextref</token>, puede habilitar la inscripción BYOD (siglas en inglés de "traiga su propio dispositivo") del dispositivo iOS para proporcionar acceso al correo electrónico y a las aplicaciones de la empresa a los usuarios de iPhone y iPad.</caps:sentence>
          <caps:sentence sentenceid="1db7033964c7d387beb17f15127b059e" id="tgt2" class="tgtSentence"> Una vez que los usuarios instalen la aplicación del portal de empresa <token>wit_nextref</token>, puede aplicar directivas a sus dispositivos mediante la consola de administración de <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence sentenceid="58af814403ab15a055e4905c680e8564" id="tgt3" class="tgtSentence">  Antes de que pueda administrar dispositivos iOS, debe importar un certificado del Servicio de notificaciones push de Apple (APN).</caps:sentence>
          <caps:sentence sentenceid="370454f031e2743f6b35c41672a13350" id="tgt4" class="tgtSentence"> Este certificado permite a Intune administrar dispositivos iOS y establecer una conexión de IP acreditada y cifrada con los servicios de entidad de administración de dispositivos móviles.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e52ea201e8a2cc4e3eedc1d86ef3dc41" id="tgt5" class="tgtSentence">Como alternativa a la inscripción con la aplicación Portal de empresa, también puede <externalLink><linkText>inscribir los dispositivos iOS pertenecientes a la empresa</linkText><linkUri>https://technet.microsoft.com/en-US/library/dn408185.aspx#BKMK_CODiOS</linkUri></externalLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="fa3c8c4f950751a988785196a61b524f" id="tgt6" class="tgtSentence">Prepararse para administrar dispositivos móviles iOS con Microsoft Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="db84b43c361fdd756b66572b349d3b69" id="tgt7" class="tgtSentence">Los pasos siguientes permiten a <token>wit_nextref</token> administrar dispositivos iOS mediante el Portal de empresa.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="8003ce531ed49eabc0bdbc740575ef4d" id="tgt8" class="tgtSentence">Configurar la inscripción de iOS con Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt9" class="tgtSentence">
                      <embeddedLabel>Configurar Intune</embeddedLabel> <br />Si aún no lo ha hecho, prepárese para la administración de dispositivos móviles. Para ello, <externalLink><linkText>defina la entidad de administración de dispositivos móviles</linkText><linkUri>https://technet.microsoft.com/library/mt346013.aspx</linkUri></externalLink> como <embeddedLabel>Microsoft Intune</embeddedLabel>. </caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt10" class="tgtSentence">
                      <embeddedLabel>Obtener una solicitud de firma de certificado</embeddedLabel> <br />Como usuario administrativo, abra el <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, vaya a <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui> &gt; <ui>iOS</ui> &gt; <ui>Cargar un certificado de APN</ui> y haga clic en <ui>Descargar la solicitud de certificado de APN</ui>. </caps:sentence>
                    <caps:sentence sentenceid="931d1e075d8401e764cfeae7da29d8e9" id="tgt11" class="tgtSentence"> Guarde la solicitud de firma de certificado (.csr) en el equipo local.</caps:sentence>
                    <caps:sentence sentenceid="66368b93adc60e7da74b1bfc6418418b" id="tgt12" class="tgtSentence"> Se utiliza el archivo .csr para solicitar un certificado de relación de confianza desde el portal de certificados push de Apple.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="41179d1e-2fb6-4f01-954e-06aa4740fc06"></image>
                  </mediaLink>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="45568fffc1aefb85bb60ebc96a472dda" id="tgt13" class="tgtSentence">
                      <embeddedLabel>Obtener un certificado de servicio de notificaciones de inserción de Apple</embeddedLabel>
                      <br />Vaya al <externalLink target="_blank"><linkText>Portal de certificados push de Apple</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=269844</linkUri></externalLink> e inicie sesión con el Id. de Apple de empresa para crear el certificado de APN mediante el archivo .csr.</caps:sentence>
                    <caps:sentence sentenceid="a92eb35e079c0546e17286cd7b1792d1" id="tgt14" class="tgtSentence"> Este ID de Apple debe utilizarse en el futuro para renovar el certificado APNs.</caps:sentence>
                    <caps:sentence sentenceid="9a972200cfae67edd6c1bfda20525509" id="tgt15" class="tgtSentence"> Descargue el certificado de APNs (.pem) y guarde el archivo localmente.</caps:sentence>
                    <caps:sentence sentenceid="93db2c9f1a1f06bbae4bf0456e506814" id="tgt16" class="tgtSentence"> Este archivo de certificado de APNs se usa para establecer una relación de confianza entre el servidor de notificaciones push de Apple y la entidad de administración de dispositivos móviles de Intune.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt17" class="tgtSentence">
                      <embeddedLabel>Agregar el certificado de APN a Intune</embeddedLabel> <br />En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, vaya a <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui> &gt; <ui>iOS</ui> &gt; <ui>Cargar un certificado de APN</ui> y haga clic en <ui>Cargar el certificado de APN</ui>. </caps:sentence>
                    <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt18" class="tgtSentence">
                      <ui>Busque</ui> el archivo de certificado (.pem), haga clic en <ui>Abrir</ui> y, a continuación, escriba su <ui>ID de Apple</ui>.</caps:sentence>
                    <caps:sentence sentenceid="bd79e2ae2234dc288a54beee42048bd5" id="tgt19" class="tgtSentence"> Con el certificado APNs, Intune puede inscribir y administrar dispositivos iOS insertando la directiva en los dispositivos móviles inscritos.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt20" class="tgtSentence">
                      <embeddedLabel>Agregar usuarios de Intune</embeddedLabel> <br />El propietario del dispositivo móvil debe agregarse al portal de cuentas para poder inscribir dispositivos. </caps:sentence>
                    <caps:sentence sentenceid="4ad3f37ced51ee31a6023786a31e0a36" id="tgt21" class="tgtSentence"> Inicie sesión en el <externalLink><linkText>Portal de cuentas de Microsoft Intune</linkText><linkUri>http://account.manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Agregar usuarios</ui> y seleccione una opción:</caps:sentence>
                  </para>
                  <para></para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="18c21fa550c6e43924af228a0679d742" id="tgt22" class="tgtSentence">
                          <embeddedLabel>Usuario</embeddedLabel>: para agregar un solo usuario, seleccione <ui>Nuevo</ui> &gt; <ui>Usuario</ui> y especifique <ui>Detalles</ui>, <ui>Asignar roles</ui> y <ui>Establecer ubicación de usuario</ui>; a continuación, asigne el usuario a un <ui>Grupo</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="73a0cf31c1339b90e62f3aeedb300145" id="tgt23" class="tgtSentence">
                          <embeddedLabel>Adición en masa</embeddedLabel>: cree un archivo .csv (consulte los archivos de ejemplo proporcionados) e impórtelo en el portal de cuentas.</caps:sentence>
                        <caps:sentence sentenceid="c1b650589e7e36a0c106e31a527a915b" id="tgt24" class="tgtSentence"> Especifique los roles, la ubicación y el grupo y, después, cree las cuentas.</caps:sentence>
                        <caps:sentence sentenceid="89fdb17258d09eaf586195abfab87f86" id="tgt25" class="tgtSentence"> Los archivos .csv de ejemplo y en blanco se pueden descargar desde el portal de cuentas.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="665358b9ae967c6584e5f22475cbb77e" id="tgt26" class="tgtSentence">También puede habilitar la sincronización de Active Directory o Azure Active Directory.</caps:sentence>
                    <caps:sentence sentenceid="ccabfe774f8edea6ef04ff48472298c4" id="tgt27" class="tgtSentence"> Para obtener más información sobre la integración de otros usuarios de Azure Active Directory con Intune, consulte la <externalLink><linkText>Guía de sincronización de directorios</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=511540</linkUri></externalLink> o haga clic en <embeddedLabel>Otras formas de agregar usuarios</embeddedLabel> en el portal de cuentas.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9781b62d0e687e3d5e772f805a335d75" id="tgt28" class="tgtSentence">
                      <embeddedLabel>Crear grupos </embeddedLabel> (opcional)<br />Los grupos ofrecen flexibilidad para administrar dispositivos y usuarios.</caps:sentence>
                    <caps:sentence sentenceid="507c76716449010dc59f1483e3964cd5" id="tgt29" class="tgtSentence"> Los grupos se pueden configurar según sus necesidades de organización (por ejemplo, por ubicación geográfica, departamento o características de hardware).</caps:sentence>
                    <caps:sentence sentenceid="e3d2410d4aed3acc53c4e7d50a0202e7" id="tgt30" class="tgtSentence">   Consulte <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt31" class="tgtSentence">
                    <para>
                      <embeddedLabel>Agregar directivas para dispositivos</embeddedLabel> (opcional)<br />Las directivas son grupos de configuraciones que controlan las características de los dispositivos. La mayoría de las directivas MDM son específicas de la plataforma. Las directivas se crean mediante plantillas que contienen configuraciones recomendadas o personalizadas y, luego, se implementan en grupos. Consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</para> </caps:sentence>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ebc4e07b040da274fbcd0bc615d552aa" id="tgt32" class="tgtSentence">
                      <embeddedLabel>Establecer el límite de inscripción de dispositivos</embeddedLabel> (opcional) <br />Para limitar el número de dispositivos móviles que puede inscribir un usuario, inicie sesión en la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui> &gt; <ui>Reglas de inscripción</ui>.</caps:sentence>
                    <caps:sentence sentenceid="81896f17af8e74876e83bdcbfb84232d" id="tgt33" class="tgtSentence"> Seleccione el número máximo de dispositivos que un usuario puede inscribir y haga clic en <ui>Guardar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="486bbd9b1c2d83f16fd091ae8a3e3110" id="tgt34" class="tgtSentence">
                      <embeddedLabel>Establecer la configuración del portal de empresa </embeddedLabel>
                      <br /> Puede personalizar Portal de empresa de Intune para su empresa.</caps:sentence>
                    <caps:sentence sentenceid="4f4f145aafdf6ea8a38164ebe7706661" id="tgt35" class="tgtSentence"> En la <externalLink><linkText>consola de administrador de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Portal de empresa</ui>.</caps:sentence>
                    <caps:sentence sentenceid="625a8686dac7b5297d90d5266d7fcd78" id="tgt36" class="tgtSentence"> Configure lo siguiente</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9bb4c85dfbafa8c61f627241bb21358c" id="tgt37" class="tgtSentence">Nombre de compañía</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="16576d71cb733d359db3b6e40b97b228" id="tgt38" class="tgtSentence">Nombre del contacto del departamento de TI</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="965d8e507652fcc1b19d4b13823cf800" id="tgt39" class="tgtSentence">Número de teléfono del departamento de TI</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt40" class="tgtSentence">Información adicional</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2ddf6ec5ba19603e0bbf4dd9dd16b1c5" id="tgt41" class="tgtSentence">Dirección URL de la declaración de privacidad de la empresa</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="07c657dc49d79de1aa99cc410449492d" id="tgt42" class="tgtSentence">Dirección URL del sitio web de soporte técnico (no se muestra)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ca75dc95767c2d020aba7b02bb2837c8" id="tgt43" class="tgtSentence">Nombre del sitio web</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step address="BKMK_Terms">
                <content>
                  <para address="BKMK_TAC">
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt44" class="tgtSentence">
                      <embeddedLabel>Definir los términos y condiciones</embeddedLabel> <br />Puede publicar los términos y condiciones que verán los usuarios cuando utilicen el portal de empresa por primera vez desde cualquier dispositivo, tanto si ya está inscrito como si no. </caps:sentence>
                    <caps:sentence sentenceid="76e70313975a4f1d7b0b80371cb657f6" id="tgt45" class="tgtSentence"> Los usuarios tendrán que aceptar estos términos para acceder al portal.</caps:sentence>
                    <caps:sentence sentenceid="def8f09519f1300abba2ac736f61ee85" id="tgt46" class="tgtSentence"> Cuando realice una actualización importante de los términos y condiciones y quiera que los usuarios los vean y los acepten, puede marcar los nuevos términos y condiciones como una nueva versión y los usuarios pasarán por el mismo proceso la próxima vez que visiten el portal.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt47" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <embeddedLabel>Portal de empresa</embeddedLabel> &gt; <embeddedLabel>Términos y condiciones</embeddedLabel>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="22314166c09f0092afd164769c05a96e" id="tgt48" class="tgtSentence">Especifique lo siguiente:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3f5f5b4690de486cf3b84721660d5361" id="tgt49" class="tgtSentence">Requerir a los usuarios que acepten los términos y condiciones de empresa antes de usar el Portal de empresa</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d5d3db1765287eef77d7927cc956f50a" id="tgt50" class="tgtSentence">Título</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ff4ab5876abeb4588a20510293a5034e" id="tgt51" class="tgtSentence">Texto de los términos</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="87d46459cbea451b0c3ddceea31ed8db" id="tgt52" class="tgtSentence">Texto para explicar lo que significa que el usuario acepte</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="3a6b2cc8591e95b30009877a9298f3c3" id="tgt53" class="tgtSentence">Puede ver los <externalLink><linkText>detalles acerca de los términos y las condiciones </linkText><linkUri>https://technet.microsoft.com/library/mt405893.aspx</linkUri></externalLink>.</caps:sentence>
                    <caps:sentence sentenceid="68cdeeeedf05ae0db0b3c5b322c28358" id="tgt54" class="tgtSentence">  Asimismo, también puede ver qué usuarios han aceptado los términos y condiciones mediante el uso de los <externalLink><linkText>informes de términos y condiciones</linkText><linkUri>https://technet.microsoft.com/library/dn646977.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt55" class="tgtSentence">
                      <embeddedLabel>Indique a los usuarios cómo obtener acceso a los recursos de empresa con el portal de empresa</embeddedLabel> <br /><link xlink:href="48914533-f138-4dc0-8b93-4cea3ac61f7b">What to tell your end users about using Intune</link></caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_CODiOS">
        <title address="BKMK_COD">
          <caps:sentence sentenceid="af8d3858bba3a87d2a50083b6d7f2861" id="tgt56" class="tgtSentence">Administración de dispositivos de propiedad corporativa (COD) con Microsoft Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bc07529172931a63cba1fd1bc46c6d48" id="tgt57" class="tgtSentence">Como alternativa a la inscripción con la aplicación Portal de empresa, también puede inscribir los dispositivos iOS de empresa adquiridos en Apple.</caps:sentence>
            <caps:sentence sentenceid="01cd8279b69f2dce3837a39af943b7d2" id="tgt58" class="tgtSentence"> Intune permite inscribir dispositivos iOS de empresa con el programa de inscripción de dispositivos (DEP) de Apple o la herramienta <externalLink><linkText>Apple Configurator</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=518017</linkUri></externalLink> en ejecución en un equipo Mac.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="303586d3180bbe7d73c4789ae604f491" id="tgt59" class="tgtSentence">Puede inscribir dispositivos iOS de empresa de tres maneras:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="66e48cf6228a96c725492903193d5b13" id="tgt60" class="tgtSentence">
                  <ui>Programa de inscripción de dispositivos (DEP)</ui>: implementa un perfil de inscripción que inscribe el dispositivo “por aire” y puede incluir opciones de asistente para la instalación para el dispositivo.</caps:sentence>
                <caps:sentence sentenceid="9a61517ce0f241c2456f79f39b60eb29" id="tgt61" class="tgtSentence"> Los usuarios no pueden anular la inscripción de dispositivos inscritos a través de DEP.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c05e1907e5ef2790ae7fd1b827a0a9ee" id="tgt62" class="tgtSentence">
                  <ui>Inscripción con el asistente de configuración</ui>: restablece la configuración de fábrica del dispositivo y lo prepara para que el nuevo usuario del dispositivo lo instale.</caps:sentence>
                <caps:sentence sentenceid="a2489181211cd40c7f7a9f0cb189ec5e" id="tgt63" class="tgtSentence"> Este método admite inscripciones de DEP o de Apple Configurator.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9cf6caf947ad8544a85f03de2f2ce7a0" id="tgt64" class="tgtSentence">
                  <ui>Inscripción directa</ui>: crea un archivo compatible con Apple Configurator para su uso durante la preparación del dispositivo.</caps:sentence>
                <caps:sentence sentenceid="d0056eee143760d6143904bfaa0943af" id="tgt65" class="tgtSentence"> El dispositivo inscrito no tiene los valores predeterminados de fábrica restablecidos.</caps:sentence>
                <caps:sentence sentenceid="8a6abad11aeacfeb9cb4f9424d14651c" id="tgt66" class="tgtSentence"> Este método no puede usarse para la inscripción de DEP.</caps:sentence>
                <caps:sentence sentenceid="5dae8aa3eb9d2488964afa21f763dba7" id="tgt67" class="tgtSentence"> Este método sólo funciona si la afiliación de usuarios se define como "Sin afinidad de usuario".</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="caution">
            <para>
              <caps:sentence sentenceid="c46f23030048ec926619ee1040836db2" id="tgt68" class="tgtSentence">La aplicación Portal de empresa de Intune no se admite en dispositivos inscritos con estos métodos.</caps:sentence>
              <caps:sentence sentenceid="e655aad1fc688ed7e7e9b4eb7b7d8fa0" id="tgt69" class="tgtSentence"> Como resultado, ciertas capacidades de Intune como el <externalLink><linkText>acceso condicional</linkText><linkUri>https://technet.microsoft.com/library/dn818907.aspx</linkUri></externalLink> y la <externalLink><linkText>administración de aplicaciones móviles</linkText><linkUri>https://technet.microsoft.com/library/dn878026.aspx</linkUri></externalLink>, no están disponibles.</caps:sentence>
              <caps:sentence sentenceid="be797b8362b4426099b65097d3a01fe7" id="tgt70" class="tgtSentence"> De todos modos, todavía puede implementar las <externalLink><linkText>directivas</linkText><linkUri>https://technet.microsoft.com/library/mt346005.aspx</linkUri></externalLink>, los <externalLink><linkText>perfiles de acceso a recursos</linkText><linkUri>https://technet.microsoft.com/library/dn997277.aspx</linkUri></externalLink> y las <externalLink><linkText>aplicaciones necesarias</linkText><linkUri>https://technet.microsoft.com/library/dn646955.aspx</linkUri></externalLink> de Intune en estos dispositivos (excepto en <externalLink><linkText>aquellos que requieran la directiva MAM</linkText><linkUri>https://technet.microsoft.com/library/dn708489.aspx</linkUri></externalLink>).</caps:sentence>
              <caps:sentence sentenceid="aa8cd92386b4e8ba80a73c4fa7325453" id="tgt71" class="tgtSentence"> Para garantizar que en el futuro el Portal de empresa siga siendo compatible, debe configurar <ui>Solicitar afinidad de usuario</ui> para el perfil de inscripción de DEP y establecer un identificador de Apple en los dispositivos.</caps:sentence>
            </para>
          </alert>
        </content>
        <sections>
          <section expanded="false" address="BKMK_DEP">
            <title>
              <caps:sentence sentenceid="e2c15825bf5f1891c8787ce85f518f4d" id="tgt72" class="tgtSentence">Administración de DEP de Apple para dispositivos iOS con Microsoft Intune</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="7b19b8f5d166c0a92c4ec004a5378cba" id="tgt73" class="tgtSentence">Para administrar dispositivos iOS de empresa con el programa de inscripción de dispositivos (DEP) de Apple, la organización debe unirse a DEP de Apple y adquirir dispositivos a través de ese programa.</caps:sentence>
                <caps:sentence sentenceid="859f62e05d464031cd587313435d171e" id="tgt74" class="tgtSentence"> Puede consultar los detalles de este proceso en: <externalLink><linkText>https://deploy.apple.com</linkText><linkUri>https://deploy.apple.com</linkUri></externalLink>.</caps:sentence>
                <caps:sentence sentenceid="dca29e3e3595b6383789c50fbc1b548c" id="tgt75" class="tgtSentence"> Las ventajas del programa incluyen dispositivos configurados con manos libres sin necesidad de conectar por USB cada dispositivo a un equipo.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="6533f7e386680fd3c2f490bb5af5b9ed" id="tgt76" class="tgtSentence">Para poder inscribir dispositivos iOS de empresa con DEP, necesita un token de DEP de Apple.</caps:sentence>
                <caps:sentence sentenceid="5bc4c3b9ec25c012fc47f247c169a741" id="tgt77" class="tgtSentence"> Este token permite a Intune sincronizar información sobre dispositivos propiedad de la empresa que participan en DEP.</caps:sentence>
                <caps:sentence sentenceid="f5de4f6ef01442a525c733fa9e76be2c" id="tgt78" class="tgtSentence"> También permite a Intune realizar cargas de perfiles de inscripción a Apple y asignar dispositivos a esos perfiles.</caps:sentence>
              </para>
              <procedure address="BKMK_DEPtok" expanded="true">
                <title>
                  <caps:sentence sentenceid="9c06f7616ae353b64e3ae96c3dc0507f" id="tgt79" class="tgtSentence">Habilitar la administración de DEP con Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt80" class="tgtSentence">
                          <embeddedLabel>Empezar a administrar dispositivos iOS con Microsoft Intune</embeddedLabel>
                          <br />Para poder inscribir dispositivos del programa de inscripción de dispositivos (DEP) iOS, debe habilitar la opción de administación iOS para Intune.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt81" class="tgtSentence">
                          <embeddedLabel>Obtener una clave de cifrado</embeddedLabel>
                          <br />Como usuario administrativo, abra la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, vaya a <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui> &gt; <ui>iOS</ui> &gt; <ui>Programa de Inscripción de Dispositivos</ui> y haga clic en <ui>Descargar clave de cifrado</ui>.</caps:sentence>
                        <caps:sentence sentenceid="1657876527b3dbbd15423164ccb4828a" id="tgt82" class="tgtSentence"> Guarde el archivo de clave de cifrado (.pem) localmente.</caps:sentence>
                        <caps:sentence sentenceid="518eee79ba2c94f620e8c3917fedd64f" id="tgt83" class="tgtSentence"> El archivo .pem se usa para solicitar un certificado de relación de confianza en el portal del Programa de Inscripción de Dispositivos de Apple.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt84" class="tgtSentence">
                          <embeddedLabel>Obtener un token del programa de inscripción de dispositivos</embeddedLabel>
                          <br />Vaya al <externalLink><linkText>Portal del programa de inscripción de dispositivos</linkText><linkUri>https://deploy.apple.com</linkUri></externalLink> (https://deploy.apple.com) e inicie sesión con su identificador de Apple de empresa.</caps:sentence>
                        <caps:sentence sentenceid="ccdaa92f4f66f42dd6f31d1a6cbf4b7a" id="tgt85" class="tgtSentence"> Este identificador de Apple debe usarse posteriormente para renovar el token de DEP.</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt86" class="tgtSentence">En el <externalLink><linkText>portal del programa de inscripción de dispositivos</linkText><linkUri>https://deploy.apple.com</linkUri></externalLink>, vaya a <ui>Programa de inscripción de dispositivos</ui> &gt; <ui>Administrar servidores</ui> y, después, haga clic en <ui>Agregar servidor MDM</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="eb2d3f6b2893bd777f6281d9aadf569f" id="tgt87" class="tgtSentence">Escriba el <ui>nombre del servidor MDM</ui> y, a continuación, haga clic en <ui>Siguiente</ui>.</caps:sentence>
                            <caps:sentence sentenceid="8a9cfdefa9c750bb44ac703a3886fff4" id="tgt88" class="tgtSentence"> El nombre del servidor es su referencia para identificar el servidor MDM.</caps:sentence>
                            <caps:sentence sentenceid="d7655cb13f676b895984df544464d07e" id="tgt89" class="tgtSentence"> No es el nombre o la dirección URL del servidor de Microsoft Intune.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt90" class="tgtSentence">Se abre el cuadro de diálogo <ui>Agregar &lt;NombreDeServidor&gt;</ui>.</caps:sentence>
                            <caps:sentence sentenceid="9c246454e1fc1fdab04143e527678570" id="tgt91" class="tgtSentence"> Haga clic en <ui>Elegir archivo...</ui> para cargar el archivo .pem y, a continuación, haga clic en <ui>Siguiente</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt92" class="tgtSentence">En el cuadro de diálogo <ui>Agregar &lt;NombreDeServidor&gt;</ui> se muestra el vínculo <ui>Su token de servidor</ui>.</caps:sentence>
                            <caps:sentence sentenceid="ebaa63a6ec82a3b12bed6788a8db6fa5" id="tgt93" class="tgtSentence"> Descargue el archivo de token de servidor (.p7m) en el equipo y, a continuación, haga clic en <ui>Listo</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="b5ad22a3f2b4ecbe0dce991b29572b17" id="tgt94" class="tgtSentence">Este archivo de certificado (.p7m) se usa para establecer una relación de confianza entre los servidores de Intune y los del Programa de Inscripción de Dispositivos de Apple.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt95" class="tgtSentence">
                          <embeddedLabel>Agregar el token de DEP a Intune</embeddedLabel>
                          <br />En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, vaya a <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui> &gt; <ui>iOS</ui> &gt; <ui>Programa de inscripción de dispositivos</ui> y haga clic en <ui>Cargar el token de DEP</ui>.</caps:sentence>
                        <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt96" class="tgtSentence">
                          <ui>Busque</ui> el archivo de certificado (.p7m), escriba su <ui>ID de Apple</ui> y haga clic en <ui>Cargar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt97" class="tgtSentence">
                          <embeddedLabel>Agregar la directiva de inscripción de dispositivos corporativos</embeddedLabel>
                          <br />En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, vaya a <ui>Directiva</ui> &gt; <ui>Inscripción de dispositivos corporativos</ui> y, a continuación, haga clic en <ui>Agregar</ui>.</caps:sentence>
                        <caps:sentence sentenceid="fe87bded0fe1ea76cdbf038550f513f2" id="tgt98" class="tgtSentence"> Proporcione los detalles de <ui>General</ui>, incluidos los de <ui>Nombre</ui> y <ui>Descripción</ui>, especifique si los dispositivos asignados al perfil tienen afinidad de usuario o pertenecen a un grupo y, después, habilite la opción <ui>Configure los ajustes del Programa de inscripción de dispositivos para esta directiva</ui> para permitir el uso de DEP.</caps:sentence>
                        <caps:sentence sentenceid="90adbbe7112a5ab0269194573e650cc6" id="tgt99" class="tgtSentence"> Los <ui>paneles de Asistente para la instalación</ui> definen la configuración de dispositivos iOS que se definió durante la instalación.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt100" class="tgtSentence">
                          <embeddedLabel>Asignar dispositivos DEP para la administración</embeddedLabel> <br />Vaya al <externalLink><linkText>portal del programa de inscripción de dispositivos</linkText><linkUri>https://deploy.apple.com</linkUri></externalLink> (https://deploy.apple.com) e inicie sesión con su identificador de Apple corporativo.</caps:sentence>
                        <caps:sentence sentenceid="e97841d337def7d4f114dfc86090f795" id="tgt101" class="tgtSentence"> Vaya a <ui>Programa de implementación</ui> &gt; <ui>Programa de inscripción de dispositivos</ui> &gt; <ui>Administrar dispositivos</ui>.</caps:sentence>
                        <caps:sentence sentenceid="fd43d2b2cffc210b891f464f4921b741" id="tgt102" class="tgtSentence"> Especifique cómo va a <ui>elegir los dispositivos</ui>, proporcione información del dispositivo y especifique los detalles de cada dispositivo, como <ui>Número de serie</ui> y <ui>Número de pedido</ui>, o seleccione <ui>Cargar archivo CSV</ui>.</caps:sentence>
                        <caps:sentence sentenceid="2b3410399cbcb86430dd8ad616d8696a" id="tgt103" class="tgtSentence"> A continuación, seleccione <ui>Asignar al servidor</ui>, seleccione el &lt;NombreDeServidor&gt; especificado para Microsoft Intune y, después, haga clic en <ui>Aceptar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt104" class="tgtSentence">
                          <embeddedLabel>Distribuir los dispositivos a los usuarios</embeddedLabel>
                          <br />Los dispositivos corporativos pueden distribuirse ahora a los usuarios.</caps:sentence>
                        <caps:sentence sentenceid="c047818304e59c0bed2979b9fe6a2017" id="tgt105" class="tgtSentence"> Los dispositivos iOS quedan inscritos para su administración mediante Intune al activarlos.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt106" class="tgtSentence">
                          <embeddedLabel>Sincronizar dispositivos administrados mediante DEP</embeddedLabel>
                          <br />Como usuario administrativo, abra la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, vaya a <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui> &gt; <ui>iOS</ui> &gt; <ui>Programa de inscripción de dispositivos</ui> y haga clic en <ui>Sincronizar ahora</ui>.</caps:sentence>
                        <caps:sentence sentenceid="e521685a2d82c0736572d86bc825c0da" id="tgt107" class="tgtSentence"> Se envía una solicitud de sincronización a Apple.</caps:sentence>
                        <caps:sentence sentenceid="56fad6b34aab270bfd5fb76ed4c40fdc" id="tgt108" class="tgtSentence"> Para ver dispositivos administrados mediante DEP después de la sincronización, en la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> vaya a <ui>Grupos</ui> &gt; <ui>Todos los dispositivos corporativos</ui>.</caps:sentence>
                        <caps:sentence sentenceid="4f4f145aafdf6ea8a38164ebe7706661" id="tgt109" class="tgtSentence"> En el área de trabajo <ui>Dispositivos corporativos</ui>, el <ui>Estado</ui> de los dispositivos administrados es "No contactado" hasta que el dispositivo se enciendo y ejecute el Asistente de configuración para inscribir el dispositivo.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para></para>
            </content>
          </section>
          <section expanded="false" address="BKMK_SAE">
            <title address="BKMK_SA">
              <caps:sentence sentenceid="400b5892032c5309dd175dde8f6da95b" id="tgt110" class="tgtSentence">Inscripción de Asistente para la instalación para dispositivos iOS con Microsoft Intune</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="2fdd050619045997a791137f61fe47f1" id="tgt111" class="tgtSentence">Con el Configurador de Apple, puede restablecer los valores de fábrica de los dispositivos iOS y prepararlos para la configuración por parte del usuario nuevo del dispositivo.</caps:sentence>
                <caps:sentence sentenceid="99413736b48fdff24cccf85328ece4e9" id="tgt112" class="tgtSentence">  Este método requiere que conecte por USB el dispositivo iOS a un equipo Mac para configurar la inscripción corporativa.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="0dd941c23a980d534f8ae0a938374c08" id="tgt113" class="tgtSentence">Habilitar la inscripción del Asistente para la instalación con Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ebc4e07b040da274fbcd0bc615d552aa" id="tgt114" class="tgtSentence">
                          <embeddedLabel>Crear un grupo de dispositivos móviles</embeddedLabel> (opcional)<br /> Si su empresa requiere grupos de dispositivos móviles para ayudar a administrar los dispositivos, cree los grupos.</caps:sentence>
                        <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt115" class="tgtSentence">
                          <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="acc797d11fca324a82aa3399a1d16307" id="tgt116" class="tgtSentence">
                          <embeddedLabel>Crear un perfil para dispositivos</embeddedLabel>
                          <br />Un perfil de inscripción de dispositivo define la configuración que se aplica a un grupo de dispositivos.</caps:sentence>
                        <caps:sentence sentenceid="b9ede7eff33f96119a3ac603f27dc12c" id="tgt117" class="tgtSentence"> Si aún no lo tiene, cree un perfil de inscripción de dispositivo para los dispositivos iOS inscritos mediante Apple Configurator.</caps:sentence>
                        <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt118" class="tgtSentence">
                          <embeddedLabel>Pedir afiliación de usuario</embeddedLabel> debe habilitarse para la inscripción con el <embeddedLabel>Asistente de configuración</embeddedLabel></caps:sentence>
                      </para>
                      <procedure expanded="false">
                        <title>
                          <caps:sentence sentenceid="9bae58b04cbb48e75c02266a4ff67e98" id="tgt119" class="tgtSentence">Para crear un perfil</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt120" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, vaya a <ui>Directiva</ui> &gt; <ui>Dispositivos corporativos</ui> y haga clic en <ui>Agregar...</ui>.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="c5841209b5e1af5966e6f50e8b922d68" id="tgt121" class="tgtSentence">Especifique los detalles de los perfiles de dispositivo:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="eb5c0ebbf0b89afdaf5d416acd09c6d7" id="tgt122" class="tgtSentence">
                                      <ui>Nombre</ui>: nombre del perfil de inscripción de dispositivo.</caps:sentence>
                                    <caps:sentence sentenceid="b7ef49439a509c31852b9a0d01e95852" id="tgt123" class="tgtSentence"> (No es visible para los usuarios)</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="a1cd8cb3a38cc32d04335a01870505a4" id="tgt124" class="tgtSentence">
                                      <ui>Descripción</ui>: descripción del perfil de inscripción de dispositivo.</caps:sentence>
                                    <caps:sentence sentenceid="b7ef49439a509c31852b9a0d01e95852" id="tgt125" class="tgtSentence"> (No es visible para los usuarios)</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="4ba197cae6ce2742c6782177f7ec14f8" id="tgt126" class="tgtSentence">
                                      <ui>Afiliación de usuario</ui>: especifica cómo se inscriben los dispositivos.</caps:sentence>
                                  </para>
                                  <list class="bullet">
                                    <listItem>
                                      <para>
                                        <caps:sentence sentenceid="73e39fcd6baea45bba0130ed42e2ca9b" id="tgt127" class="tgtSentence">
                                          <ui>Pedir afinidad de usuario</ui>: el dispositivo se puede afiliar con un usuario durante la instalación inicial y, a continuación, se le puede permitir el acceso a los datos y al correo electrónico de la compañía como dicho usuario.</caps:sentence>
                                        <caps:sentence sentenceid="81d0f63fb1ef261fbabd677a8cbdbfb5" id="tgt128" class="tgtSentence"> Este modo admite varios escenarios:</caps:sentence>
                                      </para>
                                      <list class="bullet">
                                        <listItem>
                                          <para>
                                            <caps:sentence sentenceid="158b2bb95596a8b2e101914bc06f55ea" id="tgt129" class="tgtSentence">
                                              <embeddedLabel>Dispositivo personal de empresa</embeddedLabel>: elección de un dispositivo propio, o lo que se conoce como "Choose Your Own Device" (CYOD). Similar a dispositivos personales o de propiedad privada, pero el administrador tiene ciertos privilegios, incluidos permisos para borrar, restablecer, administrar y anular la inscripción del dispositivo.</caps:sentence>
                                            <caps:sentence sentenceid="a848a9defd944cd544f70b074baa28fc" id="tgt130" class="tgtSentence"> El usuario del dispositivo puede instalar aplicaciones y tiene la mayoría de los demás permisos para usar el dispositivo que no estén bloqueados por la directiva de administración.</caps:sentence>
                                          </para>
                                        </listItem>
                                        <listItem>
                                          <para>
                                            <caps:sentence sentenceid="49be8a789255cac55fa548939abee863" id="tgt131" class="tgtSentence">
                                              <embeddedLabel>Cuenta de administrador de inscripción de dispositivos</embeddedLabel>: el dispositivo se inscribe con una cuenta de administrador de Intune especial.</caps:sentence>
                                            <caps:sentence sentenceid="3ef7b21e1f79ec84211340a194171e9f" id="tgt132" class="tgtSentence"> Se puede administrar como una cuenta privada, pero solo un usuario que conozca las credenciales del administrador de inscripción puede instalar aplicaciones, borrar, restablecer, administrar y anular la inscripción del dispositivo.</caps:sentence>
                                            <caps:sentence sentenceid="92de4216dc2353f733b908abdb451504" id="tgt133" class="tgtSentence"> Para obtener información acerca de cómo inscribir un dispositivo compartido por varios usuarios mediante una cuenta común, consulte <link xlink:href="a23abc61-69ed-44f1-9b71-b86aefc6ba03">Manage multiple devices with the Device Enrollment Manager account in Microsoft Intune</link>.</caps:sentence>
                                          </para>
                                        </listItem>
                                      </list>
                                    </listItem>
                                    <listItem>
                                      <para>
                                        <caps:sentence sentenceid="5992ae9836efb2ffafa205548c222992" id="tgt134" class="tgtSentence">
                                          <ui>No hay afinidad de usuario</ui>: el dispositivo no tiene usuarios.</caps:sentence>
                                        <caps:sentence sentenceid="78db3c54fc60bd9cf01aff2b4a7cef52" id="tgt135" class="tgtSentence"> Utilice esta afiliación para dispositivos que realizan tareas sin tener acceso a datos de usuario local.</caps:sentence>
                                        <caps:sentence sentenceid="cd526861a67f51ac718d325082a51006" id="tgt136" class="tgtSentence"> Las aplicaciones que requieren una afiliación de usuario están deshabilitadas o no funcionarán.</caps:sentence>
                                      </para>
                                    </listItem>
                                  </list>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="18ca52d61820bdc1ed493a52272de540" id="tgt137" class="tgtSentence">
                                      <ui>Asignación previa de grupo de dispositivos</ui>: todos los dispositivos que implementan este perfil pertenecerán inicialmente a este grupo.</caps:sentence>
                                    <caps:sentence sentenceid="cde83324dc29c1397d43a5cca68b632f" id="tgt138" class="tgtSentence"> Puede reasignar los dispositivos después de la inscripción.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt139" class="tgtSentence">Haga clic en <ui>Guardar perfil</ui> para agregar el perfil.</caps:sentence>
                              </para>
                            </content>
                          </step>
                        </steps>
                      </procedure>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt140" class="tgtSentence">
                          <embeddedLabel>Agregar dispositivos iOS para inscribirse con el Asistente para la instalación</embeddedLabel>
                          <br />En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, vaya a <ui>Grupos</ui> &gt; <ui>Todos los dispositivos</ui> &gt; <ui>Todos los dispositivos corporativos</ui> &gt; <ui>Todos los dispositivos</ui> y, a continuación, haga clic en <ui>Agregar dispositivos...</ui>.</caps:sentence>
                        <caps:sentence sentenceid="a469a00e531ad5a950ccbf77329ef6ff" id="tgt141" class="tgtSentence"> Puede agregar dispositivos de dos maneras:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="b3ab63450ce495064c023cfe5759fd71" id="tgt142" class="tgtSentence">
                              <ui>Cargar un archivo CSV que contiene números de serie</ui>: cree una lista de valores separados por comas (.csv) con dos columnas sin encabezado, limitada a 5000 dispositivos o 5 MB por archivo csv.</caps:sentence>
                          </para>
                          <table>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="bfbece119c4ebdeaa62c597bf570bfa0" id="tgt143" class="tgtSentence">&lt;N.º de serie 1&gt;</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="4475fae3d6fd812f6fba2a5dd4ea2d77" id="tgt144" class="tgtSentence">&lt;Detalles del dispositivo n.º 1&gt;</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="b13d7b43c01db35f4aaeed065467ccdf" id="tgt145" class="tgtSentence">&lt;N.º de serie 2&gt;</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="ba042fefe56c341e10ab6566c3b93b2d" id="tgt146" class="tgtSentence">&lt;Detalles del dispositivo n.º 2&gt;</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                          <para>
                            <caps:sentence sentenceid="7317b085c8ded0a1c0ba8c0393754296" id="tgt147" class="tgtSentence">Este archivo .csv, cuando se ve en un editor de texto, aparece como:</caps:sentence>
                          </para>
                          <code>0000000,PO 1234 111111111,PO 1234</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="bd88b42b323e9214f1afc812a75ee49e" id="tgt148" class="tgtSentence">
                              <ui>Agregar manualmente los detalles del dispositivo</ui>: especifique el número de serie y los detalles de hasta cinco dispositivos</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <alert class="security note">
                        <para>
                          <caps:sentence sentenceid="a4eab771e92a33dd2ae7de19c93d9c23" id="tgt149" class="tgtSentence">Si posteriormente necesita quitar dispositivos corporativos de la administración de Intune, debe quitar el número de serie del dispositivo de Intune del grupo <ui>Dispositivos corporativos</ui> para deshabilitar la inscripción de dispositivos.</caps:sentence>
                          <caps:sentence sentenceid="d6f38db07610ce8fa1eef9cd9b0ff524" id="tgt150" class="tgtSentence">  Si Intune realiza un procedimiento de recuperación ante desastres en el momento en que se quitan los números de serie o en torno a este momento, se deberá comprobar que solo los números de serie de los dispositivos activos están presentes en ese grupo.</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence sentenceid="90c8fbbf77aa6bdaffe4da44c9d6b74d" id="tgt151" class="tgtSentence">A continuación, haga clic en <ui>Siguiente</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="e548b8791a1d73dffd98b12d4626dd3e" id="tgt152" class="tgtSentence">
                          <embeddedLabel>Seleccionar dispositivos para inscribir</embeddedLabel>
                          <br />Confirme los dispositivos que se van a inscribir.</caps:sentence>
                        <caps:sentence sentenceid="8fe436a601eba35979f18215474491db" id="tgt153" class="tgtSentence"> No se pueden importar los números de serie ya inscritos o inscritos por otros medios.</caps:sentence>
                        <caps:sentence sentenceid="9c246454e1fc1fdab04143e527678570" id="tgt154" class="tgtSentence"> Haga clic en <ui>Siguiente</ui> para continuar.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="2e049c44231f3c44b21cb6e9cb706108" id="tgt155" class="tgtSentence">
                          <embeddedLabel>Asignar perfil</embeddedLabel>
                          <br />Especifique el perfil que se va a asignar a los dispositivos agregados desde la lista de perfiles disponibles, consulte los <ui>detalles del perfil de inscripción</ui> y, a continuación, haga clic en <ui>Finalizar</ui>.</caps:sentence>
                        <caps:sentence sentenceid="81ece60872af3f969c39a425707dacc9" id="tgt156" class="tgtSentence"> Los dispositivos agregados manualmente pueden asignarse a cualquier perfil de inscripción, pero los dispositivos sincronizados por DEP deben asignarse a un perfil habilitado para DEP.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt157" class="tgtSentence">
                          <embeddedLabel>Seleccionar un perfil para implementarlo en dispositivos iOS</embeddedLabel>
                          <br />En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, vaya a <ui>Directiva</ui> &gt; <ui>Inscripción de dispositivos corporativos</ui> y, después, seleccione el perfil de dispositivo que desee implementar en los dispositivos móviles.</caps:sentence>
                        <caps:sentence sentenceid="9c246454e1fc1fdab04143e527678570" id="tgt158" class="tgtSentence"> Haga clic en <ui>Exportar...</ui> en la barra de tareas.</caps:sentence>
                        <caps:sentence sentenceid="4ceb43f79df040d4300a8e2e30701940" id="tgt159" class="tgtSentence"> Copie y guarde el valor de <ui>Dirección URL del perfil</ui>.</caps:sentence>
                        <caps:sentence sentenceid="1763a1b6edc15263f4520b9057943cec" id="tgt160" class="tgtSentence"> Se cargará en Apple Configurator más tarde para definir el perfil de Intune utilizado por los dispositivos iOS.</caps:sentence>
                        <caps:sentence sentenceid="932c9b669b63ffebc91c1180c4707b97" id="tgt161" class="tgtSentence"> En el caso de dispositivos DEP, simplemente ejecute el Asistente para la instalación desde una imagen de fábrica o el restablecimiento de fábrica en el dispositivo.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt162" class="tgtSentence">
                          <embeddedLabel>Preparar el dispositivo con Apple Configurator</embeddedLabel> <br />Los dispositivos iOS están conectados al equipo Mac e inscritos para la administración de dispositivos móviles.</caps:sentence>
                      </para>
                      <alert class="warning">
                        <para>
                          <caps:sentence sentenceid="1292ae22fd5925216374dcee3195e037" id="tgt163" class="tgtSentence">Los dispositivos se restablecerán en la configuración de fábrica durante el proceso de inscripción.</caps:sentence>
                        </para>
                      </alert>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="fa78982b11a039ebef612ccf782e3d6e" id="tgt164" class="tgtSentence">En un equipo Mac, abra <ui>Apple Configurator</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt165" class="tgtSentence">Seleccione <ui>Instalación</ui> y, después, <ui>Inscripción de dispositivo</ui>.</caps:sentence>
                            <caps:sentence sentenceid="83af9b8862f724f24c3ba8b77b30cbef" id="tgt166" class="tgtSentence"> Escriba la dirección URL de inscripción de Intune en <ui>Dirección URL del servidor MDM</ui> y, después, haga clic en <ui>Guardar</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="eca39e06ac153dd678a770b7ac24f5b6" id="tgt167" class="tgtSentence">Conecte los dispositivos móviles iOS al equipo Apple con un adaptador USB.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt168" class="tgtSentence">Haga clic en <ui>Preparar</ui>.</caps:sentence>
                            <caps:sentence sentenceid="63cc6cad24118fd0139628f67234cd27" id="tgt169" class="tgtSentence"> El progreso se muestra en Apple Configurator.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt170" class="tgtSentence">
                          <embeddedLabel>Distribuir los dispositivos</embeddedLabel> <br />Los dispositivos ya están listos para la inscripción corporativa.</caps:sentence>
                        <caps:sentence sentenceid="a82571872d951dfdb0399910be2ca824" id="tgt171" class="tgtSentence"> Apague los dispositivos y distribúyalos a los usuarios.</caps:sentence>
                        <caps:sentence sentenceid="adabb4668e75dd0d41029093f1ee5def" id="tgt172" class="tgtSentence"> Cuando el dispositivo se encienda, se iniciará el asistente de configuración y pedirá al usuario su cuenta profesional o educativa.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section expanded="false" address="BKMK_DE">
            <title>
              <caps:sentence sentenceid="372ffcb41dc94728fb209469e42de7d1" id="tgt173" class="tgtSentence">Inscripción directa para dispositivos iOS con Microsoft Intune</caps:sentence>
            </title>
            <content>
              <procedure expanded="true">
                <title>
                  <caps:sentence sentenceid="20e0e566a2b1a75b635a402c947949bc" id="tgt174" class="tgtSentence">Habilitar la inscripción directa con Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ebc4e07b040da274fbcd0bc615d552aa" id="tgt175" class="tgtSentence">
                          <embeddedLabel>Crear un grupo de dispositivos móviles</embeddedLabel> (opcional) <br />Si su empresa u organización requiere grupos de dispositivos móviles para ayudar a administrar los dispositivos, cree los grupos.</caps:sentence>
                        <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt176" class="tgtSentence">
                          <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="05a74595c45747647ca41f1c360cb075" id="tgt177" class="tgtSentence">
                          <embeddedLabel>Crear un perfil para dispositivos</embeddedLabel>
                          <br />Un perfil de inscripción de dispositivo define la configuración que se aplica a los dispositivos.</caps:sentence>
                        <caps:sentence sentenceid="b9ede7eff33f96119a3ac603f27dc12c" id="tgt178" class="tgtSentence"> Si aún no lo tiene, cree un perfil de inscripción de dispositivo para los dispositivos iOS inscritos mediante Apple Configurator.</caps:sentence>
                      </para>
                      <procedure expanded="false">
                        <title>
                          <caps:sentence sentenceid="9bae58b04cbb48e75c02266a4ff67e98" id="tgt179" class="tgtSentence">Para crear un perfil</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt180" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, vaya a <ui>Directiva</ui> &gt; <ui>Inscripción de dispositivos corporativos</ui> y, después, haga clic en <ui>Agregar...</ui>.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="c5841209b5e1af5966e6f50e8b922d68" id="tgt181" class="tgtSentence">Especifique los detalles de los perfiles de dispositivo:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="eb5c0ebbf0b89afdaf5d416acd09c6d7" id="tgt182" class="tgtSentence">
                                      <ui>Nombre</ui>: nombre del perfil de inscripción de dispositivo.</caps:sentence>
                                    <caps:sentence sentenceid="7431479182e53a65b8d811ae8f4e9dd5" id="tgt183" class="tgtSentence"> No es visible para los usuarios.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="a1cd8cb3a38cc32d04335a01870505a4" id="tgt184" class="tgtSentence">
                                      <ui>Descripción</ui>: descripción del perfil de inscripción de dispositivo.</caps:sentence>
                                    <caps:sentence sentenceid="7431479182e53a65b8d811ae8f4e9dd5" id="tgt185" class="tgtSentence"> No es visible para los usuarios.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="4ba197cae6ce2742c6782177f7ec14f8" id="tgt186" class="tgtSentence">
                                      <ui>Afiliación de usuario</ui>: especifica cómo se inscriben los dispositivos.</caps:sentence>
                                    <caps:sentence sentenceid="6e7df50c1e0ed37d9cb87faaeb5decae" id="tgt187" class="tgtSentence"> Para la inscripción directa, seleccione <ui>Sin afinidad usuario</ui>.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="18ca52d61820bdc1ed493a52272de540" id="tgt188" class="tgtSentence">
                                      <ui>Asignación previa de grupo de dispositivos</ui>: todos los dispositivos que implementan este perfil pertenecerán inicialmente a este grupo.</caps:sentence>
                                    <caps:sentence sentenceid="cde83324dc29c1397d43a5cca68b632f" id="tgt189" class="tgtSentence"> Puede reasignar los dispositivos después de la inscripción.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt190" class="tgtSentence">Haga clic en <ui>Guardar perfil</ui> para agregar el perfil.</caps:sentence>
                              </para>
                            </content>
                          </step>
                        </steps>
                      </procedure>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt191" class="tgtSentence">
                          <embeddedLabel>Seleccionar y exportar un archivo de perfil de inscripción</embeddedLabel>
                          <br />En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, vaya a <ui>Directiva</ui> &gt; <ui>Inscripción de dispositivos corporativos</ui> y, después, seleccione el perfil de dispositivo para implementar en los dispositivos iOS.</caps:sentence>
                        <caps:sentence sentenceid="9c246454e1fc1fdab04143e527678570" id="tgt192" class="tgtSentence"> Haga clic en <ui>Exportar...</ui> en la barra de tareas.</caps:sentence>
                        <caps:sentence sentenceid="90adbbe7112a5ab0269194573e650cc6" id="tgt193" class="tgtSentence"> Se abre la ventana <ui>Método de configuración de Apple</ui>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt194" class="tgtSentence">En <ui>Método de configuración de Apple</ui>, seleccione <ui>Inscripción directa</ui>.</caps:sentence>
                        <caps:sentence sentenceid="fe1f0736eeba01fcd192f7d2b301c79f" id="tgt195" class="tgtSentence"> Descargue y guarde el archivo de perfil de inscripción directa (.mobileconfig).</caps:sentence>
                        <caps:sentence sentenceid="44fe7250fdf8ba6b58e245dc8e026ece" id="tgt196" class="tgtSentence"> Debe importar este archivo a Apple Configurator para definir el perfil de Intune que utilizan los dispositivos iOS.</caps:sentence>
                        <caps:sentence sentenceid="6dc98b37bde440b088c4e90c0a55b6ca" id="tgt197" class="tgtSentence"> Un archivo de perfil de inscripción es válido durante 2 semanas.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt198" class="tgtSentence">
                          <embeddedLabel>Importar el archivo de perfil y preparar el dispositivo</embeddedLabel>
                          <br />Copie el archivo de perfil de inscripción de Intune (.mobileconfig) a un equipo Mac e importe el archivo en Apple Configurator.</caps:sentence>
                        <caps:sentence sentenceid="dfc6cac244df56e72916fc950395a007" id="tgt199" class="tgtSentence"> Ya puede conectar dispositivos iOS por USB para inscribirlos con Apple Configurator.</caps:sentence>
                        <caps:sentence sentenceid="d7acbbc3e21d580f0d4a635a65b9dd52" id="tgt200" class="tgtSentence"> Los dispositivos configurados con este archivo deben haber completado el Asistente para la instalación y deben tener una conexión a Internet al aplicar el archivo.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
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
          <caps:sentence id="src1" class="srcSentence">With <token>wit_nextref</token>, you can enable BYOD ("bring your own device") iOS device enrollment to give access to company email and apps to iPhone and iPad users.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Once users install the <token>wit_nextref</token> company portal app, their devices can be targeted with policy using the <token>wit_nextref</token> administration console.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence">  Before you can manage iOS devices, you must import an Apple Push Notification service (APNs) certificate from Apple.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> This certificate allows Intune to manage iOS devices and establishes an accredited and encrypted IP connection with the mobile device management authority services.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">As an alternative to enrollment with the Company Portal app, you can also <externalLink><linkText>enroll corporate-owned iOS devices</linkText><linkUri>https://technet.microsoft.com/en-US/library/dn408185.aspx#BKMK_CODiOS</linkUri></externalLink> .</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Prepare to manage iOS mobile devices with Microsoft Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">The following steps allow <token>wit_nextref</token> to manage iOS devices using the Company Portal.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src8" class="srcSentence">Set up iOS enrollment with Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">
                      <embeddedLabel>Set up Intune</embeddedLabel> <br />If you haven’t already, prepare for mobile device management by  <externalLink><linkText>setting the mobile device management authority</linkText><linkUri>https://technet.microsoft.com/library/mt346013.aspx</linkUri></externalLink> as <embeddedLabel>Microsoft Intune</embeddedLabel>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">
                      <embeddedLabel>Get a certificate signing request</embeddedLabel> <br />As an administrative user, open the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, go to <ui>Administration</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>iOS</ui> &gt; <ui>Upload an APNs Certificate</ui>, and click <ui>Download the APNs certificate request</ui>.</caps:sentence>
                    <caps:sentence id="src11" class="srcSentence"> Save the certificate signing request (.csr) file locally.</caps:sentence>
                    <caps:sentence id="src12" class="srcSentence"> The .csr file is used to request a trust relationship certificate from the Apple Push Certificates Portal.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="41179d1e-2fb6-4f01-954e-06aa4740fc06"></image>
                  </mediaLink>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">
                      <embeddedLabel>Get an Apple Push Notification service certificate</embeddedLabel>
                      <br />Go to the <externalLink target="_blank"><linkText>Apple Push Certificates Portal</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=269844</linkUri></externalLink> and sign in with your company Apple ID to create the APNs certificate using the .csr file.</caps:sentence>
                    <caps:sentence id="src14" class="srcSentence"> This Apple ID must be used in future to renew your APNs certificate.</caps:sentence>
                    <caps:sentence id="src15" class="srcSentence"> Download the APNs (.pem) certificate and save the file locally.</caps:sentence>
                    <caps:sentence id="src16" class="srcSentence"> This APNs certificate file is used to establish a trust relationship between the Apple Push Notification server and Intune’s mobile device management authority.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">
                      <embeddedLabel>Add the APNs certificate to Intune</embeddedLabel> <br />In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, go to <ui>Administration</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>iOS</ui> &gt; <ui>Upload an APNs Certificate</ui>, and click <ui>Upload the APNs certificate</ui>.</caps:sentence>
                    <caps:sentence id="src18" class="srcSentence">
                      <ui>Browse</ui> to the certificate (.pem) file and click <ui>Open</ui> and then enter your <ui>Apple ID</ui>.</caps:sentence>
                    <caps:sentence id="src19" class="srcSentence"> With the APNs certificate, Intune can enroll and manage iOS devices by pushing policy to enrolled mobile devices.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">
                      <embeddedLabel>Add Intune users</embeddedLabel> <br />The mobile device owner must be added to the account portal before devices can be enrolled.</caps:sentence>
                    <caps:sentence id="src21" class="srcSentence"> Log in to the <externalLink><linkText>Microsoft Intune Account Portal</linkText><linkUri>http://account.manage.microsoft.com</linkUri></externalLink>, click <ui>Add users</ui>, and select an option:</caps:sentence>
                  </para>
                  <para></para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">
                          <embeddedLabel>User</embeddedLabel>: To add a single user select <ui>New</ui> &gt; <ui>User</ui> and enter <ui>Details</ui>, <ui>Assign roles</ui>, <ui>Set user location</ui>, and then assign the user to a <ui>Group</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src23" class="srcSentence">
                          <embeddedLabel>Bulk add</embeddedLabel>: Create a .csv file (see samples files provided) and import it into the account portal.</caps:sentence>
                        <caps:sentence id="src24" class="srcSentence"> Specify roles, location, and group, and then create the accounts.</caps:sentence>
                        <caps:sentence id="src25" class="srcSentence"> Sample and blank .csv files can be downloaded from the account portal.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">You can also enable Active Directory or Azure Active Directory synchronization.</caps:sentence>
                    <caps:sentence id="src27" class="srcSentence"> For more information about integrating other Azure Active Directory users with Intune, see <externalLink><linkText>Directory synchronization roadmap</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=511540</linkUri></externalLink> or click <embeddedLabel>Other ways to add users</embeddedLabel> in the account portal.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">
                      <embeddedLabel>Create groups </embeddedLabel> (Optional)<br />Groups give flexibility for managing devices and users.</caps:sentence>
                    <caps:sentence id="src29" class="srcSentence"> You can set up groups to suit your organizational needs by geographic location, department, or hardware characteristics, for example.</caps:sentence>
                    <caps:sentence id="src30" class="srcSentence">   See <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <caps:sentence id="src31" class="srcSentence">
                    <para>
                      <embeddedLabel>Add policies for devices</embeddedLabel> (Optional)<br />Policies are groups of settings that control features on devices. Most MDM policies are platform specific. You create policies using templates  containing recommended or customized settings, and then deploy them to groups. See <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</para> </caps:sentence>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">
                      <embeddedLabel>Set device enrollment limit</embeddedLabel> (Optional) <br />To limit the number of mobile devices a user can enroll, log in to the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Enrollment rules</ui>.</caps:sentence>
                    <caps:sentence id="src33" class="srcSentence"> Select the maximum number of devices a user can enroll and then click <ui>Save</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">
                      <embeddedLabel>Set Company Portal settings </embeddedLabel>
                      <br /> You can customize the Intune Company Portal for your company.</caps:sentence>
                    <caps:sentence id="src35" class="srcSentence"> In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Admin</ui> &gt; <ui>Company Portal</ui>.</caps:sentence>
                    <caps:sentence id="src36" class="srcSentence"> Configure the following</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src37" class="srcSentence">Company Name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src38" class="srcSentence">IT department contact name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src39" class="srcSentence">IT department phone number</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src40" class="srcSentence">Additional information</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src41" class="srcSentence">Company privacy statement URL</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src42" class="srcSentence">Support website URL (not displayed)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src43" class="srcSentence">Website name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step address="BKMK_Terms">
                <content>
                  <para address="BKMK_TAC">
                    <caps:sentence id="src44" class="srcSentence">
                      <embeddedLabel>Set Terms and Conditions</embeddedLabel> <br />You can publish terms and conditions that your users will see when they first use the company portal from any device, whether or not that device is already enrolled.</caps:sentence>
                    <caps:sentence id="src45" class="srcSentence"> Users will have to accept those terms to access the portal.</caps:sentence>
                    <caps:sentence id="src46" class="srcSentence"> When you update the terms and conditions significantly and want users to see and accept them, you can mark the new terms and conditions as a new version, and users will go through the same process the next time they visit the portal.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <embeddedLabel>Company Portal</embeddedLabel> &gt; <embeddedLabel>Terms and Conditions</embeddedLabel>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">Specify the following:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src49" class="srcSentence">Require users to accept company terms and conditions before using the Company Portal</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src50" class="srcSentence">Title</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src51" class="srcSentence">Text for terms</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src52" class="srcSentence">Text to explain what it means if the user accepts</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">You can see <externalLink><linkText>details about  terms and condition </linkText><linkUri>https://technet.microsoft.com/library/mt405893.aspx</linkUri></externalLink>.</caps:sentence>
                    <caps:sentence id="src54" class="srcSentence">  You can also see which users have accepted the terms and conditions by using the <externalLink><linkText>Terms and conditions reports</linkText><linkUri>https://technet.microsoft.com/library/dn646977.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">
                      <embeddedLabel>Tell users how to get access to company resources with the company portal</embeddedLabel> <br /><link xlink:href="48914533-f138-4dc0-8b93-4cea3ac61f7b">What to tell your end users about using Intune</link></caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_CODiOS">
        <title address="BKMK_COD">
          <caps:sentence id="src56" class="srcSentence">Corporate-owned device (COD) management with Microsoft Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src57" class="srcSentence">As an alternative to enrollment with the Company Portal app, you can enroll corporate-owned devices purchased from Apple.</caps:sentence>
            <caps:sentence id="src58" class="srcSentence"> Intune supports the enrollment of corporate-owned iOS devices using the Apple Device Enrollment Program (DEP) or the <externalLink><linkText>Apple Configurator</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=518017</linkUri></externalLink> tool running on a Mac computer.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src59" class="srcSentence">You can enroll corporate-enrolled iOS devices in three ways:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src60" class="srcSentence">
                  <ui>Device Enrollment Program (DEP)</ui> – Deploys an enrollment profile that enrolls the device “over the air” and can include setup assistant options for the device.</caps:sentence>
                <caps:sentence id="src61" class="srcSentence"> Devices enrolled through DEP cannot be un-enrolled by users.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src62" class="srcSentence">
                  <ui>Setup Assistant Enrollment</ui> – Factory resets the device and prepares it for setup by the device’s new user.</caps:sentence>
                <caps:sentence id="src63" class="srcSentence"> This method supports DEP or Apple Configurator enrollments.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src64" class="srcSentence">
                  <ui>Direct Enrollment</ui> – Creates an Apple Configurator-compliant file for use during device preparation.</caps:sentence>
                <caps:sentence id="src65" class="srcSentence"> The enrolled device isn’t factory reset.</caps:sentence>
                <caps:sentence id="src66" class="srcSentence"> This method cannot be used for DEP enrollment.</caps:sentence>
                <caps:sentence id="src67" class="srcSentence"> This method only works if user affiliation is set to "No user affinity."</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="caution">
            <para>
              <caps:sentence id="src68" class="srcSentence">The Intune Company Portal app isn't supported on devices enrolled with these methods.</caps:sentence>
              <caps:sentence id="src69" class="srcSentence"> As a result, certain Intune capabilities such as <externalLink><linkText>Conditional Access</linkText><linkUri>https://technet.microsoft.com/library/dn818907.aspx</linkUri></externalLink> and <externalLink><linkText>Mobile Application Management</linkText><linkUri>https://technet.microsoft.com/library/dn878026.aspx</linkUri></externalLink> are unavailable.</caps:sentence>
              <caps:sentence id="src70" class="srcSentence"> You can still deploy Intune <externalLink><linkText>policies</linkText><linkUri>https://technet.microsoft.com/library/mt346005.aspx</linkUri></externalLink>, <externalLink><linkText>resource access profiles</linkText><linkUri>https://technet.microsoft.com/library/dn997277.aspx</linkUri></externalLink> and <externalLink><linkText>required apps</linkText><linkUri>https://technet.microsoft.com/library/dn646955.aspx</linkUri></externalLink> to these devices (excluding <externalLink><linkText>those that require MAM policy</linkText><linkUri>https://technet.microsoft.com/library/dn708489.aspx</linkUri></externalLink>).</caps:sentence>
              <caps:sentence id="src71" class="srcSentence"> To ensure future compatibility with the Company Portal, you should configure <ui>Prompt for User Affinity</ui> for your DEP enrollment profile and set an Apple ID on devices.</caps:sentence>
            </para>
          </alert>
        </content>
        <sections>
          <section expanded="false" address="BKMK_DEP">
            <title>
              <caps:sentence id="src72" class="srcSentence">Apple DEP  management for iOS devices with Microsoft Intune</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src73" class="srcSentence">To manage corporate-owned iOS devices with Apple’s Device Enrollment Program (DEP), your organization must join Apple DEP and acquire devices through that program.</caps:sentence>
                <caps:sentence id="src74" class="srcSentence"> Details of that process are available at:  <externalLink><linkText>https://deploy.apple.com</linkText><linkUri>https://deploy.apple.com</linkUri></externalLink>.</caps:sentence>
                <caps:sentence id="src75" class="srcSentence"> Advantages of the program include hands-free set up devices without USB-connecting each device to a computer.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src76" class="srcSentence">Before you can enroll corporate-owned iOS devices with DEP, you need a DEP Token from Apple.</caps:sentence>
                <caps:sentence id="src77" class="srcSentence"> This token allows Intune to sync information about DEP-participating devices owned by your corporation.</caps:sentence>
                <caps:sentence id="src78" class="srcSentence"> It also permits Intune to perform Enrollment Profile uploads to Apple and to assign devices to those profiles.</caps:sentence>
              </para>
              <procedure address="BKMK_DEPtok" expanded="true">
                <title>
                  <caps:sentence id="src79" class="srcSentence">Enable DEP management with Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">
                          <embeddedLabel>Start managing iOS devices with Microsoft Intune</embeddedLabel> <br />Before you can enroll iOS Device Enrollment Program (DEP) devices, you must complete enable iOS management for Intune.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">
                          <embeddedLabel>Get an Encryption Key</embeddedLabel> <br />As an administrative user, open the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, go to <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>iOS</ui> &gt; <ui>Device Enrollment Program</ui>, and click <ui>Download Encryption Key</ui>.</caps:sentence>
                        <caps:sentence id="src82" class="srcSentence"> Save the encryption key (.pem) file locally.</caps:sentence>
                        <caps:sentence id="src83" class="srcSentence"> The .pem file is used to request a trust-relationship certificate from the Apple Device Enrollment Program portal.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src84" class="srcSentence">
                          <embeddedLabel>Get a Device Enrollment Program token</embeddedLabel> <br />Go to the <externalLink><linkText>Device Enrollment Program Portal</linkText><linkUri>https://deploy.apple.com</linkUri></externalLink> (https://deploy.apple.com) and sign in with your company Apple ID.</caps:sentence>
                        <caps:sentence id="src85" class="srcSentence"> This Apple ID must be used in future to renew your DEP token.</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src86" class="srcSentence">In the <externalLink><linkText>Device Enrollment Program Portal</linkText><linkUri>https://deploy.apple.com</linkUri></externalLink> portal, go <ui>Device Enrollment Program</ui> &gt; <ui>Manage Servers</ui>, and then click <ui>Add MDM Server</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src87" class="srcSentence">Enter the <ui>MDM Server Name</ui> and then click <ui>Next</ui>.</caps:sentence>
                            <caps:sentence id="src88" class="srcSentence"> The server name is for your reference to identify the MDM server.</caps:sentence>
                            <caps:sentence id="src89" class="srcSentence"> It is not name or URL of the Microsoft Intune server.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src90" class="srcSentence">The <ui>Add &lt;ServerName&gt;</ui> dialog box opens.</caps:sentence>
                            <caps:sentence id="src91" class="srcSentence"> Click <ui>Choose File…</ui> to upload the .pem file and then click <ui>Next</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src92" class="srcSentence">The <ui>Add &lt;ServerName&gt;</ui> dialog box displays a <ui>Your Server Token</ui> link.</caps:sentence>
                            <caps:sentence id="src93" class="srcSentence"> Download the server token (.p7m) file to your computer, and then click <ui>Done</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src94" class="srcSentence">This certificate (.p7m) file is used to establish a trust relationship between Intune and Apple’s Device Enrollment Program servers.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">
                          <embeddedLabel>Add the DEP token to Intune</embeddedLabel> <br />In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, go to <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>iOS</ui> &gt; <ui>Device Enrollment Program</ui>, and click <ui>Upload the DEP Token</ui>.</caps:sentence>
                        <caps:sentence id="src96" class="srcSentence">
                          <ui>Browse</ui> to the certificate (.p7m) file, enter your <ui>Apple ID</ui>, and click <ui>Upload</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src97" class="srcSentence">
                          <embeddedLabel>Add the Corporate Device Enrollment Policy</embeddedLabel> <br />In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, go to <ui>Policy</ui> &gt; <ui>Corporate Device Enrollment</ui> and then click <ui>Add</ui>.</caps:sentence>
                        <caps:sentence id="src98" class="srcSentence"> Provide <ui>General</ui> details including <ui>Name</ui> and <ui>Description</ui>, specify whether devices assigned to the profile have user affinity or belong to a group, and then enable <ui>Configure Device Enrollment Program settings for this policy</ui> to support DEP.</caps:sentence>
                        <caps:sentence id="src99" class="srcSentence"> The <ui>Setup assistant panes</ui> define the iOS device settings configured during setup.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src100" class="srcSentence">
                          <embeddedLabel>Assign DEP Devices for Management</embeddedLabel> <br />Go to the <externalLink><linkText>Device Enrollment Program Portal</linkText><linkUri>https://deploy.apple.com</linkUri></externalLink> (https://deploy.apple.com) and sign in with your company Apple ID.</caps:sentence>
                        <caps:sentence id="src101" class="srcSentence"> Go <ui>Deployment Program</ui> &gt; <ui>Device Enrollment Program</ui> &gt; <ui>Manage Devices</ui>.</caps:sentence>
                        <caps:sentence id="src102" class="srcSentence"> Specify how you will <ui>Choose Devices</ui>, provide device information and specify details by device <ui>Serial Number</ui>, <ui>Order Number</ui>, or <ui>Upload CSV File</ui>.</caps:sentence>
                        <caps:sentence id="src103" class="srcSentence"> Next, select <ui>Assign to Server</ui> and select the &lt;ServerName&gt; specified for Microsoft Intune, and then click <ui>OK</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src104" class="srcSentence">
                          <embeddedLabel>Distribute devices to users</embeddedLabel> <br />Your corporate-owned devices can now be distributed to users.</caps:sentence>
                        <caps:sentence id="src105" class="srcSentence"> When an iOS device is turned on it will be enrolled for management by Intune.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src106" class="srcSentence">
                          <embeddedLabel>Synchronize DEP-Managed Devices</embeddedLabel> <br />As an administrative user, open the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, go to <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>iOS</ui> &gt; <ui>Device Enrollment Program</ui>, and click <ui>Sync now</ui>.</caps:sentence>
                        <caps:sentence id="src107" class="srcSentence"> A sync request is sent to Apple.</caps:sentence>
                        <caps:sentence id="src108" class="srcSentence"> To see DEP-managed devices after synchronization, in the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> go <ui>Groups</ui> &gt; <ui>All Corporate-Owned Devices</ui>.</caps:sentence>
                        <caps:sentence id="src109" class="srcSentence"> In the <ui>Corporate-owned Devices</ui> workspace, the <ui>State</ui> for managed devices reads “Not contacted” until the device is powered on and runs the Setup Assistant to enroll the device.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <para></para>
            </content>
          </section>
          <section expanded="false" address="BKMK_SAE">
            <title address="BKMK_SA">
              <caps:sentence id="src110" class="srcSentence">Setup Assistant  enrollment for iOS devices with Microsoft Intune</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src111" class="srcSentence">Using Apple Configurator you can factory reset iOS devices and prepares them for setup by the device’s new user.</caps:sentence>
                <caps:sentence id="src112" class="srcSentence">  This method requires you to USB-connect the iOS device to a Mac computer to setup corporate enrollment.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src113" class="srcSentence">Enable Setup Assistant enrollment with Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src114" class="srcSentence">
                          <embeddedLabel>Create mobile device group</embeddedLabel> (Optional) <br />If your business requires mobile device groups to help manage devices, create those groups.</caps:sentence>
                        <caps:sentence id="src115" class="srcSentence">
                          <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src116" class="srcSentence">
                          <embeddedLabel>Create a profile for devices</embeddedLabel>
                          <br />A device enrollment profile defines the settings applied to a group of devices.</caps:sentence>
                        <caps:sentence id="src117" class="srcSentence"> If you have not already, create a device enrollment profile for iOS devices enrolled using Apple Configurator.</caps:sentence>
                        <caps:sentence id="src118" class="srcSentence">
                          <embeddedLabel>Prompt for User Affiliation</embeddedLabel> should be enabled for <embeddedLabel>Setup Assistant</embeddedLabel> enrollment</caps:sentence>
                      </para>
                      <procedure expanded="false">
                        <title>
                          <caps:sentence id="src119" class="srcSentence">To create a profile</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src120" class="srcSentence">In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> go <ui>Policy</ui> &gt; <ui>Corporate Owned Devices</ui>, and then click <ui>Add…</ui>.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src121" class="srcSentence">Enter details for the device profiles:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src122" class="srcSentence">
                                      <ui>Name</ui> – Name of the device enrollment profile.</caps:sentence>
                                    <caps:sentence id="src123" class="srcSentence"> (Not visible to users)</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src124" class="srcSentence">
                                      <ui>Description</ui> - Description of the device enrollment profile.</caps:sentence>
                                    <caps:sentence id="src125" class="srcSentence"> (Not visible to users)</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src126" class="srcSentence">
                                      <ui>User affiliation</ui> – Specifies how devices are enrolled.</caps:sentence>
                                  </para>
                                  <list class="bullet">
                                    <listItem>
                                      <para>
                                        <caps:sentence id="src127" class="srcSentence">
                                          <ui>Prompt for user affinity</ui> – The device can be affiliated with a user during initial setup and could then be permitted to access company data and email as that user.</caps:sentence>
                                        <caps:sentence id="src128" class="srcSentence"> This mode supports a number of scenarios:</caps:sentence>
                                      </para>
                                      <list class="bullet">
                                        <listItem>
                                          <para>
                                            <caps:sentence id="src129" class="srcSentence">
                                              <embeddedLabel>Corporate-owned personal device</embeddedLabel> – “Choose Your Own Device” (CYOD) Similar to privately owned or personal devices but the administrator has certain privileges including permission to wipe, reset, administer, and unenroll the device.</caps:sentence>
                                            <caps:sentence id="src130" class="srcSentence"> The device’s user can install apps and has most other permissions for device use where not blocked by management policy.</caps:sentence>
                                          </para>
                                        </listItem>
                                        <listItem>
                                          <para>
                                            <caps:sentence id="src131" class="srcSentence">
                                              <embeddedLabel>Device enrollment manager account</embeddedLabel> – The device is enrolled using a special Intune administrator account.</caps:sentence>
                                            <caps:sentence id="src132" class="srcSentence"> It can be managed as a private account, but only a user who knows the enrollment manager credentials can install apps, wipe, reset, administer, and unenroll the device.</caps:sentence>
                                            <caps:sentence id="src133" class="srcSentence"> For information about enrolling a device shared by many users through a common account, see <link xlink:href="a23abc61-69ed-44f1-9b71-b86aefc6ba03">Manage multiple devices with the Device Enrollment Manager account in Microsoft Intune</link>.</caps:sentence>
                                          </para>
                                        </listItem>
                                      </list>
                                    </listItem>
                                    <listItem>
                                      <para>
                                        <caps:sentence id="src134" class="srcSentence">
                                          <ui>No user affinity</ui> – The device is user-less.</caps:sentence>
                                        <caps:sentence id="src135" class="srcSentence"> Use this affiliation for devices that perform tasks without accessing local user data.</caps:sentence>
                                        <caps:sentence id="src136" class="srcSentence"> Apps requiring user affiliation are disabled or won’t work.</caps:sentence>
                                      </para>
                                    </listItem>
                                  </list>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src137" class="srcSentence">
                                      <ui>Device group pre-assignment</ui> – All devices deployed this profile will initially belong to this group.</caps:sentence>
                                    <caps:sentence id="src138" class="srcSentence"> You can reassign devices after enrollment.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src139" class="srcSentence">Click <ui>Save Profile</ui> to add the profile.</caps:sentence>
                              </para>
                            </content>
                          </step>
                        </steps>
                      </procedure>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src140" class="srcSentence">
                          <embeddedLabel>Add iOS devices to enroll with Setup assistant</embeddedLabel>
                          <br />In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> go <ui>Groups</ui> &gt; <ui>All Devices</ui> &gt; <ui>All Corporate-owned Devices</ui> &gt; <ui>All Devices</ui>, and then click <ui>Add devices…</ui>.</caps:sentence>
                        <caps:sentence id="src141" class="srcSentence"> You can add devices in two ways:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src142" class="srcSentence">
                              <ui>Upload a CSV file containing serial numbers</ui> – Create a comma-separated value (.csv) list of two columns without a header, limited to 5000 devices or 5MB per csv file.</caps:sentence>
                          </para>
                          <table>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src143" class="srcSentence">&lt;Serial #1&gt;</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src144" class="srcSentence">&lt;Device #1 Details&gt;</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src145" class="srcSentence">&lt;Serial#2&gt;</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src146" class="srcSentence">&lt;Device #2 Details&gt;</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                          <para>
                            <caps:sentence id="src147" class="srcSentence">This .csv file when viewed in a text editor appears as:</caps:sentence>
                          </para>
                          <code>0000000,PO 1234 111111111,PO 1234</code>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src148" class="srcSentence">
                              <ui>Manually add device details</ui> - Enter the serial number and device details of up to five devices</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <alert class="security note">
                        <para>
                          <caps:sentence id="src149" class="srcSentence">If you must later remove corporate-owned devices from Intune management, you must remove the device serial number from Intune in the <ui>Corporate-owned devices</ui> group to disable device enrollment.</caps:sentence>
                          <caps:sentence id="src150" class="srcSentence">  If Intune performs a disaster recovery procedure on or around the time that serial numbers were removed, you will need to verify that only active devices’ serial numbers are present in that group.</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence id="src151" class="srcSentence">And then click <ui>Next</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src152" class="srcSentence">
                          <embeddedLabel>Select devices to enroll</embeddedLabel>
                          <br />Confirm the devices to enroll.</caps:sentence>
                        <caps:sentence id="src153" class="srcSentence"> Serial numbers already enrolled or enrolled by other means cannot be imported.</caps:sentence>
                        <caps:sentence id="src154" class="srcSentence"> Click <ui>Next</ui> to continue.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src155" class="srcSentence">
                          <embeddedLabel>Assign profile</embeddedLabel>
                          <br />Specify the profile to assign to added devices from the list of available profiles, review the <ui>Enrollment profile details</ui>, and then click <ui>Finish</ui>.</caps:sentence>
                        <caps:sentence id="src156" class="srcSentence"> Manually added devices can be assigned to any Enrollment profile, but DEP-synced devices must be assigned to a DEP-enabled profile.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src157" class="srcSentence">
                          <embeddedLabel>Select a profile to deploy to iOS devices</embeddedLabel>
                          <br />In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> go <ui>Policy</ui> &gt; <ui>Corporate Device Enrollment</ui>, and then select the device profile to deploy to mobile devices.</caps:sentence>
                        <caps:sentence id="src158" class="srcSentence"> Click <ui>Export…</ui> in the taskbar.</caps:sentence>
                        <caps:sentence id="src159" class="srcSentence"> Copy and save the <ui>Profile URL</ui>.</caps:sentence>
                        <caps:sentence id="src160" class="srcSentence"> You will upload it in Apple Configurator later to define the Intune profile used by iOS devices.</caps:sentence>
                        <caps:sentence id="src161" class="srcSentence"> For DEP devices, simply run Setup Assistant from a factory image or factory reset on the device.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src162" class="srcSentence">
                          <embeddedLabel>Prepare the device with Apple Configurator</embeddedLabel> <br />iOS devices are connected to the Mac computer and enrolled for mobile device management.</caps:sentence>
                      </para>
                      <alert class="warning">
                        <para>
                          <caps:sentence id="src163" class="srcSentence">The devices will be reset to factory configurations during the enrollment process.</caps:sentence>
                        </para>
                      </alert>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src164" class="srcSentence">On a Mac computer, open <ui>Apple Configurator</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src165" class="srcSentence">Select <ui>Setup</ui> and then <ui>Device Enrollment</ui>.</caps:sentence>
                            <caps:sentence id="src166" class="srcSentence"> Enter the enrollment URL from Intune in the <ui>MDM Server URL</ui>, and then click <ui>Save</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src167" class="srcSentence">Connect the iOS mobile devices to the Apple computer with a USB adapter.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src168" class="srcSentence">Click <ui>Prepare</ui>.</caps:sentence>
                            <caps:sentence id="src169" class="srcSentence"> Progress is displayed in Apple Configurator.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src170" class="srcSentence">
                          <embeddedLabel>Distribute devices</embeddedLabel> <br />The devices are now ready for corporate enrollment.</caps:sentence>
                        <caps:sentence id="src171" class="srcSentence"> Power down the devices and distribute them to users.</caps:sentence>
                        <caps:sentence id="src172" class="srcSentence"> When the device is turned on, the setup assistant will start and prompt the user for their work or school account.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section expanded="false" address="BKMK_DE">
            <title>
              <caps:sentence id="src173" class="srcSentence">Direct enrollment for iOS devices with Microsoft Intune</caps:sentence>
            </title>
            <content>
              <procedure expanded="true">
                <title>
                  <caps:sentence id="src174" class="srcSentence">Enable direct enrollment with Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src175" class="srcSentence">
                          <embeddedLabel>Create mobile device group</embeddedLabel> (Optional) <br />If your business or organization requires mobile device groups to help manage devices, create those groups.</caps:sentence>
                        <caps:sentence id="src176" class="srcSentence">
                          <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src177" class="srcSentence">
                          <embeddedLabel>Create a profile for devices</embeddedLabel>
                          <br />A device enrollment profile defines the settings applied to devices.</caps:sentence>
                        <caps:sentence id="src178" class="srcSentence"> If you have not already, create a device enrollment profile for iOS devices enrolled using Apple Configurator.</caps:sentence>
                      </para>
                      <procedure expanded="false">
                        <title>
                          <caps:sentence id="src179" class="srcSentence">To create a profile</caps:sentence>
                        </title>
                        <steps class="ordered">
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src180" class="srcSentence">In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> go <ui>Policy</ui> &gt; <ui>Corporate Device Enrollment</ui>, and then click <ui>Add…</ui>.</caps:sentence>
                              </para>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src181" class="srcSentence">Enter details for the device profiles:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src182" class="srcSentence">
                                      <ui>Name</ui> – Name of the device enrollment profile.</caps:sentence>
                                    <caps:sentence id="src183" class="srcSentence"> Not visible to users.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src184" class="srcSentence">
                                      <ui>Description</ui> - Description of the device enrollment profile.</caps:sentence>
                                    <caps:sentence id="src185" class="srcSentence"> Not visible to users.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src186" class="srcSentence">
                                      <ui>User affiliation</ui> – Specifies how devices are enrolled.</caps:sentence>
                                    <caps:sentence id="src187" class="srcSentence"> For Direct Enrollment, select <ui>No user affinity</ui>.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src188" class="srcSentence">
                                      <ui>Device group pre-assignment</ui> – All devices deployed this profile will initially belong to this group.</caps:sentence>
                                    <caps:sentence id="src189" class="srcSentence"> You can reassign devices after enrollment.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </content>
                          </step>
                          <step>
                            <content>
                              <para>
                                <caps:sentence id="src190" class="srcSentence">Click <ui>Save Profile</ui> to add the profile.</caps:sentence>
                              </para>
                            </content>
                          </step>
                        </steps>
                      </procedure>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src191" class="srcSentence">
                          <embeddedLabel>Select and export an enrollment profile file</embeddedLabel> <br />In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> go <ui>Policy</ui> &gt; <ui>Corporate Device Enrollment</ui>, and then select the device profile to deploy to your iOS devices.</caps:sentence>
                        <caps:sentence id="src192" class="srcSentence"> Click <ui>Export…</ui> in the taskbar.</caps:sentence>
                        <caps:sentence id="src193" class="srcSentence"> The <ui>Apple Configuration Method</ui> window opens.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src194" class="srcSentence">Under <ui>Apple configurator Method</ui>, select <ui>Direct enrollment</ui>.</caps:sentence>
                        <caps:sentence id="src195" class="srcSentence"> Download and save the direct enrollment profile file (.mobileconfig).</caps:sentence>
                        <caps:sentence id="src196" class="srcSentence"> You must import this file into Apple Configurator to define the Intune profile used by iOS devices.</caps:sentence>
                        <caps:sentence id="src197" class="srcSentence"> An enrollment profile file is valid for 2 weeks.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src198" class="srcSentence">
                          <embeddedLabel>Import the profile file and prepare the device</embeddedLabel> <br />Copy the Intune enrollment profile file (.mobileconfig) to a Mac computer and import the file into Apple Configurator.</caps:sentence>
                        <caps:sentence id="src199" class="srcSentence"> You can then USB-connect iOS devices to enroll them using Apple Configurator.</caps:sentence>
                        <caps:sentence id="src200" class="srcSentence"> Devices configured with this file must already have completed Setup Assistant and must have an internet connection when the file is applied.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>