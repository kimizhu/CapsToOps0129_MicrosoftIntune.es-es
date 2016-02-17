---
title: Habilitar el acceso a los recursos de empresa con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3dd8dd4e-e165-4d0c-97b7-b3e86ebab909
---
# Habilitar el acceso a los recursos de empresa con Microsoft Intune
Los **perfiles de acceso de los recursos** de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] funcionan juntos para ayudar a los usuarios a obtener acceso a los archivos y recursos que necesitan para hacer su trabajo correctamente, estén donde estén.

[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] proporciona las siguientes directivas de dispositivos móviles que ayudan a lograr este objetivo. Haga clic en cualquier elemento de la tabla para obtener información detallada acerca de cómo configurar la directiva:

## Perfiles de acceso de recursos y plataformas admitidas

|Directiva de Intune|Lo que hace|Windows 8.1 y posterior|Windows Phone 8.1 y versiones posteriores|iOS|Android|Samsung KNOX|
|-----------------------|---------------|---------------------------|---------------------------------------------|-------|-----------|----------------|
|[Perfiles de certificado](https://technet.microsoft.com/library/dn818904.aspx)|Contribuya a proteger el acceso a los recursos de empresa tales como las redes inalámbricas y las conexiones VPN.|Sí|Sí|Sí|Sí|Sí|
|[Perfiles de Wi-Fi](https://technet.microsoft.com/library/dn818903.aspx)|Implementar la configuración de red inalámbrica para los usuarios. Mediante la implementación de esta configuración, se minimiza la intervención del usuario final necesaria para conectarse a la red corporativa.|Sí (se puede importar un perfil de Wi-Fi de Windows)|Sí (se puede configurar el OMA-URI) <sup>1</sup>|Sí|Sí|Sí|
|[Perfiles de VPN](https://technet.microsoft.com/library/dn818905.aspx)|Implementar la configuración de red privada virtual (VPN) a los usuarios. Mediante la implementación de esta configuración, se minimiza la intervención del usuario final necesaria para conectarse a los recursos de la red corporativa.|Sí|Sí|Sí|Sí|Sí|
|[Perfiles de correo electrónico](https://technet.microsoft.com/library/dn800672.aspx)|Cree, implemente y supervise la configuración de correo electrónico Exchange ActiveSync en los dispositivos de su organización.|No|Sí|Sí|No|Sí|
<sup>1</sup> Consulte [esta entrada de blog](http://blogs.technet.com/b/microsoftintune/archive/2015/02/23/using-oma-uri-to-create-custom-wi-fi-profiles-for-windows-phone-8-1.aspx) para obtener información sobre cómo configurar un perfil de Wi-Fi de Windows Phone 8.1 mediante OMA-URI.

## Vea también
[Configurar y administrar dispositivos con Microsoft Intune](../Topic/Configure-and-manage-devices-with-Microsoft-Intune.md)

