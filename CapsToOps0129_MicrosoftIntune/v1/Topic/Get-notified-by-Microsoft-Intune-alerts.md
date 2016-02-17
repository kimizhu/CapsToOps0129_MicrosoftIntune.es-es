---
title: Recibir notificaciones mediante alertas de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 396ea714-0433-4bd5-a934-8d0b477f28e4
---
# Recibir notificaciones mediante alertas de Microsoft Intune
Las alertas le mantienen en contacto con lo que sucede en [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

Por ejemplo, las alertas le pueden notificar sobre los siguientes eventos:

-   Un problema con Exchange Connector que afecta a la administración de dispositivos móviles

-   Se encontró malware en un equipo

-   Se detectó un conflicto entre dos directivas de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

-   Las últimas actualizaciones e información sobre el servicio de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] (avisos).

## Funcionamiento de las alertas
Las alertas se generan según los **tipos de alerta**, un conjunto de reglas configuradas previamente e integradas en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Por ejemplo, el tipo de alerta **El almacenamiento en nube tiene un 10% de espacio libre o menos** le avisa cuando se está quedando sin espacio para almacenar sus aplicaciones en la nube. Puede habilitar o deshabilitar, así como configurar las propiedades de cada tipo de alerta. Por ejemplo, con el tipo de alerta anterior, puede configurar:

-   **Estado:** si el tipo de alerta está habilitado o deshabilitado

-   **Gravedad:** ¿es grave esta alerta?

    |||
    |-|-|
    |Gravedad|Descripción|
    |![](../Image/Critical-Alert.jpg)|Indica que hay un problema grave que debería investigar lo antes posible, por ejemplo, si se detectó malware en un equipo.|
    |![](../Image/Warning-Alert.jpg)|Indica que hay un problema que actualmente no es grave, pero podría llegar a serlo si no se le presta atención, por ejemplo, cuando las actualizaciones de seguridad están esperando para ser instaladas.|
    |![](../Image/Informational-Alert.jpg)|Indica información que no es crítica para sus operaciones, por ejemplo, cuando hay una nueva versión de Exchange Connector disponible.|

Otros tipos de alerta pueden contener diferentes elementos configurables, como el porcentaje de dispositivos que debe estar afectado por un problema antes de que se genere una alerta.

**Cuando se cumplen los criterios de un tipo de alerta, se genera una alerta y se muestra en la consola del administrador de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].**

Además, puede configurar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] para que le envíe una notificación por correo electrónico cuando se genere una alerta.

## Configuración de alertas
En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Administración** &gt; **Alertas y notificaciones** y, a continuación, elija una de las tareas de configuración siguientes:

|Tarea|Descripción|
|---------|---------------|
|**Tipos de alertas**|Elija el tipo de alerta que desee configurar y, a continuación, realice una de las acciones siguientes:<br /><br />-   Haga clic en **Configurar**. En el cuadro de diálogo **Configurar tipo de alerta**, configure las opciones que desee y, después, haga clic en **Aceptar**.<br />-   **Habilite** o **deshabilite** la alerta. **Tip:** Expanda el nodo **Tipos de alerta** y haga clic en una categoría para ver solo los tipos de esa categoría.|
|**Destinatarios**|Haga clic en **Agregar** para agregar una nueva dirección de correo electrónico en la que quiera recibir las notificaciones de correo electrónico que configure.<br /><br />También puede **Editar** o **Eliminar** los destinatarios existentes. **Tip:** Para recibir notificaciones, también debe agregar esta dirección de correo electrónico como destinatario en **Reglas de notificación**.|
|**Reglas de notificación**|Configura las reglas que definen a quién se enviará una alerta de correo electrónico. Puede hacer lo siguiente:<br /><br /><ul><li>**Elegir una regla existente**: elija una regla y, a continuación, haga clic en **Seleccionar destinatarios**. Después, puede seleccionar todos los destinatarios que recibirán un correo electrónico cuando se genere una alerta que cumpla esta regla.</li><li>**Crear una regla nueva**: haga clic en **Crear nueva regla** y, a continuación:<br /><br /><ol><li>Escriba un nombre para la regla y, después, seleccione las categorías y la gravedad de alerta que afectarán a la regla.</li><li>Seleccione los grupos de dispositivos a los que se aplicará la regla.</li><li>Seleccione los usuarios que recibirán un correo electrónico cuando se genere una alerta.</li></ol></li><li>Haga clic en **Guardar**.</li></ul>También puede **Habilitar**, **Deshabilitar**, **Editar** o **Eliminar** una regla existente.|

## Trabajo con alertas
Las siguientes opciones le ayudarán a trabajar con alertas desde la consola de administración de Intune.

|Opción|Descripción|
|----------|---------------|
|Ver alertas activas|Elija una de las siguientes:<br /><br />-   **Ver un resumen de las alertas**: en el área de trabajo **Panel**, los errores principales se muestran en el panel Alertas. Haga clic en el panel para ver información más detallada.<br />    Además, puede ver un resumen de las alertas en la página **General** del área de trabajo **Alertas**.<br />-   **Ver todas las alertas**: en el área de trabajo **Alertas**, haga clic en **Todas las alertas**.|
|Ver avisos|Elija una de las siguientes:<br /><br />-   En el área de trabajo **Panel**, haga clic en **Avisos**.<br />-   En el área de trabajo **Alertas**, haga clic en **Todas las alertas** &gt; **Avisos**.|
|Cerrar una alerta|En la lista de alertas, seleccione la alerta que desee cerrar y, a continuación, haga clic en **Cerrar alerta**.<br /><br />Las alertas cerradas se eliminan permanentemente después de 90 días.|
|Reactivar una alerta cerrada|En la lista de alertas, establezca el desplegable **Filtros** en **Cerradas**.<br /><br />En la lista de alertas cerradas, seleccione la alerta que desee reactivar y, a continuación, haga clic en **Reactivar alerta**.|
Las alertas de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] permanecen activas hasta que se produzca lo siguiente:

-   Se resuelve el problema que provocó la alerta

-   La alerta se cierra manualmente

-   Transcurrieron 45 días desde que se generó la alerta

> [!TIP]
> Si varios dispositivos que ejecutan sistemas operativos diferentes generan la misma alerta, es probable que vea varias versiones de la misma alerta en la lista de alertas.

## Vea también
[Supervisión e informes](../Topic/Monitoring-and-reports-with-Microsoft-Intune.md)

