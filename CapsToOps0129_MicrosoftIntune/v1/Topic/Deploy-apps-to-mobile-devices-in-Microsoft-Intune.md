---
title: Implementar aplicaciones en dispositivos m&#243;viles en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6da30550-9e8e-4333-b9b3-83928de3807a
---
# Implementar aplicaciones en dispositivos m&#243;viles en Microsoft Intune
Ahora que ya [conoce los conceptos básicos](https://technet.microsoft.com/library/dn646955.aspx) de la implementación de aplicaciones de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], aprenderá a configurar e implementar aplicaciones para dispositivos inscritos con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Por lo general, esto implica tres pasos:

-   [Configurar la aplicación](#BKMK_Conf)

-   [Implementar la aplicación](#BKMK_Depl)

-   [Supervisar la aplicación](#BKMK_Monitor)

Para obtener información sobre cómo actualizar y retirar aplicaciones, consulte [Actualizar aplicaciones con Microsoft Intune](../Topic/Update-apps-using-Microsoft-Intune.md).

> [!IMPORTANT]
> La información de este tema le ayudará a implementar aplicaciones en [equipos Windows inscritos](https://technet.microsoft.com/library/mt346003.aspx) y otros dispositivos móviles. Si desea implementar aplicaciones en [equipos Windows administrados mediante software cliente](https://technet.microsoft.com/library/dn646959.aspx), consulte [Implementar aplicaciones en equipos Windows en Microsoft Intune](../Topic/Deploy-apps-to-Windows-PCs-in-Microsoft-Intune.md).

## <a name="BKMK_Conf"></a>Configurar la aplicación
En este procedimiento, usará el Editor de software de Intune para configurar las propiedades de la aplicación y, si procede, cargarla en su espacio de almacenamiento en la nube.

#### Para configurar una aplicación

1.  En la [consola de administrador de Microsoft Intune](https://manage.microsoft.com), haga clic en **Aplicaciones** &gt; **Agregar aplicaciones** para iniciar el Editor de software de Intune.

    > [!TIP]
    > Deberá escribir su nombre de usuario y contraseña de Intune para que se inicie el editor.

2.  En la página **Instalación de software** del editor de software, configure lo siguiente:

    **Seleccione cómo debe ponerse a disposición de los dispositivos este software**: elija lo siguiente:

    -   **Instalador de software** y especifique:

        |Configuración|Detalles|
        |-----------------|------------|
        |**Seleccionar el tipo de archivo instalador de software**|Indica el tipo de software que desea implementar. Por ejemplo, si desea instalar una aplicación iOS, elija **Paquete de aplicación para iOS (archivo &#42;.ipa)**.|
        |**Especifique la ubicación de los archivos de instalación del software**|Escriba la ubicación de los archivos de instalación o haga clic en **Examinar** para seleccionar la ubicación en una lista.|
        |**Incluir archivos y subcarpetas adicionales de la misma carpeta**|Solo para el tipo de archivo **Windows Installer**<br /><br />Cierto software que usa Windows Installer necesita los archivos auxiliares que normalmente se encuentran en la misma carpeta que los archivos de instalación. Seleccione esta opción si también desea implementar estos archivos.|
        Este tipo de instalación usa parte del espacio de almacenamiento en la nube.

    -   **Vínculo externo** y especifique:

        |Configuración|Detalles|
        |-----------------|------------|
        |**Especificar una dirección URL**|Escriba la dirección URL de la tienda de aplicaciones de la aplicación que desea implementar. Por ejemplo, si desea implementar la aplicación de Escritorio remoto de Microsoft para Android, especifique **https://play.google.com/store/apps/details?id=com.microsoft.rdc.android**. **Tip:** Para buscar la dirección URL de la aplicación, use un motor de búsqueda para encontrar la página de almacenamiento que contiene la aplicación. Por ejemplo, para encontrar la aplicación de Escritorio remoto, podría buscar **Microsoft Remote Desktop Android**.|
        Este tipo de instalación no usa el espacio de almacenamiento en la nube.

    -   **Aplicación iOS administrada de la App Store** y especifique:

        |Configuración|Detalles|
        |-----------------|------------|
        |**Especificar una dirección URL**|Escriba la dirección URL de la tienda de aplicaciones de la aplicación que desea implementar. Por ejemplo, si desea implementar la aplicación Carpetas de trabajo de Microsoft para iOS, especifique **https://itunes.apple.com/us/app/work-folders/id950878067?mt=8**.|
        Este tipo de instalación no usa el espacio de almacenamiento en la nube.

3.  En la página **Descripción del software**, configure las siguientes opciones:

    > [!TIP]
    > En función del tipo de instalador que use, algunos de estos valores podrían especificarse automáticamente o no aparecer.

    |Configuración|Detalles|
    |-----------------|------------|
    |**Publicador**|Escriba el nombre del publicador de la aplicación.|
    |**Nombre**|Escriba el nombre de la aplicación tal como se mostrará en el portal de empresa. **Tip:** Asegúrese de que todos los nombres de aplicación que usa son únicos. Si el mismo nombre de aplicación existe dos veces, solo se mostrará a los usuarios una de las aplicaciones en el portal de empresa.|
    |**Descripción**|Escriba una descripción de la aplicación. Se mostrará a los usuarios en el portal de empresa.|
    |**Dirección URL para información del software**|Solo está disponible si seleccionó **Instalador de software**.<br /><br />(opcional) Escriba una dirección URL de un sitio web que contenga información sobre esta aplicación. La dirección URL se mostrará a los usuarios en el portal de empresa.|
    |**Dirección URL de privacidad**|Solo está disponible si seleccionó **Instalador de software**.<br /><br />(opcional) Escriba una dirección URL de un sitio web que contenga información de privacidad sobre esta aplicación. La dirección URL se mostrará a los usuarios en el portal de empresa.|
    |**Categoría**|(opcional) Seleccione una de las categorías de aplicaciones integradas. Así les resultará más fácil a los usuarios encontrar la aplicación cuando exploren el portal de empresa.|
    |**Mostrar esta aplicación como destacada y resaltarla en el portal de empresa**|Muestra la aplicación de forma destacada en la página principal del portal de empresa cuando los usuarios buscan aplicaciones.|
    |**Icono**|(opcional) Cargue un icono que se asociará con la aplicación. Será el icono que se muestre con la aplicación cuando los usuarios examinen el portal de empresa.|

4.  En la página **Requisitos**, seleccione los requisitos que deben cumplirse para que la aplicación pueda empezar a instalarse en un dispositivo. Por ejemplo, en el caso de un paquete de aplicación para iOS, puede seleccionar la versión mínima de iOS necesaria y el tipo de dispositivo que debe ser, como iPhone o iPad.

    > [!TIP]
    > La página **Requisitos** no se muestra para todos los tipos de aplicaciones.

5.  Se mostrarán más páginas del asistente si elige el tipo de archivo **Windows Installer**. Este tipo de archivo no se usa en dispositivos móviles. Para obtener más información, vea [Implementar aplicaciones en equipos Windows en Microsoft Intune](../Topic/Deploy-apps-to-Windows-PCs-in-Microsoft-Intune.md).

6.  En la página **Resumen**, revise la información que especificó. Cuando esté listo, haga clic en **Cargar**.

7.  Haga clic en **Cerrar** para finalizar.

La aplicación se muestra en el nodo **Aplicaciones** del área de trabajo **Aplicaciones**.

## <a name="BKMK_Depl"></a>Implementar la aplicación
En este procedimiento, implementará la aplicación en los dispositivos o para los usuarios seleccionados.

#### Para implementar la aplicación

1.  En la [consola de administrador de Microsoft Intune](https://manage.microsoft.com), haga clic en **Aplicaciones** &gt; **Aplicaciones** para ver la lista de aplicaciones que administra.

2.  Seleccione la aplicación que desea implementar y haga clic en **Administrar la implementación**.

3.  En el cuadro de diálogo *&lt;nombre de la aplicación&gt;*, en la página **Seleccionar grupos**, seleccione los grupos de usuarios o dispositivos en los que desea implementar la aplicación.

4.  En la página **Acción de implementación**, configure lo siguiente:

    |Configuración|Detalles|
    |-----------------|------------|
    |**Aprobación**|Elija una de las siguientes opciones para la implementación:<br /><br />-   **Necesaria** (instalación obligatoria)<br />-   **Disponible** (los usuarios la instalan desde el portal de empresa a petición)<br />-   **No aplicable** (la aplicación no se instala o no se muestra en el portal de empresa)<br />-   **Desinstalar** (la aplicación se desinstalará de los dispositivos de destino)|
    |**Fecha límite**|En el caso de las instalaciones necesarias, elija cuándo se implementará la aplicación. Puede elegir entre los valores predefinidos, o bien seleccionar **Personalizado** para configurar su propia fecha límite.|

5.  Si la aplicación que va a implementar se puede configurar mediante una [directiva de administración de aplicaciones móviles](https://technet.microsoft.com/library/dn878026.aspx), se mostrará la página **Administración de aplicaciones móviles**. En esta página, seleccione la directiva de administración de aplicaciones móviles que desea asociar a esta aplicación.

    > [!TIP]
    > [Vea qué aplicaciones de Microsoft son compatibles con las directivas de administración de aplicaciones móviles](https://technet.microsoft.com/library/dn708489.aspx).

6.  Si la aplicación que va a implementar es compatible con perfiles de VPN de Intune, se mostrará la página **Perfil de VPN**. En esta página, puede elegir asociar aplicaciones iOS con un perfil de VPN que haya implementado. La conexión VPN se abrirá automáticamente cuando se inicie la aplicación. Para disponer de un perfil de VPN, debe tener habilitada la configuración de perfil **VPN por aplicación**. Para obtener información acerca de cómo configurar perfiles de VPN, incluida la compatibilidad para asociar perfiles con aplicaciones, consulte [Ayudar a los usuarios a conectarse a su trabajo con perfiles de VPN con Microsoft Intune](../Topic/Help-users-connect-to-their-work-using-VPN-profiles-with-Microsoft-Intune.md).

|||
|-|-|
|![](../Image/Available-install-on-iOS.png)|Si implementó la aplicación como **Disponible**, se mostrará en el portal de empresa en el dispositivo de los usuarios, desde donde pueden instalar la aplicación. Por ejemplo, en esta captura de pantalla, se implementó la aplicación Bing for iOS usando el tipo de instalación **Vínculo externo** con un icono personalizado y se seleccionó la opción **Mostrar esta aplicación como destacada y resaltarla en el portal de empresa**.|
|![](../Image/iOS-Required-install.PNG)|Si implementó la aplicación de la manera indicada, el usuario recibirá una notificación en la que se le informará de que la aplicación está preparada para la instalación. Por ejemplo, en esta captura de pantalla, se implementó la aplicación Carpetas de trabajo para iOS usando el tipo de instalación **Aplicación iOS administrada de la App Store**.|

## <a name="BKMK_Monitor"></a>Supervisar la aplicación
Puede ver las aplicaciones que administra y su estado de implementación en la consola de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

### Para ver las aplicaciones que administra y su estado
En el área de trabajo **Aplicaciones**, haga clic en el nodo **Aplicaciones**.

Se mostrará la lista de aplicaciones que administra. Puede hacer clic en cualquier aplicación para ver el estado de la instalación en el panel inferior de las ventanas de la consola. Haga clic en el estado para ver más detalles. Por ejemplo, si se muestra el estado **1 usuario tiene este software disponible**, puede hacer clic en el mensaje para ver el nombre del usuario.

> [!TIP]
> Puede usar la lista desplegable **Filtros** para mostrar solo las aplicaciones que cumplen los criterios que especifique, como las aplicaciones que no se pudieron instalar o las aplicaciones que se implementaron correctamente.
> 
> ![](../Image/App-filters.JPG)

Además, el área de trabajo **Panel** muestra información general sobre el estado de las aplicaciones. Si hace clic en cualquier parte de la información general, accederá a la lista de aplicaciones.

### Para ver información más detallada sobre una aplicación
En la lista de aplicaciones, seleccione cualquier aplicación y haga clic en **Ver propiedades**.

En la página **Propiedades del software** de la aplicación, haga clic en una de estas pestañas:

-   **General**: muestra información general sobre la aplicación y su estado de instalación.

-   **Dispositivos**: muestra los dispositivos que instalaron correctamente una determinada implementación de la aplicación.

-   **Usuarios**: muestra los usuarios cuyos dispositivos instalaron correctamente una determinada implementación de la aplicación.

Al igual que antes, puede usar la lista desplegable **Filtros** para configurar los valores mostrados en cada una de las pestañas.

## Vea también
[Implementar y configurar aplicaciones con Microsoft Intune](../Topic/Deploy-and-configure-apps-with-Microsoft-Intune.md)

