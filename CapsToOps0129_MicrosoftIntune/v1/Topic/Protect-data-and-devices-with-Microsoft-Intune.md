---
title: Proteger datos y dispositivos con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 71e0cbf3-2bfb-412e-8a12-8503df08b4cf
---
# Proteger datos y dispositivos con Microsoft Intune
![](../Image/Nav-Icons/WIT_Tile_W_Overview.png)![](../Image/Nav-Icons/WIT_Tile_W_GetStarted.png)![](../Image/Nav-Icons/WIT_Tile_W_EnrollDevices.png)![](../Image/Nav-Icons/WIT_Tile_W_ManageDevices.png)![](../Image/Nav-Icons/WIT_Tile_W_ManageApps.png)![](../Image/Nav-Icons/WIT_Tile_W_ProtectResourcesHighlight.png)![](../Image/Nav-Icons/WIT_Tile_W_RetireData.png)![](../Image/Nav-Icons/WIT_Tile_W_TechnicalReference.png)![](../Image/Nav-Icons/WIT_Tile_W_Troubleshooting.png)
![](../Image/Nav-Icons/WIT_Banner_ProtectResources.png)

Una vez que aprovisionados y configurados los dispositivos, querrá asegurarse de que están *protegidos contra la pérdida de datos* y otras amenazas. Aquí se presentan escenarios comunes de los usuarios en los que la red y los datos pueden estar en peligro, y los métodos de los que dispone para protegerlos.

## Protección de datos del correo electrónico y SharePoint
Lo primero que desean recibir los empleados en sus dispositivos es el correo electrónico.  Dado que el correo electrónico a menudo contiene datos críticos de la empresa, querrá asegurarse de que el dispositivo está seguro. Por ejemplo, si el dispositivo no está protegido mediante un código de acceso, y lo roban, el ladrón podrá leer todo el correo electrónico de la empresa en el dispositivo.

[Administre el acceso al correo electrónico y proteja los datos corporativos en SharePoint Online ](https://technet.microsoft.com/library/dn818907.aspx) con las capacidades de Intune para establecer directivas de acceso, como la obligación de un *código de acceso* o un *cifrado de datos*.   También puede denegar el acceso si el dispositivo se *descodificó o descifró*.

Microsoft ofrece Enterprise Mobility Suite (EMS), una solución completa para la administración de identidades, dispositivos móviles y aplicaciones, así como para la protección de datos. EMS proporciona un modelo de seguridad por capas que permite al departamento de TI administrar el acceso al correo electrónico, datos y aplicaciones corporativas desde casi cualquier dispositivo. En el tema [Proteger documentos y correo electrónico corporativos](../Topic/Architecture-guidance-for-protecting-company-email-and-documents.md) se describen la solución general y las capacidades [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en detalle. El tema [Aprenda a implementar una solución para proteger los documentos y correos electrónicos de su empresa](../Topic/Learn-how-to-deploy-a-solution-for-protecting-company-email-and-documents.md) contiene instrucciones paso a paso sobre cómo implementar la solución.

## Capa adicional de protección con autenticación multifactor
[La autenticación multifactor (MFA)](https://technet.microsoft.com/library/dn889751.aspx) es una forma más segura de autenticar a los usuarios de dispositivos Windows y Windows Phone en la red.  Con MFA, los usuarios deben confirmar su identidad, más allá del nombre de usuario y la contraseña, a través de una llamada de teléfono o un mensaje de texto.

## Vea también
[Documentación de Microsoft Intune](../Topic/Documentation-for-Microsoft-Intune.md)

