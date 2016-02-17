---
title: Directivas de administraci&#243;n de aplicaciones m&#243;viles de Microsoft Intune y caracter&#237;stica Open In de iOS
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a4515c1-b325-4ac1-9f0a-45ac27e00681
---
# Directivas de administraci&#243;n de aplicaciones m&#243;viles de Microsoft Intune y caracter&#237;stica Open In de iOS
La característica de **administración Open In** para dispositivos iOS permite controlar el flujo de datos entre aplicaciones. Las restricciones de administración de Open In se establecen en los valores del perfil de configuración y se implementan con el software MDM.  Cuando el usuario instala la aplicación administrada, se aplican las restricciones.

Las directivas de administración de aplicaciones móviles (MAM) funcionan con la **administración Open In** para proteger los datos de la empresa en dispositivos, como se describe más abajo:

-   **Dispositivos BYOD no administrados por una solución MDM:** puede establecer la configuración de directiva MAM en **Permitir a la aplicación transferir datos solo a aplicaciones administradas**. Cuando el usuario final abre un archivo protegido en una aplicación no administrada, el archivo es ilegible.

-   **Dispositivos administrados por Intune o una solución MDM de terceros:** para proteger los datos de la empresa como se ha descrito más arriba solo tiene que permitir la transferencia de datos a aplicaciones administradas. También puede controlar la lista de aplicaciones a través de su proveedor MDM.   Para dispositivos inscritos y administrados mediante Intune, lea el tema [Preparar aplicaciones iOS para la administración de aplicaciones móviles con la herramienta de ajuste de aplicaciones de Microsoft Intune](../Topic/Prepare-iOS-apps-for-mobile-application-management-with-the-Microsoft-Intune-App-Wrapping-Tool.md) para más información.

## Vea también
[Configurar directivas de aplicaciones de prevención de pérdida de datos con Microsoft Intune](../Topic/Configure-data-loss-prevention-app-policies-with-Microsoft-Intune.md)

