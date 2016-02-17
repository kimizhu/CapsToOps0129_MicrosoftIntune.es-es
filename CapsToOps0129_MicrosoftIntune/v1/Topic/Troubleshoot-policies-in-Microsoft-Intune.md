---
title: Directivas de soluci&#243;n de problemas en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 99fb6db6-21c5-46cd-980d-50f063ab8ab8
---
# Directivas de soluci&#243;n de problemas en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para></para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="19194b121566fd02d810b049f8207da1" id="tgt1" class="tgtSentence">Problemas de directivas</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6504911fbecc4ed21f4319050ce2141e" id="tgt2" class="tgtSentence">A continuación verá enumerados algunos problemas que pueden surgir durante la configuración de directiva <token>wit_firstref</token> y las recomendaciones para solucionar esos problemas.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="d766a9cc7c76f2c8f4d05e7e597b249c" id="tgt3" class="tgtSentence">¿Está la directiva aplicada al dispositivo?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="0e20c8d5875981da614986a34d4b19ae" id="tgt4" class="tgtSentence">
                  <legacyBold>Problema: </legacyBold>no está claro si es una directiva concreta la que se aplica a un dispositivo o si el dispositivo se comporta de forma contraria a la directiva.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="8ce9f3574b4e578bfd4c6d7705d0385b" id="tgt5" class="tgtSentence">Compruebe la información de directivas que tiene disponible en cada dispositivo para obtener información acerca de cómo puede afectar una directiva a un dispositivo determinado.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="c898a4ef3978252cb004d77505702f8b" id="tgt6" class="tgtSentence">En la consola de administración de Intune, cada dispositivo tiene una pestaña de directivas en <ui>Propiedades del dispositivo</ui>.</caps:sentence>
                <caps:sentence sentenceid="296e060f2be8dd0bbcd25838a98a5200" id="tgt7" class="tgtSentence"> Si no es así, probablemente el dispositivo todavía esté por inscribirse o no tenga directivas aplicadas.</caps:sentence>
                <caps:sentence sentenceid="b4b5a085e1e19879352d5e6bfe7f98ea" id="tgt8" class="tgtSentence"> Cada directiva tiene un <ui>Valor previsto</ui> y un <ui>Estado</ui>.</caps:sentence>
                <caps:sentence sentenceid="ddf95e418805c9a659b2672aa8afef92" id="tgt9" class="tgtSentence"> El valor previsto es lo que tenía pensado lograr al asignar la directiva.</caps:sentence>
                <caps:sentence sentenceid="e44829a0b1075417d938ead5cb5adb3d" id="tgt10" class="tgtSentence"> El estado es lo que se logra realmente cuando todas las directivas aplicables al dispositivo, así como las restricciones y los requisitos del hardware y el sistema operativo, se consideran conjuntamente.</caps:sentence>
                <caps:sentence sentenceid="363d35b75fdc949015f8555ed5241193" id="tgt11" class="tgtSentence"> Los estados posibles son:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8f3a1a0c680b948585e1c4ec485c086d" id="tgt12" class="tgtSentence">
                      <ui>Cumple</ui>: el dispositivo ha recibido la directiva e indica al servicio que se ajusta a la configuración.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="6202f75fc61d4f6ab2fe34274e2c04c3" id="tgt13" class="tgtSentence">
                      <ui>No es aplicable</ui>: la configuración de directiva no es aplicable.</caps:sentence>
                    <caps:sentence sentenceid="23adbe8751992aef03762be8f8f85a94" id="tgt14" class="tgtSentence"> Por ejemplo, la configuración de correo electrónico para dispositivos iOS no se aplicaría a un dispositivo Android.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="d9b4817fb5e0a388de84658c984be6e8" id="tgt15" class="tgtSentence">
                      <ui>Pendiente</ui>: la directiva se ha enviado al dispositivo, pero no se ha informado de su estado al servicio.</caps:sentence>
                    <caps:sentence sentenceid="9cb90be5433aa2a0d08b99627e5e104d" id="tgt16" class="tgtSentence"> Por ejemplo, el cifrado en Android requiere que el usuario final lo habilite y, por tanto, la directiva puede estar pendiente.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="782b4afffd80df68f35cda2180094245" id="tgt17" class="tgtSentence">  En la captura de pantalla que tiene a continuación se pueden ver dos ejemplos claros:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9dc1b719ac29691cc56383ec80e5c4ec" id="tgt18" class="tgtSentence">
                      <ui>Permitir contraseñas sencillas</ui> está establecido en <ui>Sí</ui>, como se muestra en la columna <ui>Valor previsto</ui>, pero su <ui>Estado</ui> es <ui>No aplicable</ui>.</caps:sentence>
                    <caps:sentence sentenceid="7b4fb4b11c4714e0a01bbce5ee86d947" id="tgt19" class="tgtSentence"> Esto es porque no se admiten contraseñas sencillas para dispositivos Android.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f8c309ae581905cb913686891e477f38" id="tgt20" class="tgtSentence">De forma similar, el elemento de directiva expandido <ui>Configuración de correo electrónico para dispositivos iOS</ui> no se aplica a este dispositivo, ya que es un dispositivo Android.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <mediaLinkInline>
                  <image xlink:href="3032fd32-6c3b-4e4e-bf1f-8de6e9b8bf3c"></image>
                </mediaLinkInline>
              </para>
            </content>
            <content>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="604b61a544029446272926985783e200" id="tgt21" class="tgtSentence">Recuerde que cuando dos directivas con distintos niveles de restricción se aplican al mismo dispositivo o usuario, la directiva más restrictiva se aplica en la práctica.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="54eddfd986973c8db38d8dabbb90e5f7" id="tgt22" class="tgtSentence">Error 0x87D1FDE8 del dispositivo KNOX</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="e13958c250bef79fb7f47b60f8cc1f39" id="tgt23" class="tgtSentence">
                  <legacyBold>Problema</legacyBold>: después de crear e implementar un perfil de correo electrónico Exchange Active Sync de Samsung KNOX para varios dispositivos Android, estos informan del error <ui>0x87D1FDE8</ui> o del <ui>error de corrección</ui> en las propiedades del dispositivo &gt; pestaña de directivas.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="830485cd92a9ce27e28cafc52646755b" id="tgt24" class="tgtSentence"> 
Revise la configuración de su perfil EAS de Samsung KNOX y la directiva de origen.</caps:sentence>
                <caps:sentence sentenceid="a67ec1d3f85a0c5c55e9cc4b8d1961fd" id="tgt25" class="tgtSentence"> Ya no se admite la opción de sincronización de notas de Samsung y no debe estar seleccionada en el perfil.</caps:sentence>
                <caps:sentence sentenceid="81831ea42ebd09fc7e9eb9bed966f888" id="tgt26" class="tgtSentence"> Asegúrese de que los dispositivos han tenido tiempo suficiente para procesar la directiva (hasta 24 horas).</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="9919b50026f2f07e54d5230b5926273c" id="tgt27" class="tgtSentence">Alerta: error al guardar las reglas de acceso en Exchange</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="ba81c85e454f4ef361891649fbec5bf4" id="tgt28" class="tgtSentence">
                  <legacyBold>Problema</legacyBold>: recibe la alerta <ui>Error al guardar las reglas de acceso en Exchange </ui> en la consola de administración.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="6b1c4577e25a6b5767ce2448e86a1cd9" id="tgt29" class="tgtSentence">Si creó directivas en el área de trabajo de la directiva local de Exchange en la consola de administración, pero usa Office 365, Intune no aplica las opciones configuradas de la directiva.</caps:sentence>
                <caps:sentence sentenceid="d51bfc4b994a56eafef01f9efa021735" id="tgt30" class="tgtSentence"> Tenga en cuenta el origen de la directiva de la alerta.</caps:sentence>
                <caps:sentence sentenceid="95a0ba64345d6a5798e491568bd87c13" id="tgt31" class="tgtSentence">  En el área de trabajo de la directiva local de Exchange, elimine las reglas heredadas ya que son reglas de Exchange globales que se encuentran en el servicio Intune dedicado a Exchange local y no son relevantes para Office 365.</caps:sentence>
                <caps:sentence sentenceid="9f7c3125aa86dfbb84c9ffa9fda0dd85" id="tgt32" class="tgtSentence"> A continuación, cree una directiva nueva para Office 365.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="f8f2eba5eebf42d744459e6b806f7574" id="tgt33" class="tgtSentence">No se puede cambiar la directiva de seguridad de varios dispositivos MDM</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="dd205d2171f083c23705cd45507796f1" id="tgt34" class="tgtSentence">Una vez establecidas las directivas de seguridad a través de MSM o EAS, los dispositivos Windows Phone y Windows RT no permiten que se reduzca el nivel de seguridad de las mismas.</caps:sentence>
            <caps:sentence sentenceid="9dcd5cf5607e7af61bd1211551d05542" id="tgt35" class="tgtSentence"> Por ejemplo, si establece una <ui>contraseña con un número mínimo de 8 caracteres</ui> no podrá reducirla a 4.</caps:sentence>
            <caps:sentence sentenceid="6feb5ba1dde050aab6a003a6c3a701dc" id="tgt36" class="tgtSentence"> Esto es debido a que ya se ha aplicado la directiva más restrictiva en el dispositivo.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="96796a10efc23b43263416f0bfed8262" id="tgt37" class="tgtSentence">Dependiendo de la plataforma del dispositivo, si desea cambiar la directiva a un valor de menos seguro debe restablecer las directivas de seguridad.</caps:sentence>
            <caps:sentence sentenceid="3eb8f0124a4e4f2115d5a896035b8983" id="tgt38" class="tgtSentence"> Por ejemplo, en el escritorio de Windows RT, deslice el dedo desde la derecha para abrir la barra de <ui>Botones de acceso</ui> y haga clic en <ui>Configuración</ui> &gt;<ui> Panel de Control</ui>.</caps:sentence>
            <caps:sentence sentenceid="b105a1a2f5ca8898d17eddf1e7221e1d" id="tgt39" class="tgtSentence">  Seleccione el applet <ui>Cuentas de usuario</ui>.</caps:sentence>
            <caps:sentence sentenceid="92e50a7c414488552144eabb9965e265" id="tgt40" class="tgtSentence"> En el menú de navegación izquierdo, hay un vínculo denominado <ui>Restablecer las directivas de seguridad</ui> en la parte inferior.</caps:sentence>
            <caps:sentence sentenceid="7126ac6a85d1d00d6de9080fe5f91a5e" id="tgt41" class="tgtSentence"> Haga clic en él y, a continuación, haga clic en el botón <ui>Restablecer directivas</ui>.</caps:sentence>
            <caps:sentence sentenceid="9a412cfccc8b53f8bfc70f0b22d29821" id="tgt42" class="tgtSentence"> En otros dispositivos MDM como Android, Windows Phone 8.1 y posteriores e iOS, es posible que tenga que eliminar la inscripción y volver a hacerla para que pueda aplicar una directiva menos restrictiva.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="2949f14e5e0c6ab6b5c4d561fbd43e38" id="tgt43" class="tgtSentence">Los dispositivos Android no aplican los cambios en las directivas de seguridad sin que el usuario final haya dado su consentimiento</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b5d50162f3c1245303aa82a50803cdbf" id="tgt44" class="tgtSentence"> 
 
La MDM de Android no permite que el servicio fuerce cambios en las directivas iniciales de los dispositivos, tal y como hacen otras plataformas</caps:sentence>
            <caps:sentence sentenceid="4a4fc1693badb2d9619711796e5fd9b7" id="tgt45" class="tgtSentence"> Esto es debido a la funcionalidad de Android y no está relacionado con el servicio Intune.</caps:sentence>
            <caps:sentence sentenceid="49baa6713f45c1d7f64a6f8e968c8a37" id="tgt46" class="tgtSentence"> Los dispositivos Android le pedirán permiso al usuario final a través de la ventana de notificación para así poder realizar el cambio de la directiva en cuestión (es decir, contraseñas, cifrado, etc.).</caps:sentence>
            <caps:sentence sentenceid="04c57cbc3f4e4d6d66d5b52bafd59169" id="tgt47" class="tgtSentence">  El usuario final debe responder a esta solicitud y, una vez aceptada, se aplicará la directiva.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d17b70f4-17b4-4d89-88fd-70fa4f34fbea">Troubleshoot software updates in Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para></para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">Policy issues</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Listed here are some issues that may arise from your <token>wit_firstref</token> policy configuration and troubleshooting recommendations for those issues.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src3" class="srcSentence">Is policy applied to device?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src4" class="srcSentence">
                  <legacyBold>Issue: </legacyBold>It's not clear if a particular policy is being applied to a device, or a device behaves contrary to a policy.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src5" class="srcSentence">Check the policy information available for each device to understand how a policy affects a particular device.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src6" class="srcSentence">In the Intune admin console every device has a policy tab under <ui>Device Properties</ui>.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> If not the device may still be in the process of enrolling or may not have policies applied.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> Each policy has an <ui>Intended Value</ui> and a <ui>Status</ui>.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> The intended value is what you meant to achieve when assigning the policy.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> The status is what is actually achieved when all of the policies that apply to the device, as well as the restrictions and requirements of the hardware and the operating system, are considered together.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> Possible statuses are:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">
                      <ui>Conforms</ui>: the device has received the policy and reports to the service that it  conforms to the setting.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">
                      <ui>Not applicable</ui>: The policy setting is not applicable.</caps:sentence>
                    <caps:sentence id="src14" class="srcSentence"> For example,  email settings for iOS devices would not apply to an Android device.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">
                      <ui>Pending</ui>: The policy was sent to the device, but hasn't reported status to the service.</caps:sentence>
                    <caps:sentence id="src16" class="srcSentence"> For example, encryption on Android, which requires end user to enable encryption, and may therefore be pending.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src17" class="srcSentence">  In the screenshot below you can see two clear examples:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">
                      <ui>Allow simple passwords</ui> is set to <ui>Yes</ui>, as shown in the <ui>Intended Value</ui> column, but its <ui>Status</ui> is <ui>Not applicable</ui>.</caps:sentence>
                    <caps:sentence id="src19" class="srcSentence"> This is because simple passwords are not supported for Android devices.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Similarly, the expanded policy item<ui>Email settings for iOS devices</ui> is not applied to this device, as it is an Android device.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <mediaLinkInline>
                  <image xlink:href="3032fd32-6c3b-4e4e-bf1f-8de6e9b8bf3c"></image>
                </mediaLinkInline>
              </para>
            </content>
            <content>
              <alert class="note">
                <para>
                  <caps:sentence id="src21" class="srcSentence">Remember that when two policies with different levels of restriction apply to the same device or user, the more restrictive policy applies in practice.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src22" class="srcSentence">Error  0x87D1FDE8 for KNOX device</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src23" class="srcSentence">
                  <legacyBold>Issue</legacyBold>:After creating and deploying an Exchange Active Sync email profile for Samsung KNOX for  various Android devices they report the error <ui>0x87D1FDE8</ui> or <ui>remediation failed</ui>   in the device's properties &gt; policy tab.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src24" class="srcSentence"> 
Review the configuration of your EAS profile for Samsung KNOX and source policy.</caps:sentence>
                <caps:sentence id="src25" class="srcSentence"> The Samsung Notes sync option is no longer supported and that option should not be selected in your profile.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> Be sure devices have had enough time to process the policy, up to 24 hours.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src27" class="srcSentence">Alert: Saving of Access Rules to Exchange has Failed</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src28" class="srcSentence">
                  <legacyBold>Issue</legacyBold>: You receive the alert <ui>Saving of Access Rules to Exchange has Failed </ui> in the admin console.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src29" class="srcSentence">If you  created policies in the Exchange On-Premises Policy workspace under the Admin Console but are using O365, the configured policy settings are not are not enforced by Intune.</caps:sentence>
                <caps:sentence id="src30" class="srcSentence"> Note the policy source from the alert.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence">  Under the Exchange On-premises Policy workspace delete the legacy rules, as these are Global Exchange rules within Intune for on-premises Exchange, and are not relevant to O365.</caps:sentence>
                <caps:sentence id="src32" class="srcSentence"> Then, create new policy for O365.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src33" class="srcSentence">Cannot change security policy for various MDM devices</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src34" class="srcSentence">Windows Phone and Windows RT devices do not allow security policies set via MDM or EAS to be reduced in security once you've set them.</caps:sentence>
            <caps:sentence id="src35" class="srcSentence"> For example, you set a <ui>Minimum number of character password</ui>  to 8  then try to reduce it to 4.</caps:sentence>
            <caps:sentence id="src36" class="srcSentence"> The more restrictive policy has already been applied to the device.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src37" class="srcSentence">Depending on the device platform, if you want to change the policy  to a less secure value you may need to reset security policies.</caps:sentence>
            <caps:sentence id="src38" class="srcSentence"> For example, in Windows RT,  on the desktop swipe in from right to open the <ui>Charms</ui> bar and click  <ui>Settings</ui> &gt;<ui> Control Panel</ui>.</caps:sentence>
            <caps:sentence id="src39" class="srcSentence">  Select the <ui>User Accounts</ui> applet.</caps:sentence>
            <caps:sentence id="src40" class="srcSentence"> In the left hand navigation menu, there is a <ui>Reset Security Policies</ui> link at the bottom.</caps:sentence>
            <caps:sentence id="src41" class="srcSentence"> Click  it and then click the <ui>Reset Policies</ui> button.</caps:sentence>
            <caps:sentence id="src42" class="srcSentence"> Other MDM devices, such as Android, Windows Phone 8.1 and later, and iOS, may need to be retired and re-enrolled back into the service for you to be able to apply a  less restrictive policy.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src43" class="srcSentence">Android devices do not force Security Policy Changes without end user Acceptance</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src44" class="srcSentence"> 
 
Android MDM does not allow the service to force initial policy changes on devices as other platforms allow.</caps:sentence>
            <caps:sentence id="src45" class="srcSentence"> This is due to Android functionality, and is not related to the Intune service.</caps:sentence>
            <caps:sentence id="src46" class="srcSentence"> Android devices will prompt the end user via the notification window of the related policy change (i.e. Password, Encryption, etc.).</caps:sentence>
            <caps:sentence id="src47" class="srcSentence">  The end user must respond to the prompt and once accepted the policy should be applied.</caps:sentence>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d17b70f4-17b4-4d89-88fd-70fa4f34fbea">Troubleshoot software updates in Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>