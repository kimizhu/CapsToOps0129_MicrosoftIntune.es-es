---
title: Referencia sobre las cuentas de administrador de inquilinos para Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e4eff7b9-4dcd-4959-b1d6-97dc4640dbe2
---
# Referencia sobre las cuentas de administrador de inquilinos para Microsoft Intune
Cada administrador de inquilinos tiene asignado uno de los roles siguientes:

|Rol|Detalles|
|-------|------------|
|**Administrador de facturación**|realiza compras, administra suscripciones e incidencias de soporte técnico, y supervisa el estado del servicio.|
|**Administrador global**|tiene acceso a todas las funciones administrativas. De forma predeterminada, la persona que se registra para comprar un servicio de nube de Microsoft en nombre de su organización se convierte automáticamente en el primer administrador global de su inquilino.<br /><br />-   Los administradores globales son los únicos que pueden asignar otros roles de administrador.<br />-   Puede haber más de un administrador global en su organización.|
|**Administrador de contraseñas**|restablece contraseñas, administra solicitudes del servicio y supervisa el estado de dicho servicio. Los administradores de contraseñas solo pueden restablecer contraseñas de usuarios y otros administradores de contraseñas.|
|**Administrador de soporte de servicio**|Administra las solicitudes de servicio y supervisa el estado del servicio.|
|**Administrador de control de usuarios**|restablece contraseñas, controla el estado del servicio y administra cuentas de usuario, grupos de usuarios y solicitudes de servicio.|
Cada rol de administrador tiene los siguientes permisos asociados:

|Permiso|Administrador de facturación|Administrador global|Administrador de contraseñas|Administrador de soporte de servicio|Administrador de control de usuarios|
|-----------|--------------------------------|------------------------|--------------------------------|----------------------------------------|----------------------------------------|
|Ver información de la organización y los usuarios|Sí|Sí|Sí|Sí|Sí|
|Administrar vales de soporte|Sí|Sí|Sí|Sí|Sí|
|Restablecer contraseñas de usuario|No|Sí|Sí|No|Sí, con limitaciones. Este administrador no puede restablecer las contraseñas de los administradores de facturación, de servicios y global.|
|Realizar operaciones de facturación y compra|Sí|Sí|No|No|No|
|Crear y administrar vistas de usuarios|No|Sí|No|No|Sí|
|Crear, editar y eliminar usuarios y grupos, y administrar licencias de usuarios|No|Sí|No|No|Sí, con limitaciones. Este administrador no puede eliminar un administrador global ni crear otros administradores.|
|Administrar dominios|No|Sí|No|No|No|
|Administrar la información de la organización|No|Sí|No|No|No|
|Delegar roles administrativos a otras personas|No|Sí|No|No|No|
|Usar la sincronización de directorios|No|Sí|No|No|No|
Para obtener más información acerca de las cuentas administrativas en [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], lea acerca de las [cuentas administrativas y los permisos diferentes para las distintas tareas](http://technet.microsoft.com/library/dn646966.aspx). Para ayudar a administrar los usuarios administrativos, consulte [Task 5: Assign administrative users](../Topic/Get-started-with-a-paid-subscription-to-Microsoft-Intune.md#BKMK_AssignAdmins) en [Introducción a una suscripción de pago de Microsoft Intune](../Topic/Get-started-with-a-paid-subscription-to-Microsoft-Intune.md).

