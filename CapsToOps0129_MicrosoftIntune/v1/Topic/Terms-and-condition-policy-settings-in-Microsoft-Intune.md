---
title: Configuraci&#243;n de la directiva de t&#233;rminos y condiciones en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6edf0ac1-4f46-4543-a9e5-f484ac37e9a5
---
# Configuraci&#243;n de la directiva de t&#233;rminos y condiciones en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence sentenceid="0d42b69653ccf2bf223b13d6585441ee" id="tgt1" class="tgtSentence">Puede implementar los términos y condiciones de <token>wit_nextref</token> en los grupos de usuarios para explicar en qué afecta la inscripción, el acceso a los recursos de trabajo y el uso del portal de empresa a los dispositivos y los usuarios.</caps:sentence>
          <caps:sentence sentenceid="2f90f7988af1d2107646f43a95899d6e" id="tgt2" class="tgtSentence"> Los usuarios deben aceptar los términos y las condiciones para poder usar el portal de empresa a fin de inscribirse y obtener acceso a su trabajo.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="8286bb1e8d9ffd9c624293992acc1bb3" id="tgt3" class="tgtSentence">Trabajar con directivas de términos y condiciones en Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7f8f465d6c3e4148e4259f50c8e8d4c8" id="tgt4" class="tgtSentence">Puede crear e implementar varias directivas que contienen diferentes términos y condiciones.</caps:sentence>
            <caps:sentence sentenceid="95e5242bff2ac5d44da4f4b1b435e137" id="tgt5" class="tgtSentence"> También puede generar versiones de los mismos términos y condiciones en distintos idiomas e implementarlas en los grupos correspondientes.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="22095b4c56fb72213f983cb5b17ae784" id="tgt6" class="tgtSentence">Para crear una directiva de términos y condiciones</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt7" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Términos y condiciones</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt8" class="tgtSentence">Haga clic en <ui>Agregar</ui> para crear una nueva directiva de términos y condiciones.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="d61ff637002b4076012cb486d175ca1b" id="tgt9" class="tgtSentence">También puede <ui>Editar</ui> o <ui>Eliminar</ui> una directiva existente.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt10" class="tgtSentence">En la página <ui>Crear términos y condiciones</ui>, especifique la siguiente información:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c5c3a5f9b20a480f89a2ec1a209252ce" id="tgt11" class="tgtSentence">
                          <ui>Nombre</ui>: nombre de directiva único que aparece en la consola de Intune</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b98181b813921f7ec771621994d0b67d" id="tgt12" class="tgtSentence">
                          <ui>Descripción</ui>: detalles que le ayudan a identificar la directiva en la consola de Intune</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2e93c7acbfa4b1cc730f83fcd9fb72f9" id="tgt13" class="tgtSentence">
                          <ui>Título</ui>: título que se muestra a los usuarios en el portal de la empresa</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="8e9664c34d59f906c2e1f7106f810575" id="tgt14" class="tgtSentence">
                          <ui>Texto para explicar qué significa si el usuario acepta</ui>: los usuarios de etiqueta lo ven según la aceptación.</caps:sentence>
                        <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt15" class="tgtSentence">
                          <ui>Ejemplo</ui>:"Acepto los términos y condiciones".</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt16" class="tgtSentence">Cuando termine, haga clic en <ui>Guardar</ui>.</caps:sentence>
                    <caps:sentence sentenceid="5dd8e90cd890b906fc93236575cd194b" id="tgt17" class="tgtSentence"> La nueva directiva se muestra en el nodo <ui>Términos y condiciones</ui> del área de trabajo <ui>Directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure>
            <title>
              <caps:sentence sentenceid="fb35c2e0746fb37efa402dd801a2ef31" id="tgt18" class="tgtSentence">Para implementar una directiva de términos y condiciones</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt19" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Términos y condiciones</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="8503f46b111f17f4901b912269e3bc9d" id="tgt20" class="tgtSentence">	En la lista <ui>Directivas de términos y condiciones</ui>, seleccione la directiva que desea implementar y, luego, haga clic en <ui>Administrar implementación</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="8503f46b111f17f4901b912269e3bc9d" id="tgt21" class="tgtSentence">	En el cuadro de diálogo <ui>Administrar implementación</ui>, seleccione los grupos de usuarios en los que desee implementar la directiva y haga clic en <ui>Aceptar</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="5a716e65990dbfe0368ec0168d22d0b4" id="tgt22" class="tgtSentence">Cuando los usuarios de destino tienen acceso al portal de la empresa, Intune muestra los términos y las condiciones que implementó.</caps:sentence>
                    <caps:sentence sentenceid="761259cbbcd1ab39644d15429a457128" id="tgt23" class="tgtSentence"> Los usuarios deben aceptar estos términos para tener acceso a los recursos de la empresa.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure>
            <title>
              <caps:sentence sentenceid="76255b8407b6d97eaa1169468a14f31d" id="tgt24" class="tgtSentence">Para supervisar una directiva de términos y condiciones</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt25" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Términos y condiciones</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt26" class="tgtSentence">En la ventana <ui>Crear nuevo informe</ui>, haga clic en <ui>Ver informe</ui>.</caps:sentence>
                    <caps:sentence sentenceid="c9dea06511dec77614d9654c235a9c2e" id="tgt27" class="tgtSentence"> El informe se abrirá e indicará los usuarios que aceptaron los términos y las condiciones que implementó.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section address="BKMK_TCVers">
            <title>
              <caps:sentence sentenceid="0bdd0e3f7a5eb057c630283751eae18f" id="tgt28" class="tgtSentence">Actualizaciones y control de versiones de los términos y condiciones</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="ca2acd2074abf69396da580ab11d3438" id="tgt29" class="tgtSentence">Al editar una directiva existente de términos y condiciones, puede elegir el comportamiento al implementar la directiva.</caps:sentence>
                <caps:sentence sentenceid="be936089f4f75ee4fd2af9a8203c4bc7" id="tgt30" class="tgtSentence"> Use el procedimiento siguiente, que lo ayudará a actualizar las directivas existentes de términos y condiciones.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence sentenceid="39447a54c61e6ede65714904e21fa6e9" id="tgt31" class="tgtSentence">Cómo trabajar con varias versiones de los términos y las condiciones</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt32" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Términos y condiciones</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="e1048cb3f517930661d1aab16351f528" id="tgt33" class="tgtSentence">	Seleccione la directiva de términos y condiciones que desea modificar y luego haga clic en <ui>Editar</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt34" class="tgtSentence">En la página <ui>Editar términos y condiciones</ui>, realice las modificaciones necesarias y luego especifique si esta nueva versión requiere que todos los usuarios acepten los términos y las condiciones, o si solo los usuarios nuevos verán la versión nueva.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="99a5fb61cce2f0933fd61d3094c11134" id="tgt35" class="tgtSentence">Se recomienda aumentar el número de versión y requerir aceptación cada vez que realice cambios importantes en la directiva de términos y condiciones.</caps:sentence>
                        <caps:sentence sentenceid="43b596f9348f9046da2d83c6d08ef23e" id="tgt36" class="tgtSentence"> Si va a corregir errores tipográficos o cambiar el formato, por ejemplo, mantenga el número de versión actual.</caps:sentence>
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
        <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">You can deploy <token>wit_nextref</token> terms and conditions to user groups to explain how enrollment, access to work resources, and using the company portal affect devices and users.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Users must accept the terms and conditions before they can use the company portal to enroll and access their work.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src3" class="srcSentence">Working with terms and conditions policies in Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">You can create and deploy multiple policies containing different terms and conditions.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> You can also produce versions of the same terms and conditions in different languages and then deploy these to their appropriate groups.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src6" class="srcSentence">To create a terms and conditions policy</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Policy</ui> &gt; <ui>Terms and Conditions</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">Click <ui>Add</ui> to create a new terms and conditions policy.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src9" class="srcSentence">You can also <ui>Edit</ui> or <ui>Delete</ui> an existing policy.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">On the <ui>Create Terms and Conditions</ui> page, specify the following information:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src11" class="srcSentence">
                          <ui>Name</ui> - A unique policy name displayed in the Intune console</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src12" class="srcSentence">
                          <ui>Description</ui> - Details that help you identify the policy in the Intune console</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src13" class="srcSentence">
                          <ui>Title</ui> - The title displayed to users in the company portal</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">
                          <ui>Text to explain what it means if the user accepts</ui> - Label users see regarding acceptance.</caps:sentence>
                        <caps:sentence id="src15" class="srcSentence">
                          <ui>Example</ui>: “I agree to the terms and conditions.”</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">When you are finished, click <ui>Save</ui>.</caps:sentence>
                    <caps:sentence id="src17" class="srcSentence"> The new policy is displayed in the <ui>Terms and Conditions </ui>node of the <ui>Policy </ui>workspace.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure>
            <title>
              <caps:sentence id="src18" class="srcSentence">To deploy a terms and conditions policy</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Policy</ui> &gt; <ui>Terms and Conditions</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">	In the <ui>Terms and Conditions Policies</ui> list, select the policy you want to deploy, and then click <ui>Manage Deployment</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">	In the <ui>Manage Deployment</ui> dialog box, select the user groups who you want to deploy the policy to, and then click <ui>OK</ui>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">When targeted users access the company portal, Intune displays the terms and conditions you deployed.</caps:sentence>
                    <caps:sentence id="src23" class="srcSentence"> Users must accept these terms before they can gain access to company resources.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure>
            <title>
              <caps:sentence id="src24" class="srcSentence">To monitor a terms and conditions policy</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src25" class="srcSentence">In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Policy</ui> &gt; <ui>Terms and Conditions</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">In the <ui>Create New Report</ui> window, click <ui>View Report</ui>.</caps:sentence>
                    <caps:sentence id="src27" class="srcSentence"> The report will open detailing which users have accepted the terms and conditions you deployed.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section address="BKMK_TCVers">
            <title>
              <caps:sentence id="src28" class="srcSentence">Updates and version control for terms and conditions</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src29" class="srcSentence">When you edit an existing terms and conditions policy, you can choose the behavior when you deploy the policy.</caps:sentence>
                <caps:sentence id="src30" class="srcSentence"> Use the following procedure to help you update existing terms and conditions policies.</caps:sentence>
              </para>
              <procedure>
                <title>
                  <caps:sentence id="src31" class="srcSentence">How to work with multiple versions of terms and conditions</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src32" class="srcSentence">In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Policy</ui> &gt; <ui>Terms and Conditions</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src33" class="srcSentence">	Select the terms and conditions policy that you want to edit, and then click <ui>Edit</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">On the <ui>Edit Terms and Conditions </ui>page, make any required edits, and then specify whether this new version requires all users to accept the terms and conditions, or only new users will see the new version.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">We recommend you increase the version number and require acceptance any time you make significant changes to your terms and conditions policy.</caps:sentence>
                        <caps:sentence id="src36" class="srcSentence"> Keep the current version number if you are fixing typos or changing formatting, for example.</caps:sentence>
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
        <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>