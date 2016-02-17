---
title: Preguntas m&#225;s frecuentes acerca del SDK para aplicaciones de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 133d81c4-e550-404a-980e-64f6e843c649
---
# Preguntas m&#225;s frecuentes acerca del SDK para aplicaciones de Microsoft Intune
Aquí se incluyen algunas de las preguntas más frecuentes en relación con el SDK para aplicaciones de Intune.

## Tengo un problema con el SDK para aplicaciones de Intune o con la documentación. ¿Cómo puedo enviar mis comentarios o informar de problemas?

Los comentarios sobre el SDK para aplicaciones de Intune se pueden enviar a través del sitio de Microsoft Connect que encontrará aquí. Verá una opción para enviar los comentarios o el problema. Le rogamos que indique la prioridad de los problemas que envíe; una vez hecho esto, el equipo de Microsoft Intune se pondrá a trabajar en ellos tan pronto como le sea posible.

![Formulario de comentarios de la aplicación](/Image/App-Feedback-Form.png)

## ¿Cómo funciona el SDK para aplicaciones de Intune con las actualizaciones y la compatibilidad del sistema operativo?

Trabajamos duro para que las características del SDK funcionen tan pronto como sea posible en la nueva versión del sistema operativo. Como estas nuevas características del sistema operativo son accesibles para el usuario final desde las aplicaciones ya existentes, queremos garantizar que el SDK no provocará errores en las aplicaciones o que supondrá un cambio demasiado grande para el usuario final.

Cuando los proveedores del sistema operativo nos proporcionan el tiempo suficiente, Intune se encarga de proporcionar soporte técnico para las versiones del sistema operativo Beta; de esta manera, el usuario puede habilitar las pruebas de la versión preliminar de la aplicación. Los ISV deben informar de antemano de cualquier problema de compatibilidad detectado o de si existen planes para lanzar versiones de las aplicaciones destinadas a versiones de vista previa del sistema operativo.

Las nuevas características agregadas al SDK no deberán crear problemas de compatibilidad con el sistema operativo existente si antes no se ha avisado a Microsoft y sin su consentimiento previo; cualquier problema involuntario de compatibilidad se tratará como un error.

## ¿Cómo afecta el SDK para aplicaciones de Intune a mi aplicación móvil?

El SDK puede afectar a la aplicación de tres maneras principales.
* **Rendimiento**: los métodos usados para aplicar la directiva pueden afectar al rendimiento de la aplicación. Revise el rendimiento y notifique los problemas o errores que encuentre; deberá incluir los resultados de rendimiento con y sin la directiva, para que podamos revisar la situación.
* **Características opcionales**: el SDK es compatible con características opcionales a través de la superficie de la API (por ejemplo, guardar como). Debe realizar cambios en la aplicación para que estas características sean compatibles.
    System_CAPS_noteNote

    La telemetría es una característica opcional. El SDK de MAM para iOS registra los datos de telemetría acerca de los eventos de uso **de forma predeterminada**. Estos datos se envían a Microsoft Intune. Si decide no enviar los datos de telemetría del SDK a Microsoft Intune desde su aplicación, debe deshabilitar la captura de telemetría del SDK estableciendo la propiedad `MAMTelemetryDisabled` en “Sí” en `IntuneMAMSettings`.
* **Aplicación de directivas**: cuando se aplica la directiva MAM en aplicaciones del SDK, se pueden modificar las características de la aplicación y la experiencia del usuario. Los equipos de la aplicación deberían trabajar junto con el equipo de Intune para probar sus aplicaciones y así poder comprender mejor este efecto.



