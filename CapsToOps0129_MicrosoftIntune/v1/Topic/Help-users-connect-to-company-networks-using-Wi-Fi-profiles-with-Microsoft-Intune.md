---
title: Ayudar a los usuarios a conectarse a las redes de la compa&#241;&#237;a mediante perfiles de Wi-Fi con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0b1b86ed-2e80-474d-8437-17dd4bc07b55
---
# Ayudar a los usuarios a conectarse a las redes de la compa&#241;&#237;a mediante perfiles de Wi-Fi con Microsoft Intune
Use perfiles de Wi-Fi de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] para implementar la configuración de red inalámbrica para los usuarios y dispositivos de la organización. Esta configuración simplifica la conexión a redes inalámbricas para los usuarios finales.

Por ejemplo:

-   Instala una nueva red Wi-Fi denominada **Contoso Wi-Fi** y desea aprovisionar todos los dispositivos que ejecutan el sistema operativo iOS con la configuración necesaria para conectarse a esta red.

-   Crea un perfil de Wi-Fi que contiene la configuración necesaria para conectarse a la red inalámbrica **Contoso Wi-Fi**.

-   Ahora puede implementar este perfil en todos los usuarios con dispositivos iOS.

-   Los usuarios encuentran la nueva red **Contoso Wi-Fi** en la lista de redes inalámbricas y pueden conectarse fácilmente a ella.

Puede implementar perfiles de Wi-Fi en las siguientes plataformas:

-   Android 4.0 y versiones posteriores

-   iOS 7.1 y versiones posteriores

-   Mac OS X 10.9 y versiones posteriores

Además, en el caso de dispositivos que ejecutan Windows 8.1 y versiones posteriores, puede importar un perfil de configuración de Wi-Fi que se haya exportado previamente a un archivo. Para obtener más información, consulte [Importar un perfil de configuración de Wi-Fi (solo Windows 8.1 y posterior)](../Topic/Help-users-connect-to-company-networks-using-Wi-Fi-profiles-with-Microsoft-Intune.md#BKMK_Import).

## Pasos para crear e implementar un perfil de Wi-Fi

### Paso 1: Crear un perfil de Wi-Fi y proporcionar información general

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Directiva** &gt; **Agregar directiva**.

2.  Seleccione uno de los siguientes tipos de directiva y haga clic en **Crear directiva**:

    -   **Perfil de Wi-Fi (Android 4 y versiones posteriores)**

    -   **Perfil de Wi-Fi (iOS 7.1 y versiones posteriores)**

    -   **Perfil de Wi-Fi (Mac OS X 10.9 y versiones posteriores)**

    No hay ninguna configuración recomendada para este tipo de directiva. Debe crear una directiva personalizada.

3.  Especifique los valores generales siguientes:

    |Configuración|Más información|
    |-----------------|-------------------|
    |**Nombre**|Escriba un nombre único para el perfil de Wi-Fi para que sea más fácil identificarlo en la consola de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Descripción**|Proporcione una descripción del perfil de Wi-Fi para que sea más fácil encontrarlo.|

### Paso 2: Establecer la configuración de conexión de red
Especifique los valores de **Conexiones de red**:

|Configuración|Más información|
|-----------------|-------------------|
|**Nombre de red**|Especifique un nombre descriptivo para la red inalámbrica. Se trata del nombre que se muestra en el dispositivo del usuario cuando elige una red inalámbrica.|
|**SSID (identificador de conjunto de servicios)**|Especifique el SSID de la red inalámbrica a la que desea conectar los dispositivos. El SSID distingue mayúsculas de minúsculas y no se mostrará a los usuarios.|
|**Conectarse automáticamente cuando esta red esté dentro del alcance**|Seleccione esta opción para conectar dispositivos automáticamente a la red inalámbrica cuando esta se encuentre dentro del alcance.|
|**Conectarse cuando la red no está difundiendo su nombre (SSID)**|Seleccione esta opción para permitir que los dispositivos se conecten a la red cuando no está visible en la lista de redes (porque está oculta y no está difundiendo su nombre).|

### Paso 3: Configurar la seguridad
Establezca la **Configuración de seguridad** para la plataforma seleccionada. Las opciones disponibles dependen de los tipos de seguridad que seleccione.

#### En el caso de dispositivos Android

|Nombre de la configuración|Más información|Se debe usar cuando:|
|------------------------------|-------------------|------------------------|
|**Tipo de seguridad**|Seleccione el protocolo de seguridad de la red inalámbrica:<br /><br />-   **WPA-Enterprise/WPA2-Enterprise**<br />-   **Sin autenticación (sistema abierto)** si la red no es segura.|Siempre|
|**Tipo de EAP**|Elija el tipo Protocolo de autenticación extensible (EAP) que se usa para autenticar conexiones inalámbricas seguras:<br /><br />-   **EAP-TLS**<br />-   **PEAP**<br />-   **EAP-TTLS**|Seleccionó el tipo de seguridad **WPA-Enterprise/WPA2-Enterprise**.|
|**Seleccionar certificados raíz para la validación del servidor**|Haga clic en **Seleccionar** y elija el perfil de certificado raíz de confianza que se usa para autenticar la conexión. **Important:** Para crear el perfil de certificado raíz de confianza, consulte [Habilitar el acceso a los recursos de empresa mediante perfiles de certificados con Microsoft Intune](../Topic/Enable-access-to-company-resources-using-certificate-profiles-with-Microsoft-Intune.md).|Se seleccionó cualquier **Tipo de EAP**.|
|**Método de autenticación**|Seleccione el método de autenticación para la conexión:<br /><br />-   **Certificados** para especificar el certificado de cliente<br />-   **Nombre de usuario y contraseña** para especificar otro método de autenticación|El **Tipo de EAP** es **PEAP** o **EAP-TTLS**.|
|**Seleccionar un método no EAP para la autenticación (identidad interna)**|Seleccione cómo se autenticará la conexión:<br /><br />-   **Ninguno**<br />-   **Contraseña no cifrada (PAP)**<br />-   **Protocolo de autenticación de desafío mutuo (CHAP)**<br />-   **Microsoft CHAP (MS-CHAP)**<br />-   **Microsoft CHAP versión 2 (MS-CHAP v2)**<br /><br />Las opciones disponibles dependen del tipo de EAP seleccionado.|El **Método de autenticación** es **Nombre de usuario y contraseña**.|
|**Habilitar privacidad de identidad (identidad externa)**|Especifique el texto que se envía como respuesta a una solicitud de identidad EAP. Este texto puede ser cualquier valor. Durante la autenticación, esta identidad anónima se envía inicialmente, seguida de la identificación real enviada en un túnel seguro.|El **Tipo de EAP** es **PEAP** o **EAP-TTLS**.|
|**Seleccionar un certificado de cliente para la autenticación de cliente (certificado de identidad)**|Haga clic en **Seleccionar** y elija el perfil de certificado SCEP que se usa para autenticar la conexión. **Important:** Para crear un perfil de certificado SCEP, consulte [Habilitar el acceso a los recursos de empresa mediante perfiles de certificados con Microsoft Intune](../Topic/Enable-access-to-company-resources-using-certificate-profiles-with-Microsoft-Intune.md).|El tipo de seguridad es **WPA-Enterprise/WPA2-Enterprise** y se selecciona cualquier **Tipo de EAP**.|

#### Para dispositivos iOS y Mac OS X

|Nombre de la configuración|Más información|Se debe usar cuando:|
|------------------------------|-------------------|------------------------|
|**Tipo de seguridad**|Seleccione el protocolo de seguridad de red inalámbrica:<br /><br />-   **WPA-Personal/WPA2-Personal**<br />-   **WPA-Enterprise/WPA2-Enterprise**<br />-   **WEP**<br />-   **Sin autenticación (sistema abierto)** si la red no es segura.|Siempre|
|**Tipo de EAP**|Elija el tipo Protocolo de autenticación extensible (EAP) que se usa para autenticar conexiones inalámbricas seguras:<br /><br />-   **EAP-TLS**<br />-   **PEAP**<br />-   **EAP-TLS**<br />-   **EAP-AST**<br />-   **LEAP**<br />-   **EAP-SIM**|Seleccionó un tipo de seguridad de **WPA-Enterprise/WPA2-Enterprise**.|
|**Nombres de certificado de servidor de confianza**|Seleccione el perfil de certificado raíz de confianza que se usa para autenticar la conexión. **Important:** Para crear el perfil de certificado raíz de confianza, consulte [Habilitar el acceso a los recursos de empresa mediante perfiles de certificados con Microsoft Intune](../Topic/Enable-access-to-company-resources-using-certificate-profiles-with-Microsoft-Intune.md).|Seleccionó un tipo de EAP de **EAP-TLS**, **PEAP**, **EAP-TTLS** o **EAP-FAST**.|
|**Usar credenciales de acceso protegido (PAC)**|Seleccione esta opción para usar credenciales de acceso protegido para establecer un túnel autenticado entre el cliente y el servidor de autenticación. Si está presente, se utiliza un archivo PAC existente.|El **Tipo de EAP** es **EAP-FAST**.|
|**Aprovisionar PAC**|Aprovisiona el archivo PAC en los dispositivos.<br /><br />Cuando se usa, también puede seleccionar **Aprovisionar PAC de forma anónima** para asegurarse de que el archivo PAC se aprovisione sin autenticar el servidor.|Se seleccionó **Usar credenciales de acceso protegido (PAC)**.|
|**Método de autenticación**|Seleccione el método de autenticación que se usa para la conexión:<br /><br /><ul><li>**Certificados** para especificar el certificado de cliente</li><li>**Nombre de usuario y contraseña** para especificar uno de los siguientes métodos de autenticación no EAP (también conocidos como identidad interna):<br /><br /><ul><li>**Ninguno**</li><li>**Contraseña no cifrada (PAP)**</li><li>**Protocolo de autenticación de desafío mutuo (CHAP)**</li><li>**Microsoft CHAP (MS-CHAP)**</li><li>**Microsoft CHAP versión 2 (MS-CHAP v2)**</li><li>**EAP-TLS**</li></ul></li></ul>|El **Tipo de EAP** es **PEAP** o **EAP-TTLS**.|
|**Seleccionar un certificado de cliente para la autenticación de cliente (certificado de identidad)**|Seleccione el perfil de certificado SCEP que se usa para autenticar la conexión. **Important:** Para crear un perfil de certificado SCEP, consulte [Habilitar el acceso a los recursos de empresa mediante perfiles de certificados con Microsoft Intune](../Topic/Enable-access-to-company-resources-using-certificate-profiles-with-Microsoft-Intune.md).|El tipo de seguridad es **WPA-Enterprise/WPA2-Enterprise** y el **Tipo de EAP** es **EAP-TLS**, **PEAP** o **EAP-TTLS**.|
|**Habilitar privacidad de identidad (identidad externa)**|Especifique el texto que se envía como respuesta a una solicitud de identidad EAP. Este texto puede ser cualquier valor.<br /><br />Durante la autenticación, esta identidad anónima se envía inicialmente, seguida de la identificación real enviada en un túnel seguro.|El **Tipo de EAP** está establecido en **PEAP**, **EAP-TTLS** o **EAP-FAST**.|

### Paso 4: Configurar el proxy (solo iOS y MAC OS X)

1.  En el caso de perfiles de Wi-Fi de iOS y Mac OS X, configure las siguientes opciones (si usa un servidor proxy para que sea más fácil proteger la red) en **Configuración de proxy**:

    |Nombre de la configuración|Más información|Se debe usar cuando:|
    |------------------------------|-------------------|------------------------|
    |**Configuración del proxy para esta conexión Wi-Fi**|Elija el tipo de configuración de proxy:<br /><br />-   **Ninguna** (valor predeterminado)<br />-   **Manual**: especifique manualmente la dirección URL y el número de puerto del servidor proxy.<br />-   **Automática**: use un archivo de configuración para configurar el servidor proxy.|Siempre|
    |**Dirección del servidor proxy** y **Número de puerto**|Especifique la dirección URL y el número de puerto del servidor proxy.|La **Configuración del proxy para esta conexión Wi-Fi** está establecida en **Manual**|
    |**Dirección URL del servidor proxy**|Especifique la dirección URL del archivo que contiene la configuración del servidor proxy.|La **Configuración del proxy para esta conexión Wi-Fi** está establecida en **Automática**|

### Paso 5: Guardar el perfil de Wi-Fi

1.  Cuando haya terminado haga clic en **Guardar directiva**.

La nueva directiva se muestra en el nodo **Directivas de configuración** del área de trabajo **Directiva**.

### Paso 6: Implementar el perfil de Wi-Fi

1.  Implemente el perfil de Wi-Fi en uno o más grupos de usuarios o dispositivos de su organización.

Para obtener más información sobre cómo implementar directivas, consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

En el área de trabajo **Directiva**, un resumen de estado y las alertas identifican los problemas de la directiva que requieren su atención. Además, aparece un resumen de estado en el área de trabajo **Panel**.

Tras una implementación correcta, los dispositivos de los usuarios pueden conectarse automáticamente a la red inalámbrica empresarial que configuró.

## <a name="BKMK_Import"></a>Importar un perfil de configuración de Wi-Fi (solo Windows 8.1 y posterior)
Use la **Directiva de importación de Wi-Fi de Windows** para importar un conjunto de opciones de Wi-Fi que luego puede implementar en los grupos de usuarios o de dispositivos necesarios.

> [!TIP]
> En Windows, puede usar la utilidad **netsh wlan** para exportar un perfil de Wi-Fi existente a un archivo XML que [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] pueda leer.
> 
> Por ejemplo, para exportar una conexión Wi-Fi denominada **MyConnection** a un archivo XML, escriba lo siguiente desde un símbolo del sistema de Windows:
> 
> **netsh wlan export profile MyConnection**

1.  En la [consola de administración de Microsoft Intune](https://manage.microsoft.com), haga clic en **Directiva** &gt; **Agregar directiva**.

2.  Configure una directiva del tipo **Windows** &gt; **Directiva de importación de Wi-Fi de Windows**.

    Solo puede crear e implementar una directiva personalizada de importación de Wi-Fi de Windows. La configuración recomendada no está disponible.

    Si necesita más información acerca de cómo crear e implementar directivas, consulte el tema [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

3.  Especifique los siguientes valores generales para la Directiva de importación de Wi-Fi de Windows:

    |Nombre de la configuración|Más información|
    |------------------------------|-------------------|
    |**Nombre**|Escriba un nombre único para el perfil de Wi-Fi que permita identificarlo en la consola de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Descripción**|Proporcione una descripción del perfil de Wi-Fi y cualquier otra información relevante para que sea más fácil encontrarlo.|

4.  Especifique los valores siguientes en el encabezado **Perfil de Wi-Fi personalizado**:

    |Nombre de la configuración|Más información|
    |------------------------------|-------------------|
    |**Archivo del perfil de configuración**|Haga clic en **Importar** para seleccionar el archivo XML que contiene la configuración del perfil de Wi-Fi que desea importar a [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Nombre del perfil de configuración personalizada (que se muestra a los usuarios)**|Muestra el nombre del perfil de configuración de Wi-Fi tal y como se mostrará a los usuarios en su dispositivo.|
    |**Detalles del perfil de configuración**|Muestra el código XML para el perfil de configuración seleccionado.|

5.  Cuando haya terminado haga clic en **Guardar directiva**.

6.  La nueva directiva se muestra en el nodo **Directivas de configuración** del área de trabajo **Directiva**.

Ahora puede usar la información del **paso 6** anterior para que sea más fácil implementar el perfil de Wi-Fi personalizado.

## Vea también
[Habilitar el acceso a los recursos de empresa con Microsoft Intune](../Topic/Enable-access-to-company-resources-with-Microsoft-Intune---deleted.md)

