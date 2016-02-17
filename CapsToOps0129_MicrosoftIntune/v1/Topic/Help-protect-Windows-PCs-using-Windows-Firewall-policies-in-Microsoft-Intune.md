---
title: Ayudar a proteger los equipos de Windows mediante directivas del Firewall de Windows en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 62c44f36-d866-439e-8553-948cc0ea2504
---
# Ayudar a proteger los equipos de Windows mediante directivas del Firewall de Windows en Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] puede ayudar a proteger los equipos administrados de varias maneras, incluido el uso de directivas que le permiten ajustar la configuración del Firewall de Windows en los equipos cliente.

Si aún no ha instalado el cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en los equipos, vea [Instalar al cliente de equipos Windows con Microsoft Intune](../Topic/Install-the-Windows-PC-client-with-Microsoft-Intune.md).

Use la información de las siguientes secciones como ayuda para configurar, implementar y supervisar las directivas del Firewall de Windows en equipos cliente.

## <a name="BKMK_Firewall"></a>Usar directivas de Microsoft Intune para administrar el Firewall de Windows
La directiva de Firewall de Windows le permite crear e implementar la configuración que controla el Firewall de Windows en los equipos administrados. No se puede administrar excepciones personalizadas para Firewall de Windows y esta configuración no afecta a ningún firewall que no sea de Microsoft.

> [!NOTE]
> Si la directiva de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] y la directiva de grupo se configuran para administrar la misma configuración en el equipo, la configuración de la directiva de grupo invalidará la directiva de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Para obtener información acerca de cómo evitar conflictos entre las directivas de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] y la directiva de grupo, consulte [Resolver conflictos de directivas de Microsoft Intune y GPO](../Topic/Resolve-GPO-and-Microsoft-Intune-policy-conflicts.md).
> 
> Si quiere implementar la configuración de Firewall de Windows en equipos que ejecutan Windows Vista, primero debe instalar la [revisión KB971800](http://support2.microsoft.com/kb/971800) en estos equipos.

> [!IMPORTANT]
> Para administrar el firewall de Windows mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], debe asegurarse de que los dos servicios siguientes están habilitados en los equipos que va a administrar:
> 
> -   Firewall de Windows
> -   Agente de directivas IPsec

#### Para configurar una directiva de Firewall de Windows

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com/), haga clic en **Directiva** &gt; **Agregar directiva**.

2.  Configurar e implementar una directiva de **Configuración de Firewall de Windows**. Puede usar la configuración recomendada o personalizar la configuración. Si necesita más información acerca de cómo crear e implementar directivas, consulte el tema [Tareas comunes de administración de PC Windows con el cliente de equipo de Microsoft Intune](../Topic/Common-Windows-PC-management-tasks-with-the-Microsoft-Intune-computer-client.md).

    Las tablas de después de este procedimiento muestran los valores que puede configurar en la directiva y también los valores recomendados que se utilizarán si no se personaliza la directiva.

Puede ver la directiva de Firewall de Windows implementada en la página **Todas las directivas** del área de trabajo **Directiva**.

### Configuración de directiva para Firewall de Windows

#### Activar Firewall de Windows

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Perfil de dominio**|Habilita el Firewall de Windows en los equipos administrados mientras estén conectados a redes de dominio, como en el lugar de trabajo.<br /><br />Valor recomendado: **Sí**|
|**Perfil privado**|Habilita el Firewall de Windows en los equipos administrados mientras estén conectados a redes de confianza, como una red doméstica.<br /><br />Valor recomendado: **Sí**|
|**Perfil público**|Habilita el Firewall de Windows en los equipos administrados mientras estén conectados a redes que no son de confianza en lugares públicos, como en una cafetería.<br /><br />Valor recomendado: **Sí**<br /><br />Sistema operativo necesario: [!INCLUDE[firstref_vista](../Token/firstref_vista_md.md)] o versiones posteriores|

#### Bloquear todas las conexiones entrantes, incluidas las de la lista de programas permitidos.
> [!IMPORTANT]
> Si su entorno incluye equipos administrados que ejecutan Windows Vista sin ningún Service Pack instalado, debe instalar la actualización asociada con el [artículo 971800](http://go.microsoft.com/fwlink/?LinkId=188405) en Microsoft Knowledge Base, o bien deshabilitar la configuración de directiva **Bloquear todas las conexiones entrantes** en las directivas implementadas en dichos equipos.

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Perfil de dominio**|Bloquea todas las conexiones entrantes mientras los equipos estén conectados a redes de dominio, como en el lugar de trabajo. Se incluyen las conexiones de la lista de excepciones.<br /><br />Valor recomendado: **No**|
|**Perfil privado**|Bloquea todas las conexiones entrantes mientras los equipos estén conectados a redes domésticas, como una red doméstica. Se incluyen las conexiones de la lista de excepciones.<br /><br />Valor recomendado: **No**|
|**Perfil público**|Bloquea todas las conexiones entrantes mientras los equipos estén conectados a redes que no son de confianza en lugares públicos, como una cafetería. Se incluyen las conexiones de la lista de excepciones.<br /><br />Valor recomendado: **No**<br /><br />Sistema operativo necesario: [!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o versiones posteriores|

#### Notificar al usuario cuando Firewall de Windows bloquee un nuevo programa

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**Perfil de dominio**|Notifica a los usuarios cuándo Firewall de Windows bloquea un programa nuevo mientras los equipos estén conectados a redes de dominios, como un lugar de trabajo.<br /><br />Valor recomendado: **Sí**|
|**Perfil privado**|Notifica a los usuarios cuándo Firewall de Windows bloquea un programa nuevo mientras los equipos estén conectados a redes de confianza, como una red doméstica.<br /><br />Valor recomendado: **Sí**|
|**Perfil público**|Notifica a los usuarios cuándo Firewall de Windows bloquea un programa nuevo mientras los equipos estén conectados a redes que no son de confianza en lugares públicos, como una cafetería.<br /><br />Valor recomendado: **Sí**<br /><br />Sistema operativo necesario: [!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o versiones posteriores|

#### Excepciones predefinidas

|Configuración de directiva|Más información|
|------------------------------|-------------------|
|**BranchCache: recuperación de contenido**|Si está habilitada, permite a los clientes de BranchCache usar HTTP para recuperar contenido de otros en el modo distribuido y desde la caché hospedada en el modo de caché hospedada. Esta configuración usa HTTP.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[firstref_client_7](../Token/firstref_client_7_md.md)] o posterior).|
|**BranchCache: cliente de caché hospedada**|Si está habilitada, permite a los clientes de BranchCache usar una caché hospedada. Esta configuración usa HTTPS.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)] o posterior).|
|**BranchCache: servidor de caché hospedada**|Si está habilitada, permite a los clientes de BranchCache usar una caché hospedada para comunicarse con otros clientes. Esta configuración usa HTTPS.<br /><br />Valor recomendado: no configurado<br /><br />([!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)] o posterior).|
|**BranchCache: detección de pares**|Si está habilitada, permite a los clientes de BranchCache usar el protocolo de detección WS para comprobar la disponibilidad del contenido en la subred local.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)] o posterior).|
|**Caché del mismo nivel de BITS**|Si está habilitada, permite a los clientes usar Servicio de transferencia inteligente en segundo plano (BITS) para buscar y compartir archivos que se almacenan en la caché de BITS de clientes de la misma subred. Esta configuración usa WSDAPI y RPC.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Conectarse a un proyector de red**|Si está habilitada, permite a los usuarios conectarse a proyectores a través de redes cableadas o inalámbricas para poder mostrar una presentación. Esta configuración usa WSDAPI.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Redes principales**|Si está habilitada, permite a los clientes usar IPv4 e IPv6 para conectarse a recursos de red.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Coordinador de transacciones distribuidas**|Si está habilitada, permite a los equipos administrados coordinar las transacciones que actualizan los recursos protegidos contra transacciones, como, por ejemplo, las bases de datos, las colas de mensajes y los sistemas de archivos.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Compartir archivos e impresoras**|Si está habilitada, permite a los usuarios compartir archivos e impresoras locales con otros usuarios de la red. Esta configuración utiliza NetBIOS, LLMNR, SMB y RPC.<br /><br />Valor recomendado: No configurado<br /><br />(Windows XP o posterior)|
|**Grupo Hogar**|Si está habilitada, permite a los equipos administrados participar en una red Grupo Hogar.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)] o posterior).|
|**Servicio iSCSI**|Si está habilitada, permite los equipos administrados conectarse a servidores y dispositivos iSCSI.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Servicio de administración de claves**|Si está habilitada, permite el recuento de equipos para el cumplimiento de licencias en entornos de empresa.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Media Center Extenders**|Si está habilitada, permite que los Media Center Extender se comuniquen con un equipo que ejecuta Windows Media Center. Esta configuración usa SSDP y qWave.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Servicio de Net Logon**|Si está habilitada, configura un canal de seguridad entre clientes del dominio y un controlador de dominio para la autenticación de usuarios y servicios. Esta configuración usa RPC.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Detección de redes**|Si está habilitada, permite a los equipos detectar otros dispositivos y ser detectados por otros dispositivos en la red. Esta configuración usa Host de detección de funciones y Servicios de publicación, así como los protocolos de red SSDP, NetBIOS, LLMNR y UPnP.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Registros y alertas de rendimiento**|Si está habilitada, permite la administración remota del servicio Registros y alertas de rendimiento. Esta configuración usa RPC.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Administración remota**|Si está habilitada, permite la administración remota del equipo.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Asistencia remota**|Si está habilitada, permite a los usuarios de equipos administrados solicitar asistencia remota desde otros usuarios de la red. Esta configuración usa los protocolos de red SSDP, PNRP, Teredo y UPnP.<br /><br />Valor recomendado: No configurado<br /><br />(Windows XP o posterior)|
|**Escritorio remoto**|Si está habilitada, permite al equipo usar Escritorio remoto para tener acceso a otros equipos.<br /><br />Valor recomendado: No configurado<br /><br />(Windows XP o posterior)|
|**Administración remota de registro de eventos**|Si está habilitada, permite ver y administrar de forma remota el registro de eventos del cliente. Esta configuración usa Canalizaciones con nombre y RPC.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Administración remota de tareas programadas**|Si está habilitada, permite la administración remota del servicio de programación de tareas. Esta configuración usa RPC.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Administración remota de servicios**|Si está habilitada, permite la administración remota de los servicios locales en los clientes. Esta configuración usa Canalizaciones con nombre y RPC.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Administración remota del volumen**|Si está habilitada, permite la administración remota de volúmenes de disco de software y de hardware. Esta configuración usa RPC.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Enrutamiento y acceso remoto**|Si está habilitada, permite conexiones VPN y de acceso remoto entrantes a los equipos.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Protocolo de túnel de sockets seguros**|Si está habilitada, permite las conexiones VPN entrantes a los equipos administrados mediante el empleo del protocolo de túnel de sockets seguros (SSTP). Esta configuración usa HTTPS.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Captura de SNMP**|Si está habilitada, permite a los equipos administrados recibir tráfico del servicio Captura de SNMP.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Entorno UPnP**|Si está habilitada, configura el servicio Entorno UPnP en los equipos para permitirles detectar o utilizar dispositivos UPnP certificados.<br /><br />Valor recomendado: No configurado<br /><br />(Windows XP o posterior)|
|**Servicio de registro de nombres de equipo de Windows Collaboration**|Si está habilitada, permite a los equipos buscar y comunicarse con otros equipos mediante el Protocolo de resolución de nombres de mismo nivel (PRNP). Esta configuración usa SSDP y PNRP.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Reproductor de Windows Media**|Si está habilitada, permite a los usuarios recibir archivos multimedia de transmisión por secuencias sobre UDP.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Servicio de uso compartido de red del Reproductor de Windows Media**|Si está habilitada, permite a los usuarios compartir archivos multimedia a través de una red. Esta configuración usa los protocolos de red SSDP, qWave y UPnP.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Servicio de uso compartido de red del Reproductor de Windows Media (Internet)**|Si está habilitada, permite a los usuarios compartir archivos multimedia domésticos a través de Internet.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)] o posterior).|
|**Área de encuentro de Windows**|Si está habilitada, permite a los usuarios colaborar a través de una red para compartir con otras personas documentos, programas o el escritorio. Esta configuración usa DFSR y P2P.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Windows Peer to Peer Collaboration Foundation**|Si está habilitada, configura varios programas y tecnologías punto a punto para que puedan conectarse. Esta configuración usa SSDP y PNRP.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Administración remota de Windows (Compatibilidad)**|Si está habilitada, permite la administración remota de equipos administrados mediante el empleo de WS-Management, un protocolo basado en servicios Web para la administración remota de sistemas operativos y dispositivos.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|
|**Administración remota de Windows**|Si está habilitada, permite la administración remota de equipos administrados mediante el empleo de WS-Management, un protocolo basado en servicios Web para la administración remota de sistemas operativos y dispositivos.<br /><br />Valor recomendado: No configurado<br /><br />(Windows 8 o posterior)|
|**Windows Virtual PC**|Si está habilitada, permite a las máquinas virtuales comunicarse con otros equipos.<br /><br />Valor recomendado: No configurado<br /><br />(solo [!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)])|
|**Dispositivos portátiles inalámbricos**|Si está habilitada, permite la transferencia de archivos multimedia a equipos administrados desde cualquier cámara o dispositivo multimedia que se pueda conectar a la red, por medio del Protocolo de transferencia multimedia (MTP). Esta configuración usa los protocolos de red SSDP y UPnP.<br /><br />Valor recomendado: No configurado<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] o posterior).|

## Vea también
[Administrar equipos Windows con Microsoft Intune](../Topic/Manage-Windows-PCs-with-Microsoft-Intune.md)

