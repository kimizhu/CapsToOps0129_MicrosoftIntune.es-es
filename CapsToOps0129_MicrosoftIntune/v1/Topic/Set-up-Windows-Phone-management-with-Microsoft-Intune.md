---
title: Configurar la administraci&#243;n de Windows Phone con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f
---
# Configurar la administraci&#243;n de Windows Phone con Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0a604f324c694ee705db618e2cc994e9" id="tgt1" class="tgtSentence">Para poder administrar dispositivos móviles de Windows Phone con <token>wit_nextref</token>, tendrá que configurar los requisitos de administración.</caps:sentence>
          <caps:sentence sentenceid="6f851c45e9fe79c5ab6de4130d2b9cbe" id="tgt2" class="tgtSentence"> La creación de un CNAME de DNS ayuda a los usuarios a conectarse al portal de empresa de <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence sentenceid="5048746af5eac71abe898d904199556e" id="tgt3" class="tgtSentence"> Windows Phone 8.0 requiere un certificado de Symantec para establecer una conexión de IP cifrada entre los dispositivos e <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence sentenceid="7596d820b20382b1f595d4fa01fc958a" id="tgt4" class="tgtSentence"> Windows Phone 8.1 también podría acceder al portal de empresa en función de cómo lo hagan los usuarios.</caps:sentence>
          <caps:sentence sentenceid="2d1734cd0fa2c65f906473cecceca448" id="tgt5" class="tgtSentence"> También es necesario un certificado para firmar aplicaciones de línea de negocio.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="2a52668cbd9bfc247e2bf159f9d980ce" id="tgt6" class="tgtSentence">
                <embeddedLabel>Windows Phone 8.1</embeddedLabel>: necesita un certificado solo si:</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence sentenceid="e22b0f840d2e0467c16eb174f11e04f2" id="tgt7" class="tgtSentence">Los usuarios no van a descargar el portal de empresa desde la Tienda.</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence sentenceid="f0de3decc6ae84fd99714b0ad425c29d" id="tgt8" class="tgtSentence">Va a implementar aplicaciones de línea de negocio (también denominadas "de instalación de prueba")</caps:sentence>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="323f02ea3fa5ad027c887ea625be0018" id="tgt9" class="tgtSentence">
                <embeddedLabel>Windows Phone 8</embeddedLabel>: necesario </caps:sentence>
            </para>
          </listItem>
        </list>
        <mediaLink>
          <image xlink:href="b457bc08-2634-4137-86f6-5f7cc330fbd2"></image>
        </mediaLink>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="d4e96b071977754f0ffe26a9bede39c0" id="tgt10" class="tgtSentence">Preparar la administración de dispositivos móviles Windows Phone con Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="37424f9fbd3c42659c22e62c71daf0f2" id="tgt11" class="tgtSentence">Los requisitos de instalación para la administración de dispositivos móviles de Windows Phone dependen de cómo se administrarán los dispositivos.</caps:sentence>
            <caps:sentence sentenceid="42c1899193d3a45f4bb620920c6b9b20" id="tgt12" class="tgtSentence">  Si se establecen dos CNAME en el registro DNS de la empresa, se facilita la inscripción para los usuarios.</caps:sentence>
            <caps:sentence sentenceid="f5b7fd6292695d16931124513f401587" id="tgt13" class="tgtSentence"> Si los usuarios van a descargar la aplicación de Portal de empresa desde la Tienda, una vez configure los ajustes de DNS, solo deberá configurar el Portal de empresa e informar a los usuarios sobre cómo inscribirse.</caps:sentence>
            <caps:sentence sentenceid="1ce89ba3e652aab3dc4cbc73697fd68e" id="tgt14" class="tgtSentence">  Para Windows Phone 8.0 o Windows Phone 8.1, donde va a implementar el Portal de empresa, necesitará un certificado de Symntec para firmar el código de la aplicación.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="27a772f8b3aee6a88266de7b2f38dd01" id="tgt15" class="tgtSentence">Configurar la inscripción de Windows Phone con Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt16" class="tgtSentence">
                      <embeddedLabel>Configurar <token>wit_nextref</token></embeddedLabel> <br />Si aún no lo hizo, prepare la administración de dispositivos móviles <externalLink><linkText>estableciendo la entidad de administración de dispositivos móviles</linkText><linkUri>https://technet.microsoft.com/library/mt346013.aspx</linkUri></externalLink> en <embeddedLabel>Microsoft Intune</embeddedLabel>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9781b62d0e687e3d5e772f805a335d75" id="tgt17" class="tgtSentence">
                      <embeddedLabel>Establecer un alias DNS para la dirección del servidor de inscripción</embeddedLabel> (opcional)<br /> </caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f560aa912f671a18f3703213593be7cb" id="tgt18" class="tgtSentence">Un alias DNS (tipo de registro CNAME) facilita a los usuarios la inscripción de sus dispositivos, ya que rellena automáticamente el nombre del servidor durante la inscripción.</caps:sentence>
                  </para>
                  <procedure>
                    <title>
                      <caps:sentence sentenceid="749993060a7e3a66e889394faf5c9e22" id="tgt19" class="tgtSentence">Comprobar y crear CNAME de DNS</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt20" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="5471ca9a49d6463fbc7f3306fe385bd7" id="tgt21" class="tgtSentence">Escriba la dirección URL del dominio comprobado del sitio web de empresa en el cuadro <ui>Especificar un nombre de dominio comprobado</ui> y, después, haga clic en <ui>Probar detección automática</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="e7791f265c2e6ed258d1beb636e351c5" id="tgt22" class="tgtSentence">Cree registros de recursos CNAME para el dominio de su empresa.</caps:sentence>
                            <caps:sentence sentenceid="e38c4e5bb6340155dd5172a5b1971886" id="tgt23" class="tgtSentence"> Los registros de recursos CNAME deben contener la siguiente información:</caps:sentence>
                          </para>
                          <table border="1">
                            <thead>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt24" class="tgtSentence">TYPE</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="7bac9dc63b9408f7043a63c902ca5bdf" id="tgt25" class="tgtSentence">Nombre de host</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="9a69c94d460695b849447f29c4698904" id="tgt26" class="tgtSentence">Apunta a</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="c431a4425bc56080c868435c8d910f83" id="tgt27" class="tgtSentence">TTL</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </thead>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="056301054c43f8bbea2090debfec16b1" id="tgt28" class="tgtSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence sentenceid="8e2237c00eca06c96d1d66c5a5b546c7" id="tgt29" class="tgtSentence">  <para>enterpriseenrollment.company_domain.com</para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="103f16169e6c5483d3c3522b5673024d" id="tgt30" class="tgtSentence">manage.microsoft.com
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="72ab9d0304d3e84c6aa2dd15eda282f2" id="tgt31" class="tgtSentence">1 hora</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="056301054c43f8bbea2090debfec16b1" id="tgt32" class="tgtSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt33" class="tgtSentence"> <para>enterpriseregistration.company_domain.com</para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="b8e596718f436b22e7d47c18522a0117" id="tgt34" class="tgtSentence">enterpriseregistration.windows.net
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="72ab9d0304d3e84c6aa2dd15eda282f2" id="tgt35" class="tgtSentence">1 hora</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                          <para>
                            <caps:sentence sentenceid="0ddb188e0c3d6f753fa556e387c3eedb" id="tgt36" class="tgtSentence">Por ejemplo, si el sitio web de la empresa es contoso.com, debe crear un CNAME en DNS que redirija EnterpriseEnrollment.contoso.com a manage.microsoft.com.</caps:sentence>
                            <caps:sentence sentenceid="74ebccfb9a34b27966e6e47a30e9a2ac" id="tgt37" class="tgtSentence"> Si hay más de un dominio comprobado, debe crear un registro CNAME para cada dominio.</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="fc2c4794f88183cd526fc7be558726b6" id="tgt38" class="tgtSentence">
                                  <codeInline>manage.microsoft.com</codeInline>: admite una redirección al servicio Intune con reconocimiento de dominio del nombre de dominio del correo electrónico.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="a2983dbe3d567d4058550acda540ca05" id="tgt39" class="tgtSentence">
                                  <codeInline>enterpriseregistration.windows.net</codeInline>: admite la unión al área de trabajo para dispositivos móviles.</caps:sentence>
                                <caps:sentence sentenceid="99fde62d77c6759ad6803da7822eab47" id="tgt40" class="tgtSentence"> También admite el acceso condicional para Windows 8.1.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                  <mediaLink>
                    <image xlink:href="33622fc8-d7ad-4f20-a4ec-c50de6a158bc"></image>
                  </mediaLink>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a596843407babf6e4c25e584affedd4b" id="tgt41" class="tgtSentence">
                      <embeddedLabel>Administración de certificados para admitir la firma de aplicaciones</embeddedLabel>
                      <br />[Requerido para los dispositivos de Windows Phone 8.0 y Windows Phone 8.1 que no accederán a la Tienda de Windows Phone y/o que necesitan aplicaciones de línea de negocio].</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="1ea59c51f5e88f231ce3342443a35380" id="tgt42" class="tgtSentence">Para admitir la aplicación Portal de empresa para Windows Phone 8.0 e implementar aplicaciones de empresa en Windows Phone 8.1, debe obtener un <embeddedLabel>certificado de firma de código móvil empresarial de Symantec</embeddedLabel>.</caps:sentence>
                    <caps:sentence sentenceid="1973c953a5aedfde14cbef8d3a7448e3" id="tgt43" class="tgtSentence"> No puede utilizar un certificado emitido por su propia entidad emisora de certificados porque el certificado de Symantec es el único que es de confianza para los dispositivos Windows Phone.</caps:sentence>
                    <caps:sentence sentenceid="2ff6639b8ad24df47cc02757d66f1c8a" id="tgt44" class="tgtSentence"> Este certificado se requiere para:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="eed648e5bed91d657e01816fdb7be98c" id="tgt45" class="tgtSentence">Firmar la aplicación Portal de empresa para su implementación en <token>winphone8_client_1</token> para la administración de inscripciones y teléfonos</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a4104207177adb1ac885342c9c759d74" id="tgt46" class="tgtSentence">Firmar aplicaciones de línea de negocio de empresa para que <token>wit_nextref</token> pueda implementarlas en dispositivos Windows Phone</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt47" class="tgtSentence">Para obtener más información, consulte <externalLink><linkText>Preguntas más frecuentes sobre la administración de dispositivos móviles de Windows Phone</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_FAQ</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="37e3d99e42a049de76e0dfebd9dfb8f9" id="tgt48" class="tgtSentence">Los pasos que figuran a continuación le ayudarán a obtener los certificados necesarios y a firmar la aplicación de portal de empresa.</caps:sentence>
                    <caps:sentence sentenceid="28646b41405959e87441d471b331ff11" id="tgt49" class="tgtSentence"> Necesitará una cuenta del Centro de desarrollo de Windows Phone y, a continuación, deberá adquirir un certificado de Symantec.</caps:sentence>
                  </para>
                  <procedure expanded="false" address="BKMK_CodeSign">
                    <title>
                      <caps:sentence sentenceid="ff3c52f78f7a2aa39610b4221277e835" id="tgt50" class="tgtSentence">Para obtener un certificado y firmar el código de Portal de empresa</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt51" class="tgtSentence">
                              <embeddedLabel>Unirse al Centro de desarrollo de Windows Phone</embeddedLabel> <br />Únase al <externalLink target="_blank"><linkText>Centro de desarrollo de Windows Phone</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268442</linkUri></externalLink> usando información de cuenta corporativa al iniciar sesión para comprar su cuenta de la compañía.</caps:sentence>
                            <caps:sentence sentenceid="a261c9138f990d03116c76f848cafd13" id="tgt52" class="tgtSentence"> Esta solicitud deberá estar autorizada por un oficial de la empresa antes de recibir un certificado de firma de código.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt53" class="tgtSentence">
                              <embeddedLabel>Obtener un certificado de empresa de Symantec</embeddedLabel> <br />Adquiera un certificado desde el <externalLink target="_blank"><linkText>sitio web de Symantec</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268441</linkUri></externalLink> mediante su identificador de Symantec.</caps:sentence>
                            <caps:sentence sentenceid="c139bb5145d959ef2cde38b0e3628817" id="tgt54" class="tgtSentence"> Después de adquirir el certificado, el aprobador corporativo que designase en su cuenta del Centro de desarrollo de Windows Phone recibirá un mensaje correo electrónico en el que se pide la aprobación de la solicitud de certificado.</caps:sentence>
                            <caps:sentence sentenceid="25dd18ac503217d095e40e9383a2e9c3" id="tgt55" class="tgtSentence"> Para obtener más información acerca del requisito de certificado de Symantec, consulte <externalLink><linkText>¿Por qué Windows Phone requiere un certificado de Symantec?</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_Symantec</linkUri></externalLink> Preguntas más frecuentes sobre la inscripción de dispositivos Windows.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt56" class="tgtSentence">
                              <embeddedLabel>Importar certificados</embeddedLabel> <br />Una vez que se apruebe la solicitud, recibirá un correo electrónico con instrucciones para la importación de certificados.</caps:sentence>
                            <caps:sentence sentenceid="203edf623515d6f2eae34af754786d57" id="tgt57" class="tgtSentence"> Siga las instrucciones indicadas en el correo electrónico para importar los certificados.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt58" class="tgtSentence">
                              <embeddedLabel>Comprobar los certificados importados</embeddedLabel> <br />Para comprobar que los certificados se importasen correctamente, vaya al complemento <ui>Certificados</ui>, haga clic con el botón derecho en <ui>Certificados</ui> y seleccione <ui>Buscar certificados</ui>.</caps:sentence>
                            <caps:sentence sentenceid="4f4f145aafdf6ea8a38164ebe7706661" id="tgt59" class="tgtSentence"> En el campo <ui>Contiene</ui>, escriba "Symantec" y haga clic en <ui>Buscar ahora</ui>.</caps:sentence>
                            <caps:sentence sentenceid="4f457d2e2b9d837831a16cf2dafd91fe" id="tgt60" class="tgtSentence"> Los certificados que haya importado deberían aparecer en los resultados.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="52f7f33c-987f-48ad-b661-d826489044cd"></image>
                            </mediaLinkInline>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt61" class="tgtSentence">
                              <embeddedLabel>Exportar un certificado de firma</embeddedLabel> <br />Después de comprobar que los certificados están presentes, puede exportar el archivo .pfx para firmar el portal de empresa.</caps:sentence>
                            <caps:sentence sentenceid="95b28e0eac464de8a1ea35219cdc8fd6" id="tgt62" class="tgtSentence"> Seleccione el certificado de Symantec con la “firma de código” <ui>Propósito planteado</ui>.</caps:sentence>
                            <caps:sentence sentenceid="9df574524024f4ac803c969217c4c6b1" id="tgt63" class="tgtSentence"> Haga clic con el botón derecho en el certificado de firma de código y seleccione <ui>Exportar</ui>.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="a5e198a5-7d2b-4797-bdfa-853a8e664b3c"></image>
                            </mediaLinkInline>
                          </para>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt64" class="tgtSentence">En el <ui>Asistente para exportar certificado</ui>, seleccione <ui>Sí, exportar la clave privada</ui> y, a continuación, haga clic en <ui>Siguiente</ui>.</caps:sentence>
                            <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt65" class="tgtSentence"> Seleccione <ui>Intercambio de información personal: PKCS #12 (.PFX)</ui> y active <ui>Si es posible, incluir todos los certificados en la ruta de acceso de certificación</ui>.</caps:sentence>
                            <caps:sentence sentenceid="476c3dffb6ddcfdd6308dcf7ac393bb6" id="tgt66" class="tgtSentence"> Complete el asistente.</caps:sentence>
                            <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt67" class="tgtSentence"> Para obtener más información, consulte <externalLink><linkText>Exportar un certificado con la clave privada</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=203031</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <embeddedLabel>
                              <caps:sentence sentenceid="09b777d4b84b7ca37eca8d47cb17a4f7" id="tgt68" class="tgtSentence">Descargar y firmar la aplicación Portal de empresa</caps:sentence>
                            </embeddedLabel>
                            <br />
                          </para>
                          <para>
                            <caps:sentence sentenceid="2fb11af53d6b4d40a30c696b128fe5fa" id="tgt69" class="tgtSentence">La compatibilidad para la inscripción de Windows Phone requiere que la aplicación Portal de empresa de Windows Phone 8.0 esté firmada y cargada en Intune.</caps:sentence>
                          </para>
                          <procedure expanded="true">
                            <title>
                              <caps:sentence sentenceid="5df8bc8d708ed06a1927b3b6dcff7f22" id="tgt70" class="tgtSentence">Windows Phone 8.0: descargar y firmar la aplicación Portal de empresa </caps:sentence>
                            </title>
                            <steps class="ordered">
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt71" class="tgtSentence">
                                      <embeddedLabel>Descargar Portal de empresa</embeddedLabel> <br />Descargue la aplicación <externalLink target="_blank"><linkText>Portal de empresa de Intune para Windows Phone</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink> desde el centro de descarga.</caps:sentence>
                                    <caps:sentence sentenceid="66a94af7ea41447f1131ef2d9f973fd4" id="tgt72" class="tgtSentence"> La ubicación de instalación predeterminada es <codeInline>C:\Program Files (x86)\Microsoft Corporation\Windows Intune Company Portal for Windows Phone</codeInline>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence sentenceid="23bd19fcedd382955bc35818765ace04" id="tgt73" class="tgtSentence">
                                      <embeddedLabel>Descargar el SDK de Windows Phone 8.0</embeddedLabel>
                                      <br />Descargue el <externalLink target="_blank"><linkText>SDK de Windows Phone</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt74" class="tgtSentence">
                                      <embeddedLabel>Firmar el código de la aplicación Portal de empresa</embeddedLabel> <br />Use la aplicación XAPSignTool descargada con el SDK para firmar el portal de empresa con el archivo .pfx creado mediante el certificado de Symantec.</caps:sentence>
                                    <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt75" class="tgtSentence"> Para obtener más información, consulte <externalLink target="_blank"><linkText>Cómo firmar una aplicación de la compañía mediante XapSignTool</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=280195</linkUri></externalLink>.</caps:sentence>
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
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt76" class="tgtSentence">
                              <embeddedLabel>Cargar la aplicación Portal de empresa en <token>wit_nextref</token></embeddedLabel> <br />Cargue el archivo de la aplicación Portal de empresa firmado y su certificado de firma de código para que la aplicación esté disponible para los usuarios finales.</caps:sentence>
                          </para>
                          <list class="ordered">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt77" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="41ad10da17628099ea69f30e0bc238ba" id="tgt78" class="tgtSentence">Haga clic en el <ui>Cargar archivo de aplicación firmado</ui> e inicie sesión con su identificador de administrador de <token>wit_nextref</token>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt79" class="tgtSentence">En la página <ui>Instalación de software</ui> de <ui>Especifique la ubicación de los archivos de instalación del software</ui>, vaya a la ubicación de la aplicación Portal de empresa (.xap para Windows Phone 8.0 o .appx para Windows Phone 8.1) con firma de código.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="a3dd3999c7c2f2311b445428e3279147" id="tgt80" class="tgtSentence">Si está evaluando <token>wit_nextref</token> y cargando un archivo de aplicación con código firmado en una cuenta de <token>wit_nextref</token> de evaluación, desactive la casilla <ui>Usar el archivo de aplicación Portal de empresa firmado por el certificado de firma de código Symantec de muestra</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="699e0486160e2a34fb947dc0d669fb82" id="tgt81" class="tgtSentence">Agregue el archivo de certificado (.pfx) que ha exportado a <ui>Certificado de firma de código</ui> y cree una contraseña para el certificado.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt82" class="tgtSentence">En la página <ui>Descripción del software</ui>, complete los campos teniendo en cuenta que los usuarios ven esta información en sus dispositivos cuando consultan los detalles en el Portal de empresa.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="2267545103c9e1387bf304a0df2c06f5" id="tgt83" class="tgtSentence">Complete el asistente.</caps:sentence>
                                <caps:sentence sentenceid="fa2ac8e896b35eb1e96d789e6f67fffc" id="tgt84" class="tgtSentence"> Los usuarios que inscriben un dispositivo Windows Phone 8.0 ahora obtendrán la aplicación Portal de empresa en sus dispositivos durante la inscripción.</caps:sentence>
                                <caps:sentence sentenceid="ba525c5963210483a84bfef0dd02203d" id="tgt85" class="tgtSentence"> Los usuarios de Windows Phone 8.1 pueden instalar la aplicación Portal de empresa desde la versión de la Tienda de Portal de empresa.</caps:sentence>
                                <caps:sentence sentenceid="d56409e2c2ed2fbf8715df89e747e428" id="tgt86" class="tgtSentence">  Si los dispositivos Windows Phone 8.1 están bloqueados en la Tienda de Windows Phone o desea implementar la aplicación Portal de empresa mediante Intune, debe descargar y firmar la aplicación Portal de empresa de Windows Phone 8.1 (SSP.appx).</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt87" class="tgtSentence">
                      <embeddedLabel>Agregar usuarios de Intune</embeddedLabel>
                      <br />El propietario del dispositivo móvil debe agregarse al Portal de cuentas de Microsoft Intune para poder inscribir dispositivos.</caps:sentence>
                    <caps:sentence sentenceid="4ad3f37ced51ee31a6023786a31e0a36" id="tgt88" class="tgtSentence"> Inicie sesión en el <externalLink><linkText>Portal de cuentas de Microsoft Intune</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=698854</linkUri></externalLink>, haga clic en <ui>Agregar usuarios</ui> y seleccione una opción:</caps:sentence>
                  </para>
                  <para></para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="18c21fa550c6e43924af228a0679d742" id="tgt89" class="tgtSentence">
                          <embeddedLabel>Usuario</embeddedLabel>: para agregar un solo usuario, seleccione <ui>Nuevo</ui> &gt; <ui>Usuario</ui> y especifique <ui>Detalles</ui>, <ui>Asignar roles</ui> y <ui>Establecer ubicación de usuario</ui>; a continuación, asigne el usuario a un <ui>Grupo</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a2f878d4f238f251d1ca75147c9c0fbf" id="tgt90" class="tgtSentence">
                          <embeddedLabel>Adición en masa</embeddedLabel>: cree un archivo .csv (vea los archivos de ejemplo proporcionados) e impórtelo al Portal de cuentas de Intune.</caps:sentence>
                        <caps:sentence sentenceid="c1b650589e7e36a0c106e31a527a915b" id="tgt91" class="tgtSentence"> Especifique los roles, la ubicación y el grupo y, después, cree las cuentas.</caps:sentence>
                        <caps:sentence sentenceid="310c151380683e4137bd81b5c16379fa" id="tgt92" class="tgtSentence"> Se pueden descargar archivos .csv en blanco y de ejemplo desde el Portal de cuentas de Microsoft Intune.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="665358b9ae967c6584e5f22475cbb77e" id="tgt93" class="tgtSentence">También puede habilitar la sincronización de Active Directory o Azure Active Directory.</caps:sentence>
                    <caps:sentence sentenceid="ccabfe774f8edea6ef04ff48472298c4" id="tgt94" class="tgtSentence"> Para obtener más información sobre la integración de otros usuarios de Azure Active Directory con Intune, consulte la <externalLink><linkText>Guía de sincronización de directorios</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=511540</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9781b62d0e687e3d5e772f805a335d75" id="tgt95" class="tgtSentence">
                      <embeddedLabel>Crear grupos </embeddedLabel> (opcional)<br />Los grupos ofrecen flexibilidad para administrar dispositivos y usuarios.</caps:sentence>
                    <caps:sentence sentenceid="507c76716449010dc59f1483e3964cd5" id="tgt96" class="tgtSentence"> Los grupos se pueden configurar según sus necesidades de organización (por ejemplo, por ubicación geográfica, departamento o características de hardware).</caps:sentence>
                    <caps:sentence sentenceid="e3d2410d4aed3acc53c4e7d50a0202e7" id="tgt97" class="tgtSentence">   Consulte <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt98" class="tgtSentence">
                    <para>
                      <embeddedLabel>Agregar directivas para dispositivos</embeddedLabel> (opcional)<br />Las directivas son grupos de configuraciones que controlan las características de los dispositivos. La mayoría de las directivas MDM son específicas de la plataforma. Las directivas se crean mediante plantillas que contienen configuraciones recomendadas o personalizadas y, luego, se implementan en grupos. Consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</para> </caps:sentence>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ebc4e07b040da274fbcd0bc615d552aa" id="tgt99" class="tgtSentence">
                      <embeddedLabel>Establecer el límite de inscripción de dispositivos</embeddedLabel> (opcional) <br />Para limitar el número de dispositivos móviles que puede inscribir un usuario, inicie sesión en la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui> &gt; <ui>Reglas de inscripción</ui>.</caps:sentence>
                    <caps:sentence sentenceid="81896f17af8e74876e83bdcbfb84232d" id="tgt100" class="tgtSentence"> Seleccione el número máximo de dispositivos que un usuario puede inscribir y haga clic en <ui>Guardar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="486bbd9b1c2d83f16fd091ae8a3e3110" id="tgt101" class="tgtSentence">
                      <embeddedLabel>Establecer la configuración del portal de empresa </embeddedLabel>
                      <br /> Puede personalizar Portal de empresa de Intune para su empresa.</caps:sentence>
                    <caps:sentence sentenceid="4f4f145aafdf6ea8a38164ebe7706661" id="tgt102" class="tgtSentence"> En la <externalLink><linkText>consola de administrador de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Portal de empresa</ui>.</caps:sentence>
                    <caps:sentence sentenceid="625a8686dac7b5297d90d5266d7fcd78" id="tgt103" class="tgtSentence"> Configure lo siguiente</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9bb4c85dfbafa8c61f627241bb21358c" id="tgt104" class="tgtSentence">Nombre de compañía</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="16576d71cb733d359db3b6e40b97b228" id="tgt105" class="tgtSentence">Nombre del contacto del departamento de TI</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="965d8e507652fcc1b19d4b13823cf800" id="tgt106" class="tgtSentence">Número de teléfono del departamento de TI</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt107" class="tgtSentence">Información adicional</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2ddf6ec5ba19603e0bbf4dd9dd16b1c5" id="tgt108" class="tgtSentence">Dirección URL de la declaración de privacidad de la empresa</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="07c657dc49d79de1aa99cc410449492d" id="tgt109" class="tgtSentence">Dirección URL del sitio web de soporte técnico (no se muestra)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ca75dc95767c2d020aba7b02bb2837c8" id="tgt110" class="tgtSentence">Nombre del sitio web</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step address="BKMK_Terms">
                <content>
                  <tokenBlock>CPEnrollmentTermsAndConditions</tokenBlock>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt111" class="tgtSentence">
                      <embeddedLabel>Indicar a los usuarios cómo acceder a los recursos de empresa con el portal de empresa</embeddedLabel> <br />Los usuarios necesitan saber cómo inscribir sus dispositivos y qué esperar una vez que se incorporan a la administración.</caps:sentence>
                    <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt112" class="tgtSentence">
                      <link xlink:href="48914533-f138-4dc0-8b93-4cea3ac61f7b">What to tell your end users about using Intune</link>
                    </caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="58f2e45a7f16fb7d9bb18f3e983eebf2" id="tgt113" class="tgtSentence">Implementar la aplicación Portal de empresa de Windows Phone 8.1</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a40f9fafcca406b45bc874831dbb4b58" id="tgt114" class="tgtSentence">Puede implementar la aplicación Portal de empresa en dispositivos Windows Phone 8.1 con <token>wit_nextref</token> en lugar de instalarla desde la Tienda Windows Phone.</caps:sentence>
                <caps:sentence sentenceid="60e7e9dcd9deab69d4aefb99d1eb669f" id="tgt115" class="tgtSentence"> Debe habilitar la inscripción de dispositivos de Windows Phone con los pasos anteriores usando el certificado de Symantec.</caps:sentence>
                <caps:sentence sentenceid="f2855d100c99c8677c7ce473fb8bb0fe" id="tgt116" class="tgtSentence"> A continuación, debe descargar la aplicación Portal de empresa de Windows Phone 8.1 y firmarla con el certificado de Symantec.</caps:sentence>
                <caps:sentence sentenceid="38239abcf1644ec61ea21beda72d8faa" id="tgt117" class="tgtSentence">  Esto solo es necesario si los usuarios no usan la Tienda de empresa y desea implementar el Portal de empresa en dispositivos Windows Phone 8.1.</caps:sentence>
              </para>
              <procedure expanded="false" address="BKMK_WP81appx">
                <title>
                  <caps:sentence sentenceid="593063f388f896f2b7939233bc0b76d1" id="tgt118" class="tgtSentence">Pasos para descargar y firmar la aplicación Portal de empresa de Windows Phone 8.1 para la implementación con Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt119" class="tgtSentence">
                          <embeddedLabel>Descargar Portal de empresa</embeddedLabel> <br /></caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="23bd19fcedd382955bc35818765ace04" id="tgt120" class="tgtSentence">Descargue la <externalLink target="_blank"><linkText>aplicación Portal de empresa de Microsoft Intune para Windows Phone 8.1</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink> desde el centro de descarga y ejecute el archivo autoextraíble (.exe).</caps:sentence>
                        <caps:sentence sentenceid="915293ff28ecd13258a5c246d8ff93e6" id="tgt121" class="tgtSentence"> Este archivo contiene dos archivos:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d3b17b87a0f03614ef445ef6e1871e7e" id="tgt122" class="tgtSentence">CompanyPortal.appx: aplicación de instalación de Portal de empresa para Windows Phone 8.1</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="9b70becfcf3be271def18686c811a1d5" id="tgt123" class="tgtSentence">WinPhoneCompanyPortal.ps1: script de PowerShell que se puede usar para firmar el archivo de aplicación de Portal de empresa para que se pueda implementar en dispositivos Windows Phone 8.1</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="23bd19fcedd382955bc35818765ace04" id="tgt124" class="tgtSentence">
                          <embeddedLabel>Descargar el SDK de Windows Phone</embeddedLabel>
                          <br />Descargue el <externalLink target="_blank"><linkText>SDK de Windows Phone 8.0</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink> (http://go.microsoft.com/fwlink/?LinkId=268439) e instálelo en el equipo.</caps:sentence>
                        <caps:sentence sentenceid="7c37c9028d2f59387e2b9f2db1452021" id="tgt125" class="tgtSentence"> Este SDK es necesario para generar un token de inscripción de aplicaciones.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="def41a67e2ddf550a1efd2f9dcbec355" id="tgt126" class="tgtSentence">
                          <embeddedLabel>Generar un archivo AETX</embeddedLabel>
                          <br />Genere un token de inscripción de aplicaciones (.aetx) a partir del archivo PFX de Symantec con AETGenerator.exe, parte del SDK de Windows Phone 8.0.</caps:sentence>
                        <caps:sentence sentenceid="ad2cb60a6fa7c1facec37cfb7a9c337b" id="tgt127" class="tgtSentence"> Para obtener instrucciones sobre cómo crear un archivo AETX, consulte <externalLink><linkText>Cómo generar un token de inscripción de aplicaciones para Windows Phone</linkText><linkUri>https://msdn.microsoft.com/library/windows/apps/jj735576.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="599f968755b3fd6fb4191c3386a799f0" id="tgt128" class="tgtSentence">
                          <embeddedLabel>Descargar Windows SDK para Windows 8.1</embeddedLabel>
                          <br />Descargue e instale el <externalLink target="_blank"><linkText>SDK de Windows Phone</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=613525</linkUri></externalLink> (http://go.microsoft.com/fwlink/?LinkId=613525).</caps:sentence>
                        <caps:sentence sentenceid="e052a473d1029072cf5b45d0ecd3934d" id="tgt129" class="tgtSentence"> Tenga en cuenta que el script de PowerShell incluido con la aplicación Portal de empresa usa la ubicación de instalación predeterminada, <codeInline>${env:ProgramFiles(x86)}\Windows Kits\8.1</codeInline>.</caps:sentence>
                        <caps:sentence sentenceid="2b4b5bf4ef49b31264c4644aca27912f" id="tgt130" class="tgtSentence"> Si lo instala en otra ubicación, deberá incluir dicha ubicación en un parámetro de cmdlet.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="c5aa190bef9dfa4cf52860037fb9a409" id="tgt131" class="tgtSentence">
                          <embeddedLabel>Firmar el código de la aplicación mediante PowerShell</embeddedLabel>
                          <br />Como administrador, abra <ui>Windows PowerShell</ui> en el equipo host donde están instalados Windows SDK y el certificado de firma de código móvil empresarial de Symantec, desplácese hasta el archivo Sign-WinPhoneCompanyPortal.ps1 y ejecute el script.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="e93b3fa481be3932aa08bd68c3deee70" id="tgt132" class="tgtSentence">Ejemplo 1</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -AetxPath 'C:\signing\cert.aetx'</code>
                      <para>
                        <caps:sentence sentenceid="99b6b6e0e44a19e34c86098e5979a3f0" id="tgt133" class="tgtSentence">Este ejemplo firma el archivo CompanyPortal.appx en C:\temp\ y genera el archivo CompanyPortalEnterpriseSigned.appx.</caps:sentence>
                        <caps:sentence sentenceid="e0571817898d04af0c95c719456cf5f3" id="tgt134" class="tgtSentence"> Usaría la contraseña de PFX 1234 y leería el identificador del editor del archivo PFX.</caps:sentence>
                        <caps:sentence sentenceid="0c83a38d77d189b78d21a6f71153363e" id="tgt135" class="tgtSentence"> También leería el identificador de la empresa del archivo cert.aetx.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="a6b23ee7f9c084154997ea3bf5b4c1e3" id="tgt136" class="tgtSentence">Ejemplo 2</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -PublisherId 'OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1' -EnterpriseId 1000000001</code>
                      <para>
                        <caps:sentence sentenceid="99b6b6e0e44a19e34c86098e5979a3f0" id="tgt137" class="tgtSentence">Este ejemplo firma el archivo CompanyPortal.appx en C:\temp\ y genera el archivo CompanyPortalEnterpriseSigned.appx.</caps:sentence>
                        <caps:sentence sentenceid="b38e6ecb4a008c1d5ae7bcddb70adb6d" id="tgt138" class="tgtSentence"> Usaría la contraseña de PFX 1234 y el identificador del editor especificado.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="bf987f0415d3fefd8fbfbb5a6ab3a60a" id="tgt139" class="tgtSentence">Parámetros:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="2154f1323d71cabff7d84e69486cbb99" id="tgt140" class="tgtSentence">
                              <codeInline>-InputAppx</codeInline>: ruta de acceso local al archivo CompanyPortal.appx entre comillas simples.</caps:sentence>
                            <caps:sentence sentenceid="8e7c82dcb51ef0a29f4c91c6d48afda8" id="tgt141" class="tgtSentence"> Por ejemplo, 'C:\temp\CompanyPortal.appx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="db0f98a70046962795dda19d1353f7d7" id="tgt142" class="tgtSentence">
                              <codeInline>-OutputAppx</codeInline>: ruta de acceso local y nombre de archivo de la aplicación Portal de empresa firmada entre comillas simples.</caps:sentence>
                            <caps:sentence sentenceid="0403882cb14e21a75053b8fe46e4660f" id="tgt143" class="tgtSentence"> Por ejemplo, 'C:\temp\CompanyPortalEnterpriseSigned.appx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="37406b23da0c95feeadffe0ed2f2e2f2" id="tgt144" class="tgtSentence">
                              <codeInline>-PfxFilePath</codeInline>: ruta de acceso local y nombre de archivo del archivo PFX exportado del certificado de Symantec.</caps:sentence>
                            <caps:sentence sentenceid="cb7e1c17fd7fbccdfee34f6ec3517046" id="tgt145" class="tgtSentence"> Por ejemplo, 'C:\signing\cert.pfx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="608a28ced851bec9f91fd064f5951e1a" id="tgt146" class="tgtSentence">
                              <codeInline>-PfxPassword</codeInline>: contraseña usada para firmar el archivo PFX entre comillas simples.</caps:sentence>
                            <caps:sentence sentenceid="a1c69f54fcc3343fbe05ee9e1b639a7b" id="tgt147" class="tgtSentence"> Por ejemplo, '1234'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="a2ae2bbf3241fcd3cbad4e21210007ae" id="tgt148" class="tgtSentence">
                              <codeInline>-AetxPath</codeInline>: ruta de acceso local al archivo .aetx que se usa para leer el identificador de empresa si el argumento 'EnterpriseId' no está definido.</caps:sentence>
                            <caps:sentence sentenceid="8026272ac081154b279b2ec9d1f56295" id="tgt149" class="tgtSentence"> Debe proporcionar este argumento o el identificador de la empresa.</caps:sentence>
                            <caps:sentence sentenceid="92ed377af9bc50371ea5446337c47cdb" id="tgt150" class="tgtSentence"> Por ejemplo, 'C:\signing\cert.aetx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0054ce9e0acf26959d5f7755005669f8" id="tgt151" class="tgtSentence">
                              <codeInline>-PublisherId</codeInline>: identificador del editor de la empresa.</caps:sentence>
                            <caps:sentence sentenceid="e57c41ca30767da4088e84d285ebea57" id="tgt152" class="tgtSentence"> Si está ausente, se usa el campo 'Asunto' del certificado de firma de código móvil empresarial de Symantec.</caps:sentence>
                            <caps:sentence sentenceid="447aa2f9d4781de497f6fe66f1dd35af" id="tgt153" class="tgtSentence"> Por ejemplo, 'OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0eaa511e60ba861b2b429991814e3b4e" id="tgt154" class="tgtSentence">
                              <codeInline>-SdkPath</codeInline>: ruta de acceso a la carpeta raíz de Windows SDK para Windows 8.1.</caps:sentence>
                            <caps:sentence sentenceid="4e16b4deaf8c428580187b116de8d533" id="tgt155" class="tgtSentence"> Este argumento es opcional y está establecido de forma predeterminada en ${env:ProgramFiles(x86)}\Windows Kits\8.1.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="72598cc79faa20a87ad1c8e33e9d7214" id="tgt156" class="tgtSentence">
                              <codeInline>-EnterpriseId</codeInline>: identificador de la empresa.</caps:sentence>
                            <caps:sentence sentenceid="07968656625d1c14a856a4e62db43118" id="tgt157" class="tgtSentence"> Debe proporcionar este argumento o 'AetxPath'.</caps:sentence>
                            <caps:sentence sentenceid="4180f108ac1f3ae2e8d9735c058f6773" id="tgt158" class="tgtSentence"> Si no se proporciona este argumento, el identificador de la empresa se lee del archivo AETX.</caps:sentence>
                            <caps:sentence sentenceid="1ff4112e83e346066d3e4ba0d4c33bc1" id="tgt159" class="tgtSentence"> Por ejemplo, 1000000001</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="78ed0e740ca082d18b5b55d5445d1cda" id="tgt160" class="tgtSentence">Implemente la aplicación Portal de empresa de Windows Phone 8.1 (SSP.appx).</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence sentenceid="660dbabe465935d074e99c94422cbe4e" id="tgt161" class="tgtSentence">Tanto el ssp.xap y como el Portal de empresa desde la tienda pueden instalarse al mismo tiempo, lo que puede resultar confuso para los usuarios.</caps:sentence>
                          <caps:sentence sentenceid="7b153146551f60db93bc0d7b4ee78bf9" id="tgt162" class="tgtSentence"> Para que todos los usuarios usen ssp.xap, cree una aplicación bloqueada para la versión de la tienda del Portal de empresa.</caps:sentence>
                          <caps:sentence sentenceid="42234178a8dc0432f4f0234ce726c309" id="tgt163" class="tgtSentence"> Para que todos los dispositivos Windows Phone 8.1 usen solo la versión de la tienda del Portal de empresa, tiene tres opciones:</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="d21d43181a8ebfa6f82099e6abbea447" id="tgt164" class="tgtSentence">Si no desea realizar una instalación de prueba de las aplicaciones y no necesita admitir Windows Phone 8.0, no cargue el ssp.xap firmado.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="11fc13be9f3cde7c629ce0337906461a" id="tgt165" class="tgtSentence">Si se necesitan aplicaciones con instalación de prueba y si no se está inscribiendo ningún dispositivo Windows Phone 8, cambie la implementación de ssp.xap creada automáticamente de "disponible" a "desinstalar".</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="14c0fdbc4a0ce4ce8ddfbda28f481f4e" id="tgt166" class="tgtSentence">Si es necesario instalar aplicaciones con instalación de prueba y se deben inscribir dispositivos Windows Phone 8.0, que deben recibir el ssp.xap, cree una nueva implementación de software del ssp.xap e impleméntela con la acción <ui>desinstalar</ui>.</caps:sentence>
                              <caps:sentence sentenceid="2ceab1c373f1181739ed568303dc2ba4" id="tgt167" class="tgtSentence"> Los dispositivos Windows Phone 8.0 no admiten la instalación o desinstalación forzada de aplicaciones, por lo que ignorarán la implementación.</caps:sentence>
                              <caps:sentence sentenceid="3af88cba174c19fa141be3b55f0598c5" id="tgt168" class="tgtSentence"> Los dispositivos Windows Phone 8.1 admiten la acción desinstalar y quitarán el ssp.xap.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0ae8e358ce25de11f47161cfaf786819" id="tgt169" class="tgtSentence">Renovar el certificado de firma de código de a de Symantec para dispositivos Windows</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="51bfdd2c469f2f32f7ee1784438cc90c" id="tgt170" class="tgtSentence">Debe renovar periódicamente el certificado de Symantec que se utiliza para administrar determinados dispositivos móviles Windows y Windows Phone.</caps:sentence>
            <caps:sentence sentenceid="326cb7aa260d149bc539350181b33bac" id="tgt171" class="tgtSentence"> En el caso de los dispositivos Windows Phone 8.0, para inscribir dispositivos se necesitan una aplicación Portal de empresa firmada y el certificado de firma de código.</caps:sentence>
            <caps:sentence sentenceid="80ae8b75cfe475eff3037cedfc65ee80" id="tgt172" class="tgtSentence"> Posteriormente, los dispositivos Windows Phone pueden utilizar la aplicación del portal de empresa descargada desde la tienda.</caps:sentence>
            <caps:sentence sentenceid="0e1f6a8e9350b2b4e355406fb6b90232" id="tgt173" class="tgtSentence"> Puede que también se necesite un certificado de firma de código para implementar aplicaciones de línea de negocio.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="779e8425c55023567c0632d6ab4473af" id="tgt174" class="tgtSentence">Cómo renovar el certificado de firma de código de empresa de Symantec</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="02971f9aca16d5e2a7ce66fb3ca89d07" id="tgt175" class="tgtSentence">Busque un correo electrónico de renovación enviado desde Symantec aproximadamente 14 días antes de la expiración del certificado.</caps:sentence>
                    <caps:sentence sentenceid="ea9c74b6105f1c78a125f30f5ae444a1" id="tgt176" class="tgtSentence"> Este mensaje de correo contiene instrucciones de Symantec sobre cómo renovar el certificado de empresa.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="bb5af1c3a6d60b4947f070de9780726c" id="tgt177" class="tgtSentence">Para obtener información adicional sobre certificados de Symantec, visite <externalLink><linkText>www.symantec.com</linkText><linkUri>http://www.symantec.com</linkUri></externalLink> o llame al 1-877-438-8776 o al 1-650-426-3400.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="8a20404fb2a9dceb5dc3641a00eb463b" id="tgt178" class="tgtSentence">Vaya al sitio web (ejemplo: <externalLink><linkText>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkText><linkUri>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkUri></externalLink>) e inicie sesión con el identificador de editor de Symantec y el correo electrónico asociado al certificado que recibió.</caps:sentence>
                    <caps:sentence sentenceid="a9387d7047bd71af5ca17dc633e94791" id="tgt179" class="tgtSentence"> Recuerde que para iniciar la renovación debe usar el mismo equipo que va a utilizar para descargar el certificado.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d4099a7d6380929b7b5c6b5a6623ae09" id="tgt180" class="tgtSentence">Una vez aprobada y pagada por la renovación, descargue el certificado.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="b922e0fb4a86449b6aff176e41af7e88" id="tgt181" class="tgtSentence">Cómo instalar el certificado actualizado para Windows Phone 8.0</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="444257c164a32b232b9ede0412edc362" id="tgt182" class="tgtSentence">Descargue y firme la aplicación Portal de empresa de Windows Phone más reciente que encontrará aquí: <externalLink><linkText>http://www.microsoft.com/es-es/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="84f8df8e69faaf38b6a258b5e17b3926" id="tgt183" class="tgtSentence">Abra la consola de administración de Intune (<externalLink><linkText>https://admin.manage.microsoft.com</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink>), vaya a <ui>Administración</ui>, <ui>Administración de dispositivos móviles</ui> &gt; <ui>Windows Phone</ui> y haga clic en <ui>Cargar aplicación firmada</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fd66cd717e159db47ce295d4bcd12623" id="tgt184" class="tgtSentence">Cargue el Portal de empresa recién firmado.</caps:sentence>
                    <caps:sentence sentenceid="6f3395584021182930fb87574e71da98" id="tgt185" class="tgtSentence"> Necesitará el archivo SSP.xap recién firmado y el nuevo archivo .PFX que recibió de Symantec o el token de inscripción de la aplicación que se creó con este nuevo archivo .PFX.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="5101a1da5de5102b696fa683c6c7c620" id="tgt186" class="tgtSentence">Una vez finalizada la carga, quite la versión antigua de Portal de empresa en el área de trabajo <ui>Software</ui> de la consola de administración de Intune.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1d2af3b8610e8640021243c7527825f7" id="tgt187" class="tgtSentence">Firme de nuevo todas las aplicaciones de línea de negocio de empresa con el mismo certificado y cargue y reemplace las aplicaciones existentes.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="c1cf3e547f3444db486cda0bccd743ad" id="tgt188" class="tgtSentence">Proporcionar un archivo firmado SSP.xap es actualmente la única manera de facilitar el certificado de firma de código actualizado.</caps:sentence>
                  <caps:sentence sentenceid="615a79d1519ef0e08e059151c7c938f3" id="tgt189" class="tgtSentence"> Para admitir aplicaciones de línea de negocio firmadas, deberá firmar y cargar una aplicación Portal de empresa, aunque los usuarios instalen la aplicación Portal de empresa desde la Tienda.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="3761619c03e867047963ca0a54e469c8" id="tgt190" class="tgtSentence">Cómo instalar el certificado actualizado para Windows Phone 8.1 y dispositivos posteriores</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="b524d5abe0e85f658b0662dc161112b8" id="tgt191" class="tgtSentence">Descargue y firme la aplicación Portal de empresa de Windows Phone más reciente del centro de descarga que encontrará aquí: <externalLink><linkText>http://www.microsoft.com/es-es/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="41ab81aedec29d904a088b53214e2e6b" id="tgt192" class="tgtSentence">Abra la <externalLink><linkText>consola de administración de Intune</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink> (https://admin.manage.microsoft.com), vaya a <ui>Administración</ui> &gt; <ui>Administración de dispositivos móviles</ui> &gt; <ui>Windows Phone</ui> y haga clic en <ui>Cargar aplicación firmada</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fd66cd717e159db47ce295d4bcd12623" id="tgt193" class="tgtSentence">Cargue el Portal de empresa recién firmado.</caps:sentence>
                    <caps:sentence sentenceid="6f3395584021182930fb87574e71da98" id="tgt194" class="tgtSentence"> Necesitará el archivo SSP.xap recién firmado y el nuevo archivo .PFX que recibió de Symantec o el token de inscripción de la aplicación que se creó con este nuevo archivo .PFX.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="5101a1da5de5102b696fa683c6c7c620" id="tgt195" class="tgtSentence">Una vez finalizada la carga, quite la versión antigua de Portal de empresa del área de trabajo <ui>Software</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1ab4bf40c46f0ac064fb574c89e0f60e" id="tgt196" class="tgtSentence">Firme todas las aplicaciones de línea de negocio nuevas y actualizadas con el nuevo certificado.</caps:sentence>
                    <caps:sentence sentenceid="135e5abbaa26e9cd47fdb5b9fbaf2c5e" id="tgt197" class="tgtSentence"> No es necesario retirar ni volver a implementar las aplicaciones existentes.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_FAQ">
        <title>
          <caps:sentence sentenceid="a8473d2d445d6121c874811a283e6f1e" id="tgt198" class="tgtSentence">Preguntas más frecuentes sobre la administración de dispositivos móviles de Microsoft Intune, incluida la administración con Configuration Manager 2012</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section expanded="false" address="BKMK_Symantec">
            <title>
              <caps:sentence sentenceid="0acc04a99923ff487f1e62cc62ac9283" id="tgt199" class="tgtSentence">¿Por qué Windows Phone requiere un certificado de Symantec para la administración?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="bca5bdf78a9a87711a6a2f3191e339a6" id="tgt200" class="tgtSentence">Windows Phone controla la instalación de aplicaciones.</caps:sentence>
                <caps:sentence sentenceid="aeca71661d91b31dd20f037d310b34d6" id="tgt201" class="tgtSentence"> Cualquier usuario que tenga una cuenta de Microsoft puede instalar aplicaciones desde la Tienda de Windows Phone, o bien las empresas pueden instalar o realizar la instalación de prueba de aplicaciones de línea de negocio (LOB) desarrolladas internamente mediante un proceso especial que se describe en la documentación de Windows Phone.</caps:sentence>
                <caps:sentence sentenceid="63c52d556e83a21fa24b077fe618d2ba" id="tgt202" class="tgtSentence"> Al instalar las aplicaciones LOB, los dispositivos Windows Phone solo confían en un tipo especial de certificado emitido por Symantec.</caps:sentence>
                <caps:sentence sentenceid="f967bb0d3d96cb9455c59003bf2f1a63" id="tgt203" class="tgtSentence"> No puede usar ningún otro certificado generado por vía comercial o privada.</caps:sentence>
                <caps:sentence sentenceid="09cd94f170cf68ec7afe6f8b3f228614" id="tgt204" class="tgtSentence"> Este requisito se aplica a todas soluciones de administración de dispositivos móviles, no solo a Intune.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="4486bedaf2aad8fbd8ce6308c36365dc" id="tgt205" class="tgtSentence">El certificado de Symantec crea un token de inscripción de aplicación (AET).</caps:sentence>
                <caps:sentence sentenceid="cd7946b0d209a2874b077a3e4b85958c" id="tgt206" class="tgtSentence"> El AET puede instalarse en un dispositivo cuando el dispositivo se inscribe para la administración de dispositivos móviles, o puede instalarse fuera de banda desde un sitio web seguro o desde un archivo adjunto de correo electrónico.</caps:sentence>
                <caps:sentence sentenceid="e23ee43b117aa2f05f7ce0678c65031b" id="tgt207" class="tgtSentence"> Los administradores deben firmar todas las aplicaciones de LOB con el certificado de Symantec mediante las herramientas proporcionadas en el <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268439</linkUri></externalLink>.</caps:sentence>
                <caps:sentence sentenceid="d9f30d299b5c3971eac4739d37396740" id="tgt208" class="tgtSentence"> Cuando los usuarios intentan instalar aplicaciones de LOB, el sistema operativo Windows Phone comprueba la firma en el AET para compararla con la firma de la aplicación.</caps:sentence>
                <caps:sentence sentenceid="8a269fe729dc7c14c459805ff817eef8" id="tgt209" class="tgtSentence"> Si las firmas coinciden, se puede continuar con la instalación.</caps:sentence>
                <caps:sentence sentenceid="e72acee76aeaa6415d939c088ceb8f84" id="tgt210" class="tgtSentence"> Si no se puede consultar el AET, se produce un error en la instalación.</caps:sentence>
                <caps:sentence sentenceid="a4d47b612e312de7101ea5ec01510e5b" id="tgt211" class="tgtSentence"> Existen varios motivos por los que quizás no se pueda consultar el AET:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fd645953ed631257d19883615b793f22" id="tgt212" class="tgtSentence">El AET nunca se instaló en el dispositivo</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="16368cf359f2911f56f6321b92beef47" id="tgt213" class="tgtSentence">El AET ha expirado</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="71a1e04f27919212d81bb91fbcc26f01" id="tgt214" class="tgtSentence">El AET no se creó con el mismo certificado de Symantec utilizado para firmar la aplicación</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="a6aef39c4d509b2213305476b24cd130" id="tgt215" class="tgtSentence">Windows Phone no requiere que el AET esté presente durante la inscripción de MDM, pero antes de la versión de noviembre de 2014, Intune necesitaba el AET y un ssp.xap firmado porque no existía ninguna otra manera de instalar el AET y ssp.xap excepto durante la inscripción.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="c5579fc500647b65bf98f37f19979c94" id="tgt216" class="tgtSentence">¿Cómo se crea el AET para usuarios de Intune?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="5ae84604a7e2d71341406f67047c6ca3" id="tgt217" class="tgtSentence">Cuando los administradores cargan el archivo .pfx para su certificado de Symantec, Intune crea automáticamente el AET y lo implementa en dispositivos Windows Phone inscritos.</caps:sentence>
                <caps:sentence sentenceid="3673950fa30fb4a5b214efc6c1ece8c8" id="tgt218" class="tgtSentence"> No es necesario que los administradores de Intune usen la herramienta AET Generator en el Windows Phone SDK.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="77fefb917a7ab6999763d45d4eab2972" id="tgt219" class="tgtSentence">Intune no admite la creación manual del AET ni su implementación fuera de banda.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="06f29a6979696756b4ca89ca6e4655c3" id="tgt220" class="tgtSentence">¿Qué cambios que se han producido para reducir la necesidad de un certificado de Symantec?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="16a954d50815f14c2eaae99c548348e0" id="tgt221" class="tgtSentence">En la versión de noviembre de 2014, Intune realizó cambios para permitir situaciones en las que las empresas no tengan un certificado de Symantec.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8e5785e0f2a407289b2b448597ee4ed2" id="tgt222" class="tgtSentence">El Portal de empresa para Windows Phone 8.1 está disponible para su instalación desde la tienda, por lo que no necesita la firma de un certificado de Symantec y ni es necesario validarlo con respecto a un AET.</caps:sentence>
                    <caps:sentence sentenceid="870b721c9c385fe3b369476a0ccb4c5e" id="tgt223" class="tgtSentence"> En su lugar, la aplicación se valida como parte del proceso de publicación de la tienda.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3fd9c84ead013cd036b409c5f6b4e687" id="tgt224" class="tgtSentence">Los dispositivos Windows Phone 8.1 se pueden inscribir con o sin un AET en el teléfono.</caps:sentence>
                    <caps:sentence sentenceid="17e8f2f82c4f4daa47f60466d31857ab" id="tgt225" class="tgtSentence"> Si hay un AET disponible, se instalará la primera vez que el dispositivo se sincronice con Intune.</caps:sentence>
                    <caps:sentence sentenceid="ab1784c5d6cb3c52abf66f14a2a0352a" id="tgt226" class="tgtSentence"> Si no hay ningún AET, el dispositivo puede seguir administrándose mediante Intune y los usuarios pueden instalar el Portal de empresa desde la tienda y usar la mayoría de las características del Portal de empresa sin un certificado de Symantec para firmar aplicaciones.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="f9bff7cb4f98158765d890ba47c27592" id="tgt227" class="tgtSentence">No hay ningún cambio en el requisito de Symantec para dispositivos Windows Phone 8.</caps:sentence>
                <caps:sentence sentenceid="968858e5bbf674e1176a63319dd99275" id="tgt228" class="tgtSentence"> Los dispositivos Windows Phone 8 deben tener el ssp.xap firmado y el AET presentes durante la inscripción; de lo contrario, se bloqueará de inscripción.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="27f38a368b320d3bbda10e828f5db6a2" id="tgt229" class="tgtSentence">¿Qué funcionalidad se admite si se inscribe un dispositivo Windows Phone 8.1 pero no hay ningún certificado de Symantec?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="d37d81db57a8768a88d00a5b32137827" id="tgt230" class="tgtSentence">Si se inscribe un dispositivo Windows Phone 8.1 pero no hay ningún certificado de Symantec, puede:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a6eff3471ecee6ba66f3a757e9dc7857" id="tgt231" class="tgtSentence">Crear directivas e insertarlas en el dispositivo</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="617b7bebf9b5e89394b404b407e3d5e9" id="tgt232" class="tgtSentence">Configurar la información de contacto del departamento de TI que se muestra en el Portal de empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="878fb2365222c016787648a0d3ef3001" id="tgt233" class="tgtSentence">Crear vínculos profundos a la tienda e implementarlos en el Portal de empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ed637eb5906e5ebdc91f81d3053198a7" id="tgt234" class="tgtSentence">Crear vínculos a páginas web e implementarlos en el Portal de empresa</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e95d654aba16b07959b72d850e5f12b7" id="tgt235" class="tgtSentence">Crear los términos y condiciones que deben aceptar los usuarios para poder usar el Portal de empresa</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="80ada9528124e15df4dd26935aa605ae" id="tgt236" class="tgtSentence">Lo único que no puede hacer sin un certificado de Symantec es implementar aplicaciones de LOB.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="a81bff7622c8e73171ad3e2b93dc1ca4" id="tgt237" class="tgtSentence">Intune Software Publisher no comprueba que las aplicaciones estén firmadas al cargarlas.</caps:sentence>
                  <caps:sentence sentenceid="46660005128f53bc64e6c7bceceb2bcd" id="tgt238" class="tgtSentence"> Si implementa aplicaciones sin firmar, se producirá un error cuando los usuarios intenten instalarlas.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="d959623c7541516bd9a781d53b0c4d3e" id="tgt239" class="tgtSentence">¿Qué pueden hacer los usuarios si tienen el Portal de empresa pero no hay ningún certificado de Symantec?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="552f4dae42c6b84b79e6bebb5d79ec29" id="tgt240" class="tgtSentence">No es necesario que los dispositivos Windows Phone 8.1 estén inscritos para que los usuarios puedan instalar el Portal de empresa desde la tienda.</caps:sentence>
                <caps:sentence sentenceid="275b38084299a98feb7e0a323b5dd812" id="tgt241" class="tgtSentence"> Si el dispositivo no está inscrito, se solicitará a los usuarios que lo inscriban.</caps:sentence>
                <caps:sentence sentenceid="a65d8c8ad714514177dfcd664bc69b9c" id="tgt242" class="tgtSentence"> Al tocar el mensaje del Portal de empresa, los usuarios acceden directamente a <ui>Configuración / Área de trabajo</ui>, donde pueden inscribir el dispositivo.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a47ea5cf9d9625766c7477800cd6d202" id="tgt243" class="tgtSentence">Incluso sin inscribir el dispositivo, los usuarios pueden realizar las siguientes acciones con el Portal de empresa instalado desde la tienda:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="86a130c9193962978650feab26546162" id="tgt244" class="tgtSentence">Aceptar o rechazar los términos y condiciones configurados por el administrador.</caps:sentence>
                    <caps:sentence sentenceid="aedd567dbc376df8e6e4b11fb43e7996" id="tgt245" class="tgtSentence"> Si los usuarios rechazan los términos y condiciones, se cierra el Portal de empresa.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5b8adf835d42ecf17a11dcab8a95fa7d" id="tgt246" class="tgtSentence">Ver la información de contacto del departamento de TI</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="425b6b3da98781c5b55f481080080d5d" id="tgt247" class="tgtSentence">Ver los dispositivos inscritos, entre ellos, los dispositivos iOS, Android y Windows</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="bf4492432aa4d31374f36fe6cb0db216" id="tgt248" class="tgtSentence">Usar vínculos profundos a aplicaciones en la tienda</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5245e8a94087a5a2082528f421784aae" id="tgt249" class="tgtSentence">Usar vínculos web para abrir páginas web</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="681cef1de549baba59faf4f773c29f5e" id="tgt250" class="tgtSentence">Con el dispositivo inscrito, los usuarios pueden ver el dispositivo en la lista <ui>Mis dispositivos</ui>.</caps:sentence>
                <caps:sentence sentenceid="453ba15b346c9557a686cb0db7a346e4" id="tgt251" class="tgtSentence"> Una vez inscrito, el dispositivo está sujeto a las directivas de Intune implementadas.</caps:sentence>
                <caps:sentence sentenceid="2b3bf3125ff7527a76fc76a2a4982d6f" id="tgt252" class="tgtSentence"> Los dispositivos deben inscribirse para obtener el AET e instalar aplicaciones de LOB.</caps:sentence>
                <caps:sentence sentenceid="274077dccf96d6b4d7e6e2ff6be0b8a9" id="tgt253" class="tgtSentence"> A los dispositivos no inscritos que intenten instalar una aplicación de LOB se les solicitará que se inscriban.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="44fc05b4e45d60fc7658f2f7bb9f722e" id="tgt254" class="tgtSentence">Lo único que los usuarios no pueden hacer si la empresa no tiene un certificado de Symantec es instalar aplicaciones de LOB implementadas por el administrador.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="8908a0afb06ed65c1edef45b122baa65" id="tgt255" class="tgtSentence">Nuestra empresa ya tiene un certificado y ha inscrito dispositivos Windows Phone 8.1.</caps:sentence>
              <caps:sentence sentenceid="cdd7ef49ee7488b490b74a567305aa8f" id="tgt256" class="tgtSentence"> ¿Es necesario hacer algo diferente ahora que el Portal de empresa está disponible en la tienda?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="cdb72a02b423f4db13f9914d497fedf6" id="tgt257" class="tgtSentence">El ssp.xap actual desde el centro de descarga sigue funcionando en dispositivos Windows Phone 8.1.</caps:sentence>
                <caps:sentence sentenceid="635f418afd05eff3c5a8c22f835f6426" id="tgt258" class="tgtSentence"> Puede seguir indicando a los usuarios que se inscriban y obtengan el portal de empresa durante la instalación.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="5c9f54b558a579c725d95fa79d038f6c" id="tgt259" class="tgtSentence">¿Cuáles son las ventajas y desventajas de que los usuarios obtengan el Portal de empresa desde la tienda?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="b028aaa3d7589d6f1a8f4dcc51bc5886" id="tgt260" class="tgtSentence">Ventajas:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="44b59bd5003a52759f5badd8abe57c0c" id="tgt261" class="tgtSentence">Los usuarios obtienen vínculos profundos y vínculos web, incluso si el dispositivo Windows Phone 8.1 no está inscrito</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="930a4f8505ad69bd7f0d04a1e85b6a8f" id="tgt262" class="tgtSentence">Cuando Microsoft actualiza el Portal de empresa, la aplicación de la tienda se actualiza automáticamente sin necesidad de que descargue, firme o vuelva a implementar el ssp.xap</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f59020828d42d1f89021c34991e5fb27" id="tgt263" class="tgtSentence">La documentación para los usuarios de Windows Phone 8.1, iOS, Android y Windows es coherente: “Ir a la tienda e instalar el Portal de empresa”.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a8b1fc65f186cd804791e0063b4822e6" id="tgt264" class="tgtSentence">Los usuarios ven la aplicación tal y como se instala y reciben instrucciones de inscripción al abrirse</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="c5e9cbdfd23494eade05650d2e315736" id="tgt265" class="tgtSentence">Desventajas:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="67b0cdf5eb7cc1353e29dc9091eeda50" id="tgt266" class="tgtSentence">Los usuarios ven una casilla para instalar un "<ui>hub de empresa</ui>", pero no hay nada que les dirija al Portal de empresa en la lista de aplicaciones del dispositivo</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="527369e8b7bcd296bf39deeb7102bccf" id="tgt267" class="tgtSentence">No se solicita a los usuarios que acepten términos y condiciones personalizados hasta que abran el Portal de empresa</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="e0670c64da4d7a389e3edc4f98074a3d" id="tgt268" class="tgtSentence">En las siguientes circunstancias, puede seguir indicando a los usuarios que se inscriban e instalen el ssp.xap durante la inscripción:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2e775f1961bb6cf07c5a85ae329a4f14" id="tgt269" class="tgtSentence">Si la empresa bloquea el acceso a la tienda desde los dispositivos Windows Phone, los usuarios deben instalar el ssp.xap durante la inscripción.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c549b0bfebbc3da38fcb01ac665be91c" id="tgt270" class="tgtSentence">Si los usuarios no tienen cuentas de Microsoft configuradas en sus dispositivos Windows Phone, no podrán instalar el Portal de empresa desde la tienda.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="21b30a7e587b3dbe09fdec247f457275" id="tgt271" class="tgtSentence">Si la documentación existente para la inscripción de Windows Phone les indica que vayan primero a Configuración, Área de trabajo, es posible que se tarde un tiempo en actualizar los documentos y dirigir a los usuarios a la tienda.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="fe8f3c69642c11e2b9ea6d84f0371765" id="tgt272" class="tgtSentence">¿Cuál es la diferencia entre el ssp.xap del centro de descarga y la aplicación de la tienda?</caps:sentence>
            </title>
            <content>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9158d571d0ffe116fdd82a094e7beab5" id="tgt273" class="tgtSentence">El Portal de empresa de la tienda no exige la firma de un certificado de Symantec para su instalación</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ff8c41c93a55cc70906a725b57770f47" id="tgt274" class="tgtSentence">El Portal de empresa de la tienda presenta los términos y condiciones para el usuario pero no así el ssp.xap del centro de descarga</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="47295996a58c02577f305efe2c34562e" id="tgt275" class="tgtSentence">El Portal de empresa de la tienda es un archivo .appx en lugar de .xap</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="b2e4b482c2464ea642f30472708b0fd4" id="tgt276" class="tgtSentence">¿Puedo obtener el archivo de Portal de empresa e insertarlo en los dispositivos de mis usuarios en lugar de enviarlos a la tienda?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4f7b50bec76bcf2b862eeb2140701427" id="tgt277" class="tgtSentence">Sí.</caps:sentence>
                <caps:sentence sentenceid="863d73f5079173aed48a39a775f609f7" id="tgt278" class="tgtSentence"> La aplicación Portal de empresa se puede descargar para los siguientes sistemas operativos desde el centro de descarga:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="80ca961f21952f878b8688c0b28b72d1" id="tgt279" class="tgtSentence">Windows Phone 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615799</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="132a42035119c4b6819173ebaefee335" id="tgt280" class="tgtSentence">Windows Phone 8.0 : <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=268440</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4e458d4908dd91d3612a8e39fd1b9903" id="tgt281" class="tgtSentence">Windows 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615800</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615800</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="07a844f479ec1aa2a83c1de9c238a276" id="tgt282" class="tgtSentence">¿Las empresas pueden seguir usando la herramienta de soporte para la administración de versión de prueba de Windows Intune de Windows Phone si no tienen un certificado de Symantec y seguir indicando a los usuarios que instalen el Portal de empresa desde la tienda?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4f7b50bec76bcf2b862eeb2140701427" id="tgt283" class="tgtSentence">Sí.</caps:sentence>
                <caps:sentence sentenceid="8c24975691fabd85fb3ead253d3c9451" id="tgt284" class="tgtSentence"> Si necesita realizar una prueba de concepto que incluya la instalación de aplicaciones de LOB, la herramienta de administración de pruebas funciona con la versión de la tienda del portal de empresa.</caps:sentence>
                <caps:sentence sentenceid="6b9cdd25078fdd8f3f3544de94cb24e6" id="tgt285" class="tgtSentence"> Sin embargo, puesto que el AET del certificado de Symantec ya no es necesario para inscribir dispositivos Windows Phone 8.1, las empresas pueden probar la instalación de aplicaciones mediante vínculos profundos a aplicaciones de la tienda.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e0b94b3beb8578f9a74f62aa274e8de8" id="tgt286" class="tgtSentence">La herramienta de soporte para la administración de versión de prueba de Windows Intune de Windows Phone es solo para suscripciones de prueba de Intune.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="b423f1f2cd0cd14a02d5a88c115ce89e" id="tgt287" class="tgtSentence">Use solo las pruebas de la herramienta de administración de pruebas.</caps:sentence>
                  <caps:sentence sentenceid="a10570b481f6494ad67cbda562791b19" id="tgt288" class="tgtSentence"> Los dispositivos inscritos con el AET desde la herramienta de administración de pruebas deben anular la inscripción y volver a inscribirse si el certificado de Symantec para la herramienta de administración de pruebas ya no está disponible, o bien si la empresa obtiene su propio certificado de Symantec para firmar aplicaciones.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="9b2d8eef1c442aab1669ce98878685c9" id="tgt289" class="tgtSentence">¿Las empresas pueden comenzar sin ningún certificado de Symantec y, a continuación, agregar uno más tarde, incluso después de que se hayan inscrito dispositivos Windows Phone 8.1?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4f7b50bec76bcf2b862eeb2140701427" id="tgt290" class="tgtSentence">Sí.</caps:sentence>
                <caps:sentence sentenceid="c542071594b3362f2e3a769ea372178b" id="tgt291" class="tgtSentence"> Incluso si ya se han inscrito dispositivos Windows Phone 8.1, puede obtener un certificado de Symantec, firmar el ssp.xap y cargar este archivo y el archivo pfx.</caps:sentence>
                <caps:sentence sentenceid="8e37b1ff45265fcef519fe877434c54e" id="tgt292" class="tgtSentence"> A continuación, Intune generará el AET.</caps:sentence>
                <caps:sentence sentenceid="0366852c1413d4a083ea32d99992e9dc" id="tgt293" class="tgtSentence"> Los dispositivos Windows Phone 8.1 obtendrán el AET la próxima vez que se sincronicen, hasta un máximo de ocho horas.</caps:sentence>
                <caps:sentence sentenceid="fee18265465e2efd8f40eba170049879" id="tgt294" class="tgtSentence"> Deje que pasen al menos ocho horas antes de implementar las aplicaciones de línea de negocio después de cargar los archivos xap y pfx.</caps:sentence>
              </para>
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
          <caps:sentence id="src1" class="srcSentence">Before you can manage Windows Phone mobile devices with <token>wit_nextref</token>, you have to set up management requirements.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Creating a DNS CNAME helps users connect to the <token>wit_nextref</token> company portal.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Windows Phone 8.0 requires a Symantec certificate to establish an encrypted IP connection between devices and <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Depending upon how users access the company portal, Windows Phone 8.1 might also.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> A certificate is also required to sign line-of-business apps.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">
                <embeddedLabel>Windows Phone 8.1</embeddedLabel> - Requires a certificate only if:</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Users won't download the company portal from the Store</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence id="src8" class="srcSentence">You'll deploy  line-of-business (AKA "sideloaded") apps</caps:sentence>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">
                <embeddedLabel>Windows Phone 8</embeddedLabel> - Required </caps:sentence>
            </para>
          </listItem>
        </list>
        <mediaLink>
          <image xlink:href="b457bc08-2634-4137-86f6-5f7cc330fbd2"></image>
        </mediaLink>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Prepare to manage Windows Phone mobile devices with Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">Setup requirements for Window Phone mobile device management depend upon how you'll manage devices.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence">  Setting two CNAMEs in your company's DNS registration makes enrollment easier for uses.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> If your users will download the Company Portal app from the Store, then once you've configured DNS settings you just need to set up the Company Portal and inform users how to enroll.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence">  For Windows Phone 8.0, or Windows Phone 8.1 where you'll deploy the Company Portal, you'll need a Symntec certificate to code-sign the app.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src15" class="srcSentence">Set up Windows Phone enrollment with Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">
                      <embeddedLabel>Set up <token>wit_nextref</token></embeddedLabel> <br />If you haven’t already, prepare for mobile device management by  <externalLink><linkText>setting the mobile device management authority</linkText><linkUri>https://technet.microsoft.com/library/mt346013.aspx</linkUri></externalLink> as <embeddedLabel>Microsoft Intune</embeddedLabel>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">
                      <embeddedLabel>Set a DNS alias for the enrollment server address</embeddedLabel> (optional)<br /> </caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">A DNS alias (CNAME record type) makes it easier users to enroll their devices by automatically populating the server name during enrollment.</caps:sentence>
                  </para>
                  <procedure>
                    <title>
                      <caps:sentence id="src19" class="srcSentence">Verify and create DNS CNAME</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src20" class="srcSentence">In the <externalLink target="_blank"><linkText>Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, click <ui>Administration</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src21" class="srcSentence">Type the URL of the verified domain of the company website in the <ui>Specify a verified domain name</ui> box and then click <ui>Test Auto-Detection</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src22" class="srcSentence">Create CNAME resource records for your company’s domain.</caps:sentence>
                            <caps:sentence id="src23" class="srcSentence"> The CNAME resource records must contain the following information:</caps:sentence>
                          </para>
                          <table border="1">
                            <thead>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src24" class="srcSentence">TYPE</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src25" class="srcSentence">Host Hame</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src26" class="srcSentence">Points to</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src27" class="srcSentence">TTL</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </thead>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src28" class="srcSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence id="src29" class="srcSentence">  <para>enterpriseenrollment.company_domain.com </para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src30" class="srcSentence">manage.microsoft.com
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src31" class="srcSentence">1 Hour</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src32" class="srcSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence id="src33" class="srcSentence"> <para>enterpriseregistration.company_domain.com </para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src34" class="srcSentence">enterpriseregistration.windows.net
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src35" class="srcSentence">1 Hour</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                          <para>
                            <caps:sentence id="src36" class="srcSentence">For example, if your company’s website is contoso.com, you would create a CNAME in DNS that redirects EnterpriseEnrollment.contoso.com to manage.microsoft.com.</caps:sentence>
                            <caps:sentence id="src37" class="srcSentence"> If there is more than one verified domain, create a CNAME record for each domain.</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src38" class="srcSentence">
                                  <codeInline>manage.microsoft.com</codeInline> – Supports a redirect to the Intune service with domain recognition from the email’s domain name</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src39" class="srcSentence">
                                  <codeInline>enterpriseregistration.windows.net</codeInline> – Supports workplace join for mobile devices.</caps:sentence>
                                <caps:sentence id="src40" class="srcSentence"> It also supports conditional access for Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                  <mediaLink>
                    <image xlink:href="33622fc8-d7ad-4f20-a4ec-c50de6a158bc"></image>
                  </mediaLink>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">
                      <embeddedLabel>Certificate management to support app signing</embeddedLabel>
                      <br />[Required for Windows Phone 8.0 and Windows Phone 8.1 that won’t access the Windows Phone Store and/or need line-of-business apps.]</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">To support the Company Portal app for Windows Phone 8.0 and to deploy company apps to Windows Phone 8.1 you must get a <embeddedLabel>Symantec Enterprise Mobile Code Signing Certificate</embeddedLabel>.</caps:sentence>
                    <caps:sentence id="src43" class="srcSentence"> You cannot use a certificate issued by your own certification authority because only the Symantec certificate is trusted by Windows Phone devices.</caps:sentence>
                    <caps:sentence id="src44" class="srcSentence"> This certificate is required in order to:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">Sign the Company Portal app for deployment to <token>winphone8_client_1</token> for enrollment and phone management</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Sign company line-of-business apps so <token>wit_nextref</token> can deploy them to Windows Phones</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">For more information, see <externalLink><linkText>Frequently Asked Questions about Windows Phone Mobile Device Management</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_FAQ</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">The steps below will help you get the required certificates and sign the company portal app.</caps:sentence>
                    <caps:sentence id="src49" class="srcSentence"> You will need a Windows Phone Dev Center account and then you will need to purchase a Symantec certificate.</caps:sentence>
                  </para>
                  <procedure expanded="false" address="BKMK_CodeSign">
                    <title>
                      <caps:sentence id="src50" class="srcSentence">To get a certificate and code-sign the Company Portal</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src51" class="srcSentence">
                              <embeddedLabel>Join the Windows Phone Dev Center</embeddedLabel> <br />Join the <externalLink target="_blank"><linkText>Windows Phone Dev Center</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268442</linkUri></externalLink> using corporate account information when logging in to purchase your company account.</caps:sentence>
                            <caps:sentence id="src52" class="srcSentence"> This request will need to be authorized by a company officer before you receive a code-signing certificate.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src53" class="srcSentence">
                              <embeddedLabel>Get a company Symantec certificate</embeddedLabel> <br />Purchase a certificate from the <externalLink target="_blank"><linkText>Symantec website</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268441</linkUri></externalLink> using your Symantec ID.</caps:sentence>
                            <caps:sentence id="src54" class="srcSentence"> After you purchase the certificate, the corporate approver whom you designated in your Windows Phone Dev Center account will receive an email asking for approval of the certificate request.</caps:sentence>
                            <caps:sentence id="src55" class="srcSentence"> For more information about the Symantec certificate requirement, see the <externalLink><linkText>Why Windows Phone requires a Symantec certificate?</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_Symantec</linkUri></externalLink> Windows device enrollment FAQ.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src56" class="srcSentence">
                              <embeddedLabel>Import certificates</embeddedLabel> <br />Once the request has been approved, you will receive an email containing instructions for importing certificates.</caps:sentence>
                            <caps:sentence id="src57" class="srcSentence"> Follow the instructions in the email to import the certificates.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src58" class="srcSentence">
                              <embeddedLabel>Verify certificates imported</embeddedLabel> <br />To verify that the certificates have been imported correctly, go to the <ui>Certificates</ui> snap-in, right-click <ui>Certificates</ui>, and select <ui>Find Certificates</ui>.</caps:sentence>
                            <caps:sentence id="src59" class="srcSentence"> In the <ui>Contains</ui> field, enter “Symantec”, and click <ui>Find Now</ui>.</caps:sentence>
                            <caps:sentence id="src60" class="srcSentence"> The certificates you imported should appear in the results.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="52f7f33c-987f-48ad-b661-d826489044cd"></image>
                            </mediaLinkInline>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src61" class="srcSentence">
                              <embeddedLabel>Export a signing certificate</embeddedLabel> <br />Having verified that the certificates are present, you can export the .pfx file to sign the company portal.</caps:sentence>
                            <caps:sentence id="src62" class="srcSentence"> Select the Symantec certificate with <ui>Intended purpose</ui> “code-signing.”</caps:sentence>
                            <caps:sentence id="src63" class="srcSentence"> Right-click the code-signing certificate and select <ui>Export</ui>.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="a5e198a5-7d2b-4797-bdfa-853a8e664b3c"></image>
                            </mediaLinkInline>
                          </para>
                          <para>
                            <caps:sentence id="src64" class="srcSentence">In the <ui>Certificate Export Wizard</ui>, select <ui>Yes, export the private key</ui> and then click <ui>Next</ui>.</caps:sentence>
                            <caps:sentence id="src65" class="srcSentence">
                              <ui>Select Personal Information Exchange –PKCS #12 (.PFX)</ui> and check <ui>Include all the certificates in the certification path if possible</ui>.</caps:sentence>
                            <caps:sentence id="src66" class="srcSentence"> Complete the wizard.</caps:sentence>
                            <caps:sentence id="src67" class="srcSentence"> For more information, see <externalLink><linkText>How to Export a Certificate with the Private Key</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=203031</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <embeddedLabel>
                              <caps:sentence id="src68" class="srcSentence">Download and sign the Company Portal app</caps:sentence>
                            </embeddedLabel>
                            <br />
                          </para>
                          <para>
                            <caps:sentence id="src69" class="srcSentence">Support for Windows Phone enrollment requires the Windows Phone 8.0 Company Portal app be signed and uploaded to Intune.</caps:sentence>
                          </para>
                          <procedure expanded="true">
                            <title>
                              <caps:sentence id="src70" class="srcSentence">Windows Phone 8.0: Download and sign the Company Portal app </caps:sentence>
                            </title>
                            <steps class="ordered">
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence id="src71" class="srcSentence">
                                      <embeddedLabel>Download the Company Portal</embeddedLabel> <br />Download the <externalLink target="_blank"><linkText>Intune Company Portal for Windows Phone</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink> from the Download Center.</caps:sentence>
                                    <caps:sentence id="src72" class="srcSentence"> The default installation location is <codeInline>C:\Program Files (x86)\Microsoft Corporation\Windows Intune Company Portal for Windows Phone</codeInline>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence id="src73" class="srcSentence">
                                      <embeddedLabel>Download the Windows Phone 8.0 SDK</embeddedLabel>
                                      <br />Download the <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence id="src74" class="srcSentence">
                                      <embeddedLabel>Code-sign the Company Portal app</embeddedLabel> <br />Use the XAPSignTool app downloaded with the SDK to sign the company portal with the .pfx file you created from the Symantec certificate.</caps:sentence>
                                    <caps:sentence id="src75" class="srcSentence"> For more information, see <externalLink target="_blank"><linkText>How to sign a company app by using XapSignTool</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=280195</linkUri></externalLink>.</caps:sentence>
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
                            <caps:sentence id="src76" class="srcSentence">
                              <embeddedLabel>Upload the Company Portal app to <token>wit_nextref</token></embeddedLabel> <br />Upload the signed Company Portal app file and your code-signing certificate to make the app available to your end users.</caps:sentence>
                          </para>
                          <list class="ordered">
                            <listItem>
                              <para>
                                <caps:sentence id="src77" class="srcSentence">In the <externalLink target="_blank"><linkText>Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Administration</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src78" class="srcSentence">Click the <ui>Upload Signed App File</ui> and sign in with your <token>wit_nextref</token> Administrator ID.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src79" class="srcSentence">On the <ui>Software setup</ui> page for <ui>Specify the location of the software setup files</ui>, browse to the code-signed Company Portal app location (.xap for Windows Phone 8.0 or .appx for Windows Phone 8.1).</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src80" class="srcSentence">If you are evaluating <token>wit_nextref</token> and uploading a code-signed app file in a trial <token>wit_nextref</token> account, uncheck the <ui>Use the Company Portal App file signed by the sample Symantec code-signed certificate</ui> checkbox.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src81" class="srcSentence">Add the certificate (.pfx) file that you exported to <ui>Code-signing certificate</ui> and create a password for the certificate.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src82" class="srcSentence">On the <ui>Software description</ui> page, complete the fields remembering that users see this information on their devices when viewing details about the app in the Company Portal.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src83" class="srcSentence">Complete the wizard.</caps:sentence>
                                <caps:sentence id="src84" class="srcSentence"> Users who enroll a Windows Phone 8.0 device will now get the Company Portal app on their devices during enrollment.</caps:sentence>
                                <caps:sentence id="src85" class="srcSentence"> Windows Phone 8.1 users can install the Company Portal app from the store version of the Company Portal.</caps:sentence>
                                <caps:sentence id="src86" class="srcSentence">  If Windows Phone 8.1 devices are blocked from the Windows Phone Store or you want to deploy the Company Portal app using Intune, you must download and sign the Windows Phone 8.1 Company Portal (SSP.appx) app.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">
                      <embeddedLabel>Add Intune users</embeddedLabel> <br />The mobile device owner must be added to the Microsoft Intune Account Portal before devices can be enrolled.</caps:sentence>
                    <caps:sentence id="src88" class="srcSentence"> Log in to the <externalLink><linkText>Microsoft Intune Account Portal</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=698854</linkUri></externalLink>, click <ui>Add users</ui>, and select an option:</caps:sentence>
                  </para>
                  <para></para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">
                          <embeddedLabel>User</embeddedLabel>: To add a single user select <ui>New</ui> &gt; <ui>User</ui> and enter <ui>Details</ui>, <ui>Assign roles</ui>, <ui>Set user location</ui>, and then assign the user to a <ui>Group</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">
                          <embeddedLabel>Bulk add</embeddedLabel>: Create a .csv file (see samples files provided) and import it into the Intune Account Portal.</caps:sentence>
                        <caps:sentence id="src91" class="srcSentence"> Specify roles, location, and group, and then create the accounts.</caps:sentence>
                        <caps:sentence id="src92" class="srcSentence"> Sample and blank .csv files can be downloaded from the Microsoft Intune Account Portal.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">You can also enable Active Directory or Azure Active Directory synchronization.</caps:sentence>
                    <caps:sentence id="src94" class="srcSentence"> For more information about integrating other Azure Active Directory users with Intune, see <externalLink><linkText>Directory synchronization roadmap</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=511540</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">
                      <embeddedLabel>Create groups </embeddedLabel> (Optional)<br />Groups give flexibility for managing devices and users.</caps:sentence>
                    <caps:sentence id="src96" class="srcSentence"> You can set up groups to suit your organizational needs by geographic location, department, or hardware characteristics, for example.</caps:sentence>
                    <caps:sentence id="src97" class="srcSentence">   See <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <caps:sentence id="src98" class="srcSentence">
                    <para>
                      <embeddedLabel>Add policies for devices</embeddedLabel> (Optional)<br />Policies are groups of settings that control features on devices. Most MDM policies are platform specific. You create policies using templates  containing recommended or customized settings, and then deploy them to groups. See <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</para> </caps:sentence>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">
                      <embeddedLabel>Set device enrollment limit</embeddedLabel> (Optional) <br />To limit the number of mobile devices a user can enroll, log in to the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Enrollment rules</ui>.</caps:sentence>
                    <caps:sentence id="src100" class="srcSentence"> Select the maximum number of devices a user can enroll and then click <ui>Save</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">
                      <embeddedLabel>Set Company Portal settings </embeddedLabel>
                      <br /> You can customize the Intune Company Portal for your company.</caps:sentence>
                    <caps:sentence id="src102" class="srcSentence"> In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Admin</ui> &gt; <ui>Company Portal</ui>.</caps:sentence>
                    <caps:sentence id="src103" class="srcSentence"> Configure the following</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src104" class="srcSentence">Company Name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src105" class="srcSentence">IT department contact name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src106" class="srcSentence">IT department phone number</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src107" class="srcSentence">Additional information</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src108" class="srcSentence">Company privacy statement URL</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src109" class="srcSentence">Support website URL (not displayed)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src110" class="srcSentence">Website name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step address="BKMK_Terms">
                <content>
                  <tokenBlock>CPEnrollmentTermsAndConditions</tokenBlock>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">
                      <embeddedLabel>Tell users how to get access to company resources with the company portal</embeddedLabel> <br />Your users will need to know how to enroll their devices and what to expect once they're brought into management.</caps:sentence>
                    <caps:sentence id="src112" class="srcSentence">
                      <link xlink:href="48914533-f138-4dc0-8b93-4cea3ac61f7b">What to tell your end users about using Intune</link>
                    </caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src113" class="srcSentence">Deploy the Windows Phone 8.1 Company Portal app</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src114" class="srcSentence">You can deploy the Company Portal app to Windows Phone 8.1 devices with <token>wit_nextref</token> instead of installing from the Windows Phone Store.</caps:sentence>
                <caps:sentence id="src115" class="srcSentence"> You must still enable Windows Phone device enrollment with the steps above using the Symantec certificate.</caps:sentence>
                <caps:sentence id="src116" class="srcSentence"> You must then download the Windows Phone 8.1 Company Portal app and sign it with your Symantec certificate.</caps:sentence>
                <caps:sentence id="src117" class="srcSentence">  This is only necessary if your users won't use the Company Store and you want to deploy the Company Portal to Windows Phone 8.1 devices.</caps:sentence>
              </para>
              <procedure expanded="false" address="BKMK_WP81appx">
                <title>
                  <caps:sentence id="src118" class="srcSentence">Steps to download and sign the Windows Phone 8.1 Company Portal app for deployment with Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">
                          <embeddedLabel>Download the Company Portal</embeddedLabel> <br /></caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">Download the <externalLink target="_blank"><linkText>Microsoft Intune Company Portal App for Windows Phone 8.1</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink> from the Download Center and run the self-extracting (.exe) file.</caps:sentence>
                        <caps:sentence id="src121" class="srcSentence"> This file contains two files:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src122" class="srcSentence">CompanyPortal.appx– The Company Portal installation app for Windows Phone 8.1</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src123" class="srcSentence">WinPhoneCompanyPortal.ps1 – A PowerShell script you can use to sign the Company Portal app file so it can be deployed to Windows Phone 8.1 devices</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src124" class="srcSentence">
                          <embeddedLabel>Download the Windows Phone SDK</embeddedLabel>
                          <br />Download the <externalLink target="_blank"><linkText>Windows Phone SDK 8.0</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink> (http://go.microsoft.com/fwlink/?LinkId=268439) and install the SDK to your computer.</caps:sentence>
                        <caps:sentence id="src125" class="srcSentence"> This SDK is needed to generate an application enrollment token.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src126" class="srcSentence">
                          <embeddedLabel>Generate an AETX file</embeddedLabel>
                          <br />Generate an application enrollment token (.aetx) file from the Symantec PFX file using AETGenerator.exe, part of Windows Phone SDK 8.0.</caps:sentence>
                        <caps:sentence id="src127" class="srcSentence"> For instructions on how to create an AETX file, see <externalLink><linkText>How to generate an application enrollment token for Windows Phone</linkText><linkUri>https://msdn.microsoft.com/library/windows/apps/jj735576.aspx</linkUri></externalLink></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src128" class="srcSentence">
                          <embeddedLabel>Download the Windows SDK for Windows 8.1</embeddedLabel>
                          <br />Download and install the <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=613525</linkUri></externalLink> (http://go.microsoft.com/fwlink/?LinkId=613525).</caps:sentence>
                        <caps:sentence id="src129" class="srcSentence"> Note that the PowerShell script included with the Company Portal app uses the default install location, <codeInline>${env:ProgramFiles(x86)}\Windows Kits\8.1</codeInline>.</caps:sentence>
                        <caps:sentence id="src130" class="srcSentence"> If you install elsewhere, you must include the location in a cmdlet parameter.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src131" class="srcSentence">
                          <embeddedLabel>Code-sign the app using PowerShell</embeddedLabel>
                          <br />As an administrator, open <ui>Windows PowerShell</ui> on the host computer installed with the Windows SDK, the Symantec Enterprise Mobile Code Signing Certificate, navigate to the Sign-WinPhoneCompanyPortal.ps1 file and run the script.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src132" class="srcSentence">Example 1</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -AetxPath 'C:\signing\cert.aetx'</code>
                      <para>
                        <caps:sentence id="src133" class="srcSentence">This example signs the CompanyPortal.appx at C:\temp\ and produces the CompanyPortalEnterpriseSigned.appx.</caps:sentence>
                        <caps:sentence id="src134" class="srcSentence"> It would use PFX password 1234 and read the publisher ID from the PFX file.</caps:sentence>
                        <caps:sentence id="src135" class="srcSentence"> It reads the enterprise ID from the cert.aetx file as well.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src136" class="srcSentence">Example 2</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -PublisherId 'OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1' -EnterpriseId 1000000001</code>
                      <para>
                        <caps:sentence id="src137" class="srcSentence">This example signs the CompanyPortal.appx at C:\temp\ and produces the CompanyPortalEnterpriseSigned.appx.</caps:sentence>
                        <caps:sentence id="src138" class="srcSentence"> It would use PFX password 1234 and use the publisher ID specified.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src139" class="srcSentence">Parameters:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src140" class="srcSentence">
                              <codeInline>-InputAppx</codeInline> – The local path to the CompanyPortal.appx file in single quotes.</caps:sentence>
                            <caps:sentence id="src141" class="srcSentence"> For example 'C:\temp\CompanyPortal.appx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src142" class="srcSentence">
                              <codeInline>-OutputAppx</codeInline> – The local path and file name for the signed Company Portal app in single quotes.</caps:sentence>
                            <caps:sentence id="src143" class="srcSentence"> For example, 'C:\temp\CompanyPortalEnterpriseSigned.appx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src144" class="srcSentence">
                              <codeInline>-PfxFilePath</codeInline> – The local path and file name for the exported PFX file of the Symantec certificate.</caps:sentence>
                            <caps:sentence id="src145" class="srcSentence"> For example, 'C:\signing\cert.pfx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src146" class="srcSentence">
                              <codeInline>-PfxPassword</codeInline> – The password used to sign the PFX file in single quotes.</caps:sentence>
                            <caps:sentence id="src147" class="srcSentence"> For example '1234'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src148" class="srcSentence">
                              <codeInline>-AetxPath</codeInline> – The local path to the .aetx file which is used for reading the enterprise ID if the 'EnterpriseId' argument is not defined.</caps:sentence>
                            <caps:sentence id="src149" class="srcSentence"> Either this argument or EnterpriseId must be provided.</caps:sentence>
                            <caps:sentence id="src150" class="srcSentence"> For example 'C:\signing\cert.aetx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src151" class="srcSentence">
                              <codeInline>-PublisherId</codeInline> - The Publisher ID of the enterprise.</caps:sentence>
                            <caps:sentence id="src152" class="srcSentence"> If absent, the 'Subject' field of the Symantec Enterprise Mobile Code Signing Certificate is used.</caps:sentence>
                            <caps:sentence id="src153" class="srcSentence"> For example, 'OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src154" class="srcSentence">
                              <codeInline>-SdkPath</codeInline> - The path to the root folder of the Windows SDK for Windows 8.1.</caps:sentence>
                            <caps:sentence id="src155" class="srcSentence"> This argument is optional and defaults to ${env:ProgramFiles(x86)}\Windows Kits\8.1.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src156" class="srcSentence">
                              <codeInline>-EnterpriseId</codeInline> - The enterprise ID.</caps:sentence>
                            <caps:sentence id="src157" class="srcSentence"> Either this argument or 'AetxPath' must be provided.</caps:sentence>
                            <caps:sentence id="src158" class="srcSentence"> If this argument is not provided, the enterprise ID is read from the AETX file.</caps:sentence>
                            <caps:sentence id="src159" class="srcSentence"> For example, 1000000001</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src160" class="srcSentence">Deploy the Windows Phone 8.1 Company Portal (SSP.appx) app.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence id="src161" class="srcSentence">The ssp.xap and the Company Portal from the store can both be installed at the same time, which can be confusing for users.</caps:sentence>
                          <caps:sentence id="src162" class="srcSentence"> To have all users using the ssp.xap, create a blocked app for the store version of the Company Portal.</caps:sentence>
                          <caps:sentence id="src163" class="srcSentence"> To have all Windows Phone 8.1 devices to use only the store version of the Company Portal, you have three choices:</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence id="src164" class="srcSentence">If you won’t sideload apps and don’t need to support Windows Phone 8.0, don’t upload the signed ssp.xap.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence id="src165" class="srcSentence">If sideloaded apps are needed, and if there are no Windows Phone 8 devices enrolling, change the automatically created ssp.xap deployment from “available” to “uninstall.”</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence id="src166" class="srcSentence">If sideloaded apps need to be installed and Windows Phone 8.0 devices need to enroll and receive the ssp.xap, create a new software deployment of the ssp.xap and deploy it with the <ui>uninstall</ui> action.</caps:sentence>
                              <caps:sentence id="src167" class="srcSentence"> Windows Phone 8.0 devices don’t support forced install or uninstall of apps, so they will ignore the deployment.</caps:sentence>
                              <caps:sentence id="src168" class="srcSentence"> Windows Phone 8.1 devices support the uninstall action and will remove the ssp.xap.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src169" class="srcSentence">Renew your Symantec enterprise code-signing certificate for Windows devices</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src170" class="srcSentence">The Symantec certificate used to manage certain Windows and Windows Phone mobile devices must be renewed periodically.</caps:sentence>
            <caps:sentence id="src171" class="srcSentence"> For Windows Phone 8.0 devices, a signed Company Portal app and the code-signing certificate are needed for device enrollment.</caps:sentence>
            <caps:sentence id="src172" class="srcSentence"> Later Windows Phone devices can use the company portal app downloaded from the store.</caps:sentence>
            <caps:sentence id="src173" class="srcSentence"> A code-signing certificate is also be required for deploying line-of-business apps.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src174" class="srcSentence">How to renew the Symantec enterprise code-signing certificate</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">Look for a renewal email sent from Symantec approximately 14 days prior to certificate expiration.</caps:sentence>
                    <caps:sentence id="src176" class="srcSentence"> This email contains directions from Symantec about renewing your enterprise certificate.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">For additional information about Symantec certificates, visit <externalLink><linkText>www.symantec.com</linkText><linkUri>http://www.symantec.com</linkUri></externalLink> or call 1-877-438-8776 or 1-650-426-3400.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">Go to the website (example: <externalLink><linkText>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkText><linkUri>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkUri></externalLink>) and login with the Symantec Publisher ID and email addressed associated with the certificate.</caps:sentence>
                    <caps:sentence id="src179" class="srcSentence"> Remember to use the same machine for starting the renewal that you’ll use to download the certificate.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">Once the renewal is approved and paid for, download the certificate.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src181" class="srcSentence">How to install the updated certificate for Windows Phone 8.0</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">Download and sign the latest Windows Phone Company Portal located here: <externalLink><linkText>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">Open your Intune Administration Console (<externalLink><linkText>https://admin.manage.microsoft.com</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink>) and go to <ui>Admin</ui>, <ui>Mobile Device Management</ui> &gt; <ui>Windows Phone</ui> and click <ui>Upload Signed App</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">Upload the newly signed Company Portal.</caps:sentence>
                    <caps:sentence id="src185" class="srcSentence"> You’ll need the newly signed SSP.xap and the new .PFX file you received from Symantec or the application enrollment token that was created with this new .PFX file.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">When the upload is complete, remove the old Company Portal version in the <ui>Software</ui> workspace in the Intune Management Console.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">Sign all enterprise line-of-business apps again using the same certificate and upload and replace existing applications.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src188" class="srcSentence">Providing a signed SSP.xap file is currently the only way to provide the updated code signing certificate.</caps:sentence>
                  <caps:sentence id="src189" class="srcSentence"> To support signed line-of-business apps, you must sign and upload a Company Portal app even though your users will install the Company Portal app from the store.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src190" class="srcSentence">How to install the updated certificate for Windows Phone 8.1 and later devices</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">Download and sign the latest Windows Phone Company Portal from the Download Center located here: <externalLink><linkText>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src192" class="srcSentence">Open your <externalLink><linkText>Intune Administration Console</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink> (https://admin.manage.microsoft.com) and go to <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Windows Phone</ui> and click <ui>Upload Signed App</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src193" class="srcSentence">Upload the newly signed Company Portal.</caps:sentence>
                    <caps:sentence id="src194" class="srcSentence"> You’ll need the newly signed SSP.xap and the new .PFX file you received from Symantec or the Application enrollment token that was created with this new .PFX file.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">When the upload is complete, remove the old Company Portal version in the <ui>Software </ui> workspace.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src196" class="srcSentence">Sign all new and any updated enterprise line-of-business apps using the new certificate.</caps:sentence>
                    <caps:sentence id="src197" class="srcSentence"> Existing applications do not need to be resigned and redeployed.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_FAQ">
        <title>
          <caps:sentence id="src198" class="srcSentence">Frequently asked questions about mobile device management for Microsoft Intune including management with Configuration Manager 2012</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section expanded="false" address="BKMK_Symantec">
            <title>
              <caps:sentence id="src199" class="srcSentence">Why does Windows Phone require a Symantec certificate for management?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src200" class="srcSentence">Windows Phone controls how you can install apps.</caps:sentence>
                <caps:sentence id="src201" class="srcSentence"> Any user with a Microsoft account can install apps from the Windows Phone store, or companies can install or sideload their internally developed line of business (LOB) apps using a special process described in the Windows Phone documentation.</caps:sentence>
                <caps:sentence id="src202" class="srcSentence"> When installing LOB apps, Windows Phones trust only one special type of certificate issued by Symantec.</caps:sentence>
                <caps:sentence id="src203" class="srcSentence"> You cannot use any other commercially or privately generated certificate.</caps:sentence>
                <caps:sentence id="src204" class="srcSentence"> This requirement is true for all mobile device management solutions, not just Intune.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src205" class="srcSentence">The Symantec certificate creates an application enrollment token (AET).</caps:sentence>
                <caps:sentence id="src206" class="srcSentence"> The AET can be installed on a device when the device enrolls for mobile device management, or it can be installed out-of-band from a secure website or from an email attachment.</caps:sentence>
                <caps:sentence id="src207" class="srcSentence"> Administrators must sign every LOB app with the Symantec certificate, using the tools provided in the <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268439</linkUri></externalLink>.</caps:sentence>
                <caps:sentence id="src208" class="srcSentence"> When users attempt to install LOB apps, the Windows Phone operating system checks the signature in the AET against the signature on the app.</caps:sentence>
                <caps:sentence id="src209" class="srcSentence"> If the signatures match, the installation is allowed to proceed.</caps:sentence>
                <caps:sentence id="src210" class="srcSentence"> If the AET cannot be verified, installation fails.</caps:sentence>
                <caps:sentence id="src211" class="srcSentence"> There are several reasons the AET might not be verified:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">The AET was never installed on the device</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src213" class="srcSentence">The AET has expired</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src214" class="srcSentence">The AET was not created using the same Symantec certificate used to sign the app</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src215" class="srcSentence">Windows Phone does not require that the AET be present during MDM enrollment, but prior to the November 2014 release, Intune required the AET and a signed ssp.xap because there was no other way to install the AET and ssp.xap except during enrollment.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src216" class="srcSentence">How is the AET created for Intune users?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src217" class="srcSentence">When administrators upload the .pfx file for their Symantec certificate, Intune automatically creates the AET and deploys it to enrolled Windows Phones.</caps:sentence>
                <caps:sentence id="src218" class="srcSentence"> It is not necessary for Intune admins to use the AET Generator tool in the Windows Phone SDK.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src219" class="srcSentence">Intune does not support manually creating the AET and deploying it out-of-band.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src220" class="srcSentence">What changes happened to reduce the requirement for a Symantec certificate?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src221" class="srcSentence">For the November 2014 release, Intune made changes to allow for scenarios where companies do not have a Symantec certificate.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src222" class="srcSentence">The Company Portal for Windows Phone 8.1 is available to install from the store, so it needn’t be signed with a Symantec certificate and validated against an AET.</caps:sentence>
                    <caps:sentence id="src223" class="srcSentence"> Instead, the app is validated as part of the store publishing process.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src224" class="srcSentence">Windows Phone 8.1 devices can enroll with or without an AET on the phone.</caps:sentence>
                    <caps:sentence id="src225" class="srcSentence"> If an AET is available, it will be installed the first time the device synchronizes with Intune.</caps:sentence>
                    <caps:sentence id="src226" class="srcSentence"> If there is no AET, the device can still be managed by Intune, and users can install the Company Portal from the store and use most features of the Company Portal without a Symantec certificate to sign apps.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src227" class="srcSentence">There are no changes to the Symantec requirement for Windows Phone 8 devices.</caps:sentence>
                <caps:sentence id="src228" class="srcSentence"> Windows Phone 8 devices must have the signed ssp.xap and the AET present during enrollment or they will be blocked from enrolling.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src229" class="srcSentence">What functionality is supported if a Windows Phone 8.1 device is enrolled but there is no Symantec certificate?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src230" class="srcSentence">If a Windows Phone 8.1 device is enrolled but there’s no Symantec certificate, you can:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src231" class="srcSentence">Create policies and push them to the device</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src232" class="srcSentence">Configure contact information for the IT department that will shows in the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src233" class="srcSentence">Create deep links to the store and deploy them to the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src234" class="srcSentence">Create links to web pages and deploy them to the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src235" class="srcSentence">Create terms and conditions that must be accepted by users before they can use the Company Portal</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src236" class="srcSentence">The one thing you cannot do without a Symantec certificate is deploy LOB apps.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src237" class="srcSentence">The Intune Software Publisher does not verify that apps are signed when you upload them.</caps:sentence>
                  <caps:sentence id="src238" class="srcSentence"> If you deploy unsigned apps, they will fail when users try to install them.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src239" class="srcSentence">What can users do if they have the Company Portal but there is no Symantec certificate?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src240" class="srcSentence">Windows Phone 8.1 devices don’t have to be enrolled before users install the Company Portal from the store.</caps:sentence>
                <caps:sentence id="src241" class="srcSentence"> If the device is not enrolled, users are prompted to enroll.</caps:sentence>
                <caps:sentence id="src242" class="srcSentence"> Touching the prompt in the Company Portal takes users directly to <ui>Settings / Workplace</ui> where they can enroll their devices.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src243" class="srcSentence">Even without enrolling the device, uses can perform the following actions with the Company Portal installed from the store:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src244" class="srcSentence">Accept or decline any terms and conditions configured by the admin.</caps:sentence>
                    <caps:sentence id="src245" class="srcSentence"> If users decline the terms and conditions, the Company Portal closes.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src246" class="srcSentence">View the contact information for the IT department</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src247" class="srcSentence">View any enrolled devices including iOS, Android, and Windows devices</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src248" class="srcSentence">Use deep links to apps in the store</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src249" class="srcSentence">Use web links to open web pages</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src250" class="srcSentence">With the device enrolled, users can view the device in the <ui>My Devices</ui> list.</caps:sentence>
                <caps:sentence id="src251" class="srcSentence"> Once enrolled, the device is subject to any deployed Intune policies.</caps:sentence>
                <caps:sentence id="src252" class="srcSentence"> Devices must be enrolled to get the AET and install LOB apps.</caps:sentence>
                <caps:sentence id="src253" class="srcSentence"> An unenrolled device trying to install an LOB app will be directed to enroll.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src254" class="srcSentence">The only thing users cannot do if the company does not have a Symantec certificate is install LOB apps deployed by the admin.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src255" class="srcSentence">Our company already has a certificate and has been enrolling Windows Phone 8.1 devices.</caps:sentence>
              <caps:sentence id="src256" class="srcSentence"> Do I have to do anything different now that the Company Portal is available in the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src257" class="srcSentence">The current ssp.xap from the Download Center still works on Windows Phone 8.1 devices.</caps:sentence>
                <caps:sentence id="src258" class="srcSentence"> You can continue to direct users to enroll and get the company portal during installation.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src259" class="srcSentence">What are the advantages and disadvantages of users getting the Company Portal from the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src260" class="srcSentence">Advantages:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src261" class="srcSentence">Users get deep links and web links, even if the Windows Phone 8.1 device isn’t enrolled</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src262" class="srcSentence">When Microsoft updates the Company Portal, the store app updates automatically without your downloading, signing, and redeploying the ssp.xap</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src263" class="srcSentence">Documentation for Windows Phone 8.1, iOS, Android, and Windows users is consistent: “Go to the store and install the Company Portal.”</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src264" class="srcSentence">Users see the app as it installs and get enrollment instructions when it opens</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src265" class="srcSentence">Disadvantages:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src266" class="srcSentence">Users see a checkbox to install a “<ui>company hub</ui>” but nothing directs them to the Company Portal in the device’s app list</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src267" class="srcSentence">Users aren’t required to accept custom terms and conditions until they open the Company Portal</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src268" class="srcSentence">In the following circumstances, you can continue directing users to enroll and have the ssp.xap installed during enrollment:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src269" class="srcSentence">If the company blocks access to the store from Windows Phones, users must get the ssp.xap installed during enrollment.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src270" class="srcSentence">If users do not have Microsoft accounts configured on their Windows Phones, they will not be able to install the Company Portal from the store.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src271" class="srcSentence">If the existing documentation for Windows Phone enrollment tells them to go to Settings, Workplace first, it may take a while to update the docs and direct users to the store.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src272" class="srcSentence">What’s the difference between the ssp.xap on the Download Center and the app in the store?</caps:sentence>
            </title>
            <content>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src273" class="srcSentence">The Company Portal in the store does not have to be signed by a Symantec certificate to be installed</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src274" class="srcSentence">The Company Portal in the store presents the terms and conditions to the user but the ssp.xap on the Download Center doesn’t</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src275" class="srcSentence">The Company Portal in the store is an .appx instead of a .xap</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src276" class="srcSentence">Can I get the Company Portal file and push it to my users instead of sending them to the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src277" class="srcSentence">Yes.</caps:sentence>
                <caps:sentence id="src278" class="srcSentence"> The Company Portal app can be downloaded for the following operating systems from the Download Center:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src279" class="srcSentence">Windows Phone 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615799</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src280" class="srcSentence">Windows Phone 8.0 : <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=268440</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src281" class="srcSentence">Windows 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615800</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615800</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src282" class="srcSentence">Can companies still use the Support Tool for Windows Intune Trial Management of Windows Phone if they don’t have a Symantec certificate, and still have users install the Company Portal from the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src283" class="srcSentence">Yes.</caps:sentence>
                <caps:sentence id="src284" class="srcSentence"> If you need to do a proof of concept that includes installation of LOB apps, the trial management tool works with the store version of the company portal.</caps:sentence>
                <caps:sentence id="src285" class="srcSentence"> Because the AET from the Symantec certificate is no longer required to enroll Windows Phone 8.1 devices, however, companies can test app installation using deep links to apps in the store.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src286" class="srcSentence">The Support Tool for Windows Intune Trial Management of Windows Phone is only for trial subscriptions of Intune.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src287" class="srcSentence">Only use the trial management tool testing.</caps:sentence>
                  <caps:sentence id="src288" class="srcSentence"> Devices enrolled with the AET from the trial management tool must unenroll and reenroll if the Symantec certificate for the trial management tool is no longer available, or if the company obtains its own Symantec certificate for signing apps.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src289" class="srcSentence">Can companies start without any Symantec certificate and then add one later, even after Windows Phone 8.1 devices have enrolled?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src290" class="srcSentence">Yes.</caps:sentence>
                <caps:sentence id="src291" class="srcSentence"> Even if Windows Phone 8.1 devices have already enrolled, you can get a Symantec certificate, sign the ssp.xap, and upload it and the pfx file.</caps:sentence>
                <caps:sentence id="src292" class="srcSentence"> Intune will then generate the AET.</caps:sentence>
                <caps:sentence id="src293" class="srcSentence"> Windows Phone 8.1 devices will get the AET the next time they sync, up to eight hours.</caps:sentence>
                <caps:sentence id="src294" class="srcSentence"> Allow at least eight hours before deploying line of business apps after uploading the xap and pfx.</caps:sentence>
              </para>
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