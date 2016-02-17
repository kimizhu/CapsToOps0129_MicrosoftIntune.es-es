---
title: Tareas comunes de administraci&#243;n de PC Windows con el cliente de equipo de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb912c73-54d2-4d78-ac34-3cbe825804c7
---
# Tareas comunes de administraci&#243;n de PC Windows con el cliente de equipo de Microsoft Intune
Revise la información de este tema para aprender a administrar los equipos que ejecutan el cliente de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Si aún no ha instalado el cliente en sus equipos, vea [Instalar al cliente de equipos Windows con Microsoft Intune](../Topic/Install-the-Windows-PC-client-with-Microsoft-Intune.md).

## <a name="BKMK_PolicyTasks"></a>Tareas que utilizan directivas de Microsoft Intune

### Uso de directivas para administrar el Firewall de Windows
Las directivas simplifican la administración de la configuración del Firewall de Windows en los equipos administrados. Para obtener más información, consulte [Ayudar a proteger los equipos de Windows con Endpoint Protection para Microsoft Intune](../Topic/Help-secure-Windows-PCs-with-Endpoint-Protection-for-Microsoft-Intune.md).

### Usar directivas para administrar Microsoft Intune Center
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center permite a los usuarios:

-   Obtener aplicaciones desde el portal de empresa.

-   Comprobar si hay actualizaciones.

-   Administrar [!INCLUDE[epshort](../Token/epshort_md.md)] de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

-   Solicitar asistencia remota.

[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center se instala en todos los equipos administrados. Puede establecer la siguiente configuración en una directiva de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center; estos valores de configuración se muestran a los usuarios en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Center:

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Nombre**|El nombre del administrador del equipo.<br /><br />Longitud máxima: 40 caracteres|
|**Número de teléfono**|El número de teléfono del administrador del equipo.<br /><br />Longitud máxima: 20 caracteres|
|**Dirección de correo electrónico**|La dirección de correo electrónico del administrador del equipo.<br /><br />Longitud máxima: 40 caracteres|
|**Nombre del sitio web**|El nombre del sitio web de soporte para los usuarios.<br /><br />Longitud máxima: 40 caracteres|
|**Dirección URL del sitio web**|La dirección URL del sitio web de soporte.<br /><br />Longitud máxima: 150 caracteres|
|**Notas**|Una nota que se muestra a los usuarios.<br /><br />Longitud máxima: 120 caracteres|

### Uso de directivas para administrar la configuración de actualizaciones de software
Use directivas para establecer la configuración que los equipos administrados utilizan para buscar y descargar actualizaciones de software de Microsoft y de otros fabricantes. Para obtener más información, vea [Mantener los equipos Windows al día con las actualizaciones de software de Microsoft Intune](../Topic/Keep-Windows-PCs-up-to-date-with-software-updates-in-Microsoft-Intune.md).

### Uso de directivas para administrar la configuración de Endpoint Protection
Use directivas para establecer la configuración de [!INCLUDE[epshort](../Token/epshort_md.md)] que se implementará en los equipos administrados. Esto incluye, entre otras cosas, la programación de exámenes y las acciones que hay que realizar cuando se detecta malware. Para obtener más información, vea [Ayudar a proteger los equipos de Windows con Endpoint Protection para Microsoft Intune](../Topic/Help-secure-Windows-PCs-with-Endpoint-Protection-for-Microsoft-Intune.md).

## <a name="BKMK_Inventory"></a>Ver el Inventario de hardware y software
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] recopila información detallada sobre el hardware y el software de los equipos administrados. Use la información de los siguientes procedimientos para aprender a crear:

-   Un informe que muestra información acerca de las capacidades de hardware de los equipos.

-   Un informe que muestra la lista de software instalado en cada equipo.

-   Cómo actualizar un inventario de equipos para asegurarse de que los datos del informe estén al día.

#### Para mostrar información acerca de los equipos

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com/), haga clic en **Informes** &gt; **Informes de inventario de equipos**.

2.  En la página **Crear nuevo informe**, acepte los valores predeterminados o personalícelos para filtrar los resultados devueltos por el informe. Por ejemplo, puede seleccionar que en el informe sólo se muestren los equipos que ejecutan Windows 8.1.

3.  Haga clic en **Ver informe** para abrir el **Informe de inventario de equipos** en una nueva ventana.

    Puede ordenar el informe por cualquiera de las columnas, como **Nombre**, **Tipo de chasis** o **Fabricante** haciendo clic en el encabezado de columna correspondiente.

#### Para mostrar el software instalado en sus equipos

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com/), haga clic en **Informes** &gt; **Informes de software detectado**.

2.  En la página **Crear nuevo informe**, acepte los valores predeterminados o personalícelos para filtrar los resultados devueltos por el informe. Por ejemplo, puede seleccionar que en el informe sólo se muestre el software publicado por Microsoft.

3.  Haga clic en **Ver informe** para abrir el **Informe de software detectado** en una nueva ventana.

    Puede ordenar el informe por cualquiera de las columnas, como **Nombre**, **Editor** o **Categoría** haciendo clic en el encabezado de columna correspondiente. Puede hacer clic en la flecha situada junto al elemento de lista para expandir las actualizaciones de la lista a fin de mostrar más detalles (como los equipos en los que están instaladas).

#### Para actualizar el inventario de equipos a fin de asegurarse de que está al día

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com/), haga clic en **Grupos** &gt; **Todos los dispositivos** (o en otro grupo que contenga el equipo para el que desea actualizar el inventario).

2.  Seleccione un equipo o mantenga presionada la tecla **Ctrl** para seleccionar varios equipos.

3.  En la barra de tareas, haga clic en **Tareas remotas** &gt; **Actualizar inventario**.

4.  Para ver el estado de la tarea, haga clic en **Tareas remotas** en la esquina inferior derecha de la página.

    Se abre el cuadro de diálogo **Estado de la tarea**, que muestra las tareas remotas actuales, el estado de la tarea, el nombre del dispositivo y los errores notificados, y proporciona un vínculo a información de solución de problemas, si es necesario.

## <a name="BKMK_Additional"></a>Tareas adicionales
Además de las directivas, también puede realizar las siguientes tareas de administración en los equipos:

#### Para reiniciar de forma remota un equipo

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com/), haga clic en **Grupos** &gt; **Todos los dispositivos** (o en otro grupo que contenga el equipo que desea reiniciar).

2.  Seleccione uno o más equipos y, a continuación, haga clic en **Tareas remotas** &gt; **Reiniciar el equipo**.

3.  Para ver el estado de la tarea, haga clic en **Tareas remotas** en la esquina inferior derecha de la página.

4.  En el cuadro de diálogo **Estado de la tarea**, revise las tareas remotas actuales, el estado de la tarea, el nombre del dispositivo y los errores notificados.

### <a name="BKMK_Retire"></a>Para retirar un equipo

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com/), haga clic en **Grupos** &gt; **Todos los dispositivos** (o en otro grupo que contenga el equipo que desea retirar).

2.  Seleccione los dispositivos que desea retirar y, a continuación, haga clic en **Retirar/Eliminar datos**.

Para volver a inscribir un equipo en el servicio [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], vuelva a instalar el software cliente en el equipo, de la manera indicada en el tema [Instalar al cliente de equipos Windows con Microsoft Intune](../Topic/Install-the-Windows-PC-client-with-Microsoft-Intune.md).

Si un equipo no puede conectarse a [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], se muestra un mensaje en el área de trabajo **Panel**.

Cuando retira un equipo:

-   Se quita del inventario de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] y la licencia asociada al equipo queda disponible para su reutilización.

-   Su estado deja de aparecer en la [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

-   [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] quita el software cliente del equipo. Si el equipo no está conectado al servicio [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], se quitará el software cliente la próxima vez que se conecte.

-   Se quita [!INCLUDE[epshort](../Token/epshort_md.md)] del equipo. Si el equipo tiene instalada otra aplicación de extremos que se encuentra deshabilitada, dicha aplicación puede habilitarse de nuevo después de quitar [!INCLUDE[epshort](../Token/epshort_md.md)], a fin de garantizar la protección del equipo.

-   Se quitan las directivas del equipo y se cambian los valores establecidos por las directivas.

-   El equipo deja de recibir las actualizaciones de software o de definiciones de malware desde el servicio [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

-   Según como estén configurados, los equipos retirados pueden seguir recibiendo actualizaciones mediante Windows Server Update Services, Windows Update o Microsoft Update.

    > [!IMPORTANT]
    > Si el software cliente se instaló con un objeto de directiva de grupo (GPO), debe quitar dicho objeto para poder quitar el software cliente, a fin de evitar que el software se reinstale.

    Si no se puede desinstalar el cliente, lea [Solucionar problemas de Endpoint Protection en Microsoft Intune](../Topic/Troubleshoot-Endpoint-Protection-in-Microsoft-Intune.md) para obtener más ayuda.

### <a name="BKMK_UserDeviceLinking"></a>Administración de la vinculación usuario-dispositivo
Antes de implementar software en un usuario, debe vincular el usuario a un equipo. Puede vincular un usuario a varios equipos, pero cada equipo puede vincularse sólo a un usuario. Los usuarios se vinculan automáticamente a los equipos que inscriben en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a través del portal de empresa.

##### Para vincular un usuario a un equipo

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com/), haga clic en **Grupos** &gt; **Todos los dispositivos** (o en otro grupo que contenga el equipo que desea vincular a un usuario).

2.  Seleccione el equipo que desea vincular a un usuario y, a continuación, haga clic en **Vincular usuario**.

    El cuadro de diálogo **Vincular usuario** muestra una lista de usuarios disponibles con su nombre para mostrar, Id. de usuario, y el número de equipos a los que cada usuario que está vinculado. Si un usuario ya está vinculado al equipo seleccionado, el nombre del usuario y su Id. se muestran en **Usuario actual**. Si el equipo no está vinculado a ningún usuario, aparece **Ningún usuario** bajo el **Usuario actual**.

3.  Realice una de las siguientes acciones:

    -   Para dejar el equipo vinculado a su usuario actual, si hay alguno, haga clic en **Cancelar**.

    -   Para quitar el vínculo al usuario actual, si lo hubiera, haga clic en **Quitar vínculo** &gt; **Aceptar**.

    -   Para vincular el equipo a un usuario nuevo, en la lista **Todos los usuarios**, seleccione un usuario. Confirme que los datos de usuario están correctos y, a continuación, haga clic en **Aceptar**.

> [!TIP]
> Si desea restringir la capacidad de los usuarios finales para vincularse a equipos, habilite la opción **Restringir la capacidad de los usuarios de vincularse a equipos** en la directiva de **Configuración de agente de Microsoft Intune**.

### Respuesta a una solicitud de asistencia remota
Los usuarios pueden solicitar ayuda mediante Asistencia remota a través de Microsoft Easy Assist, que se instala automáticamente en los equipos administrados. Cuando se realiza una solicitud, se muestra una alerta en la consola de administrador de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

> [!IMPORTANT]
> La asistencia remota no está disponible en los equipos que ejecutan Windows 8 o versiones posteriores.
> 
> Si acepta una solicitud de asistencia remota de un equipo que no tiene Microsoft Easy Assist instalado, se pedirá al usuario que lo instale. Después de la instalación debe reiniciar el equipo. Considere la posibilidad de realizar una carga previa de Microsoft Easy Assist en los equipos del usuario para evitar este reinicio.

##### Para administrar una solicitud de asistencia remota

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com/), haga clic en **Alertas** &gt; **Asistencia remota**.

2.  Seleccione una solicitud de asistencia remota en la lista **Alertas** para abrir la página de propiedades de la solicitud.

3.  Haga clic en **Aprobar solicitud e iniciar asistencia remota** para abrir un cuadro de diálogo que proporciona opciones para resolver la alerta.

4.  Realice una de las siguientes acciones:

    -   **Aceptar la solicitud**: para unirse a la sesión remota, haga clic en **Aceptar la solicitud de asistencia remota**.

        El usuario recibe el siguiente mensaje: **Se aceptó la solicitud**. **Siga las instrucciones indicadas en Easy Assist para compartir un programa o su escritorio con el administrador del sistema**.

        > [!IMPORTANT]
        > No puede aceptar una solicitud de asistencia remota en un equipo Mac que ejecuta la [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

    -   **Rechazar la solicitud**: cierre la ventana **Ver información de solución de problemas** y después haga clic en **Cerrar esta alerta** en la ventana de propiedades de la alerta.

        Se cierra la solicitud y el usuario verá un mensaje que indica que la solicitud ha sido rechazada. Para volver a solicitar asistencia remota el usuario deberá enviar una nueva solicitud de asistencia remota. Si cierra accidentalmente una alerta de asistencia remota, póngase en contacto con el usuario que envió la solicitud de asistencia remota para pedirle que envíe otra solicitud.

## <a name="BKMK_Next"></a>¿Necesita más ayuda?
Para obtener más ayuda y soporte técnico, vea [Solucionar problemas de Endpoint Protection en Microsoft Intune](../Topic/Troubleshoot-Endpoint-Protection-in-Microsoft-Intune.md).

## Vea también
[Administrar equipos Windows con Microsoft Intune](../Topic/Manage-Windows-PCs-with-Microsoft-Intune.md)

