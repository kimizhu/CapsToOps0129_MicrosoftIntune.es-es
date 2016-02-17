---
title: Recursos para ayudarle a solucionar problemas durante la instalaci&#243;n de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6865f1fb-c2c1-47af-83f5-5704e7210a49
robots: noindex,nofollow
---
# Recursos para ayudarle a solucionar problemas durante la instalaci&#243;n de Microsoft Intune
Como [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] es un servicio en la nube, debería haber poca necesidad de reparar o solucionar problemas de funcionamiento. Si tuviera problemas de acceso al servicio, las secciones siguientes pueden ayudarle a identificar los pasos que debe seguir.

## <a name="BKMK_ResolveSetupProblems"></a>Sugerencias para solucionar problemas de instalación y configuración de Microsoft Intune
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] no genera registros de instalación u operaciones que se puedan utilizar para solucionar problemas.

Las acciones administrativas se efectúan mediante un explorador web para conectarse al servicio en la nube. Los problemas para acceder al servicio suelen deberse a una de las siguientes causas:

|Problema|Detalles|
|------------|------------|
|Permisos insuficientes para el [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)]|Para utilizar el [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)] para administrar más elementos además de su propio perfil de usuario, su cuenta debe:<br /><br />-   tener una licencia para utilizar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]<br />-   tener un estado de inicio de sesión de **Permitido** para iniciar sesión<br />-   debe ser un administrador de inquilinos del [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)]<br /><br />Para obtener información, consulte [Cuentas de administrador de Intune y permisos especiales](../Topic/What-to-know-before-setting-up-Microsoft-Intune.md#BKMK_AdminAccounts).|
|Acceso de red que incluye:<br /><br />-   Dominios utilizados por [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]<br />-   Tráfico en la red<br />-   Compatibilidad con exploradores web|Para conectarse a [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], debe:<br /><br />-   utilizar un explorador web compatible<br />-   tener acceso en la red a través de los firewalls y los servidores proxy a los distintos dominios que utiliza el servicio de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].<br /><br />Para obtener información acerca de los requisitos y las configuraciones necesarios para utilizar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte:<br /><br />-   [Infrastructure requirements](../Topic/Network-infrastructure-requirements-for-Microsoft-Intune.md#BKMK_InfrastructureReqs)<br />-   [Web browsers supported by Microsoft Intune](../Topic/Network-infrastructure-requirements-for-Microsoft-Intune.md#BKMK_SupportedBrowsers)|
|Disponibilidad del servicio de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|Para ver los detalles en línea o suscribirse a fuentes RSS sobre el estado del servicio [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte:<br /><br />-   [Servicio Microsoft Intune](http://status.manage.microsoft.com/)|

## Vea también
[Introducción a Microsoft Intune](../Topic/Introduction-to-Microsoft-Intune.md)

