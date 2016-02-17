---
title: Ayudar a proteger los equipos de Windows con Endpoint Protection para Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 682a83ec-bcf4-46ed-9a74-61b87b6a86a3
---
# Ayudar a proteger los equipos de Windows con Endpoint Protection para Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] puede ayudarle a proteger los equipos administrados de varias maneras. Una de ellas es Endpoint Protection, que proporciona protección en tiempo real contra amenazas de malware, mantiene las definiciones de malware actualizadas y examina automáticamente los equipos.[!INCLUDE[epshort](../Token/epshort_md.md)] también proporciona herramientas que ayudan a administrar y supervisar los ataques de malware

Si aún no ha instalado el cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en los equipos, vea [Instalar al cliente de equipos Windows con Microsoft Intune](../Topic/Install-the-Windows-PC-client-with-Microsoft-Intune.md).

Use la información de las secciones siguientes, que le facilitará la configuración de la implementación y la subpervisión de [!INCLUDE[epshort](../Token/epshort_md.md)].

## Usar Endpoint Protection en Microsoft Intune

### Antes de empezar
Una de las principales prioridades de un administrador de TI es proteger los equipos administrados contra virus y malware. Antes de implementar [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] en los equipos cliente de su organización debe decidir la manera de proteger los equipos seleccionando una de las siguientes opciones y configurando las opciones de la directiva asociada:

|Deseo:|Configuración de directivas de Endpoint Protection|Más información|
|----------|------------------------------------------------------|-------------------|
|Use [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] únicamente si no está instalada ninguna aplicación de protección de extremos de otro fabricante.<br /><br />Puede usar [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] en todos los equipos en los que no esté instalada una aplicación de protección de extremos de otro fabricante.|-   Instalar Endpoint Protection = **Sí**<br />-   Habilitar Endpoint Protection = **Sí**<br />-   Instalar Endpoint Protection incluso si hay una aplicación de protección de extremos de otro fabricante instalada = **No**|Si se detecta una aplicación de protección de extremos de otro fabricante, [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] no se instalará o se desinstalará si ya se ha instalado.|
|Use [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] aunque esté instalada una aplicación de protección de extremos de otro fabricante.<br /><br />Con este enfoque, se ejecutarán simultáneamente [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] y la aplicación de protección de extremos de otro fabricante (si está instalada). No se recomienda esta configuración porque puede provocar problemas de rendimiento.|-   Instalar Endpoint Protection = **Sí**<br />-   Habilitar Endpoint Protection = **Sí**<br />-   Instalar Endpoint Protection incluso si hay una aplicación de protección de extremos de otro fabricante instalada = **Sí**|Se debe usar cuando:<br /><br />-   Se desea cambiar a [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)].<br />-   Se implementa un cliente nuevo que va a utilizar [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)].<br />-   Se actualiza cualquier cliente que va a utilizar [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)].|
|Se usa [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] sin [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)].<br /><br />En este caso, no usará [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] para proteger los equipos frente a malware y virus. En lugar de ello va a utilizar una aplicación de protección de extremos de otro fabricante.|-   Instalar Endpoint Protection = **No**|Si no utiliza una aplicación de protección de extremos de otro fabricante, no se recomienda esta configuración, ya que podría exponer los equipos de su organización a malware u otros ataques.<br /><br />[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)] no se instala, o se desinstala si estaba instalada.|
Si desea cambiar de su aplicación de protección de extremos actual a [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)], realice los siguientes pasos, que se describen con mayor detalle más adelante en este tema:

1.  Deje que su aplicación de actual de protección de extremos se siga ejecutando mientras se implementa el software cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en esos equipos.

2.  Compruebe que [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] está instalado y ayuda a proteger los equipos cliente.

3.  Quite el software de protección de extremos de un tercero de la manera siguiente:

    -   Utilice la distribución de software de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] para implementar una herramienta de eliminación de software proporcionada por el fabricante de la aplicación de protección de extremos de un tercero. Para obtener más información, vea [Implementar y configurar aplicaciones con Microsoft Intune](../Topic/Deploy-and-configure-apps-with-Microsoft-Intune.md).

    -   Quitar manualmente la aplicación de protección de extremos de otro fabricante.

> [!NOTE]
> [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] no desinstala aplicaciones de protección de extremos de otro fabricante.

### <a name="BKMK_HowtoConf"></a>Configuración de Microsoft Intune Endpoint Protection
Utilice el siguiente procedimiento como ayuda para configurar [!INCLUDE[epshort](../Token/epshort_md.md)] para [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] puede administrar [!INCLUDE[epshort](../Token/epshort_md.md)] para Windows 10 Technical Preview. Es posible que alguna configuración de directiva solo esté disponible para Windows 10.

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com/), haga clic en **Directiva** &gt; **Agregar directiva**.

2.  Configure e implemente una directiva de **configuración de agente de Microsoft Intune** para la configuración de [!INCLUDE[epshort](../Token/epshort_md.md)]. Puede usar la configuración recomendada o personalizar la configuración. Si necesita más información acerca de cómo crear e implementar directivas, consulte el tema [Tareas comunes de administración de PC Windows con el cliente de equipo de Microsoft Intune](../Topic/Common-Windows-PC-management-tasks-with-the-Microsoft-Intune-computer-client.md).

    Las tablas de después de este procedimiento muestran los valores que puede configurar en la directiva y también los valores recomendados que se utilizarán si no se personaliza la directiva. Puede encontrar estos valores en la sección **Endpoint Protection**.

Puede ver la directiva de [!INCLUDE[epshort](../Token/epshort_md.md)] implementada en la página **Todas las directivas** del área de trabajo **Directiva**.

#### Configuración del servicio Endpoint Protection

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Instalar Endpoint Protection**|Debe establecerse en **Sí** para instalar [!INCLUDE[epshort](../Token/epshort_md.md)] en equipos administrados. Si se detecta una aplicación de protección de extremos de otro fabricante durante la instalación, [!INCLUDE[epshort](../Token/epshort_md.md)] no se instalará a menos que la opción **Instalar Endpoint Protection incluso si hay una aplicación de protección de extremos de otro fabricante instalada** se establezca en **Sí**. **Note:** Intune [!INCLUDE[epshort](../Token/epshort_md.md)] se instala de manera predeterminada en equipos administrados. Si no desea que [!INCLUDE[epshort](../Token/epshort_md.md)] se instale en los equipos administrados, debe establecer explícitamente esta directiva en **No**. Si [!INCLUDE[epshort](../Token/epshort_md.md)] se instaló previamente y la directiva se actualiza a **No**, el cliente de [!INCLUDE[epshort](../Token/epshort_md.md)] se desinstalará.<br />Valor recomendado: **Sí**|
|**Instalar Endpoint Protection incluso si hay una aplicación de protección de extremos de otro fabricante instalada**|Debe establecerse en **Sí** para instalar [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)] aunque se detecte una aplicación de protección de extremos de otro fabricante.<br /><br />Valor recomendado: **Sí**|
|**Habilitar Endpoint Protection**|Debe establecerse en **Sí** para habilitar [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)] en equipos que tienen el cliente de [!INCLUDE[epshort](../Token/epshort_md.md)].<br /><br />Si se establece en **No** y [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)] está instalado, no se mostrará a los usuarios la interfaz de usuario cliente de [!INCLUDE[epshort](../Token/epshort_md.md)] y todas las características de protección estarán inactivas.<br /><br />Valor recomendado: **Sí**|
|**Deshabilitar UI cliente**|Debe establecerse en **Sí** para ocultar la interfaz de usuario cliente de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] a los usuarios (para que surta efecto hay que reiniciar el equipo cliente).<br /><br />Valor recomendado: **No**|
|**Instalar Endpoint Protection incluso si hay una aplicación de protección de extremos de otro fabricante instalada**|Debe establecerse en **Sí** para forzar la instalación de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] aunque se detecte una aplicación de protección de extremos de otro fabricante.<br /><br />Valor recomendado: **No**|
|**Crear un punto de restauración del sistema antes de eliminar malware**|Debe establecerse en **Sí** para crear un punto de restauración del sistema de Windows antes de que comience cualquier corrección de software malintencionado.<br /><br />Valor recomendado: **Sí**|
|**Realizar seguimiento de malware resuelto (días)**|Permite que [!INCLUDE[epshort](../Token/epshort_md.md)] haga un seguimiento de malware resuelto durante un tiempo especificado para que pueda comprobar manualmente los equipos infectados anteriormente.<br /><br />Puede especificar un valor comprendido entre 0 y 30 días.<br /><br />Valor recomendado: **7 días**|
Si estableció los valores de directivas de **Instalar Endpoint Protection** y **Habilitar Endpoint Protection** en **Sí** y de **Instalar Endpoint Protection incluso si hay una aplicación de protección de extremos de otro fabricante instalada** en **No**, [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] detectará que hay otra aplicación de protección de extremos instalada y no se instalará, o se desinstalará si ya está presente (sin embargo, [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] informará del estado de la otra aplicación de protección de extremos en la [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)]).

#### Configuración de protección en tiempo real

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Habilitar protección en tiempo real**|Habilita la supervisión y el examen de todos los archivos y aplicaciones a los que se accede. También bloquea las aplicaciones y los archivos malintencionados antes de que puedan ejecutarse en los equipos.<br /><br />Valor recomendado: **Sí**|
|**Analizar todas las descargas**|Habilita el examen de todos los archivos y datos adjuntos que se descargan de Internet a los equipos.<br /><br />Valor recomendado: **Sí**|
|**Supervisar la actividad de archivos y programas en los equipos**|Habilita la supervisión de los archivos entrantes y los archivos salientes, así como la actividad de los programas en los equipos. Con esta opción de configuración, [!INCLUDE[epshort](../Token/epshort_md.md)] puede supervisar cuándo empieza la ejecución de archivos y programas, y le envía alertas sobre las acciones que realizan o las acciones que se realizan con ellos.<br /><br />Valor recomendado: **Sí**|
|**Archivos supervisados**|Si la opción **Supervisar la actividad de archivos y programas en los equipos** está habilitada, esta opción de configuración permite elegir supervisar sólo los archivos entrantes, sólo los salientes o todos los archivos.<br /><br />Valor recomendado: **Supervisar todos los archivos**|
|**Habilitar supervisión del comportamiento**|Permite a [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] comprobar determinados patrones de actividad sospechosa en los equipos cliente.<br /><br />Valor recomendado: **Sí**|
|**Habilitar Sistema de inspección de red**|Habilita el Sistema de inspección de red (NIS) en los equipos cliente. NIS usa firmas de vulnerabilidades conocidas del [Microsoft Malware Protection Center (Centro de protección contra malware de Microsoft)](http://go.microsoft.com/fwlink/?LinkId=234249) para ayudar a detectar y bloquear tráfico de red malintencionado.<br /><br />Valor recomendado: **Sí**|

#### Configuración de programación de examen

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Programar un examen rápido diario**|Programa un examen rápido diario de los archivos de uso frecuente y los archivos importantes del sistema en los equipos. Este examen rápido tiene un efecto mínimo sobre el rendimiento.<br /><br />Valor recomendado: **Sí**|
|**Ejecutar un análisis rápido si no se han ejecutado dos análisis rápidos consecutivos**|Configura [!INCLUDE[epshort](../Token/epshort_md.md)] para que ejecute automáticamente un examen rápido en los equipos en caso de que no se realicen dos exámenes rápidos programados consecutivos.<br /><br />Valor recomendado: **Sí**|
|**Programar un examen completo**|Configura un examen completo de todos los archivos y recursos de los discos duros locales de los equipos. Este examen puede tardar y puede afectar al rendimiento de los equipos (en función del número de archivos y recursos analizados).<br /><br />Valor recomendado: **No**|
|**Ejecutar un análisis completo si no se han ejecutado dos análisis completos consecutivos**|Configura [!INCLUDE[epshort](../Token/epshort_md.md)] para que ejecute automáticamente un examen completo en los equipos en caso de que no se realicen dos exámenes consecutivos.<br /><br />Valor recomendado: No configurado|

#### Configuración de opciones de examen

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Ejecutar un análisis completo tras la instalación de Endpoint Protection**|Configura [!INCLUDE[epshort](../Token/epshort_md.md)] para que ejecute automáticamente un análisis completo del sistema después de instalarse en los equipos. Este examen se ejecuta únicamente cuando los equipos están inactivos para minimizar así el efecto en la productividad de los usuarios.<br /><br />Valor recomendado: **Sí**|
|**Ejecutar un examen completo automáticamente cuando es necesario hacer un seguimiento después de quitar malware**|Debe establecerse en **Sí** para permitir a [!INCLUDE[epshort](../Token/epshort_md.md)] ejecutar automáticamente un examen completo del sistema en los equipos tras eliminar malware, para comprobar que no haya otros archivos afectados.<br /><br />Valor recomendado: **Sí**|
|**Iniciar un examen programado sólo cuando el equipo está inactivo**|Debe establecerse en **Sí** para impedir que se inicien exámenes programados cuando los equipos se están usando a fin de no mermar la productividad de los usuarios.<br /><br />Valor recomendado: **Sí**|
|**Buscar las últimas definiciones de malware antes de iniciar un examen**|Debe establecerse en **Sí** para permitir que [!INCLUDE[epshort](../Token/epshort_md.md)] compruebe automáticamente las definiciones de malware más recientes antes de empezar a examinar los equipos.<br /><br />Valor recomendado: **Sí**|
|**Examinar archivos de almacenamiento**|Debe establecerse en **Sí** para configurar [!INCLUDE[epshort](../Token/epshort_md.md)] de forma que examine los archivos de almacenamiento (como los archivos .zip o .cab) de los equipos en busca de malware.<br /><br />Valor recomendado: **No**|
|**Analizar mensajes de correo electrónico**|Debe establecerse en **Sí** para configurar [!INCLUDE[epshort](../Token/epshort_md.md)] de forma que examine los mensajes entrantes cuando llegan a los equipos.<br /><br />Valor recomendado: **Sí**|
|**Examinar archivos abiertos desde carpetas compartidas de red**|Debe establecerse en **Sí** para configurar [!INCLUDE[epshort](../Token/epshort_md.md)] de forma que examine los archivos abiertos desde carpetas compartidas en la red. Normalmente se trata de archivos a los que se tiene acceso mediante una ruta de acceso UNC. Si se habilita esta función, los usuarios que tienen acceso de solo lectura pueden tener problemas, ya que no pueden eliminar el malware.<br /><br />Valor recomendado: **No**|
|**Examinar unidades de red asignadas**|Debe establecerse en **Sí** para configurar [!INCLUDE[epshort](../Token/epshort_md.md)] de forma que examine archivos en unidades de red asignadas. Si se habilita esta función, los usuarios que tienen acceso de solo lectura pueden tener problemas, ya que no pueden eliminar el malware.<br /><br />Valor recomendado: **No**|
|**Analizar unidades extraíbles**|Debe establecerse en **Sí** para configurar [!INCLUDE[epshort](../Token/epshort_md.md)] de forma que examine el contenido de las unidades extraíbles (como las unidades flash USB) en busca de malware al realizar un examen completo en los equipos.<br /><br />Valor recomendado: **Sí**|
|**Limitar el uso de la CPU durante un análisis a**|Configura el porcentaje máximo de uso de la CPU que se puede utilizar durante los exámenes programados en los equipos. Puede establecer este valor entre el 1 y el 100 por ciento.<br /><br />Valor recomendado: **50%**|

#### Configuración de acciones predeterminadas

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Elija cómo debe actuar Endpoint Protection ante malware de los siguientes niveles de alerta**|Especifica la acción predeterminada que [!INCLUDE[epshort](../Token/epshort_md.md)] lleva a cabo cuando se detecta malware de diversos niveles de alerta.<br /><br />Para cada nivel de la alerta puede quitar el malware, ponerlo en cuarentena o realizar la acción recomendada por Microsoft.<br /><br />Valor recomendado: **Acción recomendada**|

#### Configuración de archivos y carpetas excluidos

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Archivos y carpetas que se van a excluir al ejecutar un análisis o al usar la protección en tiempo real**|Excluye archivos o carpetas específicos cuando se ejecuta un examen o cuando se utiliza la protección en tiempo real en los equipos.|

#### Configuración de procesos excluidos

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Procesos que se deben excluir al ejecutar un análisis o al utilizar protección en tiempo real**|Permite excluir procesos específicos de la protección en tiempo real o al ejecutar un examen. Solo se pueden excluir los archivos con las siguientes extensiones: **.exe**, **.com** o **.scr**.|

#### Configuración de tipos de archivo excluidos

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Extensiones de archivo que se deben excluir al ejecutar un análisis o al utilizar protección en tiempo real**|Permite excluir extensiones de nombre de archivo específicas cuando se ejecute un análisis o cuando se use la protección en tiempo real en los equipos.|

#### Configuración de Microsoft Active Protection Service
Microsoft Active Protection Service es una comunidad en línea que ayuda a decidir cómo responder a amenazas potenciales. La comunidad también ayuda a detener la propagación de nuevas infecciones de malware.

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Únase a Microsoft Active Protection Service**|**Sí** envía automáticamente información sobre malware detectado a Microsoft Active Protection Service. Microsoft no usará la información recopilada para identificarle ni para ponerse en contacto con usted.<br /><br />Valor recomendado: **Sí**|
|**Nivel de pertenencia**|Si ha elegido unirse a Microsoft Active Protection Service, esta opción permite elegir uno de los siguientes niveles de pertenencia:<br /><br />-   **Básica**: envía a Microsoft información básica sobre el malware detectado. Esta información incluye de dónde procede el software, las acciones que el usuario aplica o que [!INCLUDE[epshort](../Token/epshort_md.md)] aplica automáticamente, y si las acciones obtuvieron resultados satisfactorios.<br />-   **Avanzada**: envía más información a Microsoft acerca de malware, spyware y software potencialmente no deseado. Esta información incluye la ubicación del software, los nombres de archivo, cómo funciona el software y cómo ha afectado al equipo.<br /><br />Valor recomendado: **Opciones avanzadas**|
|**Recibir definiciones dinámicas en función de los informes de Microsoft Active Protection Service**|**Sí** permite que los equipos reciban definiciones de malware dinámicas basándose en la información que [!INCLUDE[epshort](../Token/epshort_md.md)] envía a Microsoft Active Protection Service (si se ha unido a él) acerca del malware detectado.<br /><br />Valor recomendado: **Sí**|

### Tareas de administración para Endpoint Protection
Las siguientes tareas ayudan a realizar diversas tareas de administración en equipos administrados que ejecutan [!INCLUDE[epshort](../Token/epshort_md.md)].

|Deseo|Desde la consola de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|Desde el equipo administrado|
|---------|-----------------------------------------------------------------------------|--------------------------------|
|Actualizar definiciones de malware|Desde el área de trabajo **Grupos**, seleccione los equipos que desea actualizar.<br /><br />Haga clic en **Tareas remotas** &gt; **Actualizar definiciones de malware**.|Inicie el software cliente de [!INCLUDE[epshort](../Token/epshort_md.md)] en el área de notificación de Windows.<br /><br />Haga clic en la ficha **Actualizar** y, a continuación, haga clic en **Actualizar**.|
|Ejecutar un examen de malware|Desde el área de trabajo **Grupos**, seleccione los equipos que desea examinar.<br /><br />Haga clic en **Ejecutar un examen completo de malware** o en **Ejecutar un examen rápido de malware**.|Inicie el software cliente de [!INCLUDE[epshort](../Token/epshort_md.md)] en el área de notificación de Windows.<br /><br />Seleccione **Rápido**, **Completo** o **Personalizado** y, a continuación, haga clic en **Examinar ahora**.|
Para ver el estado de una tarea remota, haga clic en el vínculo **Tareas remotas** situado en la esquina inferior derecha de la [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

El cuadro de diálogo **Estado de la tarea remota** enumera las tareas remotas actuales, el estado de las tareas, el nombre del dispositivo y los errores notificados, y proporciona un vínculo a información de solución de problemas, si corresponde.

### <a name="BKMK_SCEPmon"></a>Supervisión de Endpoint Protection
Puede supervisar el estado de infección con malware en sus equipos a través del área de trabajo **Protección** de la [consola de administración de Microsoft Intune](https://manage.microsoft.com/). Esta área de trabajo contiene dos páginas:

|Nombre de la página|Más información|
|-----------------------|-------------------|
|**Información general de Endpoint Protection**|Muestra temas importantes como vínculos en los que puede hacer clic para obtener más información. Algunos problemas que podrían aparecer son:<br /><br />-   **Instancias de malware que requieren seguimiento**: haga clic en el vínculo para ver una lista de problemas de malware y las acciones de seguimiento correspondientes que hay que realizar para solucionar el problema. Puede profundizar en la lista para ver qué equipos están afectados.<br />-   **Equipos con malware que requieren seguimiento**: haga clic en el vínculo para ver todos los equipos con problemas de malware sin solucionar y las acciones de seguimiento correspondientes que hay que realizar para solucionar el problema.<br />-   **Dispositivos que no están protegidos**: haga clic en el vínculo para ver los equipos que no están protegidos por ningún software de protección de extremos, ya sea porque no hay ningún software instalado o porque hay un error. Seleccione un equipo para ver más detalles.<br />-   **Dispositivos con otra aplicación de Endpoint Protection en ejecución**: haga clic en el vínculo para ver los equipos que ejecutan una aplicación de protección del extremo de otro fabricante.|
|**Todo el malware**|Muestra una lista de todo el malware activo en los equipos. Puede profundizar en la para ver todos los equipos afectados por un elemento de malware determinado o puede seleccionar una de las siguientes tareas:<br /><br />-   **Ver propiedades**: abre una página con más información sobre el malware seleccionado.<br />-   **Más información sobre este malware** : abre un tema desde el Centro de protección contra malware de Microsoft con más información sobre el malware.|
> [!IMPORTANT]
> El área de trabajo **Protección** no se muestra en la consola de administrador hasta que se ha instalado el cliente y está administrando correctamente al menos un equipo cliente.

### Cómo ver las rutas de acceso de detección recientes de malware en equipos
Intune puede mostrar las 10 instancias de malware detectadas más recientemente en un dispositivo. La opción **Rutas de acceso de detección recientes** está deshabilitada de forma predeterminada. Para habilitar esta vista:

##### Cómo ver las rutas de acceso de detección recientes de malware en equipos

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com/), haga clic en **Grupos** &gt; **Todos los dispositivos**.**Malware**.

2.  Haga clic con el botón derecho en un encabezado de columna. Aparece una lista de las columnas disponibles.

3.  Marque la casilla **Rutas de acceso de detección recientes** en la lista. La columna **Rutas de acceso de detección recientes** aparece y muestra hasta las 10 instancias de malware más recientes que se han supervisado en el dispositivo.

## ¿Necesita más ayuda?
Para obtener más ayuda y soporte técnico, vea [Solucionar problemas de Endpoint Protection en Microsoft Intune](../Topic/Troubleshoot-Endpoint-Protection-in-Microsoft-Intune.md).

## Vea también
[Administrar equipos Windows con Microsoft Intune](../Topic/Manage-Windows-PCs-with-Microsoft-Intune.md)

