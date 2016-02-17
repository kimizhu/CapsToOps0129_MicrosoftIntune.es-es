---
title: Usar acceso condicional con Intune y Configuration Manager
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5b021c5a-b7a4-4ea5-957d-d6f2cdc1812c
---
# Usar acceso condicional con Intune y Configuration Manager
En esta solución, ya usa System Center Configuration Manager y Microsoft Exchange Server (local, Exchange Online o una implementación híbrida de ambos) en su empresa para administrar el acceso al correo electrónico. Esta solución combina su entorno existente de Configuration Manager con Intune para administrar el acceso al correo electrónico en todos los tipos de dispositivos, independientemente de su ubicación, de forma segura.

> [!TIP]
> Obtenga una copia descargable de este tema completo en la [Galería de TechNet](https://gallery.technet.microsoft.com/Deploying-Enterprise-16499404).

## <a name="ExchangeOnPrem"></a>Exchange Server local
Si ya usa System Center Configuration Manager y Exchange en la infraestructura local, puede incorporar Intune para administrar el acceso al correo electrónico y proteger los datos de correo electrónico en dispositivos móviles. El proceso de alto nivel para implementar esta solución es la siguiente:

-   Configure el Intune Exchange Connector local con la consola de Configuration Manager, que permite que Configuration Manager se comunique con el Exchange Server que aloja los buzones de los dispositivos móviles.

-   Ejecute una sincronización completa del conector de Exchange Server para detectar a los usuarios y hacer un inventario de todos los identificadores de Exchange ActiveSync (EASID) para dispositivos móviles que se conectan al Exchange Server local.

-   Cree recopilaciones de usuarios para grupos de usuarios a los que se dirigirá la directiva de acceso condicional, o que quedarán exentos. A continuación, cree las directivas de cumplimiento que definen las reglas y los valores de configuración que un dispositivo debe respetar para que se le considerarse conforme a las directivas de acceso condicional.

-   Para empezar, aplique el acceso condicional.

### El acceso condicional controla el flujo de Exchange Server local
Este diagrama muestra el flujo de control para los clientes que intentan obtener acceso al correo electrónico de Exchange local.

![](../Image/Hybrid_on-prem_CA_architecture.png)

-   Microsoft Intune: administra las directivas de acceso condicional y de cumplimiento para el dispositivo

-   Microsoft Azure Active Directory: autentica al usuario y ofrece el estado de cumplimiento del dispositivo

-   Configuration Manager: administra la inscripción de dispositivos y ofrece informes

-   Exchange local: aplica el acceso al correo electrónico basado en el estado del dispositivo

### Requisitos previos
Antes de continuar, asegúrese de que su entorno incluya estos requisitos para implementar esta solución.

> [!NOTE]
> Si ya ha configurado Configuration Manager para administrar dispositivos móviles mediante el servicio Intune, puede continuar con [Pasos de implementación](#DeploySteps).

-   Compruebe que cumple los [requisitos de hardware del conector local](https://technet.microsoft.com/en-us/library/dn646950.aspx#BKMK_ExchanceConnectorReqs).

-   Compruebe que está ejecutando System Center 2012 R2 Configuration Manager SP1 con actualización acumulativa 1 o posterior.

-   Asegúrese de que el [extremo de servicios Web Exchange (EWS) ](https://technet.microsoft.com/library/hh529912(v=exchg.150).aspx)esté configurado correctamente para la detección. Si es necesario, póngase en contacto con el equipo de soporte técnico de Configuration Manager para obtener una herramienta que pueda ayudar a identificar problemas de conexión de EWS. EWS permite a los programadores interactuar con los buzones y el contenido de Exchange con HTTP estándar.

-   Instale y asigne los servicios de Exchange en un [certificado digital válido ](https://technet.microsoft.com/library/dd351044(v=exchg.150).aspx) adquirido en una entidad de certificación pública confianza.

-   Configure una cuenta (administrador local o de dominio) con permisos para ejecutar los siguientes cmdlets de Exchange Server:

    **Clear-ActiveSyncDevice**

    **Get-ActiveSyncDevice**

    **Get-ActiveSyncDeviceAccessRule**

    **Get-ActiveSyncDeviceStatistics**

    **Get-ActiveSyncMailboxPolicy**

    **Get-ActiveSyncOrganizationSettings**

    **Get-ExchangeServer**

    **Get-Recipient**

    **Set-ADServerSettings**

    **Set-ActiveSyncDeviceAccessRule**

    **Set-ActiveSyncMailboxPolicy**

    **Set-CASMailbox**

    **New-ActiveSyncDeviceAccessRule**

    **New-ActiveSyncMailboxPolicy**

    **Remove-ActiveSyncDevice**

> [!IMPORTANT]
> Si intenta instalar o usar el conector de Exchange Server sin los cmdlets necesarios, verá un error con el mensaje Invoking cmdlet &lt;cmdlet&gt; failed en el archivo EasDisc.log en el equipo de servidor de sitio.

### <a name="DeploySteps"></a>Pasos de implementación
Siga estos pasos para implementar la solución local de Exchange:

#### Paso 1: asegúrese de que esté instalado el rol de conector de Intune.
Asegúrese de que esté instalado el rol de conector de Intune para que Configuration Manager pueda interactuar con Intune. Para más información, vea [Administrar dispositivos móviles con Configuration Manager e Intune](https://technet.microsoft.com/en-us/library/JJ884158.aspx).

#### Paso 2: para instalar y configurar un conector de Exchange Server.
Configuration Manager solo admite un conector en una organización de Exchange.

> [!IMPORTANT]
> Antes de instalar el conector de Exchange Server, confirme que Configuration Manager es compatible con la versión de Microsoft Exchange que está usando. Para más información, vea [Configuraciones compatibles en Configuration Manager](https://technet.microsoft.com/en-us/library/gg682077.aspx).

Siga los pasos de [Cómo administrar dispositivos móviles con Configuration Manager y Exchange](https://technet.microsoft.com/en-us/library/gg682001.aspx) para instalar y configurar el conector de Exchange Server.

#### Paso 3: ejecute una sincronización completa para detectar a los usuarios.

1.  En la consola de Configuration Manager, haga clic en **Administración**, expanda **Configuración de jerarquía** y, después, seleccione **Conectores de Exchange Server**.

2.  Seleccione el conector de Exchange Server que instaló en el paso 2.

3.  Haga clic en **Sincronizar ahora**.

    ![](../Image/HybridOnpremRunFullSync.png)

Esta sincronización completa puede tardar varias horas en completarse, según el número de dispositivos. Se ejecutará una sincronización completa una vez cada 24 horas de forma predeterminada. Una sincronización delta detecta las conexiones del dispositivo desde la última sincronización completa y se produce según el intervalo establecido durante la instalación del conector de Exchange Server. Esto garantiza que los usuarios nuevos y los usuarios nuevos de Exchange se detecten rápidamente y que se pueda aplicar el acceso condicional.

Con la herramienta de registro de seguimiento de Configuration Manager, puede abrir el archivo EasDisc.log (ubicado en la carpeta **Microsoft Configuration Manager/Logs** donde instaló Configuration Manager) para comprobar si el conector está activo y si consulta las conexiones del dispositivo. Una vez finalizada la sincronización completa, se hará un inventario de todos los identificadores de Exchange ActiveSync (EASID) de los dispositivos móviles que se conectan a Exchange de forma local.

#### Paso 4: creación de recopilaciones de usuarios.
Determine los grupos de usuarios de Intune a los que se dirigirá la directiva de acceso condicional. Luego, cree recopilaciones de usuarios para grupos de usuarios a los que se dirigirá la directiva de acceso condicional, o que quedarán exentos. Especificará estos grupos más adelante, cuando aplique el acceso condicional.

Siga los pasos de [Cómo crear recopilaciones en Configuration Manager](https://technet.microsoft.com/en-us/library/gg712295.aspx) crear recopilaciones de usuario.

#### <a name="Step_5"></a>Paso 5: cree directivas de cumplimiento y distribúyalas a los usuarios.
Las directivas de cumplimiento definen las reglas y los valores de configuración que un dispositivo debe cumplir para que se le considere conforme a las directivas de acceso condicional. Siga los pasos de [Directivas de cumplimiento en Configuration Manager](https://technet.microsoft.com/en-us/library/mt131417.aspx) para crear directivas de cumplimiento.

> [!NOTE]
> Si quiere tener la capacidad de quitar todos los mensajes de correo corporativo de un dispositivo iOS cuando este deje de formar parte de la empresa, tiene que crear e implementar un perfil de correo electrónico. Luego, establezca una directiva de cumplimiento que especifique que Intune administra los perfiles de correo electrónico. Debe implementar el perfil de correo electrónico en el mismo conjunto de usuarios al que va dirigido esta directiva de cumplimiento.
> 
> ![](../Image/HybridOnpremExchSrvrWizard6.PNG)
> 
> Si se especifica esta directiva de cumplimiento, un usuario que ya haya configurado su cuenta de correo electrónico tendrá que eliminarla manualmente y, luego, Intune la agregará de nuevo en el proceso de registro descrito en [Experiencia de acceso condicional del usuario final](../Topic/End-user-experience-of-conditional-access.md).

Después de crear la directiva de cumplimiento, seleccione el nombre de dicha directiva en la lista y haga clic en **Implementar**.

#### Paso 6: configure la directiva de acceso condicional.
En primer lugar, decida cómo y cuándo desea aplicar el acceso condicional y los empleados que se verán afectados. Luego, siga los pasos descritos en [Acceso condicional para correo electrónico de Exchange en Configuration Manager](https://technet.microsoft.com/en-us/library/mt131421.aspx) para configurar la directiva de acceso condicional de Exchange local.

#### Paso 7: supervise las inscripciones y aplique el acceso condicional.
Si ya tiene un número significativo de usuarios inscritos en Intune y compatibles, puede empezar a aplicar el acceso condicional a unos 500 usuarios al día. En total, se emplearán unos 4 o 5 meses con los 70.000 usuarios y se podrán solucionar los posibles problemas que surgirían si no se evitase que demasiados usuarios accediesen al correo electrónico al mismo tiempo.

Si no hay muchos usuarios ya inscritos en Intune, el acceso condicional les ofrece una experiencia guiada para la inscripción, como se describe en [Experiencia de acceso condicional del usuario final](../Topic/End-user-experience-of-conditional-access.md).

### Pasos de comprobación
Con la herramienta de registro de seguimiento de Configuration Manager, abra el archivo EasDisc.log (que se encuentra en la carpeta Microsoft Configuration Manager/Logs, donde se haya instalado Configuration Manager). Busque el archivo de registro del "Conector de Exchange" para obtener información sobre si se está ejecutando el conector de Exchange y cuántos dispositivos están conectados.

![](../Image/HybridOnpremEasDiscLogSample.PNG)

La herramienta de registro de seguimiento de Configuration Manager se incluye en el [el kit de herramientas de System Center 2012 R2 Configuration Manager](http://www.microsoft.com/en-us/download/details.aspx?id=36213).

### Generación de informes
Puede usar la consola de Configuration Manager para ver información específica sobre los dispositivos detectados por el conector de Exchange. Para los dispositivos a los que se aplica el acceso condicional, puede ver el estado actual de cada dispositivo, la última conexión del dispositivo con el servidor de Exchange, etc.

En la consola de Configuration Manager, haga clic en **Activos y compatibilidad** y en **Dispositivos**. Puede ver el estado actual de cada dispositivo (Bloqueado o Permitido) en la columna **estado de acceso de Exchange**. Agregue esta columna si aún no aparece al hacer clic con el botón secundario en el área de la barra de título de la columna. También puede ver la hora de la última sincronización correcta para cada dispositivo, indicada por Exchange, agregando la columna **Hora de última sincronización correcta con Exchange Server** .

![](../Image/HybridOnpremVerifyDevicesState.png)

Si está ejecutando SQL Server Reporting Services (SSRS), puede ver un informe de acceso condicional que muestre el estado de cumplimiento de los dispositivos, si hay un conector de Exchange instalado y activo, y el estado de acceso de EAS. También ofrecerá información sobre el registro de Active Directory, la activación de EAS y el propietario del dispositivo.

![](../Image/HybridReports_CA.png)

Para ver los informes de SSRS, debe tener un rol de informes instalado en el servidor principal:

1.  En Configuration Manager, haga clic en **Administración**, **Configuración de jerarquía**, **Configuración del sitio**, y, por último, **Servidores y roles del sistema de sitios**.

2.  Seleccione un servidor y haga clic en **Agregar rol de sistema de sitio** para abrir el asistente Agregar rol de sistema de sitio.

3.  En la página Selección de rol de sistema, active la casilla **Punto de servicios de informes**. El punto de servicios de informes muestra los informes relacionados con la administración de cliente.

4.  Haga clic en **Siguiente**.

A continuación, se muestra el estado de implementación de la directiva de configuración:

![](../Image/HybridReportsDeploymentStatus.png)

#### Latencia
Un dispositivo se bloquea en cuanto lo detecta el conector de Exchange. La latencia de bloqueo depende de los intervalos configurados para la sincronización completa y la sincronización diferencial y el tiempo entre estos intervalos cuando el dispositivo se conecta al servidor de Exchange. De forma predeterminada, una sincronización completa se produce cada 24 horas, la sincronización diferencial se produce cada 240 minutos. Durante este período de latencia, un dispositivo podría considerarse conforme.

## <a name="ExchangeOnline"></a>Exchange Online
Si ya usa System Center Configuration Manager y Exchange Online, puede incorporar Intune para administrar el acceso al correo electrónico y proteger los datos de correo electrónico en dispositivos móviles. El proceso de alto nivel para implementar esta solución es la siguiente:

-   Cree las directivas de cumplimiento que definen las reglas y los valores de configuración que un dispositivo debe cumplir para que se considere conforme a las directivas de acceso condicional.

-   Para empezar, aplique el acceso condicional.

-   Opcionalmente, configure el conector de Exchange Server para Exchange Online. Este conector solo se necesita con fines informativos. No es necesario para habilitar el acceso condicional.

### Flujo de control de acceso condicional para Exchange Online
Este diagrama muestra el flujo de control para los clientes que intentan obtener acceso al correo electrónico en Exchange Online. A y B pueden realizarse antes de aplicar el acceso condicional.

![](../Image/Hybrid_Exchange-Online_CA_architecture.png)

-   Microsoft Intune: administra las directivas de acceso condicional y de cumplimiento para el dispositivo

-   Microsoft Azure Active Directory: autentica al usuario y ofrece el estado de cumplimiento del dispositivo

-   Configuration Manager: administra la inscripción de dispositivos y ofrece informes, si se habilita esa opción

-   Exchange Online: aplica el acceso al correo electrónico según el estado del dispositivo

### Requisitos previos
Antes de continuar, asegúrese de que su entorno incluya estos requisitos para implementar esta solución.

-   Instale y asigne los servicios de Exchange en un [certificado digital válido ](https://technet.microsoft.com/library/dd351044(v=exchg.150).aspx) adquirido en una entidad de certificación pública confianza.

-   Compruebe que está ejecutando System Center 2012 R2 Configuration Manager SP1 con actualización acumulativa 1 o posterior.

-   Configure una cuenta (administrador local o de dominio) con permisos para ejecutar los siguientes cmdlets de Exchange Server:

    **Clear-ActiveSyncDevice**

    **Get-ActiveSyncDevice**

    **Get-ActiveSyncDeviceAccessRule**

    **Get-ActiveSyncDeviceStatistics**

    **Get-ActiveSyncMailboxPolicy**

    **Get-ActiveSyncOrganizationSettings**

    **Get-ExchangeServer**

    **Get-Recipient**

    **Set-ADServerSettings**

    **Set-ActiveSyncDeviceAccessRule**

    **Set-ActiveSyncMailboxPolicy**

    **Set-CASMailbox**

    **New-ActiveSyncDeviceAccessRule**

    **New-ActiveSyncMailboxPolicy**

    **Remove-ActiveSyncDevice**

### Pasos de implementación
Siga estos pasos para implementar la solución Exchange Online:

#### Paso 1: cree directivas de cumplimiento e impleméntelas a los usuarios.
Las directivas de cumplimiento definen las reglas y los valores de configuración que un dispositivo debe cumplir para que se le considere conforme a las directivas de acceso condicional. Siga los pasos de [Directivas de cumplimiento en Configuration Manager](https://technet.microsoft.com/en-us/library/mt131417.aspx)para crear directivas de cumplimiento.

> [!NOTE]
> Si quiere tener la capacidad de quitar todos los mensajes de correo corporativo de un dispositivo iOS cuando este deje de formar parte de la empresa, tiene que crear e implementar un perfil de correo electrónico. Luego, establezca una directiva de cumplimiento que especifique que Intune administra los perfiles de correo electrónico. Debe implementar el perfil de correo electrónico en el mismo conjunto de usuarios al que va dirigido esta directiva de cumplimiento.
> 
> ![](../Image/HybridOnpremExchSrvrWizard6.PNG)
> 
> Si se especifica esta directiva de cumplimiento, un usuario que ya haya configurado su cuenta de correo electrónico tendrá que eliminarla manualmente y, luego, Intune la agregará de nuevo en el proceso de registro descrito en [Experiencia de acceso condicional del usuario final](../Topic/End-user-experience-of-conditional-access.md).

Después de crear la directiva de cumplimiento, seleccione el nombre de dicha directiva en la lista y haga clic en **Implementar**.

#### Paso 2: configure la directiva de acceso condicional.
En primer lugar, decida cómo y cuándo desea aplicar el acceso condicional y los empleados que se verán afectados. Luego, siga los pasos descritos en [Acceso condicional para correo electrónico de Exchange en Configuration Manager](https://technet.microsoft.com/en-us/library/mt131421.aspx) para habilitar la directiva de acceso condicional para Exchange Online.

> [!NOTE]
> Debe configurar la directiva de acceso condicional en la consola de Intune. Los siguientes pasos empiezan por el acceso a la consola de Intune a través de Configuration Manager. Si se le solicita, inicie sesión con las mismas credenciales que usó para configurar el conector entre Configuration Manager e Intune.

#### Paso 3: (*Opcional*) instale y configure un conector de Exchange Server.
Configuration Manager solo admite un conector en una organización de Exchange.

> [!IMPORTANT]
> Antes de instalar el conector de Exchange Server, confirme que Configuration Manager es compatible con la versión de Microsoft Exchange que está usando. Para más información, vea [Configuraciones compatibles en Configuration Manager](https://technet.microsoft.com/en-us/library/gg682077.aspx).

Siga los pasos de [Cómo administrar dispositivos móviles con Configuration Manager y Exchange](https://technet.microsoft.com/en-us/library/gg682001.aspx) para instalar y configurar el conector de Exchange Server.

### Pasos de comprobación
Si ha configurado el conector opcional de Exchange Server para esta solución, puede usar la herramienta de registro de seguimiento de Configuration Manager para abrir el archivo EasDisc.log (que se encuentra en la carpeta Microsoft Configuration Manager/Logs donde se ha instalado Configuration Manager). Busque el archivo de registro del "Conector de Exchange" para obtener información sobre si se está ejecutando el conector de Exchange y cuántos dispositivos están conectados.

![](../Image/HybridOnpremEasDiscLogSample.PNG)

La herramienta de registro de seguimiento de Configuration Manager se incluye en el [el kit de herramientas de System Center 2012 R2 Configuration Manager](http://www.microsoft.com/en-us/download/details.aspx?id=36213).

### Generación de informes
Si ha configurado el conector opcional de Exchange Server, puede usar la consola de Configuration Manager para ver información específica sobre los dispositivos detectados por el conector de Exchange. Para los dispositivos a los que se aplica el acceso condicional, puede ver el estado actual de cada dispositivo, la última conexión del dispositivo con el servidor de Exchange, etc.

En la consola de Configuration Manager, haga clic en **Activos y compatibilidad** y en **Dispositivos**. Puede ver el estado actual de cada dispositivo (En cuarentena o permitido) en la columna **Estado de acceso de Exchange**. Agregue esta columna si aún no aparece al hacer clic con el botón secundario en el área de la barra de título de la columna. También puede ver la hora de la última sincronización correcta para cada dispositivo, indicada por Exchange, agregando la columna **Hora de última sincronización correcta con Exchange Server** .

![](../Image/HybridOnpremVerifyDevicesState.png)

Si está ejecutando SQL Server Reporting Services (SSRS), puede ver un informe de acceso condicional que muestre el estado de cumplimiento de los dispositivos, si hay un conector de Exchange instalado y activo, y el estado de acceso de EAS. También ofrecerá información sobre el registro de Active Directory, la activación de EAS y el propietario del dispositivo.

![](../Image/HybridReports_CA.png)

Para ver los informes de SSRS, debe tener un rol de informes instalado en el servidor principal:

1.  En Configuration Manager, haga clic en **Administración &gt; Configuración de jerarquía &gt; Configuración del sitio &gt; Servidores y roles del sistema de sitios**.

2.  Seleccione un servidor y haga clic en **Agregar rol de sistema de sitio** para abrir el asistente Agregar rol de sistema de sitio.

3.  En la página Selección de rol de sistema, active la casilla **Punto de servicios de informes**. El punto de servicios de informes muestra los informes relacionados con la administración de cliente.

4.  Haga clic en **Siguiente**.

A continuación, se muestra el estado de implementación de la directiva de configuración:

![](../Image/HybridReportsDeploymentStatus.png)

#### Latencia
A los dispositivos que usan la autenticación moderna se les aplica de inmediato el acceso condicional. Para dispositivos que se conectan a través del protocolo EAS, puede haber un intervalo de tiempo de seis horas antes de que se aplique el acceso condicional, según la configuración predeterminada. Durante ese tiempo, un dispositivo podría considerarse conforme.

## Coexistencia de Exchange Server local y Exchange Online
Un entorno en el que tanto Exchange local como Exchange Online se usen para administrar los perfiles de correo electrónico ofrece a las empresas la capacidad de ampliar la experiencia con múltiples características y el control administrativo de los que ya disponen con la organización local existente de Microsoft Exchange en la nube. Este tipo "híbrido" de implementación ofrece la apariencia y el funcionamiento sin problemas de una sola organización de Exchange entre una organización de Exchange Server 2013 local y Exchange Online en Microsoft Office 365. Además, este tipo de implementación puede servir como un paso intermedio para pasar completamente a una organización de Exchange Online.

Si ya usa Configuration Manager junto con una coexistencia de Exchange local y Exchange Online, puede incorporar Intune para administrar el acceso al correo electrónico y proteger los datos de correo electrónico en dispositivos móviles. Para implementar esta solución, siga las instrucciones de arriba para implementar cada solución por separado.

### Requisitos previos
Para configurar un tipo de coexistencia del entorno que implemente Exchange local y Exchange Online, la organización de Exchange existente debe cumplir determinados requisitos. Si no se cumplen estos requisitos, no se podrán completar los pasos necesarios para configurar una implementación híbrida entre la organización de Exchange local y la organización de Exchange Online de Microsoft Office 365.

Vea [Requisitos previos de implementación híbrida](https://technet.microsoft.com/en-us/library/hh534377.aspx) para revisar los requisitos para crear y configurar este tipo de entorno.

### Pasos de implementación
Para implementar una solución de coexistencia, siga los pasos de arriba para implementar las soluciones [Exchange Server local](#ExchangeOnPrem) y [Exchange Online](#ExchangeOnline).

## Vea también
[Aprenda a implementar una solución para proteger los documentos y correos electrónicos de su empresa](../Topic/Learn-how-to-deploy-a-solution-for-protecting-company-email-and-documents.md)
[Experiencia de acceso condicional del usuario final](../Topic/End-user-experience-of-conditional-access.md)

