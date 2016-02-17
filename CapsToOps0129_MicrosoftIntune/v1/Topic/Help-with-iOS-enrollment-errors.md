---
title: Ayuda con errores de inscripci&#243;n de iOS
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c91075e8-e184-49a9-bedf-4a213872613f
robots: noindex,nofollow
---
# Ayuda con errores de inscripci&#243;n de iOS
Este tema le ayuda a solucionar errores de inscripción de iOS.

## Errores de inscripción de iOS
La siguiente tabla muestra los errores que los usuarios pueden encontrar durante la inscripción de dispositivos iOS. Para cada error se proporciona una causa posible y detalles de la solución.

|Mensaje de error|Causa posible|Resolución mediante [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|Resolución mediante System Center 2012 R2 Configuration Manager|
|--------------------|-----------------|-----------------------------------------------------------------------------|-------------------------------------------------------------------|
|DeviceCapReached|Este mensaje indica que el usuario ya tiene demasiados dispositivos móviles inscritos.|Antes de que el usuario inscriba otro dispositivo móvil, debe quitar uno de los dispositivos móviles actualmente inscritos en el portal de empresa.|Antes de que el usuario inscriba otro dispositivo móvil, debe quitar uno de los dispositivos móviles actualmente inscritos en el portal de empresa.|
|APNSCertificateNotValid|El servicio de notificaciones de inserción de Apple (APNS) proporciona un canal para llegar a dispositivos iOS inscritos. Si no se realizaron los pasos para obtener un certificado de APNS o ha expirado el certificado de APNS, los intentos de inscripción producirán un error.|Revise la sección “Dependencias externas para inscribir dispositivos iOS” del documento [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).|Revise la sección “Dependencias externas para inscribir dispositivos iOS” del documento [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).|
|AccountNotOnboarded|El servicio de notificaciones de inserción de Apple (APNS) proporciona un canal para llegar a dispositivos iOS inscritos. Si no se realizaron los pasos para obtener un certificado de APNS, los intentos de inscripción producirán un error.|Revise la sección “Dependencias externas para inscribir dispositivos iOS” del documento [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).|Revise la sección “Dependencias externas para inscribir dispositivos iOS” del documento [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).|
|DeviceTypeNotSupported|Puede obtener este mensaje si intenta realizar la inscripción con un dispositivo que no es iOS.|Compruebe que el dispositivo ejecuta iOS versión 5.0 o posterior.|Compruebe que el dispositivo ejecuta iOS versión 5.0 o posterior.|
|UserLicenseTypeInvalid|Para que los usuarios puedan inscribir sus dispositivos, deben ser miembros del grupo de usuarios adecuado. Este mensaje indica que el usuario tiene el tipo de licencia incorrecto para la entidad de administración de dispositivos móviles designada. Por ejemplo, si [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] fue designado como su entidad de administración de dispositivos móviles y el usuario utiliza una licencia de System Center 2012 R2 Configuration Manager, recibirá un error.|Revise la sección “Aprovisionar usuarios para la inscripción de dispositivos” del documento [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).|Revise la sección “Aprovisionar usuarios para la inscripción de dispositivos” del documento [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).|
|MdmAuthorityNotDefined|Este mensaje indica que la entidad de administración de dispositivos móviles no fue designada en [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].|Revise la sección “Establecer la entidad de administración de dispositivos móviles en Microsoft Intune” del documento [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).|Revise la sección “Establecer la entidad de administración de dispositivos móviles en Microsoft Intune” del documento [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).|
