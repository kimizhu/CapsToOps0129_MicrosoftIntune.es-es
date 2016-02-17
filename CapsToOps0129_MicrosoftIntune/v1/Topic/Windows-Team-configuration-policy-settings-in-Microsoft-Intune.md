---
title: Configuraci&#243;n de directivas de configuraci&#243;n del Equipo de Windows en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 38194ef3-e26e-4682-958d-14b395fccba1
---
# Configuraci&#243;n de directivas de configuraci&#243;n del Equipo de Windows en Microsoft Intune
Use la **directiva de configuración del Equipo de Windows 10**[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] para definir la configuración para dispositivos del Equipo de Windows 10 inscritos como Microsoft Surface Hub.

## Crear una directiva de configuración del Equipo de Windows 10

#### Para proporcionar la configuración básica de una directiva de configuración

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Directiva** &gt; **Información general** &gt; **Agregar directiva**.

2.  Haga clic en **Windows** &gt; **Configuración general (Equipo de Windows 10 y versiones posteriores)** y luego haga clic en **Crear directiva**.

    > [!NOTE]
    > No se puede crear una directiva de configuración usando la configuración recomendada. Debe crear una directiva personalizada.

3.  En la sección **General** de la página **Crear directiva**, especifique un nombre y una descripción para la nueva directiva.

4.  Use la información que encontrará en la siguiente sección para ayudarle a ofrecer la configuración de la directiva.

5.  Cuando haya terminado haga clic en **Guardar directiva**.

La nueva directiva se muestra en el nodo **Directivas de configuración** del área de trabajo **Directiva**.

## <a name="BKMK_Settings"></a>Lista de opciones de configuración de esta directiva

### <a name="BKMK_sec"></a>Configuración del dispositivo

|Nombre de la configuración|Detalles|
|------------------------------|------------|
|**Permitir que la pantalla se active automáticamente cuando haya alguien en la habitación**|Permite que el dispositivo se active automáticamente cuando su sensor detecta alguien en la sala.|
|**Requerir PIN para la proyección inalámbrica**|Especifica si debe escribir un PIN para poder usar las capacidades de proyección inalámbrica del dispositivo.|
|**Establecer ventana de mantenimiento**|Configura la ventana cuando las actualizaciones tienen lugar en el dispositivo. Puede configurar la hora de inicio de la ventana y la duración (de 1 a 5 horas).|

## Implementar la directiva de configuración

1.  Implemente la directiva de configuración en uno o más grupos de usuarios o dispositivos de su organización.

Para obtener más información sobre cómo implementar directivas, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

En el área de trabajo **Directiva**, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención. Además, aparece un resumen de estado en el área de trabajo **Panel**.

## Vea también
[Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md)

