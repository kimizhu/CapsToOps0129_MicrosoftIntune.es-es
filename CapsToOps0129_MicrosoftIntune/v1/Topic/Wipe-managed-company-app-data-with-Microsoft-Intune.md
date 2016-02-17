---
title: Borrar los datos administrados de la aplicaci&#243;n de la empresa con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2742e1d5-d2d5-42cd-b719-665dd6e0a0e9
---
# Borrar los datos administrados de la aplicaci&#243;n de la empresa con Microsoft Intune
Puede quitar datos específicos de la empresa desde las aplicaciones, sin tener que tocar los datos personales que se encuentren en un dispositivo.  Para borrar los datos de la aplicación de la empresa, debe realizar una solicitud de borrado.  Una vez hecha, la próxima vez que ejecute la aplicación en el dispositivo, los datos de la empresa se quitarán de la aplicación.

El icono **Solicitud de borrado** que se encuentra en la hoja **Administración de aplicaciones móviles de Intune** muestra el número de solicitudes pendientes y de errores.

> [!IMPORTANT]
> En la versión actual, aplicaciones como Microsoft Word, Excel y PowerPoint no tienen la capacidad de borrado selectivo.

**En este tema**

[Realizar una solicitud de borrado de datos](#bkmk_makerequest)

[Supervisar las solicitudes de borrado de datos](#bkmk_monitorrequest)

#### <a name="bkmk_makerequest"></a>Realizar una solicitud de borrado de datos

1.  En la hoja **Administración de aplicaciones móviles de Intune** , haga clic en el icono **Borrar solicitudes**.

    ![](../Image/AppManagement/AzurePortal_MAM_WipeRequests.png)

2.  Haga clic en **Nueva solicitud de borrado**.

    ![](../Image/AppManagement/AzurePortal_MAM_NewWipeRequest.png)

3.  En la hoja **Nueva solicitud de borrado**, haga clic en **Usuario** para abrir la hoja **Usuario** y seleccione el usuario cuyos datos de aplicación desea borrar.

4.  Haga clic en **Dispositivo**.  Se abrirá la hoja **Dispositivo** que enumera todos los dispositivos asociados con el usuario seleccionado.  Seleccione el dispositivo que desea borrar.

5.  Volverá a la hoja **Nueva solicitud de borrado**. Haga clic en **Aceptar** para realizar una solicitud de borrado. El servicio crea y realiza el seguimiento de una solicitud de borrado de datos independiente para cada aplicación protegida en el dispositivo.

En la hoja **Administración de aplicaciones móviles de Intune** , encontrará un informe resumido en el icono **Borrar solicitudes**.  Esta opción muestra el estado general e incluye el número de solicitudes pendientes y de errores. Puede obtener más detalles si hace clic en el icono, el cual abrirá la hoja **Solicitud de borrado**.

![](../Image/AppManagement/AzurePortal_MAM_WipeRequestsSummary.png)

#### <a name="bkmk_monitorrequest"></a>Supervisar las solicitudes de borrado de datos

1.  En la hoja **Administración de aplicaciones móviles de Intune** , haga clic en el icono **Borrar solicitudes** para abrir la hoja **Solicitud de borrado**.

2.  En la hoja **Solicitud de borrado**, puede ver la lista de solicitudes agrupadas según usuarios.  Debido a que el sistema crea una solicitud de borrado para cada aplicación protegida que se ejecuta en el dispositivo, puede que vea varias solicitudes para un mismo usuario.  Este estado indica si una solicitud de borrado está **pendiente**, ha provocado un **error** o si es **correcta**.

## Vea también
[Configurar directivas de aplicaciones de prevención de pérdida de datos con Microsoft Intune](../Topic/Configure-data-loss-prevention-app-policies-with-Microsoft-Intune.md)

