---
title: Habilitar el acceso a los recursos de empresa mediante perfiles de certificados con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8cbb8499-611d-4217-a7b4-e9b864785dd0
---
# Habilitar el acceso a los recursos de empresa mediante perfiles de certificados con Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6ad24a3828bbe378593f8bfd8740d9e1" id="tgt1" class="tgtSentence">Los perfiles de certificado son directivas de <token>wit_nextref</token> que configuran los dispositivos administrados con los certificados que se necesitan para que los usuarios de dispositivos puedan conectarse a los recursos de empresa locales mediante Wi-Fi o VPN.</caps:sentence>
          <caps:sentence sentenceid="dc18cd32d7e6f13aa623b15234dcd23a" id="tgt2" class="tgtSentence"> Al implementar perfiles de certificado, aprovisiona los dispositivos con un certificado raíz de confianza para la PKI y los configura para que soliciten certificados específicos del dispositivo.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="49d71e874cdca7189da6fe08d9d8b873" id="tgt3" class="tgtSentence">Puede crear tres tipos de perfiles de certificado:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="bbcbdf80ea752b973228cb8f384d6f8c" id="tgt4" class="tgtSentence">Perfil de certificado PKCS #12 (.PFX): se puede usar con Android 4.0 o posterior, así como con Windows 10 (escritorio y móvil) y versiones posteriores.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5ea62101efc39af46d89c767dcebf2a1" id="tgt5" class="tgtSentence">Perfil de certificado SCEP: se puede usar con iOS 6.0 y versiones posteriores, Android 4.0 o posterior y Windows Phone 8.1 y versiones posteriores.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0aaa520e4e732b28016e21792618a709" id="tgt6" class="tgtSentence">Perfil de certificado de confianza: se puede usar con iOS 6.0 y versiones posteriores, Android 4.0 o posterior y Windows Phone 8.1 y versiones posteriores.</caps:sentence>
            </para>
          </listItem>
        </list>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="dd6edde4f3adef42958c8bc92729fa33" id="tgt7" class="tgtSentence">Acerca de los perfiles de certificado</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt8" class="tgtSentence">Detalles</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4b39f7e68c8fb1820e3a8c540e28572b" id="tgt9" class="tgtSentence">Use perfiles de certificado para:</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="f5bfb85dec5e77a36f5ac3e38d49d8c8" id="tgt10" class="tgtSentence">Configurar dispositivos automáticamente de modo que se pueda obtener acceso a recursos de la empresa sin tener que instalar certificados manualmente o mediante un proceso fuera de banda</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="fbcc47b16401ee95c6e235d2b24a0a3a" id="tgt11" class="tgtSentence">Ayudar a proteger los recursos de empresa mediante el uso de la infraestructura de clave pública (PKI) de la empresa</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="22758fd9d54345ad24cd44e8315eabd7" id="tgt12" class="tgtSentence">Poder usar la autenticación de servidor para todas las conexiones, por ejemplo, VPN y Wi-Fi, porque ya aprovisionó los certificados necesarios en los dispositivos administrados</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="3763a2f295e86b45f49223fb08be1e2c" id="tgt13" class="tgtSentence">Los perfiles de certificado proporcionan las siguientes capacidades de administración:</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="d33be784350e1ab72ffa555611eeda89" id="tgt14" class="tgtSentence">Inscripción y renovación de certificados de una entidad de certificación (CA) empresarial para dispositivos que ejecutan:</caps:sentence>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="c31b32364ce19ca8fcd150a417ecce58" id="tgt15" class="tgtSentence">Android</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="9e304d4e8df1b74cfa009913198428ab" id="tgt16" class="tgtSentence">iOS</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="ff096d14c13e95dfc9db9eb98f194114" id="tgt17" class="tgtSentence">Windows 8.1</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence sentenceid="4693857bd32521105efeea9c79338cde" id="tgt18" class="tgtSentence">Windows Phone 8,1</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </listItem>
                </list>
                <para>
                  <caps:sentence sentenceid="48b79636f396331a3f0bc735cdfa1a05" id="tgt19" class="tgtSentence">Estos certificados se pueden usar después para realizar conexiones a nuestra infraestructura local.</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="f6a831ffce41e27077a4a8f88b358bc3" id="tgt20" class="tgtSentence">Implementación de certificados de CA raíz de confianza y certificados de CA intermedia para configurar una cadena de confianza en dispositivos para conexiones en las que se requiere la autenticación de servidor.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="f8ad15aa470c65132aa3a3d7f2ea2145" id="tgt21" class="tgtSentence">Supervisar los certificados instalados y notificar acerca de ellos.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e0aaea9ecd805033b2c0441cf5b607aa" id="tgt22" class="tgtSentence">Ejemplos de cuándo usar perfiles de certificado:</caps:sentence>
                </para>
                <para></para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="932b9085b2fe69e5dca42882fe9a75b4" id="tgt23" class="tgtSentence">Los empleados deben poder conectarse a zonas Wi-Fi en varias ubicaciones de la empresa.</caps:sentence>
                      <caps:sentence sentenceid="448c1bac9b9302e81f1e52fff2c3b153" id="tgt24" class="tgtSentence"> Para ello, puede usar perfiles de certificado para implementar los certificados necesarios para proteger la conexión Wi-Fi.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="649bfdffbc04d8ac9ee3814271cd6e1d" id="tgt25" class="tgtSentence">Dispone de una PKI local y quiere optar por un método más flexible y seguro de aprovisionamiento de certificados que permita a los usuarios obtener acceso a los recursos de empresa desde sus dispositivos personales sin poner en riesgo la seguridad.</caps:sentence>
                      <caps:sentence sentenceid="90b656b383ab3c076de765bcf8d9f0b7" id="tgt26" class="tgtSentence"> Para ello, puede configurar perfiles de certificados con las opciones y los protocolos admitidos en la plataforma específica del dispositivo.</caps:sentence>
                      <caps:sentence sentenceid="21457a9d60710d4795a2d7c74cfae59f" id="tgt27" class="tgtSentence"> Los dispositivos pueden solicitar automáticamente estos certificados desde un servidor de inscripción accesible desde Internet.</caps:sentence>
                      <caps:sentence sentenceid="87777ccb79c76f744e484b0a533d42bb" id="tgt28" class="tgtSentence"> Después, puede configurar los perfiles de VPN para que usen estos certificados y que el dispositivo pueda acceder a los recursos de empresa.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="11d96e1b00b8baa7532310017343c23a" id="tgt29" class="tgtSentence">Tipos de perfiles de certificado</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt30" class="tgtSentence">Detalles</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <embeddedLabel>
                    <caps:sentence sentenceid="c03810aeecedbc4d64ed7ec340dd347a" id="tgt31" class="tgtSentence">Perfil de certificado raíz de confianza</caps:sentence>
                  </embeddedLabel>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="766304761b19f5d8bdc7045b8923366c" id="tgt32" class="tgtSentence">Use este perfil para implementar el certificado de CA raíz de confianza o certificado de CA intermedia en dispositivos:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="a27eeefc5391e9f1beddde41a5de00c1" id="tgt33" class="tgtSentence">Cree un perfil de certificado raíz de confianza para cada plataforma que use.</caps:sentence>
                      <caps:sentence sentenceid="dbb86062b46bb150548741bbb5e034b6" id="tgt34" class="tgtSentence"> Asócielo a cada perfil de certificado SCEP que cree para esa misma plataforma.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <embeddedLabel>
                    <caps:sentence sentenceid="57d86cbe96e309396ad75e1cd46ea484" id="tgt35" class="tgtSentence">Perfil de certificado .PFX</caps:sentence>
                  </embeddedLabel>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d80fc3c92f3a3faf5f402bd76ed89b98" id="tgt36" class="tgtSentence">Use este perfil para implementar la configuración específica de la plataforma para solicitudes de certificados de dispositivo:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="47435b08da0d06de018709e321a1000e" id="tgt37" class="tgtSentence">Cree un perfil de certificado .PFX para cada plataforma que use y emparéjelo con el perfil de certificado de CA de confianza.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="5eb9277dd9eff86e8cd7c4a000085382" id="tgt38" class="tgtSentence">Para completar la tarea de crear un perfil de certificado .PFX, debe seleccionar un perfil de certificado de CA de confianza creado anteriormente.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <embeddedLabel>
                    <caps:sentence sentenceid="93967096991e77284da494250069039c" id="tgt39" class="tgtSentence">Perfil de configuración del Protocolo de inscripción de certificados simple (SCEP)</caps:sentence>
                  </embeddedLabel>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d80fc3c92f3a3faf5f402bd76ed89b98" id="tgt40" class="tgtSentence">Use este perfil para implementar la configuración específica de la plataforma para solicitudes de certificados de dispositivo:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="ab9f933c26d753e4afbca53f8294e968" id="tgt41" class="tgtSentence">Cree un perfil de certificado SCEP para cada plataforma que use y emparéjelo con el perfil de certificado de CA de confianza.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence sentenceid="3419615289691fb3312e6a98507f9db4" id="tgt42" class="tgtSentence">Para completar la tarea de crear un perfil de certificado SCEP, debe seleccionar un perfil de certificado de CA de confianza creado anteriormente.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="4b7148d84e7fcf2dbbfcdec648dd07a4" id="tgt43" class="tgtSentence">Para usar perfiles de certificado SCEP, debe integrar la siguiente infraestructura local con <token>wit_nextref</token>:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="6d0970bb1961a81a5c06d9e17fefb45d" id="tgt44" class="tgtSentence">Un servidor que ejecute el Servicio de inscripción de dispositivos de red</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="3804e8a3fe7a969d59028aacfa3975d0" id="tgt45" class="tgtSentence">Una entidad de certificación empresarial</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e99876cbac0de49bd2dfb540530e852e" id="tgt46" class="tgtSentence">El conector de certificado de Intune, que se instala en el servidor de Windows Server 2012 R2 que ejecuta NDES</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="0c2492ffde9ce4a3e227ba4646130de5" id="tgt47" class="tgtSentence">Para usar perfiles de certificado .PFX, debe integrar la siguiente infraestructura local con <token>wit_nextref</token>:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="f326524ca1b727b4e3f519730b4a611b" id="tgt48" class="tgtSentence">Una entidad de certificación empresarial.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="97dc2896324c3b319a44aa4e454cc376" id="tgt49" class="tgtSentence">Un equipo que puede comunicarse con la entidad de certificación o usar el mismo equipo de la entidad de certificación.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6119b57b39f2964124533c78ce3e1f98" id="tgt50" class="tgtSentence">El conector de certificado de Intune, que se ejecuta en el equipo que puede comunicarse con la entidad de certificación.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="d68d31d46d060f2a875dc84360e05ed5" id="tgt51" class="tgtSentence">En este tema:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0#BKMK_CertProfileRequirements">Requirements for certificate profiles</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0#BKMK_ConfigureInfrastructure">Configure your infrastructure</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0#BKMK_ConfigProfiles">Configure certificate profiles</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0#BKMK_Deploy">Deploy certificate profiles</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_CertProfileRequirements">
        <title>
          <caps:sentence sentenceid="307d40c1ec68fad9507d8b56479ef214" id="tgt52" class="tgtSentence">Requisitos de los perfiles de certificado</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section address="BKMK_OnPremises" expanded="false">
            <title>
              <caps:sentence sentenceid="d6167847a99d514149a0df6871047aed" id="tgt53" class="tgtSentence">Infraestructura local</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6e3301c94e4de897ec67fa9735a848d5" id="tgt54" class="tgtSentence">Infraestructura</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt55" class="tgtSentence">Detalles</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="793d7ce16c080766e2d47ef3ff703353" id="tgt56" class="tgtSentence">Dominio de Active Directory</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2fd0d10c9dfe7448bfb9da7c6af94490" id="tgt57" class="tgtSentence">Todos los servidores enumerados en esta sección (excepto el servidor proxy de aplicación web) deben estar unidos al dominio de Active Directory.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="1939cb07b2c5a9364225fcdd9fcc3566" id="tgt58" class="tgtSentence">Servidor de la entidad de certificación</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5a99053965263faad79089009dea465e" id="tgt59" class="tgtSentence">También llamada CA emisora, es necesario disponer de una entidad de certificación (CA) empresarial que se ejecute en una edición Enterprise de <token>nextref_server_7</token> o en una posterior.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="76a433db2d3979e5c9da0e2de2335672" id="tgt60" class="tgtSentence">No se admiten CA independientes.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="eb65a20938cf7a683c4b6e108901e9e0" id="tgt61" class="tgtSentence">Para obtener instrucciones sobre cómo configurar una entidad de certificación, consulte <externalLink><linkText>Instalar la entidad de certificación</linkText><linkUri>http://technet.microsoft.com/library/jj125375.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="873db829e9faae3bffc58afba54423f4" id="tgt62" class="tgtSentence">Si la CA ejecuta Windows Server 2008 R2, se debe <externalLink><linkText>instalar la revisión de KB2483564</linkText><linkUri>http://support.microsoft.com/kb/2483564/</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="64d00273ce506e922cad589b29c1d395" id="tgt63" class="tgtSentence">Para el perfil SCEP únicamente: <embeddedLabel>servidor NDES</embeddedLabel></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="51478fce5857cc916cdc1186fcbc5111" id="tgt64" class="tgtSentence">En un servidor que ejecute <token>winblue_server_2</token> o versiones posteriores, debe configurar el Servicio de inscripción de dispositivos de red:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="1173819e58da9ba2d0fcfbce7e338d00" id="tgt65" class="tgtSentence">
                              <token>wit_nextref</token> no admite el uso del Servicio de inscripción de dispositivos de red cuando se ejecuta en un servidor que también ejecuta la CA empresarial.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="4462659de4d522ffbc363a78e3f7fd9f" id="tgt66" class="tgtSentence">Consulte la <externalLink><linkText>Orientación para el Servicio de inscripción de dispositivos de red</linkText><linkUri>http://technet.microsoft.com/library/hh831498.aspx</linkUri></externalLink> a fin de obtener instrucciones sobre cómo configurar <token>winblue_server_2</token> para hospedar el Servicio de inscripción de dispositivos de red.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5a81c11d73b1f907825765fc6585e7ed" id="tgt67" class="tgtSentence">Para el perfil del certificado .PFX: <embeddedLabel>un equipo que puede comunicarse con la entidad de certificación</embeddedLabel></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3acefd8ef1a79834b1180a4df2756f34" id="tgt68" class="tgtSentence">También puede usar el mismo equipo de la entidad de certificación.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9781b62d0e687e3d5e772f805a335d75" id="tgt69" class="tgtSentence">
                          <embeddedLabel>Servidor proxy de aplicación web</embeddedLabel> (opcional).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="87395bb0daf640f7cf758132d75d61c4" id="tgt70" class="tgtSentence">Puede usar un servidor que ejecute <token>winblue_server_2</token> o una versión posterior como servidor proxy de aplicación web (WAP).</caps:sentence>
                        <caps:sentence sentenceid="7bb1df2f4ddea1e50769f2d8f0431377" id="tgt71" class="tgtSentence"> Esta configuración:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="6ccf387a9957436f963e5302e5f0043c" id="tgt72" class="tgtSentence">Permite a los dispositivos recibir certificados mediante una conexión a Internet.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="9be3bc5f8fa204585560ef5434afb15e" id="tgt73" class="tgtSentence">Es una recomendación de seguridad cuando los dispositivos se conectan a través de Internet para recibir y renovar certificados.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="5cddce056f7250fe92b20dda8183e544" id="tgt74" class="tgtSentence">El servidor que hospeda WAP <externalLink><linkText>debe instalar una actualización</linkText><linkUri>http://blogs.technet.com/b/ems/archive/2014/12/11/hotfix-large-uri-request-in-web-application-proxy-on-windows-server-2012-r2.aspx</linkUri></externalLink> que habilite la compatibilidad con las direcciones URL largas que usa el Servicio de inscripción de dispositivos de red.</caps:sentence>
                        <caps:sentence sentenceid="a2f46c06b36b50d332d21e532c42dca6" id="tgt75" class="tgtSentence"> Esta actualización está incluida en el <externalLink><linkText>paquete acumulativo de actualizaciones de diciembre de 2014</linkText><linkUri>http://support.microsoft.com/kb/3013769</linkUri></externalLink> o está disponible por separado, en <externalLink><linkText>KB3011135</linkText><linkUri>http://support.microsoft.com/kb/3011135</linkUri></externalLink>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="114b4e7e345073b5a0983b44b01487aa" id="tgt76" class="tgtSentence">Además, el servidor que hospeda WAP debe:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="974f951f8f549d676ee1a199fdb48715" id="tgt77" class="tgtSentence">Tener un certificado SSL que coincida con el nombre que se publica para los clientes externos.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d56550fbb2e9765cbf11ccee4cd9e0ab" id="tgt78" class="tgtSentence">Confiar en el certificado SSL que se usa en el servidor NDES.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="d456170d35f5144bd3772b3d2616ba7b" id="tgt79" class="tgtSentence">Estos certificados habilitan al servidor WAP para terminar la conexión SSL entre clientes y crear una nueva conexión SSL hacia el servidor NDES.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="258e3d81ad718c3a5eac8e4e71393c53" id="tgt80" class="tgtSentence">Para obtener información sobre certificados de WAP, consulte la sección <embeddedLabel>Planear certificados</embeddedLabel> de <externalLink><linkText>Instalar y configurar el Proxy de aplicación web para publicar aplicaciones internas</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn383650.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="bf7db0e86631dca5a3aae7ea9013b42b" id="tgt81" class="tgtSentence">Para obtener información general sobre los servidores WAP, consulte <externalLink><linkText>Working with Web Application Proxy</linkText><linkUri>http://technet.microsoft.com/library/dn584113.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="93746d37532d2138f1b604991c0028db" id="tgt82" class="tgtSentence">Conector de certificado de Microsoft Intune</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2658fee835b96fbcb558640f217a4ed7" id="tgt83" class="tgtSentence">Use la consola de administración de <token>wit_nextref</token> para descargar el instalador del <embeddedLabel>Conector de certificado</embeddedLabel> (<legacyBold>ndesconnectorssetup.exe</legacyBold>).</caps:sentence>
                        <caps:sentence sentenceid="4c6866ebfe399e340f6b0b54f3d7fee7" id="tgt84" class="tgtSentence"> Después, puede ejecutar <embeddedLabel>ndesconnectorssetup.exe</embeddedLabel> en el equipo donde desee instalar el conector de certificado.</caps:sentence>
                        <caps:sentence sentenceid="4cf0ae1668c595f7f2c4ebc229e0853e" id="tgt85" class="tgtSentence"> Para perfiles de certificado .PFX, instale el conector de certificado en el equipo que se comunica con la entidad de certificación.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_CertsAndTemplates" expanded="false">
            <title>
              <caps:sentence sentenceid="bc85113e7e2abda72b3529d241638d12" id="tgt86" class="tgtSentence">Certificados y plantillas</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a8cfde6331bd59eb2ac96f8911c4b666" id="tgt87" class="tgtSentence">Objeto</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt88" class="tgtSentence">Detalles</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="6b3e14469608dc57fc7fbc2fce41e1e2" id="tgt89" class="tgtSentence">Plantilla de certificado</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="69d9cf356d1cabae8e85396cf967d421" id="tgt90" class="tgtSentence">Esta plantilla se configura en la CA emisora.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="0b7dbdc46cb3f88fd0e9561117e5632e" id="tgt91" class="tgtSentence">Certificado de autenticación del cliente</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a9355623f07a0d5f6b7f034c31df8b64" id="tgt92" class="tgtSentence">Solicitado desde la CA emisora o la CA pública, instale este certificado en el servidor NDES.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="e47ac2dedde8390879763ba8ced5ed8b" id="tgt93" class="tgtSentence">Certificado de autenticación de servidor</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b48f1cd40a83dfc7198f1779f7b54336" id="tgt94" class="tgtSentence">Solicitado desde la CA emisora o la CA pública, este certificado SSL se instala y se enlaza en IIS, en el servidor NDES.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="bf5a0d198b294873502034b0fc8d384f" id="tgt95" class="tgtSentence">Certificado de CA raíz de confianza</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7ecef5d4400c91c0054534516dfad14c" id="tgt96" class="tgtSentence">Expórtelo como archivo <embeddedLabel>.cer</embeddedLabel> desde la CA emisora o desde cualquier dispositivo que confíe en la CA emisora e impleméntelo en dispositivos con el perfil de certificado de CA de confianza.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="53f8f710d62cc02eee893d0471d41a24" id="tgt97" class="tgtSentence">Use un único certificado de CA raíz de confianza por cada plataforma de sistema operativo y asócielo a cada perfil de certificado raíz de confianza que cree.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="68420e0b6d8ea99dc38d8bdd9763f749" id="tgt98" class="tgtSentence">Puede usar certificados de CA raíz de confianza adicionales cuando sea necesario.</caps:sentence>
                            <caps:sentence sentenceid="3620c4202eba5eb7a5617531c1133eea" id="tgt99" class="tgtSentence"> Por ejemplo, podría hacerlo para proporcionar una relación de confianza con una CA que firme los certificados de autenticación de servidor para los puntos de acceso Wi-Fi.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_Accounts" expanded="false">
            <title>
              <caps:sentence sentenceid="7a90e38a211ece1c346928e7d1f3e968" id="tgt100" class="tgtSentence">Cuentas</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt101" class="tgtSentence">Nombre</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="27792947ed5d5da7c0d1f43327ed9dab" id="tgt102" class="tgtSentence">Detalles</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="45910ff07ebdaa8a2433a9652f1b6f5f" id="tgt103" class="tgtSentence">Cuenta de servicio NDES</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="21e0a9bc6077ce6b8e3760403ad82486" id="tgt104" class="tgtSentence">Especifique una cuenta de usuario de dominio que se vaya a usar como cuenta de servicio NDES.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_ConfigureInfrastructure">
        <title>
          <caps:sentence sentenceid="839111dde777e0180f30d43c814fd3b3" id="tgt105" class="tgtSentence">Configurar la infraestructura</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f273bbd6217ee69362ebc42596e5b5d4" id="tgt106" class="tgtSentence">Para poder configurar perfiles de certificado debe completar las tareas siguientes, que requieren conocimientos de Windows Server 2012 R2 y Servicios de certificados de Active Directory (ADCS):</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="5f902456eab0b713ecdbc1f1ae8a5820" id="tgt107" class="tgtSentence">
              <embeddedLabel>Tarea 1</embeddedLabel>: configurar plantillas de certificado en la entidad de certificación <br /><embeddedLabel>Tarea 2</embeddedLabel> (únicamente para el perfil SCEP): configurar los requisitos previos en el servidor NDES <br /><embeddedLabel>Tarea 3</embeddedLabel> (únicamente para el perfil SCEP): configurar NDES para su uso con <token>wit_nextref</token><br /><embeddedLabel>Tarea 4</embeddedLabel>: habilitar, instalar y configurar el conector del certificado de Intune</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_ConfigOnPremTask1">
            <title>
              <caps:sentence sentenceid="0c43e42ecbe27d1cf79194c43c4154e8" id="tgt108" class="tgtSentence">Tarea 1: configurar plantillas de certificado en la entidad de certificación</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="1d1a0de5dbaf576b7fb1d3c1fa53960a" id="tgt109" class="tgtSentence">En esta tarea tendrá que:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a9b017c94494459e6ee02c78cf625af5" id="tgt110" class="tgtSentence">Crear una cuenta de servicio NDES</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="ceb660e279a229a4708f928020d3f1ea" id="tgt111" class="tgtSentence">Para revocar certificados de la cuenta de servicio NDES, necesitará los derechos para <legacyItalic>emitir y administrar certificados</legacyItalic> referentes a cada plantilla de certificado que use un perfil de certificado.</caps:sentence>
                    </para>
                  </alert>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="1137bca9ad54e771092ebdd8eff3fc8c" id="tgt112" class="tgtSentence">Configurar una plantilla de certificado para NDES</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="374fcf741cc7055e14a2c9648d92cd80" id="tgt113" class="tgtSentence">Publicar la plantilla de certificado para NDES</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="957c0ced48d7f4583728fba675ae2a05" id="tgt114" class="tgtSentence">Para configurar la entidad de certificación</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ef36acad492f9a83b90572b627f1b435" id="tgt115" class="tgtSentence">Cree una cuenta de usuario de dominio que vaya a usar como cuenta de servicio NDES.</caps:sentence>
                        <caps:sentence sentenceid="893b906701299d99685a614640444c9c" id="tgt116" class="tgtSentence"> Deberá especificar esta cuenta al configurar las plantillas en la CA emisora antes de instalar y configurar NDES.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="f421e06fc59a010345039f992681046c" id="tgt117" class="tgtSentence">En la CA emisora, use el complemento Plantillas de certificado para crear una nueva plantilla personalizada o copiar una plantilla existente y, luego, editarla (por ejemplo, la plantilla de usuario) para su uso con NDES.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1dd97edcae8ce2ddcc5ff5edf4401bf4" id="tgt118" class="tgtSentence">La plantilla debe tener las siguientes configuraciones:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="6ff09561e6d910d44e20273eaadda002" id="tgt119" class="tgtSentence">Especifique <ui>Nombre para mostrar de plantilla</ui> descriptivo para la plantilla.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt120" class="tgtSentence">En la pestaña <ui>Nombre del firmante</ui>, seleccione <ui>Proporcionado por el solicitante</ui>.</caps:sentence>
                            <caps:sentence sentenceid="e1713b0524c8d01785f1f4d93027b82a" id="tgt121" class="tgtSentence"> (La seguridad la aplica el módulo de directivas de <token>wit_nextref</token> para NDES).</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt122" class="tgtSentence">En la pestaña <ui>Extensiones</ui>, asegúrese de que <ui>Descripción de las directivas de aplicación</ui> incluya <ui>Autenticación del cliente</ui>.</caps:sentence>
                          </para>
                          <alert class="important">
                            <para>
                              <caps:sentence sentenceid="afacb8a67ecd6e34a6c4103a81c40864" id="tgt123" class="tgtSentence">En el caso de plantillas de certificado de iOS, en la pestaña <ui>Extensiones</ui>, edite <ui>Uso de claves</ui> y asegúrese de que la opción <ui>Firma como prueba de origen</ui> no esté seleccionada.</caps:sentence>
                            </para>
                          </alert>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt124" class="tgtSentence">En la pestaña <ui>Seguridad</ui>, agregue la cuenta de servicio NDES y otórguele permisos de <ui>Lectura</ui> e <ui>Inscripción</ui> en la plantilla.<br /></caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="676a72738c92d941904ce541c153e3ae" id="tgt125" class="tgtSentence">Revise la configuración de <ui>Período de validez</ui> en la pestaña <ui>General</ui> de la plantilla.</caps:sentence>
                        <caps:sentence sentenceid="59c2118fd6b6def5354a8537930622c0" id="tgt126" class="tgtSentence"> De forma predeterminada, <token>wit_nextref</token> usa el valor configurado en la plantilla.</caps:sentence>
                        <caps:sentence sentenceid="a7da7ba166aeeee2b927a28b1f6a6e41" id="tgt127" class="tgtSentence"> Sin embargo, tiene la opción de configurar la CA para permitir que el solicitante especifique un valor diferente, lo que se puede establecer desde la consola de administrador de <token>wit_nextref</token>.</caps:sentence>
                        <caps:sentence sentenceid="c62e687a5b129c3da51e00e218cbe436" id="tgt128" class="tgtSentence"> Si desea usar siempre el valor de la plantilla, omita el resto de este paso.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence sentenceid="2c38acc61f119f8e2bdfc330c78bcab0" id="tgt129" class="tgtSentence">La plataforma iOS siempre usa el valor establecido en la plantilla con independencia de otras configuraciones que realice.</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence sentenceid="3738f17a48ea68a0571595ecc4d76ccf" id="tgt130" class="tgtSentence">Para configurar la CA para permitir que el solicitante especifique el período de validez, en la CA, ejecute los siguientes comandos:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <userInput>
                              <caps:sentence sentenceid="e861718e4d63f8499bad2b6fe60c4a11" id="tgt131" class="tgtSentence">certutil -setreg Policy\EditFlags +EDITF_ATTRIBUTEENDDATE</caps:sentence>
                            </userInput>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <userInput>
                              <caps:sentence sentenceid="648591291926d0f1ae9b97b2fcc5a112" id="tgt132" class="tgtSentence">net stop certsvc</caps:sentence>
                            </userInput>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <userInput>
                              <caps:sentence sentenceid="ccf748c45a6ac0a5fbdf96ca486cea33" id="tgt133" class="tgtSentence">net start certsvc</caps:sentence>
                            </userInput>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="fadc9ebfdf92c0816690fe501d42d339" id="tgt134" class="tgtSentence">En la CA emisora, use el complemento Entidad de certificación para publicar la plantilla de certificado.</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="7486589d03c162162a7c4e75345fcca4" id="tgt135" class="tgtSentence">Seleccione el nodo <ui>Plantillas de certificado</ui>, haga clic en <ui>Acción</ui> &gt; <ui>Nueva</ui> &gt; <ui>Plantilla de certificado que se va a emitir</ui> y seleccione la plantilla que creó en el paso 2.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="f4a8fd189854ec1308e12aa4d1a1fe43" id="tgt136" class="tgtSentence">Valide que la plantilla se publicó visualizándola en la carpeta <ui>Plantillas de certificado</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="989fe4f2791953694a5188d1e0476462" id="tgt137" class="tgtSentence">Para perfiles .PFX: en el equipo de CA asegúrese de que el equipo que hospeda el conector de certificado de Intune haya inscrito el permiso, para que pueda tener acceso a la plantilla utilizada en la creación del perfil .PFX.</caps:sentence>
                        <caps:sentence sentenceid="4fe55a0891cac48f6dda8fd345997451" id="tgt138" class="tgtSentence"> Establezca ese permiso en la pestaña <ui>Seguridad</ui> de las propiedades del equipo de CA.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_ConfigOnPremTask2">
            <title>
              <caps:sentence sentenceid="cf3eec31e5ed6d78a9aa93c2527a2d26" id="tgt139" class="tgtSentence">Tarea 2 (para el perfil SCEP únicamente): configurar los requisitos previos en el servidor NDES</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="1d1a0de5dbaf576b7fb1d3c1fa53960a" id="tgt140" class="tgtSentence">En esta tarea tendrá que:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="77adffb303f17e4aa577d942c1d97e9a" id="tgt141" class="tgtSentence">Agregar NDES a un servidor con Windows Server y configurar IIS para que admita NDES</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="6e1c5ff83614dcd2877b4caf07a40518" id="tgt142" class="tgtSentence">Agregar la cuenta de servicio NDES al grupo IIS_IUSRS</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="24bcdf96b9336781b912f5f996eebb8a" id="tgt143" class="tgtSentence">Establecer el SPN para la cuenta de servicio NDES</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="1cce14a8e70988a3d8ac0bf0269e8d6c" id="tgt144" class="tgtSentence">Para configurar los requisitos previos para el servidor NDES</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="f02093136bffa980690ab1df11bbcb0a" id="tgt145" class="tgtSentence">En el servidor que hospedará NDES, debe iniciar sesión como <embeddedLabel>Administrador de la empresa</embeddedLabel> y, luego, usar el <externalLink><linkText>Asistente para agregar roles y características</linkText><linkUri>https://technet.microsoft.com/library/hh831809.aspx</linkUri></externalLink> para instalar NDES:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="32f890ff57d30e6074a0ec2127700f39" id="tgt146" class="tgtSentence">En el asistente, seleccione <ui>Servicios de certificados de Active Directory</ui> para obtener acceso a los servicios de rol de AD CS.</caps:sentence>
                            <caps:sentence sentenceid="e397ae5004e76a0a4a6e45a8f91313c8" id="tgt147" class="tgtSentence"> Seleccione el <ui>Servicio de inscripción de dispositivos de red</ui>, desactive <ui>Entidad de certificación</ui> y complete el asistente.</caps:sentence>
                          </para>
                          <alert class="tip">
                            <para>
                              <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt148" class="tgtSentence">En la página <ui>Progreso de la instalación</ui> del asistente, no haga clic en <ui>Cerrar</ui>.</caps:sentence>
                              <caps:sentence sentenceid="2cb4c07c7fa5721358be76f36535b78e" id="tgt149" class="tgtSentence"> En su lugar, haga clic en el vínculo para <ui>Configurar Servicios de certificados de Active Directory en el servidor de destino</ui>.</caps:sentence>
                              <caps:sentence sentenceid="f7279eec1c07b17b4dab2a2c14c9dd9b" id="tgt150" class="tgtSentence"> Se abrirá el asistente para <ui>Configuración de AD CS</ui> que se usa en la siguiente tarea.</caps:sentence>
                              <caps:sentence sentenceid="64eca550349d010e953ad4767dc45e2d" id="tgt151" class="tgtSentence"> Una vez abierta la configuración de AD CS, puede cerrar al Asistente para agregar roles y características.</caps:sentence>
                            </para>
                          </alert>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="7fcaae039c059ee42899a3d48dee1240" id="tgt152" class="tgtSentence">Cuando NDES se agrega al servidor, el asistente instala también IIS.</caps:sentence>
                            <caps:sentence sentenceid="f8de239cf4e041008662a2d5f4c6072f" id="tgt153" class="tgtSentence"> Asegúrese de que IIS tenga las siguientes configuraciones:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="c30787c07468ff7428148bc7a038edb4" id="tgt154" class="tgtSentence">
                                  <ui>Servidor web</ui> &gt; <ui>Seguridad</ui> &gt; <ui>Filtrado de solicitudes</ui></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="c30787c07468ff7428148bc7a038edb4" id="tgt155" class="tgtSentence">
                                  <ui>Servidor web</ui> &gt; <ui>Desarrollo de aplicaciones</ui> &gt; <ui>ASP.NET 3.5</ui>.</caps:sentence>
                                <caps:sentence sentenceid="483497dc1df873a44ab37fb1f9bd4c35" id="tgt156" class="tgtSentence"> Al instalar ASP.NET 3.5, se instalará .NET Framework 3.5.</caps:sentence>
                                <caps:sentence sentenceid="3feb5d338f73c1465b49320cec4e39eb" id="tgt157" class="tgtSentence"> Al instalar .NET Framework 3.5, se instala tanto la característica básica <ui>.NET Framework 3.5</ui> como la característica <ui>Activación HTTP</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="c30787c07468ff7428148bc7a038edb4" id="tgt158" class="tgtSentence">
                                  <ui>Servidor web</ui> &gt; <ui>Desarrollo de aplicaciones</ui> &gt; <ui>ASP.NET 4.5</ui>.</caps:sentence>
                                <caps:sentence sentenceid="86faafe3fb137d32863e5b8b8b0ceb12" id="tgt159" class="tgtSentence"> Al instalar ASP.NET 4,5 se instalará .NET Framework 4,5.</caps:sentence>
                                <caps:sentence sentenceid="f9cda9497b94ef5229ad0732fb5bea57" id="tgt160" class="tgtSentence"> Al instalar .NET Framework 4.5, se instalan la característica básica <ui>.NET Framework 4.5</ui>, la característica <ui>ASP.NET 4.5</ui> y la característica <ui>Servicios WCF</ui> &gt; <ui>Activación HTTP</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="c30787c07468ff7428148bc7a038edb4" id="tgt161" class="tgtSentence">
                                  <embeddedLabel>Herramientas de administración</embeddedLabel> &gt; <embeddedLabel>Compatibilidad con la administración de IIS 6</embeddedLabel> &gt; <ui>Compatibilidad con la metabase de IIS</ui></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="c30787c07468ff7428148bc7a038edb4" id="tgt162" class="tgtSentence">
                                  <embeddedLabel>Herramientas de administración</embeddedLabel> &gt; <embeddedLabel>Compatibilidad con la administración de IIS 6</embeddedLabel> &gt; <ui>Compatibilidad con WMI de IIS 6</ui></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="4d0896fd09ff226b1f74256aa251c2b5" id="tgt163" class="tgtSentence">En el servidor, agregue la cuenta de servicio NDES como miembro del grupo <ui>IIS_IUSR</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="06135bd9388d3f4bc571fbac77603c4f" id="tgt164" class="tgtSentence">Ejecute el siguiente comando para establecer el SPN de la cuenta de servicio NDES:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <userInput>
                              <caps:sentence sentenceid="46646bdd23fd08255c73378f5ab35025" id="tgt165" class="tgtSentence">setspn -s http/&lt;nombre DNS del servidor NDES&gt; &lt;nombre de dominio&gt;\&lt;nombre de la cuenta de servicio NDES&gt;</caps:sentence>
                            </userInput>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="02cdde6ab94d790d41fd67483e9dfd70" id="tgt166" class="tgtSentence">Por ejemplo, si el servidor NDES se denomina <embeddedLabel>Server01</embeddedLabel>, su dominio es <embeddedLabel>Contoso.com</embeddedLabel> y la cuenta de servicio es <embeddedLabel>NDESService</embeddedLabel>, use:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <userInput>
                              <caps:sentence sentenceid="45819a59d06428f128a365bda986063a" id="tgt167" class="tgtSentence">setspn –s http/Server01.contoso.com contoso\NDESService</caps:sentence>
                            </userInput>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_ConfigOnPremTask3">
            <title>
              <caps:sentence sentenceid="13f04446b56033def2723c90da2a03f0" id="tgt168" class="tgtSentence">Tarea 3 (para el perfil SCEP únicamente): configurar NDES para su uso con <token>wit_nextref</token></caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="1d1a0de5dbaf576b7fb1d3c1fa53960a" id="tgt169" class="tgtSentence">En esta tarea tendrá que:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2dde94c1a421e4b15b8f50dc792d1035" id="tgt170" class="tgtSentence">Configurar NDES para su uso con la CA emisora</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="143f201f0e786f6b253b6d36af048041" id="tgt171" class="tgtSentence">Enlazar el certificado de autenticación (SSL) de servidor en IIS</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e2978d7df0a3d7e3dc284b8f1bf0f798" id="tgt172" class="tgtSentence">Configurar el filtrado de solicitudes en IIS</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="f72b4d5fd6e69421139001282185c79e" id="tgt173" class="tgtSentence">Para configurar NDES para su uso con <token>wit_nextref</token></caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="000a0d1bb6d9b71bea032279740d7e4b" id="tgt174" class="tgtSentence">En el servidor NDES, abra el asistente para Configuración de AD CS y realice las siguientes configuraciones.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence sentenceid="a6e8b070b8b0fb01c77559e7195382ef" id="tgt175" class="tgtSentence">Si hizo clic en el vínculo de la tarea anterior, este asistente ya está abierto.</caps:sentence>
                          <caps:sentence sentenceid="a0e189d702012e428e6350cc9cc546e5" id="tgt176" class="tgtSentence"> De lo contrario, abra el Administrador del servidor para obtener acceso a la configuración posterior a la implementación de Servicios de certificados de Active Directory.</caps:sentence>
                        </para>
                      </alert>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt177" class="tgtSentence">En la página <ui>Servicios de rol</ui>, seleccione el <ui>Servicio de inscripción de dispositivos de red</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt178" class="tgtSentence">En la página <ui>Cuenta de servicio para NDES</ui>, especifique la cuenta de servicio NDES.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt179" class="tgtSentence">En la página <ui>CA para NDES</ui>, haga clic en <ui>Seleccionar</ui> y seleccione la CA emisora en donde configuró la plantilla de certificado.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt180" class="tgtSentence">En la página <ui>Criptografía para NDES</ui>, establezca la longitud de clave que satisfaga los requisitos de su empresa.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt181" class="tgtSentence">En la página <ui>Confirmación</ui>, haga clic en <ui>Configurar</ui> para completar el asistente.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="54cc6ffe7123665096d60615be952282" id="tgt182" class="tgtSentence">Una vez finalizado el asistente, edite la siguiente clave del registro en el servidor NDES:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="2c9996e5b9677b8ded94d141fbe0646b" id="tgt183" class="tgtSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Cryptography\MSCEP\</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="7be60f8ff30cbafdc7c5b2d5ee2b4d28" id="tgt184" class="tgtSentence">Para editar esta clave, identifique el <ui>Propósito</ui> de las plantillas de certificado disponible en la pestaña <ui>Control de solicitudes</ui> y, a continuación, modifique la entrada correspondiente del registro reemplazando los datos existentes por el nombre de la plantilla de certificado (no el nombre para mostrar de la plantilla) que especificó en la tarea 1.</caps:sentence>
                        <caps:sentence sentenceid="5c25449610a06431ac461f63a61bed46" id="tgt185" class="tgtSentence"> La tabla siguiente asigna el propósito de la plantilla de certificado a los valores del registro:</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="411554943626ce2f4063c289ac09fe2b" id="tgt186" class="tgtSentence">Plantilla de certificado Propósito (en la pestaña Tratamiento de la solicitud)</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="561c4c688092b4644a4f5f1d67340351" id="tgt187" class="tgtSentence">Valor del registro que se va a editar</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="7582226272b4dc6873d3f498ee0a18ee" id="tgt188" class="tgtSentence">Valor que se ve en la consola de administración de <token>wit_nextref</token> para el perfil de SCEP </caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="ac201fd270c3b96beab24f2829780ab2" id="tgt189" class="tgtSentence">Firma</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="b05a523008b62e8a5438f96edca4a45e" id="tgt190" class="tgtSentence">SignatureTemplate</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="8003c0303b4fa36d8f18c007d0daa59f" id="tgt191" class="tgtSentence">Firma digital</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="5bdf74912a51c34815f11e9a3d20b609" id="tgt192" class="tgtSentence">Cifrado</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="89e18473fed3ccef3d1a4ce0fd1dba74" id="tgt193" class="tgtSentence">EncryptionTemplate</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="4513a77827dfd1cc74359eaf154c19f3" id="tgt194" class="tgtSentence">Cifrado de clave</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="7de7a5b0f88eac6a8015094b21fb5955" id="tgt195" class="tgtSentence">Firma y cifrado</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="832ef88e6e66290d409e1b0033b8072e" id="tgt196" class="tgtSentence">GeneralPurposeTemplate</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="4513a77827dfd1cc74359eaf154c19f3" id="tgt197" class="tgtSentence">Cifrado de clave</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="8003c0303b4fa36d8f18c007d0daa59f" id="tgt198" class="tgtSentence">Firma digital</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <para>
                        <caps:sentence sentenceid="7110f29cbbb02a14e694c251a00e1981" id="tgt199" class="tgtSentence">Por ejemplo, si el propósito de la plantilla de certificado es <ui>Cifrado</ui>, edite el valor <ui>EncryptionTemplate</ui> para que sea el nombre de la plantilla de certificado.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="eeb9d4e9a8b8b23d5870f20337048e18" id="tgt200" class="tgtSentence">Después de editar el registro, ejecute <userInput>iisreset</userInput> en el servidor para forzar al servidor a recoger los cambios recientes de configuración.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="ac691e42c0d0e1191e39769fdcc5e3ae" id="tgt201" class="tgtSentence">Para instalar y enlazar certificados en el servidor NDES</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="00376b168a99e6bf5c8ee513c32f1c34" id="tgt202" class="tgtSentence">En el servidor NDES, solicite e instale un certificado de <embeddedLabel>autenticación de servidor</embeddedLabel> de la CA interna o de una CA pública.</caps:sentence>
                        <caps:sentence sentenceid="0368cbf4809f2d0c721da56d591dabc7" id="tgt203" class="tgtSentence"> Este certificado SSL se enlazará luego en IIS.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence sentenceid="0bb21051fcfaeb2514b2a0729c8c20e4" id="tgt204" class="tgtSentence">Después de enlazar el certificado SSL en IIS, también debe instalar un certificado de autenticación del cliente.</caps:sentence>
                          <caps:sentence sentenceid="fe39ef07cc086f4111c220b9558405db" id="tgt205" class="tgtSentence"> Este certificado puede estar emitido por una CA de confianza para el servidor NDES.</caps:sentence>
                          <caps:sentence sentenceid="008dcb6cc2905a9a51e559576ae1a601" id="tgt206" class="tgtSentence"> Aunque no es un procedimiento recomendado, puede usar el mismo certificado para la autenticación de servidor y del cliente, siempre y cuando el certificado tenga dos usos mejorados de clave (EKU).</caps:sentence>
                          <caps:sentence sentenceid="e152f6d53d977d9e3db0d8a9f1d492eb" id="tgt207" class="tgtSentence"> Revise los siguientes pasos para obtener información sobre estos certificados de autenticación.</caps:sentence>
                        </para>
                      </alert>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="3f67682c0a501e823a68a4831668da54" id="tgt208" class="tgtSentence">Después de obtener el certificado de autenticación de servidor, abra el <ui>Administrador de IIS</ui>, seleccione el <ui>Sitio web predeterminado</ui> en el panel <ui>Conexiones</ui> y haga clic en <ui>Enlaces</ui> en el panel <ui>Acciones</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt209" class="tgtSentence">Haga clic en <ui>Agregar</ui>, establezca <ui>Tipo</ui> en <ui>https</ui> y compruebe que el puerto sea el <ui>443</ui>.</caps:sentence>
                            <caps:sentence sentenceid="83e2007b0c6b8f54dfdc0cfd11d29d52" id="tgt210" class="tgtSentence"> (Solo se admite el puerto 443 para <token>wit_nextref</token> independiente).</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="62fd3f87581663e4371e40eb51d66e76" id="tgt211" class="tgtSentence">En el caso de <ui>Certificado SSL</ui>, especifique el certificado de autenticación de servidor.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence sentenceid="7d87767cfa4744de86b56a4a3120fb44" id="tgt212" class="tgtSentence">Si el servidor NDES usa tanto un nombre externo como interno para una única dirección de red, el certificado de autenticación de servidor debe tener un <ui>Nombre del firmante</ui> con un nombre de servidor público externo y un <ui>Nombre alternativo del firmante</ui> que incluya el nombre del servidor interno.</caps:sentence>
                            </para>
                          </alert>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="00376b168a99e6bf5c8ee513c32f1c34" id="tgt213" class="tgtSentence">En el servidor NDES, solicite e instale un certificado de <embeddedLabel>autenticación del cliente</embeddedLabel> de la CA interna o de una entidad de certificación pública.</caps:sentence>
                        <caps:sentence sentenceid="5b670f9dff9a1508a739ca1d138e7b04" id="tgt214" class="tgtSentence"> Este puede ser el mismo certificado que el certificado de autenticación de servidor si dicho certificado tiene ambas capacidades.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="ab1a17a71ea1fdb0dc15bce3a5508fa5" id="tgt215" class="tgtSentence">El certificado de autenticación del cliente debe tener las siguientes propiedades:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d60a703b059e79e30f43e99e406e8857" id="tgt216" class="tgtSentence">
                              <ui>Uso mejorado de clave</ui>: debe incluir <ui>Autenticación del cliente</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="329ca25049828faa680377f66b46bd8c" id="tgt217" class="tgtSentence">
                              <ui>Nombre del firmante</ui>: debe ser igual al nombre DNS del servidor donde se instala el certificado (el servidor NDES).</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="a57c88dd2c0f200cb5580f512a3d4750" id="tgt218" class="tgtSentence">Para configurar el filtrado de solicitudes de IIS</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ad5cf20b6e6d8be7c96a26589a6b5fc3" id="tgt219" class="tgtSentence">En el servidor NDES, abra el <ui>Administrador de IIS</ui>, seleccione el <ui>Sitio web predeterminado</ui> en el panel <ui>Conexiones</ui> y abra <ui>Filtrado de solicitudes</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt220" class="tgtSentence">Haga clic en <ui>Modificar configuración de característica</ui> y configure lo siguiente:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="fcacca1424f339192c748b8e531c8ec3" id="tgt221" class="tgtSentence">
                              <ui>Cadena de consulta (Bytes)</ui> = <userInput>65534</userInput></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="fcacca1424f339192c748b8e531c8ec3" id="tgt222" class="tgtSentence">
                              <ui>Longitud máxima de dirección URL (Bytes)</ui> = <userInput>65534</userInput></caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="e0731327a8cfd305b2e7c1df40bfa5da" id="tgt223" class="tgtSentence">Revise la siguiente clave del registro:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="e3797b436fe1ec49facd7873cd7a3cca" id="tgt224" class="tgtSentence">HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\HTTP\Parameters</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="1fcc2d014f1015d86ad8a9b8aa7597d7" id="tgt225" class="tgtSentence">Asegúrese de que los siguientes valores se establezcan como entradas DWORD:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="bf7ed2d215c357ed9f7cee9fac246ab9" id="tgt226" class="tgtSentence">Nombre: <ui>MaxFieldLength</ui>, con un valor decimal de <userInput>65534</userInput></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="bf7ed2d215c357ed9f7cee9fac246ab9" id="tgt227" class="tgtSentence">Nombre: <ui>MaxRequestBytes</ui>, con un valor decimal de <userInput>65534</userInput></caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9b98142051eab349467512ff27082850" id="tgt228" class="tgtSentence">Reinicie el servidor de NDES.</caps:sentence>
                        <caps:sentence sentenceid="830a01c2c703dcb943d9729ed4906329" id="tgt229" class="tgtSentence"> El servidor está ya preparado para admitir el conector certificado.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_ConfigOnPremTask4">
            <title>
              <caps:sentence sentenceid="a8fa74bddc30b4726a3edf2d88f1f806" id="tgt230" class="tgtSentence">Tarea 4: habilitar, instalar y configurar el conector de certificado de Intune (para certificados SCEP y .PFX)</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="1d1a0de5dbaf576b7fb1d3c1fa53960a" id="tgt231" class="tgtSentence">En esta tarea tendrá que:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="da416ee822b1e245ba6ca1659b51b197" id="tgt232" class="tgtSentence">Habilitar la compatibilidad de NDES en <token>wit_nextref</token></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="63771f072fcd2de3a50a8d5b6b40a539" id="tgt233" class="tgtSentence">Descargar, instalar y configurar el conector de certificado en el servidor NDES</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="fb65631e68ef434bb154b3c232472351" id="tgt234" class="tgtSentence">Para habilitar la compatibilidad del conector de certificado</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt235" class="tgtSentence">Abra la <externalLink><linkText>Consola de administración de Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Administración</ui> &gt; <ui>Conector de certificado</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt236" class="tgtSentence">Haga clic en <ui>Configurar conector de certificado local</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt237" class="tgtSentence">Seleccione <ui>Habilitar conector de certificado</ui> y, a continuación, haga clic en <ui>Aceptar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="4118faae2320b79489ef2208bad1c1a8" id="tgt238" class="tgtSentence">Para descargar, instalar y configurar el conector de certificado</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt239" class="tgtSentence">Abra la <externalLink><linkText>Consola de administración de Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink> y, a continuación, haga clic en <ui>Administrador</ui> &gt; <ui>Administración de dispositivos móviles</ui> &gt; <ui>Conector de certificado</ui> &gt; <ui>Descargar conector de certificado</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="88b77d43988c4a935002301cfd10689a" id="tgt240" class="tgtSentence">Una vez finalizada la descarga, ejecute el instalador descargado (<embeddedLabel>ndesconnectorssetup.exe</embeddedLabel>):</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="141daadbd2805764df6369823175af42" id="tgt241" class="tgtSentence">Para los certificados .PFX, ejecute el instalador en el equipo que puede conectarse con la entidad de certificación.</caps:sentence>
                            <caps:sentence sentenceid="382ff048d3609489f1b8414bdec2a766" id="tgt242" class="tgtSentence"> Elija la opción de distribución .PFX y haga clic en Instalar.</caps:sentence>
                            <caps:sentence sentenceid="0ddbd1e7a0e7898642f75de198110edb" id="tgt243" class="tgtSentence"> Cuando haya finalizado la instalación, cree un perfil de certificado.</caps:sentence> </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="c478122f9132c2dfdd7aa8c077846190" id="tgt244" class="tgtSentence">Para los certificados SCEP, ejecute el instalador en un servidor de Windows Server 2012 R2</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="e7b56d0f43ed18c07ed813ec45d70baf" id="tgt245" class="tgtSentence">  Para la opción de SCEP, el instalador también instala el módulo de directivas para NDES y el servicio web de CRP.</caps:sentence>
                        <caps:sentence sentenceid="31f443dad5df90913724dfb792d7bfb1" id="tgt246" class="tgtSentence"> (El servicio web de CRP, CertificateRegistrationSvc, se ejecuta como una aplicación en IIS).</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence sentenceid="d5c7ff7eda863e6947bd3212a9bb5568" id="tgt247" class="tgtSentence">Cuando instala NDES para <token>wit_nextref</token> independiente, el servicio de CRP se instala automáticamente con el conector de certificado.</caps:sentence>
                          <caps:sentence sentenceid="415a7e7eee5de12594f9f162a433643d" id="tgt248" class="tgtSentence"> Al usar <token>wit_nextref</token> con Configuration Manager, instale el punto de registro del certificado como un rol de sistema de sitio independiente.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="0a6883a18773bf81096e74c2dc2292f0" id="tgt249" class="tgtSentence">Cuando se le solicite el certificado de cliente para el conector de certificado, haga clic en <ui>Seleccionar</ui> y seleccione el certificado de <embeddedLabel>autenticación del cliente</embeddedLabel> instalado en el servidor NDES en la tarea 3.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="3f02854cbcd77e1747f9340e108aefdc" id="tgt250" class="tgtSentence">Después de seleccionar el certificado de autenticación del cliente, volverá a la superficie del <ui>Certificado de cliente para el conector de certificado para Microsoft Intune</ui>.</caps:sentence>
                        <caps:sentence sentenceid="f3e104805772b2dff81a097307c12c1f" id="tgt251" class="tgtSentence"> Aunque no se muestra el certificado seleccionado, haga clic en <ui>Siguiente</ui> para ver las propiedades de dicho certificado.</caps:sentence>
                        <caps:sentence sentenceid="2b5923b0f5544bce7308d091e7b9614e" id="tgt252" class="tgtSentence"> Haga clic en <ui>Siguiente</ui> y, luego, en <ui>Instalar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="e28df4931bf90e8a87b8aea301b26092" id="tgt253" class="tgtSentence">Cuando se complete el asistente, pero antes de cerrarlo, haga clic en <ui>Iniciar la UI del conector de certificado</ui>.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence sentenceid="9f75f24b34d46807aecb04b7c2aebcfd" id="tgt254" class="tgtSentence">Si cierra al asistente antes de iniciar la IU del conector de certificado, puede volver a abrirlo ejecutando el comando siguiente:</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <userInput>
                                <caps:sentence sentenceid="fb4a21fa9243f25a9f6d15e91ab08245" id="tgt255" class="tgtSentence">&lt;install_Path&gt;\NDESConnectorUI\NDESConnectorUI.exe</caps:sentence>
                              </userInput>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt256" class="tgtSentence">En la IU <ui>Conector de certificado</ui>:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt257" class="tgtSentence">Haga clic en <ui>Iniciar sesión</ui> y escriba sus credenciales de administrador de servicio de <token>wit_nextref</token> o las credenciales de un administrador de inquilinos con permiso de administración global.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="c1683ef7ca970b4aea0a1b8e9a98795c" id="tgt258" class="tgtSentence">Si su organización usa un servidor proxy y el proxy es necesario para que el servidor NDES obtenga acceso a Internet, haga clic en <ui>Usar servidor proxy</ui> y proporcione el nombre del servidor proxy, el puerto y las credenciales de la cuenta para conectarse.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="7486589d03c162162a7c4e75345fcca4" id="tgt259" class="tgtSentence">Seleccione la pestaña <ui>Avanzadas</ui>, proporcione las credenciales de una cuenta que tenga el permiso <ui>Emitir y administrar certificados</ui> en la CA emisora y haga clic en <ui>Aplicar</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="b11900368a0737cd9c2cce2398661f65" id="tgt260" class="tgtSentence">Ahora puede cerrar la IU del conector de certificado.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="f1adde3319ade645221c1ca5f866079c" id="tgt261" class="tgtSentence">Abra un símbolo del sistema, escriba <userInput>services.msc</userInput> y presione <ui>Entrar</ui>. Haga clic con el botón secundario en <ui>Servicio de conector de certificado</ui> y haga clic en <ui>Reiniciar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence sentenceid="15cdea95df57cbfc2ce072a54c6ba537" id="tgt262" class="tgtSentence">Para validar que el servicio se ejecuta, abra un explorador y escriba la siguiente dirección URL, que debe devolver un error <ui>403</ui>:</caps:sentence>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <userInput>
                            <caps:sentence sentenceid="9098432db026f83a079f1e3fe966d8db" id="tgt263" class="tgtSentence">http://&lt;FQDN_of_your_NDES_server&gt;/certsrv/mscep/mscep.dll</caps:sentence>
                          </userInput>
                        </para>
                      </listItem>
                    </list>
                    <para>
                      <caps:sentence sentenceid="90ffefb0bd07efb2b84d736aaac56442" id="tgt264" class="tgtSentence">Ya está listo para configurar perfiles de certificado.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_ConfigProfiles">
        <title>
          <caps:sentence sentenceid="dc5b8c2781701e6c41c0895bd3cf3477" id="tgt265" class="tgtSentence">Configurar perfiles de certificado</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="c9f3af6880a840d3b45fd80db0ddfddb" id="tgt266" class="tgtSentence">Después de configurar la infraestructura y los certificados, puede configurar perfiles de certificado:</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e7f925ac38bd3f04dba195a53c48a7a6" id="tgt267" class="tgtSentence">
              <embeddedLabel>Tarea 1</embeddedLabel>: exportar el certificado de CA raíz de confianza <br /><embeddedLabel>Tarea 2</embeddedLabel>: crear perfiles de certificado de CA de confianza <br /><embeddedLabel>Tarea 3</embeddedLabel>: ya sea: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="1811d1a2416fcf03e716b00448cdafbe" id="tgt268" class="tgtSentence">Crear perfiles de certificado SCEP</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="035d56cae4d5a260d1a7b89b5b57dbe8" id="tgt269" class="tgtSentence">Crear perfiles de certificado .PFX</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="BKMK_ConfigExportRootCA">
            <title>
              <caps:sentence sentenceid="295fb4aa03ffa74b8c7546398e069c56" id="tgt270" class="tgtSentence">Tarea 1: exportar el certificado de CA raíz de confianza </caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a6852ed9eacdea3caa94851f09704aa5" id="tgt271" class="tgtSentence">Exporte el certificado de CA raíz de confianza como archivo <ui>.cer</ui> archivo desde la CA emisora o desde cualquier dispositivo que confíe en la CA emisora.</caps:sentence>
                <caps:sentence sentenceid="76c9f26300b18adb66c799e188421396" id="tgt272" class="tgtSentence"> No exporte la clave privada.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="d4cb6b75d38864a75e3a4a0a4f4882f2" id="tgt273" class="tgtSentence">Volverá a importar este certificado al configurar un perfil de certificado de CA de confianza.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_ConfigRootCA">
            <title>
              <caps:sentence sentenceid="08c8effa7c5311cd2f48e9cb60cd1e81" id="tgt274" class="tgtSentence">Tarea 2: crear perfiles de certificado de CA de confianza</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="53951e8d80ed2c955dba4fd1f055e2f6" id="tgt275" class="tgtSentence">Debe crear un perfil de <ui>Certificado de CA de confianza</ui> para poder crear un perfil de <ui>configuración del Protocolo de inscripción de certificados simple</ui>.</caps:sentence>
                <caps:sentence sentenceid="7c0224b5f0e75f112d473d913155593e" id="tgt276" class="tgtSentence"> Ambos perfiles son necesarios para cada plataforma de dispositivos móviles.</caps:sentence>
              </para>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="c7f8866f682127bd118f1ccb43f59b5d" id="tgt277" class="tgtSentence">Para crear un perfil de certificado de confianza</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt278" class="tgtSentence">En la <externalLink><linkText>consola de administración de Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Agregar directiva</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="88138dda55a4d1c883b810b4940a947e" id="tgt279" class="tgtSentence">Configure uno de los siguientes tipos de directivas:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="914b669931e47037d177a3a1325436fb" id="tgt280" class="tgtSentence">Android &gt; Perfil de certificado de confianza (Android 4 y versiones posteriores)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="96fb579cc7879a65ac57b5ff4788a02c" id="tgt281" class="tgtSentence">iOS &gt; Perfil de certificado de confianza (iOS 5 y versiones posteriores)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="f5f881d41a28871a00b474290f251ada" id="tgt282" class="tgtSentence">Dispositivos Windows inscritos y Windows Phone &gt; Perfil de certificado de confianza (Windows 8.1 y versiones posteriores)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="fda5b094128790f99add055b05078063" id="tgt283" class="tgtSentence">Dispositivos Windows inscritos y Windows Phone &gt; Perfil de certificado de confianza (Windows Phone 8.1 y versiones posteriores)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="d93a4efaaccfdf196a20e05159bfa91f" id="tgt284" class="tgtSentence">Más información: <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="a6a88d1625e53f5ea4b93393b3d1ac9c" id="tgt285" class="tgtSentence">Use la siguiente información para configurar las opciones del perfil de certificado de confianza para Android, iOS, Windows 8.1 o Windows Phone 8.1:</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt286" class="tgtSentence">Nombre de la configuración</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="34a6e5d64ade17ef4e51612c50dd72f5" id="tgt287" class="tgtSentence">Plataforma</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt288" class="tgtSentence">Más información</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt289" class="tgtSentence">Nombre</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt290" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="4dfcea16279f1da2f0f8948e022cf61b" id="tgt291" class="tgtSentence">Proporcione un nombre descriptivo para el perfil de certificado.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt292" class="tgtSentence">Descripción</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt293" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="5aeae73b6d0ed40fef95291425c6f96c" id="tgt294" class="tgtSentence">Proporcione una descripción opcional para el perfil de certificado.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="b3d2f2364ce3a4c005298745bfcdd35b" id="tgt295" class="tgtSentence">Archivo de certificado</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="a181a603769c1f98ad927e7367c7aa51" id="tgt296" class="tgtSentence">Todos</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt297" class="tgtSentence">Haga clic en <ui>Importar</ui> y seleccione el certificado de CA raíz de confianza (<ui>.cer</ui>) que exportó desde la CA emisora.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="ee56d7df7055311ccf018a0b6173fced" id="tgt298" class="tgtSentence">Almacén de destino</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="bff8df2abce94b1dbe9b4fd58f2281b9" id="tgt299" class="tgtSentence">Windows 8.1</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="d38cc5ecec422c849c88762b90af136e" id="tgt300" class="tgtSentence">Para los dispositivos que tienen más de un almacén de certificados, seleccione dónde quiere almacenar el certificado.</caps:sentence>
                                <caps:sentence sentenceid="0dfd6b4955b8582f0c47c2dbb9edde1c" id="tgt301" class="tgtSentence"> Seleccione:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <ui>
                                      <caps:sentence sentenceid="caa23e246b703b54ab4c4a62e951f837" id="tgt302" class="tgtSentence">Almacén de certificados del equipo: raíz</caps:sentence>
                                    </ui>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <ui>
                                      <caps:sentence sentenceid="6b4f4f67ea3161855eb3b3aa27e7e57d" id="tgt303" class="tgtSentence">Almacén de certificados de equipo: intermedio</caps:sentence>
                                    </ui>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <ui>
                                      <caps:sentence sentenceid="ab238af47883e53da5fba68181b9cdb5" id="tgt304" class="tgtSentence">Almacén de certificados de usuario: intermedio</caps:sentence>
                                    </ui>
                                  </para>
                                </listItem>
                              </list>
                              <para>
                                <caps:sentence sentenceid="b8c421c54f9b55d49e968be7137c1f32" id="tgt305" class="tgtSentence">Para los dispositivos que solo tienen un almacén, este valor se omite.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt306" class="tgtSentence">Cuando haya terminado haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt307" class="tgtSentence">La nueva directiva se muestra en el área de trabajo <ui>Directiva</ui> y ahora puede implementarse.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
          <section address="BKMK_ConfigSCEP">
            <title>
              <caps:sentence sentenceid="f8a7d56893fd7ec51bc6e25fc1d16c10" id="tgt308" class="tgtSentence">Tarea 3: crear perfiles de certificado .PFX o SCEP</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="96139fd79304e9d7642a31f1a9dbadd4" id="tgt309" class="tgtSentence">Después de haber creado un perfil de certificado de CA de confianza, cree perfiles de certificado SCEP o .PFX para cada plataforma que desee usar.</caps:sentence>
                <caps:sentence sentenceid="9b4e22fc51de879af5b447e2498bd847" id="tgt310" class="tgtSentence"> Al crear un perfil de certificado SCEP, debe especificarse un perfil de certificado de CA de confianza para esa misma plataforma.</caps:sentence>
                <caps:sentence sentenceid="f050e84ed1d20c9d26a71507b5fca21b" id="tgt311" class="tgtSentence"> Esto vincula los dos perfiles de certificado, aunque aún debe implementar cada perfil por separado.</caps:sentence>
              </para>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="58ea7469246f11a860a6d4a4207e38b6" id="tgt312" class="tgtSentence">Para crear un perfil de certificado SCEP</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt313" class="tgtSentence">Abra la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Agregar directiva</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="88138dda55a4d1c883b810b4940a947e" id="tgt314" class="tgtSentence">Configure uno de los siguientes tipos de directivas:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="80705b274edd1c06fc82e91471e7406b" id="tgt315" class="tgtSentence">Android &gt; Perfil de certificado SCEP (Android 4 y versiones posteriores)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="840abcc1030d902e1846d5029f5e796a" id="tgt316" class="tgtSentence">iOS &gt; Perfil de certificado SCEP (iOS 5 y versiones posteriores)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="1dea91254d0cdffe762aca765daf0a58" id="tgt317" class="tgtSentence">Dispositivos Windows inscritos y Windows Phone &gt; Perfil de certificado SCEP (Windows 8.1 y versiones posteriores)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="9b23cc837e4e0f52f2d1ae4147548bf9" id="tgt318" class="tgtSentence">Dispositivos Windows inscritos y Windows Phone &gt; Perfil de certificado SCEP (Windows Phone 8.1 y versiones posteriores)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="d93a4efaaccfdf196a20e05159bfa91f" id="tgt319" class="tgtSentence">Más información: <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="88561d12fd9fb7202cc7c28246c13424" id="tgt320" class="tgtSentence">Use la siguiente información para configurar las opciones del perfil de certificado SCEP para Android, iOS, Windows 8.1 o Windows Phone 8.1:</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt321" class="tgtSentence">Nombre de la configuración</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="34a6e5d64ade17ef4e51612c50dd72f5" id="tgt322" class="tgtSentence">Plataforma</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt323" class="tgtSentence">Más información</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <embeddedLabel>
                                  <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt324" class="tgtSentence">Nombre</caps:sentence>
                                </embeddedLabel>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt325" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="4dfcea16279f1da2f0f8948e022cf61b" id="tgt326" class="tgtSentence">Proporcione un nombre descriptivo para el perfil de certificado.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <embeddedLabel>
                                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt327" class="tgtSentence">Descripción</caps:sentence>
                                </embeddedLabel>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt328" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="5aeae73b6d0ed40fef95291425c6f96c" id="tgt329" class="tgtSentence">Proporcione una descripción opcional para el perfil de certificado.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="1e9fcef79c3a69eee8549c3bc66e9a57" id="tgt330" class="tgtSentence">Umbral de renovación (%)</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt331" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="62803e4ca2f95b8a2f30c7855702fc99" id="tgt332" class="tgtSentence">Especifique qué porcentaje de la duración del certificado tiene que quedar para que el dispositivo solicite la renovación del certificado.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="67bf290f2ccbd093363cf5c0540b6d7e" id="tgt333" class="tgtSentence">Proveedor de almacenamiento de claves (KSP)</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt334" class="tgtSentence">Android <br />Windows 8.1 <br />Windows Phone 8.1</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="84d88367aad9a532a1a73b1b41aa97b5" id="tgt335" class="tgtSentence">Especifique donde se almacenará la clave del certificado.</caps:sentence>
                                <caps:sentence sentenceid="2e918a867032bf712862815ff3ab544c" id="tgt336" class="tgtSentence"> Elija una de las siguientes opciones:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="e457b95fe64e883c741384b3dc8f07d2" id="tgt337" class="tgtSentence">
                                      <ui>Instalar en Módulo de plataforma segura (TPM) si está presente</ui>: instala la clave en el TPM.</caps:sentence>
                                    <caps:sentence sentenceid="3cca91a7c23f49356717ef9e917263eb" id="tgt338" class="tgtSentence"> Si el TPM no está presente, la clave se instalará en el proveedor de almacenamiento de la clave de software.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="e457b95fe64e883c741384b3dc8f07d2" id="tgt339" class="tgtSentence">
                                      <ui>Instalar en Módulo de plataforma segura (TPM); de lo contrario, generar error</ui>: instala la clave en el TPM.</caps:sentence>
                                    <caps:sentence sentenceid="202440845090a0ada3dd79c6af160287" id="tgt340" class="tgtSentence"> Si el módulo TPM no está presente, se producirá un error en la instalación.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="0d9f1974dc5603a1994735bd62281e7b" id="tgt341" class="tgtSentence">
                                      <ui>Instalar en el proveedor de almacenamiento de claves de software</ui>: instala la clave en el proveedor de almacenamiento de la clave de software.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="0ef3f7daa9663b1f175629a63ab129e8" id="tgt342" class="tgtSentence">Dirección URL del servidor de SCEP</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt343" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="28b365d672b35a90c3cd3152a5e6fc13" id="tgt344" class="tgtSentence">Escriba una dirección URL (con el prefijo <userInput>http://</userInput> o <userInput>https://</userInput>), haga clic en <ui>Agregar</ui>; o seleccione una dirección URL y haga clic en <ui>Eliminar</ui>.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="fdc1de3ddc243da7dd3a04dffe9946e9" id="tgt345" class="tgtSentence">Por ejemplo, una dirección URL del servidor SCEP puede tener el aspecto siguiente: <embeddedLabel>https://mdmndes1.contoso.com/certsrv/mscep/mscep.dll</embeddedLabel></caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="0c0764d731687f667f3ae28796a194de" id="tgt346" class="tgtSentence">Cada perfil SCEP admite una sola dirección URL de servidor SCEP.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="b8158a09148604da7ef364bd2806f452" id="tgt347" class="tgtSentence">Formato de nombre del sujeto</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt348" class="tgtSentence">Android <br />Windows 8.1 <br />Windows Phone 8.1</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="760dd53633b3406e94abfac596694292" id="tgt349" class="tgtSentence">En la lista, seleccione cómo <token>wit_nextref</token> crea automáticamente el nombre del firmante en la solicitud de certificado.</caps:sentence>
                                <caps:sentence sentenceid="c4a024ce8ab3d0431f78351883d79b8f" id="tgt350" class="tgtSentence"> Si el certificado es para un usuario, también puede incluir la dirección de correo electrónico del usuario en el nombre del sujeto.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="c4b63b9c877ccbc0a03de768a0d85df0" id="tgt351" class="tgtSentence">Puede seleccionar <ui>Nombre común</ui> o <ui>Nombre común y dirección de correo electrónico</ui>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="4e434010fb482e4e4eb6b03c14a1116b" id="tgt352" class="tgtSentence">Nombre alternativo del sujeto</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt353" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt354" class="tgtSentence">Seleccione <ui>Dirección de correo electrónico</ui>, <ui>Nombre principal de usuario (UPN)</ui> o ambos.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="075671d59de883a4f0d159ebca3b0103" id="tgt355" class="tgtSentence">Período de validez del certificado</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt356" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="292d6c95721cba653c2f57aecbd5cfd0" id="tgt357" class="tgtSentence">Especifique la cantidad de tiempo antes de que expire el certificado.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="f3ef2d1f192c17b03ac308864756bfda" id="tgt358" class="tgtSentence">Uso de claves</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt359" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="18e3f1c4c19acd6c6810b37866a09888" id="tgt360" class="tgtSentence">Especifique las opciones de uso de claves para el certificado.</caps:sentence>
                                <caps:sentence sentenceid="5e44d50d5681f33d4bf2b2bb5faf5643" id="tgt361" class="tgtSentence"> Puede elegir entre las siguientes opciones:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="2b338cb90b19b404fdd3791a94fc6ba4" id="tgt362" class="tgtSentence">
                                      <ui>Firma digital</ui> (SignatureTemplate): úsela para firmar datos digitalmente.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="4fe3850ed5095de1f741805346916cfc" id="tgt363" class="tgtSentence">
                                      <ui>Cifrado de clave</ui> (EncryptionTemplate): úsela para cifrado.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="d7da3bf234c6f44892bed243e723254a" id="tgt364" class="tgtSentence">
                                      <ui>Cifrado de clave y Firma Digital</ui> (GeneralPurposeTemplate): úsela para firmar datos digitalmente y cifrarlos.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="3b640348aca7839d45a4107df124cf6c" id="tgt365" class="tgtSentence">Tamaño de la clave (bits)</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt366" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="7bdedae0e4fa39590ae3f2daa0e160a8" id="tgt367" class="tgtSentence">Seleccione el tamaño de la clave en bits que sea compatible con el dispositivo.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt368" class="tgtSentence">Seleccione <ui>1024</ui> o <ui>2048</ui>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="45600a24d4bc5f8fdfb3cdeb43dd531d" id="tgt369" class="tgtSentence">Algoritmo hash</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt370" class="tgtSentence">Android <br />Windows 8.1 <br />Windows Phone 8.1</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="d1bdb4b7da35839e288260e669da2bee" id="tgt371" class="tgtSentence">Seleccione uno de los tipos de algoritmos hash disponibles para usar con este certificado.</caps:sentence>
                                <caps:sentence sentenceid="2585ae37bc0f800b4fa5a7a0ae8bc742" id="tgt372" class="tgtSentence"> Seleccione el nivel máximo de seguridad que admiten los dispositivos de conexión.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="3d28822ef6b543a688f36f914f7304b4" id="tgt373" class="tgtSentence">Seleccione <ui>SHA-1</ui>, <ui>SHA-2</ui> o ambos.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="e34532d6396890d0b1b93aaf0477a857" id="tgt374" class="tgtSentence">Uso mejorado de clave</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt375" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt376" class="tgtSentence">Haga clic en <ui>Seleccionar</ui> para agregar valores para la finalidad prevista del certificado.</caps:sentence>
                                <caps:sentence sentenceid="22ad99c1092198317cd323fb821e0df4" id="tgt377" class="tgtSentence"> En la mayoría de los casos, el certificado requerirá <ui>Autenticación de cliente</ui> para que el usuario o dispositivo pueda autenticarse en un servidor.</caps:sentence>
                                <caps:sentence sentenceid="9cab23c77503eee5ee463a8a6e70abbf" id="tgt378" class="tgtSentence"> Sin embargo, puede agregar otros usos de clave según sea necesario.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="ee92da0bdb150bae24df474e9ca8a283" id="tgt379" class="tgtSentence">Seleccionar el certificado raíz</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="06f4292f4a1e7942782628cfcec8bc6d" id="tgt380" class="tgtSentence">Todos </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt381" class="tgtSentence">Haga clic en <ui>Seleccionar</ui> para elegir un perfil de certificado de CA raíz que previamente ha configurado e implementado para el usuario o dispositivo.</caps:sentence>
                                <caps:sentence sentenceid="26c248d938e23bd7a310acd562927e69" id="tgt382" class="tgtSentence"> Este certificado de CA debe ser el certificado raíz para la entidad de certificación que emitirá el certificado que va a configurar en este perfil de certificado.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt383" class="tgtSentence">Cuando haya terminado haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt384" class="tgtSentence">La nueva directiva se muestra en el área de trabajo <ui>Directiva</ui> y ahora puede implementarse.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="4cffc9119d9f9b57bcfb47335dd8cc42" id="tgt385" class="tgtSentence">Para crear un perfil de certificado .PFX</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt386" class="tgtSentence">Abra la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Agregar directiva</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="88138dda55a4d1c883b810b4940a947e" id="tgt387" class="tgtSentence">Configure uno de los siguientes tipos de directivas:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="4bc935a9f0b21674ce49da33bbc3f2ad" id="tgt388" class="tgtSentence">Android &gt; Perfil de certificado .PFX (Android 4 y versiones posteriores)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="6f3a590d771233462259e49171cecede" id="tgt389" class="tgtSentence">Dispositivos Windows inscritos y Windows Phone &gt; Perfil de certificado .PFX (Windows 10 y versiones posteriores)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="127a7e4b2d675bbc62a91f8d89ada4bd" id="tgt390" class="tgtSentence">Dispositivos Windows inscritos y Windows Phone &gt; Perfil de certificado .PFX (Windows Phone 10 y versiones posteriores)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="d93a4efaaccfdf196a20e05159bfa91f" id="tgt391" class="tgtSentence">Más información: <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="5673898a6bbf1ec1ca8ff1527b281a44" id="tgt392" class="tgtSentence">Use la siguiente información para configurar las opciones del perfil de certificado .PFX para Android, Windows 10 y Windows Phone 10:</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt393" class="tgtSentence">Nombre de la configuración</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="34a6e5d64ade17ef4e51612c50dd72f5" id="tgt394" class="tgtSentence">Plataforma</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt395" class="tgtSentence">Más información</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <embeddedLabel>
                                  <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt396" class="tgtSentence">Nombre</caps:sentence>
                                </embeddedLabel>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt397" class="tgtSentence">Android <br />Windows 10 <br />Windows Phone 10</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="4dfcea16279f1da2f0f8948e022cf61b" id="tgt398" class="tgtSentence">Proporcione un nombre descriptivo para el perfil de certificado.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <embeddedLabel>
                                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt399" class="tgtSentence">Descripción</caps:sentence>
                                </embeddedLabel>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt400" class="tgtSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="5aeae73b6d0ed40fef95291425c6f96c" id="tgt401" class="tgtSentence">Proporcione una descripción opcional para el perfil de certificado.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="1e9fcef79c3a69eee8549c3bc66e9a57" id="tgt402" class="tgtSentence">Umbral de renovación (%)</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt403" class="tgtSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="62803e4ca2f95b8a2f30c7855702fc99" id="tgt404" class="tgtSentence">Especifique qué porcentaje de la duración del certificado tiene que quedar para que el dispositivo solicite la renovación del certificado.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="32913fa628bfc4d5cdbcc32410461bac" id="tgt405" class="tgtSentence">Entidad de certificación</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt406" class="tgtSentence">Android <br />Windows 10 <br />Windows Phone 10</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="c99e576496724b78bfe18089cad683cb" id="tgt407" class="tgtSentence">Proporcione el FQDN de la entidad de certificación, por ejemplo, <legacyItalic>device.certs.contoso.com</legacyItalic>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="18811cac4da5433e841114540f0ca3e8" id="tgt408" class="tgtSentence">Nombre de la entidad de certificación</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt409" class="tgtSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="8e2366578e73097b464a5734c9b974f2" id="tgt410" class="tgtSentence">Proporcione el nombre de la entidad de certificación, por ejemplo <legacyItalic>device-contoso-CA</legacyItalic>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="5af27f2cab111f64b56338edacf30838" id="tgt411" class="tgtSentence">Nombre de plantilla de certificado</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt412" class="tgtSentence">Android <br />Windows 10 <br />Windows Phone 10</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="f1065b7a17d9b461fa578a72735f038b" id="tgt413" class="tgtSentence">Proporcione el nombre de la plantilla de certificado (no el nombre para mostrar).</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="b8158a09148604da7ef364bd2806f452" id="tgt414" class="tgtSentence">Formato de nombre del sujeto</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt415" class="tgtSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="cbdb5f129367261cb7dec461f0b62864" id="tgt416" class="tgtSentence">Proporcione un formato de nombre de asunto de las opciones proporcionadas:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="3f2b150f808bc3e27a2f440ab2d8a3c6" id="tgt417" class="tgtSentence">Nombre común</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence sentenceid="1ec6fa265d149df441529792bdc7eff5" id="tgt418" class="tgtSentence">Nombre común y dirección de correo electrónico</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="b5b78c3e3afa0d819c3d6d43d8bffd2e" id="tgt419" class="tgtSentence">Nombre alternativo del firmante </caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt420" class="tgtSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="23f7fbb91ec32e29a96ead7199da5fcb" id="tgt421" class="tgtSentence">Elija los nombres alternativos del firmante.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="075671d59de883a4f0d159ebca3b0103" id="tgt422" class="tgtSentence">Período de validez del certificado</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="82e19e371070699d910c556dec4e25ef" id="tgt423" class="tgtSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence sentenceid="292d6c95721cba653c2f57aecbd5cfd0" id="tgt424" class="tgtSentence">Especifique la cantidad de tiempo antes de que expire el certificado.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt425" class="tgtSentence">Cuando haya terminado haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt426" class="tgtSentence">La nueva directiva se muestra en el área de trabajo <ui>Directiva</ui> y ahora puede implementarse.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_Deploy">
        <title>
          <caps:sentence sentenceid="cffe6871fe144239dce236951cc16f85" id="tgt427" class="tgtSentence">Implementar perfiles de certificado</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0fe17c22a6dcbad22e587d23c65b96fc" id="tgt428" class="tgtSentence">Al implementar perfiles de certificado, el archivo de certificado del perfil de certificado de CA de confianza se instala en los dispositivos y el dispositivo usa el perfil de certificado SCEP o .PFX para crear una solicitud de certificado.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b27707eb114ed2e8e9f642921c041c74" id="tgt429" class="tgtSentence">Los perfiles de certificado solo se instalan en dispositivos aplicables en función de la plataforma que use al crear el perfil.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="7a47ecbf0139fdc63c3bf389bf25382a" id="tgt430" class="tgtSentence">Puede implementar perfiles de certificado en recopilaciones de usuarios o en recopilaciones de dispositivos.</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence sentenceid="2a35d093367de004f6c3f33001c64467" id="tgt431" class="tgtSentence">Para permitir que los certificados se publiquen en dispositivos rápidamente después de inscribir el dispositivo, implemente el perfil de certificado en un grupo de usuarios (no en un grupo de dispositivos).</caps:sentence>
                  <caps:sentence sentenceid="d9e39bcb198ba4728737ca8e444cce20" id="tgt432" class="tgtSentence"> Si se implementa en un grupo de dispositivos, debe realizarse un registro de todos los dispositivos antes de que el dispositivo reciba la directiva.</caps:sentence>
                </para>
              </alert>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="63ecd67eb59aed651dc70e2b9ed94276" id="tgt433" class="tgtSentence">Aunque cada perfil se implementa por separado, debe implementarse tanto el perfil de raíz de confianza como el perfil SCEP o .PFX o, de lo contrario, se producirá un error en la directiva de certificado SCEP o .PFX.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="0dea6691e66283f7d71d8ad54f3d0137" id="tgt434" class="tgtSentence">Implemente perfiles de certificado del mismo modo que implementa otra directiva para <token>wit_nextref</token>.</caps:sentence>
            <caps:sentence sentenceid="504a0c4ab23df8243554dc4d0d60d21f" id="tgt435" class="tgtSentence"> Para obtener información sobre cómo implementar y administrar directivas, consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5b090c5a-6f12-4e60-ace0-c9929afaa9a3">Enable access to company resources with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Certificate profiles are <token>wit_nextref</token> policies that configure managed devices with the certificates they need so device users can connect to your on-premises company resources using connections like Wi-Fi or VPN.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> When you deploy certificate profiles, you provision devices with a trusted root certificate for your PKI, and configure them to request device specific certificates.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">You can create three types of certificate profiles:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">PKCS #12 (.PFX) Certificate Profile: this can be used with Android 4.0 or later, and Windows 10 (desktop and mobile) and later.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">SCEP Certificate Profile: this can be used with iOS 6.0 and later, Android 4.0 or later, and Windows Phone 8.1 and later.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Trusted Certificate Profile: this can be used with iOS 6.0 and later, Android 4.0 or later, and Windows Phone 8.1 and later.</caps:sentence>
            </para>
          </listItem>
        </list>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">About certificate profiles</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Details</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">Use certificate profiles to:</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src10" class="srcSentence">Automatically configure devices so that company resources can be accessed without having to install certificates manually or by using an out-of-band process</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src11" class="srcSentence">Help to keep company resources secure by using your enterprise public key infrastructure (PKI)</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src12" class="srcSentence">Enable you to use server authentication for all connections like Wi-Fi and VPN because you have provisioned the required certificates on the managed devices</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Certificate profiles provide the following management capabilities:</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src14" class="srcSentence">Certificate enrollment and renewal from an Enterprise Certification Authority (CA) for devices that run:</caps:sentence>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <caps:sentence id="src15" class="srcSentence">Android</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src16" class="srcSentence">iOS</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src17" class="srcSentence">Windows 8.1</caps:sentence>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <caps:sentence id="src18" class="srcSentence">Windows Phone 8.1</caps:sentence>
                        </para>
                      </listItem>
                    </list>
                  </listItem>
                </list>
                <para>
                  <caps:sentence id="src19" class="srcSentence">These certificates can then be used for connections to our on-premises infrastructure.</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src20" class="srcSentence">Deployment of Trusted Root CA certificates and intermediate CA certificates to configure a chain-of-trust with devices for connections where server authentication is required.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src21" class="srcSentence">Monitor and report about the installed certificates.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Examples of when to use certificate profiles:</caps:sentence>
                </para>
                <para></para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src23" class="srcSentence">Employees must be able to connect to Wi-Fi hotspots in multiple corporate locations.</caps:sentence>
                      <caps:sentence id="src24" class="srcSentence"> To do this, you can use certificate profiles to deploy the certificates required to secure the Wi-Fi connection.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src25" class="srcSentence">You have a PKI in place and want to move to a more flexible, secure method of provisioning certificates that lets users access company resources from their personal devices without compromising security.</caps:sentence>
                      <caps:sentence id="src26" class="srcSentence"> To do this, you can configure certificate profiles with settings and protocols that are supported for the specific device platform.</caps:sentence>
                      <caps:sentence id="src27" class="srcSentence"> The devices can then automatically request these certificates from an Internet-facing enrollment server.</caps:sentence>
                      <caps:sentence id="src28" class="srcSentence"> You can then configure VPN profiles to use these certificates so that the device can access company resources.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">Types  of certificate profiles</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">Details</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <embeddedLabel>
                    <caps:sentence id="src31" class="srcSentence">Trusted Root Certificate profile</caps:sentence>
                  </embeddedLabel>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">Use this profile to deploy the Trusted Root CA certificate or intermediate CA certificate to devices:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src33" class="srcSentence">Create a Trusted Root Certificate profile for each platform you use.</caps:sentence>
                      <caps:sentence id="src34" class="srcSentence"> You will pair this with each SCEP certificate profile you create for that same platform.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <embeddedLabel>
                    <caps:sentence id="src35" class="srcSentence">.PFX Certificate profile</caps:sentence>
                  </embeddedLabel>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">Use this profile to deploy platform specific settings for device certificate requests:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src37" class="srcSentence">Create a .PFX certificate profile for each platform you use, and pair it with the Trusted CA certificate profile.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src38" class="srcSentence">To complete the task of creating a .PFX certificate profile, you must select a previously created Trusted CA certificate profile.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <embeddedLabel>
                    <caps:sentence id="src39" class="srcSentence">Simple Certificate Enrollment Protocol (SCEP) settings profile</caps:sentence>
                  </embeddedLabel>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">Use this profile to deploy platform specific settings for device certificate requests:</caps:sentence>
                </para>
                <list class="bullet">
                  <listItem>
                    <para>
                      <caps:sentence id="src41" class="srcSentence">Create a SCEP certificate profile for each platform you use, and pair it with the Trusted CA certificate profile.</caps:sentence>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <caps:sentence id="src42" class="srcSentence">To complete the task of creating a SCEP certificate profile, you must select a previously created Trusted CA certificate profile.</caps:sentence>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src43" class="srcSentence">To use SCEP certificate profiles, you must integrate the following on-premises infrastructure with  <token>wit_nextref</token>:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src44" class="srcSentence">A server that runs the Network Device Enrollment Service</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src45" class="srcSentence">An Enterprise Certification Authority</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src46" class="srcSentence">The Intune Certificate Connector, which installs on the Windows Server 2012 R2 server that runs NDES</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src47" class="srcSentence">To use .PFX Certificate profiles, you must integrate the following on-premises infrastructure with  <token>wit_nextref</token>:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src48" class="srcSentence">An enterprise certification authority.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src49" class="srcSentence">A computer that can communicate with the Certification Authority, or use the Certification Authority computer itself.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src50" class="srcSentence">The Intune Certificate Connector, which runs on the computer that can communicate with the Certification Authority.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src51" class="srcSentence">In this topic:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0#BKMK_CertProfileRequirements">Requirements for certificate profiles</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0#BKMK_ConfigureInfrastructure">Configure your infrastructure</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0#BKMK_ConfigProfiles">Configure certificate profiles</link>
            </para>
          </listItem>
          <listItem>
            <para>
              <link xlink:href="8cbb8499-611d-4217-a7b4-e9b864785dd0#BKMK_Deploy">Deploy certificate profiles</link>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_CertProfileRequirements">
        <title>
          <caps:sentence id="src52" class="srcSentence">Requirements for certificate profiles</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section address="BKMK_OnPremises" expanded="false">
            <title>
              <caps:sentence id="src53" class="srcSentence">On-premises Infrastructure</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">Infrastructure</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src55" class="srcSentence">Details</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src56" class="srcSentence">Active Directory domain</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src57" class="srcSentence">All servers listed in this section (except for the Web Application Proxy Server) must be joined to your Active Directory domain.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src58" class="srcSentence">Certification Authority server</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src59" class="srcSentence">Referred to as the issuing CA, you must have an Enterprise Certification Authority (CA) that runs on an Enterprise edition of <token>nextref_server_7</token> or later.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src60" class="srcSentence">A Standalone CA is not supported.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src61" class="srcSentence">For instructions on how to set up a Certification Authority, see <externalLink><linkText>Install the Certification Authority</linkText><linkUri>http://technet.microsoft.com/library/jj125375.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src62" class="srcSentence">If your CA runs Windows Server 2008 R2, you must <externalLink><linkText>install the hotfix from KB2483564</linkText><linkUri>http://support.microsoft.com/kb/2483564/</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">For SCEP profile only: <embeddedLabel>NDES Server</embeddedLabel></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">On a server that runs <token>winblue_server_2</token> or later, you must setup up the Network Device Enrollment Service:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src65" class="srcSentence">
                              <token>wit_nextref</token> does not support using the Network Device Enrollment Service when it runs on a server that also runs the Enterprise CA.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src66" class="srcSentence">See <externalLink><linkText>Network Device Enrollment Service Guidance</linkText><linkUri>http://technet.microsoft.com/library/hh831498.aspx</linkUri></externalLink> for instructions on how to configure <token>winblue_server_2</token> to host the Network Device Enrollment Service.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src67" class="srcSentence">For .PFX Certificate profile only: <embeddedLabel>Computer that can communicate with Certification Authority</embeddedLabel></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">Alternatively, use the Certification Authority computer itself.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">
                          <embeddedLabel>Web Application Proxy Server</embeddedLabel> (optional)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src70" class="srcSentence">You can use a server that runs <token>winblue_server_2</token> or later as a Web Application Proxy (WAP) server.</caps:sentence>
                        <caps:sentence id="src71" class="srcSentence"> This configuration:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src72" class="srcSentence">Allows devices to receive certificates using an Internet connection.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src73" class="srcSentence">Is a security recommendation when devices connect through the Internet to receive and renew certificates.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">The server that hosts WAP <externalLink><linkText>must install an update</linkText><linkUri>http://blogs.technet.com/b/ems/archive/2014/12/11/hotfix-large-uri-request-in-web-application-proxy-on-windows-server-2012-r2.aspx</linkUri></externalLink> that enables support for the long URLs that are used by the Network Device Enrollment Service.</caps:sentence>
                        <caps:sentence id="src75" class="srcSentence"> This update is included with the <externalLink><linkText>December 2014 update rollup</linkText><linkUri>http://support.microsoft.com/kb/3013769</linkUri></externalLink>, or individually from <externalLink><linkText>KB3011135</linkText><linkUri>http://support.microsoft.com/kb/3011135</linkUri></externalLink>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src76" class="srcSentence">Also, the server that hosts WAP must:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src77" class="srcSentence">Have a SSL certificate that matches the name being published to external clients.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src78" class="srcSentence">Trust the SSL certificate that is used on the NDES server.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src79" class="srcSentence">These certificates enable the WAP server to terminate the SSL connection from clients, and create a new SSL connection to the NDES server.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">For information about certificates for WAP, see the <embeddedLabel>Plan certificates</embeddedLabel> section of <externalLink><linkText>Planning to Publish Applications Using Web Application Proxy</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn383650.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">For general information about WAP servers, see <externalLink><linkText>Working with Web Application Proxy</linkText><linkUri>http://technet.microsoft.com/library/dn584113.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src82" class="srcSentence">Microsoft Intune Certificate Connector</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src83" class="srcSentence">You use the <token>wit_nextref</token> admin console to download the <embeddedLabel>Certificate Connector</embeddedLabel> installer (<legacyBold>ndesconnectorssetup.exe</legacyBold>).</caps:sentence>
                        <caps:sentence id="src84" class="srcSentence"> Then you can run <embeddedLabel>ndesconnectorssetup.exe</embeddedLabel> on the computer where you want to install the Certificate Connector.</caps:sentence>
                        <caps:sentence id="src85" class="srcSentence"> For .PFX Certificate profiles, install the Certificate Connector on the computer that communicates with the Certification Authority.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_CertsAndTemplates" expanded="false">
            <title>
              <caps:sentence id="src86" class="srcSentence">Certificates and Templates</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src87" class="srcSentence">Object</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">Details</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src89" class="srcSentence">Certificate Template</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">You configure this template on your issuing CA.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src91" class="srcSentence">Client authentication certificate</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">Requested from your issuing CA or public CA, you install this certificate on the NDES Server.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src93" class="srcSentence">Server authentication certificate</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src94" class="srcSentence">Requested from your issuing CA or public CA, you install and bind this SSL certificate in IIS on the NDES server.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src95" class="srcSentence">Trusted Root CA certificate</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src96" class="srcSentence">You export this as a <embeddedLabel>.cer</embeddedLabel> file from the issuing CA or any device which trusts the issuing CA, and deploy it to devices by using the Trusted CA certificate profile.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src97" class="srcSentence">You use a single Trusted Root CA certificate per operating system platform, and associate it with each Trusted Root Certificate profile you create.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src98" class="srcSentence">You can use additional Trusted Root CA certificates when needed.</caps:sentence>
                            <caps:sentence id="src99" class="srcSentence"> For example, you might do this to provide a trust to a CA that signs the server authentication certificates for your Wi-Fi access points.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_Accounts" expanded="false">
            <title>
              <caps:sentence id="src100" class="srcSentence">Accounts</caps:sentence>
            </title>
            <content>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">Name</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">Details</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src103" class="srcSentence">NDES service account</caps:sentence>
                        </embeddedLabel>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src104" class="srcSentence">You specify a domain user account to use as the NDES Service account.</caps:sentence>
                      </para>
                      <para></para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_ConfigureInfrastructure">
        <title>
          <caps:sentence id="src105" class="srcSentence">Configure your infrastructure</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src106" class="srcSentence">Before you can configure certificate profiles you must complete the following tasks, which require knowledge of Windows Server 2012 R2 and Active Directory Certificate Services (ADCS):</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src107" class="srcSentence">
              <embeddedLabel>Task 1</embeddedLabel> - Configure certificate templates on the certification authority <br /><embeddedLabel>Task 2</embeddedLabel>, for SCEP profile only: - Configure prerequisites on the NDES server <br /><embeddedLabel>Task 3</embeddedLabel>, for SCEP profile only: - Configure NDES for use with <token>wit_nextref</token> <br /><embeddedLabel>Task 4</embeddedLabel> - Enable, install, and configure the Intune Certificate Connector</caps:sentence>
          </para>
        </content>
        <sections>
          <section address="BKMK_ConfigOnPremTask1">
            <title>
              <caps:sentence id="src108" class="srcSentence">Task 1 - Configure certificate templates on the certification authority</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src109" class="srcSentence">In this task you will:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">Create a NDES service account</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src111" class="srcSentence">To revoke certificates the NDES service account requires <legacyItalic>Issue and Manage Certificates</legacyItalic> rights for each certificate template used by a certificate profile.</caps:sentence>
                    </para>
                  </alert>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">Configure a certificate template for NDES</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src113" class="srcSentence">Publish the certificate template for NDES</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src114" class="srcSentence">To configure the certification authority</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src115" class="srcSentence">Create a domain user account to use as the NDES service account.</caps:sentence>
                        <caps:sentence id="src116" class="srcSentence"> You will specify this account when you configure templates on the issuing CA before you install and configure NDES.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src117" class="srcSentence">On the issuing CA, use the Certificate Templates snap-in to create a new custom template or copy an existing template and then edit an existing template (like the User template), for use with NDES.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src118" class="srcSentence">The template must have the following configurations:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src119" class="srcSentence">Specify a friendly <ui>Template display name</ui> for the template.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src120" class="srcSentence">On the <ui>Subject Name</ui> tab, select <ui>Supply in the request</ui>.</caps:sentence>
                            <caps:sentence id="src121" class="srcSentence"> (Security is enforced by the <token>wit_nextref</token> policy module for NDES).</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src122" class="srcSentence">On the <ui>Extensions</ui> tab, ensure the <ui>Description of Application Policies</ui> includes <ui>Client Authentication</ui>.</caps:sentence>
                          </para>
                          <alert class="important">
                            <para>
                              <caps:sentence id="src123" class="srcSentence">For iOS certificate templates, on the <ui>Extensions</ui> tab, edit <ui>Key Usage</ui> and ensure <ui>Signature is proof of origin</ui> is not selected.</caps:sentence>
                            </para>
                          </alert>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src124" class="srcSentence">On the <ui>Security</ui> tab, add the NDES service account, and give it <ui>Read</ui> and <ui>Enroll</ui> permissions to the template.<br /></caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src125" class="srcSentence">Review the <ui>Validity period</ui> on the <ui>General</ui> tab of the template.</caps:sentence>
                        <caps:sentence id="src126" class="srcSentence"> By default, <token>wit_nextref</token> uses the value configured in the template.</caps:sentence>
                        <caps:sentence id="src127" class="srcSentence"> However, you have the option to configure the CA to allow the requester to specify a different value, which you can then set from within the <token>wit_nextref</token> Administrator console.</caps:sentence>
                        <caps:sentence id="src128" class="srcSentence"> If you want to always use the value in the template, skip the remainder of this step.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence id="src129" class="srcSentence">The iOS platform always uses the value set in the template regardless of other configurations you make.</caps:sentence>
                        </para>
                      </alert>
                      <para>
                        <caps:sentence id="src130" class="srcSentence">To configure the CA to allow the requester to specify the validity period, on the CA run the following commands:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <userInput>
                              <caps:sentence id="src131" class="srcSentence">certutil -setreg Policy\EditFlags +EDITF_ATTRIBUTEENDDATE</caps:sentence>
                            </userInput>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <userInput>
                              <caps:sentence id="src132" class="srcSentence">net stop certsvc</caps:sentence>
                            </userInput>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <userInput>
                              <caps:sentence id="src133" class="srcSentence">net start certsvc</caps:sentence>
                            </userInput>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src134" class="srcSentence">On the issuing CA, use the Certification Authority snap-in to publish the certificate template.</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src135" class="srcSentence">Select the <ui>Certificate Templates</ui> node, click <ui>Action</ui>-&gt; <ui>New</ui> &gt; <ui>Certificate Template to Issue</ui>, and then select the template you created in step 2.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src136" class="srcSentence">Validate that the template published by viewing it under the <ui>Certificate Templates</ui> folder.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src137" class="srcSentence">For .PFX profiles: on the CA computer ensure that the computer that hosts the Intune Certificate Connector has enroll permission, so that it can access the template used in creating the .PFX profile.</caps:sentence>
                        <caps:sentence id="src138" class="srcSentence"> Set that permission on the <ui>Security</ui> tab of the CA computer properties.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_ConfigOnPremTask2">
            <title>
              <caps:sentence id="src139" class="srcSentence">Task 2 (SCEP profile only) - Configure prerequisites on the NDES server</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src140" class="srcSentence">In this task you will:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">Add NDES to a Windows Server and configure IIS to support NDES</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src142" class="srcSentence">Add the NDES Service account to the IIS_IUSR group</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src143" class="srcSentence">Set the SPN for the NDES Service account</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src144" class="srcSentence">To configure prerequisites for the NDES Server</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src145" class="srcSentence">On the server that will hosts NDES, you must log on as a an <embeddedLabel>Enterprise Administrator</embeddedLabel>, and then use the <externalLink><linkText>Add Roles and Features Wizard</linkText><linkUri>https://technet.microsoft.com/library/hh831809.aspx</linkUri></externalLink> to install NDES:</caps:sentence>
                      </para>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src146" class="srcSentence">In the Wizard, select <ui>Active Directory Certificate Services</ui> to gain access to the AD CS Role Services.</caps:sentence>
                            <caps:sentence id="src147" class="srcSentence"> Select the <ui>Network Device Enrollment Service</ui>, uncheck <ui>Certification Authority</ui>, and then complete the wizard.</caps:sentence>
                          </para>
                          <alert class="tip">
                            <para>
                              <caps:sentence id="src148" class="srcSentence">On the <ui>Installation progress</ui> page of the wizard, do not click <ui>Close</ui>.</caps:sentence>
                              <caps:sentence id="src149" class="srcSentence"> Instead, click the link for <ui>Configure Active Directory Certificate Services on the destination server</ui>.</caps:sentence>
                              <caps:sentence id="src150" class="srcSentence"> This opens the <ui>AD CS Configuration</ui> wizard that you use for the next task.</caps:sentence>
                              <caps:sentence id="src151" class="srcSentence"> After AD CS Configuration opens, you can close the Add Roles and Features wizard.</caps:sentence>
                            </para>
                          </alert>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src152" class="srcSentence">When NDES is added to the server, the wizard also installs IIS.</caps:sentence>
                            <caps:sentence id="src153" class="srcSentence"> Ensure IIS has the following configurations:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src154" class="srcSentence">
                                  <ui>Web Server</ui> &gt; <ui>Security</ui> &gt; <ui>Request Filtering</ui></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src155" class="srcSentence">
                                  <ui>Web Server</ui> &gt; <ui>Application Development</ui> &gt; <ui>ASP.NET 3.5</ui>.</caps:sentence>
                                <caps:sentence id="src156" class="srcSentence"> Installing ASP.NET 3.5 will install .NET Framework 3.5.</caps:sentence>
                                <caps:sentence id="src157" class="srcSentence"> When installing .NET Framework 3.5, install both the core <ui>.NET Framework 3.5</ui> feature and <ui>HTTP Activation</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src158" class="srcSentence">
                                  <ui>Web Server</ui> &gt; <ui>Application Development</ui> &gt; <ui>ASP.NET 4.5</ui>.</caps:sentence>
                                <caps:sentence id="src159" class="srcSentence"> Installing ASP.NET 4.5 will install .NET Framework 4.5.</caps:sentence>
                                <caps:sentence id="src160" class="srcSentence"> When installing .NET Framework 4.5, install the core <ui>.NET Framework 4.5</ui> feature, <ui>ASP.NET 4.5</ui>, and the <ui>WCF Services</ui> &gt; <ui>HTTP Activation</ui> feature.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src161" class="srcSentence">
                                  <embeddedLabel>Management Tools</embeddedLabel> &gt; <embeddedLabel>IIS 6 Management Compatibility</embeddedLabel> &gt; <ui>IIS 6 Metabase Compatibility</ui></caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src162" class="srcSentence">
                                  <embeddedLabel>Management Tools</embeddedLabel> &gt; <embeddedLabel>IIS 6 Management Compatibility</embeddedLabel> &gt; <ui>IIS 6 WMI Compatibility</ui></caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src163" class="srcSentence">On the server, add the NDES service account as a member of the <ui>IIS_IUSR</ui> group.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src164" class="srcSentence">Run the following command to set the SPN of the NDES Service account:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <userInput>
                              <caps:sentence id="src165" class="srcSentence">setspn -s http/&lt;DNS name of NDES Server&gt; &lt;Domain name&gt;\&lt;NDES Service account name&gt;</caps:sentence>
                            </userInput>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src166" class="srcSentence">For example, if your NDES Server is named <embeddedLabel>Server01</embeddedLabel>, your domain is <embeddedLabel>Contoso.com</embeddedLabel>, and the service account is <embeddedLabel>NDESService</embeddedLabel>, use:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <userInput>
                              <caps:sentence id="src167" class="srcSentence">setspn –s http/Server01.contoso.com contoso\NDESService</caps:sentence>
                            </userInput>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_ConfigOnPremTask3">
            <title>
              <caps:sentence id="src168" class="srcSentence">Task 3 (SCEP profile only) - Configure NDES for use with <token>wit_nextref</token></caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src169" class="srcSentence">In this task you will:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src170" class="srcSentence">Configure NDES for use with the issuing CA</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src171" class="srcSentence">Bind the server authentication (SSL) certificate in IIS</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src172" class="srcSentence">Configure Request Filtering in IIS</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src173" class="srcSentence">To configure NDES for use with <token>wit_nextref</token></caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src174" class="srcSentence">On the NDES Server, open the AD CS Configuration wizard and then make the following configurations.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence id="src175" class="srcSentence">If you clicked the link in the previous task, this wizard is already open.</caps:sentence>
                          <caps:sentence id="src176" class="srcSentence"> Otherwise, open Server Manager to access the post-deployment configuration for Active Directory Certificate Services.</caps:sentence>
                        </para>
                      </alert>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src177" class="srcSentence">On the <ui>Role Services</ui> Page, select the <ui>Network Device Enrollment Service</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src178" class="srcSentence">On the <ui>Service Account for NDES</ui> page, specify the NDES Service Account.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src179" class="srcSentence">On the <ui>CA for NDES</ui> page, click <ui>Select</ui>, and then select the issuing CA where you configured the certificate template.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src180" class="srcSentence">On the <ui>Cryptography for NDES</ui> page, set the key length to meet your company requirements.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src181" class="srcSentence">On the <ui>Confirmation</ui> page, click <ui>Configure</ui> to complete the wizard.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src182" class="srcSentence">After the wizard completes, edit the following registry key on the NDES Server:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src183" class="srcSentence">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Cryptography\MSCEP\</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src184" class="srcSentence">To edit this key, identify the certificate template's <ui>Purpose</ui>, as found on its <ui>Request Handling</ui> tab, and then edit the corresponding entry in the registry by replacing the existing data with the name of the certificate template (not the display name of the template) that you specified in Task 1.</caps:sentence>
                        <caps:sentence id="src185" class="srcSentence"> The following table maps the certificate template purpose to the values in the registry:</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src186" class="srcSentence">Certificate template Purpose (On the Request Handling tab)</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src187" class="srcSentence">Registry value to edit</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src188" class="srcSentence">Value seen in the <token>wit_nextref</token> admin console for the SCEP profile </caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src189" class="srcSentence">Signature</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src190" class="srcSentence">SignatureTemplate</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src191" class="srcSentence">Digital Signature</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src192" class="srcSentence">Encryption</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src193" class="srcSentence">EncryptionTemplate</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src194" class="srcSentence">Key Encipherment</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src195" class="srcSentence">Signature and encryption</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src196" class="srcSentence">GeneralPurposeTemplate</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                            <TD>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src197" class="srcSentence">Key Encipherment</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src198" class="srcSentence">Digital Signature</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                      <para>
                        <caps:sentence id="src199" class="srcSentence">For example, if the Purpose of your certificate template is <ui>Encryption</ui>, then edit the <ui>EncryptionTemplate</ui> value to be the name of your certificate template.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src200" class="srcSentence">After editing the registry, run <userInput>iisreset</userInput> on the server to force the server to pick up recent configuration changes.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src201" class="srcSentence">To Install and bind certificates on the NDES Server</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src202" class="srcSentence">On your NDES Server, request and install a <embeddedLabel>server authentication</embeddedLabel> certificate from your internal CA or public CA.</caps:sentence>
                        <caps:sentence id="src203" class="srcSentence"> You will then bind this SSL certificate in IIS.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence id="src204" class="srcSentence">After you bind the SSL certificate in IIS, you will also install a client authentication certificate.</caps:sentence>
                          <caps:sentence id="src205" class="srcSentence"> This certificate can be issued by any CA that is trusted by the NDES Server.</caps:sentence>
                          <caps:sentence id="src206" class="srcSentence"> Although it is not a best practice, you can use the same certificate for both server and client authentication as long as the certificate has both Enhance Key Usages (EKU’s).</caps:sentence>
                          <caps:sentence id="src207" class="srcSentence"> Review the following steps for information about these authentication certificates.</caps:sentence>
                        </para>
                      </alert>
                      <list class="ordered">
                        <listItem>
                          <para>
                            <caps:sentence id="src208" class="srcSentence">After you obtain the server authentication certificate, open <ui>IIS Manager</ui>, select the <ui>Default Web Site</ui> in the <ui>Connections</ui> pane, and then click <ui>Bindings</ui> in the <ui>Actions</ui> pane.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src209" class="srcSentence">Click <ui>Add</ui>, set <ui>Type</ui> to <ui>https</ui>, and then ensure the port is <ui>443</ui>.</caps:sentence>
                            <caps:sentence id="src210" class="srcSentence"> (Only port 443 is supported for standalone <token>wit_nextref</token>).</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src211" class="srcSentence">For <ui>SSL certificate</ui>, specify the server authentication certificate.</caps:sentence>
                          </para>
                          <alert class="note">
                            <para>
                              <caps:sentence id="src212" class="srcSentence">If the NDES server uses both an external and internal name for a single network address, the server authentication certificate must have a <ui>Subject Name</ui> with an external public server name, and a <ui>Subject Alternative Name</ui> that includes the internal server name.</caps:sentence>
                            </para>
                          </alert>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src213" class="srcSentence">On your NDES Server, request and install a <embeddedLabel>client authentication</embeddedLabel> certificate from your internal CA, or a public certificate authority.</caps:sentence>
                        <caps:sentence id="src214" class="srcSentence"> This can be the same certificate as the server authentication certificate if that certificate has both capabilities.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src215" class="srcSentence">The client authentication certificate must have the following properties:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src216" class="srcSentence">
                              <ui>Enhanced Key Usage</ui> - This must include <ui>Client Authentication</ui>.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src217" class="srcSentence">
                              <ui>Subject Name</ui> - This must be equal to the DNS name of the server where you are installing the certificate (the NDES Server).</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src218" class="srcSentence">To configure IIS Request Filtering</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src219" class="srcSentence">On the NDES Server open <ui>IIS Manager</ui>, select the <ui>Default Web Site</ui> in the <ui>Connections</ui> pane, and then open <ui>Request Filtering</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src220" class="srcSentence">Click <ui>Edit Feature Settings</ui>, and then set the following:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src221" class="srcSentence">
                              <ui>query string (Bytes)</ui> = <userInput>65534</userInput></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src222" class="srcSentence">
                              <ui>Maximum URL length (Bytes)</ui> = <userInput>65534</userInput></caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src223" class="srcSentence">Review the following registry key:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src224" class="srcSentence">HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\HTTP\Parameters</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src225" class="srcSentence">Ensure the following values are set as DWORD entries:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src226" class="srcSentence">Name: <ui>MaxFieldLength</ui>, with a decimal value of <userInput>65534</userInput></caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src227" class="srcSentence">Name: <ui>MaxRequestBytes</ui>, with a decimal value of <userInput>65534</userInput></caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src228" class="srcSentence">Reboot the NDES server.</caps:sentence>
                        <caps:sentence id="src229" class="srcSentence"> The server is now ready to support the Certificate Connector.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section address="BKMK_ConfigOnPremTask4">
            <title>
              <caps:sentence id="src230" class="srcSentence">Task 4 - Enable, install, and configure the Intune Certificate Connector  - For SCEP and .PFX certificates.</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src231" class="srcSentence">In this task you will:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src232" class="srcSentence">Enable support for NDES in <token>wit_nextref</token></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src233" class="srcSentence">Download, install, and configure the Certificate Connector on the NDES Server</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src234" class="srcSentence">To enable support for the Certificate Connector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src235" class="srcSentence">Open the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Certificate Connector</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src236" class="srcSentence">Click <ui>Configure On-Premises Certificate Connector</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src237" class="srcSentence">Select <ui>Enable Certificate Connector</ui>, and then click <ui>OK</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src238" class="srcSentence">To download, install and configure the Certificate Connector</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src239" class="srcSentence">Open the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, and then click <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Certificate Connector</ui> &gt; <ui>Download Certificate Connector</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src240" class="srcSentence">After the download completes, run the downloaded installer (<embeddedLabel>ndesconnectorssetup.exe</embeddedLabel>):</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src241" class="srcSentence">For .PFX certificates, run the installer on the computer that is able to connect with the Certification Authority.</caps:sentence>
                            <caps:sentence id="src242" class="srcSentence"> Choose the .PFX Distribution option then click Install.</caps:sentence>
                            <caps:sentence id="src243" class="srcSentence"> When the installation has completed, continue by creating a certificate profile.</caps:sentence> </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src244" class="srcSentence">For SCEP certificates, run the installer on a Windows Server 2012 R2 server</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src245" class="srcSentence">  For the SCEP option, the installer also installs the policy module for NDES and the CRP Web Service.</caps:sentence>
                        <caps:sentence id="src246" class="srcSentence"> (The CRP Web Service, CertificateRegistrationSvc, runs as an application in IIS.)</caps:sentence>
                      </para>
                      <alert class="note">
                        <para>
                          <caps:sentence id="src247" class="srcSentence">When you install NDES for standalone <token>wit_nextref</token>, the CRP service automatically installs with the Certificate Connector.</caps:sentence>
                          <caps:sentence id="src248" class="srcSentence"> When you use <token>wit_nextref</token> with Configuration Manager, you install the Certificate Registration Point as a separate site system role.</caps:sentence>
                        </para>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src249" class="srcSentence">When prompted for the client certificate for the Certificate Connector, click <ui>Select</ui>, and select the <embeddedLabel>client authentication</embeddedLabel> certificate you installed on your NDES Server in Task 3.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src250" class="srcSentence">After you select the client authentication certificate, you are returned to the <ui>Client Certificate for Microsoft Intune Certificate Connector</ui> surface.</caps:sentence>
                        <caps:sentence id="src251" class="srcSentence"> Although the certificate you selected is not shown, click <ui>Next</ui> to view the properties of that certificate.</caps:sentence>
                        <caps:sentence id="src252" class="srcSentence"> Then click <ui>Next</ui>, and then click <ui>Install</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src253" class="srcSentence">After the wizard completes, but before closing the wizard, click <ui>Launch the Certificate Connector UI</ui>.</caps:sentence>
                      </para>
                      <alert class="tip">
                        <para>
                          <caps:sentence id="src254" class="srcSentence">If you close the wizard before launching the Certificate Connector UI, you can reopen it by running the following command:</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <userInput>
                                <caps:sentence id="src255" class="srcSentence">&lt;install_Path&gt;\NDESConnectorUI\NDESConnectorUI.exe</caps:sentence>
                              </userInput>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src256" class="srcSentence">In the <ui>Certificate Connector</ui> UI:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src257" class="srcSentence">Click <ui>Sign In</ui> and enter your <token>wit_nextref</token> service administrator credentials, or credentials for a tenant administrator with the global administration permission.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src258" class="srcSentence">If your organization uses a proxy server and the proxy is required for the NDES server to access the Internet, click <ui>Use proxy server</ui> and then provide the proxy server name, port, and account credentials to connect.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src259" class="srcSentence">Select the <ui>Advanced</ui> tab, and then provide credentials for an account that has the <ui>Issue and Manage Certificates</ui> permission on your issuing Certificate Authority, and then click <ui>Apply</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src260" class="srcSentence">You can now close the Certificate Connector UI.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src261" class="srcSentence">Open a command prompt and type <userInput>services.msc</userInput>, and then press <ui>Enter</ui>, right-click the <ui>Certificate Connector Service</ui>, and then click <ui>Restart</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence id="src262" class="srcSentence">To validate that the service is running, open a browser and enter the following URL, which should return a <ui>403</ui> error:</caps:sentence>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <userInput>
                            <caps:sentence id="src263" class="srcSentence">http:// &lt;FQDN_of_your_NDES_server&gt;/certsrv/mscep/mscep.dll</caps:sentence>
                          </userInput>
                        </para>
                      </listItem>
                    </list>
                    <para>
                      <caps:sentence id="src264" class="srcSentence">You are now ready to configure certificate profiles.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_ConfigProfiles">
        <title>
          <caps:sentence id="src265" class="srcSentence">Configure certificate profiles</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src266" class="srcSentence">After your infrastructure and certificates are configured, you can configure certificate profiles:</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src267" class="srcSentence">
              <embeddedLabel>Task 1</embeddedLabel> - Export the Trusted Root CA certificate <br /><embeddedLabel>Task 2</embeddedLabel> - Create Trusted CA certificate profiles <br /><embeddedLabel>Task 3</embeddedLabel> - Either: </caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src268" class="srcSentence">Create SCEP certificate profiles</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src269" class="srcSentence">Create .PFX certificate profiles</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="BKMK_ConfigExportRootCA">
            <title>
              <caps:sentence id="src270" class="srcSentence">Task 1 - Export the Trusted Root CA certificate </caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src271" class="srcSentence">Export the Trusted Root CA certificate as a <ui>.cer</ui> file from the issuing CA, or any device that trusts your issuing CA.</caps:sentence>
                <caps:sentence id="src272" class="srcSentence"> You do not export the private key.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src273" class="srcSentence">You will import this certificate when you configure a Trusted CA certificate profile.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_ConfigRootCA">
            <title>
              <caps:sentence id="src274" class="srcSentence">Task 2 - Create Trusted CA certificate profiles</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src275" class="srcSentence">You must create a <ui>Trusted CA certificate profile</ui> before you can create a <ui>Simple Certificate Enrollment Protocol settings profile</ui>.</caps:sentence>
                <caps:sentence id="src276" class="srcSentence"> Both profiles are required for each mobile device platform.</caps:sentence>
              </para>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src277" class="srcSentence">To create a trusted certificate profile</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src278" class="srcSentence">Open the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, and click <ui>Policy</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src279" class="srcSentence">Configure one of the following policy types:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src280" class="srcSentence">Android &gt; Trusted Certificate Profile (Android 4 and later)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src281" class="srcSentence">iOS &gt; Trusted Certificate Profile (iOS 5 and later)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src282" class="srcSentence">Windows Phone and Enrolled Windows Devices &gt; Trusted Certificate Profile (Windows 8.1 and later)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src283" class="srcSentence">Windows Phone and Enrolled Windows Devices &gt; Trusted Certificate Profile (Windows Phone 8.1 and later)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src284" class="srcSentence">Learn more: <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src285" class="srcSentence">Use the following information to configure the trusted certificate profile settings for Android, iOS, Windows 8.1, or Windows Phone 8.1:</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src286" class="srcSentence">Setting name</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src287" class="srcSentence">Platform</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src288" class="srcSentence">More information</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src289" class="srcSentence">Name</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src290" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src291" class="srcSentence">Provide a descriptive name for the certificate profile.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src292" class="srcSentence">Description</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src293" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src294" class="srcSentence">Provide an optional description for the certificate.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src295" class="srcSentence">Certificate file</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src296" class="srcSentence">All</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src297" class="srcSentence">Click <ui>Import</ui>, and then select the Trusted Root CA certificate (<ui>.cer</ui>) that you exported from your issuing CA.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src298" class="srcSentence">Destination store</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src299" class="srcSentence">Windows 8.1</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src300" class="srcSentence">For devices that have more than one certificate store, select where to store the certificate.</caps:sentence>
                                <caps:sentence id="src301" class="srcSentence"> Select from:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <ui>
                                      <caps:sentence id="src302" class="srcSentence">Computer certificate store – Root</caps:sentence>
                                    </ui>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <ui>
                                      <caps:sentence id="src303" class="srcSentence">Computer Certificate store – Intermediate</caps:sentence>
                                    </ui>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <ui>
                                      <caps:sentence id="src304" class="srcSentence">User certificate store – Intermediate</caps:sentence>
                                    </ui>
                                  </para>
                                </listItem>
                              </list>
                              <para>
                                <caps:sentence id="src305" class="srcSentence">For devices that have only one store, this setting is ignored.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src306" class="srcSentence">When you are finished, click <ui>Save Policy</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence id="src307" class="srcSentence">The new policy displays in the <ui>Policy</ui> workspace, and can now be deployed.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
          <section address="BKMK_ConfigSCEP">
            <title>
              <caps:sentence id="src308" class="srcSentence">Task 3 – Create SCEP or .PFX certificate profiles</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src309" class="srcSentence">After you have created a Trusted CA certificate profile, create SCEP or .PFX certificate profiles for each platform you want to use.</caps:sentence>
                <caps:sentence id="src310" class="srcSentence"> When you create a SCEP certificate profile, you must specify a Trusted CA certificate profile for that same platform.</caps:sentence>
                <caps:sentence id="src311" class="srcSentence"> This links the two certificate profiles, although, you must still deploy each profile separately.</caps:sentence>
              </para>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src312" class="srcSentence">To create a SCEP certificate profile</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src313" class="srcSentence">Open the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src314" class="srcSentence">Configure one of the following policy types:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src315" class="srcSentence">Android &gt; SCEP Certificate Profile (Android 4 and later)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src316" class="srcSentence">iOS &gt; SCEP Certificate Profile (iOS 5 and later)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src317" class="srcSentence">Windows Phone and Enrolled Windows Devices &gt; SCEP Certificate Profile (Windows 8.1 and later)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src318" class="srcSentence">Windows Phone and Enrolled Windows Devices &gt; SCEP Certificate Profile (Windows Phone 8.1 and later)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src319" class="srcSentence">Learn more: <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src320" class="srcSentence">Use the following information to configure the SCEP certificate profile settings for Android, iOS, Windows 8.1, and Windows Phone 8.1:</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src321" class="srcSentence">Setting name</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src322" class="srcSentence">Platform</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src323" class="srcSentence">More information</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <embeddedLabel>
                                  <caps:sentence id="src324" class="srcSentence">Name</caps:sentence>
                                </embeddedLabel>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src325" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src326" class="srcSentence">Provide a descriptive name for the certificate profile.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <embeddedLabel>
                                  <caps:sentence id="src327" class="srcSentence">Description</caps:sentence>
                                </embeddedLabel>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src328" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src329" class="srcSentence">Provide an optional description for the certificate.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src330" class="srcSentence">Renewal threshold (%)</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src331" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src332" class="srcSentence">Specify the percentage of the certificate lifetime that remains before the device requests renewal of the certificate.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src333" class="srcSentence">Key Storage Provider (KSP)</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src334" class="srcSentence">Android <br />Windows 8.1 <br />Windows Phone 8.1</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src335" class="srcSentence">Specify where the key to the certificate will be stored.</caps:sentence>
                                <caps:sentence id="src336" class="srcSentence"> Choose from one of the following:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src337" class="srcSentence">
                                      <ui>Install to Trusted Platform Module (TPM) if present</ui> - Installs the key to the TPM.</caps:sentence>
                                    <caps:sentence id="src338" class="srcSentence"> If the TPM is not present, the key will be installed to the storage provider for the software key.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src339" class="srcSentence">
                                      <ui>Install to Trusted Platform Module (TPM) otherwise fail</ui> - Installs the key to the TPM.</caps:sentence>
                                    <caps:sentence id="src340" class="srcSentence"> If the TPM module is not present, the installation will fail</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src341" class="srcSentence">
                                      <ui>Install to Software Key Storage Provider</ui> - Installs the key to the storage provider for the software key.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src342" class="srcSentence">SCEP server URL</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src343" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src344" class="srcSentence">Enter a URL (with the <userInput>http://</userInput> or <userInput>https://</userInput> prefix), then click <ui>Add</ui>; or select a URL, and then click <ui>Delete</ui>.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src345" class="srcSentence">For example, a SCEP server URL might resemble the following:: <embeddedLabel>https://mdmndes1.contoso.com/certsrv/mscep/mscep.dll</embeddedLabel></caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src346" class="srcSentence">Each SCEP profile supports a single SCEP server URL.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src347" class="srcSentence">Subject name format</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src348" class="srcSentence">Android <br />Windows 8.1 <br />Windows Phone 8.1</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src349" class="srcSentence">From the list, select how <token>wit_nextref</token> automatically creates the subject name in the certificate request.</caps:sentence>
                                <caps:sentence id="src350" class="srcSentence"> If the certificate is for a user, you can also include the user's email address in the subject name.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src351" class="srcSentence">You can select <ui>Common Name</ui> or <ui>Common Name and email address</ui>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src352" class="srcSentence">Subject Alternative Name</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src353" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src354" class="srcSentence">Select <ui>Email Address</ui>, <ui>User principal name (UPN)</ui>, or both.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src355" class="srcSentence">Certificate validity period</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src356" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src357" class="srcSentence">Specify the amount of time before the certificate expires.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src358" class="srcSentence">Key Usage</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src359" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src360" class="srcSentence">Specify key usage options for the certificate.</caps:sentence>
                                <caps:sentence id="src361" class="srcSentence"> You can choose from the following options:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src362" class="srcSentence">
                                      <ui>Digital Signature</ui> (SignatureTemplate) – Use to digitally sign data.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src363" class="srcSentence">
                                      <ui>Key Encipherment</ui> (EncryptionTemplate) - Use for encryption.</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src364" class="srcSentence">
                                      <ui>Key Encipherment + Digital Signature</ui> (GeneralPurposeTemplate) – Use to digitally sign and encrypt data.</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src365" class="srcSentence">Key size (bits)</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src366" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src367" class="srcSentence">Select the size of the key in bits that is supported by your device.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src368" class="srcSentence">Select <ui>1024</ui> or <ui>2048</ui>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src369" class="srcSentence">Hash algorithm</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src370" class="srcSentence">Android <br />Windows 8.1 <br />Windows Phone 8.1</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src371" class="srcSentence">Select one of the available hash algorithm types to use with this certificate.</caps:sentence>
                                <caps:sentence id="src372" class="srcSentence"> Select the strongest level of security that the connecting devices support.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src373" class="srcSentence">Select <ui>SHA-1</ui>, <ui>SHA-2</ui>, or both.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src374" class="srcSentence">Extended Key Usage</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src375" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src376" class="srcSentence">Click <ui>Select</ui> to add values for the certificate’s intended purpose.</caps:sentence>
                                <caps:sentence id="src377" class="srcSentence"> In most cases, the certificate will require <ui>Client Authentication</ui> so that the user or device can authenticate to a server.</caps:sentence>
                                <caps:sentence id="src378" class="srcSentence"> However, you can add any other key usages as required.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src379" class="srcSentence">Select Root Certificate</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src380" class="srcSentence">All </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src381" class="srcSentence">Click <ui>Select</ui> to choose a root CA certificate profile that you have previously configured and deployed to the user or device.</caps:sentence>
                                <caps:sentence id="src382" class="srcSentence"> This CA certificate must be the root certificate for the CA that will issue the certificate that you are configuring in this certificate profile.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src383" class="srcSentence">When you are finished, click <ui>Save Policy</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence id="src384" class="srcSentence">The new policy displays in the <ui>Policy</ui> workspace, and can now be deployed.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src385" class="srcSentence">To create a .PFX certificate profile</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src386" class="srcSentence">Open the <externalLink><linkText>Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Add Policy</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src387" class="srcSentence">Configure one of the following policy types:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src388" class="srcSentence">Android &gt;.PFX Certificate Profile (Android 4 and later)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src389" class="srcSentence">Windows Phone and Enrolled Windows Devices &gt; .PFX Certificate Profile (Windows 10 and later)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <ui>
                              <caps:sentence id="src390" class="srcSentence">Windows Phone and Enrolled Windows Devices &gt; .PFX Certificate Profile (Windows Phone 10 and later)</caps:sentence>
                            </ui>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src391" class="srcSentence">Learn more: <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src392" class="srcSentence">Use the following information to configure the .PFX  certificate profile settings for Android, Windows 10, and Windows Phone 10:</caps:sentence>
                      </para>
                      <table>
                        <thead>
                          <tr>
                            <TD>
                              <para>
                                <caps:sentence id="src393" class="srcSentence">Setting name</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src394" class="srcSentence">Platform</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src395" class="srcSentence">More information</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <TD>
                              <para>
                                <embeddedLabel>
                                  <caps:sentence id="src396" class="srcSentence">Name</caps:sentence>
                                </embeddedLabel>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src397" class="srcSentence">Android <br />Windows 10 <br />Windows Phone 10</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src398" class="srcSentence">Provide a descriptive name for the certificate profile.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <embeddedLabel>
                                  <caps:sentence id="src399" class="srcSentence">Description</caps:sentence>
                                </embeddedLabel>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src400" class="srcSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src401" class="srcSentence">Provide an optional description for the certificate.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src402" class="srcSentence">Renewal threshold (%)</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src403" class="srcSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src404" class="srcSentence">Specify the percentage of the certificate lifetime that remains before the device requests renewal of the certificate.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src405" class="srcSentence">Certification authority</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src406" class="srcSentence">Android <br />Windows 10 <br />Windows Phone 10</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src407" class="srcSentence">Provide the FQDN of the certification authority, for example, <legacyItalic>device.certs.contoso.com</legacyItalic>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src408" class="srcSentence">Certification authority name</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src409" class="srcSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src410" class="srcSentence">Provide the name of the certification authority, such as <legacyItalic>device-contoso-CA</legacyItalic>.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src411" class="srcSentence">Certification template name</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src412" class="srcSentence">Android <br />Windows 10 <br />Windows Phone 10</caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src413" class="srcSentence">Provide the name of the certification template (not the display name).</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src414" class="srcSentence">Subject name format</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src415" class="srcSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src416" class="srcSentence">Provide one subject name format from the choices provided:</caps:sentence>
                              </para>
                              <list class="bullet">
                                <listItem>
                                  <para>
                                    <caps:sentence id="src417" class="srcSentence">Common name</caps:sentence>
                                  </para>
                                </listItem>
                                <listItem>
                                  <para>
                                    <caps:sentence id="src418" class="srcSentence">Common name and email address</caps:sentence>
                                  </para>
                                </listItem>
                              </list>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src419" class="srcSentence">Subject alternative name </caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src420" class="srcSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src421" class="srcSentence">Choose the subject alternative names.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                          <tr>
                            <TD>
                              <para>
                                <ui>
                                  <caps:sentence id="src422" class="srcSentence">Certificate validity period</caps:sentence>
                                </ui>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src423" class="srcSentence">Android <br />Windows 10 <br />Windows Phone 10 </caps:sentence>
                              </para>
                            </TD>
                            <TD>
                              <para>
                                <caps:sentence id="src424" class="srcSentence">Specify the amount of time before the certificate expires.</caps:sentence>
                              </para>
                            </TD>
                          </tr>
                        </tbody>
                      </table>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src425" class="srcSentence">When you are finished, click <ui>Save Policy</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence id="src426" class="srcSentence">The new policy displays in the <ui>Policy</ui> workspace, and can now be deployed.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_Deploy">
        <title>
          <caps:sentence id="src427" class="srcSentence">Deploy certificate profiles</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src428" class="srcSentence">When you deploy certificate profiles, the certificate file from the Trusted CA certificate profile is installed on devices, and the SCEP or .PFX certificate profile is used by the device to create a certificate request by the device.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src429" class="srcSentence">Certificate profiles install only on applicable devices based on the platform you use when creating the profile.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src430" class="srcSentence">You can deploy certificate profiles to user collections or device collections.</caps:sentence>
              </para>
              <alert class="tip">
                <para>
                  <caps:sentence id="src431" class="srcSentence">To allow certificates to be published to devices quickly after the device enrolls, deploy the certificate profile to a user group (not a device group).</caps:sentence>
                  <caps:sentence id="src432" class="srcSentence"> If you deploy to a device group, a full device registration must take place before the device receives policy.</caps:sentence>
                </para>
              </alert>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src433" class="srcSentence">Although each profile is deployed separately, both the Trusted Root and the SCEP/.PFX profile must be deployed or else the SCEP/.PFX certificate policy will fail.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src434" class="srcSentence">You deploy certificate profiles the same way you deploy other policy for <token>wit_nextref</token>.</caps:sentence>
            <caps:sentence id="src435" class="srcSentence"> For information about how to deploy and manage policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="5b090c5a-6f12-4e60-ace0-c9929afaa9a3">Enable access to company resources with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>