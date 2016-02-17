---
title: Ayudar a proteger dispositivos iOS con el bypass del bloqueo de activaci&#243;n para Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2804b69c-f210-4a11-aaee-b47ecc430d9c
---
# Ayudar a proteger dispositivos iOS con el bypass del bloqueo de activaci&#243;n para Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] puede ayudarle a administrar el bloqueo de activación de iOS, una característica de la aplicación Buscar mi iPhone para dispositivos iOS 7.1 o versiones posteriores. El bloqueo de activación se habilita automáticamente cuando se usa la aplicación Buscar mi iPhone en un dispositivo. Una vez habilitado, se debe escribir el identificador y la contraseña de Apple del usuario para poder:

-   Desactivar Buscar mi iPhone

-   Borrar el dispositivo

-   Reactivar el dispositivo

## Cómo afecta el bloqueo de activación
Aunque el bloqueo de activación ayuda a proteger dispositivos iOS y aumenta las posibilidades de recuperarlos ante la pérdida o el robo, esta funcionalidad puede suponerle una serie de desafíos como administrador de TI. Por ejemplo:

-   Uno de los usuarios establece el bloqueo de activación en un dispositivo. Luego, el usuario se va de la empresa y devuelve el dispositivo. Sin el identificador y la contraseña de Apple del usuario, no hay forma de volver a activar el dispositivo.

-   Necesita un informe de todos los dispositivos que tienen habilitado el bloqueo de activación.

-   Durante una actualización de los dispositivos de la organización, puede que desee reasignar algunos dispositivos a un departamento diferente. Solo puede volver a asignar dispositivos que no tengan habilitado el bloqueo de activación.

Para ayudar a resolver estos problemas, Apple incorporó el bypass del bloqueo de activación en iOS 7.1. Esto permite quitar el bloqueo de activación de los dispositivos supervisados sin el identificador y la contraseña de Apple del usuario. Los dispositivos supervisados pueden generar un código de bypass del bloqueo de activación específico del dispositivo, que se almacena en el servidor de activación de Apple.

> [!TIP]
> El modo supervisado de los dispositivos iOS permite usar la herramienta Apple Configurator para bloquear un dispositivo a fin de limitar la funcionalidad para fines empresariales específicos. Generalmente, el modo supervisado es solo para los dispositivos de la empresa.

## Cómo ayuda Intune a administrar el bloqueo de activación
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] puede solicitar el estado de bloqueo de activación de dispositivos supervisados y no supervisados que ejecutan iOS 7.1 y posterior. Para los dispositivos supervisados, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] puede recuperar el código de bypass de bloqueo de activación y emitirlo directamente al dispositivo. Si el dispositivo se borró, puede acceder directamente a él usando el código mencionado como nombre de usuario y dejando la contraseña en blanco.

Las ventajas empresariales de esto son:

-   El usuario obtiene los beneficios de seguridad de la aplicación Buscar mi iPhone

-   Permite que el usuario haga su trabajo sabiendo que, cuando el dispositivo se deba reasignar, podrá retirarlo o desbloquearlo.

## Usar el bypass del bloqueo de activación desde la consola de administración de Intune
> [!IMPORTANT]
> Después de omitir el bloqueo de activación en un dispositivo, se aplica automáticamente un nuevo bloqueo de activación si se abre la aplicación Buscar mi iPhone. Por este motivo, para realizar este procedimiento, debe tener el dispositivo físicamente.

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Grupos** &gt; **Todos los dispositivos** &gt; **Todos los dispositivos corporativos**.

2.  Seleccione el dispositivo para el que desea omitir el bloqueo de activación y, después, haga clic en **Bypass del bloqueo de activación**.

3.  Lea el mensaje de advertencia y haga clic en **Sí** para continuar.

Puede examinar el estado de la solicitud de desbloqueo en la página de detalles del dispositivo.

## Ver los dispositivos que usan el bloqueo de activación
Para ver los dispositivos que usan el bloqueo de activación, existen dos métodos:

-   Ejecute los **Informes de inventario de dispositivos móviles**. Este informe muestra las columnas **Estado de activación de bloqueo** y **Supervisado** para indicar el estado de los dispositivos. Los valores de **Supervisado** son **Sí** o **No**, mientras que los de **Estado de activación de bloqueo** son:

    -   **Habilitado con código de derivación**

    -   **Habilitado sin código de derivación (el dispositivo no está supervisado)**

    -   **Habilitado sin código de derivación (no se puede establecer contacto con el dispositivo)**

    -   **No habilitado**

    El campo **Estado de bloqueo de activación** está en blanco para los dispositivos que no ejecutan iOS 7.1 o versiones posteriores.

-   Seleccione un dispositivo en una vista de grupos para ver el estado de bloqueo de activación en el panel de detalles del dispositivo.

    Si selecciona un dispositivo del nodo **Todos los dispositivos corporativos** y el bloqueo de activación está habilitado para el dispositivo, también podrá ver el código de bypass. Este código se puede usar para emitir un bypass del bloqueo de activación manualmente.

## Vea también
[Retirar datos y dispositivos de la administración de Microsoft Intune](../Topic/Retire-data-and-devices-from-Microsoft-Intune-management.md)

