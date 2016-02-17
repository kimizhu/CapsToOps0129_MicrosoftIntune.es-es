---
title: Preguntas m&#225;s frecuentes acerca del portal de empresa
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 523caa6b-d792-4bb6-bddb-24b2479932d8
---
# Preguntas m&#225;s frecuentes acerca del portal de empresa

## P+F acerca del portal de empresa

-   [¿Qué es el portal de empresa?](../Topic/Company-Portal-Frequently-Asked-Questions.md#BKMK_WhatIs)

-   [¿Qué puedo hacer en el portal de empresa?](../Topic/Company-Portal-Frequently-Asked-Questions.md#BKMK_WhatCanIDo)

-   [¿Qué ocurre cuando se agrega un equipo o dispositivo al portal de empresa?](../Topic/Company-Portal-Frequently-Asked-Questions.md#BKMK_AddDevice)

-   [¿Qué tipos de equipos o dispositivos puedo agregar al portal de empresa?](../Topic/Company-Portal-Frequently-Asked-Questions.md#BKMK_WhatCanIAdd)

-   [¿Puedo eliminar un equipo o dispositivo del portal de empresa?](../Topic/Company-Portal-Frequently-Asked-Questions.md#BKMK_RemoveDevice)

-   [¿Por qué no veo todos mis dispositivos en el portal de empresa?](../Topic/Company-Portal-Frequently-Asked-Questions.md#BKMK_CantSeeDevices)

-   [Tengo que instalar una nueva versión del portal de empresa](../Topic/Company-Portal-Frequently-Asked-Questions.md#BKMK_InstallNewVersion)

-   [Aparece un error que indica que el equipo ya está inscrito](../Topic/Company-Portal-Frequently-Asked-Questions.md#BKMK_NotEnrolled)

-   [Solución de problemas de mensajes de error de iPhone durante la inscripción](../Topic/Company-Portal-Frequently-Asked-Questions.md#BKMK_TroubleshootingiOS)

### <a name="BKMK_WhatIs"></a>¿Qué es el portal de empresa?
El portal de empresa es la interfaz de su empresa a través de la cual puede administrar sus equipos y dispositivos de trabajo, o administrar sus equipos o dispositivos personales que decida usar en el trabajo.El portal de empresa puede ser un sitio web; también puede ser una aplicación que se instala en el dispositivo.

### <a name="BKMK_WhatCanIDo"></a>¿Qué puedo hacer en el portal de empresa?
Si agrega un equipo o dispositivo al portal de empresa, podrá buscar aplicaciones de empresa para instalarlas, administrar otros dispositivos agregados y buscar los datos de contacto del administrador de TI.

### <a name="BKMK_AddDevice"></a>¿Qué ocurre cuando se agrega un equipo o dispositivo al portal de empresa?
Al agregar un equipo o dispositivo al portal de empresa, es posible que se instale software o se descargue una aplicación (en función del dispositivo).También proporciona al administrador de TI permiso para administrar el dispositivo, a fin de ayudar a proteger la información de la empresa en el dispositivo.Para obtener más información, consulte [What Happens if you Add a Device to the Company Portal (Implicaciones de agregar un dispositivo al portal de empresa)](http://go.microsoft.com/fwlink/?LinkID=265350).

### <a name="BKMK_WhatCanIAdd"></a>¿Qué tipos de equipos o dispositivos puedo agregar al portal de empresa?

-   Dispositivos Windows 8.1

-   Dispositivos Windows RT

-   Windows Phone 8

-   Windows Phone 8,1

-   iPhone y iPad

-   Dispositivos Android

### <a name="BKMK_RemoveDevice"></a>¿Puedo eliminar un equipo o dispositivo del portal de empresa?
Sí, puede quitar o restablecer un equipo o dispositivo del portal de empresa.Hay una diferencia entre **quitar** y **restablecer**:

-   Si quita un equipo o dispositivo, este dejará de tener acceso al portal de empresa y es posible que se quiten del dispositivo algunos datos de la empresa.

-   Al restablecer un equipo o dispositivo, el portal de empresa intenta restablecer la configuración predeterminada de fábrica del equipo o dispositivo.Esto puede hacer que se borren todos los datos, tanto los de la empresa como los datos personales.

Para obtener más información, consulte [Quitar o borrar un dispositivo mediante el portal de empresa](http://go.microsoft.com/fwlink/?LinkID=260958).

### <a name="BKMK_CantSeeDevices"></a>¿Por qué no veo todos mis dispositivos en el portal de empresa?
Para ver un dispositivo, antes debe agregarlo al portal de empresa.Siga las indicaciones del administrador para acceder al portal de la empresa y siga los pasos para su dispositivo.Además, no podrá ver los dispositivos que posee y administra su empresa.

### <a name="BKMK_InstallNewVersion"></a>Tengo que instalar una nueva versión del portal de empresa
Si su versión del portal de empresa ya no es compatible, o si hay disponible una versión más actualizada del mismo, use los procedimientos siguientes para actualizar su dispositivo.

##### Para actualizar el dispositivo Windows

1.  Vaya a la Tienda Windows y busque **portal de empresa**.

2.  Siga las instrucciones de instalación.

    > [!NOTE]
    > Si no puede tener acceso a la Tienda Windows, póngase en contacto con el administrador.

##### Para actualizar el dispositivo iOS

1.  La AppStore de Apple le avisará cuando haya disponible una nueva versión del portal de empresa.Siga las instrucciones en la alerta para actualizar el dispositivo.

### <a name="BKMK_NotEnrolled"></a>Aparece un error que indica que el equipo ya está inscrito
Esto significa que el equipo ya se ha agregado al portal de empresa pero aún no está vinculado a su cuenta de usuario.Siga este procedimiento para vincular el equipo a su cuenta de usuario y completar el proceso.

##### Para vincular el equipo

1.  En el equipo que quiere vincular a su cuenta, haga clic en **Inicio** y después en **Microsoft Intune Center**.

2.  Abra el portal de empresa.

3.  Siga las instrucciones para vincular el equipo a su cuenta de usuario.

### <a name="BKMK_TroubleshootingiOS"></a>Solución de problemas de mensajes de error de iPhone durante la inscripción
Si se producen errores al inscribir su iPhone, siga las instrucciones siguientes.

#### DeviceCapReached
**Problema:** este mensaje indica que ya hay demasiados dispositivos móviles inscritos.

**Solución:** antes de inscribir otro dispositivo móvil, debe quitar uno de los dispositivos móviles inscritos actualmente del portal de empresa.

#### APNSCertificateNotValid
**Problema:** este mensaje indica que hay un problema con el certificado que permite al dispositivo móvil comunicarse con la red de la compañía.

**Solución:** póngase en contacto con el administrador de TI e indíquele que recibió el mensaje **APNSCertificateNotValid** mientras intentaba inscribir el dispositivo móvil. Encontrará la solución en el tema sobre cómo [solucionar problemas de inscripción de iOS con Windows Intune o System Center 2012 R2 Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=327928).

#### AccountNotOnboarded
**Problema:** este mensaje indica que hay un problema con el certificado que permite al dispositivo móvil comunicarse con la red de la compañía.

**Solución:** póngase en contacto con el administrador de TI e indíquele que recibió el mensaje **AccountNotOnboarded** mientras intentaba inscribir el dispositivo móvil. Encontrará la solución en el tema sobre cómo [solucionar problemas de inscripción de iOS con Windows Intune o System Center 2012 R2 Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=327928).

#### DeviceTypeNotSupported
**Problema:** este mensaje indica que no se admite el tipo de dispositivo móvil que intenta inscribir.

**Solución:** póngase en contacto con el administrador de TI e indíquele que recibió el mensaje **DeviceTypeNotSupported** mientras intentaba inscribir el dispositivo móvil. Encontrará la solución en el tema sobre cómo [solucionar problemas de inscripción de iOS con Windows Intune o System Center 2012 R2 Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=327928).

#### UserLicenseTypeInvalid
**Problema:** este mensaje indica que no puede inscribir el dispositivo móvil porque su cuenta de usuario ya no pertenece a ningún grupo de usuarios requerido.

**Solución:** póngase en contacto con el administrador de TI e indíquele que recibió el mensaje **UserLicenseTypeInvalid** mientras intentaba inscribir el dispositivo móvil. Encontrará la solución en el tema sobre cómo [solucionar problemas de inscripción de iOS con Windows Intune o System Center 2012 R2 Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=327928).

#### MdmAuthorityNotDefined
**Problema:** este mensaje indica que el administrador de TI necesita configurar la forma en que se administran los dispositivos móviles de la compañía.

**Solución:** póngase en contacto con el administrador de TI e indíquele que recibió el mensaje **MdmAuthorityNotDefined** mientras intentaba inscribir el dispositivo móvil. Encontrará la solución en el tema sobre cómo [solucionar problemas de inscripción de iOS con Windows Intune o System Center 2012 R2 Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=327928).

