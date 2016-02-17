---
title: Solucionar los problemas de configuraci&#243;n del cliente en Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e46d292b-1d16-46db-a87f-d53eefa4d22a
---
# Solucionar los problemas de configuraci&#243;n del cliente en Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para></para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="470463b90223d08e68f063820c6f37da" id="tgt1" class="tgtSentence">Solucionar los problemas de configuración del cliente</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="731625dd51d439f2df673de6a8155135" id="tgt2" class="tgtSentence">Utilice las secciones siguientes para ayudarle a solucionar problemas comunes de configuración del cliente.</caps:sentence>
          </para>
        </content>
        <sections>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="252d067fff61d870e49b3667995896d9" id="tgt3" class="tgtSentence">Qué hacer si se produce un error en la instalación del cliente</caps:sentence>
            </title>
            <content>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8b4d43c2b9fbe84ea275d0de03b94bf0" id="tgt4" class="tgtSentence">Si no se muestra ninguna alerta de implementación del software cliente para el equipo en la <token>wit_adminconsole</token>, compruebe la conectividad a Internet y la configuración proxy del equipo, y asegúrese de que el equipo se pueda comunicar con la dirección URL del servicio, <externalLink><linkText>https://manage.microsoft.com</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>.</caps:sentence>
                    <caps:sentence sentenceid="00631a2d42793fa87e4517211454fe5a" id="tgt5" class="tgtSentence"> Posteriormente vuelva a intentar la instalación del software cliente.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cef0a8ae5c4f6feb33a301572ebe25ed" id="tgt6" class="tgtSentence">Mediante la configuración de una regla de notificación en el área de trabajo <ui>Administración</ui>, puede enviar un correo electrónico a los destinatarios seleccionados cuando se produzca una alerta de error de implementación del software cliente.</caps:sentence>
                    <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt7" class="tgtSentence"> Para obtener más información, vea <link xlink:href="396ea714-0433-4bd5-a934-8d0b477f28e4">Configure Alerts in Windows Intune</link>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ba73fec0afeb67e902e41fdf0fb81c3c" id="tgt8" class="tgtSentence">
                      <token>wit_firstref</token> muestra la alerta crítica <ui>Error de implementación del software cliente</ui> si se produce un error en la implementación del software cliente.</caps:sentence>
                    <caps:sentence sentenceid="cbc106d68a571e08dbafd5026eda939d" id="tgt9" class="tgtSentence"> Esto se mostrará en las páginas <ui>Información general del sistema</ui> y <ui>Alertas</ui> de la <token>wit_adminconsole</token>.</caps:sentence>
                    <caps:sentence sentenceid="0c38089cd311768c26f83b6b1427be6c" id="tgt10" class="tgtSentence"> Compruebe las alertas utilizando el procedimiento siguiente:</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence sentenceid="06a497d7c955a5b1ce5691ef0d1b6a63" id="tgt11" class="tgtSentence">Para comprobar las alertas de errores de instalación</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt12" class="tgtSentence">En la <externalLink><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, haga clic en <ui>Alertas</ui> &gt; <ui>Información general</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt13" class="tgtSentence">En la página <ui>Información general de alertas</ui> puede revisar la información siguiente:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="b530a93da64f123d395deb1f37d0df23" id="tgt14" class="tgtSentence">Las tres primeras alertas, que se pueden ordenar por fecha, categoría o gravedad </caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="cdfd4b0643b96fe1eb14e9ac71907748" id="tgt15" class="tgtSentence">El número total de alertas activas</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt16" class="tgtSentence">Haga clic en <ui>Todas las alertas</ui> para mostrar la información siguiente en la página <ui>Alertas</ui>.</caps:sentence>
                        <caps:sentence sentenceid="489e569a46741aa4752e390ab29094ef" id="tgt17" class="tgtSentence"> Las alertas críticas se muestran en primer lugar:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="25628c552207d794a3eb247c22f2fd1a" id="tgt18" class="tgtSentence">
                              <ui>Nombre</ui>: el nombre del tipo de alerta que generó la alerta.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="f4669c69a54a5b96c2dc644cad9ebe95" id="tgt19" class="tgtSentence">
                              <ui>Origen</ui>: el vínculo al origen de la alerta.</caps:sentence>
                            <caps:sentence sentenceid="a6681bc9735595ee59deb866084bdbdf" id="tgt20" class="tgtSentence">  Si el umbral para mostrar del tipo de alerta se configura como <ui>Todo</ui>, este vínculo permitirá ver un único dispositivo afectado.</caps:sentence>
                            <caps:sentence sentenceid="8d16f6ce69c147f924f336601e5861b1" id="tgt21" class="tgtSentence">  Si el umbral para mostrar del tipo de alerta se configura como un valor, este vínculo permitirá ver una lista de todos los dispositivos afectados por la alerta en cuestión.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="fd2afd4456a70ed032333dcd0ecab176" id="tgt22" class="tgtSentence">
                              <ui>Última actualización</ui>: indica el momento de la última modificación de la alerta.</caps:sentence>
                            <caps:sentence sentenceid="94dcf41a1578a3e6caa6889fc2de22ed" id="tgt23" class="tgtSentence"> Si una alerta está cerrada, se muestra el momento en el que se cerró.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="824c66c0cde03c27b18b527450aafc80" id="tgt24" class="tgtSentence">
                              <ui>Gravedad</ui>: indica la gravedad de la alerta</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section expanded="true" address="BKMK_Whattodo">
            <title>
              <caps:sentence sentenceid="2bacd322f3aad9dec0f345a58847d276" id="tgt25" class="tgtSentence">Qué hacer si el cliente no se desinstala de la consola de administrador de Microsoft Intune</caps:sentence>
            </title>
            <content>
              <para></para>
              <procedure expanded="true">
                <title>
                  <caps:sentence sentenceid="98734e8cfa81aba275809cb68e5ab0f4" id="tgt26" class="tgtSentence">Para quitar el software cliente mediante la herramienta de línea de comandos de Microsoft Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ee72fb7abbe57466fd5fadef3a019ed2" id="tgt27" class="tgtSentence">Abra un símbolo del sistema en modo de administrador.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="791bb693836622968b88625af1fb18b4" id="tgt28" class="tgtSentence">Vaya a la carpeta <legacyItalic>%programfiles%\Microsoft\OnlineManagement\Common</legacyItalic></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="bc8d6831a209a830277de6abef0e452b" id="tgt29" class="tgtSentence">Ejecute el comando siguiente: <system>ProvisioningUtil.exe /UninstallAgents /MicrosoftIntune</system></caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence sentenceid="333cdc48ec95de867de3409208d9d96a" id="tgt30" class="tgtSentence">Códigos de error de instalación del cliente</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="7e8cef6ca12b123c38c5734473aace3a" id="tgt31" class="tgtSentence">En la siguiente tabla se describen los códigos de error que se muestran en <ui>Alertas</ui> si se produce un error en la instalación del software cliente.</caps:sentence>
                <caps:sentence sentenceid="0a95a9130b89839ed0a7ddf595dfd085" id="tgt32" class="tgtSentence"> Se incluyen sugerencias para resolver el problema representado por cada código de error.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d22fbcfa8424b1e6c55b784be952198b" id="tgt33" class="tgtSentence">Código de error</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="89e1e1576cad39d8552ca53932a1fddd" id="tgt34" class="tgtSentence">Posible problema</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="235febb44058cda9744c2c032ccdf06a" id="tgt35" class="tgtSentence">Solución recomendada</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5875863939f398559277e442505d8e23" id="tgt36" class="tgtSentence">0x80CF0437</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bf39983f19b5274d6d66e9ed434fb862" id="tgt37" class="tgtSentence">El reloj del equipo cliente no está configurado en la hora correcta.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9a20e21848ae37ea26f950fa1853d9a8" id="tgt38" class="tgtSentence">Asegúrese de que el reloj y la zona horaria del equipo cliente se hayan configurado en la hora y la zona horaria correctas.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fc763cb31e9938f37737394681228f83" id="tgt39" class="tgtSentence">
                          <ui>0x80240438</ui>, <ui>0x80CF0438</ui>, <ui>0x80CF401B</ui></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="da197ff94231e76b44c539c0c5a1db02" id="tgt40" class="tgtSentence">No se puede conectar con el servicio <token>wit_firstref</token>.</caps:sentence>
                        <caps:sentence sentenceid="75642e0888415bcdff17bda583aec24f" id="tgt41" class="tgtSentence"> Compruebe la configuración del proxy del cliente.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cfb0315cbe0305c262bf13e966b3f011" id="tgt42" class="tgtSentence">Compruebe que la configuración del proxy del cliente sea compatible con <token>wit_firstref</token> y que el equipo cliente tenga acceso a Internet.</caps:sentence>
                        <caps:sentence sentenceid="924f4dcbadf5defaeeae484528e2c56f" id="tgt43" class="tgtSentence"> Para obtener más información acerca de las configuraciones de proxy compatibles, vea <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help secure your computers with Endpoint Protection and Windows Firewall policy for Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3ac6f7e03926a09f359b60d0da81be2d" id="tgt44" class="tgtSentence">0x80CF402C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="da197ff94231e76b44c539c0c5a1db02" id="tgt45" class="tgtSentence">No se puede conectar con el servicio <token>wit_firstref</token>.</caps:sentence>
                        <caps:sentence sentenceid="42801ae1cc868c8d5c68c68c5b10425b" id="tgt46" class="tgtSentence"> Compruebe la conectividad de red.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="377c3370f33442697974f807accd6ca8" id="tgt47" class="tgtSentence">Compruebe que el equipo tiene conectividad de red.</caps:sentence>
                        <caps:sentence sentenceid="795432ec8d728f30b03bbfd35fe134a0" id="tgt48" class="tgtSentence"> Asegúrese de que el cable de red está conectado o que la red inalámbrica está activa.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="29f1b263da5a24223a0ba42cc44b056a" id="tgt49" class="tgtSentence">0x80240438, 0x80CF0438</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b442eb54be695d4316231c33152e5b9a" id="tgt50" class="tgtSentence">La configuración del proxy en Internet Explorer y el sistema local no se ha establecido.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8c9b27cf4ba89591d8f0cc2025de4e4b" id="tgt51" class="tgtSentence">Compruebe la configuración del proxy del cliente y confirme que la configuración del proxy en el equipo cliente sea compatible con <token>wit_firstref</token> y que el equipo cliente tiene acceso a Internet.</caps:sentence>
                        <caps:sentence sentenceid="924f4dcbadf5defaeeae484528e2c56f" id="tgt52" class="tgtSentence"> Para obtener más información acerca de las configuraciones de proxy compatibles, vea <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help secure your computers with Endpoint Protection and Windows Firewall policy for Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt53" class="tgtSentence">
                          <ui>0x80043001</ui> </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="83b73154a955ba8678d270cbcd71a61d" id="tgt54" class="tgtSentence">El paquete de inscripción no está actualizado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8debf8778c8529fe04cf3eda93c6bb94" id="tgt55" class="tgtSentence">Descargue e instale el paquete de software cliente actual del área de trabajo <ui>Administración</ui>.</caps:sentence>
                        <caps:sentence sentenceid="c42080e0c75e224ec570b3d0b91cf94c" id="tgt56" class="tgtSentence"> Para obtener instrucciones, consulte el tema <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be Managed by Windows Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8d6772563c15bcb66b4994da41573e40" id="tgt57" class="tgtSentence">0x80043004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bed09621c09af1b4d8be8f2aee7e3f62" id="tgt58" class="tgtSentence">La suscripción no existe o está deshabilitada.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="64f3611084d4201b2ae1b5aa9051b989" id="tgt59" class="tgtSentence">Compruebe que su cuenta y la suscripción a <token>wit_nextref</token> todavía están activas.</caps:sentence>
                        <caps:sentence sentenceid="e14bf57faf6d681707fb4f1752bb4d8a" id="tgt60" class="tgtSentence"> Para ver la configuración de la cuenta, inicie sesión con su cuenta en el <externalLink><linkText>Portal de cuentas de Microsoft Intune</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=247978</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4ce87444ac3e3158964c9d7ed402887f" id="tgt61" class="tgtSentence">0x80043002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="84b285d65fee5813acbf190521baca17" id="tgt62" class="tgtSentence">La cuenta está en modo de mantenimiento.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="675782b2f56835b5c49f0690ff484adc" id="tgt63" class="tgtSentence">No es posible inscribir nuevos equipos cliente cuando la cuenta está en modo de mantenimiento.</caps:sentence>
                        <caps:sentence sentenceid="e14bf57faf6d681707fb4f1752bb4d8a" id="tgt64" class="tgtSentence"> Para ver la configuración de la cuenta, inicie sesión con su cuenta en el <externalLink><linkText>Portal de cuentas de Microsoft Intune</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=247978</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ea6ea9f0f78ec32c6d3da32d02e9a38c" id="tgt65" class="tgtSentence">0x80043003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="99baa28fa222aa9fb75787f41e19857b" id="tgt66" class="tgtSentence">Se ha eliminado la cuenta.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="64f3611084d4201b2ae1b5aa9051b989" id="tgt67" class="tgtSentence">Compruebe que su cuenta y la suscripción a <token>wit_nextref</token> todavía están activas.</caps:sentence>
                        <caps:sentence sentenceid="e14bf57faf6d681707fb4f1752bb4d8a" id="tgt68" class="tgtSentence"> Para ver la configuración de la cuenta, inicie sesión con su cuenta en el <externalLink><linkText>Portal de cuentas de Microsoft Intune</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=247978</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="33ced72ae5a53530dd7754d11baabacf" id="tgt69" class="tgtSentence">0x80043005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c7cb4259ff001fe2bf7aa78d763c43da" id="tgt70" class="tgtSentence">Se ha retirado el equipo cliente.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4c4e213a398dbbb4981246dd9f7c1877" id="tgt71" class="tgtSentence">Espere unas pocas horas, quite cualquier versión anterior del software cliente del equipo y, a continuación, intente instalar de nuevo el software cliente.</caps:sentence>
                        <caps:sentence sentenceid="dba73f72c649c5a7c9a7b7f3cb9b69ff" id="tgt72" class="tgtSentence"> Para ver instrucciones, consulte <link xlink:href="e31df2d2-bb1b-491b-9a71-04e0b18829c1#BKMK_Whattodo">What to do if the client will not uninstall from the Microsoft Intune administrator console</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d069fd814feb1f4dc37bf07bae2ae96e" id="tgt73" class="tgtSentence">0x80043006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="de5ec21772f82f8b82ea127c00d17887" id="tgt74" class="tgtSentence">Se alcanzó el máximo número de puestos permitido para la cuenta.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="92936eb7ac96d30c3c731c365853b5ec" id="tgt75" class="tgtSentence">Su organización debe adquirir puestos adicionales antes de inscribir más equipos cliente en el servicio.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="79a2356706d117d056878a74eadfb327" id="tgt76" class="tgtSentence">0x80043007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b34770e788000dbb89e2386c54008a0e" id="tgt77" class="tgtSentence">No se encontró el archivo de certificado en la misma carpeta que el programa de instalación.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b4c35067af361a4841bd2110bcf7b1be" id="tgt78" class="tgtSentence">Extraiga todos los archivos antes de iniciar la instalación.</caps:sentence>
                        <caps:sentence sentenceid="4598f9272d519bd0bf685d4f2211ce46" id="tgt79" class="tgtSentence"> No cambie el nombre ni la ubicación de los archivos extraídos: todos los archivos deben existir en la misma carpeta o de lo contrario, la instalación será errónea.</caps:sentence>
                        <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt80" class="tgtSentence"> Para obtener más información, vea <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be Managed by Windows Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="fc763cb31e9938f37737394681228f83" id="tgt81" class="tgtSentence">
                          <ui>0x8024D015</ui>, <ui>0x00240005</ui>, <ui>0x80070BC2</ui>, <ui>0x80070BC9</ui>, <ui>0x80CFD015</ui></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="aa67ccb90cef3f31c561c6593aea0538" id="tgt82" class="tgtSentence">No se puede instalar el software porque el equipo cliente está pendiente de reiniciarse.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9f2276687f4a1d2cf2a47002bb58d49c" id="tgt83" class="tgtSentence">Reinicie el equipo y, a continuación, intente instalar de nuevo el software cliente.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5bc7ff30c3364a538a79884d42936113" id="tgt84" class="tgtSentence">0x80070032</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5fdd8c92b1f201c3ab09167fd0e3c6e9" id="tgt85" class="tgtSentence">No se encontró uno o más requisitos previos para instalar el software cliente en el equipo cliente.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8f36b6bbe71bad4308fb1c92cef0d875" id="tgt86" class="tgtSentence">Asegúrese de que las actualizaciones necesarias están instaladas en el equipo cliente y, a continuación, intente instalar de nuevo el software cliente.</caps:sentence>
                        <caps:sentence sentenceid="26dffe1cfe503a8fbcef471063a3b80f" id="tgt87" class="tgtSentence"> Para obtener más información sobre los requisitos previos para instalar el software cliente, vea <link xlink:href="074de65b-84a5-4a01-a824-18ffd838eab0">Requirements for Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="7cd81359d7a563abd094dc55989fb265" id="tgt88" class="tgtSentence">0x80043008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ff4155a57d02787e570efcb41524ffec" id="tgt89" class="tgtSentence">No se pudo iniciar el servicio Microsoft Online Management Updates.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="76c2f1165dda60bcf89ff1a5b1635a2c" id="tgt90" class="tgtSentence">Póngase en contacto con el <externalLink><linkText>Soporte técnico</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=246606</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="004fedea1020dd94462ec7084c5633ed" id="tgt91" class="tgtSentence">0x80043009</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4a53868a6463a68deb01255825fa63d5" id="tgt92" class="tgtSentence">El equipo cliente ya está inscrito en el servicio.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6532334d66ab2f94cec600bad4f43459" id="tgt93" class="tgtSentence">Debe retirar el equipo cliente para poder volver a inscribirlo en el servicio.</caps:sentence>
                        <caps:sentence sentenceid="dba73f72c649c5a7c9a7b7f3cb9b69ff" id="tgt94" class="tgtSentence"> Para ver instrucciones, consulte <link xlink:href="e31df2d2-bb1b-491b-9a71-04e0b18829c1#BKMK_Whattodo">What to do if the client will not uninstall from the Microsoft Intune administrator console</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d76b38ad1bfa2b8251266808c7f9ac04" id="tgt95" class="tgtSentence">0x8004300B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="a1fda97e567e3beaeae1fd58c8af0b8c" id="tgt96" class="tgtSentence">No se puede ejecutar el paquete de instalación del software cliente porque no se admite la versión de Windows que se está ejecutando en el cliente.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="016cb0b05f6b37887bbf56db62604781" id="tgt97" class="tgtSentence">
                          <token>wit_firstref</token> no es compatible con la versión de Windows que se está ejecutando en el equipo cliente.</caps:sentence>
                        <caps:sentence sentenceid="34bb066516068ccd41c841b626c89b53" id="tgt98" class="tgtSentence"> Para obtener una lista de sistemas operativos compatibles, consulte <link xlink:href="074de65b-84a5-4a01-a824-18ffd838eab0">Requirements for Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="65b48070f5ec2594794d6b184b0017f0" id="tgt99" class="tgtSentence">0xAB2</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="06a617bd88682c0130b0a9e2aac4d0d6" id="tgt100" class="tgtSentence">Windows Installer no pudo tener acceso al tiempo de ejecución de VBScript para una acción personalizada.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="43c9b75a1525731845091a8f7a217a4a" id="tgt101" class="tgtSentence">Este error está causado por una acción personalizada basada en Bibliotecas de vínculos dinámicos (DLL).</caps:sentence>
                        <caps:sentence sentenceid="74ffa7faa6a4ca45af899b0702aa3c3f" id="tgt102" class="tgtSentence"> Cuando solucione problemas de DLL, quizás deba usar las herramientas que se describen en <externalLink><linkText>Microsoft Support KB198038: Herramientas útiles para problemas de implementación y de paquete</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=234255</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="d2ffbb3c0cde188e7145c2daa4d383d6" id="tgt103" class="tgtSentence">0x8004300f</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="86820bead769eaf1574d045a67063992" id="tgt104" class="tgtSentence">No se puede instalar el software porque ya está instalado el cliente de System Center Configuration Manager.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="4398e009efbc6ed30947e2680bdd81cf" id="tgt105" class="tgtSentence">Quite el cliente de Configuration Manager y, a continuación, vuelva a intentar la instalación del software cliente.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="5b7ea17883f49bc7203fdc784f15d4a9" id="tgt106" class="tgtSentence">0x80043010</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0652352d6340d4d261cd71ed267098d4" id="tgt107" class="tgtSentence">El software no se puede instalar porque ya está instalado el cliente de Open Mobile Alliance Device Management (OMADM).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5649f1898cf750f0548386fa310a0ec3" id="tgt108" class="tgtSentence">Anule la inscripción del cliente de OMADM y vuelva a intentar instalar el software cliente.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="33bc860974a8935e8053a6f686a61416" id="tgt109" class="tgtSentence">Si el problema de instalación continúa, póngase en contacto con el <externalLink><linkText>Soporte técnico</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=246606</linkUri></externalLink>.</caps:sentence>
                <caps:sentence sentenceid="cc4bcfd2e59502e289dc7dbb7f5ceef3" id="tgt110" class="tgtSentence"> Tenga a mano el registro de inscripción del equipo cliente (que se encuentra en % <placeholder>archivosdeprograma</placeholder>% \Microsoft\OnlineManagement\Logs\Enrollment.log), y %<placeholder>perfildeusuario</placeholder>%\AppData\Local\Microsoft\OnlineManagement\Logs\Enrollement.log) y el registro de Windows Update (%<placeholder>windir</placeholder>%\windowsupdate.log) para mostrarlos a los ingenieros de soporte técnico.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para></para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">Troubleshooting client set up problems</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">Use the following sections to help you troubleshoot common client setup problems.</caps:sentence>
          </para>
        </content>
        <sections>
          <section expanded="true">
            <title>
              <caps:sentence id="src3" class="srcSentence">What to do if client installation fails</caps:sentence>
            </title>
            <content>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src4" class="srcSentence">If no client software deployment alerts for the computer are displayed in the <token>wit_adminconsole</token>, check the computer’s Internet connectivity and proxy configuration and make sure that the computer can communicate with the service URL, <externalLink><linkText>https://manage.microsoft.com</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>.</caps:sentence>
                    <caps:sentence id="src5" class="srcSentence"> Then retry the client software installation.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">You can have an email sent to selected recipients when a client software deployment failure alert occurs by configuring a notification rule in the <ui>Admin</ui> workspace.</caps:sentence>
                    <caps:sentence id="src7" class="srcSentence"> For more information, see <link xlink:href="396ea714-0433-4bd5-a934-8d0b477f28e4">Configure Alerts in Windows Intune</link>.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src8" class="srcSentence">
                      <token>wit_firstref</token> displays the critical alert <ui>Client Software Deployment Failure</ui> if the client software fails to deploy.</caps:sentence>
                    <caps:sentence id="src9" class="srcSentence"> This will display in the <ui>System Overview</ui> page and <ui>Alerts</ui> pages of the <token>wit_adminconsole</token>.</caps:sentence>
                    <caps:sentence id="src10" class="srcSentence"> Check for alerts by using the following procedure:</caps:sentence>
                  </para>
                </listItem>
              </list>
              <procedure expanded="false">
                <title>
                  <caps:sentence id="src11" class="srcSentence">To check alerts for failed installations</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src12" class="srcSentence">In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com/</linkUri></externalLink>, click <ui>Alerts</ui> &gt; <ui>Overview</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src13" class="srcSentence">On the <ui>Alerts overview</ui> page, you can review the following information:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src14" class="srcSentence">The top three alerts, which can be sorted by date, category, or severity </caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src15" class="srcSentence">The total number of active alerts</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src16" class="srcSentence">Click <ui>All Alerts</ui> to display the following information on the <ui>Alerts</ui> page.</caps:sentence>
                        <caps:sentence id="src17" class="srcSentence"> Critical alerts are displayed first:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src18" class="srcSentence">
                              <ui>Name</ui> – The name of the alert type that generated the alert.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src19" class="srcSentence">
                              <ui>Source</ui> – A link to the source of the alert.</caps:sentence>
                            <caps:sentence id="src20" class="srcSentence">  If the display threshold of the alert type is set to <ui>All</ui>, then this link will display a single affected device.</caps:sentence>
                            <caps:sentence id="src21" class="srcSentence">  If the display threshold of the alert type is set to a value, then this link will display a list of all the devices that are affected by this alert.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src22" class="srcSentence">
                              <ui>Last Updated</ui> – This indicates the time when the alert was last modified.</caps:sentence>
                            <caps:sentence id="src23" class="srcSentence"> If an alert is closed, the time when the alert was closed is displayed.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src24" class="srcSentence">
                              <ui>Severity</ui> – This indicates the severity of the alert</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section expanded="true" address="BKMK_Whattodo">
            <title>
              <caps:sentence id="src25" class="srcSentence">What to do if the client will not uninstall from the Microsoft Intune administrator console</caps:sentence>
            </title>
            <content>
              <para></para>
              <procedure expanded="true">
                <title>
                  <caps:sentence id="src26" class="srcSentence">To remove the client software by using the Microsoft Intune command line tool</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src27" class="srcSentence">Open a command prompt in administrator mode.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src28" class="srcSentence">Go to the folder <legacyItalic>%programfiles%\Microsoft\OnlineManagement\Common</legacyItalic></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src29" class="srcSentence">Run the following command - <system>ProvisioningUtil.exe /UninstallAgents /MicrosoftIntune</system></caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
          <section expanded="true">
            <title>
              <caps:sentence id="src30" class="srcSentence">Client installation error codes</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src31" class="srcSentence">The following table describes error codes that are displayed in <ui>Alerts</ui> if client software installation fails.</caps:sentence>
                <caps:sentence id="src32" class="srcSentence"> It includes suggestions for resolving the problem that is represented by each error code.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src33" class="srcSentence">Error code</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">Possible problem</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">Suggested resolution</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src36" class="srcSentence">0x80CF0437</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">The clock on the client computer is not set to the correct time.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">Make sure that the clock and the time zone on the client computer are set to the correct time and time zone.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src39" class="srcSentence">
                          <ui>0x80240438</ui>, <ui>0x80CF0438</ui>, <ui>0x80CF401B</ui></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">Cannot connect to the <token>wit_firstref</token> service.</caps:sentence>
                        <caps:sentence id="src41" class="srcSentence"> Check the client proxy settings.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">Verify that the proxy configuration on the client computer is supported by <token>wit_firstref</token>, and that the client computer has Internet access.</caps:sentence>
                        <caps:sentence id="src43" class="srcSentence"> For more information about supported proxy configurations, see <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help secure your computers with Endpoint Protection and Windows Firewall policy for Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src44" class="srcSentence">0x80CF402C</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">Cannot connect to the <token>wit_firstref</token> service.</caps:sentence>
                        <caps:sentence id="src46" class="srcSentence"> Check network connectivity.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src47" class="srcSentence">Verify the computer has network connectivity.</caps:sentence>
                        <caps:sentence id="src48" class="srcSentence"> Ensure the network cable is connected or wireless network in on.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src49" class="srcSentence">0x80240438, 0x80CF0438</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">Proxy settings in Internet Explorer and Local System are not configured.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">Check the client proxy settings and confirm that the proxy configuration on the client computer is supported by <token>wit_firstref</token>, and that the client computer has Internet access.</caps:sentence>
                        <caps:sentence id="src52" class="srcSentence"> For more information about supported proxy configurations, see <link xlink:href="682a83ec-bcf4-46ed-9a74-61b87b6a86a3">Help secure your computers with Endpoint Protection and Windows Firewall policy for Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">
                          <ui>0x80043001</ui> </caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src54" class="srcSentence">Enrollment package is out of date.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src55" class="srcSentence">Download and install the current client software package from the <ui>Admin</ui> workspace.</caps:sentence>
                        <caps:sentence id="src56" class="srcSentence"> For instructions, see the <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be Managed by Windows Intune</link> topic.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src57" class="srcSentence">0x80043004</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">Subscription does not exist, or is disabled.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src59" class="srcSentence">Verify that your account and subscription to <token>wit_nextref</token> is still active.</caps:sentence>
                        <caps:sentence id="src60" class="srcSentence"> To view your account settings, sign in to your account in the <externalLink><linkText>Microsoft Intune account portal</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=247978</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src61" class="srcSentence">0x80043002</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src62" class="srcSentence">Account is in maintenance mode.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">You cannot enroll new client computers when the account is in maintenance mode.</caps:sentence>
                        <caps:sentence id="src64" class="srcSentence"> To view your account settings, sign in to your account in the <externalLink><linkText>Microsoft Intune account portal</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=247978</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src65" class="srcSentence">0x80043003</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">Account is deleted.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src67" class="srcSentence">Verify that your account and subscription to <token>wit_nextref</token> is still active.</caps:sentence>
                        <caps:sentence id="src68" class="srcSentence"> To view your account settings, sign in to your account in the <externalLink><linkText>Microsoft Intune account portal</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=247978</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src69" class="srcSentence">0x80043005</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src70" class="srcSentence">The client computer is retired.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">Wait a few hours, remove any older versions of the client software from the computer, and then retry the client software installation.</caps:sentence>
                        <caps:sentence id="src72" class="srcSentence"> For instructions, see <link xlink:href="e31df2d2-bb1b-491b-9a71-04e0b18829c1#BKMK_Whattodo">What to do if the client will not uninstall from the Microsoft Intune administrator console</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src73" class="srcSentence">0x80043006</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src74" class="srcSentence">The maximum number of seats allowed for the account is reached.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src75" class="srcSentence">Your organization must purchase additional seats before you can enroll more client computers in the service.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src76" class="srcSentence">0x80043007</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src77" class="srcSentence">Could not find the certificate file in the same folder as the installer program.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src78" class="srcSentence">Extract all files before you start the installation.</caps:sentence>
                        <caps:sentence id="src79" class="srcSentence"> Do not rename or relocate any of the extracted files: all files must exist in the same folder or the installation will fail.</caps:sentence>
                        <caps:sentence id="src80" class="srcSentence"> For more information, see <link xlink:href="64c11e53-8d64-41b9-9550-4b4e395e8c52">Set up Your Computers to be Managed by Windows Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src81" class="srcSentence">
                          <ui>0x8024D015</ui>, <ui>0x00240005</ui>, <ui>0x80070BC2</ui>, <ui>0x80070BC9</ui>, <ui>0x80CFD015</ui></caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src82" class="srcSentence">The software cannot be installed because a restart of the client computer is pending.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src83" class="srcSentence">Restart the computer and then retry the client software installation.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src84" class="srcSentence">0x80070032</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src85" class="srcSentence">One or more prerequisites for installing the client software were not found on the client computer.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src86" class="srcSentence">Make sure that all required updates are installed on the client computer and then retry the client software installation.</caps:sentence>
                        <caps:sentence id="src87" class="srcSentence"> For more information about prerequisites for installing the client software, see <link xlink:href="074de65b-84a5-4a01-a824-18ffd838eab0">Requirements for Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src88" class="srcSentence">0x80043008</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">Could not start the Microsoft Online Management Updates service.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">Contact <externalLink><linkText>Support</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=246606</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src91" class="srcSentence">0x80043009</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">The client computer is already enrolled into the service.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src93" class="srcSentence">You must retire the client computer before you can re-enroll it in the service.</caps:sentence>
                        <caps:sentence id="src94" class="srcSentence"> For instructions, see <link xlink:href="e31df2d2-bb1b-491b-9a71-04e0b18829c1#BKMK_Whattodo">What to do if the client will not uninstall from the Microsoft Intune administrator console</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src95" class="srcSentence">0x8004300B</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src96" class="srcSentence">The client software installation package cannot run because the version of Windows that is running on the client is not supported.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src97" class="srcSentence">
                          <token>wit_firstref</token> does not support the version of Windows that is running on the client computer.</caps:sentence>
                        <caps:sentence id="src98" class="srcSentence"> For a list of supported operating systems, see <link xlink:href="074de65b-84a5-4a01-a824-18ffd838eab0">Requirements for Microsoft Intune</link>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src99" class="srcSentence">0xAB2</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src100" class="srcSentence">The Windows Installer could not access VBScript run time for a custom action.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src101" class="srcSentence">This error is caused by a custom action that is based on Dynamic-Link Libraries (DLLs).</caps:sentence>
                        <caps:sentence id="src102" class="srcSentence"> When troubleshooting the DLL, you might have to use the tools that are described in <externalLink><linkText>Microsoft Support KB198038: Useful Tools for Package and Deployment Issues</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=234255</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src103" class="srcSentence">0x8004300f</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src104" class="srcSentence">The software cannot be installed because the System Center Configuration Manager client is already installed.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src105" class="srcSentence">Remove the Configuration Manager client and then retry the client software installation.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src106" class="srcSentence">0x80043010</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">The software cannot be installed because the Open Mobile Alliance Device Management (OMADM) client is already installed.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src108" class="srcSentence">Un-enroll the OMADM client and then retry the client software installation.</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src109" class="srcSentence">If installation problems persist, contact <externalLink><linkText>Support</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=246606</linkUri></externalLink>.</caps:sentence>
                <caps:sentence id="src110" class="srcSentence"> Have the client computer enrollment log (located in %<placeholder>programfiles</placeholder>%\Microsoft\OnlineManagement\Logs\Enrollment.log and %<placeholder>userprofile</placeholder>%\AppData\Local\Microsoft\OnlineManagement\Logs\Enrollement.log) and Windows Update log (%<placeholder>windir</placeholder>%\windowsupdate.log) available to show to support engineers.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>