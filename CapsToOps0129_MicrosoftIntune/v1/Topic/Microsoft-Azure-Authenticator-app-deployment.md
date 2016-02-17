---
title: Implementaci&#243;n de la aplicaci&#243;n Microsoft Azure Authenticator
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: db9a294a-8409-450b-9b83-808a43a64788
robots: noindex,nofollow
---
# Implementaci&#243;n de la aplicaci&#243;n Microsoft Azure Authenticator
Microsoft Azure Authenticator es una parte de Microsoft Enterprise Mobility Suite (EMS) de aplicaciones. Use esta aplicación para permitir a los usuarios y sus dispositivos conectarse de forma segura a los servicios de Microsoft como Office 365. Esta aplicación es necesaria para el control de acceso, la protección de datos y las características de cumplimiento de Microsoft Intune.

Esta aplicación también optimiza la inscripción de los usuarios, lo que proporciona el inicio de sesión único (SSO) y la autenticación multifactor (MFA) para las aplicaciones de sus dispositivos.

Para obtener la mejor experiencia, debe implementar la aplicación como parte de la inscripción de dispositivos de Intune. A partir de septiembre, Intune y Configuration Manager híbrido implementarán automáticamente la aplicación Azure Authenticator para dispositivos Android de Google Play como una instalación necesaria.

[Haga clic aquí](https://msdn.microsoft.com/en-us/library/azure/dn858223.aspx) para más información acerca de la aplicación Azure Authenticator.

## ¿Por qué Intune implementará esta aplicación?
Más adelante este año, Microsoft emitirá una actualización de la aplicación Portal de empresa de Microsoft Intune para simplificar la experiencia de inscripción. Por ejemplo, eliminará los mensajes 'Cuenta profesional Microsoft' y 'Asigne un nombre al certificado' que aparecen durante la inscripción de Intune en dispositivos Android.

![](../Image/Azure-Authenticator-certificate.jpg)

Cuando se actualiza el portal de empresa, los dispositivos Android sin la aplicación Azure Authenticator instalada hacen lo siguiente:

-   Pierden el inicio de sesión único para Intune

-   Pierden el inicio de sesión único para aplicaciones de Office

-   Quedan en cuarentena si está habilitado el acceso condicional

### Recomendaciones para los administradores de TI
Para evitar estos problemas, debe implementar la aplicación Azure Authenticator como instalación necesaria para dispositivos Android antes de la actualización del portal de empresa. Puede hacer esto de dos maneras:

-   Indique a los usuarios finales que instalen la aplicación Microsoft Azure Authenticator ahora desde [Google Play](https://play.google.com/store/apps/details?id=com.azure.authenticator)

-   Implemente manualmente la aplicación Azure Authenticator desde Google Play como una instalación necesaria para todos los usuarios.

O bien, indique a los usuarios finales que sigan la notificación de aplicación necesaria para instalar la aplicación Azure Authenticator desde Google Play después del lanzamiento de las actualizaciones de septiembre de Microsoft Intune y Microsoft System Center Configuration Manager.

![](../Image/Azure-Authenticator-required-install.jpg)

Aunque se recomienda que esta característica permanezca habilitada, si su organización no usa el inicio de sesión único o las características de acceso condicional, puede deshabilitar la implementación automática de la aplicación Azure Authenticator desde la consola de Intune de la siguiente manera:

**Intune:** Vaya al nodo **Administración de dispositivos móviles** &gt; **Android** en la consola de Intune.

**Configuration Manager híbrido:** Vaya a la página **Propiedades de suscripción de Microsoft Intune** de la consola de Configuration Manager.

## Qué hacer si los usuarios están en cuarentena
Si los usuarios con dispositivos Android que son el destino de una directiva de acceso condicional no instalan la aplicación de Azure Authenticator, quedarán en cuarentena del correo electrónico de Exchange cuando se actualice el portal de empresa en sus dispositivos.

Para recuperar el acceso, los usuarios deben hacer clic en el vínculo del correo electrónico de cuarentena que reciben para tener acceso a la aplicación Portal de empresa y, luego, seguir las instrucciones para completar la actualización y la activación de la inscripción.

## Vea también
[Documentación de Microsoft Intune](../Topic/Documentation-for-Microsoft-Intune.md)

