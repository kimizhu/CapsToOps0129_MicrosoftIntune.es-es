---
title: El equipo ya est&#225; inscrito
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d3a40f5-99e9-48dc-9706-f7a3a23e5704
---
# El equipo ya est&#225; inscrito
Está viendo esta página porque ejecutó el programa de instalación del software cliente de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Sin embargo, el software ya está instalado en el equipo y el programa de instalación no puede continuar.

Esto puede deberse a:

-   El software cliente se instaló anteriormente y el programa de instalación se ejecutó de nuevo.

-   El programa de instalación se ejecutó en el equipo después de que un administrador de TI retirara el dispositivo de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Después de retirar el dispositivo, puede pasar varias horas hasta que se quite el software cliente del equipo.

-   El programa de instalación ha detectado una instalación o eliminación incorrecta reciente del software cliente.

## <a name="bkmk_install"></a>Qué instala el programa de instalación en el equipo
El programa de instalación instala el cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Una vez finalizada la instalación, el software cliente continúa ejecutándose en segundo plano cuando configura el equipo para su uso con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Este proceso puede tardar algún tiempo en completarse e incluye:

-   La inscripción de su equipo en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

-   El envío del inventario del hardware del equipo y del software instalado

-   Configuración de la directiva de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], incluida la instalación de Endpoint Protection (si está configurado)

-   Instalación de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center

Después de instalar [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center, puede usarlo para acceder al portal de empresa donde puede vincular su equipo con la cuenta del trabajo.

## <a name="bkmk_center"></a>Microsoft Intune Center
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center se instala como una aplicación en el equipo después de que el equipo instale correctamente el software cliente e inscriba el equipo en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Puede usar [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center para:

-   **Obtener aplicaciones del portal de empresa**: busque e instale las aplicaciones que el administrador de TI implementa. Al iniciar sesión por primera vez en el portal de empresa de un equipo recién inscrito, tendrá la opción de vincular la cuenta de trabajo con ese equipo.

-   **Buscar actualizaciones de software**: busque las actualizaciones de software que el administrador de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] implementa.

-   **Iniciar un análisis del equipo con Endpoint Protection**: puede iniciar un análisis para buscar software malintencionado en el equipo.

-   **Solicitar asistencia remota**: esta opción está disponible solo cuando el sistema operativo de los equipos admite la asistencia remota.

## <a name="bkmk_validate"></a>Validar que el software cliente está instalado o se ha quitado
**Validar si el cliente está instalado:**
La instalación del cliente [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] está completa cuando las aplicaciones siguientes están disponibles en el equipo:

-   **[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center**

-   **[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Endpoint Protection** (si el administrador de TI ha habilitado Endpoint Protection)

Si está familiarizado con el Administrador de tareas, puede buscar el servicio de cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], que debe estar en ejecución:

-   **OmcSvc**

**Validar si se ha quitado el cliente:**
Después de desinstalar el cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] de un equipo, se quitan las aplicaciones que se instalaron cuando se instaló el cliente, incluido [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center.

Se quita el servicio de cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], **OmcSvc**.

## <a name="bkmk_remove"></a>Cómo quitar el software cliente del equipo
De forma predeterminada, varias horas después de su administrador de TI retire el equipo de la consola de administración de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], se desinstalará el software cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

Para desinstalar manualmente el software cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] de un equipo, puede utilizar los siguientes pasos para forzar la desinstalación:

1.  En el equipo, abra un símbolo del sistema en modo de administrador.

2.  Vaya a la carpeta **%programfiles%\Microsoft\OnlineManagement\Common**

3.  Ejecute el comando siguiente: **ProvisioningUtil.exe /UninstallAgents /MicrosoftIntune**

Esto programará la eliminación del software cliente.

