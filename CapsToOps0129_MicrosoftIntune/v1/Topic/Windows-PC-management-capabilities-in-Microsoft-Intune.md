---
title: Funciones de administraci&#243;n de equipos Windows en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 77fa5c66-a87c-47df-964c-800eea509b33
---
# Funciones de administraci&#243;n de equipos Windows en Microsoft Intune
Puede usar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] para administrar equipos Windows con el cliente de Intune instalado. La administración de equipos le permite implementar aplicaciones y software, incluidas las actualizaciones de software, en los equipos administrados, administrar Endpoint Protection y Firewall de Windows, y mucho más.  A continuación se muestra una lista de las configuraciones y las funciones admitidas.

## <a name="BKMK_ClientReqs"></a>Requisitos para la administración de equipos
**Sistemas operativos**: 
puede instalar el cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en equipos que ejecutan los siguientes sistemas operativos (x86 y x64):

-   **Windows Vista**: versiones Business, Enterprise y Ultimate.

-   **Windows 7**: versiones Professional, Enterprise y Ultimate (sin Service Pack o con SP1).

-   **Windows 8**: versiones Professional y Enterprise.

-   **Windows 8.1**: versiones Professional y Enterprise.

-   **Windows 10**: versiones Professional y Enterprise.

**Hardware**:
los siguientes son requisitos mínimos de hardware para instalar el cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]:

|Requisito|Más información|
|-------------|-------------------|
|Red|El cliente requiere que el equipo tenga conectividad a Internet.|
|Procesador y memoria|Consulte los requisitos de RAM y procesador para el sistema operativo del equipo.|
|Espacio en disco|200 MB de espacio disponible en el disco antes de que se instale el software cliente.|
**Software**: 
los siguientes son los requisitos de software para instalar el cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]:

|Requisito|Más información|
|-------------|-------------------|
|Permisos administrativos|La cuenta que instala el software de cliente debe tener permisos de administrador local en ese equipo.|
|Windows Installer 3.1|El equipo debe tener, como mínimo, Windows Installer 3.1.<br /><br />Para ver la versión de Windows Installer de un equipo:<br /><br />-   En el equipo, haga clic con el botón derecho en **%windir%\System32\msiexec.exe**, y, a continuación, en **Propiedades**.<br /><br />Puede descargar la última versión de Windows Installer desde [Windows Installer Redistributables (Paquetes redistribuibles de Windows Installer)](http://go.microsoft.com/fwlink/?LinkID=234258) en el sitio web de Microsoft Developer Network.|
|Quitar software cliente incompatible|Antes de instalar el software cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], debe desinstalar el software cliente siguiente del equipo:<br /><br />-   Cualquier versión de [!INCLUDE[cm5short](../Token/cm5short_md.md)]<br />-   Cualquier versión de [!INCLUDE[sccmshortname](../Token/sccmshortname_md.md)]<br />-   Cualquier versión de Systems Management Server (SMS)|

## <a name="WIT_Cap"></a>Funciones de administración de equipos de Intune

-   **Administrar actualizaciones de software** Puede tener actualizados los equipos y administrar cuándo se aplican las actualizaciones.

-   **Directiva de Firewall de Windows** Esto ayuda a garantizar que ningún equipo utilizado por la compañía tenga un Firewall de Windows inactivo o mal configurado.

-   La **protección antimalware** [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] incluye Endpoint Protection, que ayuda a proteger los equipos del software malintencionado.

-   La **asistencia remota** [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] permite a los usuarios ponerse en contacto con el personal de soporte técnico de TI, que puede proporcionar asistencia mediante una característica de escritorio remoto que se incluye con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

-   Administración de **licencias de software**.  Realice el seguimiento del número de licencias de software disponibles y el número de licencias disponibles que se usan.

## Vea también
[Introducción a Microsoft Intune](../Topic/Introduction-to-Microsoft-Intune.md)
[Administrar equipos Windows con Microsoft Intune](../Topic/Manage-Windows-PCs-with-Microsoft-Intune.md)

