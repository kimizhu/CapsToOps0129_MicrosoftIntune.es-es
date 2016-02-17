---
title: Configurar la administraci&#243;n de dispositivos Windows con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9a18c0fe-9f03-4e84-a4d0-b63821bf5d25
---
# Configurar la administraci&#243;n de dispositivos Windows con Microsoft Intune
Puede usar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] para administrar escritorios, equipos portátiles y otros dispositivos que ejecutan Windows como dispositivos móviles. Es posible que también desee [Configurar la administración de Windows Phone con Microsoft Intune](../Topic/Set-up-Windows-Phone-management-with-Microsoft-Intune.md) o [administrar equipos con el software cliente de Intune](http://technet.microsoft.com/library/dn646959.aspx) con el cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## Preparar la administración de dispositivos Windows con Intune
Para acceder a recursos administrados con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], los usuarios pueden inscribir sus equipos con Windows como dispositivos móviles.  Crear un CNAME DNS ayuda a que los usuarios se conecten al portal de empresa de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] sin especificar un nombre de servidor. Si desea implementar el portal de empresa con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], deberá habilitar la instalación de prueba con una clave de instalación de prueba.   Los usuarios también pueden descargar e instalar el portal de empresa desde la Tienda o usar el software incluido en Windows. Complete los pasos siguientes para configurar la administración de dispositivos Windows con [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

#### Configurar la administración de dispositivos Windows

1.  **Configurar [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]** 
    Si aún no lo hizo, [prepare la administración de dispositivos móviles](https://technet.microsoft.com/library/mt346013.aspx) estableciendo la entidad de administración de dispositivos móviles en **[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]**.

2.  **Establecer un alias DNS para la dirección del servidor de inscripción** (opcional)

    Un alias DNS (tipo de registro CNAME) facilita a los usuarios la inscripción de sus dispositivos, ya que rellena automáticamente el nombre del servidor durante la inscripción.

    ###### Comprobar y crear CNAME de DNS

    1.  En la [consola de administración de Intune](http://manage.microsoft.com), haga clic en **Administración** &gt; **Administración de dispositivos móviles** &gt; **Windows Phone**.

    2.  Escriba la dirección URL del dominio comprobado del sitio web de empresa en el cuadro **Especificar un nombre de dominio comprobado** y, después, haga clic en **Probar detección automática**.

    3.  Cree registros de recursos CNAME para el dominio de su empresa. Los registros de recursos CNAME deben contener la siguiente información:

        |TYPE|Nombre de host|Apunta a|TTL|
        |--------|------------------|------------|-------|
        |CNAME|enterpriseenrollment.company_domain.com|manage.microsoft.com|1 hora|
        |CNAME|enterpriseregistration.company_domain.com|enterpriseregistration.windows.net|1 hora|
        Por ejemplo, si el sitio web de la empresa es contoso.com, debe crear un CNAME en DNS que redirija EnterpriseEnrollment.contoso.com a manage.microsoft.com. Si hay más de un dominio comprobado, debe crear un registro CNAME para cada dominio.

        -   `manage.microsoft.com`: admite una redirección al servicio Intune con reconocimiento de dominio del nombre de dominio del correo electrónico.

        -   `enterpriseregistration.windows.net`: admite la unión al área de trabajo para dispositivos móviles. También admite el acceso condicional para Windows 8.1.

    ![](../Image/Windows-Device-Enrollment.bmp)

3.  **Habilitar las aplicaciones de instalación de prueba** (Opcional)
    Para dispositivos Windows RT 8.1, Windows 8.1 y Windows 10, la aplicación Portal de empresa se puede instalar desde la Tienda Windows. Si no se instala directamente desde la Tienda Windows, la instalación de la aplicación Portal de empresa requiere las claves de instalación de prueba en los equipos de destino. Consulte [http://go.microsoft.com/fwlink/?LinkID=290705](http://go.microsoft.com/fwlink/?LinkID=290705) para obtener detalles sobre cómo implementar las claves de instalación de prueba. Aunque no es necesario que las aplicaciones con instalación de prueba estén certificadas por la Tienda Windows o instaladas mediante la Tienda Windows, solo se pueden instalar en dispositivos compatibles con la instalación de prueba. Para obtener más información acerca de cómo obtener claves de instalación de prueba, consulte el sitio de [Licencias por volumen de Microsoft](http://go.microsoft.com/fwlink/?LinkId=264711).

    ###### Para aplicaciones de firma de código para dispositivos Windows

    1.  En la [consola de administración de Intune](http://manage.microsoft.com), haga clic en **Administración** &gt; **Administración de dispositivos móviles** &gt; **Windows** &gt; **Agregar clave de carga de prueba**.

    2.  En el cuadro de diálogo **Agregar clave de instalación de prueba**, escriba un nombre, la clave de activación de producto de instalación de prueba y, opcionalmente, una descripción. A continuación, haga clic en **Aceptar**.

    3.  Descargue Microsoft Intune Company Portal App for Windows 8.1 desde el centro de descarga [http://go.microsoft.com/fwlink/?LinkId=615800](http://go.microsoft.com/fwlink/?LinkId=615800). Ejecute el archivo descargado para extraer el archivo CompanyPortal.appx y colóquelo en una carpeta compartida con acceso de red.

    4.  Ejecute **Windows PowerShell** como administrador y, después, escriba el siguiente cmdlet:

        ```
        Powershell add-appxpackage –path '‹path›'
        ```

    5.  Compruebe que el icono de **Portal de empresa** está disponible en la lista de aplicaciones del equipo de destino (en dispositivos Windows 8.1 o Windows RT 8.1 se creará un icono en la pantalla Inicio automáticamente).

4.  **Agregar usuarios de Intune** 
    El propietario del dispositivo móvil debe agregarse al portal de cuentas para poder inscribir dispositivos.  Inicie sesión en el [Portal de cuentas de Microsoft Intune](http://go.microsoft.com/fwlink/?LinkId=698854), haga clic en **Agregar usuarios** y seleccione una opción:

    -   **Usuario**: para agregar un solo usuario, seleccione **Nuevo** &gt; **Usuario** y especifique **Detalles**, **Asignar roles** y **Establecer ubicación de usuario**; a continuación, asigne el usuario a un **Grupo**.

    -   **Adición en masa**: cree un archivo .csv (vea ejemplos de archivos proporcionados) e impórtelo en el portal de cuentas. Especifique los roles, la ubicación y el grupo y, después, cree las cuentas. Los archivos .csv de ejemplo y en blanco se pueden descargar desde el portal de cuentas.

    También puede habilitar la sincronización de Active Directory o Azure Active Directory. Para obtener más información sobre la integración de otros usuarios de Azure Active Directory con Intune, consulte la [Guía de sincronización de directorios](http://go.microsoft.com/fwlink/?LinkId=511540).

5.  **Crear grupos**  (opcional)
    Los grupos ofrecen flexibilidad para administrar dispositivos y usuarios. Los grupos se pueden configurar según sus necesidades de organización (por ejemplo, por ubicación geográfica, departamento o características de hardware).   Consulte [Utilizar grupos para administrar usuarios y dispositivos en Microsoft Intune](../Topic/Use-groups-to-manage-users-and-devices-with-Microsoft-Intune.md).

6.  **Agregar directivas para dispositivos** (opcional)
    Las directivas son grupos de configuraciones que controlan las características de los dispositivos. La mayoría de las directivas MDM son específicas de la plataforma. Las directivas se crean mediante plantillas que contienen configuraciones recomendadas o personalizadas y, luego, se implementan en grupos. Consulte [Usar directivas para administrar equipos y dispositivos móviles con Microsoft Intune](../Topic/Use-policies-to-manage-computers-and-mobile-devices-with-Microsoft-Intune.md).

7.  **Establecer el límite de inscripción de dispositivos** (opcional) 
    Para limitar el número de dispositivos móviles que puede inscribir un usuario, inicie sesión en la [consola de administración de Microsoft Intune](http://manage.microsoft.com), haga clic en **Administración** &gt; **Administración de dispositivos móviles** &gt; **Reglas de inscripción**. Seleccione el número máximo de dispositivos que un usuario puede inscribir y haga clic en **Guardar**.

8.  **Establecer la configuración del portal de empresa** 
     Puede personalizar Portal de empresa de Intune para su empresa. En la [consola de administrador de Microsoft Intune](http://manage.microsoft.com), haga clic en **Administración** &gt; **Portal de empresa**. Configure lo siguiente

    -   **Nombre de compañía**

    -   **Nombre del contacto del departamento de TI**

    -   **Número de teléfono del departamento de TI**

    -   **Información adicional**

    -   **Dirección URL de la declaración de privacidad de la empresa**

    -   **Dirección URL del sitio web de soporte técnico (no se muestra)**

    -   **Nombre del sitio web**

9. [!INCLUDE[CPEnrollmentTermsAndConditions](../Token/CPEnrollmentTermsAndConditions_md.md)]

10. **Indicar a los usuarios cómo acceder a los recursos de empresa con el portal de empresa** 
    Los usuarios necesitan saber cómo inscribir sus dispositivos y qué esperar una vez que se incorporan a la administración.[Qué decirles a los usuarios finales sobre el uso de Microsoft Intune](../Topic/What-to-tell-your-end-users-about-using-Microsoft-Intune.md)

## Vea también
[Preparar la inscripción de dispositivos en Microsoft Intune](../Topic/Get-ready-to-enroll-devices-in-Microsoft-Intune.md)

