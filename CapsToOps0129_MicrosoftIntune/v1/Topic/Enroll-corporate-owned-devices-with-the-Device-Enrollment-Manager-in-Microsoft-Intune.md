---
title: Inscribir dispositivos propiedad de la empresa con el Administrador de inscripci&#243;n de dispositivos de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a23abc61-69ed-44f1-9b71-b86aefc6ba03
---
# Inscribir dispositivos propiedad de la empresa con el Administrador de inscripci&#243;n de dispositivos de Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="373c6d950addefa9532d5cb524080ff8" id="tgt1" class="tgtSentence">Las organizaciones pueden usar Intune para administrar un gran número de dispositivos móviles con una sola cuenta de usuario.</caps:sentence>
          <caps:sentence sentenceid="90adbbe7112a5ab0269194573e650cc6" id="tgt2" class="tgtSentence"> El <newTerm>administrador de inscripción de dispositivos</newTerm> es una cuenta especial de Intune con permisos para inscribir más de cinco dispositivos.</caps:sentence>
          <caps:sentence sentenceid="699453b338b285913a3a70aa9bcd8eec" id="tgt3" class="tgtSentence"> Puede asignar un administrador o supervisor de almacén, por ejemplo, una cuenta de usuario de administrador de inscripción de dispositivos que le permita hacer lo siguiente:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="9d253ec01f8b137280fbf94173eddd40" id="tgt4" class="tgtSentence">Inscribir dispositivos en Intune</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="f0d241cde182163bd7dbcc91fd910faf" id="tgt5" class="tgtSentence">Iniciar sesión en el portal de empresa para obtener aplicaciones de empresa</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="98512cb6115937f8359721fef8c88a99" id="tgt6" class="tgtSentence">Instalar y desinstalar software</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a5f1d3d04f2fd3882b266953415e1a9f" id="tgt7" class="tgtSentence">Configurar el acceso a los datos de la empresa</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="651e45e83f9a44170ecfbde8f15de110" id="tgt8" class="tgtSentence">El administrador del almacén no puede restablecer el dispositivo desde el portal de empresa.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt9" class="tgtSentence">
            <embeddedLabel>Ejemplos con un administrador de inscripción de dispositivos:</embeddedLabel> <br /> Un restaurante quiere tener tabletas de punto de venta para que las usen los camareros y monitores de pedidos para el personal de cocina.</caps:sentence>
          <caps:sentence sentenceid="930cc8c1987b221b1e8a1363107faea9" id="tgt10" class="tgtSentence"> Los empleados no necesitan nunca acceder a los datos de la empresa ni iniciar sesión como usuario.</caps:sentence>
          <caps:sentence sentenceid="fe672b5ce4c939b8c2d95c45e90d9635" id="tgt11" class="tgtSentence"> El administrador de Intune crea una cuenta de administrador de inscripción de dispositivos e inscribe los dispositivos propiedad de la empresa usando esa cuenta.</caps:sentence>
          <caps:sentence sentenceid="4d46bf0324c3ad20af80f0eebc78d9f3" id="tgt12" class="tgtSentence"> El administrador también podría dar las credenciales de inscripción de dispositivos a un responsable del restaurante, para que pueda inscribir y administrar los dispositivos.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="f8b28186179735bc12c552183655ac30" id="tgt13" class="tgtSentence"> El administrador puede implementar aplicaciones específicas de cada rol en los dispositivos del restaurante.</caps:sentence>
          <caps:sentence sentenceid="ba0e2e2ecbdc221543c04888cb2aa3c6" id="tgt14" class="tgtSentence"> Un administrador también puede seleccionar el dispositivo en la consola de Intune y retirarlo de la administración de dispositivos móviles con la consola de administración.</caps:sentence>
        </para>
      </introduction>
      <section expanded="true">
        <title>
          <caps:sentence sentenceid="58d09bce61f78a47c635b604016fd27c" id="tgt15" class="tgtSentence">Cuentas de administrador de inscripción de dispositivos de Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="fda76d11458d2419dc8fe284c01a3ca9" id="tgt16" class="tgtSentence">Las cuentas de administrador de inscripción de dispositivos son cuentas de usuario con permisos para inscribir un gran número de dispositivos propiedad de la empresa.</caps:sentence>
            <caps:sentence sentenceid="6634cd1946451363879689998b2aae9d" id="tgt17" class="tgtSentence"> Solo los usuarios de la consola Intune pueden ser administradores de inscripción de dispositivos.</caps:sentence>
          </para>
          <procedure expanded="true">
            <title>
              <caps:sentence sentenceid="e62edc177acc55dda9bb0e89596aebce" id="tgt18" class="tgtSentence">Agregar un administrador de inscripción de dispositivos a Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="45568fffc1aefb85bb60ebc96a472dda" id="tgt19" class="tgtSentence">Vaya al <externalLink target="_blank"><linkText>portal de cuentas Microsoft Intune</linkText><linkUri>http://go.microsoft.com/fwlink/p/?LinkID=329938</linkUri></externalLink> e inicie sesión con su cuenta de administrador.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt20" class="tgtSentence">Haga clic en <embeddedLabel>Agregar usuario</embeddedLabel>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ce63a2533c6e9fd611c69b9582437826" id="tgt21" class="tgtSentence">Confirme que aparece la cuenta de usuario que será el administrador de inscripción de dispositivos.</caps:sentence>
                    <caps:sentence sentenceid="97272921af47be9551baa02a35a396de" id="tgt22" class="tgtSentence"> Si no es así, agregue el usuario haciendo clic en <embeddedLabel>Nuevo</embeddedLabel> y complete el proceso para agregar un usuario.</caps:sentence>
                    <caps:sentence sentenceid="85ea9c6c4886c25fc4fa535981239629" id="tgt23" class="tgtSentence"> Para obtener más información acerca de cómo agregar usuarios, consulte <link xlink:href="d158503c-1276-422b-ab81-5f66c1cd7e7a#Anchor_3">Task 3: Add users and assign licenses for your subscription</link>.</caps:sentence>
                    <caps:sentence sentenceid="21bb810c8de8a57e748b772722999aad" id="tgt24" class="tgtSentence"> Se requiere una licencia de suscripción para cada usuario que acceda al servicio y el <newTerm>administrador de inscripción de dispositivos</newTerm> no puede ser un administrador de Intune.</caps:sentence>
                    <caps:sentence sentenceid="f1714b7d9539bfa150797f0899ced6ba" id="tgt25" class="tgtSentence"> Determine si necesita agregar más licencias antes de usar esta característica.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d950fb5dd32dd15a00c6f44bd246075f" id="tgt26" class="tgtSentence">Inicie sesión en la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> con su inicio de sesión como administrador.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1a01bedbe23ffb0dced143ff67f51670" id="tgt27" class="tgtSentence">En el panel de navegación, haga clic en <ui>Administración</ui>, vaya a <ui>Administración de administradores</ui> y seleccione <ui>Administrador de inscripción de dispositivos</ui>.</caps:sentence>
                    <caps:sentence sentenceid="e64184fa059e1c0f7c1569c732b42767" id="tgt28" class="tgtSentence"> Se abre la página Administradores de inscripción de dispositivos.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt29" class="tgtSentence">Haga clic en <ui>Agregar...</ui>.</caps:sentence>
                    <caps:sentence sentenceid="90adbbe7112a5ab0269194573e650cc6" id="tgt30" class="tgtSentence"> Se abre el cuadro de diálogo <ui>Agregar administrador de inscripción de dispositivos</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="eb2d3f6b2893bd777f6281d9aadf569f" id="tgt31" class="tgtSentence">Escriba el <ui>Id. de usuario</ui> de la cuenta de Intune y, después, haga clic en <ui>Aceptar</ui>.</caps:sentence>
                    <caps:sentence sentenceid="7e2d516441e6d685402ccb3aa27af278" id="tgt32" class="tgtSentence"> El usuario administrador de inscripción de dispositivos no puede ser un administrador de Intune.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="512fc10aa6a24618a96698889d783ed9" id="tgt33" class="tgtSentence">El administrador de inscripción de dispositivos ahora puede inscribir dispositivos móviles mediante el mismo procedimiento que un usuario final usa para un escenario de BYOD en el portal de empresa.</caps:sentence>
                    <caps:sentence sentenceid="22f2828047960be41ad76d350e2f3b0e" id="tgt34" class="tgtSentence"> Para inscribir dispositivos mediante el portal de empresa, consulte <link xlink:href="3adf63cd-34b6-4641-aa88-766bb59dd853">Enroll mobile devices using the Windows Intune Company Portal</link>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure expanded="true">
            <title>
              <caps:sentence sentenceid="ff509fd041ab0beceb3121b207751c2e" id="tgt35" class="tgtSentence">Eliminar un administrador de inscripción de dispositivos de Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d950fb5dd32dd15a00c6f44bd246075f" id="tgt36" class="tgtSentence">Inicie sesión en el <externalLink><linkText>portal de cuentas de Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> con su inicio de sesión como administrador.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1a01bedbe23ffb0dced143ff67f51670" id="tgt37" class="tgtSentence">En el panel de navegación, haga clic en <ui>Administración</ui> y vaya a <ui>Administración de administradores</ui> y seleccione <ui>Administrador de inscripción de dispositivos</ui>.</caps:sentence>
                    <caps:sentence sentenceid="e64184fa059e1c0f7c1569c732b42767" id="tgt38" class="tgtSentence"> Se abre la página Administradores de inscripción de dispositivos.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ade273f6e8f57a574109524327dc33f9" id="tgt39" class="tgtSentence">Seleccione el <ui>Usuario</ui> administrador de inscripción de dispositivos que quiere eliminar y haga clic en <ui>Eliminar</ui>.</caps:sentence>
                    <caps:sentence sentenceid="61338c6aaeac69216b66c91d275b3816" id="tgt40" class="tgtSentence"> Este usuario no se eliminará de Intune y los dispositivos que este usuario administra permanecerán inscritos en Intune.</caps:sentence>
                    <caps:sentence sentenceid="d533b9cfaf7ed0268dcb05be0c3ea91c" id="tgt41" class="tgtSentence"> Eliminar un administrador de inscripción de dispositivos impide que el usuario inscriba más dispositivos en Intune.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt42" class="tgtSentence">Haga clic en <ui>Sí</ui> para confirmar que quiere eliminar el administrador de inscripción de dispositivos.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence sentenceid="ff76507d9ad645c2915546d383d6d5cc" id="tgt43" class="tgtSentence">La eliminación de un administrador de inscripción de dispositivos no afecta a los dispositivos inscritos.</caps:sentence>
            <caps:sentence sentenceid="e548c598af122242e2fd53cb5cfe51e1" id="tgt44" class="tgtSentence"> Cuando se elimina un administrador de inscripción de dispositivos:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="e005be4f4b570f91860cc0cec7742670" id="tgt45" class="tgtSentence">Ningún dispositivo inscrito se ve afectado</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7be0737c4de6d9ccbf6069bb8f01d6e3" id="tgt46" class="tgtSentence">Los dispositivos inscritos se continuarán administrando de manera completa</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ec0b581cc52064dd85d49d065e7b453f" id="tgt47" class="tgtSentence">Las credenciales de la cuenta del administrador de inscripción de dispositivos eliminado siguen siendo válidas para iniciar sesión en el portal de empresa para tener acceso a las aplicaciones</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f6220280d3f2617d70ed60b7a7eee325" id="tgt48" class="tgtSentence">Las credenciales de la cuenta del administrador de inscripción de dispositivos eliminado todavía no pueden borrar ni retirar dispositivos</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="35d723bfcc1109c716868036ef6aa47b" id="tgt49" class="tgtSentence">La relación de la cuenta del administrador de inscripción de dispositivos eliminado se mantiene pero no se pueden inscribir dispositivos adicionales</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d158503c-1276-422b-ab81-5f66c1cd7e7a">Start using Microsoft Intune</link>
        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage mobile devices with Microsoft Intune</link>
        <link xlink:href="3adf63cd-34b6-4641-aa88-766bb59dd853">Enable mobile device enrollment with the Microsoft Intune Company Portal</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Organizations can use Intune to manage large numbers of mobile devices with a single user account.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The <newTerm>device enrollment manager</newTerm> account is a special Intune account with permission to enroll more than five devices.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> You can assign a store manager or supervisor, for example, a device enrollment manager user account to allow her to do the following:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">Enroll devices in Intune</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Log on to company portal to get company apps</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Install and uninstall software</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Configure access to company data</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src8" class="srcSentence">The store manager cannot reset the device from the company portal.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">
            <embeddedLabel>Examples of device enrollment manager scenario:</embeddedLabel> <br />A restaurant wants point-of-sale tablets for its wait staff and order monitors for its kitchen staff.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> The employees never need access to company data or to logon as a user.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence"> The Intune administrator creates a device enrollment manager account and enrolls the company-owned devices using that account.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> Alternatively, the administrator could give the device enrollment manager credentials to a restaurant manager, allowing him or her to enroll and manage the devices.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence"> The administrator or manager can deploy role-specific apps to the restaurant devices.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> An administrator can also select the device in the Intune console and retire it from mobile device management with the administration console.</caps:sentence>
        </para>
      </introduction>
      <section expanded="true">
        <title>
          <caps:sentence id="src15" class="srcSentence">Device enrollment manager accounts in Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src16" class="srcSentence">Device enrollment manager accounts are user accounts with permission to enroll large numbers of corporate-owned devices.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> Only users in the Intune console can be device enrollment managers.</caps:sentence>
          </para>
          <procedure expanded="true">
            <title>
              <caps:sentence id="src18" class="srcSentence">Add a device enrollment manager to Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">Go to the <externalLink target="_blank"><linkText>Microsoft Intune account portal</linkText><linkUri>http://go.microsoft.com/fwlink/p/?LinkID=329938</linkUri></externalLink> and sign in your administrator account.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">Click <embeddedLabel>Add user</embeddedLabel>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">Confirm that the user account that will be a device enrollment manager is listed.</caps:sentence>
                    <caps:sentence id="src22" class="srcSentence"> If not, add the user by clicking <embeddedLabel>New</embeddedLabel> and completing the Add user process.</caps:sentence>
                    <caps:sentence id="src23" class="srcSentence"> For more information about adding users, see <link xlink:href="d158503c-1276-422b-ab81-5f66c1cd7e7a#Anchor_3">Task 3: Add users and assign licenses for your subscription</link>.</caps:sentence>
                    <caps:sentence id="src24" class="srcSentence"> A subscription license is required for each user that accesses the Service and the <newTerm>device enrollment manager</newTerm> cannot be an Intune administrator.</caps:sentence>
                    <caps:sentence id="src25" class="srcSentence"> Determine whether you need to add more licenses before you use this feature.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src26" class="srcSentence">Logon to the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> with your administrator sign in.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">In the navigation pane, click <ui>Admin</ui>, go to <ui>Administrator Management</ui> and select <ui>Device Enrollment Manager</ui>.</caps:sentence>
                    <caps:sentence id="src28" class="srcSentence"> The Device Enrollment Managers page opens.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Click <ui>Add…</ui>.</caps:sentence>
                    <caps:sentence id="src30" class="srcSentence"> The <ui>Add Device Enrollment Manager</ui> dialog box opens.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">Enter the <ui>User ID</ui> of the Intune account and then click <ui>OK</ui>.</caps:sentence>
                    <caps:sentence id="src32" class="srcSentence"> The device enrollment manager user cannot be an Intune administrator.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">The device enrollment manager can now enroll mobile devices using the same procedure an end user uses for a BYOD scenario in the company portal.</caps:sentence>
                    <caps:sentence id="src34" class="srcSentence"> To enroll devices using the company portal, see <link xlink:href="3adf63cd-34b6-4641-aa88-766bb59dd853">Enroll mobile devices using the Windows Intune Company Portal</link>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure expanded="true">
            <title>
              <caps:sentence id="src35" class="srcSentence">Delete a device enrollment manager from Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">Logon to the <externalLink><linkText>Microsoft Intune account portal</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> with your administrator sign in.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">In the navigation pane, click <ui>Admin</ui> and go to <ui>Administrator Management</ui> and select <ui>Device Enrollment Manager</ui>.</caps:sentence>
                    <caps:sentence id="src38" class="srcSentence"> The Device Enrollment Managers page opens.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src39" class="srcSentence">Select the device enrollment manager <ui>User</ui> that you want to delete, and then click <ui>Delete</ui>.</caps:sentence>
                    <caps:sentence id="src40" class="srcSentence"> This user won’t be deleted from Intune and the devices this user manages will remain enrolled in Intune.</caps:sentence>
                    <caps:sentence id="src41" class="srcSentence"> Deleting a device enrollment manager prevents that user from enrolling more devices in Intune.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Click <ui>Yes</ui> to confirm you want to delete the device enrollment manager.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <para>
            <caps:sentence id="src43" class="srcSentence">Deleting a device enrollment manager does not affect enrolled devices.</caps:sentence>
            <caps:sentence id="src44" class="srcSentence"> When a device enrollment manager is deleted:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src45" class="srcSentence">No enrolled devices are affected</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src46" class="srcSentence">Enrolled devices continue to be fully managed</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src47" class="srcSentence">The deleted device enrollment manager account credentials remain valid to logon to the company portal to access apps</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src48" class="srcSentence">The deleted device enrollment manager account credentials still cannot wipe or retire devices</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src49" class="srcSentence">The deleted device enrollment manager account’s relationship to enrolled devices remains but no additional devices can be enrolled</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="d158503c-1276-422b-ab81-5f66c1cd7e7a">Start using Microsoft Intune</link>
        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage mobile devices with Microsoft Intune</link>
        <link xlink:href="3adf63cd-34b6-4641-aa88-766bb59dd853">Enable mobile device enrollment with the Microsoft Intune Company Portal</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>