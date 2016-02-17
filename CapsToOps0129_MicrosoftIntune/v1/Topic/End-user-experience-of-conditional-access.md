---
title: Experiencia de acceso condicional del usuario final
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3e186dd2-e17c-40d8-b160-48038b2c6593
---
# Experiencia de acceso condicional del usuario final
En este tema se describe la experiencia del usuario final después de que se habilite el acceso condicional y de que un usuario final intente obtener acceso al correo electrónico en su dispositivo móvil.

> [!TIP]
> Obtenga una copia descargable de este tema completo en la [Galería de TechNet](https://gallery.technet.microsoft.com/Deploying-Enterprise-16499404).

## Windows Phone
> [!NOTE]
> El proceso de inscripción y las pantallas que ve el usuario pueden variar ligeramente en función de la versión del sistema operativo que se ejecuta en el dispositivo del usuario final.

1.  Si un usuario ya está inscrito en Intune y es compatible, no verá ninguna diferencia en los dispositivos Windows; seguirá pudiendo obtener acceso al correo electrónico. Los usuarios que aún no se hayan inscrito en Intune recibirán un correo electrónico de cuarentena parecido al de este ejemplo:

    ![](../Image/CA-EUX/EUX_Windows_quarantineEmail.png)

    El usuario hace clic en **Empezar ahora** para comenzar la inscripción del dispositivo.

2.  En la pantalla Configuración de acceso a la empresa, el usuario hace clic en **Empezar** para iniciar la configuración de su dispositivo y comprobar si es compatible.

    ![](../Image/CA-EUX/EUX_Windows_1_companyAccessSetup.png)

3.  En la pantalla Inscribir un dispositivo, el usuario hace clic en **Confirmar inscripción** para iniciar la inscripción de su dispositivo.

    ![](../Image/CA-EUX/EUX_Windows_3_enrollDevice.png)

    Durante la inscripción, se instala el perfil de administración de dispositivos móviles, que permite al administrador de TI administrar el dispositivo de forma remota. Podría pedirse al usuario que acepte un certificado que autoriza la Unión al área de trabajo.

    ![](../Image/CA-EUX/EUX_Windows_4_workplaceJoin1.png)

4.  El usuario inicia sesión con la dirección de correo electrónico que usa con Office. Después de iniciar la sesión, es posible que tenga que hacer clic en **Confirmar inscripción** otra vez para continuar con la inscripción del dispositivo.

    ![](../Image/CA-EUX/EUX_Windows_5_workplaceJoin2.png)

    Se comprueba el dispositivo para garantizar que se ha inscrito.

    ![](../Image/CA-EUX/EUX_Windows_6_checkingEnrollment.png)

5.  Luego, el usuario completa el proceso de inscripción seleccionando su dispositivo y haciendo clic en **Seleccionar**. Si el dispositivo no aparece, puede seleccionar **Mi dispositivo no está en la lista** para intentarlo de nuevo.

    ![](../Image/CA-EUX/EUX_Windows_7_confirmDevice.png)

    El dispositivo se comprueba para garantizar su conformidad con las directivas de la empresa.

    ![](../Image/CA-EUX/EUX_Windows_9_checkingCompliance.png)

6.  Si hay un problema de cumplimiento, se pedirá al usuario que resuelva el problema (por ejemplo, creando una contraseña válida) y que haga clic en **Comprobar cumplimiento** para continuar.

    ![](../Image/CA-EUX/EUX_Windows_13_resolveCompliance.png)

    Después de comprobar el cumplimiento, el usuario verá que la inscripción se está activando.

    ![](../Image/CA-EUX/EUX_Windows_10_activatingEnrollment.png)

7.  Se activa la inscripción y el usuario hace clic en **Continuar** para completar el proceso. Luego, el usuario hace clic en **Listo** para salir de la instalación.

    ![](../Image/CA-EUX/EUX_Windows_11_COMPLETE.png)

    Después de inscribir al usuario y de comprobar el cumplimiento, el acceso al correo electrónico debería estar disponible en cuestión de minutos.

Si el usuario sigue estos pasos para inscribirse y comprobar el cumplimiento, pero sigue sin tener acceso al correo electrónico en su dispositivo móvil, puede seguir estos pasos adicionales para intentar solucionar el problema:

-   En primer lugar, compruebe que el dispositivo está inscrito. De lo contrario, el usuario seguirá los pasos ya descritos.

-   Compruebe que el dispositivo cumple las normas haciendo clic en **Comprobar cumplimiento**. Si se identifica un error de cumplimiento, el usuario puede seguir las instrucciones sobre cómo resolverlo específicas para su dispositivo móvil como, por ejemplo, de qué manera restablecer la contraseña.

-   Llame al departamento de soporte técnico.

### Si un dispositivo no cumple las normas
Cada 8 horas, de forma predeterminada, se comprueban los dispositivos para garantizar que siguen cumpliendo las normas. Si un dispositivo que cumplía las normas pasa a considerarse no conforme (por ejemplo, si se agrega o se modifica una directiva de cumplimiento), el usuario puede seguir estos pasos para volver al cumplimiento:

1.  El usuario recibe la notificación, en el correo electrónico o en el dispositivo, que indica que el dispositivo no cumple las normas. En este momento, el dispositivo se pone en cuarentena en Exchange.

2.  Si el usuario intenta obtener acceso al correo electrónico, se le redirige a la pantalla Configuración de acceso a la empresa desde el portal de empresa de Intune, donde se muestra la falta de cumplimiento.

    ![](../Image/CA-EUX/EUX_Windows_14_OutOfCompliance.png)

3.  El usuario hace clic en **Continuar** y aparece el problema de cumplimiento que impide el acceso al correo electrónico.

4.  Una vez solucionado el problema, el usuario hace clic en **Comprobar cumplimiento** para comprobar que se ha resuelto el problema.

5.  Si el problema está solucionado, el usuario hace clic en **Continuar** para completar el proceso. El correo electrónico debería estar disponible de nuevo tras unos minutos.

## iOS
> [!NOTE]
> El proceso de inscripción y las pantallas que ve el usuario pueden variar ligeramente en función de la versión del sistema operativo que se ejecuta en el dispositivo del usuario final.

1.  Si un usuario ya está inscrito en Intune y cumple las normas, no verá ninguna diferencia en los dispositivos iOS; seguirá pudiendo obtener acceso al correo electrónico. Si el usuario todavía no está inscrito, verá un mensaje de cuarentena similar al siguiente al iniciar la aplicación de correo electrónico:

    ![](../Image/CA-EUX/EUX_iOS_GetStarted.PNG)

    El usuario hace clic en **Empezar ahora** para comenzar la inscripción del dispositivo.

2.  Se pedirá al usuario que instale la aplicación Portal de empresa de Intune desde la tienda de aplicaciones correspondiente.

    ![](../Image/CA-EUX/EUX_iOS_intuneCompanyPortal.png)

    Después, el usuario abre la aplicación e inicia la sesión con las credenciales de empresa.

3.  En la pantalla Configuración de acceso a la empresa, el usuario hace clic en **Empezar** para iniciar la configuración de su dispositivo y comprobar si es compatible.

    ![](../Image/CA-EUX/EUX_iOS_companyAccessSetup.png)

4.  En la pantalla Inscripción de dispositivos, el usuario hace clic en **Inscripción** para iniciar la inscripción de su dispositivo.

    ![](../Image/CA-EUX/EUX_iOS_deviceEnrollment.png)

    Durante la inscripción, se instala el perfil de administración de dispositivos móviles, que permite al administrador de TI administrar el dispositivo de forma remota. El usuario escribe su contraseña si se le solicita.

5.  En la pantalla Configuración de acceso a la empresa, el usuario hace clic en **Continuar** para iniciar la comprobación de cumplimiento en el dispositivo.

    ![](../Image/CA-EUX/EUX_iOS_deviceComplianceCheck.png)

    Si hay un problema de cumplimiento, se pedirá al usuario que resuelva el problema (por ejemplo, creando una contraseña válida) y que haga clic en **Comprobar cumplimiento** para continuar.

    ![](../Image/CA-EUX/EUX_iOS_checkCompliance.png)

6.  Cuando el dispositivo cumpla todas las normas, el usuario hará clic en **Continuar** para seguir.

    ![](../Image/CA-EUX/EUX_iOS_complianceCheckCompleted.png)

    Después de inscribir al usuario y de comprobar el cumplimiento, el acceso al correo electrónico debería estar disponible en cuestión de minutos.

Si el usuario sigue estos pasos para inscribirse y comprobar el cumplimiento, pero sigue sin tener acceso al correo electrónico en su dispositivo móvil, puede seguir estos pasos adicionales para intentar solucionar el problema:

-   En primer lugar, compruebe que el dispositivo está inscrito. De lo contrario, el usuario seguirá los pasos ya descritos.

-   Compruebe que el dispositivo cumple las normas haciendo clic en **Comprobar cumplimiento**. Si se identifica un error de cumplimiento, el usuario puede seguir las instrucciones sobre cómo resolverlo específicas para su dispositivo móvil como, por ejemplo, de qué manera restablecer la contraseña.

-   Llame al departamento de soporte técnico.

### Si un dispositivo no cumple las normas
Cada 8 horas, de forma predeterminada, se comprueban los dispositivos para garantizar que siguen cumpliendo las normas. Si un dispositivo que cumplía las normas pasa a considerarse no conforme (por ejemplo, si se agrega o se modifica una directiva de cumplimiento), el usuario puede seguir estos pasos para volver al cumplimiento:

1.  El usuario recibe la notificación, en el correo electrónico o en el dispositivo, que indica que el dispositivo no cumple las normas. En este momento, el dispositivo se pone en cuarentena en Exchange.

2.  Si el usuario intenta obtener acceso al correo electrónico, se le redirige a la pantalla Configuración de acceso a la empresa desde el portal de empresa de Intune, donde se muestra la falta de cumplimiento.

    ![](../Image/CA-EUX/EUX_iOS_fallOutCompliance.png)

3.  El usuario hace clic en **Continuar** y aparece el problema de cumplimiento que impide el acceso al correo electrónico.

    ![](../Image/CA-EUX/EUX_iOS_checkCompliance.png)

4.  Una vez solucionado el problema, el usuario hace clic en **Comprobar cumplimiento** para comprobar que se ha resuelto el problema.

5.  Si el problema está solucionado, el usuario hace clic en **Continuar** para completar el proceso.

    ![](../Image/CA-EUX/EUX_iOS_complianceCheckCompleted.png)

    El correo electrónico debería estar disponible de nuevo tras unos minutos.

## Android
> [!NOTE]
> El proceso de inscripción y las pantallas que ve el usuario pueden variar ligeramente en función de la versión del sistema operativo que se ejecuta en el dispositivo del usuario final.

1.  Al intentar obtener acceso al correo electrónico, el usuario recibe por primera vez un correo electrónico de cuarentena parecido al de este ejemplo:

    ![](../Image/CA-EUX/EUX_Android_quarantineEmail.png)

    El usuario hace clic en **Empezar ahora** para comenzar la inscripción del dispositivo.

    > [!NOTE]
    > Si un usuario no ha establecido un explorador predeterminado para su dispositivo, se le pedirá durante la inscripción del dispositivo y durante la activación de la inscripción que permita que un vínculo abra una ventana del explorador. Debe seleccionar el mismo explorador cada vez que se le pida o se producirá un error en el proceso de inscripción.

2.  Se pedirá al usuario que instale la aplicación Portal de empresa de Intune desde la tienda de aplicaciones correspondiente.

    ![](../Image/CA-EUX/EUX_AndroidPortal.png)

    Después, el usuario abre la aplicación e inicia la sesión con las credenciales de empresa.

3.  En la pantalla Configuración de acceso a la empresa, el usuario hace clic en **Empezar** para iniciar la configuración de su dispositivo y comprobar si es compatible.

    ![](../Image/CA-EUX/EUX_Android_companyAccessSetup.PNG)

4.  En la pantalla Inscripción de dispositivos, el usuario hace clic en **Inscripción** para iniciar la inscripción de su dispositivo.

    ![](../Image/CA-EUX/EUX_Android_deviceEnroll.png)

5.  Los usuarios tienen que activar el administrador de dispositivos. Para ello, solo tienen que hacer clic en **Activar** cuando se le pida. De lo contrario, se cancelará el procedimiento de inscripción de dispositivos.

    ![](../Image/CA-EUX/EUX_Android_activateDeviceAdmin.PNG)

    Empieza la inscripción de dispositivos En función del dispositivo, durante la inscripción puede aparecer un mensaje de instalación del certificado o un mensaje de directiva de privacidad de Samsung KNOX. Todo esto es necesario para que el administrador de TI pueda administrar el dispositivo de forma remota. El dispositivo está inscrito en Intune y establece una identidad de dispositivo con Azure Active Directory.

    ![](../Image/CA-EUX/EUX_Android_enrollingDevice.png)

6.  Una vez completada correctamente la inscripción, el usuario hace clic en **Continuar** para empezar la comprobación de cumplimiento en el dispositivo.

    ![](../Image/CA-EUX/EUX_Android_enrollSuccess.png)

    Si hay un problema de cumplimiento, se pedirá al usuario que resuelva el problema (por ejemplo, creando una contraseña válida) y que haga clic en **Comprobar cumplimiento** para continuar.

    ![](../Image/CA-EUX/EUX_Android_resolveComplianceIssues.png)

7.  Cuando el dispositivo cumpla todas las normas, el usuario hará clic en **Continuar** para iniciar la activación de la inscripción. Así, se conectará la identidad del dispositivo AAD con el EASID ofrecido por Exchange.

    > [!NOTE]
    > En Android, el explorador predeterminado aparecerá durante unos segundos mientras se activa la inscripción. Si el usuario no ha elegido ya un explorador predeterminado, se le pedirá que elija un explorador. Mientras completa la Configuración de acceso a la empresa, el usuario tiene que elegir el mismo explorador siempre que se le pida.

    ![](../Image/CA-EUX/EUX_Android_complianceSuccessful.PNG)

8.  La activación de la inscripción se completa y el usuario hace clic en **Listo** para salir del proceso de inscripción y comprobación del cumplimiento.

    ![](../Image/CA-EUX/EUX_Android_allSuccessful2.PNG)

    Después de inscribir al usuario y de comprobar el cumplimiento, el acceso al correo electrónico debería estar disponible en cuestión de minutos.

Si el usuario sigue estos pasos para inscribirse y comprobar el cumplimiento, pero sigue sin tener acceso al correo electrónico en su dispositivo móvil, puede seguir estos pasos adicionales para intentar solucionar el problema:

1.  En primer lugar, compruebe que el dispositivo está inscrito. De lo contrario, el usuario seguirá los pasos ya descritos.

2.  Compruebe que el dispositivo cumple las normas haciendo clic en **Comprobar cumplimiento**. Si se identifica un error de cumplimiento, el usuario puede seguir las instrucciones sobre cómo resolverlo específicas para su dispositivo móvil como, por ejemplo, de qué manera restablecer la contraseña.

3.  Llame al departamento de soporte técnico.

### Si un dispositivo no cumple las normas
Cada 8 horas, de forma predeterminada, se comprueban los dispositivos para garantizar que siguen cumpliendo las normas. Si un dispositivo que cumplía las normas pasa a considerarse no conforme (por ejemplo, si se agrega o se modifica una directiva de cumplimiento), el usuario puede seguir estos pasos para volver al cumplimiento:

1.  El usuario recibe la notificación, en el correo electrónico o en el dispositivo, que indica que el dispositivo no cumple las normas. En este momento, el dispositivo se pone en cuarentena en Exchange.

2.  Cuando el usuario intente obtener acceso al correo electrónico, verá un correo electrónico de cuarentena que le informa de que, para poder obtener acceso, es necesario solucionar los problemas de cumplimiento. Cuando el usuario hace clic en el hipervínculo del correo electrónico de cuarentena, llega a la pantalla Configuración de acceso a la empresa en el portal de empresa de Intune (mediante el explorador predeterminado y Google Play), donde se muestra que el dispositivo no cumple las normas.

    ![](../Image/CA-EUX/EUX_Android_outOfCompliance.png)

3.  El usuario hace clic en **Continuar** y aparece el problema de cumplimiento que impide el acceso al correo electrónico.

    ![](../Image/CA-EUX/EUX_Android_resolveComplianceIssues.png)

4.  Una vez solucionado el problema, el usuario hace clic en **Comprobar cumplimiento** para comprobar que se ha resuelto el problema.

5.  Si el problema está solucionado, el usuario hace clic en **Continuar** para completar el proceso. El correo electrónico debería estar disponible de nuevo tras unos minutos.

## Vea también
[Aprenda a implementar una solución para proteger los documentos y correos electrónicos de su empresa](../Topic/Learn-how-to-deploy-a-solution-for-protecting-company-email-and-documents.md)
[Usar acceso condicional con Intune y Configuration Manager](../Topic/Use-conditional-access-with-Intune-and-Configuration-Manager.md)

