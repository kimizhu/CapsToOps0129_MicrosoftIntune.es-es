---
title: Crear e implementar directivas de administraci&#243;n de aplicaciones m&#243;viles con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c1b9a343-1737-4a65-a9c6-aca48acad11c
---
# Crear e implementar directivas de administraci&#243;n de aplicaciones m&#243;viles con Microsoft Intune
Puede crear directivas de administración de aplicaciones móviles (MAM) e implementarlas para los usuarios en el portal de vista previa de Azure.  Las directivas MAM que se crean aquí son independientes de la inscripción de los dispositivos, lo que significa que pueden usarse en dispositivos no administrados en absoluto, o que están administrados por [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] u otra solución de terceros.

**En este tema**

[Crear e implementar una directiva MAM](#bkmk_createanddeploy)

[Cambiar las directivas existentes](#bkmk_changepolicy)

[Configuración de directiva](#bkmk_policysettings)

[Pasos siguientes](#bkmk_nextsteps)

### <a name="bkmk_createanddeploy"></a>Crear e implementar una directiva MAM

##### Crear una directiva MAM

1.  Haga clic en **Administración de aplicaciones móviles de Intune &gt; Configuración** para abrir la **Configuración**.

    ![](../Image/AppManagement/AzurePortal_MAM_Mainblade.png)

    > [!TIP]
    > Si esta es la primera vez que usa el portal de Azure, lea [Introducción a las directivas de administración de aplicaciones móviles en el portal de Azure](../Topic/Get-started-with-mobile-app-management-policies-in-the-Azure-portal.md) en primer lugar para familiarizarse con el portal.

2.  En la hoja **Configuración**, haga clic en **Directiva de aplicación**.  De este modo se abrirá la hoja **Directiva de aplicación**, en la que podrá crear nuevas directivas y editar las directivas existentes.

    ![](../Image/AppManagement/AzurePortal_MAM_AppPolicy.png)

3.  Haga clic en **Agregar una directiva**.

    ![](../Image/AppManagement/AzurePortal_MAM_AddPolicy.png)

4.  Escriba un nombre para la directiva, agregue una descripción breve y seleccione el tipo de plataforma para crear una directiva para iOS o Android.  Puede crear más de una directiva para cada plataforma.

    ![](../Image/AppManagement/AzurePortal_MAM_AddPolicy_only.png)

5.  Haga clic en **Aplicaciones** para abrir la **hoja aplicaciones** donde se muestra una lista de aplicaciones disponibles. Puede seleccionar una o más aplicaciones de la lista que desea asociar a la directiva que está creando. Una vez seleccionadas las aplicaciones, haga clic en el botón **Seleccionar** situado en la parte inferior de la hoja **Aplicaciones** para guardar la selección.

    > [!IMPORTANT]
    > Debe seleccionar al menos una aplicación para crear una directiva.

6.  En la **hoja Agregar una directiva**, haga clic en **Configurar la configuración necesaria** para abrir la hoja de configuración de directivas.

    Existen dos categorías de configuración de directivas: **Reubicación de datos** y **Acceso**.  Las directivas de reubicación de datos son aplicables al movimiento de datos a dentro y fuera de las aplicaciones, mientras que las directivas de acceso determinan el modo en el que el usuario final tiene acceso a las aplicaciones en un contexto de trabajo. Para comenzar, la configuración de directiva tiene valores predeterminados.  No es necesario realizar ningún cambio si los valores predeterminados satisfacen sus necesidades.

    > [!TIP]
    > Esta configuración de directiva se aplica solo al usar aplicaciones en el contexto de trabajo.  Cuando el usuario final usa la aplicación para realizar una tarea personal, no se verá afectada por estas directivas.

    ![](../Image/AppManagement/AzurePortal_MAM_PolicySettings.png)

    Consulte la sección [Configuración de directiva](#bkmk_policysettings) de este tema para obtener una lista completa de la configuración de directivas y los valores predeterminados.

7.  Haga clic en **Aceptar** para guardar esta configuración.  Ahora habrá regresado a la hoja **Agregar una directiva**. Haga clic en **Crear** para crear la directiva y guardar la configuración.

    ![](../Image/AppManagement/AzurePortal_MAM_CreatePolicy.png)

    ![](../Image/AppManagement/AzurePortal_MAM_AddingPolicyNotification.png)

Cuando termine de crear una directiva como se describe en el procedimiento anterior, no se implementará en ningún usuario.  Siga los pasos descritos a continuación para implementar la directiva.

> [!NOTE]
> Si ha creado directivas de administración de aplicaciones móviles desde las consolas de Intune o de Administrador de configuración y también ha creado una directiva de administración de aplicaciones desde la consola de Azure y, a continuación, ha asociado las dos directivas a la misma aplicación, la directiva creada desde el portal de vista previa de Azure tendrá prioridad. Sin embargo, los informes de la consola de Intune o del Administrador de configuración informará de la configuración de directiva creada en el portal de vista previa de Azure. Por ejemplo:
> 
> -   Ha creado una directiva de administración de aplicaciones móviles en la consola de administración de Intune que bloquea la copia desde una aplicación.
> -   Ha creado una directiva de administración de aplicaciones móviles en la consola de Azure que permite la copia desde una aplicación
> -   Asocie ambas directivas a la misma aplicación.
> -   El resultado es que la directiva creada desde la consola de Azure tiene prioridad y se permite la copia.
> -   Sin embargo, el estado y los informes de la consola de Intune indicarán incorrectamente que la copia está bloqueada.

##### Implementar una directiva para los usuarios

1.  En la hoja **Directiva**, haga clic en **Grupos de usuarios**, que abre la hoja **Grupos de usuarios**. Haga clic en **Agregar grupo de usuarios** en la hoja **Grupos de usuarios** para abrir la hoja **Agregar grupo de usuarios**.

    ![](../Image/AppManagement/AzurePortal_MAM_AddUserstoPolicy.png)

2.  Se mostrará una lista de grupos de usuarios en la hoja **Agregar grupo de usuarios**. Esta es una lista de todos los grupos de seguridad de su **Azure Active Directory**.  Puede seleccionar los grupos de usuarios a los que desee que se aplique esta directiva y hacer clic en **Seleccionar**.**Al hacer clic en Seleccionar se implementa la directiva a los usuarios**.

    ![](../Image/AppManagement/AzurePortal_MAM_SelectUserstoDeploy.png)

    > [!NOTE]
    > Solo se verán afectados por la directiva los usuarios con licencias [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] asignadas.  Los usuarios que estén en el grupo de seguridad que haya seleccionado que no tengan una licencia [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] asignada no se verán afectados.

    > [!NOTE]
    > Si usa Intune con Administrador de configuración para administrar los dispositivos iOS y Android, la directiva solo se aplica a los usuarios directamente en el grupo seleccionado.  No se verán afectados los miembros de los grupos secundarios anidados en el grupo seleccionado.

Ahora ha creado una directiva y la ha implementado en los usuarios.

### <a name="bkmk_changepolicy"></a>Cambiar las directivas existentes
Al cambiar las directivas existentes, los usuarios que ya han iniciado sesión en las aplicaciones no verán los cambios durante un período de 8 horas.

Si está realizando pruebas y le gustaría ver la directiva modificada inmediatamente, cierre la sesión de la aplicación y vuelva a iniciarla ver la nueva configuración.

##### Cambiar la lista de aplicaciones asociadas con la directiva

1.  En la hoja **Directiva de aplicación**, haga clic en la directiva que desee cambiar. De este modo se abrirá una hoja específica de la directiva que acaba de seleccionar.

    ![](../Image/AppManagement/AzurePortal_MAM_OpenPolicy.png)

2.  En la hoja de la directiva, haga clic en **Aplicaciones de destino** para abrir la lista de aplicaciones.

3.  Quite o agregue aplicaciones de la lista y haga clic en el **icono Guardar** para guardar los cambios.

##### Cambiar la lista de grupos de usuarios

1.  En la hoja **Directiva de aplicación**, haga clic en la directiva que desee cambiar. De este modo se abrirá la hoja específica de la directiva que ha seleccionado.

2.  En la hoja de la directiva, haga clic en **Grupos de usuarios** para abrir la hoja **Grupo de usuarios** en la que se muestra la lista de grupos de usuarios actuales con esta directiva.

3.  Para **agregar un nuevo grupo de usuarios** a la directiva, haga clic en **Agregar grupo de usuarios** y seleccione el grupo de usuarios. Haga clic en **Seleccionar** para implementar la directiva en el grupo seleccionado.

    ![](../Image/AppManagement/AzurePortal_MAM_ChangePolicy_SelectUser.png)

4.  Para **eliminar un grupo de usuarios**, resalte el grupo de usuarios que desee quitar, haga clic en el botón de puntos suspensivos (...) y, a continuación, haga clic en **Eliminar** para eliminar el grupo de usuarios.

    ![](../Image/AppManagement/AzurePortal_MAM_ChangePolicy_DeleteUser.png)

##### Cambiar la configuración de directiva

1.  En la hoja **Directiva de aplicación**, haga clic en la directiva que desee cambiar. De este modo se abrirá una hoja específica de la directiva que acaba de seleccionar.

    ![](../Image/AppManagement/AzurePortal_MAM_OpenPolicy.png)

2.  Haga clic en **Configuración de directiva** para abrir la hoja **Configuración de directiva**.

3.  Cambie la configuración y haga clic en el **icono Guardar** para guardar los cambios.

    ![](../Image/AppManagement/AzurePortal_MAM_ChangePolicy_ChangeSettings.png)

### <a name="bkmk_policysettings"></a>Configuración de directiva
**Directivas de reubicación de datos IOS**

||||
|-|-|-|
|**Configuración de directiva**|**Descripción**|**Valor predeterminado**|
|**Impedir copias de seguridad de iTunes e iCloud**|Seleccione **Sí** para deshabilitar, o **No** para permitir la copia de seguridad de cualquier información de las aplicaciones administradas por directivas.|**Sí**|
|**Permitir que la aplicación transfiera datos a otras aplicaciones**|Seleccione una de las opciones para especificar las aplicaciones a las que las aplicaciones administradas por la directiva pueden enviar datos:<br /><br />-   **Aplicaciones administradas por directiva**: permite la transferencia tan solo a aplicaciones restringidas<br />-   **Todas las aplicaciones**: permite la transferencia a cualquier aplicación<br />-   **Ninguno**: no permite la transferencia de datos a ninguna aplicación|**Aplicaciones administradas por directiva**|
|**Permitir que la aplicación reciba datos de otras aplicaciones**|Especifique desde qué aplicaciones se pueden transferir datos a las aplicaciones administradas por directiva:<br /><br />-   **Aplicaciones administradas por directiva**: permite las transferencias de datos tan solo desde otras aplicaciones restringidas<br />-   **Todas las aplicaciones**: permite la transferencia de datos desde cualquier aplicación<br />-   **Ninguno**: no permite la transferencia de datos desde ninguna aplicación|**Todas las aplicaciones**|
|**Impedir Guardar como**|Seleccione **Sí** para deshabilitar el uso de la opción Guardar como en cualquier aplicación que use esta directiva. Seleccione **No** si desea permitir el uso de Guardar como.|**Sí**|
|**Restringir cortar, copiar y pegar con otras aplicaciones**|Especifique cuándo se deben restringir las operaciones de cortar, copiar y pegar. Elija de entre las siguientes opciones:<br /><br />-   **Bloqueado**: no permite las operaciones de cortar, copiar y pegar entre aplicaciones administradas por directiva.<br />-   **Aplicaciones administradas por directiva**: solamente permite las operaciones de cortar, copiar y pegar entre aplicaciones administradas por directiva.<br />-   **Aplicaciones administradas por directiva con Pegar en**: permite el corte o copia de los datos entre aplicaciones administradas por directiva. Permitir que los datos cortados o copiados desde cualquier aplicación se peguen en esta aplicación.<br />-   Cualquier aplicación: sin restricciones para las operaciones de cortar, copiar y pegar entre cualquier aplicación.|**Aplicaciones administradas por directiva con Pegar en**|
|**Cifrar datos de aplicación**|En el caso de aplicaciones que están asociadas a una directiva de administración de aplicaciones móviles de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], los datos se cifran en reposo con el cifrado de nivel de dispositivo proporcionado por el sistema operativo. Cuando se requiere un PIN, los datos se cifran según la configuración de la directiva de administración de aplicaciones móviles. Como se indica en la documentación de Apple, [los módulos usados por iOS 7 están certificados mediante FIPS 140-2](http://support.apple.com/en-us/HT202739).<br /><br />En la configuración de directiva, puede especificar valores de cifrado de PIN.  Estos valores determinan cuándo se cifran los datos. Las opciones son:<br /><br />-   **Cuando el dispositivo esté bloqueado:** todos los datos de la aplicación asociados a esta directiva se cifran mientras el dispositivo está bloqueado.<br />-   **Cuando el dispositivo esté bloqueado (excepto archivos abiertos):** todos los datos de la aplicación asociados a esta directiva se cifran mientras el dispositivo está bloqueado, excepto los datos de los archivos que están abiertos en la aplicación.<br />-   **Después de reiniciar el dispositivo:** todos los datos de la aplicación asociados a esta directiva se cifran al reiniciar el dispositivo, hasta que se desbloquee el dispositivo por primera vez.<br />-   **Usar la configuración del dispositivo:** los datos de la aplicación se cifran en función de la configuración predeterminada del dispositivo.<br /><br />Si habilita esta configuración, el usuario final deberá configurar y usar un PIN para acceder a su dispositivo.  Si no se configura ningún PIN para el acceso al dispositivo, las aplicaciones no se iniciarán y se le solicitará al usuario final que establezca un PIN con un mensaje: "La compañía ha requerido que primero debe habilitar un PIN de dispositivo para tener acceso a esta aplicación."|La opción de cifrado no está seleccionada|
**Configuración de directiva de acceso de iOS**

||||
|-|-|-|
|**Configuración de directiva**|**Descripción**|**Valor predeterminado**|
|**Requerir PIN simple en acceso**|Seleccione **Sí** para solicitar un PIN para usar las aplicaciones administradas por directiva. Se pedirá al usuario que lo configure la primera vez que ejecuta la aplicación en un contexto laboral.|**Sí**|
|**Número de intentos antes de restablecimiento del PIN**|Especifique el número de intentos de entrada de PIN que pueden realizarse antes de que el usuario deba restablecer el PIN.|No hay ningún valor predeterminado para esta configuración|
|**Requerir huella digital en lugar de PIN (iOS 8.0+)**|Seleccione **Sí** para solicitar una identidad mediante huella digital en lugar de un número PIN para el acceso a la aplicación.<br /><br />En los dispositivos iOS, puede permitir que los usuarios se identifiquen mediante huellas digitales en dispositivos iOS en lugar de mediante un número PIN. Cuando el usuario final intenta acceder a esta aplicación con su cuenta profesional, se le solicitará que indique su identidad mediante huellas digitales en lugar de escribir un número PIN.|**Sí**|
|**Requerir credenciales corporativas en acceso**|Seleccione **Sí** para solicitar credenciales corporativas en lugar de un PIN para el acceso a la aplicación. **Note:** Si se establece en Sí, se reemplazarán los requisitos de introducción de un PIN o un Touch ID.  Se le solicitará al usuario que proporcione sus credenciales corporativas.|**No**|
|**Bloquear la ejecución de aplicaciones administradas en dispositivos liberados o modificados**|Seleccione **Sí** para bloquear la ejecución de aplicaciones en dispositivos liberados o modificados. El usuario seguirá siendo capaz de usar las aplicaciones para las tareas personales, pero tendrá que usar un dispositivo distinto para el trabajo.|**Sí**|
|**Volver a comprobar los requisitos de acceso después de (minutos)**|-   **Tiempo de espera:** tiempo (en minutos) que debe transcurrir antes de que se vuelvan a comprobar los requisitos de acceso de la aplicación.<br />-   **Período de gracia sin conexión:** si el dispositivo está desconectado, el período de tiempo (en minutos) que debe transcurrir antes de que se vuelvan a comprobar los requisitos de acceso de la aplicación.|**Tiempo de espera de 30 minutos y 720 minutos de período de gracia sin conexión**|
|**Intervalo sin conexión antes de que se borren los datos de la aplicación (días)**|Puede borrar los datos de la compañía si un dispositivo ha estado desconectado durante un período determinado.  En la hoja de configuración de la directiva, puede especificar el número de días que un dispositivo puede estar sin conexión antes de que se eliminen los datos de la compañía del dispositivo. **Tip:** Si introduce un valor de 0 se desactivará esta opción.|**90 días**|
**Configuración de la reubicación de datos de Android**

||||
|-|-|-|
|**Configuración de directiva**|**Descripción**|**Valor predeterminado**|
|**Impedir copias de seguridad de Android**|Seleccione **Sí** para deshabilitar, o **No** para permitir la copia de seguridad de cualquier información de las aplicaciones administradas por directivas.|**Sí**|
|**Permitir que la aplicación transfiera datos a otras aplicaciones**|Seleccione una de las opciones para especificar las aplicaciones a las que las aplicaciones administradas por la directiva pueden enviar datos:<br /><br />-   **Aplicaciones administradas por directiva**: permite la transferencia tan solo a aplicaciones restringidas<br />-   **Todas las aplicaciones**: permite la transferencia a cualquier aplicación<br />-   **Ninguno**: no permite la transferencia de datos a ninguna aplicación|**Aplicaciones administradas por directiva**|
|**Permitir que la aplicación reciba datos de otras aplicaciones**|Especifique desde qué aplicaciones se pueden transferir datos a las aplicaciones administradas por directiva:<br /><br />-   **Aplicaciones administradas por directiva**: permite las transferencias de datos tan solo desde otras aplicaciones restringidas<br />-   **Todas las aplicaciones**: permite la transferencia de datos desde cualquier aplicación<br />-   **Ninguno**: no permite la transferencia de datos desde ninguna aplicación|**Todas las aplicaciones**|
|**Impedir Guardar como**|Seleccione **Sí** para deshabilitar el uso de la opción Guardar como en cualquier aplicación que use esta directiva. Seleccione **No** si desea permitir el uso de Guardar como.|**Sí**|
|**Restringir cortar, copiar y pegar con otras aplicaciones**|Especifique cuándo se deben restringir las operaciones de cortar, copiar y pegar. Elija de entre las siguientes opciones:<br /><br />-   **Bloqueado**: no permite las operaciones de cortar, copiar y pegar entre aplicaciones administradas por directiva.<br />-   **Aplicaciones administradas por directiva**: solamente permite las operaciones de cortar, copiar y pegar entre aplicaciones administradas por directiva.<br />-   **Aplicaciones administradas por directiva con Pegar en**: permite el corte o copia de los datos entre aplicaciones administradas por directiva. Permitir que los datos cortados o copiados desde cualquier aplicación se peguen en esta aplicación.<br />-   Cualquier aplicación: sin restricciones para las operaciones de cortar, copiar y pegar entre cualquier aplicación.|**Aplicaciones administradas por directiva con Pegar en**|
|**Cifrar datos de aplicación**|En el caso de las aplicaciones que están asociadas a una directiva de administración de aplicaciones móviles de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], Microsoft proporciona el cifrado. Los datos se cifran de forma sincrónica durante las operaciones de E/S de archivos según la configuración de la directiva de administración de aplicaciones móviles.<br /><br />Las aplicaciones administradas en Android usan el cifrado AES-128 en modo CBC mediante las bibliotecas de criptografía de la plataforma. El método de cifrado no está certificado mediante FIPS 140-2. El cifrado SHA-256 se admite como una instrucción explícita mediante el parámetro SigAlg y solo funcionará en dispositivos 4.2 y con versiones posteriores. El contenido del almacenamiento del dispositivo estará siempre cifrado.<br /><br />Si establece esta opción en **Sí**, el usuario final deberá configurar y usar un PIN para acceder a su dispositivo.  Si no se configura ningún PIN para el acceso al dispositivo, las aplicaciones no se iniciarán y se le solicitará al usuario final que establezca un PIN con un mensaje: *"La compañía ha requerido que primero debe habilitar un PIN de dispositivo para tener acceso a esta aplicación."*|La opción de cifrado no está seleccionada|
**Configuración de directiva de acceso de Android**

||||
|-|-|-|
|**Configuración de directiva**|**Descripción**|**Valor predeterminado**|
|**Requerir PIN simple en acceso**|Seleccione **Sí** para solicitar un PIN para usar las aplicaciones administradas por directiva. Se pedirá al usuario que lo configure la primera vez que ejecuta la aplicación en un contexto laboral.|**Sí**|
|**Número de intentos antes de restablecimiento del PIN**|Especifique el número de intentos de entrada de PIN que pueden realizarse antes de que el usuario deba restablecer el PIN.|No hay ningún valor predeterminado para esta configuración|
|**Requerir credenciales corporativas en acceso**|Seleccione **Sí** para solicitar credenciales corporativas en lugar de un PIN para el acceso a la aplicación. **Note:** Si se establece en **Sí**, se reemplazarán los requisitos de introducción de un PIN o un Touch ID.  Se le solicitará al usuario que proporcione sus credenciales corporativas.|**No**|
|**Bloquear la ejecución de aplicaciones administradas en dispositivos liberados o modificados**|Seleccione **Sí** para bloquear la ejecución de aplicaciones en dispositivos liberados o modificados. El usuario seguirá siendo capaz de usar las aplicaciones para las tareas personales, pero tendrá que usar un dispositivo distinto para el trabajo.|**Sí**|
|**Volver a comprobar los requisitos de acceso después de (minutos)**|-   **Tiempo de espera:** tiempo (en minutos) que debe transcurrir antes de que se vuelvan a comprobar los requisitos de acceso de la aplicación.<br />-   **Período de gracia sin conexión:** si el dispositivo está desconectado, el período de tiempo (en minutos) que debe transcurrir antes de que se vuelvan a comprobar los requisitos de acceso de la aplicación.|**Tiempo de espera de 30 minutos y 720 minutos de período de gracia sin conexión**|
|**Intervalo sin conexión antes de que se borren los datos de la aplicación (días)**|Puede borrar los datos de la compañía si un dispositivo ha estado desconectado durante un período determinado.  En la hoja de configuración de la directiva, puede especificar el número de días que un dispositivo puede estar sin conexión antes de que se eliminen los datos de la compañía del dispositivo. **Tip:** Si introduce un valor de 0 se desactivará esta opción.|**90 días**|
|**Bloquear captura de pantalla y Android Assistant (Android 6 Marshmallow o versiones posteriores)**|Seleccione **Sí** para especificar que las funcionalidades de captura de pantalla y **Android Assistant** del dispositivo se bloqueen cuando se usa esta aplicación.||

### <a name="bkmk_nextsteps"></a>Pasos siguientes
[Supervisión de directivas de administración de aplicaciones móviles con Microsoft Intune](../Topic/Monitor-mobile-app-management-policies-with-Microsoft-Intune.md)

## Vea también
[Configurar directivas de aplicaciones de prevención de pérdida de datos con Microsoft Intune](../Topic/Configure-data-loss-prevention-app-policies-with-Microsoft-Intune.md)

