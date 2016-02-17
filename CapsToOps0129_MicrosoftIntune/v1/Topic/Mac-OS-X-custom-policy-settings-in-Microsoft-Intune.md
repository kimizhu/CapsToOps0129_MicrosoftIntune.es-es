---
title: Configuraci&#243;n de directivas personalizadas de Mac OS X en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 70459e56-17d8-4d3f-803d-22feefa7a5b6
---
# Configuraci&#243;n de directivas personalizadas de Mac OS X en Microsoft Intune
Use la **directiva de configuración personalizada de Mac OS X** de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] para implementar la configuración que creó mediante la [herramienta Apple Configurator](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12) en los dispositivos Mac OS X. Esta herramienta permite crear muchas configuraciones para controlar el funcionamiento de estos dispositivos y exportarlas a un perfil de configuración. Después, puede importar el perfil de configuración en una directiva personalizada de Mac OS X de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] e implementar la configuración para los usuarios y los dispositivos de la organización.

El fin de esta funcionalidad es permitirle implementar la configuración de Mac OS X que no se puede definir con una directiva de configuración general de Mac OS X de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Para obtener más información sobre las opciones que se pueden configurar con estas directivas, consulte [Configuración de directivas de configuración de Mac OS X en Microsoft Intune](../Topic/Mac-OS-X-configuration-policy-settings-in-Microsoft-Intune.md).

## Requisitos previos
Antes de empezar, debe tener instalado Apple Configurator y haber creado un archivo de configuración que contenga la configuración que desea implementar en usuarios o dispositivos. Puede descargar Apple Configurator y obtener información sobre esta aplicación en el [Mac App Store](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12)

> [!NOTE]
> [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] no notifica la compatibilidad de las opciones de configuración individuales de una directiva personalizada de Mac OS X. Sin embargo, se notifica el cumplimiento general de la directiva.

## Cómo crear una directiva personalizada de Mac OS X

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Directiva** &gt; **Información general** &gt; **Agregar directiva**.

2.  Configure una directiva del tipo **Mac OS X** &gt; **Configuración personalizada**.

    Para ayudar a crear e implementar directivas, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

    Solo puede crear e implementar una directiva personalizada de Mac OS X. La configuración recomendada no está disponible.

3.  Utilice la tabla siguiente como ayuda para definir la configuración de directivas:

    |Nombre de la configuración|Más información|
    |------------------------------|-------------------|
    |**Nombre**|Escriba un nombre único para la directiva personalizada de Mac OS X que le ayude a identificarla en la consola de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Descripción**|Proporcione una descripción que ofrezca información general de la directiva personalizada de Mac OS X y otra información relevante que le ayude a encontrarla.|
    |**Nombre del perfil de configuración personalizada (que se muestra a los usuarios)**|Proporcione el nombre de la directiva que se mostrará en el dispositivo y en los informes de directivas de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Archivo del perfil de configuración**|Haga clic en **Importar** y luego examine el perfil de configuración que ha creado con Apple Configurator. **Tip:** Consulte [Cómo crear un archivo de perfil de configuración](#BKMK_Prof) en este tema para obtener ayuda sobre cómo crear el perfil de configuración.|
    |**Detalles del perfil de configuración**|Muestra el código XML del perfil de configuración que ha importado.|

4.  Cuando haya terminado haga clic en **Guardar directiva**.

5.  La nueva directiva se muestra en el nodo **Directivas de configuración** del área de trabajo **Directiva**.

## <a name="BKMK_Prof"></a>Cómo crear un archivo de perfil de configuración
Para crear el archivo del perfil de configuración usado por la directiva personalizada se pueden seguir dos procesos distintos:

-   Exportar el archivo (con la extensión **.mobileconfig**) desde la herramienta Apple Configurator.

-   Crear el archivo mediante el esquema apropiado de la [referencia principal de los perfiles de configuración de Apple](https://developer.apple.com/library/ios/featuredarticles/iPhoneConfigurationProfileRef/Introduction/Introduction.html).

## Implementación de una directiva personalizada de Mac OS X

-   Implemente la directiva personalizada de Mac OS X en uno o más grupos de usuarios o dispositivos de la organización.

Para obtener ayuda acerca de la implementación de directivas, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

En el área de trabajo **Directiva** de la página **General**, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención. Además, aparece un resumen de estado en el área de trabajo **Panel**.

> [!IMPORTANT]
> Cuando un dispositivo Mac OS X está en modo de suspensión, no se pueden entregar ni inventariar las directivas y los perfiles. Como resultado, la consola de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] puede mostrar temporalmente el estado **Configuraciones de directivas con errores** hasta que el dispositivo salga del modo de suspensión.

## Vea también
[Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md)

