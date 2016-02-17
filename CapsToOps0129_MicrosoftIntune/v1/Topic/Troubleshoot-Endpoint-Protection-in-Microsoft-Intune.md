---
title: Solucionar problemas de Endpoint Protection en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e31df2d2-bb1b-491b-9a71-04e0b18829c1
---
# Solucionar problemas de Endpoint Protection en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para></para>
      </introduction>
      <section address="BKMK_EP" expanded="true">
        <title>
          <caps:sentence sentenceid="cc835bf2225ea4747844003d0c06dde0" id="tgt1" class="tgtSentence">Recursos para ayudarle a resolver problemas con Endpoint Protection</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5831421bb90d9bbd733d72a94104c6f3" id="tgt2" class="tgtSentence">Utilice la información de esta sección para resolver problemas fácilmente cuando utiliza <token>epshort</token> de <token>wit_firstref</token>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="8ffe3c8695cb2d603155f775dcf20ccd" id="tgt3" class="tgtSentence">Mensajes de error de Endpoint Protection</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="089d6ad7fea88c532bb391bf22020aae" id="tgt4" class="tgtSentence">En esta sección se describen las posibles causas y soluciones de los siguientes errores y advertencias que aparecen en el panel <ui>Estado de Endpoint Protection</ui> de la <token>wit_adminconsole</token>.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ed89d5a88df95456f428d86981265447" id="tgt5" class="tgtSentence">Elemento de estado</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e92c3fe74f93d6064ce89a536a3db726" id="tgt6" class="tgtSentence">Posibles causas</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="af6a132fda60ad5b32cf5a8417322fa0" id="tgt7" class="tgtSentence">Posibles soluciones</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para address="BKMK_MPEngineUnavailable">
                        <ui>
                          <caps:sentence sentenceid="7ed25fbc4935ce5cfa3ad8d29f04c5f3" id="tgt8" class="tgtSentence">Motor de Endpoint Protection no disponible</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt9" class="tgtSentence">El motor <token>epshort</token> de <token>wit_firstref</token> se ha dañado o eliminado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0e22f9d7dad7228c50b558971276a729" id="tgt10" class="tgtSentence">Si el motor <token>epshort</token> de <token>wit_firstref</token> se ha dañado, puede intentar actualizar o reinstalar el software.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="af7c235e92c784b34d6f2fb23be99dfc" id="tgt11" class="tgtSentence">Para forzar una actualización inmediata, haga clic en <ui>Actualizar</ui> en el software cliente de <token>epshort</token> (se encuentra en la barra de tareas de los equipos administrados.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="45d8a56a1baa25e9ef895b4a926a85eb" id="tgt12" class="tgtSentence">Si el motor no se puede actualizar, deberá reinstalar el motor de <token>epshort</token>.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="4354a96d8e12b61da06d66b8a11da2b6" id="tgt13" class="tgtSentence"> En la lista de programas instalados, en el Panel de control del equipo administrado, localice <ui>Agente de Microsoft Intune Endpoint Protection</ui> y desinstale la aplicación.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence sentenceid="b6dffef86ee8100c13e338292644a768" id="tgt14" class="tgtSentence">Durante la próxima sincronización de actualización, el Administrador de actualizaciones de Microsoft Online Management detectará el programa que falta y lo reinstalará a la hora de instalación programada.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_MPDisabled">
                        <ui>
                          <caps:sentence sentenceid="b8c1f68b00f8711a829895c6ded4e254" id="tgt15" class="tgtSentence">Endpoint Protection deshabilitado</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt16" class="tgtSentence">Un administrador o un usuario han deshabilitado <token>epshort</token> de <token>wit_firstref</token> con una directiva en un equipo administrado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="959076d2b0beff36ddd17662b927b4f9" id="tgt17" class="tgtSentence">Si se deshabilita <token>epshort</token>, puede habilitarlo desde la <token>wit_adminconsole</token> o desde un equipo administrado.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1189e1892ce26e7b8f3ad1727116bce4" id="tgt18" class="tgtSentence">Realice una de las siguientes acciones:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="5efcb292498446e163bc74f175500dcb" id="tgt19" class="tgtSentence">Para habilitar <token>epshort</token> desde la <token>wit_adminconsole</token>, abra el área de trabajo <ui>Directiva</ui> y, a continuación, cambie la configuración de <ui>Habilitar Endpoint Protection</ui> en las directivas que se aplican al equipo.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="5efcb292498446e163bc74f175500dcb" id="tgt20" class="tgtSentence">Para habilitar <token>epshort</token> desde un equipo administrado, inicie el cliente <token>epshort</token> de <token>wit_firstref</token> desde el área de notificación y se le solicitará que habilite <token>epshort</token>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_RTPDisabled">
                        <ui>
                          <caps:sentence sentenceid="6419d85ff3515765011e39e7b92a4ca9" id="tgt21" class="tgtSentence">Protección en tiempo real deshabilitada</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9d0abd18922514279737f92995bcffdc" id="tgt22" class="tgtSentence">La protección en tiempo real fue deshabilitada por un administrador mediante el uso de una directiva o por un usuario en un equipo administrado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="aed6a85ec9ab5231bab709c6ac9058a7" id="tgt23" class="tgtSentence">Si se deshabilita la protección en tiempo real, puede habilitarla desde la <token>wit_adminconsole</token> o desde un equipo administrado.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1189e1892ce26e7b8f3ad1727116bce4" id="tgt24" class="tgtSentence">Realice una de las siguientes acciones:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="9da4c3da3e7d8c937919ff5319ece0a9" id="tgt25" class="tgtSentence">Para habilitar la protección en tiempo real desde la <token>wit_adminconsole</token>, abra el área de trabajo <ui>Directiva</ui> y, a continuación, cambie la configuración de <ui>Habilitar protección en tiempo real</ui> a <ui>Sí</ui> en las directivas que se aplican a este equipo.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="68da839db4a600a6e65d32ef4e8541f8" id="tgt26" class="tgtSentence">Para habilitar la protección en tiempo real desde un equipo administrado, inicie el software cliente de <token>epshort</token> desde el área de notificación.</caps:sentence>
                            <caps:sentence sentenceid="9d070d34825a1b1e8278f1f333259eb9" id="tgt27" class="tgtSentence"> En ese momento se le solicita que habilite la protección en tiempo real.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_DownscanDisabled">
                        <ui>
                          <caps:sentence sentenceid="d5b8041f3e6238db72381d2b058eec95" id="tgt28" class="tgtSentence">Examen de descargas deshabilitado</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4846a2a99c6ee432c1bac119625e20c6" id="tgt29" class="tgtSentence">El examen de descargas ha sido deshabilitado por un administrador mediante el uso de una directiva o por un usuario en un equipo administrado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="46a4c0cd103ac64835b7550a5d9d4c1f" id="tgt30" class="tgtSentence">Si el examen de descargas está deshabilitado, puede habilitarlo desde la <token>wit_adminconsole</token> o desde un equipo administrado.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1189e1892ce26e7b8f3ad1727116bce4" id="tgt31" class="tgtSentence">Realice una de las siguientes acciones:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="83f4eeb3048e2e562cfd3d9be4fa6d3a" id="tgt32" class="tgtSentence">Para habilitar el examen de descargas desde la <token>wit_adminconsole</token>, abra el área de trabajo <ui>Directiva</ui> y cambie la configuración de <ui>Examinar todas las descargas</ui> a <ui>Sí</ui> en las directivas que se aplican a este equipo.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="bffb8ed922324c2957d0d1a46dd7d8d1" id="tgt33" class="tgtSentence">Para habilitar el examen de descargas desde un equipo administrado, inicie el software cliente de <token>epshort</token> desde el área de notificación.</caps:sentence>
                            <caps:sentence sentenceid="a07f213827196968e84f7a208e04bd2e" id="tgt34" class="tgtSentence"> Haga clic en la ficha <ui>Configuración</ui>, haga clic en <ui>Protección en tiempo real</ui>, active la casilla <ui>Examinar todas descargas</ui> y, a continuación, haga clic en <ui>Guardar cambios</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_FileMonDisabled">
                        <ui>
                          <caps:sentence sentenceid="c258a99994555180534623f6bea1719c" id="tgt35" class="tgtSentence">Supervisión de actividad de archivos y programas deshabilitada</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8fe2b0a2d9650615b16ccb3c2175910f" id="tgt36" class="tgtSentence">La supervisión de la actividad de archivos y programas fue deshabilitada por un administrador mediante el uso de una directiva o por un usuario en un equipo administrado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="750de5eca8b9d6e7226cf213d59b0233" id="tgt37" class="tgtSentence">Si la supervisión de la actividad de archivos y programas está deshabilitada, puede habilitarla desde la <token>wit_adminconsole</token> o desde un equipo administrado.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1189e1892ce26e7b8f3ad1727116bce4" id="tgt38" class="tgtSentence">Realice una de las siguientes acciones:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0ffe911f926b04e623619a9c6db8954b" id="tgt39" class="tgtSentence">Para habilitar la supervisión de la actividad de archivos y programas desde la <token>wit_adminconsole</token>, abra el área de trabajo <ui>Directiva</ui> y cambie la configuración de <ui>Supervisar la actividad de archivos y programas en los equipos</ui> a <ui>Sí</ui> en las directivas aplicables a este equipo.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d0e03d855217c33b602e88fe5c9ef500" id="tgt40" class="tgtSentence">Para habilitar la supervisión de la actividad de archivos y programas desde un equipo administrado, inicie el software cliente de <token>epshort</token> desde el área de notificación.</caps:sentence>
                            <caps:sentence sentenceid="a07f213827196968e84f7a208e04bd2e" id="tgt41" class="tgtSentence"> Haga clic en la ficha <ui>Configuración</ui>, haga clic en <ui>Protección en tiempo real</ui>, active la casilla <ui>Supervisar la actividad de archivos y programas en los equipos</ui> y, a continuación, haga clic en <ui>Guardar cambios</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_BehaveMonDisabled">
                        <ui>
                          <caps:sentence sentenceid="83be683fa3e8cd00cc138e9e1f17ece0" id="tgt42" class="tgtSentence">Supervisión de comportamiento deshabilitada</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="59b4018f314f4c6ed6970cc69ddad684" id="tgt43" class="tgtSentence">La supervisión del comportamiento fue deshabilitada por un administrador mediante el uso de una directiva o por un usuario en un equipo administrado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="289f5eeda82074c22ca77c7665977971" id="tgt44" class="tgtSentence">Si se deshabilita la supervisión del comportamiento, puede habilitarla desde la <token>wit_adminconsole</token> o desde un equipo administrado.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1189e1892ce26e7b8f3ad1727116bce4" id="tgt45" class="tgtSentence">Realice una de las siguientes acciones:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="7a26ab04a3677c3b1341398fdadad0c9" id="tgt46" class="tgtSentence">Para habilitar la supervisión del comportamiento desde la <token>wit_adminconsole</token>, abra el área de trabajo <ui>Directiva</ui> y cambie la configuración de <ui>Habilitar supervisión del comportamiento</ui> a <ui>Sí</ui> en las directivas que se aplican a este equipo; a continuación, reinicie el equipo administrado.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d14613e5f83a146b8e171c74ef72ce3d" id="tgt47" class="tgtSentence">Para habilitar la supervisión de comportamiento desde un equipo administrado, inicie el software cliente de <token>epshort</token> desde el área de notificación.</caps:sentence>
                            <caps:sentence sentenceid="a07f213827196968e84f7a208e04bd2e" id="tgt48" class="tgtSentence"> Haga clic en la ficha <ui>Configuración</ui>, haga clic en <ui>Protección en tiempo real</ui>, active la casilla <ui>Habilitar supervisión del comportamiento</ui> y, a continuación, haga clic en <ui>Guardar cambios</ui>.</caps:sentence>
                            <caps:sentence sentenceid="4f0de9a9ab4d8bf200106030b74243df" id="tgt49" class="tgtSentence"> A continuación, reinicie el equipo.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_ScriptscanDisabled">
                        <ui>
                          <caps:sentence sentenceid="1749ca6a70b4e80300905a4c5e6a8216" id="tgt50" class="tgtSentence">Análisis de scripts deshabilitado</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a747444d3c89abde465648fe6ba3269d" id="tgt51" class="tgtSentence">El examen de scripts fue deshabilitado por un administrador mediante el uso de una directiva o por un usuario en un equipo administrado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="11a38e365c1561aff4bacebf2ca2b1ab" id="tgt52" class="tgtSentence">Si el examen de scripts está deshabilitado, puede habilitarlo desde la <token>wit_adminconsole</token> o desde un equipo administrado.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1189e1892ce26e7b8f3ad1727116bce4" id="tgt53" class="tgtSentence">Realice una de las siguientes acciones:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="9b4ea4e3872f32849723ae433987ebee" id="tgt54" class="tgtSentence">Para habilitar el examen de scripts desde la <token>wit_adminconsole</token>, abra el área de trabajo <ui>Directiva</ui> y cambie la configuración de <ui>Habilitar examen de scripts</ui> a <ui>Sí</ui> en las directivas que se aplican a este equipo.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="b14d0bfd58113190282b7576fdd8dee7" id="tgt55" class="tgtSentence">Para habilitar el examen de scripts desde un equipo administrado, inicie el software cliente de <token>epshort</token> desde el área de notificación.</caps:sentence>
                            <caps:sentence sentenceid="a07f213827196968e84f7a208e04bd2e" id="tgt56" class="tgtSentence"> Haga clic en la ficha <ui>Configuración</ui>, haga clic en <ui>Protección en tiempo real</ui>, active la casilla <ui>Habilitar examen de scripts</ui> y, a continuación, haga clic en <ui>Guardar cambios</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_NISDisabled">
                        <ui>
                          <caps:sentence sentenceid="d47796f6820644b6683a0041f6bbfb61" id="tgt57" class="tgtSentence">Sistema de inspección de red deshabilitado</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c7507ea5a191fec5134bd23d360b2b44" id="tgt58" class="tgtSentence">El sistema de inspección de red ha sido deshabilitado por un administrador mediante el uso de una directiva o por el usuario en un equipo administrado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fcd0375a34ff0c966c90f1567c17517f" id="tgt59" class="tgtSentence">Si se deshabilita el sistema de inspección de red, puede habilitarlo desde la <token>wit_adminconsole</token> o desde un equipo administrado.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1189e1892ce26e7b8f3ad1727116bce4" id="tgt60" class="tgtSentence">Realice una de las siguientes acciones:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d83f720c75e03930ce81ab0619250e81" id="tgt61" class="tgtSentence">Para habilitar el sistema de inspección de red desde la <token>wit_adminconsole</token>, abra el área de trabajo <ui>Directiva</ui> y cambie la configuración de <ui>Habilitar Sistema de inspección de red</ui> a <ui>Sí</ui> en las directivas que se aplican a este equipo; a continuación, reinicie el equipo administrado.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="fcc923e189c61f8fb517fd77510bd573" id="tgt62" class="tgtSentence">Para habilitar el sistema de inspección de red desde un equipo administrado, inicie el software cliente de <token>epshort</token> desde el área de notificación.</caps:sentence>
                            <caps:sentence sentenceid="a07f213827196968e84f7a208e04bd2e" id="tgt63" class="tgtSentence"> Haga clic en la ficha <ui>Configuración</ui>, haga clic en <ui>Protección en tiempo real</ui>, active la casilla <ui>Habilitar Sistema de inspección de red</ui> y, a continuación, haga clic en <ui>Guardar cambios</ui>.</caps:sentence>
                            <caps:sentence sentenceid="b3e9e853488cca16ea5d6e6ea991a5a4" id="tgt64" class="tgtSentence"> Reinicie el equipo.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_DefOutofDate">
                        <ui>
                          <caps:sentence sentenceid="a3734799ae62b36bc557152bbc0467dc" id="tgt65" class="tgtSentence">Definiciones de malware desactualizadas</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="00d3dd785b2f1e88ebec5cfad3d02197" id="tgt66" class="tgtSentence">Puede que el equipo haya permanecido desconectado de Internet durante un período prolongado de tiempo y que sus definiciones de malware no hayan sido actualizadas aún.</caps:sentence>
                        <caps:sentence sentenceid="0a8facc5e1ebaec449dac20252411426" id="tgt67" class="tgtSentence"> Este estado aparece cuando las definiciones de malware del equipo no se han actualizado desde hace 14 días, como mínimo.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9244f6d4ccc0c7fd22bd6dd391f8917b" id="tgt68" class="tgtSentence">Si las definiciones de malware no están actualizadas, puede actualizarlas desde la <token>wit_adminconsole</token> o desde el equipo administrado.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt69" class="tgtSentence">Para obtener más información, consulte el tema <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Windows Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_FSOverdue">
                        <ui>
                          <caps:sentence sentenceid="35d1753e9b622eaaf2b528c7b9810c96" id="tgt70" class="tgtSentence">Examen completo vencido</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="66c792bac6bc97bbb27930dc7f6620fc" id="tgt71" class="tgtSentence">No se ha completado un examen completo en los últimos 14 días.</caps:sentence>
                        <caps:sentence sentenceid="4a21e6969caf7387dd25c777215d9ac3" id="tgt72" class="tgtSentence"> Esto puede deberse a un reinicio del equipo durante un examen completo.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3fc9dce9aacc7402376e80906ee72218" id="tgt73" class="tgtSentence">Si ha vencido un examen completo, puede ejecutar un examen completo único o programar exámenes completos periódicos desde la <token>wit_adminconsole</token> utilizando la información del tema <link xlink:href="eb912c73-54d2-4d78-ac34-3cbe825804c7">Manage Computers with Windows Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_QSOverdue">
                        <ui>
                          <caps:sentence sentenceid="4e3f8f175d9f8cfdad967a98e97fc8dd" id="tgt74" class="tgtSentence">Examen rápido vencido</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e5697b8f2124f2aeb83c2f0b0d9751a0" id="tgt75" class="tgtSentence">No se ha completado un examen rápido en los últimos 14 días.</caps:sentence>
                        <caps:sentence sentenceid="47573009147a162f9c3dac6ce1c7ae74" id="tgt76" class="tgtSentence"> Esto puede deberse a un reinicio durante un examen rápido.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bd94414ff219a97712799437a26bd5d5" id="tgt77" class="tgtSentence">Si ha vencido un examen rápido, puede ejecutar un examen rápido único o programar exámenes rápidos periódicos desde la <token>wit_adminconsole</token> utilizando la información del tema <link xlink:href="eb912c73-54d2-4d78-ac34-3cbe825804c7">Manage Computers with Windows Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_AnotherAMApp">
                        <ui>
                          <caps:sentence sentenceid="590118249b28a4859c8ea83df15b2bc5" id="tgt78" class="tgtSentence">Otra aplicación de protección de extremos en ejecución</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e9e2c7e10405efb1059ba7ac92885de4" id="tgt79" class="tgtSentence">Se está ejecutando otra aplicación de protección de extremos y el equipo está en buenas condiciones.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7433691c25dc121f4d08eeb518e86475" id="tgt80" class="tgtSentence">De forma predeterminada, si se instala otra aplicación de protección de extremos y <token>wit_nextref</token> detecta la aplicación, <token>epshort</token> se deshabilita automáticamente.</caps:sentence>
                        <caps:sentence sentenceid="c11a7d7ad35a93147d50646784353099" id="tgt81" class="tgtSentence"> Si <token>wit_nextref</token> no detecta la otra aplicación de protección de extremos, <token>epshort</token> seguirá habilitado.</caps:sentence>
                        <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt82" class="tgtSentence"> Para obtener más información, vea <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Windows Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="c86a4e4a-6b9f-4835-a3d3-61a3f5f4c1ec">Troubleshoot Microsoft Intune</link>
        <link xlink:href="3b8d22fe-c318-4796-b760-44f1ccf34312">Manage computers with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para></para>
      </introduction>
      <section address="BKMK_EP" expanded="true">
        <title>
          <caps:sentence id="src1" class="srcSentence">Resources to help you solve Endpoint Protection problems</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Use the information in this section to help you solve problems while using <token>wit_firstref</token> <token>epshort</token>.</caps:sentence>
          </para>
        </content>
        <sections>
          <section expanded="true">
            <title>
              <caps:sentence id="src3" class="srcSentence">Endpoint Protection error messages</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src4" class="srcSentence">This section describes potential causes and solutions for the following errors and warnings, which appear in the <ui>Endpoint Protection Status</ui> pane in the <token>wit_adminconsole</token>.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src5" class="srcSentence">Status item</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src6" class="srcSentence">Potential causes</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src7" class="srcSentence">Potential solutions</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para address="BKMK_MPEngineUnavailable">
                        <ui>
                          <caps:sentence id="src8" class="srcSentence">Endpoint Protection engine unavailable</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src9" class="srcSentence">The <token>wit_firstref</token> <token>epshort</token> engine was corrupted or deleted.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src10" class="srcSentence">If the <token>wit_firstref</token> <token>epshort</token> engine is corrupted, you can try updating or reinstalling the software.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src11" class="srcSentence">To force an immediate update, click <ui>Update</ui> in the <token>epshort</token> client software (found in the taskbar on managed computers.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src12" class="srcSentence">If the engine cannot be updated, you must reinstall the <token>epshort</token> engine.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src13" class="srcSentence"> In the list of installed programs in Control Panel on the managed computer, locate <ui>Microsoft Intune Endpoint Protection Agent</ui>, and then uninstall the application.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">During the next update synchronization, the Microsoft Online Management Update Manager detects the missing program and reinstalls it at the scheduled installation time.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_MPDisabled">
                        <ui>
                          <caps:sentence id="src15" class="srcSentence">Endpoint Protection disabled</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src16" class="srcSentence">
                          <token>wit_firstref</token> <token>epshort</token> was disabled by an administrator using a policy or by a user on a managed computer.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src17" class="srcSentence">If <token>epshort</token> is disabled, you can enable it from the <token>wit_adminconsole</token> or from a managed computer.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src18" class="srcSentence">Do one of the following:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src19" class="srcSentence">To enable <token>epshort</token> from the <token>wit_adminconsole</token>, open the <ui>Policy</ui> workspace, and then change the <ui>Enable Endpoint Protection</ui> setting in the policies that apply to the computer.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src20" class="srcSentence">To enable <token>epshort</token> from a managed computer, start the <token>wit_firstref</token> <token>epshort</token> client from the notification area and you will be prompted to enable <token>epshort</token>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_RTPDisabled">
                        <ui>
                          <caps:sentence id="src21" class="srcSentence">Real-time protection disabled</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src22" class="srcSentence">Real-time protection was disabled by an administrator who used Policy or by a user on a managed computer.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src23" class="srcSentence">If real-time protection is disabled, you can enable it from the <token>wit_adminconsole</token> or from a managed computer.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src24" class="srcSentence">Do one of the following:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src25" class="srcSentence">To enable real-time protection from the <token>wit_adminconsole</token>, open the <ui>Policy</ui> workspace, and then change the <ui>Enable real-time protection</ui> setting to <ui>Yes</ui> in the policies that apply to the computer.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src26" class="srcSentence">To enable real-time protection from a managed computer, start the <token>epshort</token> client software from the notification area.</caps:sentence>
                            <caps:sentence id="src27" class="srcSentence"> You are prompted to enable real-time protection at that time.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_DownscanDisabled">
                        <ui>
                          <caps:sentence id="src28" class="srcSentence">Download scanning disabled</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src29" class="srcSentence">Download scanning was disabled by an administrator by using policy or by a user on a managed computer.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src30" class="srcSentence">If download scanning is disabled, you can enable it from the <token>wit_adminconsole</token> or from a managed computer.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src31" class="srcSentence">Do one of the following:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src32" class="srcSentence">To enable download scanning from the <token>wit_adminconsole</token>, open the <ui>Policy</ui> workspace, and then change the <ui>Scan all Downloads</ui> setting to <ui>Yes</ui> in the policies that apply to the computer.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src33" class="srcSentence">To enable download scanning from a managed computer, start the <token>epshort</token> client software from the notification area.</caps:sentence>
                            <caps:sentence id="src34" class="srcSentence"> Click the <ui>Settings</ui> tab, click <ui>Real-time protection</ui>, select the <ui>Scan all downloads</ui> check box, and then click <ui>Save changes</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_FileMonDisabled">
                        <ui>
                          <caps:sentence id="src35" class="srcSentence">File and program activity monitoring disabled</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">File and program activity monitoring was disabled by an administrator who used Policy or by a user on a managed computer.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">If file and program activity monitoring is disabled, you can enable it from the <token>wit_adminconsole</token> or from a managed computer.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">Do one of the following:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src39" class="srcSentence">To enable file and program activity monitoring from the <token>wit_adminconsole</token>, open the <ui>Policy</ui> workspace, and then change the <ui>Monitor file and program activity on computers</ui> setting to <ui>Yes</ui> in the policies that apply to the computer.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src40" class="srcSentence">To enable file and program activity monitoring from a managed computer, start the <token>epshort</token> client software from the notification area.</caps:sentence>
                            <caps:sentence id="src41" class="srcSentence"> Click the <ui>Settings</ui> tab, click <ui>Real-time protection</ui>, select the <ui>Monitor file and program activity on your computer</ui> check box, and then click <ui>Save changes</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_BehaveMonDisabled">
                        <ui>
                          <caps:sentence id="src42" class="srcSentence">Behavior monitoring disabled</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">Behavior monitoring was disabled by an administrator who used Policy or by a user on a managed computer.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">If behavior monitoring is disabled, you can enable it from the <token>wit_adminconsole</token> or from a managed computer.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">Do one of the following:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src46" class="srcSentence">To enable behavior monitoring from the <token>wit_adminconsole</token>, open the <ui>Policy</ui> workspace, change the <ui>Enable behavior monitoring</ui> setting to <ui>Yes</ui> in the policies that apply to the computer, and then restart the managed computer.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src47" class="srcSentence">To enable behavior monitoring from a managed computer, start the <token>epshort</token> client software from the notification area.</caps:sentence>
                            <caps:sentence id="src48" class="srcSentence"> Click the <ui>Settings</ui> tab, click <ui>Real-time protection</ui>, select the <ui>Enable behavior monitoring</ui> check box, and then click <ui>Save changes</ui>.</caps:sentence>
                            <caps:sentence id="src49" class="srcSentence"> Then, restart the computer.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_ScriptscanDisabled">
                        <ui>
                          <caps:sentence id="src50" class="srcSentence">Script scanning disabled</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">Script scanning was disabled by an administrator who used Policy or by a user on a managed computer.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">If script scanning is disabled, you can enable it from the <token>wit_adminconsole</token> or from a managed computer.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">Do one of the following:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src54" class="srcSentence">To enable script scanning from the <token>wit_adminconsole</token>, open the <ui>Policy</ui> workspace and change the <ui>Enable script scanning</ui> setting to <ui>Yes</ui> in the policies that apply to the computer.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src55" class="srcSentence">To enable script scanning from a managed computer, start the <token>epshort</token> client software from the notification area.</caps:sentence>
                            <caps:sentence id="src56" class="srcSentence"> Click the <ui>Settings</ui> tab, click <ui>Real-time protection</ui>, select the <ui>Enable script scanning</ui> check box, and then click <ui>Save changes</ui>.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_NISDisabled">
                        <ui>
                          <caps:sentence id="src57" class="srcSentence">Network Inspection System disabled</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">The Network Inspection System was disabled by an administrator using policy or by a user on a managed computer.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src59" class="srcSentence">If Network Inspection System is disabled, you can enable it from the <token>wit_adminconsole</token> or from a managed computer.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src60" class="srcSentence">Do one of the following:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src61" class="srcSentence">To enable Network Inspection System from the <token>wit_adminconsole</token>, open the <ui>Policy</ui> workspace, change the <ui>Enable Network Inspection System</ui> setting to <ui>Yes</ui> in the policies that apply to the computer, and then restart the managed computer.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src62" class="srcSentence">To enable Network Inspection System from a managed computer, start the <token>epshort</token> client software from the notification area.</caps:sentence>
                            <caps:sentence id="src63" class="srcSentence"> Click the <ui>Settings</ui> tab, click <ui>Real-time protection</ui>, select the <ui>Enable Network Inspection System</ui> check box, and then click <ui>Save changes</ui>.</caps:sentence>
                            <caps:sentence id="src64" class="srcSentence"> Restart the computer.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_DefOutofDate">
                        <ui>
                          <caps:sentence id="src65" class="srcSentence">Malware definitions out-of-date</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">The computer might have been disconnected from the Internet for an extended period of time, and its malware definitions might not yet have been updated.</caps:sentence>
                        <caps:sentence id="src67" class="srcSentence"> This status appears when the malware definitions on the computer are out-of-date by 14 days or more.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">If malware definitions are out-of-date, you can update the definitions from the <token>wit_adminconsole</token> or from the managed computer.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">For more information, see <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Windows Intune</link> topic.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_FSOverdue">
                        <ui>
                          <caps:sentence id="src70" class="srcSentence">Full scan overdue</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">A full scan has not been completed for 14 days.</caps:sentence>
                        <caps:sentence id="src72" class="srcSentence"> This can be caused by a computer restart during a full scan.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src73" class="srcSentence">If a full scan is overdue, you can run a one-time full scan or schedule recurring full scans from the <token>wit_adminconsole</token> by using the information in the topic <link xlink:href="eb912c73-54d2-4d78-ac34-3cbe825804c7">Manage Computers with Windows Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_QSOverdue">
                        <ui>
                          <caps:sentence id="src74" class="srcSentence">Quick scan overdue</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src75" class="srcSentence">A quick scan has not been completed for 14 days.</caps:sentence>
                        <caps:sentence id="src76" class="srcSentence"> This can be caused by a restart during a quick scan.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src77" class="srcSentence">If a quick scan is overdue, you can run a one-time quick scan or schedule recurring quick scans from the <token>wit_adminconsole</token> by using the information in the topic <link xlink:href="eb912c73-54d2-4d78-ac34-3cbe825804c7">Manage Computers with Windows Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para address="BKMK_AnotherAMApp">
                        <ui>
                          <caps:sentence id="src78" class="srcSentence">Another endpoint protection application running</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src79" class="srcSentence">Another endpoint protection application is running, and the computer is healthy.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src80" class="srcSentence">By default, if another endpoint protection application is installed and <token>wit_nextref</token>  detects that application, <token>epshort</token> automatically disables itself.</caps:sentence>
                        <caps:sentence id="src81" class="srcSentence"> If <token>wit_nextref</token> does not detect the other endpoint application, <token>epshort</token> will remain enabled.</caps:sentence>
                        <caps:sentence id="src82" class="srcSentence"> For more information, see <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help Secure Your Computers with Endpoint Protection and Windows Firewall Policy for Windows Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="c86a4e4a-6b9f-4835-a3d3-61a3f5f4c1ec">Troubleshoot Microsoft Intune</link>
        <link xlink:href="3b8d22fe-c318-4796-b760-44f1ccf34312">Manage computers with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>