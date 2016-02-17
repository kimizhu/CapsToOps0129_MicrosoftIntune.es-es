---
title: Preparar aplicaciones de Android para la administraci&#243;n de aplicaciones m&#243;viles con Microsoft Intune App Wrapping Tool
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9c349c8-51ae-4d73-b74a-6173728a520b
---
# Preparar aplicaciones de Android para la administraci&#243;n de aplicaciones m&#243;viles con Microsoft Intune App Wrapping Tool
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="16859c9da62799922bc88b1c7de34fc3" id="tgt1" class="tgtSentence">Use <ui>Microsoft Intune App Wrapping Tool para Android</ui> para modificar el comportamiento de las aplicaciones de Android internas que le permite configurar las características de la aplicación sin modificar el código de la propia aplicación.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a439d3fb68c19754c8a5f84c2aac91b4" id="tgt2" class="tgtSentence">La herramienta es una aplicación de línea de comandos de Windows que se ejecuta en PowerShell y crea un "contenedor" alrededor de la aplicación.</caps:sentence>
          <caps:sentence sentenceid="f258ccff1fb266954a63f0d56a1fbb16" id="tgt3" class="tgtSentence"> Una vez que se procesa una aplicación, puede cambiar la funcionalidad de aplicaciones con una directiva de administración de aplicaciones móviles de <token>wit_nextref</token> (consulte <link xlink:href="b4fb33a8-a2fa-4353-bd89-5bda48b68e83">Control apps using mobile application management policies with Microsoft Intune</link>).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fa8a2b98f0efead1e83eecc6ae6b1118" id="tgt4" class="tgtSentence">Si la aplicación usa la Biblioteca de autenticación de Azure Active Directory (ADAL), debe completar los pasos de <link xlink:href="#BKMK_ADAL_android"> How to wrap apps that use the Azure Active Directory Library (ADAL)</link> antes de ajustar la aplicación.</caps:sentence>
          <caps:sentence sentenceid="6d6753df9c4764c087ebba5d091e0a7e" id="tgt5" class="tgtSentence"> Si no está seguro de si su aplicación usa esta biblioteca, póngase en contacto con el desarrollador de la aplicación.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="eba3f086400611143d99728fd46d5058" id="tgt6" class="tgtSentence">Antes de ejecutar la herramienta, revise <link xlink:href="e9c349c8-51ae-4d73-b74a-6173728a520b#BKMK_androidappwraptool">Security considerations for running the app wrapping tool</link>.</caps:sentence>
          <caps:sentence sentenceid="1e327fcc5ef8a07ba04f5b42a4e1d895" id="tgt7" class="tgtSentence"> Para descargar la herramienta, consulte <externalLink><linkText>Herramienta de ajuste de aplicaciones de Microsoft Intune para Android</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=47267</linkUri></externalLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="20b5a1df0a4cc8104c2c22808ae4acb7" id="tgt8" class="tgtSentence">Paso 1: cumplir los requisitos previos para usar la herramienta de ajuste de aplicaciones</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="9f90004d2bfb5f8bef3446223b3ee15d" id="tgt9" class="tgtSentence">Debe ejecutar la herramienta de ajuste de aplicaciones en un equipo de Windows con Windows 7 o posterior.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="06668b0d20b666478a628bab968d7f4e" id="tgt10" class="tgtSentence">La aplicación de entrada debe ser un paquete de aplicación de Android válido con la extensión <ui>.apk</ui> y:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8f4cfa26146146aa86d2e1fb2a397d2b" id="tgt11" class="tgtSentence">No se puede cifrar</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fc9d5a60463895e282af5a9e6f4bfb87" id="tgt12" class="tgtSentence">No debe haberse ajustado aún con la herramienta de ajuste de aplicaciones</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="022d286a50e070197d1dd45e01b9c29a" id="tgt13" class="tgtSentence">Debe estar escrita para Android 4.0 o posterior</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d4b1fec14afd544c7762d77b4bec5f3f" id="tgt14" class="tgtSentence">La aplicación debe haber sido desarrollada por o para su compañía.</caps:sentence>
                <caps:sentence sentenceid="7a9305ec65bf0b4ae17f230120d50f98" id="tgt15" class="tgtSentence"> No se puede usar esta herramienta para procesar aplicaciones descargadas de Google Play Store.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="d64fef3ada801c18c1e7f4f1710078a3" id="tgt16" class="tgtSentence">Para ejecutar la herramienta de ajuste de aplicaciones, debe instalar la versión más reciente de <externalLink target="_blank"><linkText>Java Runtime Environment</linkText><linkUri>http://java.com/download/</linkUri></externalLink> y, luego, asegurarse de que se ha establecido la variable de ruta de acceso de Java en <ui>C:\ProgramData\Oracle\Java\javapath</ui> en las variables de entorno de Windows.</caps:sentence>
                <caps:sentence sentenceid="90114e0ccfddcdc296352e9caa9a37cf" id="tgt17" class="tgtSentence"> Para obtener más información, consulte la <externalLink><linkText>documentación de Java</linkText><linkUri>http://java.com/download/help/</linkUri></externalLink>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="393a8870d631000b80b8c9239e156944" id="tgt18" class="tgtSentence">En algunos casos, la versión de 32 bits de Java puede producir problemas de memoria.</caps:sentence>
                  <caps:sentence sentenceid="89cc5509e9e97c72a5402a4fa2f1d74c" id="tgt19" class="tgtSentence"> En su lugar, se recomienda instalar la versión de 64 bits.</caps:sentence>
                </para>
              </alert>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="acfdf3c87206282ea521092bf8f81408" id="tgt20" class="tgtSentence">Paso 2: instalar la herramienta de ajuste de aplicaciones</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence sentenceid="b25826a2a096798eef811c63a56ed0f4" id="tgt21" class="tgtSentence">Instalar la herramienta de ajuste de aplicaciones</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="c5af6594dd97713b2155c73720ee778f" id="tgt22" class="tgtSentence">Desde el centro de descarga de Microsoft, descargue y abra el archivo de instalación de de la herramienta de ajuste de aplicaciones en un equipo de Windows.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="bf63d3bf667e820965248ed3940afbfe" id="tgt23" class="tgtSentence">Acepte el contrato de licencia y complete la instalación.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="88b46f96b6de0b5eece7ed7d9b0c3f98" id="tgt24" class="tgtSentence">Tome nota de la carpeta donde instala la herramienta.</caps:sentence>
                  <caps:sentence sentenceid="7e8bc23adba31fc9bc4e574612856eb1" id="tgt25" class="tgtSentence"> La ubicación predeterminada es: <ui>C:\Archivos de programa (x86)\Administración de aplicaciones móviles de Microsoft Intune\Android\Herramienta de ajuste de aplicaciones</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="6e5cf4a90e9572a480973787810b4f9f" id="tgt26" class="tgtSentence">Paso 3: ejecutar la herramienta de ajuste de aplicaciones</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="154ef67b3bd7f0aacf016ce7c365b1fa" id="tgt27" class="tgtSentence">En el equipo de Windows donde instaló la herramienta de ajuste de aplicaciones, abra una ventana de PowerShell.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="8bdf20566f5f86c3ebfbc7e25952ff2c" id="tgt28" class="tgtSentence">Desde la carpeta donde instaló la herramienta, importe el módulo de PowerShell de la aplicación de ajuste de aplicaciones:</caps:sentence>
                  </para>
                  <code>Import-Module .\IntuneAppWrappingTool.psm1</code>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="5fdfbd6839d6dbd94d585b3f456665b0" id="tgt29" class="tgtSentence">Ejecute la herramienta mediante el comando <ui>invoke-AppWrappingTool</ui> junto con los siguientes parámetros.</caps:sentence>
                    <caps:sentence sentenceid="56ae3e1d682ac85b1cfbca9e5538de18" id="tgt30" class="tgtSentence"> Los parámetros que están marcados como "opcionales" son para las aplicaciones que usan la Biblioteca de Azure Active Directory (ADAL).</caps:sentence>
                    <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt31" class="tgtSentence"> Para obtener más información, vea <link xlink:href="#BKMK_ADAL_android"> How to wrap apps that use the Azure Active Directory Library (ADAL)</link>.</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="03144cce1fcdacdbe993e5266c0bf3f3" id="tgt32" class="tgtSentence">Parámetro</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt33" class="tgtSentence">Más información</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt34" class="tgtSentence">
                              <userInput>-InputPath</userInput> <placeholder>&lt;String&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="48f4bfe265751678a3793135678b7fdd" id="tgt35" class="tgtSentence">Ruta de acceso de la aplicación de Android (.apk) de origen.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt36" class="tgtSentence">
                              <userInput>-OutputPath</userInput> <placeholder>&lt;String&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="a9dbb3002efd6901e32da88a078ae7da" id="tgt37" class="tgtSentence">Ruta de acceso a la aplicación de Android de "salida".</caps:sentence>
                            <caps:sentence sentenceid="97f96292b9ed0b5dea44e12bced96062" id="tgt38" class="tgtSentence"> Si se trata de la misma ruta de acceso al directorio que InputPath, se producirá un error en el empaquetado.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt39" class="tgtSentence">
                              <userInput>-KeyStorePath</userInput> <placeholder>&lt;String&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="6326730627468382c5ff96da2ea16c85" id="tgt40" class="tgtSentence">Ruta de acceso al archivo de almacén de claves que contiene el par de claves pública y privada para firmar.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt41" class="tgtSentence">
                              <userInput>-KeyStorePassword</userInput> <placeholder>&lt;SecureString&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="014b48bd9342b68f589fc59ea348e2b5" id="tgt42" class="tgtSentence">Contraseña usada para descifrar el almacén de claves.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt43" class="tgtSentence">
                              <userInput>-KeyAlias</userInput> <placeholder>&lt;String&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="97d129b183a028f89c9894eb80890344" id="tgt44" class="tgtSentence">Nombre de la clave que se usará para firmar.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt45" class="tgtSentence">
                              <userInput>-KeyPassword</userInput> <placeholder>&lt;SecureString&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="fb17f615fe78f3b97a99e056fefee4d4" id="tgt46" class="tgtSentence">Contraseña usada para descifrar la clave privada que se usará para firmar.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt47" class="tgtSentence">
                              <userInput>-SigAlg</userInput> <placeholder>&lt;SecureString&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="64afa1bda7004ed2fed05b6df29b2f0e" id="tgt48" class="tgtSentence">Nombre del algoritmo de firma que se usará para firmar.</caps:sentence>
                            <caps:sentence sentenceid="e6a4d37352c76bbf73afed5b63724f74" id="tgt49" class="tgtSentence"> El algoritmo debe ser compatible con la clave privada.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="a4c5ddf27dc2ad5a494993fc14453d0b" id="tgt50" class="tgtSentence">Ejemplos: SHA256withRSA, SHA1withRSA, MD5withRSA</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt51" class="tgtSentence">
                              <userInput>-ClientID</userInput> <placeholder>&lt;GUID&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="1d10fefe1bc7d633263c21ece56e2392" id="tgt52" class="tgtSentence">Identificador de cliente de Azure Active Directory de la aplicación de entrada (opcional).</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt53" class="tgtSentence">
                              <userInput>-AuthorityURI</userInput> <placeholder>&lt;Uri&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="17e23f1437851192c9eede58a2ff2787" id="tgt54" class="tgtSentence">URI de autoridad de Azure Active Directory de la aplicación de entrada (opcional).</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt55" class="tgtSentence">
                              <userInput>-SkipBroker</userInput> <placeholder>&lt;Boolean&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="11a10bcf64ec1a53a3525ce97a596509" id="tgt56" class="tgtSentence">Indica si la aplicación de entrada admite el inicio de sesión único asíncrono en todo el dispositivo (opcional).</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ad7e9d669d2c92050903e84056ac39fa" id="tgt57" class="tgtSentence">True: la aplicación de entrada no admite el inicio de sesión único asíncrono en todo el dispositivo.</caps:sentence>
                                <caps:sentence sentenceid="fdbd9a07368778437484aa0a084305b6" id="tgt58" class="tgtSentence"> Use el parámetro NonBrokerRedirectURI.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="3aa5703204194e6f9e76b7945fb9a779" id="tgt59" class="tgtSentence">False: la aplicación de entrada admite el inicio de sesión asíncrono en todo el dispositivo.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt60" class="tgtSentence">
                              <userInput>-NonBrokerRedirectURI</userInput> <placeholder>&lt;URI&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3effe966d2a7ef43e63256fbc288a656" id="tgt61" class="tgtSentence">URI de redireccionamiento de Azure Active Directory que se debe usar si SkipBroker es true (opcional).</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <placeholder>
                              <caps:sentence sentenceid="e1638f98e453efff823153bdbfad32d3" id="tgt62" class="tgtSentence">&lt;CommonParameters&gt;</caps:sentence>
                            </placeholder>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="4e4b942e18f7323df7d24ed0e5fb35a6" id="tgt63" class="tgtSentence">(opcional, admite parámetros comunes de PowerShell como verbose, debug, etc.)</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="1c8abc0643f979bdc0042f74c71bce37" id="tgt64" class="tgtSentence">Para obtener una lista de los parámetros comunes, consulte el <externalLink><linkText>Centro de scripts de Microsoft</linkText><linkUri>https://technet.microsoft.com/library/hh847884.aspx</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <para>
                    <caps:sentence sentenceid="077b03af4afdc73094033d8db108a9bb" id="tgt65" class="tgtSentence">Para ver la ayuda de la herramienta, escriba el comando:</caps:sentence>
                  </para>
                  <code>Help Invoke-AppWrappingTool</code>
                  <para>
                    <caps:sentence sentenceid="cf7e919f701bb4e782ba5dcb5b278078" id="tgt66" class="tgtSentence">Obtenga más información acerca de la integración de Azure Active Directory (AAD) <externalLink><linkText>aquí</linkText><linkUri>https://technet.microsoft.com/library/dn878028.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <ui>
                      <caps:sentence sentenceid="ca15073256d06d36bc03993f0f30893c" id="tgt67" class="tgtSentence">Ejemplo:</caps:sentence>
                    </ui>
                  </para>
                  <code>Import-Module "C:\Program Files (x86)\Microsoft Intune Mobile Application Management\Android\App Wrapping Tool\IntuneAppWrappingTool.psm1" Invoke-AppWrappingTool –InputPath &lt;input-app.apk&gt; -OutputPath &lt;output-app.apk&gt; -KeyStorePath &lt;path-to-signing.keystore&gt; -KeyAlias &lt;signing-key-name&gt; -ClientID &lt;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx&gt; -AuthorityURI &lt;http://AzureActivieDirectory.Authority.URL&gt; -SkipBroker&lt;$True|$False&gt; -NonBrokerRedirectURI &lt;urn:xxx:xx:xxxx:xx:xxx&gt;
</code>
                  <para>
                    <caps:sentence sentenceid="0c09d9b64d697b9cfba4522eef66489c" id="tgt68" class="tgtSentence">A continuación, se le pedirá que especifique <ui>KeyStorePassword</ui> y <ui>KeyPassword</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="f5ff9316f3f1323397f4839c0d2cc069" id="tgt69" class="tgtSentence">La aplicación ajustada se genera y guarda, junto con un archivo de registro en la ruta de acceso de salida especificada.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_androidappwraptool">
        <title>
          <caps:sentence sentenceid="8bf0d825ec60bbea6a2857e62b345be1" id="tgt70" class="tgtSentence">Consideraciones de seguridad para ejecutar la aplicación en la herramienta de ajuste</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b7e8362da562e5e5cb70aea71741f93d" id="tgt71" class="tgtSentence">Para evitar posibles suplantaciones de identidad, la divulgación de información y ataques de elevación de privilegios:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="fdecc43cd3543e1e002b422c88fe963e" id="tgt72" class="tgtSentence">Asegúrese de que la aplicación de línea de negocio de entrada, la aplicación de salida y Java KeyStore estén en el mismo equipo donde se ejecuta la herramienta de ajuste de aplicaciones.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="17f4394efc03f8c1c55233160d02054a" id="tgt73" class="tgtSentence">Importe la aplicación de salida para la consola de Intune en el mismo equipo donde se ejecuta la herramienta.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4ec5e418fdc48aef2d6abf33eb53ece4" id="tgt74" class="tgtSentence">Si la aplicación de salida y la herramienta se encuentran en una ruta de acceso de convención de nomenclatura universal (UNC), y no ejecuta la herramienta y los archivos de entrada en el mismo equipo, configure el entorno para que sea seguro mediante el <externalLink><linkText>protocolo de seguridad de Internet  (IPsec)</linkText><linkUri>http://en.wikipedia.org/wiki/IPsec</linkUri></externalLink> o <externalLink><linkText>la firma del bloque de mensajes del servidor (SMB)</linkText><linkUri>https://support.microsoft.com/en-us/kb/887429</linkUri></externalLink>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8c6a66d3d58deef58e500ff2ff3fe7a7" id="tgt75" class="tgtSentence">Asegúrese de que la aplicación procede de un origen de confianza, especialmente si utiliza Azure Active Directory (AAD), que podría permitir a la aplicación acceder al token de AAD durante el tiempo de ejecución.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a6ec218c5e95c902fa87ec61a7672d6f" id="tgt76" class="tgtSentence">Proteja el directorio de salida que contiene la aplicación ajustada.</caps:sentence>
                <caps:sentence sentenceid="f7fc126bd9db0f081aa0899e43972e33" id="tgt77" class="tgtSentence"> Considere el uso de un directorio de nivel de usuario para la salida.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para></para>
        </content>
      </section>
      <section address="BKMK_ADAL_android" expanded="true">
        <title>
          <caps:sentence sentenceid="a5764d93e31c29d9303febda2e6e41cb" id="tgt78" class="tgtSentence">
          Cómo ajustar las aplicaciones que usan la biblioteca de Azure Active Directory (ADAL)</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="faf282c8e0c983229b98052a358545dd" id="tgt79" class="tgtSentence">Si la aplicación usa la Biblioteca de autenticación de Azure Active Directory (ADAL), debe completar estos pasos antes de ajustar la aplicación.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="3910ac8f65eb04e5efa4ed54e91cc53f" id="tgt80" class="tgtSentence">Paso 1: asegúrese de cumplir los requisitos de ADAL</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="66f2af5b99dde2088913e4a2cfb6b52a" id="tgt81" class="tgtSentence">Para las aplicaciones que usen ADAL, deben cumplirse las siguientes condiciones:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="7a34f85c51a2fb788117832082e04c2b" id="tgt82" class="tgtSentence">La aplicación debe incorporar una versión de ADAL igual o posterior a la versión 1.0.2.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e3eccef3e304e8c7476fc90b3464e753" id="tgt83" class="tgtSentence">El desarrollador debe <link xlink:href="99ab0369-5115-4dc8-83ea-db7239b0de97#BKMK_AD">grant their app access to the Intune Mobile Application Management resource</link>.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_review_IDs">
            <title>
              <caps:sentence sentenceid="298efb91903b1e40a459394f5ce59765" id="tgt84" class="tgtSentence">Paso 2: revise los identificadores que necesita obtener al registrar la aplicación</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="40dac0eab119021fa04798d1eb40d3c8" id="tgt85" class="tgtSentence">En el paso siguiente, va a usar el Portal de administración de Azure para registrar las aplicaciones (que usan ADAL con Azure Active Directory (AAD)) para obtener los identificadores únicos que se muestran en la siguiente tabla.</caps:sentence>
                <caps:sentence sentenceid="b943345f53bd8e72fa4ee21ee9db0c83" id="tgt86" class="tgtSentence"> A continuación, entregue los identificadores al desarrollador cuando vaya a integrar ADAL con la aplicación.</caps:sentence>
                <caps:sentence sentenceid="2f306aaa5dee30a562ebe3c78598bff8" id="tgt87" class="tgtSentence"> Para obtener más información sobre estos valores de identificador, consulte <externalLink><linkText>Biblioteca de autenticación de Microsoft Azure Active Directory (ADAL) para Android</linkText><linkUri>https://github.com/AzureAD/azure-activedirectory-library-for-android/blob/master/README.md</linkUri></externalLink>.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f393f3f5e496869a15bc72cbfd56f541" id="tgt88" class="tgtSentence">Identificador</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt89" class="tgtSentence">Más información</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="313af772d92d01300d5e89512cd93bd0" id="tgt90" class="tgtSentence">Valor predeterminado</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="796b5045502934ad2f1885a22f5b76ef" id="tgt91" class="tgtSentence">Identificador de cliente</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="7bd40a06b31cf6919691d32ce4d5ddb7" id="tgt92" class="tgtSentence">Identificador GUID único que se genera para la aplicación después de registrarla con AAD.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="bf0fc45f3187302e9acc4f5220d1e087" id="tgt93" class="tgtSentence">Si conoce el identificador de cliente de la aplicación, especifique ese valor.</caps:sentence>
                        <caps:sentence sentenceid="1415f41f35b4571f148a362903448739" id="tgt94" class="tgtSentence"> De lo contrario, use el valor predeterminado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="5dd51c3eb9be0fff84f7f746c2906e9b" id="tgt95" class="tgtSentence">6c7e8096-f593-4d72-807f-a5f86dcc9c77</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="06ba7f6730602f8c39d11777607e711c" id="tgt96" class="tgtSentence">URI de autoridad</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="d07d44695aacc7ecf377435809791163" id="tgt97" class="tgtSentence">El valor del identificador uniforme de recursos (URI) de autoridad para los objetos de AAD (por ejemplo, los usuarios y grupos).</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="1e34a62394450d789775b3667cd7b987" id="tgt98" class="tgtSentence">El parámetro AuthorityURI es opcional para la herramienta de ajuste de aplicaciones.</caps:sentence>
                        <caps:sentence sentenceid="06d78f26f03d4eb68611b837f8f1edc6" id="tgt99" class="tgtSentence"> Si no usa el parámetro, se usa el URI predeterminado.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1b813f8c6023639b686fec8f02b94ed2" id="tgt100" class="tgtSentence">https://login.windows.net/common/</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="3bb97a5f5dcc9a4dd5ca4399c3a47c24" id="tgt101" class="tgtSentence">SkipBroker</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="6adafb091b5e1eee047b703f908079c9" id="tgt102" class="tgtSentence">Valor que indica si el portal de empresa se usará como agente.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="875e8702018eff26e9ab825f55171426" id="tgt103" class="tgtSentence">
                              <ui>True</ui>: el portal de empresa no se usará para la autenticación de ADAL.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="6b57aac4f2e0f25232e9d8d7bd41c088" id="tgt104" class="tgtSentence">
                              <ui>False</ui>: el portal de empresa se usará para la autenticación de ADAL.</caps:sentence>
                            <caps:sentence sentenceid="c56c233c44d2b4a3e7ec8bd5766e1660" id="tgt105" class="tgtSentence"> El portal de empresa usa el usuario inscrito para fines de inicio de sesión único.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                    <TD></TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8f6bc12eea9f0c695f1632c2b5362e8d" id="tgt106" class="tgtSentence">URI de redireccionamiento que no es del agente</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="aaf870fa1c08525fa3d42e83bd2a7774" id="tgt107" class="tgtSentence">URI de inicio de sesión que se usará cuando ADAL no use la aplicación del agente (portal de empresa de Intune)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="55d1dba84eb7de3ff1618d4f0aaa34fc" id="tgt108" class="tgtSentence">urn:ietf:wg:oauth:2.0:oob</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="8f3ce16ef626311833c49d80b1b1ef14" id="tgt109" class="tgtSentence">Identificador de recurso</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ef4afa9bc6a41155fb12b3152528c5a1" id="tgt110" class="tgtSentence">Puntero a los recursos de AAD de la aplicación.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="82818524377c1dc55593f0736aab2fab" id="tgt111" class="tgtSentence">https://intunemam.microsoftonline.com</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_AD">
            <title>
              <caps:sentence sentenceid="738e0072ab5a46a3a75e3d573377db36" id="tgt112" class="tgtSentence">Paso 3: configure el acceso a la administración de aplicaciones móviles en AAD</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="09b5873c740b8365ad245f1a4d6e44e5" id="tgt113" class="tgtSentence">Antes de poder usar los valores de registro de AAD de una aplicación en la herramienta de ajuste de aplicaciones, el desarrollador de aplicaciones debe conceder ese acceso de la aplicación al recurso de Administración de aplicaciones móviles de Intune siguiendo estos pasos:</caps:sentence>
              </para>
              <procedure>
                <title></title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="886f67041f4fcc6723953d8d0bce3022" id="tgt114" class="tgtSentence">Inicie sesión en una cuenta de AAD existente en el Portal de administración de Azure.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt115" class="tgtSentence">Haga clic en <ui>Registro existente de la aplicación LOB</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt116" class="tgtSentence">En la sección <ui>Configurar</ui>, elija <ui>Configurar acceso a API web en otras aplicaciones</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="4aa8bb2927d80fd9fa367663dbf82e40" id="tgt117" class="tgtSentence">En la primera lista desplegable de la sección <ui>Permiso en otras aplicaciones</ui>, elija <ui>Administración de aplicaciones móviles de Intune</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence sentenceid="e697df48032d3ef8d3c44448dbbc364c" id="tgt118" class="tgtSentence">Ahora puede usar el identificador de cliente de la aplicación en la herramienta de ajuste de aplicaciones.</caps:sentence>
                      <caps:sentence sentenceid="9fddaca35cad05981fd11f47e1a73570" id="tgt119" class="tgtSentence"> Puede encontrar el identificador de cliente en el Portal de administración de Azure Active Directory, tal como se describe en la tabla de <link xlink:href="#BKMK_review_IDs">Step 2: Review the identifiers that you need to get when you register the app</link>.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="f19dbe7a512dfc8a4487b9bf672e6b95" id="tgt120" class="tgtSentence">Paso 4: use los valores del identificador de AAD en la herramienta de ajuste de aplicaciones</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="3c55cd08637aacc0a33dc68e370947a5" id="tgt121" class="tgtSentence">A partir de los valores del identificador que obtuvo en el proceso de registro, escriba los valores como propiedades de línea de comandos en la herramienta de ajuste de aplicaciones.</caps:sentence>
                <caps:sentence sentenceid="8b82184c514a4f6073a3abc0713fdf88" id="tgt122" class="tgtSentence"> Debe especificar todos los valores de la tabla en orden para que los usuarios finales puedan autenticar correctamente la aplicación.</caps:sentence>
                <caps:sentence sentenceid="bae50f4696bc7c758c794364692085e5" id="tgt123" class="tgtSentence"> Si no especifica algún valor, se usarán los predeterminados.</caps:sentence>
              </para>
              <table border="1">
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="f393f3f5e496869a15bc72cbfd56f541" id="tgt124" class="tgtSentence">Identificador</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="03144cce1fcdacdbe993e5266c0bf3f3" id="tgt125" class="tgtSentence">Parámetro</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="796b5045502934ad2f1885a22f5b76ef" id="tgt126" class="tgtSentence">Identificador de cliente</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="bf04c59b953aaad945bb10ee0eac532d" id="tgt127" class="tgtSentence">ClientID</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="06ba7f6730602f8c39d11777607e711c" id="tgt128" class="tgtSentence">URI de autoridad</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="279e678c18fc1a59391f8b0f2d290904" id="tgt129" class="tgtSentence">Authority-URI</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3bb97a5f5dcc9a4dd5ca4399c3a47c24" id="tgt130" class="tgtSentence">SkipBroker</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="3bb97a5f5dcc9a4dd5ca4399c3a47c24" id="tgt131" class="tgtSentence">SkipBroker</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8f6bc12eea9f0c695f1632c2b5362e8d" id="tgt132" class="tgtSentence">URI de redireccionamiento que no es del agente</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="b9a6fd80a9c76e4b1f2cf769e74c9503" id="tgt133" class="tgtSentence">NonBrokerRedirectURI</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8f3ce16ef626311833c49d80b1b1ef14" id="tgt134" class="tgtSentence">Identificador de recurso</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="90438536d00b39eda2092a7c2bf40d0f" id="tgt135" class="tgtSentence">ResourceID</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="f1ce4af178f6e2334f2597eddc01f5fa" id="tgt136" class="tgtSentence">Tenga presentes los siguientes puntos al ajustar la aplicación:   </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="cd60e298d272f2283e57b5323e4dc2a0" id="tgt137" class="tgtSentence">La herramienta de ajuste de aplicaciones no buscará archivos binarios ADAL (si existen) en la aplicación.</caps:sentence>
                    <caps:sentence sentenceid="5b87106d51334263de2a7e0359943956" id="tgt138" class="tgtSentence"> Si la aplicación se vincula a una versión no actualizada de los archivos binarios y si se habilitaron directivas de autenticación, pueden producirse errores en tiempo de ejecución durante el inicio de sesión.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="18e775b58778e1203999994266bce2d3" id="tgt139" class="tgtSentence">Para comprobar que la autenticación se realizó correctamente, <token>wit_nextref</token> captura el token de AAD que está asociado con el identificador de recurso MAM.</caps:sentence>
                    <caps:sentence sentenceid="bd73d8eb1e8ea24b94fa3679a08a98d8" id="tgt140" class="tgtSentence"> Sin embargo, el token no se usa en ninguna llamada que a su vez pueda comprobar la validez del token.</caps:sentence>
                    <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt141" class="tgtSentence">
                      <token>wit_nextref</token> solo lee el nombre principal de usuario (UPN) del usuario con sesión iniciada para determinar el acceso a la aplicación.</caps:sentence>
                    <caps:sentence sentenceid="2b8553864b335a64fbf9e6c219c95911" id="tgt142" class="tgtSentence"> El token de AAD no se usa para las demás llamadas de servicio.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="7de378086c300622c9db8c0d4a962329" id="tgt143" class="tgtSentence">Los tokens de autenticación se comparten entre aplicaciones del mismo editor, dado que se almacenan en llaveros compartidos.</caps:sentence>
                    <caps:sentence sentenceid="f1b624c4ce0961b2160278221cf0bd85" id="tgt144" class="tgtSentence"> Para aislar una aplicación concreta, use un certificado de firma distinto, un almacén de claves de perfiles de aprovisionamiento y el alias de la clave de esa aplicación.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="217f3f72131c9f2ae6ad873c1b0b5205" id="tgt145" class="tgtSentence">Las peticiones de inicio de sesión dobles pueden evitarse si proporciona el identificador de cliente y el URI de entidad de la aplicación cliente.</caps:sentence>
                    <caps:sentence sentenceid="269b771648ba46532fc2c6eb878c00ad" id="tgt146" class="tgtSentence"> Deberá registrar el identificador de cliente para habilitar su acceso al identificador del recurso MAM de <token>wit_nextref</token> publicado en panel de AAD.</caps:sentence>
                    <caps:sentence sentenceid="dbea281dc7aeb920b5e62d77f16d2a3e" id="tgt147" class="tgtSentence"> Si no registra el identificador de cliente, los usuarios obtendrán un error de inicio de sesión cuando se ejecute la aplicación.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <nextSteps>
        <content>
          <para>
            <caps:sentence sentenceid="2cfc7aa51cdee76b0903e5f8ce4c1fd0" id="tgt148" class="tgtSentence">Para obtener más información acerca de cómo implementar las aplicaciones ajustadas, consulte <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy apps to mobile devices in Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </nextSteps>
      <relatedTopics>
        <link xlink:href="b4fb33a8-a2fa-4353-bd89-5bda48b68e83">Protect data using mobile application management policies with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use the <ui>Microsoft Intune App Wrapping Tool for Android</ui> to modify the behavior of your in-house Android apps to let you configure features of the app without modifying the code of the app itself.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">The tool is a Windows command line application that runs in PowerShell and creates a ‘wrapper’ around your app.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Once the app is processed, you can then change the app’s functionality using an <token>wit_nextref</token> mobile application management policy (see <link xlink:href="b4fb33a8-a2fa-4353-bd89-5bda48b68e83">Control apps using mobile application management policies with Microsoft Intune</link>).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">If your app is using the Azure Active Directory Authentication Library (ADAL), you must complete the steps in <link xlink:href="#BKMK_ADAL_android"> How to wrap apps that use the Azure Active Directory Library (ADAL)</link> before you wrap your app.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> If you are unsure if your app uses this library, contact the developer of the app.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">Before running the tool, review the <link xlink:href="e9c349c8-51ae-4d73-b74a-6173728a520b#BKMK_androidappwraptool">Security considerations for running the app wrapping tool</link>.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> To download the tool, see <externalLink><linkText>Microsoft Intune App Wrapping Tool for Android</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=47267</linkUri></externalLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Step 1: Fulfill the prerequisites for using the app wrapping tool</caps:sentence>
        </title>
        <content>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src9" class="srcSentence">You must run the app wrapping tool on a Windows computer running Windows 7 or later.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src10" class="srcSentence">Your input app must be a valid Android application package with the extension <ui>.apk</ui> file and:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src11" class="srcSentence">Cannot be encrypted</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src12" class="srcSentence">Must not have already been wrapped by the app wrapping tool</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Must be written for Android 4.0 or later</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">The app must be developed by, or for your company.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> You cannot use this tool to process apps downloaded from the Google Play Store.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src16" class="srcSentence">To run the app wrapping tool, you must install the latest version of the <externalLink target="_blank"><linkText>Java Runtime Environment</linkText><linkUri>http://java.com/download/</linkUri></externalLink> and then ensure that the Java path variable has been set to <ui>C:\ProgramData\Oracle\Java\javapath</ui> in your Windows environment variables.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> For more help, see your <externalLink><linkText>Java documentation</linkText><linkUri>http://java.com/download/help/</linkUri></externalLink>.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src18" class="srcSentence">In some cases, the 32-bit version of Java may result in memory issues.</caps:sentence>
                  <caps:sentence id="src19" class="srcSentence"> We recommend that you install the 64-bit version instead.</caps:sentence>
                </para>
              </alert>
            </listItem>
          </list>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Step 2: Install the App Wrapping Tool</caps:sentence>
        </title>
        <content>
          <procedure>
            <title>
              <caps:sentence id="src21" class="srcSentence">Install the app wrapping tool</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">From the Microsoft Download Center, download and open the installation file for the app wrapping tool to a Windows computer.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">Accept the license agreement, then complete the installation.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src24" class="srcSentence">Note the folder to which you installed the tool.</caps:sentence>
                  <caps:sentence id="src25" class="srcSentence"> The default location is: <ui>C:\Program Files (x86)\Microsoft Intune Mobile Application Management\Android\App Wrapping Tool</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src26" class="srcSentence">Step 3: Run the App Wrapping Tool</caps:sentence>
        </title>
        <content>
          <procedure>
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src27" class="srcSentence">On the Windows computer where you installed the app wrapping tool, open a PowerShell window.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">From the folder where you installed the tool, import the app wrapping tool PowerShell module:</caps:sentence>
                  </para>
                  <code>Import-Module .\IntuneAppWrappingTool.psm1</code>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src29" class="srcSentence">Run the tool by using the <ui>invoke-AppWrappingTool</ui> command together with the following parameters.</caps:sentence>
                    <caps:sentence id="src30" class="srcSentence"> Parameters that are marked as "optional" are for apps that use Azure Active Directory Library (ADAL).</caps:sentence>
                    <caps:sentence id="src31" class="srcSentence"> For more information, see <link xlink:href="#BKMK_ADAL_android"> How to wrap apps that use the Azure Active Directory Library (ADAL)</link>.</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src32" class="srcSentence">Parameter</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src33" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src34" class="srcSentence">
                              <userInput>-InputPath</userInput> <placeholder>&lt;String&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src35" class="srcSentence">Path of the source Android app (.apk).</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src36" class="srcSentence">
                              <userInput>-OutputPath</userInput> <placeholder>&lt;String&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src37" class="srcSentence">Path to the "output" Android app.</caps:sentence>
                            <caps:sentence id="src38" class="srcSentence"> If this is the same directory path as InputPath, the packaging will fail.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src39" class="srcSentence">
                              <userInput>-KeyStorePath</userInput> <placeholder>&lt;String&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src40" class="srcSentence">Path to the keystore file that contains the public/private key pair for signing.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src41" class="srcSentence">
                              <userInput>-KeyStorePassword</userInput> <placeholder>&lt;SecureString&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src42" class="srcSentence">Password used to decrypt the keystore.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src43" class="srcSentence">
                              <userInput>-KeyAlias</userInput> <placeholder>&lt;String&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src44" class="srcSentence">Name of the key to be used for signing.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src45" class="srcSentence">
                              <userInput>-KeyPassword</userInput> <placeholder>&lt;SecureString&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src46" class="srcSentence">Password used to decrypt the private key that will be used for signing.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src47" class="srcSentence">
                              <userInput>-SigAlg</userInput> <placeholder>&lt;SecureString&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src48" class="srcSentence">Name of the signature algorithm to be used for signing.</caps:sentence>
                            <caps:sentence id="src49" class="srcSentence"> The algorithm must be compatible with the private key.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src50" class="srcSentence">Examples: SHA256withRSA, SHA1withRSA, MD5withRSA</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src51" class="srcSentence">
                              <userInput>-ClientID</userInput> <placeholder>&lt;GUID&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src52" class="srcSentence">Azure Active Directory Client ID of the input app (optional).</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src53" class="srcSentence">
                              <userInput>-AuthorityURI</userInput> <placeholder>&lt;Uri&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src54" class="srcSentence">Azure Active Directory Authority URI of the input app (optional).</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src55" class="srcSentence">
                              <userInput>-SkipBroker</userInput> <placeholder>&lt;Boolean&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src56" class="srcSentence">Indicates whether the input application supports device-wide brokered single sign-on (optional).</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src57" class="srcSentence">True - the input application does not support device-wide brokered single sign-on.</caps:sentence>
                                <caps:sentence id="src58" class="srcSentence"> Use the NonBrokerRedirectURI parameter.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src59" class="srcSentence">False - the input application supports device-wide brokered single sign-on</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src60" class="srcSentence">
                              <userInput>-NonBrokerRedirectURI</userInput> <placeholder>&lt;URI&gt;</placeholder></caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src61" class="srcSentence">Azure Active Directory Redirect URI to use if SkipBroker is true (optional).</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <placeholder>
                              <caps:sentence id="src62" class="srcSentence">&lt;CommonParameters&gt;</caps:sentence>
                            </placeholder>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src63" class="srcSentence">(optional – supports common PowerShell parameters such as verbose, debug, etc.)</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src64" class="srcSentence">For a list of common parameters, see the <externalLink><linkText>Microsoft Script Center</linkText><linkUri>https://technet.microsoft.com/library/hh847884.aspx</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">To see help for the tool, enter the command:</caps:sentence>
                  </para>
                  <code>Help Invoke-AppWrappingTool</code>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">To find out more about Azure Active Directory (AAD) integration, see <externalLink><linkText>here</linkText><linkUri>https://technet.microsoft.com/library/dn878028.aspx</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <ui>
                      <caps:sentence id="src67" class="srcSentence">Example:</caps:sentence>
                    </ui>
                  </para>
                  <code>Import-Module "C:\Program Files (x86)\Microsoft Intune Mobile Application Management\Android\App Wrapping Tool\IntuneAppWrappingTool.psm1" Invoke-AppWrappingTool –InputPath &lt;input-app.apk&gt; -OutputPath &lt;output-app.apk&gt; -KeyStorePath &lt;path-to-signing.keystore&gt; -KeyAlias &lt;signing-key-name&gt; -ClientID &lt;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx&gt; -AuthorityURI &lt;http://AzureActivieDirectory.Authority.URL&gt; -SkipBroker&lt;$True|$False&gt; -NonBrokerRedirectURI &lt;urn:xxx:xx:xxxx:xx:xxx&gt;
</code>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">You will then be prompted for the <ui>KeyStorePassword</ui> and <ui>KeyPassword</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src69" class="srcSentence">The wrapped app is generated, and saved, along with a log file, in the output path you specified.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section address="BKMK_androidappwraptool">
        <title>
          <caps:sentence id="src70" class="srcSentence">Security considerations for running the app wrapping tool</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src71" class="srcSentence">To prevent potential spoofing, information disclosure, and elevation of privilege attacks:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src72" class="srcSentence">Ensure that the input line-of-business application, output application, and Java KeyStore are on the same computer where the app wrapping tool is running.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src73" class="srcSentence">Import the output application to the Intune Console on the same computer where the tool is running.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src74" class="srcSentence">If the output application and the tool are on a Universal Naming Convention (UNC) path and you are not running the tool and input files on the same computer, configure the environment to be secure by using <externalLink><linkText>Internet Protocol Security (IPsec)</linkText><linkUri>http://en.wikipedia.org/wiki/IPsec</linkUri></externalLink> or <externalLink><linkText>Server Message Block (SMB) signing</linkText><linkUri>https://support.microsoft.com/en-us/kb/887429</linkUri></externalLink>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src75" class="srcSentence">Ensure that the application is coming from a trusted source, especially if you are using Azure Active Directory (AAD), which might enable the application to access the AAD token during runtime.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src76" class="srcSentence">Secure the output directory that contains the wrapped app.</caps:sentence>
                <caps:sentence id="src77" class="srcSentence"> Consider using a user-level directory for the output.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para></para>
        </content>
      </section>
      <section address="BKMK_ADAL_android" expanded="true">
        <title>
          <caps:sentence id="src78" class="srcSentence">
          How to wrap apps that use the Azure Active Directory Library (ADAL)</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src79" class="srcSentence">If your app is using the Azure Active Directory Authentication Library (ADAL), you must complete these steps before you wrap your app.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src80" class="srcSentence">Step 1: Ensure that you meet the requirements for ADAL</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src81" class="srcSentence">For apps that use ADAL, the following must be true:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">The app must incorporate an ADAL version greater than or equal to 1.0.2.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src83" class="srcSentence">The developer must <link xlink:href="99ab0369-5115-4dc8-83ea-db7239b0de97#BKMK_AD">grant their app access to the Intune Mobile Application Management resource</link>.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section address="BKMK_review_IDs">
            <title>
              <caps:sentence id="src84" class="srcSentence">Step 2: Review the identifiers that you need to get when you register the app</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src85" class="srcSentence">In the next step, you will use the Azure management portal to register your apps (which are using  ADAL with Azure Active Directory (AAD)) to get the unique identifiers listed in the following table.</caps:sentence>
                <caps:sentence id="src86" class="srcSentence"> You then give the identifiers to the developer when you integrate ADAL with the app.</caps:sentence>
                <caps:sentence id="src87" class="srcSentence"> For more information about these identifier values, see <externalLink><linkText>Microsoft Azure Active Directory Authentication Library (ADAL) for Android</linkText><linkUri>https://github.com/AzureAD/azure-activedirectory-library-for-android/blob/master/README.md</linkUri></externalLink>.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src88" class="srcSentence">Identifier</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">More information</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">Default value</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src91" class="srcSentence">Client ID</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src92" class="srcSentence">A unique GUID identifier that is generated for the app after it is registered with AAD.</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src93" class="srcSentence">If you know the app's Client ID, specify that value.</caps:sentence>
                        <caps:sentence id="src94" class="srcSentence"> Otherwise, use the default value.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src95" class="srcSentence">6c7e8096-f593-4d72-807f-a5f86dcc9c77</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src96" class="srcSentence">Authority URI</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src97" class="srcSentence">The authority Uniform Resource Identifier (URI) value for AAD) objects (for example, users and groups).</caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src98" class="srcSentence">The AuthorityURI parameter is optional for the app wrapping tool.</caps:sentence>
                        <caps:sentence id="src99" class="srcSentence"> The default URI is used if you don't use the parameter.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src100" class="srcSentence">https://login.windows.net/common/</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src101" class="srcSentence">SkipBroker</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src102" class="srcSentence">Value indicating whether the company portal will be used as a broker.</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src103" class="srcSentence">
                              <ui>True</ui> – company portal will not be used for ADAL authentication.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src104" class="srcSentence">
                              <ui>False</ui> – company portal will be used for ADAL authentication.</caps:sentence>
                            <caps:sentence id="src105" class="srcSentence"> The company portal is using the enrolled user for Single Sign On purposes.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                    </TD>
                    <TD></TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src106" class="srcSentence">Non-Broker Redirect URI</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src107" class="srcSentence">Login URI to be used when ADAL does not use the broker app (Intune company portal).</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src108" class="srcSentence">urn:ietf:wg:oauth:2.0:oob</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <ui>
                          <caps:sentence id="src109" class="srcSentence">Resource ID</caps:sentence>
                        </ui>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src110" class="srcSentence">Pointer to the app's AAD resources.</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src111" class="srcSentence">https://intunemam.microsoftonline.com</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </content>
          </section>
          <section address="BKMK_AD">
            <title>
              <caps:sentence id="src112" class="srcSentence">Step 3: Configure access to mobile application management in AAD</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src113" class="srcSentence">Before you can use an app’s AAD registration values in the app wrapping tool, the application developer must grant that application access to the Intune Mobile Application Management resource by following these steps:</caps:sentence>
              </para>
              <procedure>
                <title></title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src114" class="srcSentence">Log into an existing AAD account in the Azure management portal.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src115" class="srcSentence">Click <ui>existing LOB application registration</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src116" class="srcSentence">In the <ui>configure</ui> section, choose <ui>Configure Access to Web APIs in other applications</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src117" class="srcSentence">From the first drop-down list in the <ui>Permission to other applications</ui> section, choose <ui>Intune Mobile Application Management</ui>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                </steps>
                <conclusion>
                  <content>
                    <para>
                      <caps:sentence id="src118" class="srcSentence">You can now use the app’s Client ID in the app wrapping tool.</caps:sentence>
                      <caps:sentence id="src119" class="srcSentence"> You can find the Client ID in the Azure Active Directory management portal, as described in the table in <link xlink:href="#BKMK_review_IDs">Step 2: Review the identifiers that you need to get when you register the app</link>.</caps:sentence>
                    </para>
                  </content>
                </conclusion>
              </procedure>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src120" class="srcSentence">Step 4: Use the AAD identifier values in the app wrapping tool</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src121" class="srcSentence">Using the identifier values that you got from the registration process, enter the values as command-line properties in the app wrapping tool.</caps:sentence>
                <caps:sentence id="src122" class="srcSentence"> You must specify all of the values in the table in order for end users to successfully authenticate the app.</caps:sentence>
                <caps:sentence id="src123" class="srcSentence"> Default values are used if you don't specify a value.</caps:sentence>
              </para>
              <table border="1">
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src124" class="srcSentence">Identifier</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src125" class="srcSentence">Parameter</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src126" class="srcSentence">Client ID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src127" class="srcSentence">ClientID</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src128" class="srcSentence">Authority URI</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src129" class="srcSentence">Authority-URI</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src130" class="srcSentence">SkipBroker</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src131" class="srcSentence">SkipBroker</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src132" class="srcSentence">Non-Broker Redirect URI</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src133" class="srcSentence">NonBrokerRedirectURI</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src134" class="srcSentence">Resource ID</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src135" class="srcSentence">ResourceID</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src136" class="srcSentence">Keep the following points in mind as you wrap your app:   </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src137" class="srcSentence">The app wrapping tool does not search for ADAL binaries (if any) within the app.</caps:sentence>
                    <caps:sentence id="src138" class="srcSentence"> If the app links to an outdated version of the binaries, runtime errors may occur during login if you enabled authentication policies.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src139" class="srcSentence">To verify that the authentication was successful, <token>wit_nextref</token> fetches the AAD token that is associated with the MAM resource-id.</caps:sentence>
                    <caps:sentence id="src140" class="srcSentence"> However, the token is not used in any call that would in turn verify the validity of the token.</caps:sentence>
                    <caps:sentence id="src141" class="srcSentence">
                      <token>wit_nextref</token> only reads the user principal name (UPN) of the signed-in user to determine app access.</caps:sentence>
                    <caps:sentence id="src142" class="srcSentence"> The AAD token is not used for any further service calls.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src143" class="srcSentence">Authentication tokens are shared between apps from the same publisher since they are stored in a shared keychain.</caps:sentence>
                    <caps:sentence id="src144" class="srcSentence"> To isolate a specific app, use a different signing certificate, provisioning profile keystore, and key alias for that app.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src145" class="srcSentence">Double login prompts are prevented if you provide your client application’s Client ID and Authority URI.</caps:sentence>
                    <caps:sentence id="src146" class="srcSentence"> You need to register the Client ID to enable it to access the published <token>wit_nextref</token> MAM resource ID in the AAD Dashboard.</caps:sentence>
                    <caps:sentence id="src147" class="srcSentence"> If you don't register the Client ID, users get a login failure when the app runs.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <nextSteps>
        <content>
          <para>
            <caps:sentence id="src148" class="srcSentence">To learn more about how to deploy your wrapped apps, see <link xlink:href="6da30550-9e8e-4333-b9b3-83928de3807a">Deploy apps to mobile devices in Microsoft Intune</link>.</caps:sentence>
          </para>
        </content>
      </nextSteps>
      <relatedTopics>
        <link xlink:href="b4fb33a8-a2fa-4353-bd89-5bda48b68e83">Protect data using mobile application management policies with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>