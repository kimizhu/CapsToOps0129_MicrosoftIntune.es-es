---
title: Solucionar problemas de acceso a los recursos de la empresa con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 40622ced-6029-4abf-873e-b51d2b51934c
---
# Solucionar problemas de acceso a los recursos de la empresa con Microsoft Intune
Utilice la información de este tema para que le resulte más fácil solucionar problemas cuando una acción de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] devuelva un código de error.

Si esta información no soluciona el problema, consulte [Cómo obtener asistencia para Microsoft Intune](../Topic/How-to-get-support-for-Microsoft-Intune.md) para descubrir otras formas de obtener ayuda.

## Códigos de error relacionados con el acceso a recursos de la compañía

### Códigos de estado de dispositivos de Windows administrados mediante MDM

|Código de estado|Mensaje de error|Qué hacer|
|--------------------|--------------------|-------------|
|10 (APP_CI_ENFORCEMENT_IN_PROGRESS)|Instalación en curso||
|20 (APP_CI_ENFORCEMENT_IN_PROGRESS_WAITING_CONTENT)|Esperando contenido||
|20 (APP_CI_ENFORCEMENT_IN_PROGRESS_WAITING_CONTENT)|Recuperando contenido|Causa probable: El estado del trabajo 30 indica un error de descarga de aplicación de un usuario.<br /><br />Las causas probables pueden ser:<br /><br />El dispositivo había perdido la conectividad de Internet mientras la descarga estaba en curso.<br /><br />Puede haber expirado el certificado emitido para el dispositivo en el momento de la inscripción.<br /><br />Mitigación:<br /><br />Inicie la aplicación Aplicaciones de empresa desde el Panel de Control del dispositivo para confirmar que el certificado del dispositivo no ha expirado; en caso afirmativo, deberá volver a inscribirlo.<br /><br />Compruebe que el dispositivo está conectado a Internet y pruebe a solicitar la aplicación de nuevo.|
|40 (APP_CI_ENFORCEMENT_IN_PROGRESS_CONTENT_DOWNLOADED)|Descarga de contenido completa||
|50 (APP_CI_ENFORCEMENT_IN_PROGRESS_INSTALLING)|Instalación en curso||
|60 (APP_CI_ENFORCEMENT_ERROR_INSTALLING)|InstalaciónSe produjo un error|Error en la instalación de la aplicación después de la descarga.<br /><br />El certificado de firma de código con el que se firmó la aplicación no está presente en el dispositivo.<br /><br />Una dependencia de marco de trabajo de la que depende la aplicación no se encuentra instalada en el dispositivo.<br /><br />Asegúrese de que el certificado de firma de código con el que se firmó la aplicación está presente en el dispositivo y confirme con el administrador que este certificado está destinado a todos los dispositivos de Windows RT inscritos de la empresa.<br /><br />Si el error de instalación se debe a la falta de una dependencia de marco de trabajo, el administrador tendrá que volver a publicar la aplicación y empaquetar el marco de trabajo junto con el paquete de aplicación.<br /><br />El paquete de aplicación descargado no es un paquete válido, puede estar dañado o no ser compatible con la versión del sistema operativo del dispositivo.|
|70 (APP_CI_ENFORCEMENT_SUCCEEDED)|Instalación correcta||
|80 (APP_CI_ENFORCEMENT_IN_PROGRESS)|Desinstalación en curso||
|90 (APP_CI_ENFORCEMENT_ERROR)|Se produjo un error de desinstalación||
|100 (APP_CI_ENFORCEMENT_SUCCEEDED)|Desinstalación correcta||
|110 (APP_CI_ENFORCEMENT_ERROR)|Error de coincidencia de hash de contenido||
|120 (APP_CI_ENFORCEMENT_ERROR)|SLK/instalación de prueba no habilitada||
|130 (APP_CI_ENFORCEMENT_ERROR)|Error de instalación de licencias MSADP||
|Ningún estado (APP_CI_ENFORCEMENT_UNKNOWN)|n/a|Se desconoce el estado actualmente.|

### Acceso a recursos de la compañía (errores comunes)

|Código de estado|Mensaje de error|
|--------------------|--------------------|
|-2016281101|Solicitud de CRP de MDM no encontrada|
|-2016281102|URL de NDES no encontrada|
|-2016281103|Certificado CRP de MDM no encontrado|
|-2016281104|Certificado CI de MDM no encontrado|
|-2016281105|No se pudo evaluar la Regla|
|-2016281106|No aplicable porque perdió en la resolución de conflictos|
|-2016281107|Origen de detección de configuración no admitido|
|-2016281108|La configuración a la que se hace referencia no se encontró en el elemento de configuración|
|-2016281109|Error de conversión de tipo de datos|
|-2016281110|Parámetro no válido para la configuración de CIM|
|-2016281111"|No se aplica a este dispositivo|
|-2016281112|Error de corrección|
|-2016330905|El estado de la aplicación es desconocido|
|-2016330906|La aplicación está administrada pero el usuario la ha quitado|
|-2016330907|El dispositivo está canjeando el código de canje|
|-2016330908|Error al instalar la aplicación|
|-2016330909|El usuario rechazó la oferta para actualizar la aplicación|
|-2016330910|El usuario rechazó la oferta para instalar la aplicación|
|-2016330911|El usuario ha instalado la aplicación antes de que se llevar a cabo la instalación de la aplicación administrada|
|-2016330912|La aplicación está programada para la instalación pero necesita un código de canje para completar la transacción|
|-2016341109|El dispositivo iOS ha devuelto un error|
|-2016341110|El dispositivo iOS ha rechazado el comando debido a un formato incorrecto|
|-2016341111|El dispositivo iOS ha devuelto un estado Inactivo inesperado|
|-2016341112|El dispositivo iOS está ocupado actualmente|

### Errores devueltos por dispositivos iOS

|Código de estado|Mensaje de error|
|--------------------|--------------------|
|-2016299111|Error interno|
|-2016299112|Error interno|
|-2016300111|36001: (error interno)|
|-2016300112|36000: La red de telefonía móvil ya está configurada|
|-2016301110|35002: Varias fuentes en una única carga|
|-2016301111|35001: Error al instalar las fuentes|
|-2016301112|35000: Datos de fuente no válidos|
|-2016302109|34003: El nombre principal Kerberos no es válido|
|-2016302110|34002: Falta el nombre principal Kerberos|
|-2016302111|34001: Modelo de coincidencia de dirección URL no válido|
|-2016302112|34000: Modelo de coincidencia de identificador de la aplicación no válido|
|-2016304112|32000: Demasiadas aplicaciones|
|-2016305111|31001: No se puede aplicar la configuración|
|-2016305112|31000: No se puede aplicar la credencial|
|-2016306111|30001: Tiempo de espera agotado|
|-2016306112|30000: Error en la autentificación|
|-2016307109|29003: Datos de certificado incorrectos|
|-2016307110|29002:|
|-2016307111|29001:|
|-2016307112|29000: El dispositivo no está supervisado|
|-2016308110|28002: No se puede establecer el papel tapiz|
|-2016308111|28001: Imagen de papel tapiz incorrecta|
|-2016308112|28000: Elemento desconocido|
|-2016310111|26001: Cifrado de nivel de archivos no admitido|
|-2016310112|26000: Cifrado de nivel de bloque no admitido|
|-2016311110|25002: No se puede quitar|
|-2016311111|25001: No se puede instalar|
|-2016311112|25000: Perfil incorrecto|
|-2016312109|24003: Perfil final incorrecto|
|-2016312110|24002: Carga de identidad incorrecta|
|-2016312111|24001: No se puede firmar el diccionario de atributos|
|-2016312112|24000: No se puede crear el diccionario de atributos|
|-2016313110|23002: Certificado de servidor no válido|
|-2016313111|23001: Respuesta del servidor incorrecta|
|-2016313112|23000: Identidad incorrecta|
|-2016314099|22013: Respuesta de la operación PKI no válida|
|-2016314100|22012: No se puede almacenar el certificado de CA|
|-2016314101|22011: No se puede generar el CSR|
|-2016314102|22010: No se puede almacenar la identidad temporal|
|-2016314103|22009: No se puede crear la identidad temporal|
|-2016314104|22008: No se puede crear la identidad|
|-2016314105|22007: Certificado firmado no válido|
|-2016314106|22006: CAP de CA insuficientes|
|-2016314107|22005: Error de red|
|-2016314108|22004: Configuración de certificado no admitida|
|-2016314109|22003: Respuesta de RA no válida|
|-2016314110|22002: Respuesta de CA no válida|
|-2016314111|22001: No se puede generar el par de claves|
|-2016314112|22000: Uso de clave no válido|
|-2016315105|21007: No se puede verificar la cuenta|
|-2016315106|21006: No se puede descifrar el certificado|
|-2016315107|21005: La cuenta no es única|
|-2016315108|21004: No se puede crear la cuenta|
|-2016315109|21003: Sin nombre de host|
|-2016315110|21002: No se puede cumplir con la directiva de cifrado del servidor|
|-2016315111|21001: No se puede cumplir con la directiva del servidor|
|-2016315112|21000: No se puede obtener la directiva del servidor|
|-2016316110|20002: La cuenta no es única|
|-2016316111|20001: Sin nombre de host|
|-2016316112|20000: No se puede crear la cuenta|
|-2016317110|19002: La cuenta no es única|
|-2016317111|19001: Sin nombre de host|
|-2016317112|19000: No se puede crear la cuenta|
|-2016318110|18002: Credenciales no válidas|
|-2016318111|18001: El host es inalcanzable|
|-2016318112|18000: Error desconocido|
|-2016319110|17002: La cuenta no es única|
|-2016319111|17001: Sin nombre de host|
|-2016319112|17000: No se puede crear la cuenta|
|-2016320110|16002: La cuenta no es única|
|-2016320111|16001: Sin nombre de host|
|-2016320112|16000: No se puede crear la suscripción|
|-2016321109|15003: Certificado no válido|
|-2016321110|15002: No se puede bloquear la configuración de red|
|-2016321111|15001: No se puede quitar la VPN|
|-2016321112|15000: No se puede instalar la VPN|
|-2016322110|14002: La configuración de la nube ya existe|
|-2016322111|14001: Dispositivo bloqueado|
|-2016322112|14000: Campo no válido|
|-2016323107|13005: No se puede configurar el proxy|
|-2016323108|13004: No se puede configurar EAP|
|-2016323109|13003: No se puede crear la configuración de Wi-Fi|
|-2016323110|13002: Se necesita una contraseña|
|-2016323111|13001: Se necesita un nombre de usuario|
|-2016323112|13000: No se puede instalar|
|-2016324070|12042: Código de config. regional desconocido|
|-2016324071|12041: Código de idioma desconocido|
|-2016324072|12040: Se necesita iniciar sesión en iTunes Store|
|-2016324073|12039: (sin usar)|
|-2016324074|12038: Aplicación no administrada|
|-2016324075|12037: Código de canje no válido|
|-2016324076|12036: No se puede quitar la aplicación en el estado actual|
|-2016324077|12035: No se puede comprar la aplicación|
|-2016324078|12034: La dirección URL no es HTTPS|
|-2016324079|12033: Manifiesto no válido|
|-2016324080|12032: Demasiadas aplicaciones en el manifiesto|
|-2016324081|12031: Instalación de la aplicación deshabilitada|
|-2016324082|12030: Dirección URL no válida|
|-2016324083|12029: Aplicación no administrada|
|-2016324084|12028: Sin esperar al canje|
|-2016324085|12027: No es una aplicación|
|-2016324086|12026: La aplicación ya está en cola|
|-2016324087|12025: La aplicación ya está instalada|
|-2016324088|12024: No se puedo validar el manifiesto de la aplicación|
|-2016324089|12023: No se pudo validar el Id. de la aplicación|
|-2016324090|12022: Tema no válido|
|-2016324091|12021: Tipo de solicitud no válida|
|-2016324092|12020: Sin autorización del servidor|
|-2016324093|12019: No se puede copiar el secreto de Escrow|
|-2016324094|12018: No se pueden copiar los datos del contenedor de claves de Escrow|
|-2016324095|12017: No se puede crear el contenedor de claves de Escrow|
|-2016324096|12016: Falta la identidad|
|-2016324097|12015: No se puede obtener el token de inserción|
|-2016324098|12014: El perfil de aprovisionamiento no está administrado|
|-2016324099|12013: El perfil no está administrado|
|-2016324100|12012: Error de coincidencia del reemplazo de MDM|
|-2016324101|12011: Configuración de MDM no válida|
|-2016324102|12010: Error de incoherencia interna|
|-2016324103|12009: Perfil de reemplazo no válido|
|-2016324104|12008: solicitud con formato incorrecto|
|-2016324105|12007: No autorizado|
|-2016324106|12006: Redireccionamiento rechazado|
|-2016324107|12005: No se puede encontrar el certificado|
|-2016324108|12004: Certificado de inserción no válido|
|-2016324109|12003: Respuesta de desafío no válida|
|-2016324110|12002: No se puede proteger|
|-2016324111|12001: Varias instancias MDM|
|-2016324112|12000: Derechos de acceso no válidos|
|-2016325111|11001: El APN personalizado ya está instalado|
|-2016325112|11000: No se puede instalar el APN|
|-2016326111|10001: Firmante no válido|
|-2016326112|10000: No se pueden instalar los valores predeterminados|
|-2016327106|9006: El certificado no es una identidad|
|-2016327107|9005: El certificado tiene un formato incorrecto|
|-2016327108|9004: No se puede almacenar el certificado raíz|
|-2016327109|9003: No se pueden almacenar los datos WAPI|
|-2016327110|9002: No se puede almacenar el certificado|
|-2016327111|9001: Hay demasiados certificados en una carga|
|-2016327112|9000: Contraseña no válida|
|-2016328112|8000: No se puede instalar la imagen de web|
|-2016329105|7007: La cuenta SMTP no está configurada correctamente|
|-2016329106|7006: La cuenta POP no está configurada correctamente|
|-2016329107|7005: La cuenta IMAP no está configurada correctamente|
|-2016329108|7004: El certificado SMIME es incorrecto|
|-2016329109|7003: Falta el certificado SMIME|
|-2016329110|7002: Ocurrió un error desconocido durante la validación|
|-2016329111|7001: Credenciales no válidas|
|-2016329112|7000: El host es inalcanzable|
|-2016330110|6002: No se puede crear la consulta|
|-2016330111|6001: Cadena vacía|
|-2016330112|6000: Error del sistema en la cadena de claves|
|-2016331097|5015: No se puede establecer el período de gracia|
|-2016331098|5014: No se puede establecer código de acceso|
|-2016331099|5013: No se puede borrar el código de acceso|
|-2016331100|5012: (sin usar)|
|-2016331101|5011: Código de acceso incorrecto|
|-2016331102|5010: Dispositivo bloqueado|
|-2016331103|5009: (sin usar)|
|-2016331104|5008: El código de acceso es demasiado reciente|
|-2016331105|5007: Código de acceso expirado|
|-2016331106|5006: El código de acceso necesita caracteres alfabéticos|
|-2016331107|5005: El código de acceso necesita un número|
|-2016331108|5004: El código de acceso tiene caracteres ascendentes y descendentes|
|-2016331109|5003: El código de acceso tiene caracteres repetidos|
|-2016331110|5002: Muy pocos caracteres complejos|
|-2016331111|5001: Muy pocos caracteres únicos|
|-2016331112|5000: El código de acceso es demasiado corto|
|-2016332093|4019: Varias cargas de bloqueo de aplicaciones|
|-2016332094|4018: Varias cargas APN o de red de telefonía móvil|
|-2016332095|4017: Varias cargas de proxy HTTP global|
|-2016332096|4016: (Error interno)|
|-2016332097|4015: El perfil de sustitución no contiene una carga MDM|
|-2016332098|4014: No hay ninguna identidad de dispositivo disponible|
|-2016332099|4013: Error al actualizar|
|-2016332100|4012: El perfil no se puede actualizar|
|-2016332101|4011: El perfil final no es un perfil de configuración|
|-2016332102|4010: El perfil actualizado no tiene el mismo identificador|
|-2016332103|4009: Dispositivo bloqueado|
|-2016332104|4008: Certificados no coincidentes|
|-2016332105|4007: Formato de archivo no reconocido|
|-2016332106|4006: La fecha de eliminación del perfil está en el pasado|
|-2016332107|4005: El código de acceso no es compatible|
|-2016332108|4004: El usuario canceló la instalación|
|-2016332109|4003: El perfil no está en cola para la instalación|
|-2016332110|4002: UUID duplicado|
|-2016332111|4001: Error al instalar|
|-2016332112|4000: No se puede analizar el perfil|
|-2016333111|3001: El sensor de comparación de valor no es coherente (error interno)|
|-2016333112|3000: El sensor de restricción no es coherente (error interno)|
|-2016334108|2004: Valor de campo no admitido|
|-2016334109|2003: Tipo de datos incorrectos en el campo|
|-2016334110|2002: Falta el campo obligatorio|
|-2016334111|2001: Versión de carga no admitida|
|-2016334112|2000: Carga con formato incorrecto|
|-2016335102|1010: Valor de campo no admitido|
|-2016335103|1009: Error en la instalación del perfil|
|-2016335104|1008: Los identificadores de carga no son únicos|
|-2016335105|1007: Los UUID no son únicos|
|-2016335106|1006: No se puede descifrar|
|-2016335107|1005: Perfil vacío|
|-2016335108|1004: Firma incorrecta|
|-2016335109|1003: Tipo de datos incorrectos en el campo|
|-2016335110|1002: Falta el campo obligatorio|
|-2016335111|1001: Versión de perfil no admitido|
|-2016335112|1000: Perfil con formato incorrecto|

### Códigos de respuesta OMA

|Código de estado|Mensaje de error|
|--------------------|--------------------|
|-2016344008|(1404): se ha denegado el acceso al certificado|
|-2016344009|(1403): no se encuentra el certificado|
|-2016344010|DCMO(1402): Error de la operación|
|-2016344011|DCMO(1401): el usuario eligió no aceptar la operación cuando se le solicitó|
|-2016344012|DCMO(1400): error de cliente|
|-2016344108|DCMO(1204): la funcionalidad del dispositivo está deshabilitada y el usuario puede volver a habilitarla|
|-2016344109|DCMO(1203): la funcionalidad del dispositivo está deshabilitada y el usuario no puede volver a habilitarla|
|-2016344110|DCMO(1202): la operación de habilitación finalizó correctamente pero la funcionalidad del dispositivo está desconectada|
|-2016344111|DCMO(1201): la operación de habilitación finalizó correctamente y la funcionalidad del dispositivo está asociada|
|-2016344112|DCMO(1200): la operación finalizó correctamente|
|-2016345595|Syncml(517): la respuesta a un comando atómico fue demasiado grande para un único mensaje.|
|-2016345596|Syncml(516): el comando estaba dentro de un elemento atómico y se produjo un error del mismo. El comando no se revirtió correctamente.|
|-2016345598|Syncml(514):  el comando SyncML no se completó correctamente porque la operación se canceló antes de procesar el comando.|
|-2016345599|Syncml(513): el destinatario no admite o rechaza la versión especificada del protocolo de sincronización de SyncML que se usa en el mensaje de solicitud de SyncML.|
|-2016345600|Syncml(512): error de aplicación durante la sesión de sincronización.|
|-2016345601|Syncml(511): error grave en el servidor al procesar la solicitud.|
|-2016345602|Syncml(510): error al procesar la solicitud. El error está relacionado con un error en el almacén de datos del destinatario.|
|-2016345603|Syncml(509): Reservado para su uso en el futuro:|
|-2016345604|Syncml(508): se produjo un error que necesita una actualización del estado de sincronización actual del cliente con el servidor.|
|-2016345605|Syncml(507): el error hizo que todos los comandos de SyncML en un tipo de elemento atómico finalizaran incorrectamente.|
|-2016345606|Syncml(506): error de aplicación al procesar la solicitud.|
|-2016345607|Syncml(505): el destinatario no admite o rechaza admitir la versión especificada del DTD de SyncML que se usa en el mensaje de solicitud de SyncML.|
|-2016345608|Syncml(504): el destinatario, mientras actuaba como puerta de enlace o proxy, no recibió una respuesta puntual del destinatario ascendente especificado por el URI (por ejemplo, HTTP, FTP o LDAP) u otro destinatario auxiliar (por ejemplo, DNS) al que necesitaba obtener acceso para satisfacer la solicitud.|
|-2016345609|Syncml(503): el destinatario no puede controlar la solicitud porque está temporalmente sobrecargado o se está realizando el mantenimiento del mismo.|
|-2016345610|Syncml(502): el destinatario, mientras actuaba como puerta de enlace o proxy, recibió una respuesta no válida del destinatario ascendente al que obtuvo acceso para satisfacer la solicitud.|
|-2016345611|Syncml(501): el destinatario no admite el comando requerido para satisfacer la solicitud.|
|-2016345612|Syncml(500): el destinatario detectó una condición inesperada que le impidió satisfacer la solicitud|
|-2016345684|Syncml(428): no se pudo mover|
|-2016345685|Syncml(427): el elemento primario no se puede eliminar porque contiene elementos secundarios.|
|-2016345686|Syncml(426): elemento parcial no aceptado.|
|-2016345687|Syncml(425): error del comando solicitado porque el remitente no tiene permisos de control de acceso (ACL) adecuados en el destinatario.|
|-2016345688|Syncml(424): el objeto fragmentado se recibió, pero el tamaño del objeto recibido no coincidió con el tamaño declarado en el primer fragmento.|
|-2016345689|Syncml(423): error del comando solicitado porque el elemento que se eliminó temporalmente se había eliminado permanentemente previamente en el servidor.|
|-2016345690|Syncml(422): error en el servidor del comando solicitado porque el formato de script CGI en LocURI era incorrecto.|
|-2016345691|Syncml(421): error en el servidor del comando solicitado porque la gramática de búsqueda especificada era desconocida.|
|-2016345692|Syncml(420): el destinatario no dispone de más espacio de almacenamiento para los datos de sincronización restantes.|
|-2016345693|Syncml(419): la solicitud de cliente creó un conflicto que se resolvió al imponerse el comando del servidor.|
|-2016345694|Syncml(418): error del comando Put o Add porque el destino ya existe.|
|-2016345695|Syncml(417): error de solicitud. El originador debe reintentar la solicitud más tarde.|
|-2016345696|Syncml(416): error de la solicitud porque el tamaño de bytes especificado en la solicitud es demasiado grande.|
|-2016345697|Syncml(415): tipo o formato de soporte no admitido.|
|-2016345698|Syncml(414): error del comando solicitado porque la longitud del URI de destino es mayor que la que el destinatario puede o desea procesar.|
|-2016345699|Syncml(413): el destinatario rechaza realizar el comando solicitado porque el tamaño del elemento solicitado es mayor que el que el destinatario puede o desea procesar.|
|-2016345700|Syncml(412): error del comando solicitado en el destinatario porque estaba incompleto o su formato era incorrecto.|
|-2016345701|Syncml(411): información de longitud o tamaño de bytes en el tipo de elemento Meta debe acompañar al comando solicitado.|
|-2016345702|Syncml(410): el destino solicitado ya no está en el destinatario y no se conoce ningún URI de reenvío.|
|-2016345703|Syncml(409): error de solicitud porque se produjo un conflicto de actualizaciones entre las versiones de datos de cliente y servidor.|
|-2016345704|Syncml(408): no se recibió un mensaje previsto en el periodo de tiempo necesario.|
|-2016345705|Syncml(407): error del comando solicitado debido a que el originador debe proporcionar la autenticación correcta.|
|-2016345706|Syncml(406): error del comando solicitado porque una característica opcional en la solicitud no se admite.|
|-2016345707|Syncml(405): El comando solicitado no se admite en el destino.|
|-2016345708|Syncml(404): el destino solicitado no se encontró.|
|-2016345709|Syncml(403): error del comando solicitado, pero el destinatario entendió el comando solicitado.|
|-2016345710|Syncml(402): error del comando solicitado porque es preciso realizar el pago correspondiente.|
|-2016345711|Syncml(401): error del comando solicitado porque el solicitante debe proporcionar la autenticación correcta.|
|-2016345712|Syncml(400): el comando solicitado no se pudo realizar porque el formato de la sintaxis del comando es incorrecto.|
|-2016345807|Syncml(305): se debe obtener acceso al destino solicitado mediante el proxy de URI especificado.|
|-2016345808|Syncml(304): el comando SyncML solicitado no se ejecutó en el destino.|
|-2016345809|Syncml(303): el destino solicitado se puede encontrar en otro URI.|
|-2016345810|Syncml(302): el destino solicitado se ha movido temporalmente a otro URI.|
|-2016345811|Syncml(301): el destino solicitado tiene un nuevo URI.|
|-2016345812|Syncml(300): el destino solicitado es uno de varios destinos solicitados alternativos.|
|-2016345896|Syncml(216): error de Atomic debido a un comando que estaba dentro del elemento Atomic. El comando se revirtió correctamente.|
|-2016345897|Syncml(215): no se ejecutó un comando debido a la interacción del usuario, que decidió no aceptar la elección.|
|-2016345898|Syncml(214): operación cancelada. El comando SyncML se realizó correctamente, pero no se procesarán más comandos en esta sesión.|
|-2016345899|Syncml(213): se aceptó y se almacenó en búfer el elemento fragmentado.|
|-2016345900|Syncml(212): autenticación aceptada; no será necesario autenticarse de nuevo durante el resto de la sesión de sincronización. Este código de respuesta solo se puede usar para responder a una solicitud en la que se proporcionan credenciales.|
|-2016345901|Syncml(211): elemento no eliminado. No se encontró el elemento solicitado. Es posible que se haya eliminado previamente.|
|-2016345902|Syncml(210): eliminación sin archivar. La respuesta indica que los datos solicitados se eliminaron correctamente pero que no se archivaron antes de su eliminación porque esta característica OPCIONAL no es compatible con la implementación.|
|-2016345903|conflicto resuelto con duplicado. La respuesta indica que la solicitud generó un conflicto de actualización que se resolvió con una duplicación de los datos del cliente que se estaban creando en la base de datos del servidor. La respuesta incluye el URI de destino del duplicado en el elemento del estado. Además, en el caso de una sincronización bidireccional, se devuelve un comando Add con la definición de datos duplicados.|
|-2016345904|conflicto resuelto a favor del comando del cliente. La respuesta indica que se produjo un conflicto de actualización que se resolvió a favor del comando del cliente.|
|-2016345905|conflicto resuelto con combinación. La respuesta indica que la solicitud ha generado un conflicto que se ha resuelto con la combinación de las instancias de datos del cliente y del servidor. La respuesta incluye las URL de destino y origen del elemento de estado. Además, se devuelve un comando Replace con los datos combinados.|
|-2016345906|la respuesta indica que solo se completó parte del comando. Si el resto del comando se puede completar más tarde, una vez que finalice se DEBE crear un código apropiado de estado de solicitud de finalización.|
|-2016345907|el origen DEBE actualizar su contenido. Se informa al originador de la solicitud de que su contenido DEBE sincronizarse para obtener una versión actualizada.|
|-2016345908|la solicitud se completó correctamente, pero no se devolvieron datos. El código de respuesta también se devuelve como respuesta a un comando Get cuando el destino carece de contenido.|
|-2016345909|respuesta no autoritativa. La entidad que responde a la solicitud no es la de destino. La respuesta solo se devolverá cuando la solicitud genere un código de respuesta 200 por parte del destino autoritativo.|
|-2016345910|aceptado para procesamiento. La solicitud para ejecutar una aplicación de forma remota o para alertar a un usuario o aplicación se realizó correctamente.|
|-2016345911|se agregó el elemento solicitado.|
|-2016345912|el comando SyncML se realizó correctamente.|
|-2016346011|el comando SyncML se está realizando, pero todavía no ha finalizado.|

## Vea también
[Habilitar el acceso a los recursos de empresa con Microsoft Intune](../Topic/Enable-access-to-company-resources-with-Microsoft-Intune---deleted.md)

