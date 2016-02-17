---
title: Introducci&#243;n a las directivas de administraci&#243;n de aplicaciones m&#243;viles en el portal de Azure
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e6a85e7-e007-41b6-9034-64d77f547b87
---
# Introducci&#243;n a las directivas de administraci&#243;n de aplicaciones m&#243;viles en el portal de Azure
En este tema se explica lo que necesita para empezar a crear directivas de administración de aplicaciones móviles (MAM) en el portal de Azure.

**En este tema**

[Aplicaciones compatibles](#bkmk_supportedapps)

[Plataformas compatibles](#bkmk_supportedplatforms)

[Qué necesita para empezar](#bkmk_Prereqs)

[Especificar los requisitos previos](#bkmk_prereqshowto)

[Acceso al portal de vista previa de Azure](#bkmk_azureportal)

[Pasos siguientes](#bkmk_nextsteps)

## <a name="bkmk_supportedplatforms"></a>Plataformas compatibles

-   iOS 7.1 o posterior

-   Android 4 o versiones posteriores

## <a name="bkmk_supportedapps"></a>Aplicaciones compatibles
**iOS:** Microsoft Word, Excel, PowerPoint y OneDrive

**Android:** OneDrive

## <a name="bkmk_Prereqs"></a>Qué necesita para empezar
Antes de empezar, necesitará lo siguiente:

-   Una suscripción a [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].    Los usuarios finales necesitan licencias de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] para obtener aplicaciones con la directiva MAM.

-   Una suscripción a Office 365 (O365) y Azure Active Directory (Azure AD) para crear usuarios y asignar licencias de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].  Azure AD autentica al usuario cuando el usuario final inicia la aplicación y escribe sus credenciales de trabajo.

    > [!NOTE]
    > Si está configurando los usuarios mediante la consola [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], tenga en cuenta que la configuración de la directiva MAM se traslada a partir de ahora al portal de Azure y para usar este portal, deberá configurar grupos de usuarios de Azure AD mediante el portal de Office 365.

## <a name="bkmk_prereqshowto"></a>Especificar los requisitos previos
En la tabla siguiente se enumeran los roles y los permisos que puede asignar a los usuarios de administración.

|||
|-|-|
|**Rol**|**Permisos**|
|Administrador global (portal de O365)|-   Acceso al portal de O365<br />-   Acceso al portal de Azure AD<br />-   Acceso al portal de vista previa de Azure (se pueden realizar tanto la tarea de administración de roles como la de administración de aplicaciones móviles)|
|Rol de propietario (portal de vista previa)|-   Acceso al portal de vista previa de Azure (se pueden realizar tanto la tarea de administración de roles como la de administración de aplicaciones móviles)|
|Rol de colaborador (portal de vista previa)|-   Acceso al portal de vista previa de Azure (solo se pueden realizar las tareas de administración de aplicaciones móviles)|

#### Crear usuarios y asignar licencias de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

1.  Ya tiene una suscripción de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] si usa [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] actualmente para administrar los dispositivos.  También tiene una suscripción de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] si ha adquirido una licencia de EMS. Si está probando [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] para comprobar las capacidades de MAM, puede obtener una cuenta de prueba [aquí](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/).

    Para comprobar si tiene una suscripción de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], en el portal de Office, vaya a la página de facturación.  Debería ver [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] como **Activa** en las suscripciones.

2.  Inicie sesión en el [portal de Office](http://portal.office.com) con sus credenciales de administrador.

3.  Vaya a la página **Usuarios activos** para agregar usuarios y asignar licencias de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    ![](../Image/AppManagement/OfficePortal_AddUsers.png)

4.  Para conceder a un usuario la capacidad de tener acceso al portal de Office, al portal de Azure AD y al portal de vista previa de Azure, asigne el **rol de administrador global** al usuario.

    ![](../Image/AppManagement/OfficePortal_AddRoletoUser.png)

5.  Las directivas MAM se implementan para grupos de usuarios de Azure Active Directory. Para crear grupos de usuarios que desea usar para sus directivas MAM, vaya a la página **Grupos** del **portal de Office** y haga clic en el icono **+** para crear un nuevo grupo de seguridad.  Escriba un nombre y una descripción y haga clic en **Crear**. Cuando se cree el grupo, podrá agregar usuarios al grupo haciendo clic en **Editar miembros** en el grupo de seguridad recién creado. El grupo de seguridad se crea en Azure Active Directory.

    ![](../Image/AppManagement/OfficePortal_CreateGroups.png)

## <a name="bkmk_azureportal"></a>Acceso al portal de vista previa de Azure
El **portal de vista previa** permite crear directivas de aplicación, implementar la directiva a los usuarios y supervisar el estado de la implementación.

#### Para empezar a usar el portal

1.  Vaya el [portal de vista previa](https://portal.azure.com) e inicie sesión con sus credenciales de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    ![](../Image/AppManagement/AzurePortal_MAMSigninPage.png)

2.  Una vez que haya iniciado sesión correctamente, verá la página **Inicio** o la página **principal**. La página **Inicio** o la página principal incluye un conjunto de iconos predeterminados que puede quitar y agregar otros nuevos para personalizar la página.

    ![](../Image/AppManagement/AzurePortal_MAMStartboard_NoMAM.png)

3.  En el menú **Examinar**, busque **Intune**.![](../Image/AppManagement/AzurePortal_MAM_Browse_Intune.png)

4.  Haga clic en **Intune &gt; Administración de aplicaciones móviles de Intune &gt; Configuración**.

    ![](../Image/AppManagement/AzurePortal_MAM_Mainblade.png)

    > [!TIP]
    > Para anclar una hoja a la página **Inicio**, puede usar la opción **anclar** de la hoja.  Haga clic en el icono del ancla de la **Hoja de administración de aplicaciones móviles de Intune** para anclarlo a la página **Inicio**.

    ![](../Image/AppManagement/AzurePortal_MAM_PinBladeAction.png)

    ![](../Image/AppManagement/AzurePortal_MAM_Startboard_withMAM.png)

Los **administradores globales** tienen acceso al portal de Azure.  Si quiere que otros usuarios administradores puedan configurar directivas y llevar a cabo otras tareas de administración de aplicaciones móviles, puede asignar el **rol Colaborador** al usuario como se describe a continuación:

#### Asignar el rol Colaborador a un usuario

1.  En la hoja **Configuración**, en la sección **Administración de recursos**, haga clic en **Usuarios**.

    ![](../Image/AppManagement/AzurePortal_MAM_AddUsers.png)

2.  Haga clic en **Agregar** para abrir la hoja **Agregar acceso**.

3.  Haga clic en **Selecciona un rol** y, luego, **Rol Colaborador**.

    ![](../Image/AppManagement/AzurePortal_MAM_AddRole.png)

4.  Una vez haya seleccionado el rol, haga clic en **Agregar usuario** y busque el usuario por el nombre de usuario o la dirección de correo electrónico. Los usuarios que ve en esta lista son los 1000 primeros usuarios que creó anteriormente en Azure AD con el portal de Office. Haga clic en **Aceptar** en la hoja **Agregar acceso** para guardar y asignar el rol al usuario.

    ![](../Image/AppManagement/AzurePortal_MAM_AddusertoRole.png)

    > [!IMPORTANT]
    > Si selecciona un usuario que no tiene una licencia de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] asignada, ese usuario no podrá tener acceso al portal.

## <a name="bkmk_nextsteps"></a>Pasos siguientes
[Crear e implementar directivas de administración de aplicaciones móviles con Microsoft Intune](../Topic/Create-and-deploy-mobile-app-management-policies-with-Microsoft-Intune.md)

## Vea también
[Configurar directivas de aplicaciones de prevención de pérdida de datos con Microsoft Intune](../Topic/Configure-data-loss-prevention-app-policies-with-Microsoft-Intune.md)

