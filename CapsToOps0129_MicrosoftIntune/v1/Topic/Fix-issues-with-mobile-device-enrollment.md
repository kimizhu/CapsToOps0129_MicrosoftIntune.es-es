---
title: Fix issues with mobile device enrollment
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e5979ab-fc4c-4c7b-a60c-15317496dfa2
robots: noindex,nofollow
---
# Fix issues with mobile device enrollment
Si tiene problemas en los dispositivos móviles, puede enviar registros a su administrador de TI para que le ayude a solucionar el problema.

## Si tiene un dispositivo Android
Los registros que se envían no incluyen su información personal a menos que habilite "registro detallado". Los registros incluirán la dirección de correo electrónico, pero ninguna otra información personal. Puede enviar registros mediante cualquiera de los métodos siguientes:

> [!IMPORTANT]
> El registro detallado está habilitado de forma predeterminada en el dispositivo. Si habilita el registro detallado en el dispositivo, los registros que envíe a partir de ese momento incluirán su dirección de correo electrónico (hasta que deshabilite el registro detallado).

### Opción 1 de Android

1.  Abra la aplicación del portal de empresa.

2.  Pulse en **Menú**. Podría tratarse de un botón de software o un botón de hardware según el dispositivo Android.

3.  En **Menú**, pulse en **Configuración** &gt; **Enviar datos**.

Se le pedirá que elija una aplicación de correo electrónico. La aplicación creará un correo electrónico con dirección previa con todos los registros necesarios adjuntos.

### Opción 2 de Android
Si recibe un error al intentar inscribir su dispositivo en Intune, puede intentarlo de nuevo pulsando en **Reintentar**. También puede enviar la información del error a su administrador de TI en un correo electrónico pulsando en **Enviar información**. Se crea automáticamente un correo electrónico dirigido al administrador de TI, con los registros necesarios para que el administrador pueda solucionar problemas en el dispositivo.

### Opción 3 de Android

1.  Use un cable USB para conectar el dispositivo a un equipo.

2.  En el equipo, busque un directorio que contenga el nombre del teléfono. En dicho directorio busque &lt;Android Device&gt;\Phone\Android\data\com.microsoft.windowsintune.companyportal\files\.

3.  Adjunte todos los archivos en un correo electrónico y envíelos a TI.

(**Nota para administradores:** proporcione su dirección de correo electrónico a sus usuarios finales).

## Si tiene un dispositivo Windows Phone 8.1

1.  Instale la aplicación Field Medic de la [Tienda de Windows Phone](http://www.windowsphone.com/en-us/store/app/field-medic/73c58570-d5a7-46f8-b1b2-2a90024fc29c).

2.  Abra Field Medic y pulse en **Avanzadas**.

3.  En **Categorías**, asegúrese de que **Enterprise** esté habilitado.

4.  Use el botón Atrás para volver a la página principal de Field Medic y pulse en **Iniciar registro**.

5.  Abra la configuración del teléfono y pulse en **Área de trabajo**. A continuación, pulse en **Inscrito**.

6.  En la pantalla nueva, haga clic en el botón **Sincronizar** tres veces.

7.  Vuelva a Field Medic y pulse en **Detener registro**. Asigne un nombre al registro y pulse en el icono **Guardar**.

8.  A continuación, use un cable USB para conectar el teléfono a su PC. En el equipo, abra el Explorador de archivos y abra **&lt;Nombre de teléfono&gt;** &gt; **Teléfono** &gt; **Documentos** &gt; **FieldMedic** &gt; **informes**.

9. Seleccione la carpeta más reciente, cópiela y adjúntela a un correo electrónico para su administrador de TI. Las carpetas se numeran de forma secuencial, WPB_000_yyyymmdd_xxxxx.

(Nota para el administrador: Si tiene un método preferido para compartir esta carpeta, como copiar a OneDrive, descríbalo aquí).

## Si tiene un dispositivo iOS

1.  Abra el portal de empresa.

2.  Agite el dispositivo y, en el menú emergente Diagnóstico, elija **Correo electrónico**. Se abrirá un nuevo mensaje con los registros como datos adjuntos. Envíe dicho mensaje al departamento de TI.

> [!TIP]
> Si el dispositivo no reacciona cuando lo agite, abra **Configuración** &gt; **Por empr** y asegúrese de que la opción **Gesto de sacudida** está activada.

