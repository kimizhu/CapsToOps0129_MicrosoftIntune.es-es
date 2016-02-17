---
title: Formas de llevar a cabo la movilidad empresarial
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2d91b8b5-bf44-4562-ab4a-6611584f9674
---
# Formas de llevar a cabo la movilidad empresarial
Microsoft proporciona varias opciones para administrar los dispositivos móviles. En esta página se proporciona información que le ayudará a decidir entre varias opciones según sus necesidades de movilidad empresarial:

-   [Elección entre Intune y MDM para Office 365](#BKMK_MDMOfferings)

-   [Elija entre Intune por separado o bien integrar Intune con System Center Configuration Manager](#BKMK_HybridOfferings)

## <a name="BKMK_MDMOfferings"></a>Elección entre Intune y MDM para Office 365

|Consideración|MDM para Office 365|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|
|-----------------|-----------------------|---------------------------------------------------------|
|Coste|Se incluye en muchas [suscripciones comerciales de Office 365](http://products.office.com/business/enterprise-productivity-tools).|Se necesita una [suscripción de pago a Microsoft Intune](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/Purchasing.aspx) o se puede adquirir con [Enterprise Mobility Suite](http://www.microsoft.com/en-us/server-cloud/products/enterprise-mobility-suite/Purchasing.aspx).|
|Cómo administrar dispositivos|Administre dispositivos mediante el [Centro de administración de Office 365](https://support.office.com/article/About-the-Office-365-admin-center-58537702-d421-4d02-8141-e128e3703547).|Si usa [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] por separado, administre los dispositivos por medio de la [consola de administración de Intune](https://technet.microsoft.com/library/dn646966.aspx).<br /><br />Si integra Intune con System Center 2012 Configuration Manager, use la consola de Configuration Manager para administrar los dispositivos locales y en la nube.|
|Dispositivos que se pueden administrar|Administración basada en la nube para:<br /><br />-   iOS<br />-   Android<br />-   Windows Phone|Administración basada en la nube para:<br /><br />-   iOS<br />-   Mac OS X<br />-   Android<br />-   Windows Phone<br />-   Equipos de Windows|
|Capacidades clave|-   Asegúrese de que los teléfonos y las tabletas que su empresa administra pueden acceder a los documentos y al correo electrónico corporativo de Office 365, y de que cumplen con las directivas de TI.<br />-   Establecer y administrar directivas de seguridad, como el bloqueo de PIN y detección de jailbreak en el nivel del dispositivo, para ayudar a evitar que usuarios no autorizados tengan acceso a datos y correo electrónico corporativo en un dispositivo extraviado o robado.<br />-   Quitar datos de la empresa de Office 365 en el dispositivo de un empleado y dejar sus datos personales.<br /><br />Para obtener la información más reciente sobre las capacidades de MDM para Office 365, vea [Capacidades de administración de dispositivos móviles integrada para Office 365](https://technet.microsoft.com/library/ms.o365.cc.devicepolicysupporteddevice.aspx).|Capacidades de MDM para Office 365, además de:<br /><br />-   Ayudar a los usuarios a acceder con seguridad a los recursos corporativos con certificados, Wi-Fi, VPN y perfiles de correo electrónico.<br />-   Inscribir y administrar colecciones de dispositivos de empresa para simplificar la implementación de aplicaciones y directivas.<br />-   Implementar las aplicaciones de línea de negocio internas y las aplicaciones en tiendas para los usuarios.<br />-   Permitir a los usuarios acceder con seguridad a información corporativa por medio de las aplicaciones de línea de negocio y móviles de Office, y al mismo tiempo garantizar la seguridad de datos restringiendo las acciones como *copiar*, *cortar*, *pegar* y *guardar como* a aquellas aplicaciones administradas por [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].<br />-   Habilitar la exploración web segura mediante la aplicación Explorador administrado de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].<br />-   Administrar equipos desde la nube sin ninguna infraestructura necesaria mediante [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] o conectar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a [!INCLUDE[cm5short](../Token/cm5short_md.md)] para administrar todos los dispositivos, incluidos equipos de Windows, Mac, servidores Linux y UNIX, así como dispositivos móviles, desde una sola consola de administración.|
A partir de octubre de 2015, los administradores pueden administrar los usuarios y sus dispositivos móviles mediante Intune y Office 365 simultáneamente en el mismo inquilino. Esto le permite decidir qué solución es la mejor para usuarios específicos y sus dispositivos correspondientes. A continuación, puede especificar si un usuario y sus dispositivos se administran con MDM de Office 365 o bien con la solución de administración de Intune, que cuenta con más características.

## <a name="BKMK_HybridOfferings"></a>Elija entre Intune por separado o bien integrar Intune con System Center Configuration Manager

|Puede elegir [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] independiente si:|Puede elegir [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] + Configuration Manager si:|
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
|-   Quiere administrar dispositivos móviles<br />-   Quiere administrar equipos que no están unidos a un dominio<br />-   Tiene menos de 50.000 dispositivos que administrar<br />-   No tiene infraestructura local de TI (o es limitada) **Note:**     [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] no requiere una infraestructura de TI local, pero puede usar las funciones de Exchange ActiveSync o los servicios de dominio de Active Directory, si están instalados.<br />-   Tiene una plantilla móvil o muy distribuida. La administración de dispositivos basada en la nube permite administrar dispositivos móviles y equipos en todo el mundo.|-   Quiere administrar equipos unidos a un dominio.<br />-   Quiere administrar servidores.<br />-   Quiere administrar equipos con el cliente de Configuration Manager, equipos Mac, servidores Linux y UNIX y dispositivos móviles inscritos con Intune desde la misma consola.<br />-   Tiene más de 50.000 dispositivos que administrar.<br />-   Cuenta con una infraestructura de TI local o tiene previsto implementarla. En esta configuración, la experiencia de administración de dispositivos y recursos está totalmente unificada.<br />-   Los nombres de usuario y las contraseñas se sincronizan, y proporcionan a los usuarios una sola cuenta que pueden usar para acceder a los recursos de la compañía desde un equipo unido al dominio o desde un dispositivo móvil.|

### Comparación detallada de capacidades
En las siguientes tablas se comparan las capacidades de administración de dispositivos y aplicaciones disponibles cuando se usa solo [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], solo Configuration Manager o una solución que usa ambos productos.

Para obtener información sobre el uso de Configuration Manager con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Administrar dispositivos móviles con Configuration Manager y Microsoft Intune](http://msdn.microsoft.com/en-us/library/2c6bd0e5-d436-41c8-bf38-30152d76be10).

#### Compatibilidad con dispositivos

|Plataforma|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|System Center 2012 Configuration Manager SP2|System Center 2012 Configuration Manager SP2 y [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|
|--------------|---------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------------|
|Microsoft Windows|Sí|Sí|Sí|
|Microsoft Windows Server|No|Sí|Sí|
|Windows Phone|Sí|No|Sí|
|Windows RT|Sí|No|Sí|
|iOS|Sí|No|Sí|
|Android y Samsung KNOX|Sí|No|Sí|
|Mac OS X|Sí|Sí|Sí|
|Servidores UNIX/Linux|No|Sí|Sí|

#### Capacidades del producto
> [!TIP]
> Donde se indique con (R2), la capacidad de la lista necesita Microsoft System Center 2012 R2 Configuration Manager o posterior.

|Escenario|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|System Center 2012 Configuration Manager SP2|System Center 2012 Configuration Manager SP2 y [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|
|-------------|---------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------------|
|**Configuración de conformidad**||||
|Implementar y personalizar los parámetros de configuración del equipo Windows (por ejemplo, WMI, Registro)|No|Sí|Sí|
|Implementar y personalizar los parámetros de configuración de Mac OS X|Sí|Sí|Sí|
|Implementar los parámetros de configuración en dispositivos móviles.|Sí|Sí|Sí|
|Implementar la configuración de dispositivos móviles personalizada (como OMA-URI y el Configurador de Apple)|Sí|Sí|Sí|
|**Implementación**||||
|Implementar aplicaciones en dispositivos y equipos Windows|Sí|Sí|Sí|
|Implementar sistemas operativos Windows|No|Sí|Sí|
|**Seguridad y privacidad**||||
|Administrar actualizaciones de software de Windows|Sí|Sí|Sí|
|Supervisar el malware en equipos Windows con Endpoint Protection|Sí|Sí|Sí|
|**Administración y generación de informes**||||
|Supervisar e informar sobre la frecuencia con que se usa el software con medición de software|No|Sí|Sí|
|Inventario de hardware y software|Sí|Sí|Sí|
|Ampliar el inventario de software y hardware para equipos Windows|No|Sí|Sí|
|Usar informes y administración basada en roles para controlar quién tiene acceso a las funciones del producto|No|Sí|Sí|
|Ejecutar informes para equipos Windows y dispositivos móviles inscritos desde la misma consola|No|No|Sí|
|Personalizar informes existentes y crear sus propios informes mediante SQL Server Reporting Services|No|Sí|Sí|
|**Protección de datos para dispositivos móviles**||||
|Implementar la configuración de seguridad en dispositivos móviles|Sí|Sí|Sí|
|Borrado remoto|Sí|Sí|Sí|
|Bloqueo remoto|Sí|Sí|Sí|
|Restablecimiento de la contraseña|Sí|Sí|Sí|
|**Acceso a los recursos de la empresa**||||
|Perfiles de correo electrónico|Sí|Sí (R2)|Sí (R2)|
|Perfiles de Wi-Fi|Sí|Sí (R2)|Sí (R2)|
|Perfiles de VPN|Sí|Sí (R2)|Sí (R2)|
|Perfiles de certificado|Sí|Sí (R2)|Sí (R2)|
|Administrar el acceso al correo electrónico de Exchange y SharePoint con acceso condicional|Sí|Sí|Sí|
|Administración de aplicaciones móviles|Sí|Sí|Sí|
|Directivas de conformidad de las aplicaciones (aplicaciones conformes y no conformes)|Sí|Sí|Sí|
|Modo de quiosco|Sí|Sí|Sí|
|Directiva de exploradores de Internet administrados|Sí|Sí|Sí|
|**Automatización**||||
|Uso de PowerShell para automatizar las operaciones|No|Sí|Sí|

## Vea también
[Introducción a Microsoft Intune](../Topic/Introduction-to-Microsoft-Intune.md)

