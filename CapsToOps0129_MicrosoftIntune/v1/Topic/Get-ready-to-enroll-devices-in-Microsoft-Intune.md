---
title: Preparar la inscripci&#243;n de dispositivos en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 44fd4af0-f9b0-493a-b590-7825139d9d40
---
# Preparar la inscripci&#243;n de dispositivos en Microsoft Intune
[![](../Image/Nav-Icons/WIT_Tile_W_Overview.png)](https://technet.microsoft.com/library/dn646960.aspx/?WT.mc_id=IntuneOverview20150801)[![](../Image/Nav-Icons/WIT_Tile_W_GetStarted.png)](https://technet.microsoft.com/library/dn646953.aspx/?WT.mc_id=IntuneGS20150801)![](../Image/Nav-Icons/WIT_Tile_W_EnrollDevicesHighlight.png)[![](../Image/Nav-Icons/WIT_Tile_W_ManageDevices.png)](https://technet.microsoft.com/library/mt313202.aspx/?WT.mc_id=IntuneConfig20150801)[![](../Image/Nav-Icons/WIT_Tile_W_ManageApps.png)](https://technet.microsoft.com/library/dn646965.aspx/?WT.mc_id=IntuneDeploy20150801)[![](../Image/Nav-Icons/WIT_Tile_W_ProtectResources.png)](https://technet.microsoft.com/library/mt313203.aspx/?WT.mc_id=IntuneProtect20150801)[![](../Image/Nav-Icons/WIT_Tile_W_RetireData.png)](https://technet.microsoft.com/library/mt313204.aspx/?WT.mc_id=IntuneRetire20150801)[![](../Image/Nav-Icons/WIT_Tile_W_TechnicalReference.png)](https://technet.microsoft.com/library/mt282239.aspx/?WT.mc_id=IntuneTR20150801)[![](../Image/Nav-Icons/WIT_Tile_W_Troubleshooting.png)](https://technet.microsoft.com/library/mt345521.aspx)
![](../Image/Nav-Icons/WIT_Banner_EnrollDevices.png)

Para permitir que los empleados usen recursos de la empresa en dispositivos móviles (como Windows Phone, iOS y Android), debe habilitar la inscripción de dispositivos, que es el proceso que incorpora dispositivos en la administración. Para ello, primero debe establecer [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] como entidad de dispositivo móvil y habilitar la inscripción para el sistema operativo del dispositivo. Los equipos que ejecutan Windows 8.1 y Windows 10 también se pueden administrar como dispositivos móviles, o bien puede administrarlos mediante el [software cliente de Intune](http://technet.microsoft.com/library/dn646959.aspx).

## Habilitar la inscripción de dispositivos móviles
Para habilitar la inscripción de MDM, debe establecer la *entidad de administración de dispositivos móviles*. La entidad de MDM define el servicio de administración que tiene permiso para administrar un conjunto de dispositivos.  Las opciones para la entidad de MDM incluyen [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], Administrador de configuración con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] o las soluciones MDM de Office 365.  Office 365 e Intune pueden usarse conjuntamente para administrar dispositivos móviles. Si System Center Configuration Manager se establece como la entidad de gestión, ningún otro servicio podrá usarse para la administración de dispositivos móviles. Para empezar, [establezca Intune como la entidad de MDM](https://technet.microsoft.com/library/mt346013.aspx).

A continuación, debe habilitar la inscripción para los sistemas operativos que su organización desea admitir. Algunos sistemas operativos de dispositivos móviles (como Windows e iOS) requieren una relación de confianza entre los dispositivos e [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] para permitir la administración.

-   [Configurar la administración de Android con Microsoft Intune](../Topic/Set-up-Android-management-with-Microsoft-Intune.md)

-   [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md): incluidos los [dispositivos iOS propiedad de la empresa](https://technet.microsoft.com/library/dn408185.aspx#BKMK_DEP)

-   [Configurar la administración de Windows Phone con Microsoft Intune](../Topic/Set-up-Windows-Phone-management-with-Microsoft-Intune.md)

-   [Configurar la administración de dispositivos Windows con Microsoft Intune](../Topic/Set-up-Windows-device-management-with-Microsoft-Intune.md)

## Administrar varios dispositivos con la cuenta de administrador de inscripción de dispositivos
Las organizaciones pueden usar Intune para administrar un gran número de dispositivos móviles con una sola cuenta de usuario. El *administrador de inscripción de dispositivos* es una cuenta especial de Intune con permisos para inscribir más de cinco dispositivos. Consulte [Inscribir dispositivos propiedad de la empresa con el Administrador de inscripción de dispositivos de Microsoft Intune](../Topic/Enroll-corporate-owned-devices-with-the-Device-Enrollment-Manager-in-Microsoft-Intune.md).

## MDM con Intune y Exchange ActiveSync
Para que [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] administre dispositivos móviles directamente, los usuarios deben inscribir los dispositivos en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Para los dispositivos móviles que los usuarios no inscriban se puede habilitar la administración de Exchange ActiveSync mediante Exchange Connector. Los dispositivos de Exchange se pueden administrar tanto en servidores locales como, en el caso de Exchange hospedado en Microsoft Office 365, en la nube. Exchange Connector le conecta con su implementación de Exchange y le permite administrar los dispositivos móviles a través de la consola de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Consulte [Administración de dispositivos móviles con Exchange ActiveSync e Microsoft Intune](../Topic/Mobile-device-management-with-Exchange-ActiveSync-and-Microsoft-Intune.md).

## Vea también
[Documentación de Microsoft Intune](../Topic/Documentation-for-Microsoft-Intune.md)

