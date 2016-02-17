---
title: Caracter&#237;sticas de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 118a36f6-02c6-4e99-9c72-0b9daddc3b03
robots: noindex,nofollow
---
# Caracter&#237;sticas de Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] proporciona un servicio basado en la nube que puede ayudar a su empresa a proteger y administrar dispositivos. Como está basado en la nube, se puede administrar desde cualquier explorador web habilitado para Silverlight. [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] puede administrar:

-   **Dispositivos móviles** (incluidos los teléfonos y las tabletas que ejecutan los sistemas operativos Android, iOS, Windows Phone y Windows RT) Los equipos que ejecutan Windows 8.1 se pueden administrar como dispositivos móviles o como equipos que utilizan el software cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

-   Los **equipos** que ejecutan una edición profesional de Windows Vista, Windows 7, Windows 8 o Windows 8.1.

Para obtener más información acerca de los dispositivos móviles y equipos que se pueden administrar con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Capacidades de administración de dispositivos móviles en Microsoft Intune](../Topic/Mobile-device-management-capabilities-in-Microsoft-Intune.md) y [Funciones de administración de equipos Windows en Microsoft Intune](../Topic/Windows-PC-management-capabilities-in-Microsoft-Intune.md).

En esta guía de evaluación se tratan los temas siguientes:

-   [Capacidades de Intune](../Topic/Microsoft-Intune-features.md#WIT_Cap)

-   [Administración de Intune](../Topic/Microsoft-Intune-features.md#WIT_Adm)

-   [Versión de evaluación gratuita y precios de Intune](../Topic/Microsoft-Intune-features.md#WIT_Fre)

## <a name="WIT_Cap"></a>Capacidades de Intune
**Capacidades generales:**

-   **Administre dispositivos móviles y equipos sin necesidad de usar servidores ni una intranet.** Puede administrar dispositivos móviles y equipos, aunque esos dispositivos no se hayan unido a un dominio ni se utilicen in situ. Por esta razón [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] es ideal para una empresa cuyo personal es móvil o está distribuido geográficamente.

-   **Exigir el cifrado de dispositivos móviles y equipos.** Se puede exigir que los dispositivos móviles que admiten el cifrado lo utilicen. También se puede exigir que los equipos que admiten el cifrado de unidad Bitlocker lo utilicen. Si se extravía o roban un dispositivo móvil o un equipo con cifrado, los datos del medio de almacenamiento del dispositivo serán ilegibles, lo que contribuye a proteger los datos.

-   **Genere informes e inventarios de hardware y software.** Puede recopilar información sobre el hardware y el software utilizados en su empresa como ayuda para planear un clico de actualización de hardware o para determinar si se ha instalado software no deseado en dispositivos administrados.

-   **Supervisar dispositivos móviles y equipos.** Puede crear alertas que le notifiquen cuando se produzca un problema en un dispositivo móvil o un equipo, y hacer que las alertas desencadenen notificaciones por correo electrónico para comunicar el problema a las personas adecuadas.

-   **Proporciona un modelo de "autoservicio" para TI.** Los usuarios pueden utilizar el portal de empresa para inscribir dispositivos, instalar software con licencia para el sitio, o buscar información de contacto para administradores de TI.

-   **Admite autenticación multifactor.** [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ahora admite autenticación multifactor. Para obtener más información, consulte [Usar la autenticación multifactor en Microsoft Intune](../Topic/Protect-Windows-devices-with-multi-factor-authentication.md).

-   **Está disponible en varios idiomas.** Intune ahora está disponible en los siguientes idiomas:

    -   Chino (simplificado y tradicional)

    -   Checo

    -   Danés

    -   Neerlandés

    -   Inglés

    -   Finés

    -   Francés

    -   Alemán

    -   Griego

    -   Húngaro

    -   Italiano

    -   Japonés

    -   Coreano

    -   Noruego

    -   Polaco

    -   Portugués

    -   Rumano

    -   Ruso

    -   Español

    -   Sueco

    -   Turco

Para obtener una lista de los países donde se admite el servicio [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Disponibilidad internacional](https://products.office.com/en-us/business/international-availability).

**Capacidades de administración de dispositivos móviles (MDM):**

-   **Configurar las contraseñas.** Las capacidades de administración de contraseñas varían ligeramente de una plataforma para dispositivos móviles a otra, pero todas las plataformas compatibles permiten exigir una contraseña, limitar el número de intentos de inicio de sesión con error, limitar los minutos de actividad antes de que la pantalla se bloquee, establecer el plazo de expiración de una contraseña e impedir el uso de contraseñas usadas previamente.

-   **Controlar la configuración del sistema y del almacenamiento en nube para dispositivos móviles.** Esta configuración varía de una plataforma de dispositivos móviles a otra, pero la información destacada incluye la posibilidad de bloquear la vista de notificaciones en pantalla de iOS (para mantener la confidencialidad de los detalles de una reunión) y la posibilidad de recopilar datos de diagnóstico de dispositivos Windows Phone 8.1 e iOS.

-   **Administrar el acceso a correo electrónico para dispositivos móviles utilizando Exchange ActiveSync.** Puede controlar la configuración de acceso al correo electrónico para establecer, por ejemplo, si los dispositivos pueden descargar datos adjuntos o qué parte de una carpeta de correo electrónico se sincroniza con un dispositivo móvil.

-   **Configuración de aplicaciones.** Puede controlar la configuración del explorador y de aplicaciones, para establecer, por ejemplo, si se pueden utilizar tiendas de aplicaciones en los dispositivos móviles.

-   **Capacidades de dispositivo, móvil y voz.** Puede permitir o prohibir el uso de una cámara, controlar la configuración de roaming y habilitar o deshabilitar el asistente de voz de iOS y las características de marcación por voz.

-   **Restablecer, bloquear o eliminar códigos de acceso.** Puede restablecer los códigos de acceso si los usuarios dejan de tener acceso a sus dispositivos, bloquear dispositivo que faltan o han sido robados, e incluso borrar los datos de dispositivos que faltan o han sido robados.

-   **Certificado, correo electrónico, perfiles de VPN y Wi-Fi.** Puede implementar perfiles de certificados en dispositivos móviles y también implementar correo electrónico, perfiles de VPN y Wi-Fi. Consulte [Habilitar el acceso a los recursos de empresa con Microsoft Intune](../Topic/Enable-access-to-company-resources-with-Microsoft-Intune---deleted.md).

-   **Administrar dispositivos iOS propiedad de la empresa** Puede configurar dispositivos para la inscripción y distribuirlos después a usuarios específicos, o bien puede inscribir dispositivos para que los puedan compartir varios usuarios. Consulte [Inscribir dispositivos iOS de empresa en Microsoft Intune](../Topic/Enroll-corporate-owned-iOS-devices-in-Microsoft-Intune.md).

-   **Administración de aplicaciones móviles.** Las aplicaciones móviles administradas pueden configurarse para restringir ciertas operaciones de aplicaciones, como copiar y pegar, para ayudar a proteger los datos de su organización. También puede usar el explorador administrado para controlar los sitios que pueden visitar los usuarios. Consulte [Proteger datos mediante las directivas de administración de aplicaciones móviles con Microsoft Intune](../Topic/Configure-and-deploy-mobile-application-management-policies-in-the-Microsoft-Intune-console.md) y [Administrar el acceso a Internet mediante directivas de explorador administrado con Microsoft Intune](../Topic/Manage-Internet-access-using-managed-browser-policies-with-Microsoft-Intune.md).

-   **Acceso condicional.** Utilice las directivas de acceso condicional de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] para controlar el acceso a correo electrónico de Microsoft Exchange local desde dispositivos móviles, incluso cuando el dispositivo no se administre mediante Intune. Consulte [Administrar el acceso al correo electrónico y SharePoint con Microsoft Intune](../Topic/Manage-access-to-email-and-SharePoint-with-Microsoft-Intune.md).

Para obtener una lista completa de capacidades de MDM, consulte [Capacidades de administración de dispositivos móviles en Microsoft Intune](../Topic/Mobile-device-management-capabilities-in-Microsoft-Intune.md).

**Capacidad de administración de equipos de Intune:**

-   **Administrar actualizaciones de software.** Puede mantener actualizados los equipos y administrar la aplicación de actualizaciones.

-   **Establezca la directiva de Firewall de Windows.** Esto ayuda a garantizar que ningún equipo usado en su empresa tenga un firewall inactivo o mal configurado.

-   **Protección antimalware.**[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] incluye [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Endpoint Protection y permite establecer directivas para garantizar que los equipos se mantengan protegidos con las actualizaciones de definiciones antimalware más recientes.

-   **Asistencia remota.**[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]permite a los usuarios ponerse en contacto con el personal de soporte de TI, que puede proporcionar asistencia mediante una característica de escritorio remoto incluida en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

-   Administración de **licencias de software**.  Realice el seguimiento del número de licencias de software disponibles y el número de licencias disponibles que se usan.

Para obtener una lista completa de capacidades de administración de equipos, consulte [Funciones de administración de equipos Windows en Microsoft Intune](../Topic/Windows-PC-management-capabilities-in-Microsoft-Intune.md).

## <a name="WIT_Adm"></a>Administración de Intune
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] tiene una gran variedad de áreas de trabajo de administración que ofrecen capacidades que puede utilizar para administrar dispositivos móviles y equipos. En el tutorial se presentan los conceptos básicos. Para obtener más información, consulte [Referencia de las consolas de administración de Microsoft Intune](../Topic/Reference-for-the-Microsoft-Intune-administrative-consoles.md)

|Característica|Capacidades|
|------------------|---------------|
|**Portal de cuentas**|El [Portal de cuentas de Intune](http://go.microsoft.com/fwlink/?LinkID=232813) le permite administrar su suscripción de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] y especificar los usuarios con acceso a [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Desde el [!INCLUDE[wit_icp_2](../Token/wit_icp_2_md.md)] puede administrar el servicio y los usuarios mediante la adición de cuentas de usuario y grupos de seguridad, la configuración y administración de las opciones de los servicios, así como la comprobación del estado del servicio [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. También puede ponerse en contacto con el soporte técnico de Microsoft y obtener ayuda de la comunidad en línea de Microsoft. Los usuarios pueden acceder al [!INCLUDE[wit_icp_2](../Token/wit_icp_2_md.md)] para cambiar su contraseña.<br /><br />Para obtener más información acerca del [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)] consulte la [ayuda de Azure Active Directory](http://go.microsoft.com/fwlink/?LinkID=248116). En la ayuda de Azure Active Directory se ofrece orientación sobre Microsoft Online Services, por ejemplo, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], y Microsoft Office 365. También se tratan los temas siguientes: .<br /><br />-   Suscripción a un servicio de Microsoft Online<br />-   Administración de la cuenta<br />-   Inicio de sesión<br />-   Asignación de roles de administrador para Microsoft Online Services<br />-   Cambio de contraseñas de los usuarios|
|**Consola del administrador:**<br />**área de trabajo Información general**|Le permite evaluar rápidamente el estado de los dispositivos administrados en toda la organización. Entre las principales tareas se incluyen:<br /><br />-   Ver un resumen de los primeros tipos de alerta<br />-   Comprobar el estado del sistema de varias áreas clave<br />-   Ver resúmenes de los dispositivos que administra<br />-   Crear un nuevo grupo de dispositivos o de usuarios<br />-   Ver un informe<br /><br />Si se produce un problema, los vínculos aparecen en la zona afectada para que se pueda dirigir directamente al área de trabajo correspondiente para investigar y resolver el problema.|
|**Consola del administrador: áreas de trabajo**<br />**Todos los usuarios**<br />y<br />**Todos los dispositivos**|Estas áreas de trabajo le permiten administrar los dispositivos y usuarios organizándolos en grupos. Puede organizar los grupos de la forma que mejor se ajuste a sus necesidades de organización (por ejemplo, por ubicación geográfica, departamento o características de hardware). Un dispositivo o un usuario pueden pertenecer a más de un grupo.|
|**Consola de administrador:**<br /> **Área de trabajo Actualizaciones**|Administre el proceso de actualización de software de manera eficaz para todos los dispositivos administrados de la organización. Entre las principales tareas se incluyen:<br /><br />-   Ver las actualizaciones pendientes<br />-   Aprobar o rechazar actualizaciones<br />-   Configurar las opciones de aprobación automática de actualizaciones<br />-   Establecer una fecha límite para la instalación de una actualización|
|**Consola del administrador:**<br />**área de trabajo Protección**|Ayuda a mejorar la seguridad de todos los equipos administrados de la organización al<br /><br />-   proporcionar protección en tiempo real contra amenazas potenciales,<br />-   mantener actualizadas las definiciones de software malintencionado<br />-   y ejecutar automáticamente análisis programados.<br /><br />Esta área de trabajo proporciona resúmenes de estado de Endpoint Protection, de modo que si se detecta software malintencionado en un equipo administrado, o si un equipo no está protegido, se puede identificar rápidamente y tomar las medidas correspondientes.|
|**Consola de administrador:**<br /> **Área de trabajo Alertas**|Evalúe rápidamente el estado general de los equipos administrados de la organización. Reaccione ante los problemas para que pueda evitar o minimizar sus efectos negativos sobre las operaciones empresariales. Por ejemplo, puede:<br /><br />-   Ver todas las alertas recientes para obtener una visión general del estado de todos los dispositivos administrados<br />-   Investigar problemas específicos que se están produciendo en miembros de grupos específicos de dispositivos administrados (o bien, en áreas de trabajo específicas, como el área de trabajo **Endpoint Protection**)<br />-   Utilizar filtros para ver todas las alertas con un nivel de gravedad específico o para revisar la lista de alertas activas o cerradas<br />-   Notificar las alertas a las personas que correspondan, utilizando las reglas de notificación de alertas para que [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] envíe notificaciones por correo electrónico sobre tipos específicos de alertas a las personas adecuadas|
|**Consola de administrador:**<br /> **Área de trabajo Software**|Detecte y administre software para todos los dispositivos administrados. En esta área de trabajo puede:<br /><br />-   Obtener un inventario de todo el software instalado en los equipos (no está disponible para dispositivos móviles)<br />-   Distribuir el software en los equipos, con la opción de exigir la instalación del software en los equipos (e instalar dicho software sin la intervención del usuario final)<br />-   Implementar paquetes de software administrado<br />-   Crear un vínculo a una aplicación basada en web o una aplicación de la Tienda Windows para las plataformas Windows, Windows RT, Windows Phone 8 y Windows Phone 8.1; crear un vínculo a una aplicación de la iTunes Store para iOS, o vínculo a una aplicación de Google Play para la plataforma Android<br />-   Buscar, ordenar y filtrar las listas de software administrado o software detectado|
|**Consola de administrador:**<br /> **Área de trabajo Licencias**|Agregue y administre información sobre contratos de licencia de software adquiridos a través de los contratos de licencias por volumen de Microsoft, así como del software de Microsoft o de terceros que se adquirió por otros medios. En esta área de trabajo puede:<br /><br />-   Introducir y administrar licencias<br />-   Comparar el conjunto de licencias de Microsoft en el área de trabajo para el inventario de software detectado en los equipos administrados<br />-   Crear informes de licencia para hacer un seguimiento de la instalación de software y los recuentos de licencias|
|**Consola de administrador:**<br /> **Área de trabajo Directiva**|Proporciona la configuración que controla las actualizaciones de software, Endpoint Protection, Firewall de Windows y la configuración de seguridad en dispositivos móviles.|
|**Consola de administrador:**<br /> **Área de trabajo Informes**|Ejecute informes que proporcionen información sobre el software y las licencias de hardware y software de la organización.|
|**Consola de administrador:**<br /> **Área de trabajo Administración**|Vea detalles sobre su cuenta de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] (por ejemplo, nombre de cuenta, estado y recuento de puestos disponibles). En esta área de trabajo puede administrar lo siguiente:<br /><br />-   **Actualizaciones.** Seleccione los productos para los que desea administrar las actualizaciones y determine los tipos de actualizaciones que desea administrar.<br />-   **Alertas y notificaciones.** Habilite los tipos de alertas que sean importantes, deshabilite los que no sean importantes, establezca umbrales de alerta para recibir una notificación en caso de que se alcance o supere un umbral, y recibir notificación de (y notificar a otros usuarios) las alertas por correo electrónico.<br />-   **Administración de administradores.** Designar **Administradores del servicio** que tengan permisos para ver o editar la configuración de la consola de administrador; y asignar también **Administradores de inquilinos** que tengan los mismos permisos que los administradores del servicio y que puedan administrar también cuentas de administrador mediante el portal de cuentas de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].<br />-   **Descarga de software cliente.** Implementar el software cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] de forma manual o automática.<br />-   **Uso del almacenamiento.** Administrar el uso del almacenamiento en nube de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], que se utiliza para distribuir el software a los equipos.<br />-   **Administración de dispositivos móviles.** Configurar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] para administrar directamente los dispositivos móviles de su organización<br />-   **Portal de empresa.** Configurar el portal de empresa de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] para mostrar información específica de su empresa, como el nombre de la empresa, la información de contacto para el soporte de TI y las direcciones URL de la declaración de privacidad de la empresa y el sitio web de soporte interno.|

## <a name="WIT_Fre"></a>Versión de evaluación gratuita y precios de Intune
Puede comenzar a usar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] con una versión de evaluación gratuita de 30 días que incluye 100 licencias de usuario. Con cada usuario puede usar hasta 5 dispositivos y puede hacerse una idea de lo que se puede hacer con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Para iniciar la versión de prueba gratuita, [visite la página de registro de Intune](http://aka.ms/TryMSIntune).

> [!NOTE]
> Si su organización tiene una cuenta profesional o educativa de Microsoft Online Services y es posible que continúe con esta suscripción de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en producción una vez finalizado el período de evaluación, haga clic en la opción **Iniciar sesión** de esa página y autentíquese con la cuenta de administrador global de la organización. Esta acción asegurará de que su versión de evaluación de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] se vincula con su cuenta de trabajo o académica existente. Si su organización tiene un contrato Enterprise o el contrato de licencias por volumen equivalente, póngase en contacto con su representante de Microsoft para configurar la versión de evaluación gratuita.

Para obtener información sobre los precios de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], vaya a la [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)][página de compra](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/buy.aspx) y, a continuación, haga clic en **Ver precios de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**.

Para obtener instrucciones detalladas sobre la suscripción a la versión de evaluación y tener acceso a un tutorial que puede usar para evaluar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] durante el periodo de evaluación de 30 días, consulte [Empezar a trabajar con una versión de prueba de 30 días de Microsoft Intune](../Topic/Get-started-with-a-30-day-trial-of-Microsoft-Intune.md). Para adquirir una suscripción de pago, consulte [Pasar de una versión de prueba gratuita de Microsoft Intune a una suscripción de pago](../Topic/Move-from-a-Microsoft-Intune-free-trial-to-a-paid-subscription.md).

