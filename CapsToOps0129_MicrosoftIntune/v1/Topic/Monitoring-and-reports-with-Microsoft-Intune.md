---
title: Supervisi&#243;n e informes con Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0f7dc155-cb8e-477b-ba02-2623194a9575
---
# Supervisi&#243;n e informes con Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="70adde6b9ccf32f57021f49bbf8cd702" id="tgt1" class="tgtSentence">Como administrador de TI, deseará supervisar el estado de los dispositivos de su organización.</caps:sentence>
          <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt2" class="tgtSentence">
            <token>wit_firstref</token> ofrece dos métodos para supervisar estos dispositivos, así como el estado de la licencia de software y las acciones que afectan a los dispositivos (por ejemplo, la eliminación de un dispositivo).</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="790eaf34912a6ca854a3ed4ffbb6551e" id="tgt3" class="tgtSentence">Los <legacyBold><externalLink><linkText>Informes</linkText><linkUri>https://technet.microsoft.com/library/dn646977.aspx</linkUri></externalLink></legacyBold> le ayudan a supervisar el estado de los dispositivos administrados por <token>wit_nextref</token> (incluido el estado de instalación del software, el software instalado y el cumplimiento de certificados).</caps:sentence>
              <caps:sentence sentenceid="5d7b762eea9b1d8eb75c0f1588e8a6d6" id="tgt4" class="tgtSentence"> Asimismo, estos informes le permiten examinar el inventario de hardware y software recopilado por los equipos y los dispositivos.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="adce1679a87d5bb772e3889b22b3012f" id="tgt5" class="tgtSentence">Las <legacyBold><externalLink><linkText>Alertas</linkText><linkUri>https://technet.microsoft.com/library/dn646958.aspx</linkUri></externalLink></legacyBold> le ayudan a supervisar el estado de los dispositivos administrados por <token>wit_nextref</token> (incluido el estado y las alertas de Endpoint Protection, el cual le avisará sobre la existencia de malware, así como advertencias relacionadas con la escasez de conectividad de red o de espacio de disco).</caps:sentence> 
  </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="48ce53fe11e0edcc0f418116392bf8f9" id="tgt6" class="tgtSentence">Aquellos dispositivos y equipos que están administrados por <token>wit_nextref</token>, devuelven información detallada sobre sus propiedades y el software instalado.</caps:sentence>
              <caps:sentence sentenceid="23b58def11b45727d3351702515f86af" id="tgt7" class="tgtSentence">
                <token>wit_nextref</token> le proporciona herramientas e informes que le permitirán examinar y presentar estos datos.</caps:sentence>
              <caps:sentence sentenceid="363ddf43df695c296401df2564573a36" id="tgt8" class="tgtSentence"> Para obtener más información, consulte <link xlink:href="312911fe-b963-4949-9911-ae425e0590b2">Understand your devices with inventory in Microsoft Intune</link>.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="110cbdbf-8f9b-4c1b-9e3e-184113cd711c">Technical reference for Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">As an IT Administrator, you want to monitor the status of devices in your organization.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence">
            <token>wit_firstref</token> provides two ways that you can monitor these devices, as well as software license status and actions that affect devices (such as wiping a device).</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">
                <legacyBold>
                  <externalLink>
                    <linkText>Reports</linkText>
                    <linkUri>https://technet.microsoft.com/library/dn646977.aspx</linkUri>
                  </externalLink>
                </legacyBold> help you to monitor the status of devices managed by <token>wit_nextref</token> (including software update status, software installed, and certificate compliance).</caps:sentence>
              <caps:sentence id="src4" class="srcSentence"> These reports also let you examine the hardware and software inventory collected by devices and computers.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">
                <legacyBold>
                  <externalLink>
                    <linkText>Alerts</linkText>
                    <linkUri>https://technet.microsoft.com/library/dn646958.aspx</linkUri>
                  </externalLink>
                </legacyBold> help you to monitor the health of devices managed by <token>wit_nextref</token> (including Endpoint Protection status and warnings, to alert you to malware; and warnings related to scarcity of disk space or network connectivity).</caps:sentence> 
  </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Devices and computers that are managed by <token>wit_nextref</token> return detailed information about their properties and installed software.</caps:sentence>
              <caps:sentence id="src7" class="srcSentence">
                <token>wit_nextref</token> gives you tools and reports to examine and present this data.</caps:sentence>
              <caps:sentence id="src8" class="srcSentence"> For details, see <link xlink:href="312911fe-b963-4949-9911-ae425e0590b2">Understand your devices with inventory in Microsoft Intune</link>.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics>
        <link xlink:href="110cbdbf-8f9b-4c1b-9e3e-184113cd711c">Technical reference for Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>