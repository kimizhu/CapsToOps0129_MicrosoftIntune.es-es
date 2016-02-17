---
title: Inscribir dispositivos iOS de empresa en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2d3ca4ab-f20c-4d56-9413-f8ef19cf0722
robots: noindex,nofollow
---
# Inscribir dispositivos iOS de empresa en Microsoft Intune
Intune permite inscribir dispositivos iOS de empresa con el programa de inscripción de dispositivos (DEP) de Apple o la herramienta [Apple Configurator](http://go.microsoft.com/fwlink/?LinkId=518017) en ejecución en un equipo Mac.

Puede inscribir dispositivos iOS de empresa de tres maneras:

-   **Inscripción con el asistente de configuración**: restablece la configuración de fábrica del dispositivo y lo prepara para que el nuevo usuario del dispositivo lo instale.Este método admite inscripciones de DEP o de Apple Configurator.

-   **Inscripción directa**: crea un archivo compatible con Apple Configurator para su uso durante la preparación del dispositivo.No se restablece la configuración de fábrica del dispositivo inscrito pero no tiene ninguna afiliación de usuario.Este método no puede usarse para la inscripción de DEP.

-   **Programa de inscripción de dispositivos (DEP)**: implementa un perfil de inscripción que inscribe el dispositivo “por aire” y puede incluir opciones de asistente para la instalación para el dispositivo.Los usuarios no pueden anular la inscripción de dispositivos inscritos a través de DEP.

## Instrucciones para el asistente de configuración

1.  **Crear un grupo de dispositivos móviles** (opcional)
     Si su empresa requiere grupos de dispositivos móviles para ayudar a administrar los dispositivos, cree los grupos.[Utilizar grupos para administrar usuarios y dispositivos en Microsoft Intune](../Topic/Use-groups-to-manage-users-and-devices-with-Microsoft-Intune.md).

2.  **Crear un perfil para dispositivos**
    Un perfil de inscripción de dispositivo define la configuración que se aplica a un grupo de dispositivos.Si aún no lo tiene, cree un perfil de inscripción de dispositivo para los dispositivos iOS inscritos mediante Apple Configurator.**Pedir afiliación de usuario** debe habilitarse para la inscripción con el **Asistente de configuración**

    ###### Instrucciones

    1.  En la [consola de administración de Microsoft Intune](http://manage.microsoft.com), vaya a **Directiva** &gt; **Dispositivos corporativos** y haga clic en **Agregar...**.

    2.  Especifique los detalles de los perfiles de dispositivo:

        -   **Nombre**: nombre del perfil de inscripción de dispositivo.(No es visible para los usuarios)

        -   **Descripción**: descripción del perfil de inscripción de dispositivo.(No es visible para los usuarios)

        -   **Afiliación de usuario**: especifica cómo se inscriben los dispositivos.

            -   **Pedir afinidad de usuario**: el dispositivo se puede afiliar con un usuario durante la instalación inicial y, a continuación, se le puede permitir el acceso a los datos y al correo electrónico de la compañía como dicho usuario.Este modo admite varios escenarios:

                -   **Dispositivo personal de empresa**: elección de un dispositivo propio, o lo que se conoce como "Choose Your Own Device" (CYOD). Similar a dispositivos personales o de propiedad privada, pero el administrador tiene ciertos privilegios, incluidos permisos para borrar, restablecer, administrar y anular la inscripción del dispositivo.El usuario del dispositivo puede instalar aplicaciones y tiene la mayoría de los demás permisos para usar el dispositivo que no estén bloqueados por la directiva de administración.

                -   **Cuenta de administrador de inscripción de dispositivos**: el dispositivo se inscribe con una cuenta de administrador de Intune especial.Se puede administrar como una cuenta privada, pero solo un usuario que conozca las credenciales del administrador de inscripción puede instalar aplicaciones, borrar, restablecer, administrar y anular la inscripción del dispositivo.Para obtener información acerca de cómo inscribir un dispositivo compartido por varios usuarios mediante una cuenta común, consulte [Inscribir dispositivos propiedad de la empresa con el Administrador de inscripción de dispositivos de Microsoft Intune](../Topic/Enroll-corporate-owned-devices-with-the-Device-Enrollment-Manager-in-Microsoft-Intune.md).

            -   **No hay afinidad de usuario**: el dispositivo no tiene usuarios.Utilice esta afiliación para dispositivos que realizan tareas sin tener acceso a datos de usuario local.Las aplicaciones que requieren una afiliación de usuario están deshabilitadas o no funcionarán.

        -   **Asignación previa de grupo de dispositivos**: todos los dispositivos que implementan este perfil pertenecerán inicialmente a este grupo.Puede reasignar los dispositivos después de la inscripción.

    3.  Haga clic en **Guardar perfil** para agregar el perfil.

3.  **Agregar dispositivos iOS para inscribirse con el Asistente para la instalación**
    En la [consola de administración de Microsoft Intune](http://manage.microsoft.com), vaya a **Grupos** &gt; **Todos los dispositivos** &gt; **Todos los dispositivos corporativos** &gt; **Todos los dispositivos** y, a continuación, haga clic en **Agregar dispositivos...**.Puede agregar dispositivos de dos maneras:

    -   **Cargar un archivo CSV que contiene números de serie**: cree una lista de valores separados por comas (.csv) con dos columnas sin encabezado, limitada a 5000 dispositivos o 5 MB por archivo csv.

        |||
        |-|-|
        |&lt;N.º de serie 1&gt;|&lt;Detalles del dispositivo n.º 1&gt;|
        |&lt;N.º de serie 2&gt;|&lt;Detalles del dispositivo n.º 2&gt;|
        Este archivo .csv, cuando se ve en un editor de texto, aparece como:

        ```
        0000000,PO 1234
        111111111,PO 1234
        ```

    -   **Agregar manualmente los detalles del dispositivo**: especifique el número de serie y los detalles de hasta cinco dispositivos

    > [!NOTE]
    > Si posteriormente necesita quitar dispositivos corporativos de la administración de Intune, debe quitar el número de serie del dispositivo de Intune del grupo **Dispositivos corporativos** para deshabilitar la inscripción de dispositivos.  Si Intune realiza un procedimiento de recuperación ante desastres en el momento en que se quitan los números de serie o en torno a este momento, se deberá comprobar que solo los números de serie de los dispositivos activos están presentes en ese grupo.

    A continuación, haga clic en **Siguiente**.

4.  **Seleccionar dispositivos para inscribir**
    Confirme los dispositivos que se van a inscribir.No se pueden importar los números de serie ya inscritos o inscritos por otros medios.Haga clic en **Siguiente** para continuar.

5.  **Asignar perfil**
    Especifique el perfil que se va a asignar a los dispositivos agregados desde la lista de perfiles disponibles, consulte los **detalles del perfil de inscripción** y, a continuación, haga clic en **Finalizar**.Los dispositivos agregados manualmente pueden asignarse a cualquier perfil de inscripción, pero los dispositivos sincronizados por DEP deben asignarse a un perfil habilitado para DEP.

6.  **Seleccionar un perfil para implementarlo en dispositivos iOS**
    En la [consola de administración de Microsoft Intune](http://manage.microsoft.com), vaya a **Directiva** &gt; **Inscripción de dispositivos corporativos** y, después, seleccione el perfil de dispositivo que desee implementar en los dispositivos móviles.Haga clic en **Exportar...** en la barra de tareas.Copie y guarde el valor de **Dirección URL del perfil**.Se cargará en Apple Configurator más tarde para definir el perfil de Intune utilizado por los dispositivos iOS.En el caso de dispositivos DEP, simplemente ejecute el Asistente para la instalación desde una imagen de fábrica o el restablecimiento de fábrica en el dispositivo.

7.  **Preparar el dispositivo con Apple Configurator** 
    Los dispositivos iOS están conectados al equipo Mac e inscritos para la administración de dispositivos móviles.

    > [!WARNING]
    > Los dispositivos se restablecerán en la configuración de fábrica durante el proceso de inscripción.

    1.  En un equipo Mac, abra **Apple Configurator**.

    2.  Seleccione **Instalación** y, después, **Inscripción de dispositivo**.Escriba la dirección URL de inscripción de Intune en **Dirección URL del servidor MDM** y, después, haga clic en **Guardar**.

    3.  Conecte los dispositivos móviles iOS al equipo Apple con un adaptador USB.

    4.  Haga clic en **Preparar**.El progreso se muestra en Apple Configurator.

8.  **Distribuir los dispositivos** 
    Los dispositivos ya están listos para la inscripción corporativa.Apague los dispositivos y distribúyalos a los usuarios.Cuando el dispositivo se encienda, se iniciará el asistente de configuración y pedirá al usuario su cuenta profesional o educativa.

## Instrucciones para la inscripción directa

1.  **Crear un grupo de dispositivos móviles** (opcional) 
    Si su empresa u organización requiere grupos de dispositivos móviles para ayudar a administrar los dispositivos, cree los grupos.[Utilizar grupos para administrar usuarios y dispositivos en Microsoft Intune](../Topic/Use-groups-to-manage-users-and-devices-with-Microsoft-Intune.md).

2.  **Crear un perfil para dispositivos**
    Un perfil de inscripción de dispositivo define la configuración que se aplica a los dispositivos.Si aún no lo tiene, cree un perfil de inscripción de dispositivo para los dispositivos iOS inscritos mediante Apple Configurator.

    ###### Instrucciones

    1.  En la [consola de administración de Microsoft Intune](http://manage.microsoft.com), vaya a **Directiva** &gt; **Inscripción de dispositivos corporativos** y, después, haga clic en **Agregar...**.

    2.  Especifique los detalles de los perfiles de dispositivo:

        -   **Nombre**: nombre del perfil de inscripción de dispositivo.No es visible para los usuarios.

        -   **Descripción**: descripción del perfil de inscripción de dispositivo.No es visible para los usuarios.

        -   **Afiliación de usuario**: especifica cómo se inscriben los dispositivos.Para Inscripción directa, seleccione **No preguntar**.

        -   **Asignación previa de grupo de dispositivos**: todos los dispositivos que implementan este perfil pertenecerán inicialmente a este grupo.Puede reasignar los dispositivos después de la inscripción.

    3.  Haga clic en **Guardar perfil** para agregar el perfil.

3.  **Seleccionar y exportar un archivo de perfil de inscripción**
    En la [consola de administración de Microsoft Intune](http://manage.microsoft.com), vaya a **Directiva** &gt; **Inscripción de dispositivos corporativos** y, después, seleccione el perfil de dispositivo para implementar en los dispositivos iOS.Haga clic en **Exportar...** en la barra de tareas.Se abre la ventana **Método de configuración de Apple**.

    En **Método de configuración de Apple**, seleccione **Inscripción directa**.Descargue y guarde el archivo de perfil de inscripción directa (.mobileconfig).Debe importar este archivo a Apple Configurator para definir el perfil de Intune que utilizan los dispositivos iOS.Un archivo de perfil de inscripción es válido durante 2 semanas.

4.  **Importar el archivo de perfil y preparar el dispositivo**
    Copie el archivo de perfil de inscripción de Intune (.mobileconfig) a un equipo Mac e importe el archivo en Apple Configurator.Ya puede conectar dispositivos iOS por USB para inscribirlos con Apple Configurator.Los dispositivos configurados con este archivo deben haber completado el Asistente para la instalación y deben tener una conexión a Internet al aplicar el archivo.

## Inscribir dispositivos iOS de empresa en Microsoft Intune mediante el Programa de Inscripción de Dispositivos de Apple
Para administrar dispositivos iOS de empresa con el Programa de Inscripción de Dispositivos de Apple (DEP), las empresas deben unirse al DEP de Apple y adquirir los dispositivos a través de dicho programa.Los detalles de dicho proceso están disponibles en: [https://deploy.apple.com](https://deploy.apple.com)

Para poder inscribir dispositivos iOS de empresa con DEP, necesita un token de DEP de Apple.Este token permite a Intune sincronizar información sobre dispositivos propiedad de la empresa que participan en DEP.También permite a Intune realizar cargas de perfiles de inscripción a Apple y asignar dispositivos a esos perfiles.

### <a name="BKMK_DEPtok"></a>

1.  **Empezar a administrar dispositivos iOS con Microsoft Intune**
    Para poder inscribir dispositivos del programa de inscripción de dispositivos (DEP) iOS, debe completar los pasos que se detallan en [Configurar la administración de iOS con Microsoft Intune](../Topic/Set-up-iOS-and-Mac-management-with-Microsoft-Intune.md).

2.  **Obtener una clave de cifrado**
    Como usuario administrativo, abra la [consola de administración de Microsoft Intune](http://manage.microsoft.com), vaya a **Administración** &gt; **Administración de dispositivos móviles** &gt; **iOS** &gt; **Programa de Inscripción de Dispositivos** y haga clic en **Descargar clave de cifrado**.Guarde el archivo de clave de cifrado (.pem) localmente.El archivo .pem se usa para solicitar un certificado de relación de confianza en el portal del Programa de Inscripción de Dispositivos de Apple.

3.  **Obtener un token del programa de inscripción de dispositivos**
    Vaya al [Portal del programa de inscripción de dispositivos](https://deploy.apple.com) (https://deploy.apple.com) e inicie sesión con su identificador de Apple de empresa.Este identificador de Apple debe usarse posteriormente para renovar el token de DEP.

    1.  En el [portal del programa de inscripción de dispositivos](https://deploy.apple.com), vaya a **Programa de inscripción de dispositivos** &gt; **Administrar servidores** y, después, haga clic en **Agregar servidor MDM**.

    2.  Escriba el **nombre del servidor MDM** y, a continuación, haga clic en **Siguiente**.El nombre del servidor es su referencia para identificar el servidor MDM.No es el nombre o la dirección URL del servidor de Microsoft Intune.

    3.  Se abre el cuadro de diálogo **Agregar &lt;NombreDeServidor&gt;**.Haga clic en **Elegir archivo...** para cargar el archivo .pem y, a continuación, haga clic en **Siguiente**.

    4.  En el cuadro de diálogo **Agregar &lt;NombreDeServidor&gt;** se muestra el vínculo **Su token de servidor**.Descargue el archivo de token de servidor (.p7m) en el equipo y, a continuación, haga clic en **Listo**.

    Este archivo de certificado (.p7m) se usa para establecer una relación de confianza entre los servidores de Intune y los del Programa de Inscripción de Dispositivos de Apple.

4.  **Agregar el token de DEP a Intune**
    En la [consola de administración de Microsoft Intune](http://manage.microsoft.com), vaya a **Administración** &gt; **Administración de dispositivos móviles** &gt; **iOS** &gt; **Programa de inscripción de dispositivos** y haga clic en **Cargar el token de DEP**.**Busque** el archivo de certificado (.p7m), escriba su **ID de Apple** y haga clic en **Cargar**.

5.  **Agregar la directiva de inscripción de dispositivos corporativos**
    En la [consola de administración de Microsoft Intune](http://manage.microsoft.com), vaya a **Directiva** &gt; **Inscripción de dispositivos corporativos** y, a continuación, haga clic en **Agregar**.Proporcione los detalles de **General**, incluidos los de **Nombre** y **Descripción**, especifique si los dispositivos asignados al perfil tienen afinidad de usuario o pertenecen a un grupo y, después, habilite la opción **Configure los ajustes del Programa de inscripción de dispositivos para esta directiva** para permitir el uso de DEP.Los **paneles de Asistente para la instalación** definen la configuración de dispositivos iOS que se definió durante la instalación.

6.  **Asignar dispositivos DEP para la administración** 
    Vaya al [portal del programa de inscripción de dispositivos](https://deploy.apple.com) (https://deploy.apple.com) e inicie sesión con su identificador de Apple corporativo.Vaya a **Programa de implementación** &gt; **Programa de inscripción de dispositivos** &gt; **Administrar dispositivos**.Especifique cómo va a **elegir los dispositivos**, proporcione información del dispositivo y especifique los detalles de cada dispositivo, como **Número de serie** y **Número de pedido**, o seleccione **Cargar archivo CSV**.A continuación, seleccione **Asignar al servidor**, seleccione el &lt;NombreDeServidor&gt; especificado para Microsoft Intune y, después, haga clic en **Aceptar**.

7.  **Distribuir los dispositivos a los usuarios**
    Los dispositivos corporativos pueden distribuirse ahora a los usuarios.Los dispositivos iOS quedan inscritos para su administración mediante Intune al activarlos.

8.  **Sincronizar dispositivos administrados mediante DEP**
    Como usuario administrativo, abra la [consola de administración de Microsoft Intune](http://manage.microsoft.com), vaya a **Administración** &gt; **Administración de dispositivos móviles** &gt; **iOS** &gt; **Programa de inscripción de dispositivos** y haga clic en **Sincronizar ahora**.Se envía una solicitud de sincronización a Apple.Para ver dispositivos administrados mediante DEP después de la sincronización, en la [consola de administración de Microsoft Intune](http://manage.microsoft.com) vaya a **Grupos** &gt; **Todos los dispositivos corporativos**.En el área de trabajo **Dispositivos corporativos**, el **Estado** de los dispositivos administrados es "No contactado" hasta que el dispositivo se enciendo y ejecute el Asistente de configuración para inscribir el dispositivo.

## Pasos siguientes
**Una vez inscritos los dispositivos, puede:**

-   [Supervisar dispositivos móviles con Microsoft Intune](../Topic/Understand-your-devices-with-inventory-in-Microsoft-Intune.md)

-   [Habilitar el acceso a los recursos de empresa con Microsoft Intune](../Topic/Enable-access-to-company-resources-with-Microsoft-Intune---deleted.md)

-   [Implementar aplicaciones en dispositivos móviles en Microsoft Intune](../Topic/Deploy-apps-to-mobile-devices-in-Microsoft-Intune---deleted.md)

-   [Administrar la configuración y las características de los dispositivos con directivas de Microsoft Intune](../Topic/Manage-settings-and-features-on-your-devices-with-Microsoft-Intune-policies.md)

-   [Ayude a proteger sus datos mediante la eliminación remota, el bloqueo remoto o el restablecimiento de código de acceso mediante Microsoft Intune.](../Topic/Help-protect-your-data-with-remote-wipe,-remote-lock,-or-passcode-reset-using-Microsoft-Intune.md)

## Vea también
[Preparar la inscripción de dispositivos en Microsoft Intune](../Topic/Get-ready-to-enroll-devices-in-Microsoft-Intune.md)

