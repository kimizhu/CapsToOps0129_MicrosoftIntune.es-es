---
title: Ayuda para partners de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9cb7da1d-8ecb-4b08-818a-54782e846def
---
# Ayuda para partners de Microsoft Intune
El portal de partners y sus servicios son una extensión de su suscripción a [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] asociada a su identidad de partner. Al iniciar sesión en el portal de cuentas de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] con una cuenta de trabajo que está asociada a su identificador de partner, tiene acceso al portal de partners usando el vínculo **Partner** de la parte superior del portal de cuentas.

|¿Qué desea hacer?|Detalles|
|---------------------|------------|
|**Comprobar la información de la empresa**|Asegúrese siempre de que la información de su empresa, como los números de teléfono y las direcciones de correo electrónico, sea correcta y visible para sus clientes.<br /><br />Para verificar su información, en el panel de la izquierda del portal de partners haga clic en el nombre de la empresa para ver y editar la información de la empresa.<br /><br />Su cuenta de usuario debe ser un [administrador global](http://technet.microsoft.com/library/dn646966.aspx#BKMK_AdminAccounts) para poder editar la información de la empresa.|
|**Buscar clientes**|Utilice el portal de partners para [Buscar y ayudar a clientes](../Topic/Help-for-Microsoft-Intune-Partners.md#BKMK_FindCustomers) que sean posibles destinatarios de sus servicios, o con quien ya esté trabajando.<br /><br />Puede buscar los clientes con suscripción a [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] por su nombre de cuenta de usuario o por su nombre de dominio.|
|**Crear y enviar invitaciones de evaluación y ofertas de compra**|Como partner, puede [Crear invitaciones de evaluación y ofertas de compra](../Topic/Help-for-Microsoft-Intune-Partners.md#BKMK_CreateTrials) que faciliten a sus clientes probar primero el servicio y posteriormente realizar una compra.<br /><br />Las ofertas que cree incluyen un vínculo desde el cual los clientes pueden obtener acceso a la oferta. El vínculo contiene un código incorporado que le identifica como asesor de la suscripción.|
|**Ofrecer administración delegada**|Como partner, puede [Ofrecer administración delegada](../Topic/Help-for-Microsoft-Intune-Partners.md#BKMK_OfferAdmin), que permite a los usuarios de su empresa proporcionar soporte adicional a sus clientes.|
|**Configurar sus usuarios para ser administradores delegados**|Además de administrar la suscripción de su propia empresa, (incluyendo dar a los usuarios acceso administrativo a su suscripción), puede [Conceder permiso a los usuarios para actuar como administradores delegados](../Topic/Help-for-Microsoft-Intune-Partners.md#BKMK_AssignDelAdmin) para las empresas a las cuales proporciona soporte.|
|**Administrar un cliente**|Cuando sus usuarios tienen acceso administrativo a las empresas a las cuales proporciona soporte, pueden utilizar el portal de partners para [Administrar un cliente como administrador delegado](../Topic/Help-for-Microsoft-Intune-Partners.md#BKMK_Administer).|
Usted sigue utilizando la consola de administración y el portal de cuentas de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] para administrar su propia suscripción, incluyendo dispositivos y usuarios. Para obtener más información acerca de la administración de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], consulte [Documentación de Microsoft Intune](../Topic/Documentation-for-Microsoft-Intune.md).

## <a name="BKMK_FindCustomers"></a>Buscar y ayudar a clientes
Utilice el portal de partners para identificar a los clientes a quien puede ayudar. Tras localizar a un cliente, puede proporcionar servicios o asistencia, lo cual incluye:

-   Ofrecer evaluaciones y suscripciones pagadas

-   Administrar los clientes que han aceptado la administración delegada

-   Crear y enviar solicitudes de servicio

-   Restablecer contraseñas de usuario

Para buscar un cliente en el portal de partners, busque el nombre de dominio o el nombre de usuario del cliente. Si ya es un administrador delegado de un cliente, puede buscar cualquier nombre de dominio asociado a la suscripción.

#### Para buscar y ayudar a un cliente

1.  En la página **Introducción al partner** del portal de partners de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], haga clic en **Búsqueda de usuario o dominio**.

2.  En la página **Buscar usuario o dominio**, escriba el nombre de usuario completo (usuario@contoso.com) o el nombre de dominio (contoso.com) que desea buscar. El nombre debe ser una coincidencia exacta. No se admiten los caracteres comodín. Pulse **Siguiente** para empezar la búsqueda.

3.  Cuando se encuentra una coincidencia, aparece una página de resultados con información acerca de la cuenta del cliente y vínculos a acciones en la parte superior de la página. Haga clic en el vínculo correspondiente a la acción que desea realizar.

    |Acción|Detalles|
    |----------|------------|
    |**Administrar en nombre de**|Únicamente disponible cuando el cliente le ha concedido permisos como administrador delegado.<br /><br />Este vínculo abre un portal de cuentas de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] a la suscripción del cliente.<br /><br />-   Confirme la suscripción que está administrando visualizando el nombre de la empresa en pantalla, en la parte superior del panel izquierdo.<br />-   Cuando las credenciales de su partner estén configuradas para **Administración limitada** no tendrá acceso a los nodos **Administrar**, **Comprar** o **Dominio** de la suscripción del cliente.<br />-   Si hace clic en un vínculo a una consola disponible, como la consola de administración o el portal de la empresa, se le dirigirá a la consola para su empresa, no a la consola para el cliente.|
    |**Crear solicitud de servicio**|Abre una solicitud de servicio en nombre del cliente.|
    |**Mostrar todos los administradores**|Muestra una lista de todos los administradores de inquilinos de la empresa del cliente.|
    |**Restablecer contraseña**|Restablece la contraseña de la cuenta de usuario del cliente en [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].<br /><br />-   Cuando usted es un administrador global, puede restablecer contraseñas desde el portal de partners.<br />-   Si usted es un administrador limitado, únicamente puede restablecer contraseñas desde el portal de cuentas de clientes.|

## <a name="BKMK_CreateTrials"></a>Crear invitaciones de evaluación y ofertas de compra
Una invitación de evaluación puede incluir una oferta para solo una suscripción de evaluación cada vez.

Las ofertas de compra pueden contener una o más suscripciones, lo cual le permite empaquetar varias suscripciones en una única oferta.

**Las evaluaciones y las ofertas tienen lo siguiente en común:**

-   Al crear una invitación de evaluación o una oferta, [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] crea un mensaje que contiene los detalles. Posteriormente puede personalizar este mensaje y enviarlo a su cliente.

-   Tras personalizar el mensaje, puede hacer clic en **Abrir en correo** para crear automáticamente un mensaje de correo electrónico con los detalles del mensaje. También puede copiar y pegar manualmente el mensaje en un formato de comunicación distinto.

-   Los detalles del mensaje contienen un vínculo con un código incorporado que identifica a su empresa como asesor de suscripción asociado a los servicios que especifique.

-   Puede usar el mismo mensaje para varios clientes. Ningún contenido de la invitación de evaluación o la oferta de compra está asociado a un cliente específico.

-   Cuando un cliente hace clic en el vínculo de los detalles del mensaje, se muestran con la evaluación o la oferta de compra, con los detalles especificados.

-   Un cliente puede aceptar la invitación de evaluación o la oferta de compra sin aceptar una oferta de administración delegada.

Cuando un cliente acepta una oferta desde el vínculo del mensaje, se le dirige a una página de registro estándar y un proceso para la evaluación o la compra del servicio. El vínculo de la página de registro contiene el código incorporado que identifica a su empresa como asesor de la suscripción.

**Al personalizar el mensaje, tenga en cuenta lo siguiente:**

-   Identifíquese como partner autorizado de Microsoft.

-   Haga saber a los clientes que Microsoft les facturará directamente.

-   Indique a los clientes cómo pueden ponerse en contacto con usted si tienen alguna pregunta sobre el servicio o la oferta.

-   Los clientes controlan el número de licencias adquiridas. Una vez que acepten la oferta, podrán cambiar el número de licencias.

-   Si ofrece administración delegada, explique lo que significa y cuáles son sus responsabilidades.

#### Para crear y enviar una invitación de evaluación o una oferta de compra

1.  En la página **Introducción al partner** del portal de partners de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], haga clic en **Enviar invitaciones de evaluación** o **Crear ofertas de compra**.

2.  En el asistente, configure las opciones disponibles:

    -   **Oficina del partner**: si la empresa tiene varias oficinas, seleccione la oficina que desea asociar a esta invitación de evaluación. Si su oficina no aparece en la lista, agregue ubicaciones nuevas en el sitio web [Microsoft Partner Network](http://go.microsoft.com/fwlink/?linkid=235720). Pueden transcurrir 24 horas antes de que las nuevas entradas aparezcan en la lista de **oficinas de partners**.

    -   **Ubicación de uso**: seleccione la ubicación en la que el cliente usará los servicios.

    -   **Suscripciones de evaluación** (para evaluaciones) o **Suscripciones** (para ofertas de compra): la lista de suscripciones disponibles está determinada por la ubicación de uso del país o la región del cliente.

        Para las ofertas de compra, se le pedirá que especifique el número de licencias de usuario tras seleccionar una suscripción.

    -   **Administración delegada**: seleccione esta opción si desea ofrecer administración delegada a su cliente. Los clientes pueden aceptar una oferta o una invitación de evaluación aceptando o sin aceptar la administración delegada.

3.  Cuando haya terminado, haga clic en **Abrir en correo** para abrir un correo electrónico nuevo que contenga el vínculo a la invitación, o copie y pegue manualmente el vínculo en un formato de mensaje que usted elija y posteriormente envíelo al cliente.

    -   Al hacer clic en **Abrir en correo**, si la función Control de cuentas de usuario (UAC) está activada en el equipo, puede que se abra una página web en blanco además del mensaje de correo electrónico.

    -   Anote el **id. de la oferta**. Puede usar este id. para realizar un seguimiento de la oferta en el panel Microsoft Online Services Partner Commerce.

## <a name="BKMK_OfferAdmin"></a>Ofrecer administración delegada
Como partner de Microsoft autorizado, puede ofrecer la administración delegada. Esto significa que puede ofrecerse para administrar la suscripción de una empresa en nombre de la empresa.

Administradores delegados:

-   **Son administradores de inquilinos** que pueden utilizar el portal de cuentas para realizar tareas sencillas, como agregar usuarios y restablecer contraseñas para el cliente, o tareas más técnicas, como agregar un dominio a la cuenta del cliente.

-   **No son administradores de servicio** y por lo tanto no tienen acceso a la administración de las operaciones cotidianas del cliente, como la implementación de software, tal y como están configuradas en la consola de administración.

Antes de poder administrar la suscripción de un cliente, el [Administrar las relaciones con los partners](../Topic/Maintain-Microsoft-Intune.md#BKMK_ManagePartners). Para obtener la aprobación del cliente, puede enviar una oferta de administración delegada, que el cliente puede aceptar. Un cliente puede aceptar la invitación de evaluación o la oferta de compra sin aceptar su oferta de administración delegada.

-   Puede ofrecer la administración delegada cuando crea invitaciones de prueba y ofertas de compra. Esto puede ayudarle a establecer una sólida relación con su cliente desde el principio.

-   Puede ofrecer la administración delegada a un cliente que previamente ha comprado una suscripción.

Cuando un cliente ha aceptado su oferta y configura su id. de partner como administrador delegado, los usuarios de su empresa que tienen permisos para obtener acceso a la empresa del cliente pueden proporcionar servicio como administrador delegado.

#### Para ofrecer la administración delegada a una cuenta existente

1.  En la página **Introducción al partner** del portal de partners de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], haga clic en **Enviar ofertas de administración delegada**.

2.  Haga clic en **Abrir en correo** o copie el vínculo para la oferta y péguelo manualmente en un mensaje de correo electrónico.

3.  Cuando su cliente reciba la oferta que contiene el vínculo, puede seguirlo para autorizarle como administrador delegado.

También puede incluir una oferta de administración delegada cuando cree una suscripción de evaluación o una oferta de compra mediante la selección de **Incluir autorización para administración delegada** cuando seleccione las opciones para la evaluación o la oferta.

## <a name="BKMK_AssignDelAdmin"></a>Conceder permiso a los usuarios para actuar como administradores delegados
En el portal de cuentas de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] de su suscripción, puede configurar sus usuarios para que tengan acceso administrativo a las empresas a las cuales proporciona soporte:

-   Puede hacer esta configuración exclusiva de partner cuando crea nuevas cuentas de usuario o cuando edita cuentas de usuario existentes.

-   No es necesario que los usuarios sean administradores de su empresa para que se les conceda acceso administrativo a las empresas a las cuales proporciona servicio.

Los usuarios que son administradores delegados pueden:

-   Obtener acceso a su portal de partners

-   Buscar usuarios y dominios de los clientes

-   Crear invitaciones de evaluación y ofertas de compra, y ofrecer administración delegada a los clientes

-   Administrar las suscripciones de los clientes conforme al rol asignado a su cuenta de usuario

Para obtener información acerca de cómo configurar usuarios administrativos, consulte [Task 5: Assign administrative users](../Topic/Get-started-with-a-paid-subscription-to-Microsoft-Intune.md#BKMK_AssignAdmins). Para obtener información sobre los roles y permisos de administrador, consulte el tema de [asignación de funciones de administrador](http://technet.microsoft.com/library/hh967622).

#### Para configurar un usuario para ser administrador delegado

1.  En el [portal de cuentas de Microsoft Intune](https://account.manage.microsoft.com/) de su empresa, haga clic en **Usuarios**.

2.  Seleccione la cuenta de usuario que desea configurar y, a continuación, haga clic en **Editar**.

3.  En la página Configuración, en **Asignar acceso administrativo a las empresas a las que proporciona soporte**, haga clic en **Sí** y seleccione el rol adecuado para esta cuenta:

    -   **Administración completa**: concede al usuario privilegios equivalentes al rol de administrador global para las empresas a las cuales proporciona soporte.

    -   **Administración limitada**: concede al usuario privilegios equivalentes al rol de administrador de contraseñas para las empresas a las cuales proporciona soporte.

4.  Haga clic en **Guardar** para completar el procedimiento.

Los permisos como administrador delegado se aplican exclusivamente para administrar una suscripción de cliente. No conceden al usuario permisos de administrador de inquilinos o administrador de servicios para la suscripción de su empresa.

## <a name="BKMK_Administer"></a>Administrar un cliente como administrador delegado
Cuando un cliente ha configurado su id. de partner como administrador delegado, sus usuarios configurados como administradores delegados pueden administrar la suscripción del cliente.

**Cuando usted administra la suscripción de un cliente:**

-   Únicamente puede acceder al portal de cuentas del cliente

-   Si mientras navega sale del portal de cuentas del cliente, finaliza la sesión de administración para el cliente

-   Si utiliza el botón Atrás en el explorador para intentar volver al portal del cliente, en lugar de ello será devuelto al portal de cuentas de su propia suscripción

-   Para volver al portal de cuentas para el cliente, debe iniciar la sesión en su portal de partners, buscar y posteriormente administrar el cliente seleccionado

#### Para administrar un cliente

1.  Inicie la sesión en el portal de partners de su empresa.

2.  En la página **Introducción al partner**, haga clic en **Búsqueda de usuario o dominio** y posteriormente busque la suscripción del cliente que quiere administrar.

3.  Una vez encontrado el cliente, haga clic en **Administrar en nombre de**.

Cuando se abra el portal de cuentas de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], confirme que está trabajando con la cuenta del cliente visualizando el nombre de la empresa en la esquina superior izquierda del panel de la izquierda; posteriormente, lleve a cabo las tareas de administración necesarias.

