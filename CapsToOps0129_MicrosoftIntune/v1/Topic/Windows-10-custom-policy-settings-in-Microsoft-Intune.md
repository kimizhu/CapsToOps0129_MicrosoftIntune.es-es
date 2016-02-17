---
title: Configuraci&#243;n de directivas personalizadas de Windows 10 en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5756b025-6fe9-418d-a1c4-cae576d31b79
---
# Configuraci&#243;n de directivas personalizadas de Windows 10 en Microsoft Intune
Use la [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] **directiva de configuración personalizada** para Windows 10 y Windows 10 Mobile para implementar la configuración de OMA-URI (identificador uniforme de recursos de Open Mobile Alliance) que puede usarse para controlar las características en dispositivos con Windows 10 y Windows 10 Mobile. Se trata de una configuración estándar que muchos fabricantes de dispositivos móviles usan para controlar las características del dispositivo.

Esta capacidad está destinada a permitirle implementar la configuración de Windows 10 que no se puede configurar con una directiva de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Para obtener información acerca de las opciones que se pueden configurar con estas directivas, consulte [Administrar la configuración y las características de los dispositivos con directivas de Microsoft Intune](../Topic/Manage-settings-and-features-on-your-devices-with-Microsoft-Intune-policies.md).

Para obtener una lista de los valores de OMA-URI que se pueden configurar en dispositivos de Windows 10 inscritos, consulte [Configuración de URI personalizada para dispositivos de Windows 10](../Topic/Custom-URI-settings-for-Windows-10-devices.md).

## Crear una directiva personalizada de Windows 10

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Directiva** &gt; **Agregar directiva**.

2.  En **Windows**, configure una directiva de **configuración personalizada (Windows 10 Escritorio y Mobile y versiones posteriores)**.

    Para crear e implementar directivas fácilmente, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

    Solo puede crear e implementar una directiva personalizada. La configuración recomendada no está disponible.

3.  La tabla siguiente le facilitará la configuración de directivas generales:

    |Nombre de la configuración|Más información|
    |------------------------------|-------------------|
    |**Nombre**|Escriba un nombre único para la directiva que le ayude a identificarla en la consola de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Descripción**|Proporcione una descripción general de la directiva y otra información relevante que le ayude a encontrarla.|

4.  En la sección **Configuración OMA-URI**, haga clic en **Agregar** para agregar un valor. También puede editar o eliminar un valor existente.

5.  En el cuadro de diálogo **Agregar o editar configuración OMA-URI**, especifique la siguiente información:

    |Elemento|Más información|
    |------------|-------------------|
    |**Nombre de la configuración**|Escriba un nombre único para el valor OMA-URI que le ayude a identificarlo en la lista de valores de configuración.|
    |**Descripción del valor**|Proporcione una descripción que ofrezca una visión general del valor y otra información relevante que le ayude a encontrarlo.|
    |**Tipo de datos**|Seleccione el tipo de fecha en que especificará este valor OMA-URI. Elija de entre las siguientes opciones:<br /><br />-   **String**<br />-   **Cadena (XML)**<br />-   **Fecha y hora**<br />-   **Integer**<br />-   **Punto flotante**<br />-   **Boolean**|
    |**OMA-URI (distingue mayúsculas de minúsculas)**|Especifique el OMA-URI para el que desee suministrar un valor.|
    |**Valor**|Especifique el valor asociado con el OMA-URI especificado anteriormente.|

6.  Haga clic en **Aceptar** para guardar el valor y volver a la página **Crear directiva**.

7.  Continúe agregando tantos valores como sea necesario. Cuando haya terminado, haga clic en **Guardar directiva**.

La nueva directiva se muestra en el nodo **Directivas de configuración** del área de trabajo **Directiva**.

## Implementar una directiva personalizada de Windows 10

1.  Implemente la directiva en uno o más grupos de usuarios o dispositivos de su organización.

Para obtener más información sobre cómo implementar directivas, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

En el área de trabajo **Directiva** de la página **General**, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención. Además, aparece un resumen de estado en el área de trabajo **Panel**.

## Vea también
[Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md)

