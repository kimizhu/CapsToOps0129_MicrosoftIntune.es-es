---
title: Configuraci&#243;n de directivas personalizadas de iOS en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 04e60d5a-3da6-4943-b6ff-e6a331bcbcfa
---
# Configuraci&#243;n de directivas personalizadas de iOS en Microsoft Intune
Use la [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] **directiva de configuración personalizada de iOS** para implementar la configuración que creó mediante la [herramienta Apple Configurator](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12) en dispositivos iOS. Esta herramienta permite crear muchas configuraciones para controlar el funcionamiento de estos dispositivos y exportarlas a un perfil de configuración. A continuación, puede importar este perfil de configuración en una directiva personalizada de iOS [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] e implementar la configuración para los usuarios y dispositivos de su organización.

Esta capacidad es adecuada para que pueda implementar la configuración de E/s que no es configurables con directivas [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Para obtener información acerca de las opciones que puede configurar con estas directivas, consulte [Configuración de directivas de configuración de iOS en Microsoft Intune](../Topic/iOS-configuration-policy-settings-in-Microsoft-Intune.md).

## Requisitos previos
Antes de empezar, debe tener instalado Apple Configurator y haber creado un archivo de configuración que contenga la configuración que desea implementar en usuarios o dispositivos. Puede descargar Apple Configurator y obtener información sobre esta aplicación en el [Mac App Store](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12)

> [!NOTE]
> [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] no notifica el cumplimiento de opciones de configuración individuales de una directiva personalizada de iOS. Sin embargo, se notifica el cumplimiento general de la directiva.

## Cómo crear una directiva personalizada de iOS

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Directiva** &gt; **Información general** &gt; **Agregar directiva**.

2.  Configure una directiva del tipo **iOS** &gt; **Configuración personalizada**.

    Para ayudar a crear e implementar directivas, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

    Solo puede crear e implementar una directiva personalizada de iOS. La configuración recomendada no está disponible.

3.  Utilice la tabla siguiente como ayuda para definir la configuración de directivas:

    |Nombre de la configuración|Más información|
    |------------------------------|-------------------|
    |**Nombre**|Escriba un nombre único para la directiva personalizada de iOS que le ayude a identificarla en la consola de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Descripción**|Proporcione una descripción que ofrezca una visión general de la directiva personalizada de iOS y otra información relevante que le ayude a encontrarla.|
    |**Nombre del perfil de configuración personalizada (que se muestra a los usuarios)**|Proporcione el nombre de la directiva que se mostrará en el dispositivo y en los informes de directivas de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Archivo del perfil de configuración**|Haga clic en **Importar** y luego examine el perfil de configuración que ha creado con Apple Configurator. **Note:** Asegúrese de que la configuración que exporta de la herramienta Apple Configurator sea compatible con la versión de iOS en los dispositivos en los que implementa la directiva personalizada de iOS. Para obtener información sobre la resolución de las opciones de configuración incompatibles, busque la **referencia de perfiles de configuración** y la **referencia del protocolo de administración de dispositivos móviles** en el sitio web para [desarrolladores de Apple](https://developer.apple.com/).|
    |**Detalles del perfil de configuración**|Muestra el código XML del perfil de configuración que ha importado.|

4.  Cuando haya terminado haga clic en **Guardar directiva**.

5.  La nueva directiva se muestra en el nodo **Directivas de configuración** del área de trabajo **Directiva**.

## Implementar una directiva personalizada de iOS

-   Implemente la directiva personalizada de iOS en uno o más grupos de usuarios o dispositivos de su organización.

Para obtener ayuda acerca de la implementación de directivas, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

En el área de trabajo **Directiva** de la página **General**, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención. Además, aparece un resumen de estado en el área de trabajo **Panel**.

## Vea también
[Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md)

