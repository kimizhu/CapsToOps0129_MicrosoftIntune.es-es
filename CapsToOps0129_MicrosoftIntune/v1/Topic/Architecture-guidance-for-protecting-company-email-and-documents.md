---
title: Gu&#237;a de arquitectura para proteger los documentos y correos electr&#243;nicos de la empresa
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc9c7d79-d2ca-4cb2-8456-c7a88cbbf6fd
---
# Gu&#237;a de arquitectura para proteger los documentos y correos electr&#243;nicos de la empresa
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b077a4307c07c79606209379427cad61" id="tgt1" class="tgtSentence">Este tema comienza con una visión general de cómo puede proteger los datos de su empresa y garantizar que la experiencia del usuario final sea sencilla y que no afecte a la productividad.</caps:sentence>
          <caps:sentence sentenceid="251b5d7977ff1015f3333de3c31ead69" id="tgt2" class="tgtSentence"> A continuación, nos centraremos específicamente en cómo puede proporcionar un acceso seguro al correo electrónico de su empresa y en cómo proteger los datos de la empresa que aparezcan en correos electrónicos y en archivos adjuntos mediante la solución de Microsoft Enterprise Mobility Suite.</caps:sentence>
        </para>
        <alert class="tip">
          <para>
            <caps:sentence sentenceid="d548bb1b404073073816696b4fc230f0" id="tgt3" class="tgtSentence">Obtenga una copia descargable de este tema completo en la <externalLink><linkText>Galería de TechNet</linkText><linkUri>https://gallery.technet.microsoft.com/Managing-Access-and-Help-b7a05d0d/file/140056/1/Managing%20Access%20and%20Help%20Protect%20Corporate%20Email%20Data%20on%20Mobile%20Devices.pdf</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6b62db269c7b86a7ce2ec34a153856da" id="tgt4" class="tgtSentence">Equilibrio entre la productividad y seguridad</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8537ca008f57cd2e55e9118defc12a71" id="tgt5" class="tgtSentence">Los empleados quieren poder usar sus propios dispositivos para tener acceso a recursos y herramientas de productividad de la empresa.</caps:sentence>
            <caps:sentence sentenceid="4f720aed9e8356f0542156c39b5c5e1e" id="tgt6" class="tgtSentence"> El departamento de TI debe asegurarse de que los empleados tienen esta capacidad, pero se protegen los datos confidenciales de la empresa.</caps:sentence>
            <caps:sentence sentenceid="58246a07a34a85a5bf3da2b7a8b411aa" id="tgt7" class="tgtSentence"> BYOD, o <externalLink><linkText>Bring your own device</linkText><linkUri>https://technet.microsoft.com/en-us/library/Dn656905(l=en-us,v=WS.11).aspx</linkUri></externalLink>, supone un desafío específico, ya que debe haber una separación de datos personales y de trabajo en los dispositivos personales y se debe evitar la compartición, intencional o involuntaria, de datos de la empresa.</caps:sentence>
          </para>
          <para>
            <embeddedLabel>
              <caps:sentence sentenceid="41cbcf243be0fc45d0f9ffdd26b83477" id="tgt8" class="tgtSentence">Los estudios demuestran que:</caps:sentence>
            </embeddedLabel>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="5a8808d37bdf0ec4a3fb2c53575f4baa" id="tgt9" class="tgtSentence">El 37% del personal de todo el mundo es móvil*</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3d29aba07bc51299ff1b673e8c1f4efb" id="tgt10" class="tgtSentence">El 53% del total de correo electrónico se abrió desde un teléfono móvil o tableta en el 3T de 2014 **</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="bdaa63ad441a789a88ddb77db0bceefe" id="tgt11" class="tgtSentence">El 61% de los trabajadores combina tareas personales y profesionales en sus dispositivos ***</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="32cc38dc4ef57bd1ddc5ac6c91ead0e8" id="tgt12" class="tgtSentence">Considere lo siguiente:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="212d75b22c4f9c3fdd4ec486317f531b" id="tgt13" class="tgtSentence">El correo electrónico suele ser la aplicación más utilizada en cualquier dispositivo.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="088012f1a55912df7949e25f533a5114" id="tgt14" class="tgtSentence">El contenido del correo electrónico y los datos adjuntos del correo electrónico se puede copiar, compartir o mover a otras ubicaciones fuera del alcance del departamento de TI, lo que puede poner en peligro la seguridad de la empresa.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="d76e2601339713d443b2b1077b6da375" id="tgt15" class="tgtSentence">Puesto que los usuarios finales quieren trabajar con sus propios dispositivos personales y el correo electrónico es la aplicación que más se utiliza, el primer paso para el departamento de TI es asegurarse de que los usuarios finales puedan acceder al correo electrónico corporativo en sus dispositivos y asegurarse de que los datos confidenciales del correo electrónico no se vean comprometidos.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="bce059749d61c1c247c303d0118d0d53" id="tgt16" class="tgtSentence">Información general</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="07a1ab208c689973089f0b1c97e0839d" id="tgt17" class="tgtSentence">Microsoft ofrece Enterprise Mobility Suite (EMS), una solución completa para la administración de identidades, dispositivos móviles y aplicaciones, así como para la protección de datos.</caps:sentence>
            <caps:sentence sentenceid="2eea99ded5b9dd53d277bbdb3476143a" id="tgt18" class="tgtSentence"> EMS proporciona un modelo de seguridad por capas que permite al departamento de TI administrar el acceso al correo electrónico, datos y aplicaciones corporativas desde casi cualquier dispositivo.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="92b0455915b92d6f1ccb3a9b0cbde3ab" id="tgt19" class="tgtSentence">EMS se compone de los siguientes servicios en la nube:</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="2c5f1cb4-2880-4efa-ae38-d4963d9f1345"></image>
          </mediaLink>
          <para>
            <caps:sentence sentenceid="a91159d7f364f5923d3aa0c26b9b4385" id="tgt20" class="tgtSentence">Con EMS, los datos están protegidos dentro y fuera de la red corporativa:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="0193efd19307883d3bc03889964126d4" id="tgt21" class="tgtSentence">Los empleados tienen acceso al correo electrónico corporativo, las aplicaciones relacionadas con el trabajo y los datos de la empresa en el dispositivo que elijan sin preocuparse por poner en peligro la información confidencial de la empresa.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="b9a7ad210bab331cb527b5dd34f91777" id="tgt22" class="tgtSentence">Los datos de la empresa se protegen a todos los niveles: usuario, dispositivo, aplicación y, finalmente, en el nivel de los datos en sí.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5f3eabbb7a9c216797f0408b64c074f6" id="tgt23" class="tgtSentence">El administrador de TI puede asegurarse de que solo acceden a los datos corporativos los usuarios de confianza desde dispositivos compatibles y administrados y en el contexto de las aplicaciones administradas.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="21bc22f14c80a5bcc77173685571ab1a" id="tgt24" class="tgtSentence">Las aplicaciones administradas de Intune incluyen las aplicaciones móviles de Office, que son esenciales para esta solución.</caps:sentence>
            <caps:sentence sentenceid="d99dfc8f3bbd535c6c01ab8efeb6c11a" id="tgt25" class="tgtSentence"> Con las aplicaciones móviles de Office, podrá contribuir a maximizar la productividad de los empleados y evitar la filtración de datos.</caps:sentence>
            <caps:sentence sentenceid="4aaa3823643810cec56558e91c500ed0" id="tgt26" class="tgtSentence"> Por ejemplo, los administradores de TI pueden configurar directivas que impidan la copia de datos de la empresa al almacenamiento personal en la nube, por ejemplo, en Dropbox.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="887e9ccb3415204836f605d092ca7192" id="tgt27" class="tgtSentence">Cuando los empleados mueven o cambian trabajos o pierden su dispositivo, EMS proporciona la opción de borrar los datos corporativos del dispositivo de forma selectiva y remota.</caps:sentence>
            <caps:sentence sentenceid="bafd83363d8f514dad55405d16e303b9" id="tgt28" class="tgtSentence"> Puede hacerlo el usuario final o el administrador de TI.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="8e0215780c5210d302017d9fbe779c81" id="tgt29" class="tgtSentence">Cómo puede ayudar a proteger los datos EMS</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f8042dee2338032a06d5c320c6291fff" id="tgt30" class="tgtSentence">El modelo de seguridad de 4 niveles de identidad, dispositivos, aplicaciones y datos consiste en asegurarse de que solo accede a los recursos de la empresa el usuario designado, desde un dispositivo que cumpla un conjunto de directivas de cumplimiento configuradas por el usuario y dentro de los límites de las aplicaciones administradas.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="ec85aa6d-b075-4c92-92fc-dc8e467eaa23"></image>
          </mediaLink>
          <para>
            <caps:sentence sentenceid="51f3c9de5d06f05c563ce15daf754f65" id="tgt31" class="tgtSentence">La protección de los datos comienza con el establecimiento y la validación de la identidad del usuario.</caps:sentence>
            <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt32" class="tgtSentence">
              <newTerm>Azure AD /</newTerm>, una herramienta de administración de identidades y acceso de nivel empresarial ofrece un inicio de sesión único, autenticación multifactor, contraseñas de autoservicio, etc.</caps:sentence>
            <caps:sentence sentenceid="a4725b455f3ae9a7f75ba258c4456bb8" id="tgt33" class="tgtSentence"> Proporciona la funcionalidad para la <embeddedLabel>capa de identidad</embeddedLabel> del modelo de seguridad.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6b0c66e667c7613a7984ea305e0432b0" id="tgt34" class="tgtSentence">A partir de la línea de base de identidad, el administrador de TI puede usar <newTerm>Microsoft Intune</newTerm> para asegurarse de que los dispositivos móviles se inscriben, administran y cumplen con las directivas corporativas.</caps:sentence>
            <caps:sentence sentenceid="534c353f372f40af02b154033f971daa" id="tgt35" class="tgtSentence"> Esta es la <embeddedLabel>capa de dispositivo</embeddedLabel>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="edbef2fba4f98afab9980b96cf2cd285" id="tgt36" class="tgtSentence">La tercera capa es la <embeddedLabel>capa de administración de aplicaciones</embeddedLabel>, con el ecosistema de aplicaciones administradas con Intune.</caps:sentence>
            <caps:sentence sentenceid="2ee1bba626f7c4d8a546afa223b7c885" id="tgt37" class="tgtSentence"> Este ecosistema, al tiempo que permite a los usuarios ser productivos y usar las herramientas que necesitan y conocen, como Office, también permite al departamento de TI mantener los datos confidenciales dentro del ecosistema de aplicaciones administradas.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d88ced107e08458d5576333c1027a86c" id="tgt38" class="tgtSentence">
              <newTerm>Azure Rights Management (Azure RMS)</newTerm> completa el modelo de seguridad al proteger los datos en el nivel de archivo.</caps:sentence>
            <caps:sentence sentenceid="8dad2717fa1635f4b14d24cf3215e1ad" id="tgt39" class="tgtSentence"> Las directivas de seguridad que se aplican a los datos viajan con los datos, ayudan a proteger los datos en tránsito y en dispositivos, independientemente del dispositivo que se use para acceder a ellos.</caps:sentence>
            <caps:sentence sentenceid="534c353f372f40af02b154033f971daa" id="tgt40" class="tgtSentence"> Esta es la <embeddedLabel>capa de datos</embeddedLabel> del modelo de seguridad.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="416c627dedbf7e1473d86b0d4ff24db0" id="tgt41" class="tgtSentence">Protección de documentos y correos electrónicos corporativos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f9a160100ab5d851ede523fa9d1461e7" id="tgt42" class="tgtSentence">La protección del correo electrónico corporativo implica dos objetivos principales:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="deed045395cda77658414bc391e72d47" id="tgt43" class="tgtSentence">Permitir que solo los dispositivos que cumplan las normas accedan al correo de la empresa</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="1f75d7a558b81c9d99fe4b9802ab0cca" id="tgt44" class="tgtSentence">Protección del contenido del correo electrónico y los datos adjuntos</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="deed045395cda77658414bc391e72d47" id="tgt45" class="tgtSentence">Permitir que solo los dispositivos que cumplan las normas accedan al correo de la empresa</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="3bf90042ce4b9a529e4f1e887d09a606" id="tgt46" class="tgtSentence">Un paso importante para proteger los datos corporativos es restringir el acceso a los dispositivos que no utilizan una contraseña segura, sin jailbreak o sin cifrar.</caps:sentence>
                <caps:sentence sentenceid="bf4da267db4b68290f3ca7d3f75230c9" id="tgt47" class="tgtSentence"> Microsoft Intune ofrece la capacidad de establecer las condiciones que los usuarios deben cumplir para obtener acceso a los recursos de la empresa.</caps:sentence>
                <caps:sentence sentenceid="798cb9159c21eac9037bddb37fa11fc3" id="tgt48" class="tgtSentence"> Esto se conoce como acceso condicional.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="83eda64e2f56b27060a9e5d375e6eef1" id="tgt49" class="tgtSentence">El acceso condicional viene determinado por dos tipos de directivas que se pueden definir en Intune:</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="ae4c629d87a29928e581fa8d01c52133" id="tgt50" class="tgtSentence">Las <embeddedLabel>directivas de cumplimiento</embeddedLabel> determinan el cumplimiento de un dispositivo.</caps:sentence>
                <caps:sentence sentenceid="fc5a02c9645c6de797a06dd909dde33d" id="tgt51" class="tgtSentence"> Evalúan la configuración y las condiciones, como:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="851d424cb7dc0541869e4a37aacf9e23" id="tgt52" class="tgtSentence">
                      <embeddedLabel>PIN y contraseñas</embeddedLabel>: el departamento de TI puede crear reglas, entre otras cosas, para solicitar contraseñas antes de desbloquear un dispositivo, para establecer la complejidad de la contraseña y la fecha de expiración.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2fe9578e401315b860d44ef5f0c46154" id="tgt53" class="tgtSentence">
                      <embeddedLabel>Cifrado</embeddedLabel>: el departamento de TI puede restringir el acceso a los dispositivos cifrados.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="15f901fb8191f6afed172517b10580cb" id="tgt54" class="tgtSentence">
                      <embeddedLabel>El dispositivo no está liberado o modificado</embeddedLabel>: Intune puede detectar si un dispositivo ha sido liberado mediante jailbreak, por lo que el departamento de TI puede establecer una directiva para bloquear el acceso a estos dispositivos.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="5c3be932160abeec9cf6d78bce3f2d39" id="tgt55" class="tgtSentence">
                  <embeddedLabel>Las directivas de acceso condicional</embeddedLabel> se configuran para un servicio determinado, como Exchange Online o SharePoint Online.</caps:sentence>
                <caps:sentence sentenceid="f3a976b13169a60fe6e74d582112c062" id="tgt56" class="tgtSentence"> Para cada servicio, puede definir a qué grupos de usuarios se deben aplicar estas directivas.</caps:sentence>
                <caps:sentence sentenceid="ab7b6178c1def173674778da8318a69b" id="tgt57" class="tgtSentence"> Por ejemplo, puede asegurarse de que todas las personas del departamento de finanzas solo puedan acceder al correo electrónico de la empresa desde dispositivos inscritos y de conformidad.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="f5ab5d92aa701fb0fb7856ee49fdc844" id="tgt58" class="tgtSentence">Mire <externalLink><linkText>este </linkText><linkUri>https://www.youtube.com/watch?feature=player_embedded&amp;v=lYx3YIezccg</linkUri></externalLink> vídeo de cuatro minutos para ver cómo afecta el acceso condicional a los usuarios finales.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="80ada9420149038e90410c5eede50aeb" id="tgt59" class="tgtSentence">Por qué importa la arquitectura</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="77303ce09ee311bf4213f63c6cb1f8f6" id="tgt60" class="tgtSentence">Los diferentes componentes de EMS y Office 365 se han creado y diseñado para ejecutarse en la nube.</caps:sentence>
            <caps:sentence sentenceid="e6ae3fa12481ac2df69d2914c52df8d3" id="tgt61" class="tgtSentence"> Esto aporta todas las ventajas que ofrece la nube: escalabilidad, flexibilidad y facilidad de administración.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="16f36128a0b198a34685af126a7c3796" id="tgt62" class="tgtSentence">Dado que las empresas diferentes tienen requisitos diferentes, EMS se ha diseñado para integrarse con la infraestructura local existente, como Active Directory, Exchange Server o System Center Configuration Manager.</caps:sentence>
            <caps:sentence sentenceid="243c3c93c8394b4915b65915936da3f7" id="tgt63" class="tgtSentence"> Esto le permite usar las credenciales ya establecidas en la red para los recursos locales y en la nube.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="bcc5f7c2be3d8b74355865ed31663011" id="tgt64" class="tgtSentence">En las secciones siguientes se describe la arquitectura diseñada para ejecutarse en la nube y se describe brevemente la opción local.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="c2f4ae8ae0b1e6172896ee8f85338b34" id="tgt65" class="tgtSentence">Flujo de acceso a correo electrónico</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="21fa67835693b08c58d3b14620ac624d" id="tgt66" class="tgtSentence">En función del tipo de aplicación de correo electrónico que utilice para acceder a a Exchange Online, la ruta para establecer un acceso seguro al correo electrónico puede ser ligeramente diferente.</caps:sentence>
                <caps:sentence sentenceid="443f6cc2cbec41792cd45e590a2da726" id="tgt67" class="tgtSentence"> Sin embargo, la de los componentes clave Azure Active Directory (Azure AD), Office 365/Exchange Online y Microsoft Intune, es la misma.</caps:sentence>
                <caps:sentence sentenceid="b57405df90e0271d3c1cf5ba93faaf6d" id="tgt68" class="tgtSentence"> La experiencia en TI y la experiencia del usuario final también son similares.</caps:sentence>
                <caps:sentence sentenceid="6a2e6d2840b5527237fc211e7dc3b58d" id="tgt69" class="tgtSentence"> Actualmente, EMS admite aplicaciones de correo electrónico nativas y la aplicación de Microsoft Outlook para iOS y Android.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="af19167672d3b1743dabfae636becd06" id="tgt70" class="tgtSentence">Flujo de control de acceso para las aplicaciones de correo electrónico nativas</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="ab44b62176c0b90fae746679bd5086dc" id="tgt71" class="tgtSentence">Los clientes de Exchange ActiveSync (EAS) que intentan acceder al correo electrónico de Exchange Online se evaluarán respecto a las siguientes propiedades:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="726b511de836521d4f265f6dc16b4249" id="tgt72" class="tgtSentence">¿El dispositivo se administra mediante Intune?</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="28bdf483505fa9447fbfa51d6ec8bc0f" id="tgt73" class="tgtSentence">¿El dispositivo está registrado con Azure Active Directory?</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fdc8a3a80e8fda23f626abd9014f363e" id="tgt74" class="tgtSentence">¿Cumple las normas el dispositivo?</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8760d91623907ee0d12ff677c8a387d4" id="tgt75" class="tgtSentence">¿Está el Id. de EAS de cliente asignado a un dispositivo registrado?</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="159dd496e73d6d8cc2aa0e3362c89e60" id="tgt76" class="tgtSentence">Para llegar a un estado de cumplimiento, el dispositivo en el que se ejecuta el cliente EAS debe:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e843b22db9f2581251d099824000ee72" id="tgt77" class="tgtSentence">Inscribirse con Intune</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8f4f34370c02ef87de2e50c5cb096f8d" id="tgt78" class="tgtSentence">Registrarse con <externalLink><linkText>Azure Active Directory</linkText><linkUri>https://msdn.microsoft.com/en-us/6a14cb1f-a058-4453-8ede-d9f4a66a7073.aspx</linkUri></externalLink> y</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="6f26e62fbe5db60566bf221f855e8ca6" id="tgt79" class="tgtSentence">Cumplir las directivas de dispositivo que ha establecido el administrador de TI.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="8d5b3f7d80a3a403080534c9dbd1e104" id="tgt80" class="tgtSentence">En la mayoría de plataformas, el registro del dispositivos en Azure Active Directory se hace automáticamente durante la inscripción</caps:sentence>
                <caps:sentence sentenceid="6d404f4da91f5086beba31cba8ca012b" id="tgt81" class="tgtSentence"> Intune anota los estados de dispositivo en Azure Active Directory y Exchange Online los lee la próxima vez que el cliente EAS intenta obtener correo electrónico.</caps:sentence>
                <caps:sentence sentenceid="fef20f03c75dc1b39d4eed5a70cb61f1" id="tgt82" class="tgtSentence"> Si el dispositivo no está registrado, el usuario recibirá un mensaje en su bandeja de entrada con instrucciones para registrarse (o inscribirse).</caps:sentence>
                <caps:sentence sentenceid="eac42f608f3d16a28ec9402ef67ee869" id="tgt83" class="tgtSentence"> Si el dispositivo no cumple las normas, el usuario obtendrá un correo electrónico diferente que le redirigirá al portal web de Intune, donde podrá obtener más información sobre el problema de cumplimiento y la forma de corregirlo.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="2d4e540c84f2675eb6b128d5e5afe25e" id="tgt84" class="tgtSentence">
                  <embeddedLabel>Azure AD</embeddedLabel> autentica el usuario y el dispositivo, Microsoft Intune administra las directivas de cumplimiento y acceso condicional y <embeddedLabel>Exchange Online</embeddedLabel> administra el acceso al correo electrónico en función del estado del dispositivo.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="35424911-894f-40fe-b4a9-12dfe03e4301"></image>
              </mediaLink>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="27e77308c87a2eb5da6a3fe05649e3fe" id="tgt85" class="tgtSentence">Flujo de control de acceso para aplicaciones de Outlook</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="22249e3db1943c13a13ba053d1c7f4c0" id="tgt86" class="tgtSentence">De forma similar al cliente EAS, la aplicación de correo electrónico de Outlook que intente tener acceso al correo electrónico de Exchange Online se evaluará respecto a las siguientes propiedades:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="726b511de836521d4f265f6dc16b4249" id="tgt87" class="tgtSentence">¿El dispositivo se administra mediante Intune?</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="28bdf483505fa9447fbfa51d6ec8bc0f" id="tgt88" class="tgtSentence">¿El dispositivo está registrado con Azure Active Directory?</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fdc8a3a80e8fda23f626abd9014f363e" id="tgt89" class="tgtSentence">¿Cumple las normas el dispositivo?</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="78d202f57d7f15626f802d6a14f48869" id="tgt90" class="tgtSentence">El cumplimiento del dispositivo se establece en gran parte de la misma manera que se describe en el flujo de control de acceso de cliente de EAS.</caps:sentence>
                <caps:sentence sentenceid="97499fedfd11e0562573932cbde64d48" id="tgt91" class="tgtSentence"> Sin embargo, para las aplicaciones de Outlook, el flujo entre los componentes es ligeramente diferente.</caps:sentence>
                <caps:sentence sentenceid="8ca78f3ff8235ea8cd99c3e93b8f3d7f" id="tgt92" class="tgtSentence"> Cuando la aplicación de Outlook intenta recibir correo electrónico, se redirige a Azure AD.</caps:sentence>
                <caps:sentence sentenceid="c9e3f8d57476a24233bbbaa0d1c13e41" id="tgt93" class="tgtSentence"> Azure AD emite un token de seguridad si, según la evaluación, el dispositivo está inscrito y es compatible.</caps:sentence>
                <caps:sentence sentenceid="b06141263b383de50227d7311fbfce0f" id="tgt94" class="tgtSentence"> A continuación, el token de seguridad se usa para obtener el correo electrónico corporativo de Exchange Online.</caps:sentence>
                <caps:sentence sentenceid="773cd0fe486f804034840860016b4ddf" id="tgt95" class="tgtSentence"> La sincronización de correo electrónico pasa por el servicio en la nube de Outlook, que recibe un token de acceso al servicio de EAS en nombre del usuario para completar la autenticación y entrega el correo electrónico.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="c9b751b8-bf07-49f5-aaa3-4a32da9d70b4"></image>
              </mediaLink>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="f79a70e259cf39c1194faf4a6a10bbf3" id="tgt96" class="tgtSentence">La experiencia de administración de TI:</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="ad9203459e7b749e4dbf4a8985999a63" id="tgt97" class="tgtSentence">No se necesita ninguna instalación compleja de infraestructura para Azure AD o Exchange.</caps:sentence>
                <caps:sentence sentenceid="1fdcea03273e312fb4373859d6355e92" id="tgt98" class="tgtSentence"> Los administradores de TI:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="245d77152fa5be93c056145bf6e3e6b0" id="tgt99" class="tgtSentence">Configure e implemente las directivas de cumplimiento que se usan para evaluar el estado de cumplimiento del dispositivo.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="422355cb3bdaa47c10fe599953fe3cfc" id="tgt100" class="tgtSentence">Configure la directiva de acceso condicional de Exchange Online y especifique qué grupos de seguridad de Azure AD se verán afectados por estas directivas y cuáles estarán exentos.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fec43a3b1d9381f00c749e7a8d2af747" id="tgt101" class="tgtSentence">Elija permitir o bloquear los dispositivos que no puedan inscribirse en Intune.</caps:sentence>
                    <caps:sentence sentenceid="7001c3b21206b5280f9e3ce4dac99b0d" id="tgt102" class="tgtSentence"> La lista de sistemas operativos compatibles para dispositivos móviles se muestra más adelante.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="ebd36635c76796fba333eeed9a427de9" id="tgt103" class="tgtSentence">Hay una fase de configuración opcional que puede ser necesaria.</caps:sentence>
                <caps:sentence sentenceid="c57990f1cb9b7135bfd63ffbf3f92736" id="tgt104" class="tgtSentence"> Los informes que se utilizan para administrar y supervisar el estado y el acceso a los dispositivos requieren la configuración del conector de servicio a servicio de Microsoft Intune.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="f3fdaf52f5d2d440952bde05202cff1c" id="tgt105" class="tgtSentence">Experiencia del usuario final:</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="dff7b49d5d251a1af9815785dcbcf9d5" id="tgt106" class="tgtSentence">Cuando el usuario intenta tener acceso al correo electrónico en el dispositivo por primera vez o sincronizar posteriormente, se comprueba el estado de cumplimiento de normas y la inscripción del dispositivo.</caps:sentence>
                <caps:sentence sentenceid="4dc93c1aeb1901adeaaf48d175b0d0e8" id="tgt107" class="tgtSentence"> El proceso de inscripción o corrección de problemas de cumplimiento de normas es una experiencia guiada.</caps:sentence>
                <caps:sentence sentenceid="1b15ba870316ed3cbdb9087984f1d49b" id="tgt108" class="tgtSentence"> Se muestran al usuario final los pasos necesarios para inscribir su dispositivo y que esté conforme con las normas sin necesidad de llamar al servicio de asistencia de TI:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="20a5a7a4368a924a7f5fe7d7576a253a" id="tgt109" class="tgtSentence">
                      <embeddedLabel>Si el dispositivo no está inscrito</embeddedLabel>, la página de inicio de sesión mostrará el acceso denegado y solicitará la inscripción.</caps:sentence>
                    <caps:sentence sentenceid="972706304b7c6278bd70bffa6dc3be5b" id="tgt110" class="tgtSentence"> En la inscripción, el dispositivo se registra automáticamente en Azure Active Directory.</caps:sentence>
                    <caps:sentence sentenceid="eef8b5aff7bf5d7c8862702303c099f4" id="tgt111" class="tgtSentence"> Intune comprueba el cumplimiento de normas del dispositivo y proporciona los pasos de corrección para solucionar los problemas de incumplimiento.</caps:sentence>
                    <caps:sentence sentenceid="4f2bcc313dbf938e1ea45e0e81adc4e2" id="tgt112" class="tgtSentence"> Una vez que el dispositivo cumple las normas, Intune establece el estado de cumplimiento del dispositivo con Azure Active Directory.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f738338632edf67dccd5f229d869117c" id="tgt113" class="tgtSentence">
                      <embeddedLabel>Si el dispositivo está inscrito, pero no cumple las normas</embeddedLabel>, se envía un vínculo con los pasos para solucionar los problemas al dispositivo.</caps:sentence>
                    <caps:sentence sentenceid="6cf208330c96228b5953aa0d3399f2cc" id="tgt114" class="tgtSentence"> Cuando el usuario final corrige el problema (por ejemplo, define la contraseña, cifrado), Intune, que administra las directivas de cumplimiento, actualiza el estado de cumplimiento del dispositivo en Azure AD.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="07bf8af13bdd39479cbb5fa4444e28ea" id="tgt115" class="tgtSentence">Una vez que el dispositivo se evalúa como inscrito y conforme a las normas, la sincronización de correo electrónico debe realizarse en pocos minutos.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0740dc7cfbe0822007389aab84099d80" id="tgt116" class="tgtSentence">Impedir el filtrado de datos de correo electrónico y datos adjuntos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1b0ce60826b23a4187666bb59e5f6516" id="tgt117" class="tgtSentence">En la sección anterior se describe cómo puede asegurarse de que solo los dispositivos compatibles puedan acceder al correo electrónico corporativo.</caps:sentence>
            <caps:sentence sentenceid="707920fb69ae24f3bd9978cdebf94904" id="tgt118" class="tgtSentence"> Sin embargo, el contenido del correo electrónico y los datos adjuntos no está protegido al proteger el acceso.</caps:sentence>
            <caps:sentence sentenceid="d3d74209ccc915bc6bb62fd5e0684d68" id="tgt119" class="tgtSentence"> El contenido se puede copiar, mover, guardar en una ubicación diferente o compartir con otro usuario.</caps:sentence>
            <caps:sentence sentenceid="9835bbb79113e3ee250d892c5310393c" id="tgt120" class="tgtSentence"> EMS soluciona este problema mediante directivas de administración de aplicaciones móviles.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="dc181b148f8f9c142e80476583bca4e1" id="tgt121" class="tgtSentence">Las aplicaciones administradas son aplicaciones que implementa el Administrador de TI que cumplen los requisitos de seguridad de las empresas.</caps:sentence>
            <caps:sentence sentenceid="8fb656726fae94b84b57fbfb27c483f3" id="tgt122" class="tgtSentence"> Con estas aplicaciones, el departamento de TI tiene control directo sobre la implementación, la administración continua, como el inventario o las actualizaciones, y la eliminación selectiva de las aplicaciones y los datos asociados.</caps:sentence>
            <caps:sentence sentenceid="779925cf11613a4ca38715e78e34611d" id="tgt123" class="tgtSentence"> Además, a través de un conjunto de directivas de administración de aplicaciones móviles (MAM), Intune permite modificar la funcionalidad de las aplicaciones y restringir la compartición de datos, como:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="43914702c3d0f940c0c40e216ad1d915" id="tgt124" class="tgtSentence">Copiar y pegar en bloque o impedir la transferencia de datos desde una aplicación administrada a una aplicación sin directiva MAM.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="73593b7e9303e76c9b21d7fcec32760a" id="tgt125" class="tgtSentence">Evitar la copia de seguridad en el almacenamiento en nube personal, la opción Guardar como, etc..</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e693c0410514f58659694030dda60c2c" id="tgt126" class="tgtSentence">Proteger el acceso a la aplicación al requerir el PIN o código de acceso o credenciales corporativas en una aplicación protegida con MAM.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3ac920308f672e7c0c5f10f547c73c30" id="tgt127" class="tgtSentence">Configurar la aplicación para que abra todos los vínculos web dentro del explorador administrado de Intune.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5f2205800a19abf647d005d8eaaed527" id="tgt128" class="tgtSentence">Borrar selectivamente solo los datos asociados con la aplicación administrada.</caps:sentence>
                <caps:sentence sentenceid="bf229e0ee1d5962dfe912f95bab41704" id="tgt129" class="tgtSentence"> Cuando un dispositivo se pierde o roba, o ya no lo administra el departamento de TI, una eliminación selectiva puede quitar todos los datos corporativos de las aplicaciones, dejando sólo los datos personales de la aplicación.</caps:sentence>
                <caps:sentence sentenceid="f7fe5aa4e1a9d2bfcfbbb98d4b867548" id="tgt130" class="tgtSentence"> Esto se conoce como multiidentidad.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="fbcdf0a327a2ea84d2819abb16a78018" id="tgt131" class="tgtSentence">Con <externalLink><linkText>Azure Rights Management Services</linkText><linkUri>https://technet.microsoft.com/en-us/library/jj585026.aspx</linkUri></externalLink>, puede ampliar la protección de correo electrónico de las maneras siguientes:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="1c8cd4af17a76ee5df94716bd676f262" id="tgt132" class="tgtSentence">Los mensajes de correo electrónico pueden cifrarse de manera que solo los usuarios deseados puedan leer o ver el contenido dentro o fuera de la empresa.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5c297802d3024c802ba60cc48126ee13" id="tgt133" class="tgtSentence">Los usuarios pueden proteger los mensajes de correo electrónico y el destinatario puede leer y utilizar los mensajes de correo electrónico protegidos que se le envían.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="98d513f543fbb2eec9f837896166e067" id="tgt134" class="tgtSentence">Un administrador puede establecer reglas para:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="73dc8319de5e0af72d10ac00f1d35afa" id="tgt135" class="tgtSentence">Aplicar las reglas automáticamente a un grupo específico de destinatarios o crear plantillas para departamentos concretos.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3402f8fce8244e38ec8e52a4e984c553" id="tgt136" class="tgtSentence">Detectar y aplicar reglas a los mensajes de correo electrónico con contenido confidencial automáticamente.</caps:sentence>
                    <caps:sentence sentenceid="4f5065b575a06e99e1dde3c12d6b9784" id="tgt137" class="tgtSentence"> La regla puede basarse en el remitente, destinatario, asunto del mensaje o contenido.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4823f9ae9455b8b8356349f24d786755" id="tgt138" class="tgtSentence">Detectar contenido confidencial y avisar al remitente para que aplique las reglas de protección antes de enviar el correo electrónico.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="5d98d5a8363d48a4d46baa4d570b01a2" id="tgt139" class="tgtSentence">Componentes de aplicaciones administradas</caps:sentence>
            </title>
            <content>
              <para></para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cda7d84c943c56938eadbe7d40ebfee0" id="tgt140" class="tgtSentence">
                      <embeddedLabel>Microsoft Intune</embeddedLabel> es el sitio donde se configuran las directivas, se asocian con la aplicación o se usa la herramienta de ajuste de aplicaciones para permitir que una aplicación interna use directivas de administración de aplicaciones móviles.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3dd5d8b06c4fe91bc32744512024c591" id="tgt141" class="tgtSentence">El <embeddedLabel>Portal de empresa</embeddedLabel> es una aplicación que se ejecuta de forma nativa en cada dispositivo o está basada en el explorador.</caps:sentence>
                    <caps:sentence sentenceid="4e8e6943851c5bb5c7346bdf3431b28e" id="tgt142" class="tgtSentence"> El departamento de TI implementa las aplicaciones administradas para los usuarios o dispositivos, y los usuarios finales pueden instalar la aplicación desde el portal.</caps:sentence>
                    <caps:sentence sentenceid="d5151632d3a2cbb27b7b1675e2653467" id="tgt143" class="tgtSentence"> Las directivas asociadas con las aplicaciones se transfieren al dispositivo con las aplicaciones.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <mediaLink>
                <image xlink:href="e1bc9e16-eb2c-4f1a-a4be-e8b44cc1ba23"></image>
              </mediaLink>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="f79a70e259cf39c1194faf4a6a10bbf3" id="tgt144" class="tgtSentence">La experiencia de administración de TI:</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="8581ce61e7bcf386776af2039b0852e1" id="tgt145" class="tgtSentence">El Administrador de TI crea las directivas de administración de aplicaciones móviles, asocia la directiva a la aplicación y distribuye a los usuarios o dispositivos.</caps:sentence>
                <caps:sentence sentenceid="772769573491ba965de1012c47da771d" id="tgt146" class="tgtSentence"> Cuando la aplicación administrada se instala en el dispositivo, se aplican las restricciones de la aplicación.</caps:sentence>
                <caps:sentence sentenceid="88dd617f35c2168c9731bdfd92ba1ba5" id="tgt147" class="tgtSentence"> Crear e implementar aplicaciones administradas supone poco o ningún esfuerzo adicional:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ccadadcaced041ca931644f6ea20972b" id="tgt148" class="tgtSentence">Hay aplicaciones existentes que ya tienen el SDK de aplicación que permite aplicar restricciones a la aplicación.</caps:sentence>
                    <caps:sentence sentenceid="d090c8e009ee8bc3344f09c1c0bda400" id="tgt149" class="tgtSentence"> No requieren ningún otro procesamiento: basta con agregar un vínculo a una tienda de aplicaciones, como iTunes o Google Play.</caps:sentence>
                    <caps:sentence sentenceid="d518e016db556c36e4c0a260fce04e61" id="tgt150" class="tgtSentence"> Lea <externalLink><linkText>este</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn708489.aspx</linkUri></externalLink> artículo para ver la lista de aplicaciones administradas.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b5a58704cbae86435af3c35d4c30b8cb" id="tgt151" class="tgtSentence">Si quiere administrar las aplicaciones creadas internamente, puede volver a empaquetar las aplicaciones con la herramienta de ajuste de aplicaciones de Microsoft Intune.</caps:sentence>
                    <caps:sentence sentenceid="f063d30c0a2402c6aad00d90ab44af43" id="tgt152" class="tgtSentence"> La herramienta vuelve a empaquetar la aplicación, lo que le permite aplicar restricciones a la aplicación.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="2d324bbb22663bffbe93b068ec3d6566" id="tgt153" class="tgtSentence">Experiencia del usuario final</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="df9a3fc04ca63d82e1d48e2df7f054ab" id="tgt154" class="tgtSentence">Los usuarios finales pueden instalar aplicaciones administradas y usarlas para hacer su trabajo.</caps:sentence>
                <caps:sentence sentenceid="edacdc6c7d17b6aaa8e3a3a0cbadf51c" id="tgt155" class="tgtSentence"> Sólo podrán mover o compartir datos entre aplicaciones administradas.</caps:sentence>
                <caps:sentence sentenceid="33a80bf544b1628fe897a5955d8a80cb" id="tgt156" class="tgtSentence"> Se bloqueará cualquier intento de mover datos fuera del ecosistema de aplicaciones administradas.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="89704e5edf5d1d828ff8449b9d2b4d76" id="tgt157" class="tgtSentence">Operaciones y respuesta a incidencias</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="4bda8667916b7067859bd03efe20b4af" id="tgt158" class="tgtSentence">Una vez implementada la solución, debe administrar el entorno e identificar posibles riesgos de seguridad.</caps:sentence>
            <caps:sentence sentenceid="14b319ab8f709b0e17005d82c69ab316" id="tgt159" class="tgtSentence"> Intune y Azure AD tienen funciones de supervisión y notificación que pueden ayudar a supervisar y responder rápidamente en caso de incidentes de seguridad.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="47bad6f115e5077a305d7fde9852fd80" id="tgt160" class="tgtSentence">Estas son algunas de las funciones de notificación:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="5b1eabfdeada8c84f9a16c7de9fd9e06" id="tgt161" class="tgtSentence">Las alertas e informes de Intune le ayudarán a supervisar el estado de los dispositivos que administra Intune.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="25bdfaf50cd33a43e5ef2a3bfe36a500" id="tgt162" class="tgtSentence">Azure AD tiene registros de actividades y auditoría.</caps:sentence>
                <caps:sentence sentenceid="8641bff5abd13773ac0d87ea7b3f753a" id="tgt163" class="tgtSentence"> Puede supervisar elementos tales como cambios de contraseña y administración de usuarios.</caps:sentence>
                <caps:sentence sentenceid="244b8d5ae36affb0f656724c2bf3e095" id="tgt164" class="tgtSentence"> Azure Active Directory premium incluye alertas e informes de seguridad de anomalías avanzados.</caps:sentence>
                <caps:sentence sentenceid="9586f751f4827d26267e9f9d2ec359b0" id="tgt165" class="tgtSentence"> Estas alertas se basan en informes de aprendizaje automático detallados que muestran la actividad de inicio de sesión, los patrones de acceso incoherentes y las áreas de amenazas potenciales.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="e7ee64d8fba4de5bf6908be93d12d164" id="tgt166" class="tgtSentence">Implementación local</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="95e155143ddcd9f01f03f56ab3103f42" id="tgt167" class="tgtSentence">Si tiene una implementación existente de System Center Configuration Manager, Active Directory o Exchange Server, puede ampliar la infraestructura existente mediante la integración con Intune, Azure AD y Office 365.</caps:sentence>
            <caps:sentence sentenceid="ac440ab2ef01b22f74ea7f3c0b4e92eb" id="tgt168" class="tgtSentence"> Con esta implementación híbrida, puede proporcionar una experiencia de administración coherente entre dispositivos locales y en la nube.</caps:sentence>
            <caps:sentence sentenceid="e3d61cb3334eeb87f28a6bb3d443b161" id="tgt169" class="tgtSentence"> Intune y el Administrador de configuración ofrecen un conjunto similar de funciones para permitir el acceso restringido al correo electrónico en función del estado del dispositivo.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="01a59f6fc3873a8890ba78a059e6a00a" id="tgt170" class="tgtSentence">Para implementaciones de Exchange Online dedicadas, si puede aprovechar la solución en la nube descrita anteriormente o la implementación híbrida depende del aspecto de la implementación actual.</caps:sentence>
            <caps:sentence sentenceid="780ec58335d641bf57a7e5bdcbf66d76" id="tgt171" class="tgtSentence"> Hable con su equipo de cuentas para determinar qué implicará la implementación.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="90241ca36c95a855d6b5bd27d4fe7392" id="tgt172" class="tgtSentence">¿Qué debe considerar al planear la implementación?</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="20c797104d4278d2bfd8612606a180a7" id="tgt173" class="tgtSentence">
                  <embeddedLabel>Compatibilidad con las plataformas de los dispositivos</embeddedLabel>: debe tener en cuenta si desea permitir el acceso al correo electrónico a aquellas plataformas que no son compatibles con Intune.</caps:sentence>
                <caps:sentence sentenceid="28656abed275ec3f3a6266e670fe1dd6" id="tgt174" class="tgtSentence"> La administración de dispositivos móviles de Intune admite los siguientes sistemas operativos:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a3511abc90618bc6d35f7a71425a6e3e" id="tgt175" class="tgtSentence">Apple iOS 7.1 y versiones posteriores (los dispositivos iOS 6.0 y 7.0 inscritos previamente permanecen inscritos, pero no se pueden inscribir nuevos dispositivos)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d16e657c04cd12d8a04e538710560ab4" id="tgt176" class="tgtSentence">Google Android 2.3.4 y versiones posteriores (incluye Samsung KNOX)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a264b63b4e15361c5e6943720038b717" id="tgt177" class="tgtSentence">Windows Phone 8.0 y versiones posteriores</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e31a7837d2f01d9d75564c2e39e7fe8e" id="tgt178" class="tgtSentence">Windows RT y versiones posteriores</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ea6e3e669e53ae0ba64b49bd34d52525" id="tgt179" class="tgtSentence">Equipos de Windows 8.1 y versiones posteriores</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="23173f6329941f93fa932ecaf2e3af24" id="tgt180" class="tgtSentence">
                  <embeddedLabel>Tipos de aplicaciones de correo electrónico</embeddedLabel>: la solución de EMS admite actualmente clientes que usan el protocolo EAS y aplicaciones de Outlook (anteriormente, Accompli en iOS y Android).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f0cec831baea833a327356782c9d9eaf" id="tgt181" class="tgtSentence">
                  <embeddedLabel>Directivas</embeddedLabel>: la solución de EMS y sus componentes tienen varias directivas que se usan para administrar la seguridad y el acceso.</caps:sentence>
                <caps:sentence sentenceid="6cfb533ff4cc77c72f9804677b008d13" id="tgt182" class="tgtSentence"> Determine qué directivas debe configurar el Administrador de TI.</caps:sentence>
                <caps:sentence sentenceid="a0c131bea5b933b81535449abd9e567c" id="tgt183" class="tgtSentence"> Las tres directivas clave que se usarán para la investigación y planificación al proteger el acceso al correo electrónico y los datos de correo electrónico son:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e72f19ecd7297e3f0c5433446926a918" id="tgt184" class="tgtSentence">
                      <embeddedLabel>Directivas de cumplimiento del dispositivo</embeddedLabel>: determine qué significa “cumplimiento” para su empresa.</caps:sentence>
                    <caps:sentence sentenceid="0924b18e380e9f7d726b37d03a2c99f4" id="tgt185" class="tgtSentence"> Intune incluye varias reglas que puede establecer, pero todas esas reglas pueden o no aplicarse a la empresa.</caps:sentence>
                    <caps:sentence sentenceid="7ef791d670a9e91fa46ecc02631be068" id="tgt186" class="tgtSentence"> Puede cambiar las directivas en cualquier momento, pero es recomendable determinar un conjunto básico de directivas para la empresa.</caps:sentence>
                    <caps:sentence sentenceid="865002b46b4374ddda21512cc491f344" id="tgt187" class="tgtSentence"> Las directivas de cumplimiento van dirigidas a grupos de dispositivos y de usuarios de Intune.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f081a8e7b9e608197566045cace73469" id="tgt188" class="tgtSentence">
                      <embeddedLabel>Directivas de acceso condicional</embeddedLabel>: las directivas de acceso condicional están dirigidas a grupos de seguridad de Azure AD.</caps:sentence>
                    <caps:sentence sentenceid="0fa2bf5ccb70a114367a5ead47ba4758" id="tgt189" class="tgtSentence"> Determine a qué usuarios se dirigirán las directivas y si hay usuarios que deben estar exentos.</caps:sentence>
                    <caps:sentence sentenceid="f4e0a7979c2addd4268d0f5840de7a30" id="tgt190" class="tgtSentence"> El acceso condicional es compatible con la solución basada en la nube y la implementación híbrida.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f4b8928dc447f063e742b3b9a7449867" id="tgt191" class="tgtSentence">
                      <embeddedLabel>Administración de aplicaciones móviles</embeddedLabel>: determine qué aplicaciones deben administrarse y qué directivas MAM se deben aplicar a estas aplicaciones.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ce845b25e83ea2863eaf43a3ec928343" id="tgt192" class="tgtSentence">
                  <embeddedLabel>Consideraciones sobre la administración de dispositivos</embeddedLabel>: seleccione la opción de administración de dispositivos que mejor satisfaga las necesidades de la empresa antes de implementar la solución.</caps:sentence>
                <caps:sentence sentenceid="88240c610c59d683235aa27289c08a8b" id="tgt193" class="tgtSentence"> Hay dos opciones: </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cc8ea19c60122cbde45e82ee25c3f678" id="tgt194" class="tgtSentence">Unificar System Center Configuration Manager con Microsoft Intune para administrar todos los dispositivos a través de una única consola.</caps:sentence>
                    <caps:sentence sentenceid="5f51874e251885d753a10cf3fdc98744" id="tgt195" class="tgtSentence"> Esto se denomina <newTerm>Implementación híbrida</newTerm>.</caps:sentence>
                    <caps:sentence sentenceid="0bf4ae229879cf514af7c5f5bbd2c068" id="tgt196" class="tgtSentence"> Ventajas de este enfoque:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="e4d76ded27a9ce0a0740dc675ce0afba" id="tgt197" class="tgtSentence">Una única consola de administración con controles de administración de derechos enriquecidos para administrar equipos locales y dispositivos móviles</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="46ff560cb5d67de83d001920258caefe" id="tgt198" class="tgtSentence">Amplias funciones de implementación y orientación</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="3793769a6811c2c957b68b4a4c90d7db" id="tgt199" class="tgtSentence">Gran escala para grandes empresas</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="0a815e32cb61d9dbfd97295737dc2cea" id="tgt200" class="tgtSentence">Administre los dispositivos móviles a través de Microsoft Intune independientemente de los dispositivos locales con System Center Configuration Manager.</caps:sentence>
                    <caps:sentence sentenceid="23762682030cf43ddbd29a9354e28089" id="tgt201" class="tgtSentence"> Esto se denomina <newTerm>Implementación independiente de Intune</newTerm>.</caps:sentence>
                    <caps:sentence sentenceid="0bf4ae229879cf514af7c5f5bbd2c068" id="tgt202" class="tgtSentence"> Ventajas de este enfoque:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8ee6d63f5dfe98124f8dc2e12c42398f" id="tgt203" class="tgtSentence">Consola basada en web sencilla diseñada específicamente para la administración de dispositivos móviles</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="cf2cc84b358e7a21b0c9aa8bfee989dd" id="tgt204" class="tgtSentence">Acceso rápido a las características más recientes</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="ac6a0c5bc57c875d4350fa3010f91884" id="tgt205" class="tgtSentence">Aunque la migración siempre es posible, es muy recomendable tomar esta decisión antes de la implementación, puesto que influirá en muchas de las decisiones del proceso de aplicación.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="853ae90f0351324bd73ea615e6487517" id="tgt206" class="tgtSentence">
                  <embeddedLabel>Entorno de Exchange</embeddedLabel>:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8e178fa955fa744e3340078c05748c93" id="tgt207" class="tgtSentence">La implementación de los conectores de Exchange y cómo se conectan cuando se implementan los equilibradores de carga de red.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="58271b7ec4baced9e8257dbd6662c20d" id="tgt208" class="tgtSentence">Exchange Online: ¿es multiempresa o dedicado?</caps:sentence>
                    <caps:sentence sentenceid="f3dd112a0fbc5ee25556e4ba526117fa" id="tgt209" class="tgtSentence"> Si es dedicado, averigüe en qué arquitectura se basa el inquilino.</caps:sentence>
                    <caps:sentence sentenceid="0a2b95d0b1594dcfc67fd9d41d55c471" id="tgt210" class="tgtSentence"> Esto determinará si se puede utilizar el acceso condicional basado en Azure AD o si se necesita un conector local.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="853ae90f0351324bd73ea615e6487517" id="tgt211" class="tgtSentence">
                  <embeddedLabel>Sincronización de Azure AD y Servicios federados de Active Directory (ADFS) u otro servicio federado de terceros</embeddedLabel>:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b191635df103e53d6d4c6c65b9425f28" id="tgt212" class="tgtSentence">El acceso condicional está diseñado para funcionar para los clientes que tengan federado su servicio de identidad con ADFS.</caps:sentence>
                    <caps:sentence sentenceid="69bc473322bb9bfe240a61dea432b891" id="tgt213" class="tgtSentence"> Generalmente, todavía se aplicarán las reglas de acceso de cliente, sin embargo, se recomienda que se realice una prueba completa.</caps:sentence>
                    <caps:sentence sentenceid="1d3638ebd3741695bc10d3c1568e44f4" id="tgt214" class="tgtSentence"> Los requisitos para la sincronización de directorios y ADFS no son diferentes de los de Office 365.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a2c462ec409073d78a47a28410754dae" id="tgt215" class="tgtSentence">Los servicios de federación de terceros, como Ping, también deberían funcionar.</caps:sentence>
                    <caps:sentence sentenceid="e5b3e903842ae0853dc56eb12e75e3f6" id="tgt216" class="tgtSentence"> Se recomienda realizar pruebas antes de la implementación.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="b1f5ed8724d5d94e5c71813dd450e352" id="tgt217" class="tgtSentence">Próximos pasos</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="90d50a94113b6593f29b711440456720" id="tgt218" class="tgtSentence">
              <externalLink>
                <linkText>Mire</linkText>
                <linkUri>https://www.youtube.com/watch?v=ltcZvm4VOFU</linkUri>
              </externalLink> este vídeo para obtener información sobre cómo registrarse para obtener una cuenta de prueba y comenzar.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f12a9e747e5118e11f8482e3ddcb3066" id="tgt219" class="tgtSentence">* IDC: "Worldwide Mobile Worker Population 2011 – 2015 Forecast"</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="02d0724f5b1851650d4502c00c6ffdf3" id="tgt220" class="tgtSentence">** Experian "informe de benchmark trimestrales mediante correo electrónico" (3T 2014)</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="08434dfb71c2048d30eb9d85b9f127ed" id="tgt221" class="tgtSentence">*** Forrester Research: "BT Futures Report: Info workers will erase boundary between enterprise &amp; consumer technologies," 21 de febrero, 2013</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="9a1207508a42a146b0fa279a7afb57bf" id="tgt222" class="tgtSentence">Arquitectura de EMS</caps:sentence>
          </linkText>
          <linkUri>https://azure.microsoft.com/en-us/documentation/infographics/enterprise-mobility/</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="75a56e8f3929bf1d395bfb37571fa815" id="tgt223" class="tgtSentence">Introducción al uso de Intune</caps:sentence>
          </linkText>
          <linkUri>https://technet.microsoft.com/en-us/library/dn646953.aspx</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="52a1301e281570437295651f0c64f273" id="tgt224" class="tgtSentence">Qué es Azure Active Directory</caps:sentence>
          </linkText>
          <linkUri>https://azure.microsoft.com/en-us/documentation/articles/active-directory-whatis/</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="003385f46b4b94501ddb271786cb0b50" id="tgt225" class="tgtSentence">¿Cómo admite Azure Active Directory Office 365, Microsoft Intune y otros servicios de Microsoft?</caps:sentence>
          </linkText>
          <linkUri>https://azure.microsoft.com/en-us/documentation/articles/active-directory-administer/#what-is-an-azure-ad-tenant</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="3df539f5fe98cbde100eceda37e5b423" id="tgt226" class="tgtSentence">¿Cómo ayuda Azure Active Directory a administrar identidades?</caps:sentence>
          </linkText>
          <linkUri>https://azure.microsoft.com/en-us/documentation/articles/active-directory-administer/</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="76ea09d2fbee23e1abe7c1e9590ab44c" id="tgt227" class="tgtSentence">¿Qué es Azure Rights Management?</caps:sentence>
          </linkText>
          <linkUri>https://technet.microsoft.com/en-us/library/jj585026.aspx</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="ea9028c667aa4307eaf2ea3ce9a559af" id="tgt228" class="tgtSentence">¿Cómo admiten las aplicaciones Azure Rights Management?</caps:sentence>
          </linkText>
          <linkUri>https://technet.microsoft.com/en-us/library/jj585004.aspx</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence sentenceid="176f8a817f61d6e2ba390208a55f965b" id="tgt229" class="tgtSentence">Protección automática de mensajes de correo electrónico con Exchange Online y directivas de prevención de pérdida de datos</caps:sentence>
          </linkText>
          <linkUri>https://technet.microsoft.com/en-us/library/jj585026.aspx#BKMK_Example_DLP</linkUri>
        </externalLink>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This topic starts with an overview of how you can provide data protection for your company while ensuring that the end-user experience is simple and does not impact productivity.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Then, we will focus specifically on how you can help provide secure access to your corporate email and help protect company data in email and attachments using the Microsoft Enterprise Mobility Suite solution.</caps:sentence>
        </para>
        <alert class="tip">
          <para>
            <caps:sentence id="src3" class="srcSentence">Get a downloadable copy of this entire topic  at the <externalLink><linkText>TechNet Gallery</linkText><linkUri>https://gallery.technet.microsoft.com/Managing-Access-and-Help-b7a05d0d/file/140056/1/Managing%20Access%20and%20Help%20Protect%20Corporate%20Email%20Data%20on%20Mobile%20Devices.pdf</linkUri></externalLink>.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src4" class="srcSentence">Balancing productivity and security</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Employees want to be able to use their own devices to access company resources and productivity tools.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> IT needs to make sure that employees have this ability but sensitive company data is protected.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> BYOD, or <externalLink><linkText>Bring your own device</linkText><linkUri>https://technet.microsoft.com/en-us/library/Dn656905(l=en-us,v=WS.11).aspx</linkUri></externalLink>, poses a specific challenge in that there needs to be a separation of personal and work data on personal devices and prevent intentional or unintentional sharing of company data.</caps:sentence>
          </para>
          <para>
            <embeddedLabel>
              <caps:sentence id="src8" class="srcSentence">Studies show that:</caps:sentence>
            </embeddedLabel>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">37% of the world’s workforce is mobile*</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">53% of total email opens occurred on a mobile phone or tablet in Q3 2014**</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">61% of workers mix personal and work tasks in their devices***</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src12" class="srcSentence">Consider this:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">Email is often the most used application on any device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">Content in email and email attachments can be copied, shared, or moved to other locations outside of your IT department purview, which can lead to compromising your company's security.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src15" class="srcSentence">Since end-users want to do company work using their own personal devices and email is the most often accessed application, the first step for your IT is to make sure that end-users can access corporate email on their devices while making sure that sensitive data in email is not compromised.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Overview</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">Microsoft offers the Enterprise Mobility Suite (EMS), a comprehensive solution for identity, mobile device management, app management, and data protection.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> EMS provides a layered security model which allows your IT department to manage access to email, data, and corporate applications from almost any device.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src19" class="srcSentence">EMS is composed of the following cloud services:</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="2c5f1cb4-2880-4efa-ae38-d4963d9f1345"></image>
          </mediaLink>
          <para>
            <caps:sentence id="src20" class="srcSentence">Using EMS, data is protected both inside and outside of your corporate network:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src21" class="srcSentence">Employees have access to corporate email, work-related applications, and company data on the device of their choice without worrying about compromising sensitive company information.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">Company data is protected at every level: user, device, application and finally, at the level of the data itself.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src23" class="srcSentence">Your IT admin can make sure that corporate data is accessed only by trusted users on managed and compliant devices, and in the context of managed applications.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src24" class="srcSentence">Intune-managed apps include Office mobile apps, which are central to this solution.</caps:sentence>
            <caps:sentence id="src25" class="srcSentence"> With Office mobile apps, you can help maximize employee productivity while preventing data leakage.</caps:sentence>
            <caps:sentence id="src26" class="srcSentence"> For example, your IT admin can set policies that prevent copying company data to personal cloud storage like Dropbox.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src27" class="srcSentence">When employees move or change jobs, or lose their device, EMS provides the option to remotely and selectively wipe corporate data from the device.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> This can be done by the end-user or by your IT admin.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src29" class="srcSentence">How EMS can help protect your data</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src30" class="srcSentence">The 4 layered security model for identity, devices, apps, and data is about making sure that your company resources are only accessed by the intended user, on a device that meets a set of compliance policies configured by you, and within the boundaries of managed apps.</caps:sentence>
          </para>
          <mediaLink>
            <image xlink:href="ec85aa6d-b075-4c92-92fc-dc8e467eaa23"></image>
          </mediaLink>
          <para>
            <caps:sentence id="src31" class="srcSentence">Protecting your data starts with establishing and validating the user identity.</caps:sentence>
            <caps:sentence id="src32" class="srcSentence">
              <newTerm>Azure AD/</newTerm>, an enterprise-grade identity and access management tool delivers single sign-on, multi-factor authentication, self-service passwords, and more.</caps:sentence>
            <caps:sentence id="src33" class="srcSentence"> It provides the functionality for the <embeddedLabel>identity layer</embeddedLabel> of the security model.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src34" class="srcSentence">Building on the identity baseline, your IT admin can use <newTerm>Microsoft Intune</newTerm> to make sure that mobile devices are enrolled, managed and compliant with your corporate policies.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> This is the <embeddedLabel>device layer</embeddedLabel>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src36" class="srcSentence">The third layer is the <embeddedLabel>app management layer</embeddedLabel> with the Intune-managed app ecosystem.</caps:sentence>
            <caps:sentence id="src37" class="srcSentence"> This ecosystem, while enabling users to be productive and use the tools that they need and know like Office, also enables your IT to keep sensitive data within the managed app ecosystem.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src38" class="srcSentence">
              <newTerm>Azure Rights Management (Azure RMS)</newTerm> completes the security model by protecting data at the file level.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence"> The security policies that are applied to the data, travel with the data, help keep the data secure in transit and at rest, regardless of the device that is used to access it.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> This is the <embeddedLabel>data layer</embeddedLabel> of the security model.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src41" class="srcSentence">Protecting coporate email and documents</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src42" class="srcSentence">Protecting corporate email involves two main objectives:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src43" class="srcSentence">Allow only compliant devices to access your company’s email</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src44" class="srcSentence">Protecting the content in email and attachments</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src45" class="srcSentence">Allow only compliant devices to access your company’s email</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src46" class="srcSentence">An important step to protecting corporate data is restricting access to devices that don’t use a strong password, are not jailbroken, or not encrypted.</caps:sentence>
                <caps:sentence id="src47" class="srcSentence"> Microsoft Intune gives you the ability to set conditions that your users have to meet to gain access to your company resources.</caps:sentence>
                <caps:sentence id="src48" class="srcSentence"> This is known as conditional access.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src49" class="srcSentence">Conditional access is determined by two types of policies you can set in Intune:</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src50" class="srcSentence">
                  <embeddedLabel>Compliance policies</embeddedLabel> determine the compliance of a device.</caps:sentence>
                <caps:sentence id="src51" class="srcSentence"> They evaluate settings and conditions like:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">
                      <embeddedLabel>PIN and passwords</embeddedLabel>: Your IT can create rules to require passwords before unlocking a device, the complexity of the password, password expiration, and other password settings.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">
                      <embeddedLabel>Encryption</embeddedLabel>: Your IT can restrict access to devices that are encrypted.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">
                      <embeddedLabel>Device is not jailbroken or rooted</embeddedLabel>: Intune can detect if an enrolled device is jailbroken, and your IT can set the policy to block access on such devices.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src55" class="srcSentence">
                  <embeddedLabel>Conditional access policies</embeddedLabel> are configured for a particular service like Exchange Online or SharePoint Online.</caps:sentence>
                <caps:sentence id="src56" class="srcSentence"> For each service, you can define which groups of users these policies should apply to.</caps:sentence>
                <caps:sentence id="src57" class="srcSentence"> For example, you can make sure that everyone in the finance department can only access company email from enrolled and compliant devices.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src58" class="srcSentence">Watch <externalLink><linkText>this</linkText><linkUri>https://www.youtube.com/watch?feature=player_embedded&amp;v=lYx3YIezccg</linkUri></externalLink> four minute video to see how conditional access affects your end users.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src59" class="srcSentence">Why Architecture Matters</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src60" class="srcSentence">The different components of EMS and Office 365 are built for and designed to run in the cloud.</caps:sentence>
            <caps:sentence id="src61" class="srcSentence"> This brings all the benefits that the cloud offers: scalability, flexibility, and ease of management.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src62" class="srcSentence">Since different businesses have different requirements, EMS is designed to integrate with existing on-premises infrastructure such as Active Directory, Exchange Server, or System Center Configuration Manager.</caps:sentence>
            <caps:sentence id="src63" class="srcSentence"> This allows you to use the credentials already established in your network for both on-premises and cloud resources.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src64" class="srcSentence">The following sections describe the architecture as designed to run in the cloud, and touch briefly on the on-premises option.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src65" class="srcSentence">Email Access Flow</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src66" class="srcSentence">Depending on the type of email application that you use to access Exchange online, the path to establishing secured access to email can be slightly different.</caps:sentence>
                <caps:sentence id="src67" class="srcSentence"> However, the key components: Azure Active Directory (Azure AD), Office 365/Exchange Online, and Microsoft Intune, are the same.</caps:sentence>
                <caps:sentence id="src68" class="srcSentence"> The IT experience, and end-user experience also are similar.</caps:sentence>
                <caps:sentence id="src69" class="srcSentence"> EMS currently supports native email apps and the Microsoft Outlook app for iOS and Android.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src70" class="srcSentence">Access control flow for native email applications</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src71" class="srcSentence">Exchange ActiveSync (EAS) clients attempting to access email in Exchange Online will be evaluated for the following properties:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">Is the device managed by Intune?</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">Is the device registered with Azure Active Directory?</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">Is the device compliant?</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src75" class="srcSentence">Is the client EAS ID mapped to a registered device?</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src76" class="srcSentence">To get to a compliant state, the device on which the EAS client is running needs to:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">Enroll with Intune</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">Register with <externalLink><linkText>Azure Active Directory</linkText><linkUri>https://msdn.microsoft.com/en-us/6a14cb1f-a058-4453-8ede-d9f4a66a7073.aspx</linkUri></externalLink>, and</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">Be compliant with the device policies set by your IT admin.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src80" class="srcSentence">On most platforms, the Azure Active Directory device registration happens automatically during enrollment.</caps:sentence>
                <caps:sentence id="src81" class="srcSentence"> The device states are written by Intune into Azure Active Directory, and then read by Exchange Online the next time the EAS client tries to get email.</caps:sentence>
                <caps:sentence id="src82" class="srcSentence"> If the device is not registered, the user will get a message in their inbox with instructions on how to register (also known as enrolling).</caps:sentence>
                <caps:sentence id="src83" class="srcSentence"> If the device is not compliant, the user will get a different email that redirects them to the Intune web portal where they can get more information on the compliance problem and how to remediate it.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src84" class="srcSentence">
                  <embeddedLabel>Azure AD</embeddedLabel>, authenticates the user and the device, Microsoft Intune manages the compliance and conditional access policies, and <embeddedLabel>Exchange Online</embeddedLabel> manages access to email based on the device state.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="35424911-894f-40fe-b4a9-12dfe03e4301"></image>
              </mediaLink>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src85" class="srcSentence">Access control flow for Outlook applications</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src86" class="srcSentence">Similar to the EAS client, the Outlook email app attempting to access mail in Exchange Online will be evaluated for the following properties:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">Is the device managed by Intune?</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">Is the device registered with Azure Active Directory?</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">Is the device compliant?</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src90" class="srcSentence">The device compliance is established in much in the same way as described in the EAS client access control flow.</caps:sentence>
                <caps:sentence id="src91" class="srcSentence"> However, for Outlook apps, the flow between the components is slightly different.</caps:sentence>
                <caps:sentence id="src92" class="srcSentence"> When the Outlook app attempts to get email, it is redirected to Azure AD.</caps:sentence>
                <caps:sentence id="src93" class="srcSentence"> Azure AD issues a security token if the device is successfully evaluated to be enrolled and compliant.</caps:sentence>
                <caps:sentence id="src94" class="srcSentence"> The security token is then used to get corporate email from Exchange Online.</caps:sentence>
                <caps:sentence id="src95" class="srcSentence"> The email sync is actually brokered through the Outlook cloud service, which gets an EAS service access token on behalf of the user to complete the authentication and delivers the email.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="c9b751b8-bf07-49f5-aaa3-4a32da9d70b4"></image>
              </mediaLink>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src96" class="srcSentence">The IT admin experience:</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src97" class="srcSentence">There is no complex infrastructure setup required for Azure AD or Exchange to make this happen.</caps:sentence>
                <caps:sentence id="src98" class="srcSentence"> Your IT admins:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">Configure and deploy the compliance polices that are used to evaluate the compliance status of the device.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">Configure the Exchange Online conditional access policy, and specify which Azure AD security groups will be affected by, or exempted from these policies.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">Choose to allow or block devices that are not capable of enrolling in Intune.</caps:sentence>
                    <caps:sentence id="src102" class="srcSentence"> The list of supported operating systems for mobile devices is listed later.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src103" class="srcSentence">There is an optional setup stage that may be needed.</caps:sentence>
                <caps:sentence id="src104" class="srcSentence"> The reporting that is used to manage and monitor device access and status requires the Microsoft Intune service to service connector to be set up.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src105" class="srcSentence">The End-user experience:</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src106" class="srcSentence">When the user attempts to access email on the device for the first time, or sync subsequently, the device enrollment and compliance status is checked.</caps:sentence>
                <caps:sentence id="src107" class="srcSentence"> The process of enrolling or fixing compliance issues is a guided experience.</caps:sentence>
                <caps:sentence id="src108" class="srcSentence"> The end-user is shown the necessary steps to enroll their device and make it compliant without needing to call your IT help desk:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src109" class="srcSentence">
                      <embeddedLabel>If the device is not enrolled</embeddedLabel>, the sign-in page will show access denied and will prompt for enrollment.</caps:sentence>
                    <caps:sentence id="src110" class="srcSentence"> On enrollment, the device is automatically registered in Azure Active Directory.</caps:sentence>
                    <caps:sentence id="src111" class="srcSentence"> Intune checks the device for compliance and provides remediation steps to resolve any non-compliance issues.</caps:sentence>
                    <caps:sentence id="src112" class="srcSentence"> Once the device is compliant, Intune sets the device compliance status with Azure Active Directory.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src113" class="srcSentence">
                      <embeddedLabel>If the device is enrolled but is not in compliance</embeddedLabel>, a link with steps to remediate the issues is sent to the device.</caps:sentence>
                    <caps:sentence id="src114" class="srcSentence"> When the end-user corrects the issue (for example, set password, encryption), Intune which manages the compliance policies updates the compliance status of the device in Azure AD.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src115" class="srcSentence">Once the device is evaluated as enrolled and compliant, the email sync should happen within a few minutes.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src116" class="srcSentence">Protect email and attachments from data leakage</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src117" class="srcSentence">The previous section talked about how you can make sure that only compliant devices can access corporate email.</caps:sentence>
            <caps:sentence id="src118" class="srcSentence"> However, the content in the email and email attachments is not protected just by securing access.</caps:sentence>
            <caps:sentence id="src119" class="srcSentence"> The content can be copied, moved, saved to a different location, or shared with another user.</caps:sentence>
            <caps:sentence id="src120" class="srcSentence"> EMS solves this problem using mobile application management policies.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src121" class="srcSentence">Managed apps are apps that are deployed by your IT admin that comply with your companies security requirements.</caps:sentence>
            <caps:sentence id="src122" class="srcSentence"> With these apps, IT has direct control over deployment, ongoing management like inventory or updates, and selective wipe of the apps and their associated data.</caps:sentence>
            <caps:sentence id="src123" class="srcSentence"> Additionally, through a set of mobile application management (MAM) policies, Intune lets you modify the functionality of apps, and restricting sharing of data like:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src124" class="srcSentence">Block copy and paste, or prevent data transfer from a managed app to an app without MAM policy.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src125" class="srcSentence">Prevent backup to personal cloud storage, preventing Save as, etc.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src126" class="srcSentence">Secure app access by requiring PIN/passcode or corporate credentials on a MAM-protected app.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src127" class="srcSentence">Configure the application to open all web links inside the Intune Managed Browser.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src128" class="srcSentence">Selectively wipe only data that is associated with the managed app.</caps:sentence>
                <caps:sentence id="src129" class="srcSentence"> When a device is lost, stolen, or is no longer managed by your IT, a selective wipe can remove all corporate data from the apps, leaving only personal app data behind.</caps:sentence>
                <caps:sentence id="src130" class="srcSentence"> This is known as multi-identity.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src131" class="srcSentence">With <externalLink><linkText>Azure Rights Management Services</linkText><linkUri>https://technet.microsoft.com/en-us/library/jj585026.aspx</linkUri></externalLink>, you can extend email protection in the following ways:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src132" class="srcSentence">Email messages can be encrypted so only the right users can read or view the content whether within your company or outside the company.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src133" class="srcSentence">Users can protect email messages and the recipient can read and use protected email messages sent to them.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src134" class="srcSentence">An administrator can set rules to:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src135" class="srcSentence">Automatically apply the rules to a specified group of recipients or create templates for specific departments.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src136" class="srcSentence">Automatically detect and apply rules to email messages with sensitive content.</caps:sentence>
                    <caps:sentence id="src137" class="srcSentence"> The rule can be based on sender, recipient, message subject, or content.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src138" class="srcSentence">Detect sensitive content and alert the sender to apply the protection rules before sending the email.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src139" class="srcSentence">Managed App Components</caps:sentence>
            </title>
            <content>
              <para></para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src140" class="srcSentence">
                      <embeddedLabel>Microsoft Intune</embeddedLabel> is where you configure the policies, associate the policies with the app, or use the app wrapping tool to enable an in-house app to use mobile application management policies.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src141" class="srcSentence">
                      <embeddedLabel>The Company portal</embeddedLabel> is an app that either runs natively on each device or is browser based.</caps:sentence>
                    <caps:sentence id="src142" class="srcSentence"> Your IT deploys the managed apps to users or devices, and end-users can install the app from the portal.</caps:sentence>
                    <caps:sentence id="src143" class="srcSentence"> The policies associated with the apps are carried over to the device with the apps.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <mediaLink>
                <image xlink:href="e1bc9e16-eb2c-4f1a-a4be-e8b44cc1ba23"></image>
              </mediaLink>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src144" class="srcSentence">The IT admin experience:</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src145" class="srcSentence">Your IT admin creates the mobile application management policies, associates the policy to the app, and deploys it to users or devices.</caps:sentence>
                <caps:sentence id="src146" class="srcSentence"> When the managed app is installed on the device, the app restrictions take effect.</caps:sentence>
                <caps:sentence id="src147" class="srcSentence"> Creating and deploying managed apps involve little or no additional effort:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src148" class="srcSentence">There are existing apps that already have the App SDK which allows you to apply restrictions to the app.</caps:sentence>
                    <caps:sentence id="src149" class="srcSentence"> These require no other processing, but just adding a link pointing to an app store such as iTunes or Google Play.</caps:sentence>
                    <caps:sentence id="src150" class="srcSentence"> Read <externalLink><linkText>this</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn708489.aspx</linkUri></externalLink> article to see the list of managed apps.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src151" class="srcSentence">If you want to manage apps that are created in-house, you can repackage the apps with Microsoft Intune App Wrapping tool.</caps:sentence>
                    <caps:sentence id="src152" class="srcSentence"> The tool repackages the app which allows you to apply restrictions to the app.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src153" class="srcSentence">The End-user experience</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src154" class="srcSentence">End-users can install managed apps and use them to do their work.</caps:sentence>
                <caps:sentence id="src155" class="srcSentence"> They will only be able to move or share data between managed apps.</caps:sentence>
                <caps:sentence id="src156" class="srcSentence"> Any attempt to move data out of the managed app ecosystem will be blocked.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src157" class="srcSentence">Operations and Incidence Response</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src158" class="srcSentence">Once you have implemented the solution, you need to manage the environment and identify potential security risks.</caps:sentence>
            <caps:sentence id="src159" class="srcSentence"> Both Intune and Azure AD have monitoring and reporting capabilities that can help in monitoring and responding quickly in case of a security incident.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src160" class="srcSentence">Here are some of the reporting capabilities:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src161" class="srcSentence">Intune reports and alerts help you monitor the status and health of devices managed by Intune.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src162" class="srcSentence">Azure AD has auditing and activity logging.</caps:sentence>
                <caps:sentence id="src163" class="srcSentence"> You can monitor things like password changes and user management.</caps:sentence>
                <caps:sentence id="src164" class="srcSentence"> Azure Active Directory premium includes advanced anomaly security reports and alerts.</caps:sentence>
                <caps:sentence id="src165" class="srcSentence"> These alerts are based on detailed machine learning based reports showing sign in activity, inconsistent access patterns, and potential threat areas.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src166" class="srcSentence">On-premises implementation</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src167" class="srcSentence">If you have an existing implementation of System Center Configuration Manager, Active Directory and/or Exchange Server you can extend the existing infrastructure by integrating with Intune, Azure AD and Office 365.</caps:sentence>
            <caps:sentence id="src168" class="srcSentence"> Using this hybrid implementation, you can provide a consistent management experience across devices on-premises and in the cloud.</caps:sentence>
            <caps:sentence id="src169" class="srcSentence"> Intune and Configuration Manager offer a similar set of capabilities to allow restricted email access based on the device state.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src170" class="srcSentence">For Exchange Online Dedicated implementations, whether you can take advantage of the cloud based solution described previously, or the hybrid implementation depends on what your current implementation looks like.</caps:sentence>
            <caps:sentence id="src171" class="srcSentence"> Talk to your account team to determine what your implementation will involve.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src172" class="srcSentence">What you should consider when planning your implementation:</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src173" class="srcSentence">
                  <embeddedLabel>Device platform support</embeddedLabel>: You must also consider if you want to allow email access on platforms that are not supported by Intune.</caps:sentence>
                <caps:sentence id="src174" class="srcSentence"> Intune mobile device management supports the following operating systems:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">Apple iOS 7.1 and later (previously enrolled iOS 6.0 and 7.0 devices remain enrolled but new devices cannot enroll)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src176" class="srcSentence">Google Android 2.3.4 and later (includes Samsung KNOX)</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">Windows Phone 8.0 and later</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">Windows RT and later</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src179" class="srcSentence">Windows 8.1 computers and later</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src180" class="srcSentence">
                  <embeddedLabel>Type of email apps</embeddedLabel>: The EMS solution currently supports clients that use EAS protocol, and Outlook apps (previously Accompli on iOS and Android).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src181" class="srcSentence">
                  <embeddedLabel>Policies</embeddedLabel>: The EMS solution and its components have several policies through which security and access is managed.</caps:sentence>
                <caps:sentence id="src182" class="srcSentence"> Determine what policies your IT admin needs to configure.</caps:sentence>
                <caps:sentence id="src183" class="srcSentence"> The three key policies to be used for research and plan when securing access to email and email data are:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">
                      <embeddedLabel>Device Compliance Policies</embeddedLabel>: Determine what compliance means for your company.</caps:sentence>
                    <caps:sentence id="src185" class="srcSentence"> Intune includes several rules that you can set, but all of those rules may or may not apply to your company.</caps:sentence>
                    <caps:sentence id="src186" class="srcSentence"> You can change policies anytime, but it is good practice to determine a basic set of policies for you company.</caps:sentence>
                    <caps:sentence id="src187" class="srcSentence"> Compliance policies are targeted at Intune user groups and device groups.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src188" class="srcSentence">
                      <embeddedLabel>Conditional Access Policies</embeddedLabel>: Conditional access policies are targeted at Azure AD Security Groups.</caps:sentence>
                    <caps:sentence id="src189" class="srcSentence"> Determine which users will be targeted by the policies and if there are users who need to be exempt.</caps:sentence>
                    <caps:sentence id="src190" class="srcSentence"> Conditional Access is supported by both the cloud based solution and the hybrid implementation.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">
                      <embeddedLabel>Mobile Application Management</embeddedLabel>: Determine what apps should be managed and the MAM policies you need to apply to these apps.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src192" class="srcSentence">
                  <embeddedLabel>Device management considerations</embeddedLabel>: Select the device management option that best meets the requirements for your organization before you implement the solution.</caps:sentence>
                <caps:sentence id="src193" class="srcSentence"> There are two options:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src194" class="srcSentence">Unify System Center Configuration Manager with Microsoft Intune to manage all devices through a single console.</caps:sentence>
                    <caps:sentence id="src195" class="srcSentence"> This is called the <newTerm>Hybrid implementation</newTerm>.</caps:sentence>
                    <caps:sentence id="src196" class="srcSentence"> Advantages of this approach:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src197" class="srcSentence">Single management console with rich rights-management controls to manage both on-premises PCs as well as mobile devices</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src198" class="srcSentence">Rich targeting and deployment capabilities</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src199" class="srcSentence">High scale for very large enterprises</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src200" class="srcSentence">Manage the mobile devices through Microsoft Intune separately from the on-premises devices using System Center Configuration Manager.</caps:sentence>
                    <caps:sentence id="src201" class="srcSentence"> This is called <newTerm>Intune Stand-alone implementation</newTerm>.</caps:sentence>
                    <caps:sentence id="src202" class="srcSentence"> Advantages of this approach:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src203" class="srcSentence">Simple web-based console tailored specifically for mobile device management</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src204" class="srcSentence">Rapid access to the latest features</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src205" class="srcSentence">While migration is always possible, we strongly recommend that you make this decision before implementing it, since it will influence a lot of the decisions you will make in the roll out process.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src206" class="srcSentence">
                  <embeddedLabel>Your Exchange environment</embeddedLabel>:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src207" class="srcSentence">Deployment of Exchange connectors and how they connect when network load balancers are implemented.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src208" class="srcSentence">Exchange Online – is it multi-tenant or dedicated?</caps:sentence>
                    <caps:sentence id="src209" class="srcSentence"> If it is dedicated, find out which architecture your tenant is on.</caps:sentence>
                    <caps:sentence id="src210" class="srcSentence"> This will determine whether Azure AD-based conditional access can be used, or if an on-premises connector is required.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src211" class="srcSentence">
                  <embeddedLabel>Azure AD synchronization and Active Directory Federated Services (ADFS), or another third-party federated service</embeddedLabel>:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">Conditional Access is designed to work for customers who have federated their identity service to ADFS.</caps:sentence>
                    <caps:sentence id="src213" class="srcSentence"> Client access rules will generally still apply, however it is recommended that full testing be conducted.</caps:sentence>
                    <caps:sentence id="src214" class="srcSentence"> Requirements for directory synchronization and ADFS are no different than for Office 365.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src215" class="srcSentence">Third-party federation services like Ping should also work.</caps:sentence>
                    <caps:sentence id="src216" class="srcSentence"> Testing before implementation is recommended.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src217" class="srcSentence">Where to go from here</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src218" class="srcSentence">
              <externalLink>
                <linkText>Watch</linkText>
                <linkUri>https://www.youtube.com/watch?v=ltcZvm4VOFU</linkUri>
              </externalLink> this video to learn how to sign up for a trial account and get started.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src219" class="srcSentence">* IDC: "Worldwide Mobile Worker Population 2011–2015 Forecast"</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src220" class="srcSentence">** Experian "Quarterly email benchmark report" (Q3 2014)</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src221" class="srcSentence">*** Forrester Research: "BT Futures Report: Info workers will erase boundary between enterprise &amp; consumer technologies," Feb. 21, 2013</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <externalLink>
          <linkText>
            <caps:sentence id="src222" class="srcSentence">EMS Architecture</caps:sentence>
          </linkText>
          <linkUri>https://azure.microsoft.com/en-us/documentation/infographics/enterprise-mobility/</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence id="src223" class="srcSentence">Start using Intune</caps:sentence>
          </linkText>
          <linkUri>https://technet.microsoft.com/en-us/library/dn646953.aspx</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence id="src224" class="srcSentence">What is Azure Active Directory</caps:sentence>
          </linkText>
          <linkUri>https://azure.microsoft.com/en-us/documentation/articles/active-directory-whatis/</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence id="src225" class="srcSentence">How does Azure Active Directory support Office 365, Microsoft Intune, and other Microsoft services?</caps:sentence>
          </linkText>
          <linkUri>https://azure.microsoft.com/en-us/documentation/articles/active-directory-administer/#what-is-an-azure-ad-tenant</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence id="src226" class="srcSentence">How does Azure Active Directory help you manage identities</caps:sentence>
          </linkText>
          <linkUri>https://azure.microsoft.com/en-us/documentation/articles/active-directory-administer/</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence id="src227" class="srcSentence">What is Azure Rights Management?</caps:sentence>
          </linkText>
          <linkUri>https://technet.microsoft.com/en-us/library/jj585026.aspx</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence id="src228" class="srcSentence">How Applications support Azure Rights Management</caps:sentence>
          </linkText>
          <linkUri>https://technet.microsoft.com/en-us/library/jj585004.aspx</linkUri>
        </externalLink>
        <externalLink>
          <linkText>
            <caps:sentence id="src229" class="srcSentence">Automatically protecting emails with Exchange Online and data loss prevention policies</caps:sentence>
          </linkText>
          <linkUri>https://technet.microsoft.com/en-us/library/jj585026.aspx#BKMK_Example_DLP</linkUri>
        </externalLink>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>