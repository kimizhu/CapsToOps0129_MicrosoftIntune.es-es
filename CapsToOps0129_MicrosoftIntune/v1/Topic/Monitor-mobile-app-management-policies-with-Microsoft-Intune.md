---
title: Supervisi&#243;n de directivas de administraci&#243;n de aplicaciones m&#243;viles con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d3aa6c74-6b5d-4b50-aa66-a040ec44393e
---
# Supervisi&#243;n de directivas de administraci&#243;n de aplicaciones m&#243;viles con Microsoft Intune
Use la información de este tema para ayudarle a supervisar las directivas de administración de aplicaciones móviles en el portal de vista previa de Azure.

### Supervisión del cumplimiento de directivas de administración de aplicaciones móviles
El icono **Estado del usuario** de la hoja **Administración de aplicaciones móviles de Intune** muestra el estado de cumplimiento de las directivas de aplicación del modo descrito a continuación:

![](../Image/AppManagement/AzurePortal_MAM_MonitorUsers.png)

-   **Usuarios**: número total de usuarios de su compañía que usan aplicaciones de trabajo en sus dispositivos.

-   **DIRECTIVA**: número de usuarios que han usado al menos una de las aplicaciones asociadas con la directiva.

-   **SIN DIRECTIVA**: número de usuarios que están usando activamente aplicaciones de trabajo pero que no están protegidos por la directiva de administración de aplicaciones móviles.

    El icono **Usuarios marcados** le ofrece la información agregada sobre cuántos usuarios están experimentando problemas. Actualmente, solo los usuarios con dispositivos liberados aparecen como marcados.

    ![](../Image/AppManagement/AzurePortal_MAM_FlaggedUserDetails.png)

-   El icono **Solicitudes de borrado** muestra el informe de resumen del estado de las solicitudes de borrado realizadas. Al hacer clic en este icono, se abrirá una nueva hoja con más información detallada. Para obtener una descripción detallada de la información de solicitudes de borrado que se muestra en esta hoja, lea el tema [Borrar los datos administrados de la aplicación de la empresa con Microsoft Intune](../Topic/Wipe-managed-company-app-data-with-Microsoft-Intune.md).

    ![](../Image/AppManagement/AzurePortal_MAM_WipeRequestsSummary.png)

## Vea también
[Crear e implementar directivas de administración de aplicaciones móviles con Microsoft Intune](../Topic/Create-and-deploy-mobile-app-management-policies-with-Microsoft-Intune.md)
[Configurar directivas de aplicaciones de prevención de pérdida de datos con Microsoft Intune](../Topic/Configure-data-loss-prevention-app-policies-with-Microsoft-Intune.md)

