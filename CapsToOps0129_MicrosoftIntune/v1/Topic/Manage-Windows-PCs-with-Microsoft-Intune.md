---
title: Administrar equipos Windows con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b8d22fe-c318-4796-b760-44f1ccf34312
---
# Administrar equipos Windows con Microsoft Intune
Además de administrar dispositivos móviles, también puede utilizar [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] para administrar equipos que ejecutan sistemas operativos compatibles a través del software cliente de equipo de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Los [requisitos de hardware y software](https://technet.microsoft.com/library/dn646975.aspx) para ejecutar el equipo cliente son mínimos, básicamente, se admite cualquier sistema capaz de ejecutar Windows Vista o posterior.  El software cliente también puede instalarse fácilmente en equipos unidos a un dominio (en cualquier dominio) o no unidos a un dominio.

[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] administra equipos mediante directivas, del mismo modo que los objetos de directiva de grupo (GPO) de Los Servicios de dominio de Active Directory (AD DS) de Windows Server. Si va a administrar equipos unidos a un dominio de Active Directory con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], debería [asegurarse de que las directivas de Intune no entran en conflicto con ningún GPO](https://technet.microsoft.com/library/dn646986.aspx) configurado para la organización.

> [!NOTE]
> Microsoft Intune, como servicio independiente, ofrece las siguientes funciones de administración de equipos. Los dispositivos que ejecutan Windows 8.1 se pueden administrar mediante el cliente de Intune o se pueden inscribir como dispositivos móviles. La siguiente información se aplica a equipos que ejecutan el cliente de Intune. Para obtener información acerca de las funciones de administración de dispositivos móviles, consulte [Capacidades de administración de dispositivos móviles en Microsoft Intune](https://technet.microsoft.com/library/dn600287(TechNet.10).aspx).

## Instalar el cliente de equipo de Intune
El primer paso en la administración de equipos con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] consiste en instalar el cliente. El software cliente se puede instalar cuando un equipo está inscrito en la administración por parte del servicio [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] de una de las maneras siguientes:

-   Puede [implementar manualmente el software cliente de Microsoft Intune](https://technet.microsoft.com/library/dn646969.aspx#BKMK_Manual). En este tipo de implementación, un administrador descarga el software de cliente de Intune y lo instala manualmente en cada equipo.

    Para descargar el software de cliente de Intune, abra la consola de administración de Intune y, en el área de descarga de software de cliente, descargue el paquete de software cliente. Después de instalar el software cliente, Intune instala automáticamente software adicional según sea necesario para administrar el equipo.

-   Puede usar los mismos archivos que descargó para instalar manualmente el cliente de Intune para [implementar el cliente en equipos unidos a un dominio mediante GPO de Active Directory](https://technet.microsoft.com/library/dn646969.aspx).

-   [Los usuarios finales pueden inscribir por sí mismos cada uno de sus equipos](https://technet.microsoft.com/library/dn646969.aspx) a través del Portal de empresa de Intune. Cada equipo inscrito, a continuación, se vincula automáticamente a la cuenta de usuario que se utilizó para instalar el software cliente de Intune.

-   Por último, también puede implementar el software cliente de Intune en equipos como parte de una [implementación de sistema operativo](https://technet.microsoft.com/library/dn646969.aspx).

## Administración de equipos con el cliente de equipos de Intune
Después de instalar el cliente de Intune, el software cliente habilita varias funciones de administración de equipo, por ejemplo: [administración de aplicaciones](https://technet.microsoft.com/library/dn646961.aspx), Endpoint Protection, inventario de hardware y software, control remoto (a través de solicitudes de asistencia remota), actualizaciones de software e informes de configuración de cumplimiento.

Varias tareas de administración de equipos habilitadas por el cliente de equipos se administran mediante directivas de Intune, como:

-   Configurar los [parámetros del Firewall de Windows](https://technet.microsoft.com/library/mt346040.aspx) en los equipos administrados.

-   Configurar [parámetros de actualización de software](https://technet.microsoft.com/library/dn646968.aspx) para que los equipos administrados busquen y descarguen actualizaciones de software necesarias.

-   Contribuir a proteger equipos administrados de posibles amenazas y software malintencionado a través de la administración de [Endpoint Protection y la supervisión en tiempo real](https://technet.microsoft.com/library/dn646970.aspx).

Además de las acciones de agente de cliente de Intune realizadas localmente en equipos individuales, también puede utilizar la consola de administración de Intune para realizar otras [tareas comunes de administración de equipos](https://technet.microsoft.com/library/dn646989.aspx) en equipos con el cliente instalado para:

-   Ver información de inventario de hardware y software sobre los equipos administrados

-   Reiniciar un equipo de forma remota

-   Retirar un equipo para desinstalar el software cliente y quitarlo de la administración con Intune

-   Vincular usuarios a determinados equipos administrados

-   Responder a solicitudes de asistencia remota

El agente cliente de Intune, normalmente, se ejecuta silenciosamente en segundo plano sin necesidad de mucha interacción con el usuario o de solucionar problemas. Sin embargo, si necesita ayuda para resolver problemas de administración de equipos, hay varios [recursos disponibles para ayudarle a solucionarlos](https://technet.microsoft.com/library/dn646987.aspx).

## Vea también
[Configurar y administrar dispositivos con Microsoft Intune](../Topic/Configure-and-manage-devices-with-Microsoft-Intune.md)

