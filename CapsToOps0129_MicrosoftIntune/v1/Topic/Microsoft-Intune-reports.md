---
title: Comprender las operaciones de Microsoft Intune mediante informes
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 857309c2-61c9-4c22-becf-4839fedeaece
---
# Comprender las operaciones de Microsoft Intune mediante informes
Utilice la información de este tema como ayuda para crear y administrar informes de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] que proporcionan información acerca del software, el hardware y las licencias de software en la organización.

## Uso de informes
Los informes de [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] proporcionan información acerca del software, el hardware y las licencias de software de la organización. Los informes pueden ayudar a confirmar las necesidades actuales y pronosticar gastos futuros. El área de trabajo **Informes** proporciona las herramientas para crear y administrar los informes. Para obtener más información sobre informes, consulte [Comprender las operaciones de Microsoft Intune mediante informes](../Topic/Understand-Microsoft-Intune-operations-by-using-reports.md).

### Report types (Tipos de informes)

|Tipo de informe|Descripción|
|-------------------|---------------|
|**Informes de actualización**|Muestra las actualizaciones de software que se realizaron correctamente en los equipos de su organización, además de las actualizaciones con error, las pendientes o las que se necesitan. Para obtener más información acerca de las actualizaciones de software, consulte [Mantener los equipos Windows al día con las actualizaciones de software de Microsoft Intune](../Topic/Keep-Windows-PCs-up-to-date-with-software-updates-in-Microsoft-Intune.md).|
|**Informes de software detectado**|Muestra el software instalado en los equipos de la organización e incluye las versiones de software. Puede filtrar la información mostrada en función de la compañía de software y la categoría de software. Puede hacer clic en la flecha situada junto al elemento de lista para expandir las actualizaciones de la lista a fin de mostrar más detalles (como los equipos en los que están instaladas). **Note:** Al retirar equipos o cambiar su pertenencia a grupos en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], los cambios pueden tardar varios minutos en quedar reflejados en el informe de software detectado. Para que los datos de inventario de software sean más precisos, espere unos minutos después de retirar equipos o cambiar su pertenencia a grupos antes de ejecutar un informe de software detectado que incluya dichos equipos.|
|**Informes de inventario de equipos**|Muestra información sobre los equipos administrados en su organización. Use este informe para planear las compras de hardware y comprender mejor las necesidades de hardware de los usuarios de la organización. Para obtener más información acerca del uso de los equipos administrados, consulte [Administrar equipos Windows con Microsoft Intune](../Topic/Manage-Windows-PCs-with-Microsoft-Intune.md).|
|**Informes de inventario de dispositivos móviles**|Muestra información sobre los dispositivos móviles en la organización. Puede filtrar la información mostrada en función de los grupos, si el dispositivo está desbloqueado o es un dispositivo raíz, y según sistema operativo.|
|**Informes de adquisición de licencias**|Muestra los títulos de software para todo el software con licencia de los grupos de licencias seleccionados, basándose en sus contratos de licencia. Los filtros disponibles son:<br /><br />-   **Todos los contratos** muestra todos los productos de software con licencia que son administrados por [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].<br />-   **Contratos de licencias por volumen** muestra solo productos de software VLSC.<br />-   **Otros contratos de licencias de software** muestra productos de software que se administran fuera de VLSC. **Note:** Si la información de la licencia de software no se ha actualizado en más de 24 horas, se actualizará cuando se genere un informe de licencias.<br />Un informe de licencia no es un cálculo exacto de los títulos de software que se utilizan ni constituye una prueba del cumplimiento de los contratos. El informe es una herramienta que facilita la toma de decisiones sobre las licencias de su organización.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] podría no detectar algunos productos que pueden tener una licencia por volumen de Microsoft.|
|**Informes de instalación de licencias**|Compara el software instado en los equipos de la organización con la cobertura actual del acuerdo de licencia según el Centro de servicios de licencias por volumen (VLSC). Los filtros incluyen:<br /><br />-   **Todos los contratos** muestra todos los productos de software con licencia que son administrados por [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].<br />-   **Contratos de licencias por volumen** muestra solo productos de software VLSC.<br />-   **Otros contratos de licencias de software** muestra productos de software que se administran fuera de VLSC.|
|**Informes de términos y condiciones**|Muestra si los usuarios han aceptado los términos y condiciones implementados y qué versión han aceptado. Puede especificar hasta 10 usuarios cuya aceptación de los términos y condiciones que se implementaron en ellos se muestran o mostrar el estado de aceptación para un término determinado implementado.|
|**Informes de aplicaciones no compatibles**|Muestra información acerca de los usuarios que tienen aplicaciones instaladas que se encuentran en las listas de las aplicaciones compatibles y no compatibles. Utilice este informe para buscar usuarios y dispositivos que no cumplan las directivas de aplicación de la empresa.|
|**Informes de cumplimiento de certificados**|Muestra los certificados que se han emitido a los usuarios y dispositivos a través del servicio de inscripción de dispositivos de red. Utilice este informe para buscar certificados que se hayan emitido, hayan expirado o se hayan revocado.|
|**Informes del historial de dispositivos**|Muestra un registro histórico de las acciones de retirada, borrado y eliminación. Use este informe para ver quién inició dichas acciones en los dispositivos en algún momento anterior.|
|**Informe de hardware de Mac OS X**|Muestra los detalles de hardware para todos los dispositivos Mac OS X inscritos de los grupos que seleccione. Para información sobre el inventario de hardware recopilado de estos dispositivos, vea [Supervisar dispositivos móviles con Microsoft Intune](../Topic/Understand-your-devices-with-inventory-in-Microsoft-Intune.md).|
|**Informe del software de Mac OS X**|Muestra el software instalado en todos los dispositivos Mac OS X de los grupos seleccionados. El informe muestra:<br /><br />-   El nombre del software (como un id. de paquete)<br />-   El nombre de versión corta (o descriptivo)<br />-   La versión<br />-   El número de dispositivos con el software instalado|

#### Para crear un informe

1.  En la [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)], haga clic en **Informes** y luego en el tipo de informe que desea generar, tal y como se describe en la tabla anterior.

2.  En la página **Crear nuevo informe**, acepte los valores predeterminados o personalícelos para filtrar los resultados devueltos por el informe. Por ejemplo, puede seleccionar que en el informe de software detectado solo se muestre el software publicado por Microsoft.

3.  Haga clic en **Ver informe** para abrir el informe en una nueva ventana.

Para ordenar el informe por cualquiera de las columnas mostradas, haga clic en el encabezado de la columna. Además, algunos informes permiten expandir elementos de la lista para mostrar más detalles.

## Más acciones de los informe
Además, los informes admiten las siguientes acciones:

|Acción|Más información|
|----------|-------------------|
|**Imprimir**|En un informe abierto, haga clic en el icono de impresión y siga las instrucciones.|
|**Exportar**|En un informe abierto, haga clic en el icono de exportación y siga las instrucciones. Puede exportar un informe en formato de valores separados por comas (.csv) o HTML.|
|**Guardar**|En la página **Crear nuevo informe**, cada usuario puede guardar hasta 100 informes. Configure los parámetros del informe según sus requisitos y, a continuación, haga clic en **Guardar** o bien en **Guardar como** si desea utilizar un nombre diferente.|
|**Cargar**|En la página **Crear nuevo informe**, haga clic en **Cargar** para recuperar cualquier conjunto de parámetros de informe previamente guardado.|
|**Eliminar**|En la esquina superior derecha del área de trabajo **Informes**, seleccione el tipo de informe deseado, haga clic en **Cargar**, desplácese hasta el nombre del informe que desea eliminar y haga clic en el icono de eliminación (x) junto al nombre del informe.|

## Vea también
[Supervisión e informes](../Topic/Monitoring-and-reports-with-Microsoft-Intune.md)

