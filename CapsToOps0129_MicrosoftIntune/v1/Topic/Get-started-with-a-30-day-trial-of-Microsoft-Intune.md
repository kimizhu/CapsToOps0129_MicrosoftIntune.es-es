---
title: Empezar a trabajar con una versi&#243;n de prueba de 30 d&#237;as de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: 619a1d11-3d22-4635-8f70-770eba3e1712
---
# Empezar a trabajar con una versi&#243;n de prueba de 30 d&#237;as de Microsoft Intune
Configurar una versión de prueba gratuita de 30 días de Microsoft Intune para administrar los equipos y dispositivos móviles es rápido y sencillo. Con solo unos pocos pasos sencillos en la versión de prueba, puede agregar hasta 100 usuarios y dispositivos, configurar grupos y directivas de cumplimiento e inscribir y administrar equipos y dispositivos móviles. En este tema, aprenderá los conceptos básicos para poner la versión de prueba de Intune en funcionamiento y obtener una visión general del servicio para que pueda evaluar las características y capacidades de Intune.

Vea este vídeo de demostración de cinco minutos para aprender lo fácil que es empezar a trabajar con una prueba gratuita de Microsoft Intune y administrar los dispositivos:

![](../Image/EM_Intune_30_Day_Trial.PNG)

## Antes de comenzar
Antes de empezar a trabajar con Intune, necesitará lo siguiente:

-   Un dispositivo con un explorador web habilitado para Silverlight que pueda usar para tener acceso a los sitios web en los que creará cuentas de usuario de Intune (el **Portal de cuentas de Intune**) y en los que administrará dispositivos, grupos y directivas (la **consola de administración de Intune**).

-   Un segundo dispositivo con un explorador web que usará para probar cómo los usuarios de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] inscriben y administran sus dispositivos mediante el portal de empresa. También probará cómo los usuarios encuentran e instalan aplicaciones y piden ayuda a los administradores. Si no tiene un segundo dispositivo, puede usar la opción de "modo de privacidad" en el mismo explorador que usa para la administración de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] (por ejemplo: en Internet Explorer, puede hacer clic en **Herramientas** &gt; **Exploración de InPrivate**).

-   Si tiene una cuenta de Microsoft Online Services, necesitará las credenciales de administrador para esa cuenta. Si no tiene este tipo de cuenta, o si desea usar este inquilino de Intune solo con fines de evaluación, no necesita estas credenciales de administrador.

-   Si va a administrar dispositivos iOS o Windows Phone con la versión de prueba de Intune, necesitará certificados (o claves) y las cuentas para recuperar dichos certificados (consulte la tabla siguiente). Los dispositivos Android no necesitan certificados adicionales.

    |Plataforma|Requisitos de certificado|Más información|
    |--------------|-----------------------------|-------------------|
    |Windows Phone 8.1 y [!INCLUDE[winphone8_client_1](../Token/winphone8_client_1_md.md)]|No es necesario ningún certificado para los usuarios de Windows Phone 8.1 que instalen la aplicación de portal de empresa desde la Tienda. Se requiere un certificado Symantec en Windows Phone 8.0 o si usa Intune para implementar la aplicación de portal de empresa en dispositivos Windows Phone 8.1.|Esta guía presupone que los usuarios obtendrán la aplicación del portal de empresa de la Tienda desde un dispositivo Windows Phone 8.1 o posterior. Para obtener información sobre el soporte técnico de Windows Phone 8.0, vea [Configurar la administración de Windows Phone con Microsoft Intune](../Topic/Set-up-Windows-Phone-management-with-Microsoft-Intune.md).|
    |Dispositivos Windows 10, [!INCLUDE[winblue_winrt_2](../Token/winblue_winrt_2_md.md)], [!INCLUDE[win8RT_client_1](../Token/win8RT_client_1_md.md)], o [!INCLUDE[winblue_client_2](../Token/winblue_client_2_md.md)]|No hay requisitos de certificado para inscribir dispositivos Windows RT y Windows.|[Instalar al cliente de equipos Windows con Microsoft Intune](../Topic/Install-the-Windows-PC-client-with-Microsoft-Intune.md).|
    |iOS 7.1 o posterior|Obtenga un certificado del servicio de notificaciones push de Apple.|Solicite a Apple un certificado de servicio de notificaciones push de Apple, tal como se describe a continuación: [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).|

## <a name="Step1"></a>Paso 1: registrarse o iniciar sesión en Intune
Antes de registrarse o iniciar sesión en Intune, debe considerar lo siguiente:

-   Si la organización ya tiene una cuenta de trabajo o académica de Microsoft Online Services

-   Si tiene un contrato Enterprise o un contrato de licencias por volumen equivalente con Microsoft

-   Si tiene pensado usar el inquilino de Intune después de la versión de prueba de 30 días

|Registre una cuenta NUEVA, si cumple alguna de las siguientes opciones:|Inicie sesión con su cuenta de TRABAJO o ACADÉMICA si:|
|---------------------------------------------------------------------------|----------------------------------------------------------|
|-   **No tiene una cuenta de trabajo o académica.** Se suministra una cuenta de trabajo o académica al firmar un contrato de licencias por volumen con Microsoft o suscribirse a Office 365. Si su organización no ha firmado un Contrato Enterprise o un contrato de licencias por volumen equivalente con Microsoft (o tiene una cuenta de Office 365), no dispone de una cuenta de Microsoft Online Services que pueda usar para iniciar sesión en Microsoft Online Services.<br />-   **Descartará el inquilino de Intune tras completar la prueba de 30 días.** Si usa la suscripción de prueba gratuita de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] con fines de evaluación únicamente y tiene previsto rehacer la configuración del servicio [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] y el aprovisionamiento de dispositivos, deberá registrarse para obtener una cuenta nueva. Esta es la opción recomendada si tiene la intención de usar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] con System Center 2012 Configuration Manager. **Important:** Si se registra para una cuenta nueva, después no podrá utilizar una cuenta de trabajo o académica existente para administrar esa cuenta ni combinarla con contratos de licencias por volumen existentes.|**Tiene una cuenta de trabajo o académica suministrada con un contrato de licencias por volumen o una suscripción a Office 365 y usa esta versión de prueba para evaluar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].** **Important:** Si va a configurar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en una cuenta existente, le recomendamos que consulte [Introducción a Microsoft Intune](../Topic/Introduction-to-Microsoft-Intune.md) antes de continuar con los pasos siguientes.|

### <a name="BKMK_ToSignUpforSubscription"></a>Registro o inicio de sesión en Intune

1.  En primer lugar, [haga clic aquí para visitar la página de registro de Intune](https://portal.office.com/Signup/Signup.aspx?OfferId=40BE278A-DFD1-470a-9EF7-9F2596EA7FF9&dl=INTUNE_A&ali=1#0%20).

2.  En la página **Suscribirse** tiene dos opciones:

    -   **Suscribirse con una cuenta profesional o educativa de Microsoft Online Services**: haga clic en **Iniciar sesión** si ya tiene una cuenta profesional o educativa y desea usar la misma cuenta para suscribirse a ambos servicios. Cuando se utiliza la misma cuenta para varios servicios, dichos servicios utilizan la misma infraestructura de Azure AD y son inquilinos de Azure AD. Azure AD proporciona las principales capacidades de administración de identidades y directorios para servicios de nube de Microsoft.

    -   **Suscribirse solo a Intune**: si todavía no se suscribió a un servicio en la nube, rellene el formulario de la página de registro para suscribirse a [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

        > [!NOTE]
        > De forma predeterminada, el nombre de dominio está asociado con su suscripción y las cuentas de usuario que agrega a [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Después de suscribirse, puede agregar y usar un nombre de dominio personalizado que ya posea o seguir usando el dominio gratuito **onmicrosoft.com**.

Después de completar el formulario de registro y aceptar el Contrato Microsoft Online Subscription, se iniciará sesión automáticamente en [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)] con la cuenta de administrador de inquilinos. También se envía un mensaje de correo electrónico con los datos de su cuenta a la dirección de correo electrónico que especificó al realizar el registro. Este mensaje de correo electrónico confirma que la suscripción está activa.

## <a name="Step2"></a>Paso 2: agregar usuarios a Intune
Ahora que configuró su cuenta, podrá usar el asistente **Nuevos usuarios** para agregar cuentas de usuario individuales a [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], o bien el asistente **Agregar usuarios en masa** para agregar usuarios en masa (consulte las instrucciones en esta sección).  Antes de empezar, es importante que comprenda cómo Intune administra las cuentas de administrador.

Un administrador de inquilinos usa el portal de cuentas para agregar usuarios al **Grupo de usuarios** de Microsoft Intune. Agregar usuarios al **Grupo de usuarios** asigna licencias de suscripción de Intune a los usuarios y también es la forma de hacer que esos usuarios aparezcan en la consola de administración de Microsoft Intune.

Las cuentas de administrador de Intune no se crean en el portal de cuentas, como ocurre con las cuentas de usuario normales. En su lugar, puede asignar a los usuarios derechos administrativos, ya sea de acceso de solo lectura o bien de acceso completo, mediante la consola de administración del área de trabajo **Administración** en **Administración de la administración**. Los administradores de servicios a los que se les asigna el acceso de solo lectura no pueden cambiar la configuración de Intune, pero pueden ver los datos y ejecutar informes. Los administradores de servicios con acceso completo tienen todos los derechos administrativos disponibles.

Puede ver la información del Administrador de inquilinos mediante la consola de administración de Intune, pero no puede crear administradores de inquilinos con ella. De forma predeterminada, el propietario de la suscripción se convierte en Administrador de inquilinos del servicio de Microsoft Intune y tiene acceso completo tanto al portal de cuentas de Intune como a la consola de administración de Intune. Le recomendamos que cree como mínimo una cuenta de Administrador de inquilinos adicional mediante el portal de cuentas para poder delegar fácilmente tareas y asegurarse de no quedar bloqueado fuera de la cuenta de administrador del servicio de Intune si olvida la contraseña.

### Agregar cuentas de usuario individuales
Use los pasos siguientes para crear cuentas de usuario adicionales en el inquilino de prueba. Recuerde que cada cuenta de usuario que agregue se contabiliza como una más de las 100 licencias en total que obtiene como parte de la versión de prueba gratuita de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

1.  En el [portal de cuentas de Intune](https://account.manage.microsoft.com), haga clic en **Agregar usuarios** &gt; **Nuevo** &gt; **Usuario** para iniciar el asistente **Nuevos usuarios**.

2.  En la página **Detalles**, rellene los campos obligatorios.

3.  En la página **Configuración**, establezca la **ubicación** del usuario.

4.  En la página **Grupo**, haga clic en **Siguiente** para aceptar los valores predeterminados y asignar una licencia para [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a la cuenta de usuario.

5.  En la página **Correo electrónico**, puede especificar hasta cinco direcciones de correo electrónico que recibirán notificación del nombre de usuario y la contraseña temporal de la cuenta. Use signos de punto y coma (;) para separar varias direcciones de correo electrónico. Cuando haya terminado, haga clic en **Crear** para agregar el usuario a su suscripción.

6.  En la página **Resultados**, puede ver el nuevo nombre de cuenta y su contraseña temporal.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] crea automáticamente la contraseña temporal.

7.  Cuando el nuevo usuario aparezca en el nodo **Usuarios** del portal de cuentas, compruebe que este se creó correctamente:

    1.  En la [consola de administración de Intune](https://manage.microsoft.com/), haga clic en **Administración** &gt; **Portal de empresa** y vaya al final de la pantalla. Copie la dirección URL que se muestra en **Portal de empresa de Intune**.

    2.  Abra una nueva ventana del explorador en "modo de privacidad" (en Internet Explorer, haga clic en **Herramientas** &gt; **Exploración de InPrivate**) o abra una nueva ventana del explorador en un dispositivo diferente y, a continuación, navegue a la dirección URL que copió en el paso anterior. Cuando los usuarios inicien sesión por primera vez, deberán proporcionar una nueva contraseña para la cuenta.

### Agregar usuarios en masa
Para agregar usuarios en masa a Intune, use el asistente **Agregar usuarios en masa** para cargar un archivo de valores separados por comas (CSV) que contenga los datos de usuario. En el asistente encontrará los vínculos que le permitirán descargar una plantilla en blanco y el archivo CSV de ejemplo. La primera fila del archivo CSV debe contener, en el orden correcto, cada una de las etiquetas de columna de datos de usuario. En el archivo CSV debe incluir el **nombre de usuario** (p. ej., **bob@contoso.com**) y un **nombre para mostrar** (p. ej., **Bob Kelly**) para cada usuario.

1.  En el [portal de cuentas de Microsoft Intune](https://account.manage.microsoft.com), haga clic en **Usuarios** &gt; **Nuevo**.

2.  Haga clic en **Agregar en masa** para iniciar el asistente para Agregar usuarios en masa.

3.  En la página **Seleccionar archivo**, haga clic en **Examinar** para especificar y cargar un archivo CSV existente desde su equipo. También puede descargar un archivo CSV de ejemplo o el archivo de plantilla en blanco mediante los vínculos del asistente.

4.  En la página **Comprobación**, revise los resultados y haga clic en **Ver** para obtener más detalles.

5.  En la página **Configuración**, compruebe que el estado de inicio de sesión es **Permitido** y establezca la **ubicación**. Esta configuración se aplica a todas las cuentas de usuarios agregadas mediante el archivo CSV.

6.  En la página **Grupo**, haga clic en **Siguiente** para aceptar los valores predeterminados y asignar una licencia para [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a todas las cuentas de usuarios agregadas mediante el archivo CSV. De manera predeterminada, la casilla está seleccionada, lo que asigna una licencia para [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a cada cuenta.

7.  En la página **Correo electrónico**, puede especificar hasta cinco direcciones de correo electrónico para que reciban notificación de los nombres de usuario y las contraseñas temporales que [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] crea para cada cuenta. Separe varias direcciones de correo electrónico con punto y coma (;). Cuando esté listo, haga clic en **Crear** para agregar los usuarios a la suscripción.

8.  En la página **Resultados** puede ver los nombres de cuenta y las contraseñas temporales para cada cuenta de usuario.

Cada cuenta de usuario agregada mediante importación, aparece ahora en el nodo **Usuarios** del portal de cuentas. Cuando los nuevos usuarios inicien sesión por primera vez, deberán especificar una nueva contraseña para su cuenta de usuario.

## <a name="Step3"></a>Paso 3: crear grupos para organizar usuarios y dispositivos
Los grupos de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ofrecen una gran flexibilidad para administrar los dispositivos y usuarios. Puede configurar los grupos para que se adapten a las necesidades de su organización (por ejemplo, por ubicación geográfica, departamento o características de hardware) y usarlos para realizar diversas tareas administrativas a escala, desde la configuración de directivas para un conjunto de usuarios hasta la implementación de aplicaciones en un conjunto de dispositivos.

### Creación de un grupo de dispositivos
Use los grupos de dispositivos para implementar software y actualizaciones y para establecer las directivas de configuración del Agente de Microsoft Intune y del Firewall de Windows. Por ejemplo, configure un grupo de "Mis dispositivos de prueba" siguiendo estos pasos:

1.  En la [consola de administración de Intune](https://manage.microsoft.com/), haga clic en **Grupos** &gt; **Información general** &gt; **Crear grupo**.

2.  En el **Nombre de grupo**, escriba "Mis dispositivos de prueba" y, en la lista de grupos principales, seleccione **Todos los dispositivos**, y, a continuación, haga clic en **Siguiente**.

3.  En la página **Definir criterios de pertenencia**, seleccione **Todos los dispositivos** para indicar que el grupo incluye tanto dispositivos móviles como equipos.

4.  En la página **Definir pertenencia directa**, haga clic en **Siguiente**. Si previamente creó un grupo que no incluye todos los dispositivos y desea agregar determinados dispositivos al nuevo grupo, puede hacerlo aquí.

5.  En la página **Resumen**, revise las acciones que se van a realizar y, a continuación, haga clic en **Finalizar**.

Puede encontrar el grupo recién creado en la lista **Grupos**, del área de trabajo **Grupos** en **Todos los dispositivos**. Aquí también puede editar o eliminar el grupo.

### Creación de un grupo de usuarios
Use grupos de usuarios para implementar las directivas de software y dispositivos. Por ejemplo, configure un grupo de "Mis usuarios de prueba" siguiendo estos pasos:

1.  En la [consola de administración de Intune](https://manage.microsoft.com/), haga clic en **Grupos** &gt; **Información general** &gt; **Crear grupo**.

2.  En el **Nombre de grupo**, escriba "Mis usuarios de prueba" y, en la lista de grupos principales, seleccione **Todos los usuarios**, y, a continuación, haga clic en **Siguiente**.

3.  En la página **Definir criterios de pertenencia**, establezca **Iniciar pertenencia a grupos con** en **Todos los usuarios del grupo primario**.

4.  Al lado de **Excluir los miembros de estos grupos de seguridad**, haga clic en **Examinar** y, después, seleccione **Administrador de la compañía**. Esta exclusión le permite administrar el grupo Mis usuarios de prueba sin que afecte a la cuenta del Administrador de la compañía (también conocido como Administrador de inquilinos).

5.  En la página **Definir pertenencia directa**, haga clic en **Siguiente**. Aquí no tiene que hacer nada, ya que desea que el grupo Mi usuarios de prueba incluya a todos los usuarios, salvo el Administrador de empresa.

6.  En la página **Resumen**, revise las acciones que se van a realizar y, a continuación, haga clic en **Finalizar**.

Puede encontrar el grupo recién creado en la lista **Grupos** del área de trabajo **Grupos** en **Todos los usuarios**. Aquí también puede editar o eliminar el grupo.

Para obtener más información sobre el uso de grupos, consulte [Utilizar grupos para administrar usuarios y dispositivos en Microsoft Intune](../Topic/Use-groups-to-manage-users-and-devices-with-Microsoft-Intune.md).

## <a name="Step4"></a>Paso 4: crear directivas y publicar una aplicación
Las directivas de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] le proporcionan una configuración que le ayuda a controlar la configuración de seguridad en dispositivos móviles, a mantener la configuración de Firewall de Windows y Endpoint Protection de los equipos, y a implementar aplicaciones. Si planea usar Intune para configurar dispositivos que van a usarse en producción después de la versión de prueba, es de gran importancia que siga las instrucciones de [Administrar la configuración y las características de los dispositivos con directivas de Microsoft Intune](../Topic/Manage-settings-and-features-on-your-devices-with-Microsoft-Intune-policies.md) y [Ayudar a proteger los equipos de Windows con Endpoint Protection para Microsoft Intune](../Topic/Help-secure-Windows-PCs-with-Endpoint-Protection-for-Microsoft-Intune.md).

Puede realizar dos tipos de instalaciones de aplicación mediante Intune. El primer tipo es una **instalación requerida**, que implementa automáticamente la aplicación en los equipos administrados. El segundo es una **instalación disponible**, que implementa la aplicación o un vínculo a la aplicación de portal de empresa de Intune, de forma que los usuarios pueden elegir si quieren instalarlo en sus equipos o en sus dispositivos móviles.

Antes de usar Intune para implementar aplicaciones, asegúrese de que tiene las licencias apropiadas para publicar, distribuir y usar la aplicación. El área de trabajo **Licencias** le permite agregar y administrar la información de contratos de licencias de aplicaciones o software adquiridos a través de contratos de Licencias por volumen de Microsoft, así como de aplicaciones o software de Microsoft o de otros fabricantes adquiridos por otros medios. A continuación, puede crear informes de licencias, que muestran la información de uso de las licencias administradas en toda la empresa, para mantenerse informado de la actividad de uso de las licencias.

Por medio de estos pasos, se establece una directiva de configuración de dispositivos móviles y una directiva de firewall para equipos Windows, y se configurar Skype como instalación disponible para dispositivos móviles después de haberse inscrito. Después de agregar e implementar una nueva directiva, todos los usuarios o dispositivos del grupo en el que se ha implementado la directiva heredan la configuración como directiva de línea de base. Siempre puede revisar y editar los detalles de estas directivas más adelante en el área de trabajo **Directiva** en la consola de administración.

#### Creación e implementación de una directiva de configuración de dispositivo móvil

1.  Abra la [consola de administración de Intune](https://manage.microsoft.com/).

2.  En el panel de la izquierda, haga clic en el icono **Directiva**.

3.  En la lista **Tareas** de la página **Información general de directivas**, haga clic en **Agregar directiva**.

4.  En la lista de directivas, expanda la plataforma para la que desea crear una directiva, seleccione **Configuración general**, elija **Crear e implementar una directiva con la configuración recomendada**, y, a continuación, haga clic en **Crear directiva**.

5.  Cuando se le pida **Seleccionar los grupos en los que quiere implementar esta directiva**, seleccione **Mis usuarios de prueba** de la lista y haga clic en **Agregar** &gt; **Aceptar**.

La directiva aparecerá en la lista de directivas de configuración y se implementará al grupo **Mis usuarios de pruebas**. Haga doble clic en la directiva para ver su configuración.

#### Publicación de la aplicación de Skype para dispositivos móviles

1.  En la [consola de administración de Intune](https://manage.microsoft.com/), haga clic en el icono **Aplicaciones** y, luego, en **Aplicaciones** &gt; **Agregar aplicación**. Si se le solicitan sus credenciales de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], especifíquelas.

    > [!NOTE]
    > Al iniciar el **editor de software de Intune** por primera vez, se producirá una breve demora mientras se instala la aplicación.

2.  Revise la advertencia de seguridad y haga clic en **Ejecutar**.

3.  En la página **Antes de comenzar**, haga clic en **Siguiente**.

4.  En la página **Instalación de software**, en **Seleccionar cómo el software debe ponerse a disposición de los dispositivos**, seleccione **Vínculo externo**.

5.  Especifique el vínculo externo del software en **Especificar la dirección URL** y, a continuación, haga clic en **Siguiente**. Asegúrese de preceder la dirección URL con **http://**. Para la aplicación de Skype, use el vínculo siguiente que coincida con la plataforma de dispositivo móvil que emplea:

    -   **iOS:** [https://itunes.apple.com/es/app/skype-for-iphone/id304878510?mt%3D8](https://itunes.apple.com/us/app/skype-for-iphone/id304878510?mt%3D8)

    -   **Android:** [https://play.google.com/store/apps/details?id=com.skype.raider](https://play.google.com/store/apps/details?id=com.skype.raider)

    -   **Windows Phone 8 o Windows Phone 8.1:** [http://www.windowsphone.com/es-es/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51](http://www.windowsphone.com/en-us/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51)

6.  En la página **Descripción del software**, proporcione la información que desea que los usuarios vean en el portal de empresa para el software y, a continuación, haga clic en **Siguiente**. Están disponibles los siguientes valores de configuración (este ejemplo hace referencia a Skype):

    -   **Publicador:** escriba el nombre del publicador, "Microsoft".

    -   **Nombre:** escriba **Skype**.

    -   **Descripción:** escriba una descripción para el software, como **aplicación de comunicación de Skype**.

    -   **Categoría:** Seleccione la categoría más adecuada para el software, como **Colaboración**.

    -   **Mostrar esta aplicación como destacada y resaltarla en el portal de empresa:** seleccione esta opción para que la aplicación se muestre de forma destacada en el portal de empresa en los dispositivos móviles.

    -   **Icono:** (Opcional) elija si desea asociar un icono con el software. El tamaño de icono máximo es 250 x 250 píxeles, pero el tamaño de icono recomendado es 32 x 32 píxeles.

7.  En la página **Resumen**, compruebe la información del software y, a continuación, haga clic en **Cargar**. Haga clic en **Cerrar** para salir del asistente.

8.  En la [consola de administración de Intune](https://manage.microsoft.com/), haga clic en **Aplicaciones** &gt; **Aplicaciones** &gt; **Skype** &gt; **Administrar la implementación**.

9. En la página **Seleccionar grupos**, seleccione **Mis usuarios de prueba** para implementar el software en ese grupo de usuarios y, a continuación, haga clic en **Agregar** &gt; **Siguiente**.

10. En la página **Acción de implementación**, seleccione **Instalación disponible** en la columna **Aprobación** para su grupo.

11. Haga clic en **Finalizar**.

La aplicación Skype ahora se puede instalar en dispositivos móviles desde el portal de empresa, pero primero debe instalar el software de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en equipos y dispositivos móviles.

## <a name="Step5"></a>Paso 5: inscribir equipos en Intune
Puede instalar el software cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en los equipos de alguna de las maneras siguientes:

-   Los usuarios pueden usar un instalador proporcionado por el administrador para inscribirse manualmente

-   El software de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] puede incluirse en una imagen de sistema operativo o implementarse por medio de una Directiva de grupo

-   Los usuarios finales pueden inscribir automáticamente sus dispositivos a través del portal de empresa de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]

Cada equipo inscrito está vinculado a la cuenta de usuario que se utilizó para instalar el software cliente. Microsoft Intune Endpoint Protection también se instala de forma predeterminada durante la instalación de cliente de Intune en los equipos. Endpoint Protection ayuda a proteger los equipos de su organización al proporcionar protección en tiempo real contra amenazas potenciales, mantener actualizadas las definiciones de software malintencionado y ejecutar automáticamente exámenes programados. Para mayor seguridad, también puede usar las directivas de Intune para administrar la configuración de Firewall de Windows en los equipos administrados.

Lo que debe saber antes de empezar:

-   Para poder instalar el software cliente, el usuario debe ser administrador del equipo.

-   La inscripción automática requiere que esté instalado Internet Explorer en el equipo cliente.

-   Cada vez que un usuario inscribe automáticamente un equipo, se usa una licencia de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]

-   Debe utilizar una cuenta de trabajo o académica de Microsoft Online Services para inscribir automáticamente un equipo. Se trata de la cuenta que utilizó para iniciar sesión o la cuenta de administrador que se creó cuando se registró para la prueba gratuita.

Para esta versión de prueba, siga estos pasos, que usan el método de inscripción automática:

1.  En la [consola de administración de Intune](https://manage.microsoft.com/), haga clic en **Administración** &gt; **Portal de empresa** y vaya al final de la pantalla. Copie la dirección URL que se muestra en **Portal de empresa de Intune**.

2.  Utilice Internet Explorer para visitar la dirección URL del portal de empresa que adquirió en el paso anterior e inicie sesión con sus credenciales de administrador.

3.  Haga clic en **Agregar dispositivo**.

4.  Haga clic en **Descargar software** y, a continuación, en **Ejecutar**.

5.  Haga clic en **Siguiente** para iniciar el Asistente para la instalación de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

6.  Cuando haya finalizado el Asistente para la instalación, haga clic en **Finalizar**.

Para obtener más información acerca de la administración de equipos mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Instalar al cliente de equipos Windows con Microsoft Intune](../Topic/Install-the-Windows-PC-client-with-Microsoft-Intune.md).

Para obtener más información acerca de la administración de software mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Implementar y configurar aplicaciones con Microsoft Intune](../Topic/Deploy-and-configure-apps-with-Microsoft-Intune.md).

## <a name="Step6"></a>Paso 6: inscribir dispositivos móviles e instalar una aplicación
Para configurar la administración de dispositivos móviles con Intune, primero debe establecer la entidad de administración de dispositivos móviles, habilitar la administración de plataformas de dispositivos e inscribir sus dispositivos con la aplicación del portal de empresa. Posteriormente, puede implementar la aplicación Microsoft Skype que publicó.

1.  **Convertir Intune en su entidad de administración de dispositivos móviles**
    En la [consola de administración de Intune](https://manage.microsoft.com/), haga clic en **Administración** &gt; **Administración de dispositivos móviles** y, luego, en **Configurar entidad de MDM** en **Tareas**.  Haga clic en **Sí** en el cuadro de diálogo **Entidad de MDM**.

2.  **Habilitación de MDM para su plataforma de dispositivo**
    Habilitación de la administración de dispositivos móviles para la plataforma de dispositivo que desea administrar. Los requisitos necesarios varían según la plataforma:

    -   **iOS**: consulte [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).

    -   **Windows Phone**: consulte [Configurar la administración de Windows Phone con Microsoft Intune](../Topic/Set-up-Windows-Phone-management-with-Microsoft-Intune.md).

    -   **Android**: los dispositivos Android permiten a los usuarios inscribirse mediante la aplicación de portal de empresa disponible en Google Play. No se requiere ninguna configuración adicional en Intune.

3.  **Inscripción de dispositivos:**

    -   **Android**: instale la aplicación **Portal de empresa de Intune** de Microsoft Corporation, disponible en [Google Play](http://go.microsoft.com/fwlink/p/?LinkId=386612), e inicie sesión con las credenciales de usuario de Intune agregadas anteriormente.

    -   **iOS**: instale la aplicación **Portal de empresa de Microsoft Intune** de Microsoft Corporation disponible en App Store e inicie sesión con las credenciales de usuario de Intune agregadas anteriormente. Consulte **Dispositivos inscritos** para agregar el dispositivo.

    -   **Windows Phone 8.1**: los usuarios deberán instalar la aplicación **Portal de empresa** de Microsoft Corporation, disponible en la Tienda de Windows Phone, e iniciar sesión con las credenciales de usuario de Intune agregadas anteriormente.  Consulte **Dispositivos inscritos**  para agregar el dispositivo.

    -   **Windows Phone 8.0** : los usuarios deben hacer clic en **configuración del sistema** &gt; **aplicaciones de la compañía** e iniciar sesión usando las credenciales de usuario de Intune agregadas anteriormente. La aplicación de portal de empresa se implementa en el teléfono.

    Si se le pide una **dirección de servidor**, escriba “manage.microsoft.com”.

4.  Abra el portal de empresa en el dispositivo móvil, seleccione **Aplicaciones** e instale **Microsoft Skype**.

Para obtener más información acerca de la administración de dispositivos móviles mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Preparar la inscripción de dispositivos en Microsoft Intune](../Topic/Get-ready-to-enroll-devices-in-Microsoft-Intune.md).

## Opciones y extras de Intune

### Alertas, notificaciones e informes
En la [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], las **alertas** se utilizan para evaluar rápidamente el estado general de los dispositivos administrados de la organización. Puede configurar y personalizar las alertas para que puedan notificar y mostrar solo la información que necesita para su organización. Puede habilitar o deshabilitar una alerta, configurar la gravedad, utilizar el umbral para mostrar a fin de determinar la frecuencia con la que se debe desencadenar un evento de alerta para que se muestre una alerta y también puede configurar opciones específicas para determinados tipos de alertas.

Las **notificaciones** son correos electrónicos que se usan para informar a los administradores (y a otros usuarios) cuando se desencadenan determinados tipos de alertas.

Los **informes** se usan para contestar diversos tipos de preguntas, como el número de equipos que tienen instalada una aplicación o actualización concreta, qué malware se ha bloqueado o qué usuarios han necesitado asistencia remota en el último mes.

Para obtener más información acerca de las alertas, notificaciones e informes, consulte [Supervisión e informes](../Topic/Monitoring-and-reports-with-Microsoft-Intune.md).

### Capacidades de Intune
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] tiene una amplia variedad de capacidades que abarcan mucho más de lo expuesto en estos breves pasos de configuración. Estos son algunos ejemplos de estas capacidades:

-   **Control del acceso a Exchange y Office 365** Para obtener más información, consulte [Administrar el acceso al correo electrónico y SharePoint con Microsoft Intune](../Topic/Manage-access-to-email-and-SharePoint-with-Microsoft-Intune.md).

-   **Administración de dispositivos iOS propiedad de la empresa.** Para obtener más información, consulte [Inscribir dispositivos iOS de empresa en Microsoft Intune](../Topic/Enroll-corporate-owned-iOS-devices-in-Microsoft-Intune.md).

-   **Administración de aplicaciones móviles.** Las aplicaciones móviles administradas funcionan con directivas de administración de aplicaciones móviles que restringen ciertas operaciones de las aplicaciones, como las funciones de copiar y pegar y la creación de capturas de pantalla. Par obtener más información, consulte [Proteger datos mediante las directivas de administración de aplicaciones móviles con Microsoft Intune](../Topic/Configure-and-deploy-mobile-application-management-policies-in-the-Microsoft-Intune-console.md) y [Administrar el acceso a Internet mediante directivas de explorador administrado con Microsoft Intune](../Topic/Manage-Internet-access-using-managed-browser-policies-with-Microsoft-Intune.md).

-   **Controle el acceso a los recursos de la empresa.** Puede implementar certificados, perfiles de correo electrónico, perfiles de VPN y perfiles de Wi-Fi en dispositivos móviles, lo que permite configurarlos más rápidamente. Para obtener más información, consulte [Habilitar el acceso a los recursos de empresa con Microsoft Intune](../Topic/Enable-access-to-company-resources-with-Microsoft-Intune---deleted.md).

Para obtener información acerca de todas las capacidades de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Capacidades de administración de dispositivos móviles en Microsoft Intune](../Topic/Mobile-device-management-capabilities-in-Microsoft-Intune.md), [Funciones de administración de equipos Windows en Microsoft Intune](../Topic/Windows-PC-management-capabilities-in-Microsoft-Intune.md) y [Descripción del servicio Microsoft Intune](../Topic/Microsoft-Intune-Service-Description.md).

Para obtener más información acerca de las capacidades incorporadas recientemente en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Novedades de Microsoft Intune](../Topic/What-s-new-in-Microsoft-Intune.md).

Las opciones de soporte técnico se describen en [Cómo obtener asistencia para Microsoft Intune](../Topic/How-to-get-support-for-Microsoft-Intune.md), y puede unirse a las discusiones sobre [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en los [foros de Microsoft Intune](https://social.technet.microsoft.com/Forums/en-US/home?forum=microsoftintuneprod).

## <a name="BKMK_BuyIntune"></a>¿Listo para pasarse a una suscripción de pago de Intune?
Si adquiere al menos 150 licencias de Microsoft Intune en un plan elegible, puede usar el "beneficio del Centro FastTrack", un servicio donde los especialistas en Microsoft trabajan con usted para preparar su entorno para Intune. Consulte [Descripción del beneficio de servicio de Microsoft Intune](https://technet.microsoft.com/library/mt228265.aspx).

Puede convertir la versión de prueba gratuita de Intune en una suscripción de pago de las maneras siguientes:

-   **Suscripción a Intune**: se ofrece mediante una licencia por cada usuario. Para obtener más información, vea [Cómo comprar Microsoft Intune](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/Purchasing.aspx). Después de realizar la compra, siga los pasos de [Introducción a una suscripción de pago de Microsoft Intune](../Topic/Get-started-with-a-paid-subscription-to-Microsoft-Intune.md) y revise los pasos de configuración adicionales si parte de cero con Intune.

-   **Enterprise Mobility Suite**: proporciona [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], Azure Active Directory Premium, servicios de Azure RMS. Póngase en contacto con el administrador de cuentas de Microsoft o distribuidor local para obtener más detalles, o vea la [información sobre Enterprise Mobility Suite](https://www.microsoft.com/en-us/server-cloud/enterprise-mobility/overview.aspx) o los [precios de Enterprise Mobility Suite](http://www.microsoft.com/en-us/server-cloud/products/enterprise-mobility-suite/Purchasing.aspx).

-   **Contrato Enterprise** (más de 250 usuarios): el mejor programa de licencias para organizaciones con más de 250 usuarios. Este contrato le ofrece la flexibilidad de elegir entre software local y servicios en línea para adaptarse mejor a las necesidades de sus usuarios y optimizar su gasto en tecnología. Póngase en contacto con el administrador de cuentas de Microsoft o con su distribuidor local para obtener más información, o consulte el [sitio de licencias por volumen para empresa](http://www.microsoft.com/licensing/licensing-options/enterprise.aspx).

-   **Programa de suscripción en línea** (menos de 250 usuarios): el programa de [licencias por volumen de Online Services](http://www.microsoft.com/licensing/online-services/default.aspx) está diseñado específicamente para organizaciones con menos de 250 usuarios. Utilice este programa para suscribirse, administrar e implementar sus servicios de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## Vea también
[Introducción a una suscripción de pago de Microsoft Intune](../Topic/Get-started-with-a-paid-subscription-to-Microsoft-Intune.md)

