---
title: Habilitar la inscripci&#243;n de dispositivos m&#243;viles con el Portal de cuentas de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3adf63cd-34b6-4641-aa88-766bb59dd853
robots: noindex,nofollow
---
# Habilitar la inscripci&#243;n de dispositivos m&#243;viles con el Portal de cuentas de Microsoft Intune
Intune admite "Trae tu propio dispositivo" (BYOD, Bring Your Own Device) y permite que los usuarios inscriban sus dispositivos a través del **Portal de cuentas** de Microsoft Intune.Para poder inscribir los dispositivos, debe configurar Intune para la administración de dispositivos móviles.Si no lo ha hecho ya, configure la administración de cada plataforma de dispositivos de su organización:

-   [Administración de iOS](http://technet.microsoft.com/library/dn408185.aspx)

-   [Administración de Android](http://technet.microsoft.com/library/dn764960.aspx)

-   [Administración de Windows](http://technet.microsoft.com/library/dn764959.aspx)

## Habilitar la inscripción de dispositivos móviles con el Portal de cuentas de Intune

1.  **Agregar usuarios de Intune**
    El propietario del dispositivo móvil debe agregarse al Portal de cuentas de Microsoft Intune para poder inscribir dispositivos.Inicie sesión en el [Portal de cuentas de Microsoft Intune](http://account.manage.microsoft.com), haga clic en **Agregar usuarios** y seleccione una opción:

    -   **Usuario:** Para agregar un solo usuario, seleccione **Nuevo** &gt; **Usuario** y especifique **Detalles**, **Asignar roles** y **Establecer ubicación de usuario**; a continuación, asigne el usuario a un **Grupo**.

    -   **Agregar en masa**: cree un archivo .csv (vea los archivos de ejemplo proporcionados) e impórtelo al Portal de cuentas de Intune.Especifique los roles, la ubicación y el grupo y, después, cree las cuentas.Se pueden descargar archivos .csv en blanco y de ejemplo desde el Portal de cuentas de Microsoft Intune.

    También puede habilitar la sincronización de Active Directory o Azure Active Directory.Para obtener más información sobre la integración de otros usuarios de Azure Active Directory con Intune, consulte [Guía de sincronización de directorios](http://go.microsoft.com/fwlink/?LinkId=511540) o haga clic en **Otras formas de agregar usuarios** en el Portal de cuentas de Intune.

2.  **Crear grupos**  (opcional)
    Los grupos ofrecen flexibilidad para administrar dispositivos y usuarios.Los grupos se pueden configurar según sus necesidades de organización (por ejemplo, por ubicación geográfica, departamento o características de hardware).Consulte [Utilizar grupos para administrar usuarios y dispositivos en Microsoft Intune](../Topic/Use-groups-to-manage-users-and-devices-with-Microsoft-Intune.md).

3.  **Agregar directivas para dispositivos** (opcional)
    Las directivas son grupos de configuraciones que controlan las características de los dispositivos. La mayoría de las directivas MDM son específicas de la plataforma. Las directivas se crean mediante plantillas que contienen configuraciones recomendadas o personalizadas y, luego, se implementan en grupos. Consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

4.  **Establecer el límite de inscripción de dispositivos** (opcional) 
    Para limitar el número de dispositivos móviles que puede inscribir un usuario, inicie sesión en la [consola de administración de Microsoft Intune](http://manage.microsoft.com), haga clic en **Administración** &gt; **Administración de dispositivos móviles** &gt; **Reglas de inscripción**.Seleccione el número máximo de dispositivos que un usuario puede inscribir y haga clic en **Guardar**.

5.  **Establecer la configuración del portal de empresa** 
     Puede personalizar el portal de empresa de Intune para su empresa.En la [consola de administrador de Microsoft Intune](http://manage.microsoft.com), haga clic en **Administración** &gt; **Portal de empresa**.Configure lo siguiente

    -   **Nombre de compañía**

    -   **Nombre del contacto del departamento de TI**

    -   **Número de teléfono del departamento de TI**

    -   **Información adicional**

    -   **Dirección URL de la declaración de privacidad de la empresa**

    -   **Dirección URL del sitio web de soporte técnico (no se muestra)**

    -   **Nombre del sitio web**

6.  **Establecer los términos y condiciones**
    Puede publicar los términos y condiciones que los usuarios verán cuando usen el portal de empresa por primera vez desde cualquier dispositivo.En la [consola de administración de Microsoft Intune](http://manage.microsoft.com), haga clic en **Portal de empresa** &gt; **Términos y condiciones**.

### <a name="BKMK_TermsAndConditions"></a>Acerca de los términos y condiciones
Puede publicar los términos y condiciones que los usuarios verán cuando usen el portal de empresa por primera vez desde cualquier dispositivo, esté inscrito o no ese dispositivo.Los usuarios tendrán que aceptar estos términos para acceder al portal.Cuando realice una actualización importante de los términos y condiciones y quiera que los usuarios los vean y los acepten, puede marcar los nuevos términos y condiciones como una nueva versión y los usuarios pasarán por el mismo proceso la próxima vez que visiten el portal.

Los términos y condiciones se aplican a los usuarios, no a los dispositivos, por lo que los usuarios solo tendrán que aceptar una vez cada versión para visitar el portal de empresa desde cualquiera de sus dispositivos.

#### Informes de términos y condiciones
Los informes de **Términos y condiciones** muestran qué usuarios aceptaron los términos y condiciones, el número de versión más reciente que aceptaron y la fecha en que aceptaron esa versión.Exporte el informe para guardar un archivo de cuándo aceptaron los usuarios las versiones anteriores.Consulte [Comprender las operaciones de Microsoft Intune mediante informes](../Topic/Understand-Microsoft-Intune-operations-by-using-reports.md).

### Cómo inscriben los usuarios sus dispositivos móviles
Una vez configurada la inscripción, puede invitar a los usuarios a que inscriban sus dispositivos.Para obtener instrucciones para ayudar a los usuarios a inscribir sus dispositivos personales, descargue [Instrucciones de inscripción para Microsoft Intune](http://go.microsoft.com/fwlink/?LinkID=534864).También puede consultar [Qué decirles a los usuarios finales sobre el uso de Microsoft Intune](../Topic/What-to-tell-your-end-users-about-using-Microsoft-Intune.md).

Instrucciones generales:

1.  Los usuarios inscriben y administran sus dispositivos móviles con la aplicación Portal de empresa.Los usuarios también pueden usar el sitio web de Portal de empresa para inscribir dispositivos.

    -   **Android**: los usuarios instalan la aplicación **Portal de empresa** de Microsoft Corporation, disponible en [Google Play](http://go.microsoft.com/fwlink/p/?LinkId=386612).

    -   **iOS**: los usuarios instalan la aplicación **Portal de empresa** de Microsoft Corporation disponible en el App Store.Los usuarios pueden ver sus **Dispositivos** para inscribir sus teléfonos.

    -   **Windows Phone 8.1**: los usuarios instalan la aplicación **Portal de empresa** de Microsoft Corporation disponible en la tienda de Windows Phone.Si se distribuye una aplicación de portal de empresa firmada, los usuarios también pueden ir a **Configuración** &gt; **Área de trabajo** &gt; **Agregar cuenta**, iniciar sesión y, después, pulsar en **Instalar aplicación o hub de la empresa** para instalar Portal de empresa.

    -   **Windows Phone 8.0**  Los usuarios deben hacer clic en **configuración del sistema** &gt; **aplicaciones de empresa** e iniciar sesión usando el identificador de usuario.La aplicación Portal de empresa se implementa en los teléfonos de los usuarios.

    -   **Windows 8.1 y Windows RT 8.1**: los usuarios descargan la aplicación **Portal de empresa** de la Tienda Windows.Si se distribuyó una aplicación de portal de empresa firmada, los usuarios también pueden ir a **Configuración de PC** &gt; **Red** &gt; **Área de trabajo**, iniciar sesión, marcar la casilla **Permitir aplicaciones y servicios del administrador de TI** y hacer clic en **Unirse**.

    -   **Windows RT**: haga clic en **Inicio**, escriba "Configuración del sistema" y haga clic en el cuadro de diálogo para abrir las **Aplicaciones de empresa**.

2.  Cuando los usuarios abran el Portal de empresa, se les pedirá las credenciales.Si no creó un CNAME de dominio público, se pedirá a los usuarios de Windows y Windows Phone la dirección del servidor, y deben escribir "manage.microsoft.com".Después, los usuarios de teléfonos Windows Phone 8.1 e iOS pueden ver sus **Dispositivos inscritos** para inscribir su teléfono.

3.  Cuando un usuario se inscribe por primera vez, o si se requirió la aceptación de una nueva versión de los términos y condiciones, los usuarios deben aceptar dichos términos y condiciones.El dispositivo se inscribe tanto si aceptan los términos como si no.Si los acepta, puede seguir al portal.Si los rechaza, se le pide que confirme que quiere rechazar y, después, se le proporciona un vínculo con instrucciones sobre cómo anular la inscripción.La inscripción no se anula automáticamente y hasta que anule la inscripción puede seguir administrando el dispositivo.

    En este punto, el proceso es diferente para los dispositivos que aún no se han inscrito, según el sistema operativo del dispositivo.

    -   En el caso de los dispositivos Windows y Windows Phone 8.1, el Portal de empresa recordará al usuario que se inscriba.Windows Phone 8.1 tendrá un vínculo a la configuración de la inscripción y Windows tendrá un vínculo a contenido de ayuda que describe cómo inscribirse.

    -   En el caso de los dispositivos iOS y Android, se dirige al usuario por el proceso de inscripción.Los usuarios seguirán viendo un mensaje de Microsoft sobre el efecto de la inscripción.

> [!CAUTION]
> Los usuarios de Windows y Windows Phone pueden encontrarse con la interfaz de inscripción e inscribirse sin llegar a ver los términos y condiciones.Aconseje a los usuarios que comiencen en la Tienda Windows o en la Tienda de Windows Phone para aumentar la visibilidad y la aceptación de los términos y condiciones.

**Una vez inscritos los dispositivos, puede:**

-   [Supervisar dispositivos móviles con Microsoft Intune](../Topic/Understand-your-devices-with-inventory-in-Microsoft-Intune.md)

-   [Habilitar el acceso a los recursos de empresa con Microsoft Intune](../Topic/Enable-access-to-company-resources-with-Microsoft-Intune---deleted.md)

-   [Implementar aplicaciones en dispositivos móviles en Microsoft Intune](../Topic/Deploy-apps-to-mobile-devices-in-Microsoft-Intune---deleted.md)

-   [Administrar la configuración y las características de los dispositivos con directivas de Microsoft Intune](../Topic/Manage-settings-and-features-on-your-devices-with-Microsoft-Intune-policies.md)

-   [Ayude a proteger sus datos mediante la eliminación remota, el bloqueo remoto o el restablecimiento de código de acceso mediante Microsoft Intune.](../Topic/Help-protect-your-data-with-remote-wipe,-remote-lock,-or-passcode-reset-using-Microsoft-Intune.md)

## Vea también
[Preparar la inscripción de dispositivos en Microsoft Intune](../Topic/Get-ready-to-enroll-devices-in-Microsoft-Intune.md)
[Inscribir dispositivos propiedad de la empresa con el Administrador de inscripción de dispositivos de Microsoft Intune](../Topic/Enroll-corporate-owned-devices-with-the-Device-Enrollment-Manager-in-Microsoft-Intune.md)
[Cómo comprar Intune](http://technet.microsoft.com/library/dn646949.aspx)

