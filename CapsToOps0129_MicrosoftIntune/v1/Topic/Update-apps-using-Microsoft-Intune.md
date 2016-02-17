---
title: Actualizar aplicaciones con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: beee6933-876a-4be0-b395-4c24cfbd519b
---
# Actualizar aplicaciones con Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] puede ayudarle a administrar actualizaciones de aplicaciones. Use la información de este tema para entender cómo actualizar aplicaciones cuando se requiere una versión nueva.

## Actualizar aplicaciones
Cuando se lanza una nueva versión de una aplicación que haya implementado, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] permite actualizar e implementar la versión más reciente de la aplicación. Una implementación solo se puede reemplazar por una versión más reciente de la misma aplicación (con el mismo identificador). No se pueden usar las actualizaciones de aplicaciones para actualizar una implementación con un paquete de la aplicación diferente.

> [!IMPORTANT]
> Si implementa una aplicación con la acción de implementación **Instalación requerida** y posteriormente cambia la acción de implementación a **Instalación disponible**, las actualizaciones de la aplicación no se instalan automáticamente en los dispositivos que instalaron la aplicación antes de que se realizara el cambio de implementación. Para corregir este problema, puede hacer lo siguiente:
> 
> -   Indique al usuario del dispositivo que vaya al portal de empresa, seleccione la aplicación instalada y haga clic en **Instalar**.
> -   Cambie la acción de implementación a **Desinstalar** y, una vez desinstalada la aplicación, vuelva a implementar la aplicación con la acción de implementación **Instalación disponible**.

#### Para actualizar una aplicación

1.  En la [consola de administrador de Microsoft Intune](https://account.manage.microsoft.com/admin/default.aspx), haga clic en **Aplicaciones** &gt; **Aplicaciones**.

2.  En la lista **Aplicaciones**, seleccione la aplicación que quiera actualizar y, a continuación, haga clic en **Editar**.

3.  En el asistente **Editar software**, proporcione los detalles nuevos del paquete de la aplicación.

4.  Cuando haya terminado haga clic en **Actualizar**.

Cuando los dispositivos comprueben posteriormente si hay aplicaciones disponibles, la aplicación se actualizará automáticamente a la última versión.

## Vea también
[Implementar y configurar aplicaciones con Microsoft Intune](../Topic/Deploy-and-configure-apps-with-Microsoft-Intune.md)
[Retirar aplicaciones mediante Microsoft Intune](../Topic/Retire-apps-using-Microsoft-Intune.md)

