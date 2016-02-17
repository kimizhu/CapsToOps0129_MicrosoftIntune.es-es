---
title: Preguntas m&#225;s frecuentes de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a8126cca-9ec4-454b-a20b-dc1bb6797327
---
# Preguntas m&#225;s frecuentes de Microsoft Intune
Este tema proporciona respuestas a las preguntas más frecuentes acerca de Microsoft Intune. Si tiene sugerencias para otras preguntas que le gustaría que se respondieran, [infórmenos de ello](https://microsoftintune.uservoice.com/).

## Acerca de estas preguntas más frecuentes
Estas Preguntas más frecuentes se dividen en las siguientes categorías:

-   [General](#BKMK_General)

-   [Cuentas](#BKMK_Accounts)

-   [Inscripción](#BKMK_Enrollment)

-   [Administración de dispositivos móviles](#BKMK_MDM)

-   [Implementación de aplicaciones](#BKMK_App_Deploy)

-   [Seguridad](#BKMK_Security)

-   [Portal de empresa](#BKMK_Company_Portal)

-   [Microsoft Intune con Configuration Manager](#BKMK_hybrid)

### <a name="BKMK_General"></a>General

-   **¿Cómo puedo saber cuándo se ha actualizado el servicio de Microsoft Intune?**

    Inicie sesión en su cuenta en manage.microsoft.com. En Información general de administración, seleccione Ver estado del servicio. La ubicación del inquilino y la programación de mantenimiento se muestran ahí. Para obtener información detallada sobre las actualizaciones del servicio, consulte [Novedades de Microsoft Intune](../Topic/What-s-new-in-Microsoft-Intune.md).

-   **Si un usuario cambia el nombre de un dispositivo dentro de la aplicación del portal de empresa, ¿cambiará ese nombre en Intune o Configuration Manager?**

    No, ese cambio de nombre es solo por conveniencia del usuario.

-   **¿Hay alguna funcionalidad de asistencia remota en Intune para dispositivos móviles?**

    No, no hay ninguna. Las aplicaciones de terceros como [Lumia Beamer](https://www.lumiabeamer.com/), [Bomgar](http://www.bomgar.com/) y [TeamViewer](https://www.teamviewer.com/) podrían resultar útiles.

### <a name="BKMK_Accounts"></a>Cuentas

-   **Si empiezo a evaluar Intune y creo un nuevo inquilino para la versión de prueba, ¿puedo agregar O365 a la evaluación mediante el mismo inquilino?**

    Sí. Simplemente inicie sesión con un administrador global desde su suscripción o inquilino existente de Intune, como *globaladmin@&lt;compañía &gt;.onmicrosoft.com*.

-   **¿Si asigno una autoridad de MDM a Intune durante una suscripción de prueba, ¿me sería difícil cambiar a un servicio de otra empresa si cambio de opinión acerca de Intune?**

    Aunque es difícil imaginar que no se quede con Intune, la elección de la autoridad de MDM no afecta a su capacidad de cambiarse a otro servicio. Se trata específicamente de elegir Intune o Intune con System Center Configuration Manager, de O365 MDM.

-   **¿Puedo usar mi nombre de dominio existente de Office 365 para mi siguiente cuenta de Intune?**

    Sí, si inicia sesión con el identificador de organización que está asociado con su dominio comprobado y su inquilino de O365 existente cuando cree su versión de evaluación de Intune o active las licencias. Intune usará el mismo dominio y los mismos usuarios que en su cuenta de O365. Tenga en cuenta que cada usuario O365 tendría que estar habilitado como usuario de Intune, con una licencia de Intune. Esto lo tendría que hacer el administrador global que administra el inquilino.

### <a name="BKMK_Enrollment"></a>Inscripción

-   **¿Dónde pueden aprender mis usuarios a inscribir sus dispositivos?**

    Puede usar o personalizar la información de las [Instrucciones de inscripción de Microsoft Intune](http://www.microsoft.com/en-us/download/46398).

-   **¿Cómo puedo solucionar problemas con la inscripción de dispositivos?**

    En [Troubleshoot device enrollment in Intune](../Topic/Troubleshoot-device-enrollment-in-Intune.md) se proporcionan métodos para solucionar problemas comunes de inscripción.

-   **¿Cómo puedo recopilar registros de inscripción si un usuario tiene un problema de inscripción?**

    Siga [estas instrucciones](http://www.microsoft.com/en-us/download/46391).

### <a name="BKMK_MDM"></a>Administración de dispositivos móviles

-   **MDM general**

    -   **¿Puede detectar Intune si un dispositivo está liberado mediante jailbreak?**

        Sí, en algunos sistemas operativos. Para obtener información sobre cómo administrar dispositivos liberados mediante jailbreak, consulte [Administrar directivas de cumplimiento del dispositivo de Microsoft Intune](../Topic/Manage-device-compliance-policies-for-Microsoft-Intune.md).

    -   **¿Puedo borrar selectivamente datos corporativos de un dispositivo?**

        Sí. Para obtener información sobre el borrado selectivo, consulte [Ayude a proteger sus datos mediante la eliminación remota, el bloqueo remoto o el restablecimiento de código de acceso mediante Microsoft Intune.](../Topic/Help-protect-your-data-with-remote-wipe,-remote-lock,-or-passcode-reset-using-Microsoft-Intune.md).

    -   **¿Hay alguna manera de bloquear determinados sitios web en el explorador del dispositivo móvil a través de Intune?**

        No en el explorador nativo de ninguna plataforma. Sin embargo, puede permitir o bloquear las URL cuando implemente el explorador web administrado de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en dispositivos iOS y Android. Para obtener más información, consulte [Administrar el acceso a Internet mediante directivas de explorador administrado con Microsoft Intune](../Topic/Manage-Internet-access-using-managed-browser-policies-with-Microsoft-Intune.md).

    -   **¿Podemos impedir que un usuario desinstale una aplicación?**

        Por lo general, no. Sin embargo, en un dispositivo iOS supervisado puede impedir que un usuario desinstale una aplicación que se distribuyó con Apple Configurator. Para obtener información acerca del uso del modo supervisado en Microsoft Intune, consulte [Manage access to apps using Microsoft Intune configuration policies - deleted](../Topic/Manage-access-to-apps-using-Microsoft-Intune-configuration-policies---deleted.md).

    -   **¿Hay alguna manera de administrar el uso de datos móviles?**

        No directamente, pero puede asegurarse de que Wi-Fi sea el método preferido para conectarse insertando perfiles de Wi-Fi en los dispositivos, tal como se describe en [Ayudar a los usuarios a conectarse a las redes de la compañía mediante perfiles de Wi-Fi con Microsoft Intune](../Topic/Help-users-connect-to-company-networks-using-Wi-Fi-profiles-with-Microsoft-Intune.md). Además, algunas plataformas (por ejemplo, iOS y Android KNOX) permiten controlar ajustes como la itinerancia de voz y de datos.

    -   **¿Hay alguna forma de evitar que un usuario anule la inscripción de un dispositivo? ¿Qué ocurre si se trata de un dispositivo que pertenece a la empresa?**

        En general, no. Sin embargo, mediante la configuración predeterminada de Windows Phone, puede aplicar esto en Windows Phone 8.1. Además, en los dispositivos iOS que están supervisados o inscritos en el programa de inscripción de dispositivos Apple, es posible impedir que un usuario anule la inscripción de un dispositivo.

    -   **¿Puedo cambiar mi autoridad de MDM seleccionada?**

        Puede cambiar la autoridad de MDM en algunos casos. Para ello, póngase en contacto con soporte técnico, tal como se describe en [Cómo obtener asistencia para Microsoft Intune](../Topic/How-to-get-support-for-Microsoft-Intune.md). En la siguiente tabla se describen los cambios que son posibles. Los cambios en la autoridad de MDM requieren volver a inscribir los dispositivos.

        |||||
        |-|-|-|-|
        ||**A:** Intune|**A:** O365|**A:** Configuration Manager con Intune|
        |**Desde:** Intune||Sí&#42;|Sí|
        |**Desde:** O365|Sí&#42;||Sí|
        |**Desde:** Configuration Manager con Intune|Sí|Sí||
        &#42;Las autoridades de MDM de Intune y O365 pueden coexistir, por lo que no tendrá que volver a inscribir dispositivos móviles.

-   **Windows**

    -   **¿Puedo transferir localmente una aplicación de la Tienda Windows?**

        Las aplicaciones disponibles públicamente no pueden transferirse localmente. Aunque es posible descargar el archivo XAP, no puede cargarlo a Intune porque es un archivo XAP público, cifrado y firmado con el certificado de firma de código del desarrollador. Solo puede transferir localmente las aplicaciones que desarrolle y firme con su propio certificado de firma de código.

    -   **¿Las aplicaciones de la Tienda de Windows Phone distribuidas a través del portal de empresa requieren que el usuario final tenga una cuenta Microsoft?**

        Sí, el usuario final no podrá obtener las aplicaciones sin una cuenta Microsoft. La excepción son las aplicaciones LOB privadas y transferidas localmente, que se pueden implementar en un dispositivo sin una cuenta Microsoft.

    -   **¿Es necesaria una cuenta Microsoft en un dispositivo Windows Phone 8.1 para que se pueda administrar mediante Intune?**

        No. Sin embargo, se necesitará para instalar la mayoría de las aplicaciones desde la tienda pública.

-   **Android**

    -   **¿Cuánto tiempo se necesita para cifrar un dispositivo Android?**

        Esto depende principalmente de la velocidad del procesador del dispositivo y la cantidad de memoria total y utilizada. No es una función de Intune.

-   **iOS**

    -   **Al implementar aplicaciones de iOS con Intune, si se han cargado el archivo de manifiesto e IPA de la aplicación, ¿el dispositivo necesita que se especifique un identificador de Apple para continuar con la instalación?**

        No. Cuando Intune proporciona los bits (IPA cargado en Intune), las aplicaciones se transfieren localmente y no necesitan un identificador de Apple.

    -   **¿Hay alguna forma de habilitar la instalación de aplicaciones en iOS sin permitir el acceso a Apple Store?**

        No, pero puede habilitar App Store y usar aplicaciones permitidas y bloqueadas en iOS para vigilar lo que los usuarios están haciendo. Las aplicaciones LOB transferidas localmente no requieren acceso al App Store de Apple.

    -   **¿Las aplicaciones de Apple Store distribuidas a través del Portal de empresa requieren que el usuario final tenga una cuenta de iTunes?**

        Sí, el usuario final no podrá obtener las aplicaciones sin una cuenta de iTunes.

    -   **¿Puedo bloquear App Store?**

        Sí, pero esto bloqueará todas las instalaciones y actualizaciones de aplicaciones de la tienda de aplicaciones, no solo las iniciadas por el usuario final. Esto significa que cualquier aplicación de App Store pública que implemente desde Intune también produciría un error.

### <a name="BKMK_App_Deploy"></a>Implementación de aplicaciones

-   **¿Cómo puedo agregar una aplicación recomendada?**

    En Intune se denominan "aplicaciones destacadas" y se documentan en [Implementar aplicaciones en dispositivos móviles en Microsoft Intune](../Topic/Deploy-apps-to-mobile-devices-in-Microsoft-Intune---deleted.md).

-   **¿Puedo obtener almacenamiento en nube adicional para las aplicaciones que quiero implementar?**

    Sí. Puede leer sobre esto en [Introducción a la implementación de aplicaciones en Microsoft Intune](../Topic/Plan-for-app-deployment-in-Microsoft-Intune.md), en la sección *Requisitos de almacenamiento en nube*.

### <a name="BKMK_Security"></a>Seguridad

-   **¿Puede Intune exigir BitLocker?**

    El agente de OMA-DM en Windows 8.1/RT permite leer (obtener) el estado de cifrado. No puede establecerlo. Esto es así para Microsoft Intune y otros servicios de administración de dispositivos móviles.

-   **Si cifro una tableta de Windows 8 mediante BitLocker, ¿puedo aplicar el borrado completo del dispositivo si un usuario no puede iniciar sesión correctamente varias veces consecutivas?**

    No hay ninguna opción de borrado completo en dispositivos Windows 8.1/RT en ningún servicio de administración de dispositivos móviles, incluido Intune. Intune permite el borrado selectivo de esos dispositivos. Para obtener más información sobre el borrado selectivo o completo en Intune, consulte [Ayude a proteger sus datos mediante la eliminación remota, el bloqueo remoto o el restablecimiento de código de acceso mediante Microsoft Intune.](../Topic/Help-protect-your-data-with-remote-wipe,-remote-lock,-or-passcode-reset-using-Microsoft-Intune.md).

### <a name="BKMK_Company_Portal"></a>Portal de empresa

-   **¿Puedo personalizar mi Portal de empresa?**

    Sí. En la consola de administración de Intune, vaya a **Administración &gt; Portal de empresa** para ver esas configuraciones

### <a name="BKMK_hybrid"></a>Microsoft Intune con Configuration Manager

-   **Al usar Configuration Manager con Intune, ¿dónde administro mis dispositivos?**

    Administre todos los dispositivos desde la consola de Configuration Manager, aunque los dispositivos con el agente de Intune instalado aparezcan en la consola de Intune. Los dispositivos móviles no aparecerán en la consola de Intune.

-   **¿Puedo realizar un borrado selectivo de los dispositivos?**

    Si usa System Center 2012 R2 Configuration Manager o una versión posterior con Intune, puede realizar un borrado selectivo de los datos de la empresa. Para obtener más información, consulte [Ayude a proteger sus datos mediante la eliminación remota, el bloqueo remoto o el restablecimiento de código de acceso mediante Microsoft Intune.](../Topic/Help-protect-your-data-with-remote-wipe,-remote-lock,-or-passcode-reset-using-Microsoft-Intune.md).

-   **Si estoy usando Configuration Manager junto con Intune, ¿puedo seguir usando el Portal de administración de Intune?**

    Puede, pero solo los equipos que tengan instalado el agente de Intune se podrán administrar desde ese portal. También hay más información útil en el portal sobre las alertas del servicio, el estado del servicio, etc., pero la configuración de administración de dispositivos no se aplicará a los dispositivos inscritos.

## Vea también
[Referencia técnica de Microsoft Intune](../Topic/Technical-reference-for-Microsoft-Intune.md)

