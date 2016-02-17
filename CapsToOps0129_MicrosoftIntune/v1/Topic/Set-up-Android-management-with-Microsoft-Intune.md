---
title: Configurar la administraci&#243;n de Android con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dbe5cad1-3e0d-41a9-966b-738156089700
---
# Configurar la administraci&#243;n de Android con Microsoft Intune
Los dispositivos móviles Android permiten a los usuarios inscribirse mediante la aplicación Portal de empresa disponible en Google Play. Para que los usuarios puedan inscribir sus dispositivos en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], realice los pasos siguientes.

## Configurar dispositivos móviles Android con Microsoft Intune

1.  **Configurar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]** 
    Si aún no lo hizo, prepare la administración de dispositivos móviles [estableciendo la entidad de administración de dispositivos móviles](https://technet.microsoft.com/library/mt346013.aspx) en **Microsoft Intune**.

2.  **Agregar usuarios de Intune** 
    El propietario del dispositivo móvil debe agregarse al portal de cuentas para poder inscribir dispositivos.  Inicie sesión en el [Portal de cuentas de Microsoft Intune](http://go.microsoft.com/fwlink/?LinkId=698854), haga clic en **Agregar usuarios** y seleccione una opción:

    -   **Usuario**: para agregar un solo usuario, seleccione **Nuevo** &gt; **Usuario** y especifique **Detalles**, **Asignar roles** y **Establecer ubicación de usuario**; a continuación, asigne el usuario a un **Grupo**.

    -   **Adición en masa**: cree un archivo .csv (vea ejemplos de archivos proporcionados) e impórtelo en el portal de cuentas. Especifique los roles, la ubicación y el grupo y, después, cree las cuentas. Los archivos .csv de ejemplo y en blanco se pueden descargar desde el portal de cuentas.

    También puede habilitar la sincronización de Active Directory o Azure Active Directory. Para obtener más información sobre la integración de otros usuarios de Azure Active Directory con Intune, consulte la [Guía de sincronización de directorios](http://go.microsoft.com/fwlink/?LinkId=511540) o haga clic en **Otras formas de agregar usuarios** en el portal de cuentas.

3.  **Crear grupos**  (opcional)
    Los grupos ofrecen flexibilidad para administrar dispositivos y usuarios. Los grupos se pueden configurar según sus necesidades de organización (por ejemplo, por ubicación geográfica, departamento o características de hardware).   Consulte [Utilizar grupos para administrar usuarios y dispositivos en Microsoft Intune](../Topic/Use-groups-to-manage-users-and-devices-with-Microsoft-Intune.md).

4.  **Agregar directivas para dispositivos** (opcional)
    Las directivas son grupos de configuraciones que controlan las características de los dispositivos. La mayoría de las directivas MDM son específicas de la plataforma. Las directivas se crean mediante plantillas que contienen configuraciones recomendadas o personalizadas y, luego, se implementan en grupos. Consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

5.  **Establecer el límite de inscripción de dispositivos** (opcional) 
    Para limitar el número de dispositivos móviles que puede inscribir un usuario, inicie sesión en la [consola de administración de Microsoft Intune](http://manage.microsoft.com), haga clic en **Administración** &gt; **Administración de dispositivos móviles** &gt; **Reglas de inscripción**. Seleccione el número máximo de dispositivos que un usuario puede inscribir y haga clic en **Guardar**.

6.  **Establecer la configuración del portal de empresa** 
     Puede personalizar Portal de empresa de Intune para su empresa. En la [consola de administrador de Microsoft Intune](http://manage.microsoft.com), haga clic en **Administración** &gt; **Portal de empresa**. Configure lo siguiente

    -   **Nombre de compañía**

    -   **Nombre del contacto del departamento de TI**

    -   **Número de teléfono del departamento de TI**

    -   **Información adicional**

    -   **Dirección URL de la declaración de privacidad de la empresa**

    -   **Dirección URL del sitio web de soporte técnico (no se muestra)**

    -   **Nombre del sitio web**

7.  [!INCLUDE[CPEnrollmentTermsAndConditions](../Token/CPEnrollmentTermsAndConditions_md.md)]

8.  **Indicar a los usuarios cómo acceder a los recursos de empresa con el portal de empresa** 
    Los usuarios necesitan saber cómo inscribir sus dispositivos y qué esperar una vez que se incorporan a la administración.[Qué decirles a los usuarios finales sobre el uso de Microsoft Intune](../Topic/What-to-tell-your-end-users-about-using-Microsoft-Intune.md)

## Vea también
[Preparar la inscripción de dispositivos en Microsoft Intune](../Topic/Get-ready-to-enroll-devices-in-Microsoft-Intune.md)

