---
title: Introducci&#243;n a Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b4e778d-ac13-4c23-974f-5122f74626bc
robots: noindex,nofollow
---
# Introducci&#243;n a Microsoft Intune
![](../Image/Nav-Icons/WIT_Tile_W_OverviewHighlight.png)[![](../Image/Nav-Icons/WIT_Tile_W_GetStarted.png)](https://technet.microsoft.com/library/dn646953.aspx/?WT.mc_id=IntuneGS20150801)[![](../Image/Nav-Icons/WIT_Tile_W_EnrollDevices.png)](https://technet.microsoft.com/library/dn646962.aspx/?WT.mc_id=IntuneEnroll20150801)[![](../Image/Nav-Icons/WIT_Tile_W_ManageDevices.png)](https://technet.microsoft.com/library/mt313202.aspx/?WT.mc_id=IntuneConfig20150801)[![](../Image/Nav-Icons/WIT_Tile_W_ManageApps.png)](https://technet.microsoft.com/library/dn646965.aspx/?WT.mc_id=IntuneDeploy20150801)[![](../Image/Nav-Icons/WIT_Tile_W_ProtectResources.png)](https://technet.microsoft.com/library/mt313203.aspx/?WT.mc_id=IntuneProtect20150801)[![](../Image/Nav-Icons/WIT_Tile_W_RetireData.png)](https://technet.microsoft.com/library/mt313204.aspx/?WT.mc_id=IntuneRetire20150801)[![](../Image/Nav-Icons/WIT_Tile_W_TechnicalReference.png)](https://technet.microsoft.com/library/mt282239.aspx/?WT.mc_id=IntuneTR20150801)[![](../Image/Nav-Icons/WIT_Tile_W_Troubleshooting.png)](https://technet.microsoft.com/library/mt345521.aspx)
![](../Image/Nav-Icons/WIT_Tile_Bar_Overview.png)

[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] es un servicio basado en la nube que permite administrar dispositivos móviles, equipos y aplicaciones, de forma que los usuarios puedan ser productivos al mismo tiempo que se protege la información de su empresa.

La administración de dispositivos móviles (MDM) y la administración de equipos Windows son la piedra angular del departamento de TI moderno. Hoy en día, trabajadores, personal y alumnos tienen más movilidad y están más involucrados que nunca. Su éxito depende de poder entregar la información donde sea necesaria, a la vez que se aseguran que estará protegida. Debe implementar aplicaciones, proteger dispositivos, asegurarse de que las actualizaciones se apliquen y aprovisionar el correo electrónico con mayor rapidez que nunca mientras defiende la información de la empresa.

## Diferentes maneras de administrar dispositivos con Microsoft Intune
Tiene varias opciones a la hora de usar Intune. En este breve vídeo se muestra cómo Intune se adapta la red existente facilitando la administración de dispositivos y aplicaciones.

[![](../Image/IT_MDM_MAMOverview2.png)](https://youtu.be/kLi3uZ_pK-g)

Obtenga más información sobre lo que Intune ofrece, como lo siguiente:

-   **Una solución independiente de administración de dispositivos**. Al tratarse de un servicio basado en la nube, podrá administrar dispositivos y proteger los datos de la compañía sin la sobrecarga de los costos de infraestructura de red.

    Intune puede administrar dispositivos iOS, Android, Mac OS X y Windows Phone, así como dispositivos Windows RT, Windows 8.1 y Windows 10 como dispositivos móviles. Si está pensando en [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] como solución de administración de dispositivos móviles (MDM), consulte [Capacidades de administración de dispositivos móviles en Microsoft Intune](https://technet.microsoft.com/library/dn600287.aspx).

    Puede instalar el software cliente de [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] en equipos Windows para habilitar la administración. Una vez administrado un equipo, puede implementar actualizaciones de aplicaciones y software, administrar Endpoint Protection y Firewalls de Windows, proporcionar asistencia remota y mucho más. Vea [una lista completa de funciones de administración de equipos](http://technet.microsoft.com/library/dn646975.aspx).

    También puede usar Intune para [implementar y administrar aplicaciones](https://technet.microsoft.com/library/dn646965.aspx). La administración de aplicaciones le ayuda a evitar que los datos se compartan fuera de la empresa restringiendo acciones (como copiar, cortar, pegar y guardar como) entre aplicaciones administradas por Intune y aplicaciones personales. Esta protección de datos se integra directamente en muchas aplicaciones móviles de Microsoft, pero puede [ ampliar la protección de datos a las aplicaciones de línea de negocio existentes con la Herramienta de ajuste de aplicaciones de Intune](https://technet.microsoft.com/library/dn878026.aspx). También puede establecer la visualización de contenido seguro con el [Explorador administrado de Intune](https://technet.microsoft.com/library/dn878029.aspx). Para proteger aún más la información corporativa, puede [borrar de forma selectiva las aplicaciones administradas y los datos relacionados con ellas](https://technet.microsoft.com/library/mt313204.aspx) en dispositivos que han cancelado la inscripción, que ya no son compatibles o que se han perdido, sustraído o retirado del uso.

-   **Una extensión de nube de Microsoft System Center 2012 Configuration Manager**. Si ya usa Configuration Manager para administrar los dispositivos locales y está buscando una forma de poder administrar muchos de los dispositivos móviles actuales, puede [usar Intune como extensión de System Center 2012 Configuration Manager](https://technet.microsoft.com/library/dn957912.aspx#BKMK_HybridOfferings). Dos ventajas clave de esta opción son la experiencia de administración unificada tanto para administrar dispositivos locales como dispositivos móviles y la escala. Esta implementación híbrida de Intune le ofrece la capacidad de administrar más de 50.000 dispositivos.

-   **Parte de su suscripción de Microsoft Office 365**. Si tiene una suscripción comercial a Office 365, puede usar las [capacidades de administración de dispositivos móviles integradas en Office 365](https://technet.microsoft.com/library/dn957912.aspx#MDMOfferings) de Intune. A pesar de no ser una opción tan amplia como Intune independiente o Intune y Configuration Manager, igualmente podrá administrar dispositivos iOS, Android y Windows Phone, crear directivas de seguridad, limitar el acceso al correo electrónico de Office 365 y los documentos en los dispositivos administrados y usar el borrado selectivo para quitar Office 365 de los dispositivos administrados.

-   **Parte de Microsoft Enterprise Mobility Suite**. La movilidad ha llegado para quedarse, y lo mismo puede decirse de la nube. Intune es un componente esencial de [Microsoft Enterprise Mobility Suite (EMS)](https://www.microsoft.com/en-us/server-cloud/enterprise-mobility/overview.aspx%20), un conjunto de servicios en la nube que proporciona detección de amenazas, administración de identidades por encima de la protección de datos y la administración de dispositivos que se entrega con Intune independiente.

## Requisitos para la instalación de Intune
Aunque Intune es un servicio y, como tal, evita muchos de los costos de infraestructura, es posible que aún tenga que cumplir algunos [requisitos de configuración de red](https://technet.microsoft.com/library/dn646950.aspx). Por ejemplo, el firewall podría, de forma predeterminada, bloquear algunos de los puertos de red que [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] necesita.  Además, si desea sincronizar los datos de Exchange Server, también habrá ciertas excepciones de firewall que tendrá que establecer.

Otros de los preparativos que deberá hacer al [prepararse para implementar Intune](https://technet.microsoft.com/library/dn646966.aspx) son los siguientes:

-   configurar un portal de empresa, de forma que los usuarios puedan inscribir sus dispositivos móviles para que Intune los administre

-   comprender el uso del ancho de banda esperado

-   decidir entre usar el nombre de dominio predeterminado **onmicrosoft.com** y otro nombre de dominio de su propiedad

## Vea también
[Guía de las consideraciones de diseño de administración de dispositivos móviles](https://technet.microsoft.com/en-us/library/mt143180.aspx)
[Documentación de Microsoft Intune](../Topic/Documentation-for-Microsoft-Intune.md)

