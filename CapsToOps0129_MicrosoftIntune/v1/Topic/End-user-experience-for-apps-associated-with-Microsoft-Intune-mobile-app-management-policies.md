---
title: Experiencia del usuario final para aplicaciones asociadas con directivas de administraci&#243;n de aplicaciones m&#243;viles de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b57e6525-b57c-4cb4-a84c-9f70ba1e8e19
---
# Experiencia del usuario final para aplicaciones asociadas con directivas de administraci&#243;n de aplicaciones m&#243;viles de Microsoft Intune
Las directivas de administración de aplicaciones móviles (MAM) solo se aplican cuando se usan aplicaciones en el contexto de trabajo.  Lea los siguientes escenarios para ayudar a educar a sus usuarios para que entiendan cómo funcionan las aplicaciones administradas.

**En este tema**

[Escenario: acceso a OneDrive en un dispositivo iOS](#bkmk_OneDriveiOS)

[Escenario: acceso a OneDrive en un dispositivo Android](#bkmk_OneDriveAndroid)

[Escenario: uso de la aplicación Microsoft Word para tareas personales y de trabajo](#bkmk_wordworkandpersonal)

#### <a name="bkmk_OneDriveiOS"></a>Escenario: acceso a OneDrive en un dispositivo iOS

1.  Inicie la aplicación **OneDrive** para abrir la página de inicio de sesión.

    ![](../Image/AppManagement/iOS_OneDriveLaunch.png)

    > [!NOTE]
    > En un dispositivo personal, normalmente el usuario final descargaría la aplicación.  Si el dispositivo está administrado por una solución MDM, puede implementar la aplicación en el dispositivo.

2.  Escriba su nombre de usuario de la cuenta profesional. Se le redirigirá a la página de **Autenticación de O365** para especificar las credenciales de trabajo.

    ![](../Image/AppManagement/iOS_O365SignInPage.png)

3.  Una vez que Azure AD haya autenticado correctamente sus credenciales, se aplicarán las directivas MAM y se le solicitará reiniciar la aplicación **OneDrive**.

    ![](../Image/AppManagement/iOS_AppRestartforMAM.png)

4.  Cuando vuelva a iniciar la aplicación **OneDrive**, la aplicación se iniciará con las directivas MAM activadas. Ahora se le solicitará establecer un **PIN** para la aplicación. (si se configuró la directiva para esto).

    ![](../Image/AppManagement/iOS_AppPINPrompt.png)

5.  En cuanto establezca el PIN y confirme que es capaz de obtener acceso a los archivos de su **OneDrive para la Empresa**.

    ![](../Image/AppManagement/iOS_OneDriveSuccess.png)

    > [!NOTE]
    > Al cambiar una directiva implementada, los cambios se aplicarán la próxima vez que abra la aplicación.

#### <a name="bkmk_OneDriveAndroid"></a>Escenario: acceso a OneDrive en un dispositivo Android

1.  Inicie la aplicación OneDrive para abrir la página de inicio de sesión.

    > [!NOTE]
    > En un dispositivo personal, normalmente el usuario final descargaría la aplicación.  Si el dispositivo está administrado por una solución MDM, puede implementar la aplicación en el dispositivo.

2.  Escriba su nombre de usuario de la cuenta profesional. Se le redirigirá a la página de **Autenticación de O365** para especificar las credenciales de trabajo.

    ![](../Image/AppManagement/Android_O365SignInPage.png)

3.  Una vez que **Azure AD** autentique correctamente sus credenciales, deberá verse un mensaje con instrucciones para instalar la aplicación del portal de empresa, si no se encuentra ya instalada en el dispositivo.  Puntee en **Obtener la aplicación** para continuar.

    ![](../Image/AppManagement/Android_CompanyPortalMessage.png)

4.  Ahora accederá a la tienda **Google Play**, donde podrá descargar e instalar la aplicación **Portal de empresa**.

    La aplicación de Portal de empresa ayuda a proteger los datos.

    ![](../Image/AppManagement/Android_CompanyPortalInstall.png)

5.  Una vez haya completado la instalación, haga clic en **Aceptar** para aceptar los términos.

    ![](../Image/AppManagement/Android_CompanyPortalAccept.png)

6.  A continuación, la aplicación **OneDrive** se iniciará automáticamente.

7.  La próxima vez que abra OneDrive, se visualizará el aviso para establecer un **PIN**, siempre que la configuración de las directivas esté establecida para solicitar un PIN para acceder a la aplicación **OneDrive**.

    ![](../Image/AppManagement/Android_OneDriveSetPIN.png)

8.  Una vez que se establezca y se confirme el PIN, podrá continuar usando **OneDrive**, que ahora estará administrado por directivas de aplicaciones.

    ![](../Image/AppManagement/Android_OneDriveConfirmPIN.png)

#### <a name="bkmk_wordworkandpersonal"></a>Escenario: uso de la aplicación Microsoft Word para tareas personales y de trabajo

1.  Abra la aplicación **Word** en su dispositivo. Estamos usando un dispositivo iOS para mostrar los pasos.

2.  Puntee **Nuevo** para crear un nuevo documento de Word.

    ![](../Image/AppManagement/iOS_WordCreateNewDoc.png)

3.  Escriba una frase o dos.  Cuando guarde este documento, se mostrarán las ubicaciones personales y de trabajo como opciones para guardar el documento que acaba de crear.  En este paso, las directivas de aplicación todavía no se han aplicado, ya que todavía no se ha establecido este contexto de trabajo o personal.

4.  Guarde el documento en su OneDrive para la ubicación de la empresa. Esto ahora se etiqueta como datos de la empresa, y se aplicarán las restricciones de las directivas.

    ![](../Image/AppManagement/iOS_WordCreateCompanyDoc.PNG)

5.  Abra el documento que se guardó en su ubicación de trabajo.  Copie el texto, abra su cuenta personal de **Facebook** e intente pegar el texto copiado.  Verá que no puede pegar el contenido en la nueva publicación de Facebook. La opción Pegar no está atenuada, pero no ocurre nada al presionar **Pegar**.

    ![](../Image/AppManagement/iOS_WordCopyCompany.png)

    ![](../Image/AppManagement/iOS_FacebookPasteCompany.png)

6.  Ahora repita los pasos 2 y 3 para crear un nuevo documento, escriba una frase o dos y en lugar de guardarlo en su trabajo, guárdelo en su ubicación personal, como **OneDrive - personal**.

    ![](../Image/AppManagement/iOS_WordCopyPersonal.png)

7.  Abra el documento guardado personal.  Copie el texto, abra la aplicación de **Facebook** e intente pegar el texto copiado. Verá que se puede pegar el contenido en una publicación de Facebook.

    ![](../Image/AppManagement/iOS_FacebookPastePersonal.png)

### Cambio de una cuenta de usuario en un dispositivo
Para las aplicaciones de OneDrive y Outlook, solo se puede usar una cuenta de trabajo que tenga una directiva MAM en un dispositivo.  La adición de varias cuentas profesionales está bloqueada en estas aplicaciones.  Sin embargo, puede quitar un usuario y agregar un usuario diferente en el dispositivo.

Si usa un dispositivo iOS, cuando intente agregar una segunda cuenta profesional en el mismo dispositivo, verá un mensaje de bloqueo.  También verá una opción para quitar la cuenta existente y agregar una nueva. Puede hacerlo haciendo clic en **Sí**.

![](../Image/AppManagement/iOS_SwitchUser.PNG)

Si utiliza un dispositivo Android, verá un mensaje de bloqueo con instrucciones para quitar la cuenta existente y agregar una nueva.  En dispositivos Android, para quitar la cuenta existente, vaya a **Configuración &gt;General &gt; Administrador de aplicaciones &gt;Portal de empresa y seleccione "Borrar datos"**.

![](../Image/AppManagement/Android_SwitchUser.png)

## Vea también
[Crear e implementar directivas de administración de aplicaciones móviles con Microsoft Intune](../Topic/Create-and-deploy-mobile-app-management-policies-with-Microsoft-Intune.md)

