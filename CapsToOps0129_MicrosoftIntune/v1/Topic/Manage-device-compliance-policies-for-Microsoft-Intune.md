---
title: Administrar directivas de cumplimiento del dispositivo de Microsoft Intune
ms.custom: na
ms.reviewer: na
ms.service: microsoft-intune
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0775107a-6662-41c8-9404-be14bbb599f3
---
# Administrar directivas de cumplimiento del dispositivo de Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="es-ES">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5a8d044c0c65f966138831b5718a7f13" id="tgt1" class="tgtSentence">
            <ui>Las directivas de cumplimiento</ui> definen las reglas y los valores de configuración que un dispositivo debe cumplir para que se considere conformes a las directivas de acceso condicional.</caps:sentence>
          <caps:sentence sentenceid="53e2dae1d13bc049d933442df0006053" id="tgt2" class="tgtSentence"> Las directivas de cumplimiento también se pueden usar para supervisar y corregir problemas de compatibilidad con dispositivos independientemente del acceso condicional.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3e597f39c3e0c518122c761719442ebd" id="tgt3" class="tgtSentence">Estas reglas incluyen:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="e32681aaa42d0e70c04f63befc2df9bd" id="tgt4" class="tgtSentence">PIN y contraseñas</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5bdf74912a51c34815f11e9a3d20b609" id="tgt5" class="tgtSentence">Cifrado</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="20254e8bd65e0e70f11991cd41058da7" id="tgt6" class="tgtSentence">Si el dispositivo está desbloqueado o modificado</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="e38167ab1b8f58dfe22da52218e652d5" id="tgt7" class="tgtSentence">Si el correo electrónico en el dispositivo administrado por una directiva de <token>wit_nextref</token></caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="e62d38855fae1d8f4bd82457dcfc2029" id="tgt8" class="tgtSentence">El usuario implementa las directivas de cumplimiento para usuarios y dispositivos.</caps:sentence>
          <caps:sentence sentenceid="4d59dea6dd8264ec07d5bca31b48dfeb" id="tgt9" class="tgtSentence"> Cuando se implementa una directiva de cumplimiento para un usuario, se comprueba el cumplimiento de todos los dispositivos del usuario.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="31a517055d4ee6078bc7d83de7ee0e82" id="tgt10" class="tgtSentence">En la siguiente tabla se enumeran los tipos de dispositivos compatibles con las directivas de cumplimiento y se indica cómo se administran los valores de configuración no compatibles cuando se usa la directiva con una directiva de acceso condicional.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="25c58563ac9a9e4d07c44dcb5ccaef38" id="tgt11" class="tgtSentence">Tipo de dispositivo</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="72d8963b8dae62ee1da2b5f309eaf953" id="tgt12" class="tgtSentence">Configuración de contraseña o PIN</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="702459b135b443bc8f5af874c17befce" id="tgt13" class="tgtSentence">Cifrado del dispositivo</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="11088d23635565074ccef4ad69147a9c" id="tgt14" class="tgtSentence">Dispositivo liberado o modificado</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="1c9275115ae474efb130b2831dc6bdb9" id="tgt15" class="tgtSentence">Perfil de correo electrónico</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="28a9b9639ef610db6fd8c6275c7e817b" id="tgt16" class="tgtSentence">Windows 8.1 y posterior</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c6f3b7d0db1365bbd45a80b5e200f773" id="tgt17" class="tgtSentence">Corregido</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt18" class="tgtSentence">No aplicable</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt19" class="tgtSentence">No aplicable</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt20" class="tgtSentence">No aplicable</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="0c22af16b4df02e420abe803e8c325e1" id="tgt21" class="tgtSentence">Windows Phone 8.1 y versiones posteriores</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c6f3b7d0db1365bbd45a80b5e200f773" id="tgt22" class="tgtSentence">Corregido</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c6f3b7d0db1365bbd45a80b5e200f773" id="tgt23" class="tgtSentence">Corregido</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt24" class="tgtSentence">No aplicable</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt25" class="tgtSentence">No aplicable</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="a830ede5c5385c4bc827afc2595ed732" id="tgt26" class="tgtSentence">iOS 6.0 y versiones posteriores</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c6f3b7d0db1365bbd45a80b5e200f773" id="tgt27" class="tgtSentence">Corregido</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f16c539228f6d39a106ec256c3cc3640" id="tgt28" class="tgtSentence">Corregido (estableciendo PIN)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="52c47055de367390cfc78a2ebe7d7fd2" id="tgt29" class="tgtSentence">En cuarentena (no es una configuración)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d67aa223e0c2171d600f68d008d29c33" id="tgt30" class="tgtSentence">En cuarentena</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="1283133a135a2d1ac9674573da9ac862" id="tgt31" class="tgtSentence">Android 4.0 y versiones posteriores</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d67aa223e0c2171d600f68d008d29c33" id="tgt32" class="tgtSentence">En cuarentena</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d67aa223e0c2171d600f68d008d29c33" id="tgt33" class="tgtSentence">En cuarentena</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="52c47055de367390cfc78a2ebe7d7fd2" id="tgt34" class="tgtSentence">En cuarentena (no es una configuración)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt35" class="tgtSentence">No aplicable</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="087d8a92155ec5c222b72ea90edf1e76" id="tgt36" class="tgtSentence">Samsung KNOX Standard 4.0 y posterior</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d67aa223e0c2171d600f68d008d29c33" id="tgt37" class="tgtSentence">En cuarentena</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d67aa223e0c2171d600f68d008d29c33" id="tgt38" class="tgtSentence">En cuarentena</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="52c47055de367390cfc78a2ebe7d7fd2" id="tgt39" class="tgtSentence">En cuarentena (no es una configuración)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="274b68192b056e268f128ff63bfcd4a4" id="tgt40" class="tgtSentence">No aplicable</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="5c61fc53b97bed1bdc73880fef225bd6" id="tgt41" class="tgtSentence">
            <ui>Corregido</ui> = el sistema operativo del dispositivo exige el cumplimiento (por ejemplo, el usuario debe establecer un PIN).</caps:sentence>
          <caps:sentence sentenceid="f2f7fb3d7b2a4f1df5ec1630ec8bfec5" id="tgt42" class="tgtSentence">  La configuración nunca será no conforme.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0c1e7e2b2bc9991e444664524c71ef7b" id="tgt43" class="tgtSentence">
            <ui>En cuarentena</ui> = el sistema operativo del dispositivo no exige el cumplimiento (por ejemplo, los dispositivos Android no obligan al usuario a cifrar el dispositivo).</caps:sentence>
          <caps:sentence sentenceid="3a515ecb941023d3abadb80f49cf4f0f" id="tgt44" class="tgtSentence">  En este caso:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="9d2fa31291ee8a1d91a95335b8b43ced" id="tgt45" class="tgtSentence">El dispositivo se bloqueará si el usuario se rige por una directiva de acceso condicional.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="b175b2adda5682ad55f6fd424966568f" id="tgt46" class="tgtSentence">El portal de empresa o portal web notificará al usuario los problemas de cumplimiento que se produzcan.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_Compliance">
        <title>
          <caps:sentence sentenceid="6dc183f26a38fcc01cb2f7bfbaee8e98" id="tgt47" class="tgtSentence">Paso 1: crear una directiva de cumplimiento</caps:sentence>
        </title>
        <content>
          <procedure expanded="false">
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt48" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Directiva</ui> &gt; <ui>Políticas de cumplimiento</ui> &gt; <ui>Agregar</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt49" class="tgtSentence">En la página <ui>Crear directiva</ui>, configure las opciones que considere necesarias:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3c6456a6367bf7e241500a2b1d147b1f" id="tgt50" class="tgtSentence">Nombre de la configuración</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="5dc731e46ae38b87ff3e3e2eaf459db2" id="tgt51" class="tgtSentence">Más información</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="26bec7c00274ab1fbeb363f54ab78bb7" id="tgt52" class="tgtSentence">Plataformas compatibles</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b068931cc450442b63f5b3d276ea4297" id="tgt53" class="tgtSentence">Nombre</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="27163f6d135e0c010f8f6889bcaecae6" id="tgt54" class="tgtSentence">Escriba un nombre único para la directiva de cumplimiento.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="a181a603769c1f98ad927e7367c7aa51" id="tgt55" class="tgtSentence">Todos</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt56" class="tgtSentence">Descripción</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="e289b12bd979e6d08be3f163bdb85fd9" id="tgt57" class="tgtSentence">Proporcione una descripción que ofrezca una visión general de la directiva de cumplimiento.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="a181a603769c1f98ad927e7367c7aa51" id="tgt58" class="tgtSentence">Todos</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="00e48d1f688610a2c1bc595a2aaad4db" id="tgt59" class="tgtSentence">Requerir una contraseña para desbloquear dispositivos móviles</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="2cf932efe750a292879b13587b350fa7" id="tgt60" class="tgtSentence">Exija a los usuarios que escriban una contraseña para acceder al dispositivo.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="24be3ee92f62c3c9274ca8059075f436" id="tgt61" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt62" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="1283133a135a2d1ac9674573da9ac862" id="tgt63" class="tgtSentence">Android 4.0 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="087d8a92155ec5c222b72ea90edf1e76" id="tgt64" class="tgtSentence">Samsung KNOX Standard 4.0 y posterior</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="9903f598b57a7f39747ca848a1376d18" id="tgt65" class="tgtSentence">Permitir contraseñas sencillas</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="44d6d67387116f5e70bc290d29214894" id="tgt66" class="tgtSentence">Permita a los usuarios crear contraseñas sencillas como "<userInput>1234</userInput>" o "<ui>1111</ui>".</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="24be3ee92f62c3c9274ca8059075f436" id="tgt67" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt68" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="2f276c6158fbb9b45297b2600181d32d" id="tgt69" class="tgtSentence">Longitud mínima de contraseña</caps:sentence>
                            </ui>
                            <superscript>
                              <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt70" class="tgtSentence">1</caps:sentence>
                            </superscript>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="da6bec5aea1ad753b735b5b58c224564" id="tgt71" class="tgtSentence">Especifica el número mínimo de dígitos o caracteres que debe contener la contraseña del usuario.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="24be3ee92f62c3c9274ca8059075f436" id="tgt72" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ff096d14c13e95dfc9db9eb98f194114" id="tgt73" class="tgtSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt74" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="1283133a135a2d1ac9674573da9ac862" id="tgt75" class="tgtSentence">Android 4.0 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="087d8a92155ec5c222b72ea90edf1e76" id="tgt76" class="tgtSentence">Samsung KNOX Standard 4.0 y posterior</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="dca92e82330f06a43bed4c39a9ae8a45" id="tgt77" class="tgtSentence">Tipo de contraseña obligatoria</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="3daabe49be4e9e2c2adef4dbc7e00ce9" id="tgt78" class="tgtSentence">Especifica si los usuarios deben crear una contraseña <ui>alfanumérica</ui> o <ui>numérica</ui>.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="24be3ee92f62c3c9274ca8059075f436" id="tgt79" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="cb088e2350f69256ddc4b220fcc7e1ea" id="tgt80" class="tgtSentence">Windows RT y Windows RT 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ff096d14c13e95dfc9db9eb98f194114" id="tgt81" class="tgtSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt82" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="e86265f097537852961fcdd0d2e8fcba" id="tgt83" class="tgtSentence">Número mínimo de conjuntos de caracteres</caps:sentence>
                            </ui>
                            <superscript>
                              <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt84" class="tgtSentence">1</caps:sentence>
                            </superscript>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="959076d2b0beff36ddd17662b927b4f9" id="tgt85" class="tgtSentence">Si la opción <ui>Tipo de contraseña requerida</ui> está establecida en <ui>Alfanumérica</ui>, esta configuración especifica el número mínimo de caracteres que debe contener la contraseña.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="89f1c6696845095114c62a832fab3a99" id="tgt86" class="tgtSentence">Los conjuntos de cuatro caracteres son los siguientes:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="82ce16d87daa2560588c7a086d8659e6" id="tgt87" class="tgtSentence">Letras minúsculas</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="0329832329101019091695156bbad617" id="tgt88" class="tgtSentence">Letras mayúsculas</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="5503577415fc1d8d6b3818212a1745bc" id="tgt89" class="tgtSentence">Símbolos</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ee5c35ce3d081da90622a10d2272ed5e" id="tgt90" class="tgtSentence">Números</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <para>
                            <caps:sentence sentenceid="19804b9beacd6d9392b33f9035ceeac3" id="tgt91" class="tgtSentence">Si se establece un número superior de caracteres, los usuarios deberán crear contraseñas más complejas.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="76ea4191c8886af62e2ae83d9dcdce57" id="tgt92" class="tgtSentence">En el caso de dispositivos iOS, este valor de configuración se refiere al número de caracteres especiales (por ejemplo, <userInput>!</userInput>, <userInput>#</userInput>, <userInput>&amp;</userInput>) que deben incluirse en la contraseña.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="24be3ee92f62c3c9274ca8059075f436" id="tgt93" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="cb088e2350f69256ddc4b220fcc7e1ea" id="tgt94" class="tgtSentence">Windows RT y Windows RT 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ff096d14c13e95dfc9db9eb98f194114" id="tgt95" class="tgtSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt96" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="9e9b99fa7ec9aee1de52865489683bc6" id="tgt97" class="tgtSentence">Calidad de contraseña</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="cdab8016b1ee295fde6fefa79994fdd1" id="tgt98" class="tgtSentence">Configura los requisitos de contraseña de los dispositivos Android.</caps:sentence>
                            <caps:sentence sentenceid="a286929ca0f740e14eb1d567ac54d6cb" id="tgt99" class="tgtSentence"> Elija de entre las siguientes opciones:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="a368a1f55ee1e0f601fe650eceb758e3" id="tgt100" class="tgtSentence">Biométrico de seguridad baja</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="ac67ede5a84eb5a1add7ff4440e9a485" id="tgt101" class="tgtSentence">Requerido</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="702a17df9a169447aee6411a806375cf" id="tgt102" class="tgtSentence">Al menos numérica</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="51e3a5014f4643220056cade61124067" id="tgt103" class="tgtSentence">Al menos alfabética</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="2ab2bc4d627df20e1af9d2ceb600f226" id="tgt104" class="tgtSentence">Al menos alfanumérica</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence sentenceid="e67ad60dbbda01967d5a5b4f97fcd75b" id="tgt105" class="tgtSentence">Alfanumérica con símbolos</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="1283133a135a2d1ac9674573da9ac862" id="tgt106" class="tgtSentence">Android 4.0 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="087d8a92155ec5c222b72ea90edf1e76" id="tgt107" class="tgtSentence">Samsung KNOX Standard 4.0 y posterior</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="c6f50988cb876f83b08878649ee5446b" id="tgt108" class="tgtSentence">Minutos de inactividad antes de que se pida la contraseña</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="19c7257a9fd4f26e0400d5ce5823fcd7" id="tgt109" class="tgtSentence">Especifica el tiempo de inactividad antes de que el usuario deba volver a escribir la contraseña.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt110" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="2fb470a15f63e1990f7635ac30db44d7" id="tgt111" class="tgtSentence">Expiración de contraseña (días)</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="9fa7d722c04b9fa2c3f9efcf5def1727" id="tgt112" class="tgtSentence">Seleccione el número de días que faltan para que la contraseña caduque y durante los cuales deben crear una nueva.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="24be3ee92f62c3c9274ca8059075f436" id="tgt113" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="cb088e2350f69256ddc4b220fcc7e1ea" id="tgt114" class="tgtSentence">Windows RT y Windows RT 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ff096d14c13e95dfc9db9eb98f194114" id="tgt115" class="tgtSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt116" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="1283133a135a2d1ac9674573da9ac862" id="tgt117" class="tgtSentence">Android 4.0 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="087d8a92155ec5c222b72ea90edf1e76" id="tgt118" class="tgtSentence">Samsung KNOX Standard 4.0 y posterior</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="bd7e3f529ae9c075d09f3b7116bbe632" id="tgt119" class="tgtSentence">Recordar el historial de contraseñas</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c67f3c6b571b9a6b374884f177762791" id="tgt120" class="tgtSentence">Use esta opción junto con <ui>Impedir la reutilización de contraseñas anteriores</ui> para impedir que el usuario cree contraseñas que se han usado anteriormente.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="24be3ee92f62c3c9274ca8059075f436" id="tgt121" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="cb088e2350f69256ddc4b220fcc7e1ea" id="tgt122" class="tgtSentence">Windows RT y Windows RT 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ff096d14c13e95dfc9db9eb98f194114" id="tgt123" class="tgtSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt124" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="1283133a135a2d1ac9674573da9ac862" id="tgt125" class="tgtSentence">Android 4.0 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="087d8a92155ec5c222b72ea90edf1e76" id="tgt126" class="tgtSentence">Samsung KNOX Standard 4.0 y posterior</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="b04fc1579e478786582f4aa79a8051a6" id="tgt127" class="tgtSentence">Impedir la reutilización de contraseñas anteriores</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="959076d2b0beff36ddd17662b927b4f9" id="tgt128" class="tgtSentence">Si la opción <ui>Recordar el historial de contraseñas</ui> está seleccionada, especifique el número de contraseñas usadas previamente que no se pueden volver a usar.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="24be3ee92f62c3c9274ca8059075f436" id="tgt129" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="cb088e2350f69256ddc4b220fcc7e1ea" id="tgt130" class="tgtSentence">Windows RT y Windows RT 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="ff096d14c13e95dfc9db9eb98f194114" id="tgt131" class="tgtSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt132" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="1283133a135a2d1ac9674573da9ac862" id="tgt133" class="tgtSentence">Android 4.0 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="087d8a92155ec5c222b72ea90edf1e76" id="tgt134" class="tgtSentence">Samsung KNOX Standard 4.0 y posterior</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="6ee61936fa4604c18cfc32efd91b93d5" id="tgt135" class="tgtSentence">Requerir cifrado en dispositivo móvil</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="8db954d0a96d6319c96b08c12cd39cce" id="tgt136" class="tgtSentence">Requiere el cifrado del dispositivo para conectarse a los recursos.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="d6e606d78ee7290f8c9c8c093bf19849" id="tgt137" class="tgtSentence">Los dispositivos que ejecutan Windows Phone 8 se cifran automáticamente.</caps:sentence>
                          </para>
                          <alert class="important">
                            <para>
                              <caps:sentence sentenceid="593d61b09e7e1b077215e9ecefe1fe8c" id="tgt138" class="tgtSentence">Los dispositivos que ejecutan iOS se cifran al configurar la opción de <ui>requerir una contraseña para desbloquear dispositivos móviles</ui>.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="24be3ee92f62c3c9274ca8059075f436" id="tgt139" class="tgtSentence">Windows Phone 8 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="1283133a135a2d1ac9674573da9ac862" id="tgt140" class="tgtSentence">Android 4.0 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="087d8a92155ec5c222b72ea90edf1e76" id="tgt141" class="tgtSentence">Samsung KNOX Standard 4.0 y posterior</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="028a5f5027ee315322f89c3ae610c2f2" id="tgt142" class="tgtSentence">El dispositivo no debe estar liberado ni modificado</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="078de6b90efd8d9dc7660ae1fcf6bfb4" id="tgt143" class="tgtSentence">Si está habilitada, los dispositivos liberados (iOS) o modificados (Android) no serán compatibles.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt144" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="1283133a135a2d1ac9674573da9ac862" id="tgt145" class="tgtSentence">Android 4.0 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="087d8a92155ec5c222b72ea90edf1e76" id="tgt146" class="tgtSentence">Samsung KNOX Standard 4.0 y posterior</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="c6955bf03941fd87282d71af61a364f2" id="tgt147" class="tgtSentence">La cuenta de correo electrónico debe administrarse mediante Intune</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="c5170217d344cbd44886bc58653bf4de" id="tgt148" class="tgtSentence">Cuando esta opción está seleccionada, si el usuario ha establecido una cuenta de correo electrónico en el dispositivo que coincida con un perfil de correo electrónico de Intune implementando por un administrador de TI, el dispositivo no será conforme.</caps:sentence>
                            <caps:sentence sentenceid="6d8228f11263d75c68b6a03382279f69" id="tgt149" class="tgtSentence"> Intune no puede sobrescribir el perfil implementado por el usuario y, por tanto, no puede administrarlo.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="a12d068d7a5455ef619a0fb97824b1bf" id="tgt150" class="tgtSentence">Para garantizar el cumplimiento, el usuario debe quitar la configuración de correo electrónico existente para que Intune pueda instalar el perfil de correo electrónico administrado.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence sentenceid="2dce93f0888ba70b7e4b71adede96ab0" id="tgt151" class="tgtSentence">Para obtener información detallada acerca de los perfiles de correo electrónico, consulte <link xlink:href="10f0cd61-e514-4e44-b13e-aeb85a8e53ae">Enable access to corporate email using email profiles with Microsoft Intune</link>.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt152" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence sentenceid="55ff7235d2432dd2b966bd33febcafed" id="tgt153" class="tgtSentence">Seleccione el perfil de correo electrónico que debe administrarse mediante Intune</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence sentenceid="959076d2b0beff36ddd17662b927b4f9" id="tgt154" class="tgtSentence">Si se selecciona la opción <ui>	La cuenta de correo electrónico debe administrarse mediante Intune</ui>, haga clic en <ui>Seleccionar</ui> para elegir el perfil de correo electrónico de Intune que debe administrar los dispositivos.</caps:sentence>
                            <caps:sentence sentenceid="01f1ea0f63177e43a078f73661a65ce3" id="tgt155" class="tgtSentence"> El perfil de correo electrónico debe estar presente en el dispositivo.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="e670b2abd6b7dbdf7df09e8f64976b92" id="tgt156" class="tgtSentence">iOS 6 y versiones posteriores</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <para>
                    <caps:sentence sentenceid="c1454fe66f5afe94cdbf0411aa7cc69e" id="tgt157" class="tgtSentence">
                      <superscript>1</superscript> En los dispositivos que ejecutan Windows y están protegidos con una cuenta de Microsoft, la directiva de cumplimiento no podrá evaluarse correctamente si la <ui>longitud mínima de la contraseña</ui> es superior a 8 caracteres o el <ui>número mínimo de conjuntos de caracteres</ui> es superior a 2.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a78c5e1839c51a5b9d531eea3fef1638" id="tgt158" class="tgtSentence">Cuando haya terminado haga clic en <ui>Guardar directiva</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="0560d77ae1afc05831810e18e2bd5719" id="tgt159" class="tgtSentence">La nueva directiva se muestra en el nodo <ui>Directivas de cumplimiento</ui> del área de trabajo <ui>Directiva</ui>.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="ec9994a8f2a66c3ff3c6651802077a75" id="tgt160" class="tgtSentence">Implementar una directiva de cumplimiento</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="46f6d9793010da6afba1cda90f7128c7" id="tgt161" class="tgtSentence">Implemente la directiva de cumplimiento en uno o más grupos de usuarios o dispositivos de su organización.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ad5c1bcb5291ef46b20f2e8f623f5ca4" id="tgt162" class="tgtSentence">Para obtener más información sobre cómo implementar directivas, consulte <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9addc66bf33c7093c867b84ef565b9e4" id="tgt163" class="tgtSentence">Use el resumen de estado y las alertas del área de trabajo <ui>Directiva</ui> de la página <ui>General</ui> para identificar los problemas de la directiva que requieren su atención.</caps:sentence>
            <caps:sentence sentenceid="f38e8d4a29f6e64f69b2faa73bb44771" id="tgt164" class="tgtSentence"> Además, aparece un resumen de estado en el área de trabajo <ui>Panel</ui>.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="1046f1da0da94de7bb5567b93886759b" id="tgt165" class="tgtSentence">Supervisar la directiva de cumplimiento</caps:sentence>
        </title>
        <content>
          <procedure expanded="true">
            <title>
              <caps:sentence sentenceid="e62c58186140bc1a955688a9f0fe27ae" id="tgt166" class="tgtSentence">Para ver los dispositivos que no cumplen una directiva de cumplimiento</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt167" class="tgtSentence">En la <externalLink target="_blank"><linkText>consola de administración de Microsoft Intune</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, haga clic en <ui>Grupos</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt168" class="tgtSentence">Abra la pestaña <ui>Directiva</ui> de cualquier dispositivo compatible con directivas de cumplimiento.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1d78457e80b3c77f152c8c399312bb34" id="tgt169" class="tgtSentence">En la lista desplegable <ui>Filtros</ui>, seleccione <ui>No cumple la directiva de cumplimiento</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="9107d250649ee1408c17ac7a773d9667" id="tgt170" class="tgtSentence">Cómo se resuelven los conflictos de directivas de Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="0a88d841cff6fec15f6ea043c99a4d49" id="tgt171" class="tgtSentence">Cuando se producen conflictos debido a la aplicación de múltiples configuraciones de Intune en un dispositivo, se aplican las siguientes reglas:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="64d5b524fdca07789a9e4b19d6db96c1" id="tgt172" class="tgtSentence">Si las configuraciones en conflicto son una directiva de configuración de Intune y una directiva de cumplimiento, la configuración de la directiva de cumplimiento tiene prioridad sobre la de la directiva de configuración, incluso en el caso de que los valores de la directiva de configuración sean más seguros.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3aefc22614e3dcb53a19587c05d80415" id="tgt173" class="tgtSentence">Si implementó varias directivas de cumplimiento, se usará la más segura.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <nextSteps>
        <content>
          <para>
            <caps:sentence sentenceid="639c0311b28872352fd569815fc9e22e" id="tgt174" class="tgtSentence">Ahora puede usar la directiva de cumplimiento con las directivas de acceso condicional para controlar el acceso a los servicios de su organización.</caps:sentence>
          </para>
        </content>
      </nextSteps>
      <relatedTopics>
        <link xlink:href="c564d292-b83b-440d-bf08-3f5b299b7a5e">Manage access to email and SharePoint with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerWalkthroughDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">
            <ui>Compliance policies</ui> define the rules and settings that a device must comply with in order to be considered compliant by conditional access polices.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You can also use compliance policies to monitor and remediate compliant issues with devices independently of conditional access.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">These rules include:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">PIN and passwords</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Encryption</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Whether the device is jailbroken or rooted</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Whether email on the device is managed by an <token>wit_nextref</token> policy</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src8" class="srcSentence">You deploy compliance policies to users and devices.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> When a compliance policy is deployed to a user, then all of the users devices are checked for compliance.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src10" class="srcSentence">The following table lists the device types supported by compliance policies and how noncompliant settings are managed when the policy is used with a conditional access policy.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Device type</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">PIN or password configuration</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Device encryption</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Jailbroken or rooted device</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">Email profile</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Windows 8.1 and later</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">Remediated</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">N/A</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">N/A</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">N/A</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">Windows Phone 8.1 and later</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">Remediated</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">Remediated</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">N/A</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">N/A</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">iOS 6.0 and later</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">Remediated</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">Remediated (by setting PIN)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src29" class="srcSentence">Quarantined (not a setting)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src30" class="srcSentence">Quarantined</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src31" class="srcSentence">Android 4.0 and later</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src32" class="srcSentence">Quarantined</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src33" class="srcSentence">Quarantined</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src34" class="srcSentence">Quarantined (not a setting)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src35" class="srcSentence">N/A</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src36" class="srcSentence">Samsung KNOX Standard 4.0 and later</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src37" class="srcSentence">Quarantined</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src38" class="srcSentence">Quarantined</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src39" class="srcSentence">Quarantined (not a setting)</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src40" class="srcSentence">N/A</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src41" class="srcSentence">
            <ui>Remediated</ui> = Compliance is enforced by the device operating system (for example, the user is forced to set a PIN).</caps:sentence>
          <caps:sentence id="src42" class="srcSentence">  There is never a case when the setting will be noncompliant.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src43" class="srcSentence">
            <ui>Quarantined</ui> = The device operating system does not enforce compliance (for example, Android devices do not force the user to encrypt the device).</caps:sentence>
          <caps:sentence id="src44" class="srcSentence">  In this case:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src45" class="srcSentence">The device will be blocked if the user is targeted by a conditional access policy.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src46" class="srcSentence">The company portal or web portal will notify the user about any compliance issues.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <section address="BKMK_Compliance">
        <title>
          <caps:sentence id="src47" class="srcSentence">Step 1: Create a compliance policy</caps:sentence>
        </title>
        <content>
          <procedure expanded="false">
            <title></title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Policy</ui> &gt; <ui>Compliance Policies</ui> &gt; <ui>Add</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">On the <ui>Create Policy</ui> page, configure the settings you require:</caps:sentence>
                  </para>
                  <table>
                    <thead>
                      <tr>
                        <TD>
                          <para>
                            <caps:sentence id="src50" class="srcSentence">Setting name</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src51" class="srcSentence">More information</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src52" class="srcSentence">Supported platforms</caps:sentence>
                          </para>
                        </TD>
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src53" class="srcSentence">Name</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src54" class="srcSentence">Enter a unique name for the compliance policy.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src55" class="srcSentence">All</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src56" class="srcSentence">Description</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src57" class="srcSentence">Provide a description that gives an overview of the compliance policy.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src58" class="srcSentence">All</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src59" class="srcSentence">Require a password to unlock mobile devices</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src60" class="srcSentence">Require users to enter a password before they can access their device.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src61" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src62" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src63" class="srcSentence">Android 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src64" class="srcSentence">Samsung KNOX Standard 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src65" class="srcSentence">Allow simple passwords</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src66" class="srcSentence">Let users create simple passwords such as ‘<userInput>1234</userInput>’ or ‘<ui>1111</ui>’.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src67" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src68" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src69" class="srcSentence">Minimum password length</caps:sentence>
                            </ui>
                            <superscript>
                              <caps:sentence id="src70" class="srcSentence">1</caps:sentence>
                            </superscript>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src71" class="srcSentence">Specifies the minimum number of digits or characters that the user’s password must contain.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src72" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src73" class="srcSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src74" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src75" class="srcSentence">Android 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src76" class="srcSentence">Samsung KNOX Standard 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src77" class="srcSentence">Required password type</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src78" class="srcSentence">Specifies whether users must create an <ui>Alphanumeric</ui>, or a <ui>Numeric</ui> password.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src79" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src80" class="srcSentence">Windows RT and Windows RT 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src81" class="srcSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src82" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src83" class="srcSentence">Minimum number of character sets</caps:sentence>
                            </ui>
                            <superscript>
                              <caps:sentence id="src84" class="srcSentence">1</caps:sentence>
                            </superscript>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src85" class="srcSentence">If <ui>Required password type</ui> is set to <ui>Alphanumeric</ui>, this setting specifies the minimum number of character sets that the password must contain.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src86" class="srcSentence">The four character sets are:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src87" class="srcSentence">Lowercase letters</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src88" class="srcSentence">Uppercase letters</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src89" class="srcSentence">Symbols</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src90" class="srcSentence">Numbers</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                          <para>
                            <caps:sentence id="src91" class="srcSentence">Setting a higher number for this setting will require users to create more complex passwords.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src92" class="srcSentence">For iOS devices, this setting refers to the number of special characters (for example, <userInput>!</userInput>, <userInput>#</userInput>, <userInput>&amp;</userInput>) that must be included in the password.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src93" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src94" class="srcSentence">Windows RT and Windows RT 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src95" class="srcSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src96" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src97" class="srcSentence">Password quality</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src98" class="srcSentence">Configures password requirements for Android devices.</caps:sentence>
                            <caps:sentence id="src99" class="srcSentence"> Choose from:</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src100" class="srcSentence">Low security biometric</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src101" class="srcSentence">Required</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src102" class="srcSentence">At least numeric</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src103" class="srcSentence">At least alphabetic</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src104" class="srcSentence">At least alphanumeric</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <ui>
                                  <caps:sentence id="src105" class="srcSentence">Alphanumeric with symbols</caps:sentence>
                                </ui>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src106" class="srcSentence">Android 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src107" class="srcSentence">Samsung KNOX Standard 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src108" class="srcSentence">Minutes of inactivity before password is required</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src109" class="srcSentence">Specifies the idle time before the user must re-enter their password.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src110" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src111" class="srcSentence">Password expiration (days)</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src112" class="srcSentence">Select the number of days before the user’s password expires and they must create a new one.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src113" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src114" class="srcSentence">Windows RT and Windows RT 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src115" class="srcSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src116" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src117" class="srcSentence">Android 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src118" class="srcSentence">Samsung KNOX Standard 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src119" class="srcSentence">Remember password history</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src120" class="srcSentence">Use this setting in conjunction with <ui>Prevent reuse of previous passwords</ui> to restrict the user from creating previously used passwords.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src121" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src122" class="srcSentence">Windows RT and Windows RT 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src123" class="srcSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src124" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src125" class="srcSentence">Android 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src126" class="srcSentence">Samsung KNOX Standard 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src127" class="srcSentence">Prevent reuse of previous passwords</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src128" class="srcSentence">If <ui>Remember password history</ui> is selected, specify the number of previously used passwords that cannot be re-used.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src129" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src130" class="srcSentence">Windows RT and Windows RT 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src131" class="srcSentence">Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src132" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src133" class="srcSentence">Android 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src134" class="srcSentence">Samsung KNOX Standard 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src135" class="srcSentence">Require encryption on mobile device</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src136" class="srcSentence">Requires the device to be encrypted in order to connect to resources.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src137" class="srcSentence">Devices that run Windows Phone 8 are automatically encrypted.</caps:sentence>
                          </para>
                          <alert class="important">
                            <para>
                              <caps:sentence id="src138" class="srcSentence">Devices that run iOS are encrypted when you configure the setting <ui>Require a password to unlock mobile devices</ui>.</caps:sentence>
                            </para>
                          </alert>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src139" class="srcSentence">Windows Phone 8 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src140" class="srcSentence">Android 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src141" class="srcSentence">Samsung KNOX Standard 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src142" class="srcSentence">Device must not be jailbroken or rooted</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src143" class="srcSentence">If enabled, jailbroken (iOS), or rooted (Android) devices will not be compliant.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src144" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src145" class="srcSentence">Android 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src146" class="srcSentence">Samsung KNOX Standard 4.0 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src147" class="srcSentence">Email account must be managed by Intune</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src148" class="srcSentence">When this option is selected, the device will be reported as noncompliant if the user has set up an email account on the device that matches an Intune email profile that was deployed to the device by an IT admin.</caps:sentence>
                            <caps:sentence id="src149" class="srcSentence"> Intune cannot overwrite the user-provisioned profile, and therefore cannot manage it.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src150" class="srcSentence">To ensure compliance, the user must remove the existing email settings, then, Intune can install the managed email profile.</caps:sentence>
                          </para>
                          <para>
                            <caps:sentence id="src151" class="srcSentence">For details about email profiles, see <link xlink:href="10f0cd61-e514-4e44-b13e-aeb85a8e53ae">Enable access to corporate email using email profiles with Microsoft Intune</link>.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src152" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                      <tr>
                        <TD>
                          <para>
                            <ui>
                              <caps:sentence id="src153" class="srcSentence">Select the email profile that must be managed by Intune</caps:sentence>
                            </ui>
                          </para>
                        </TD>
                        <TD>
                          <para>
                            <caps:sentence id="src154" class="srcSentence">If <ui>Email account must be managed by Intune</ui> is selected, click <ui>Select</ui> to choose the Intune email profile that devices must be managed by.</caps:sentence>
                            <caps:sentence id="src155" class="srcSentence"> The email profile must be present on the device.</caps:sentence>
                          </para>
                        </TD>
                        <TD>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src156" class="srcSentence">iOS 6 and later</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </TD>
                      </tr>
                    </tbody>
                  </table>
                  <para>
                    <caps:sentence id="src157" class="srcSentence">
                      <superscript>1</superscript> For devices that run Windows and are secured with a Microsoft Account, the compliance policy will fail to evaluate correctly if <ui>Minimum password length</ui> is greater than 8 characters or if <ui>Minimum number of character sets</ui> is more than 2.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src158" class="srcSentence">When you are finished, click <ui>Save Policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src159" class="srcSentence">The new policy displays in the <ui>Compliance Policies</ui> node of the <ui>Policy</ui> workspace.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src160" class="srcSentence">Deploy a compliance policy</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src161" class="srcSentence">Deploy the compliance policy to one or more groups of users or devices in your organization.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src162" class="srcSentence">For more information about how to deploy policies, see <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src163" class="srcSentence">Use the status summary and alerts on the <ui>Overview</ui> page of the <ui>Policy</ui> workspace to identify issues with the policy that require your attention.</caps:sentence>
            <caps:sentence id="src164" class="srcSentence"> Additionally, a status summary appears in the <ui>Dashboard</ui> workspace.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src165" class="srcSentence">Monitor the compliance policy</caps:sentence>
        </title>
        <content>
          <procedure expanded="true">
            <title>
              <caps:sentence id="src166" class="srcSentence">To view devices that do not conform to a compliance policy</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">In the <externalLink target="_blank"><linkText>Microsoft Intune administration console</linkText><linkUri>https://manage.microsoft.com</linkUri></externalLink>, click <ui>Groups</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src168" class="srcSentence">Open the <ui>Policy</ui> tab for any device that is compatible with compliance policies.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src169" class="srcSentence">From the <ui>Filters</ui> drop-down list, select <ui>Does not conform to compliance policy</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src170" class="srcSentence">How Intune policy conflicts are resolved</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src171" class="srcSentence">When conflicts occur due to multiple Intune settings being applied to a device, the following rules apply:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src172" class="srcSentence">If the conflicting settings are from an Intune configuration policy and a compliance policy, the settings in the compliance policy take precedence over the settings in the configuration policy, even if the settings in the configuration policy are more secure.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src173" class="srcSentence">If you have deployed multiple compliance policies, the most secure of these policies will be used.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <nextSteps>
        <content>
          <para>
            <caps:sentence id="src174" class="srcSentence">You can now use the compliance policy with conditional access policies to control access to services in your organization.</caps:sentence>
          </para>
        </content>
      </nextSteps>
      <relatedTopics>
        <link xlink:href="c564d292-b83b-440d-bf08-3f5b299b7a5e">Manage access to email and SharePoint with Microsoft Intune</link>
      </relatedTopics>
    </developerWalkthroughDocument>
  </caps:SxSSource>
</caps:SxS>