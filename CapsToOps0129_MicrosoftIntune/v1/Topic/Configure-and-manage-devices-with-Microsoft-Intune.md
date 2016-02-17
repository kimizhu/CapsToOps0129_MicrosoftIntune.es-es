---
title: Configurar y administrar dispositivos con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7b938d95-c068-4d71-a580-c1492c4bff27
---
# Configurar y administrar dispositivos con Microsoft Intune
[![](../Image/Nav-Icons/WIT_Tile_W_Overview.png)](https://technet.microsoft.com/library/dn646960.aspx/?WT.mc_id=IntuneOverview20150801)[![](../Image/Nav-Icons/WIT_Tile_W_GetStarted.png)](https://technet.microsoft.com/library/dn646953.aspx/?WT.mc_id=IntuneGS20150801)[![](../Image/Nav-Icons/WIT_Tile_W_EnrollDevices.png)](https://technet.microsoft.com/library/dn646962.aspx/?WT.mc_id=IntuneEnroll20150801)![](../Image/Nav-Icons/WIT_Tile_W_ManageDevicesHighlight.png)[![](../Image/Nav-Icons/WIT_Tile_W_ManageApps.png)](https://technet.microsoft.com/library/dn646965.aspx/?WT.mc_id=IntuneDeploy20150801)[![](../Image/Nav-Icons/WIT_Tile_W_ProtectResources.png)](https://technet.microsoft.com/library/mt313203.aspx/?WT.mc_id=IntuneProtect20150801)[![](../Image/Nav-Icons/WIT_Tile_W_RetireData.png)](https://technet.microsoft.com/library/mt313204.aspx/?WT.mc_id=IntuneRetire20150801)[![](../Image/Nav-Icons/WIT_Tile_W_TechnicalReference.png)](https://technet.microsoft.com/library/mt282239.aspx/?WT.mc_id=IntuneTR20150801)[![](../Image/Nav-Icons/WIT_Tile_W_Troubleshooting.png)](https://technet.microsoft.com/library/mt345521.aspx)
![](../Image/Nav-Icons/WIT_Banner_ManageDevices.png)

Use perfiles de VPN, perfiles de WiFi y directivas de configuración para ofrecer a los empleados acceso a la red mientras cumple los requisitos de seguridad de su empresa.

Los usuarios quieren recibir su correo electrónico y tener acceso a su trabajo en varios dispositivos diferentes, y desean disfrutar de esa libertad donde sea que estén. Esto le brinda oportunidades de aumentar la productividad, pero también presenta ciertos problemas en torno a la seguridad de los datos de su compañía.

[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] puede resolver estos problemas con los perfiles de VPN, los perfiles de WiFi y las directivas de configuración.

## Usar perfiles de VPN o perfiles de WiFi para habilitar el acceso a recursos de la empresa
Mediante los [perfiles de acceso de los recursos](https://technet.microsoft.com/library/dn997277.aspx), puede hacer que sea fácil para los empleados recibir correo electrónico o usar Wi-Fi o VPN para obtener acceso a los recursos de la empresa. Estos perfiles permiten realizar una configuración previa de los dispositivos con los ajustes de acceso que necesitan para el correo electrónico y los archivos de la empresa. Por ejemplo, muchas personas usan la conexión de red privada virtual (VPN) para trabajar de forma remota. La configuración para crear una conexión VPN (o **perfil**) es compleja y puede que un usuario final típico no la entienda.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] permite realizar una configuración previa de estos valores para implementarlos en los dispositivos de los usuarios. Esto significa que los empleados no tienen que especificar los ajustes complejos de VPN, sino simplemente seleccionar el perfil de VPN de una lista y conectarse automáticamente. Además, puede aprovechar las capacidades de seguridad de los certificados para proteger estas conexiones.

## Administrar la configuración y características con directivas de Intune
Imagine que es el administrador de TI de una empresa de diseño. Está trabajando en un nuevo producto y no desea que los detalles del producto se filtren al público. Para mayor seguridad, desea deshabilitar el uso de la cámara en los dispositivos móviles de los empleados.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] le permite usar una **directiva de configuración** para lograr este objetivo fácilmente.

Aunque [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] proporciona [una amplia gama de opciones de configuración](https://technet.microsoft.com/library/dn646984.aspx) para configurar los dispositivos, podría haber casos en los que la configuración que necesita no está disponible. En muchos casos, puede resolver este problema mediante una directiva personalizada que le permite ajustar la configuración OMA-URI, un estándar común para configurar dispositivos móviles a fin de establecer los valores necesarios.

## Administrar equipos
Aunque puede [inscribir los equipos que ejecutan Windows 8.1 y versiones posteriores](https://technet.microsoft.com/library/dn764959.aspx) como dispositivos móviles, en algunos casos quizás quiera administrarlos instalando el cliente de equipo de Intune en ellos. La [administración de equipos con Intune](https://technet.microsoft.com/library/dn646959.aspx) le proporciona algunas opciones que no están disponibles cuando los equipos se administran como dispositivos móviles, por ejemplo, la administración de actualizaciones de software de Windows, EndPoint Protection y la configuración del Firewall de Windows.

## Vea también
[Documentación de Microsoft Intune](../Topic/Documentation-for-Microsoft-Intune.md)

