---
title: Retirar datos y dispositivos de la administraci&#243;n de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3dbec400-5d8a-47be-b892-7745811d9de2
---
# Retirar datos y dispositivos de la administraci&#243;n de Microsoft Intune
[![](../Image/Nav-Icons/WIT_Tile_W_Overview.png)](https://technet.microsoft.com/library/dn646960.aspx/?WT.mc_id=IntuneOverview20150801)[![](../Image/Nav-Icons/WIT_Tile_W_GetStarted.png)](https://technet.microsoft.com/library/dn646953.aspx/?WT.mc_id=IntuneGS20150801)[![](../Image/Nav-Icons/WIT_Tile_W_EnrollDevices.png)](https://technet.microsoft.com/library/dn646962.aspx/?WT.mc_id=IntuneEnroll20150801)[![](../Image/Nav-Icons/WIT_Tile_W_ManageDevices.png)](https://technet.microsoft.com/library/mt313202.aspx/?WT.mc_id=IntuneConfig20150801)[![](../Image/Nav-Icons/WIT_Tile_W_ManageApps.png)](https://technet.microsoft.com/library/dn646965.aspx/?WT.mc_id=IntuneDeploy20150801)[![](../Image/Nav-Icons/WIT_Tile_W_ProtectResources.png)](https://technet.microsoft.com/library/mt313203.aspx/?WT.mc_id=IntuneProtect20150801)![](../Image/Nav-Icons/WIT_Tile_W_RetireDevicesHighlight.png)[![](../Image/Nav-Icons/WIT_Tile_W_TechnicalReference.png)](https://technet.microsoft.com/library/mt282239.aspx/?WT.mc_id=IntuneTR20150801)[![](../Image/Nav-Icons/WIT_Tile_W_Troubleshooting.png)](https://technet.microsoft.com/library/mt345521.aspx)
![](../Image/Nav-Icons/WIT_Banner_RetireDevices.png)

Llega un momento en que un empleado abandona o bien la empresa o bien su dispositivo. En tales casos, deberá poder garantizar que ni el empleado ni otra persona que use el dispositivo pueda tener acceso a los recursos de la empresa. También es posible que desee asegurarse de quitar toda la información de la empresa del dispositivo.

## Protección de datos de empresa en dispositivos perdidos o robados
Cuando un empleado pierde un dispositivo móvil o se lo roban, la primera preocupación es asegurarse de que no se pueda leer la información de la empresa. También querrá asegurarse de que el dispositivo no se pueda usar para iniciar sesión en los recursos de la empresa. Tiene varias opciones:

-   Puede [borrar los datos y las aplicaciones de la empresa](https://technet.microsoft.com/library/jj676679.aspx) que seleccione del dispositivo. Esta es la acción preferida para los empleados que inscribieron sus propios dispositivos en Intune, porque no afecta a la información personal del dispositivo. El borrado selectivo también quita el dispositivo de Intune, lo que significa que ya no tendrá las credenciales necesarias para iniciar sesión en los recursos de la empresa, como Microsoft SharePoint, el correo electrónico u Office 365.

-   También puede realizar un borrado completo, que [ restablece la configuración de fábrica en dicho dispositivo](https://technet.microsoft.com/library/jj676679.aspx). Con esto se asegura de que ningún dato, personal o corporativo, caiga en las manos equivocadas; esta es la acción preferida para dispositivos que son propiedad de la empresa. También quita el dispositivo de Intune.

**Restablecer los códigos de acceso cuando los usuarios quedan bloqueados fuera de sus dispositivos**
Dado que el primer paso para proteger los datos de la empresa en dispositivos móviles es requerir un código de acceso para poder usar el dispositivo, a veces será necesario [restablecer un código de acceso](https://technet.microsoft.com/library/jj676679.aspx#BKMK_passcode) o ayudar a un empleado a hacerlo, ya sea quitando el código de acceso o estableciendo un código de acceso temporal de forma remota.

**Realizar un bypass del bloqueo de activación en dispositivos iOS**
Cuando los dispositivos iOS propiedad de la empresa están protegidos por bloqueo de activación y el dispositivo se pierde o sustrae, el bloqueo de activación puede impedir que las personas equivocadas usen el dispositivo y sus datos. Sin embargo, si puede recuperar el dispositivo, o si un empleado devuelve el dispositivo pero se olvida de desactivar el bloqueo de activación, deberá desbloquear el dispositivo. Si no tiene el identificador y la contraseña de Apple del usuario para desbloquearlo, puede usar el [bypass del bloqueo de activación de Intune](https://technet.microsoft.com/library/mt414176.aspx).

## Revocar el acceso a la red de empresa
También querrá asegurarse de que cuando un empleado deje la empresa, no se lleve datos empresariales, ya sea porque usó su propio dispositivo o porque olvidó devolver el hardware corporativo.  En el primer caso, solo hay que [seleccionar y borrar el dispositivo personal del empleado](https://technet.microsoft.com/library/jj676679.aspx). En el segundo caso, puede [bloquearlo de forma remota](https://technet.microsoft.com/library/jj676679.aspx). Esto impide que la información y el hardware de la empresa se usen incorrectamente, aunque puede que tenga que cancelar el dispositivo por pérdida.

También querrá revocar la licencia de la cuenta de usuario de Intune del empleado. Esto hace que se libere la licencia para poder asignarla a una cuenta de usuario nueva.

## Retirar hardware
A veces, es el propio dispositivo el que llega al final del ciclo de vida. En tales casos, al [restablecer el dispositivo a la configuración de fábrica](https://technet.microsoft.com/library/jj676679.aspx), se quitan todos los datos y se elimina el dispositivo de Intune. Luego, puede deshacerse del hardware según las directivas de su empresa.

**Auditar el uso de inventario y licencia**
Puede realizar un seguimiento de los cambios en el inventario y las licencias mediante los [informes de inventario](https://technet.microsoft.com/library/dn646977.aspx) integrados.

## Vea también
[Documentación de Microsoft Intune](../Topic/Documentation-for-Microsoft-Intune.md)

