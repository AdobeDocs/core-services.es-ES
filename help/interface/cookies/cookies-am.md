---
description: Audience Manager cuenta con unas cookies sencillas para llevar a cabo diferentes funciones. Entre estas funciones se incluyen la asignación de ID, el registro de llamadas de datos, el error de seguimiento y las comprobaciones para ver si se pueden establecer cookies. En esta sección se enumeran y describen diferentes cookies configuradas por Audience Manager.
keywords: cookies
seo-description: Audience Manager cuenta con unas cookies sencillas para llevar a cabo diferentes funciones. Entre estas funciones se incluyen la asignación de ID, el registro de llamadas de datos, el error de seguimiento y las comprobaciones para ver si se pueden establecer cookies. En esta sección se enumeran y describen diferentes cookies configuradas por Audience Manager.
seo-title: Cookies de Audience Manager
solution: Marketing Cloud, Audience Manager
title: Cookies de Audience Manager
uuid: 8 b 384 c 38-b 85 a -4 e 93-b 00 e -41 a 9 d 3 ae 2 b 21
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 426c1fecf16e1cf83cd28971e4de6fdb66b0e10d

---


# Cookies de Audience Manager{#audience-manager-cookies}

Audience Manager cuenta con unas cookies sencillas para llevar a cabo diferentes funciones. Entre estas funciones se incluyen la asignación de ID, el registro de llamadas de datos, el error de seguimiento y las comprobaciones para ver si se pueden establecer cookies. En esta sección se enumeran y describen diferentes cookies configuradas por Audience Manager.

Contenido:

<ul class="simplelist"> 
 <li> <a href="../cookies-overview/cookies-am.md#section-089407f3e2fe4f489b97164df3cd036c" format="dita" scope="local"> Cookie demdex </a> </li> 
 <li> <a href="../cookies-overview/cookies-am.md#section-a71050d788d54350adc6b3f6ebf32398" format="dita" scope="local"> Cookie dextp </a> </li> 
 <li> <a href="../cookies-overview/cookies-am.md#section-670ae9e671874576b528b46e8a1d24ac" format="dita" scope="local"> Cookie dstjs </a> </li> 
 <li> <a href="../cookies-overview/cookies-am.md#section-0d1fea09c83249dfa944cc028a8ef840" format="dita" scope="local">Cookie _dp</a> </li> 
</ul>

## Cookie demdex {#section-089407f3e2fe4f489b97164df3cd036c}

<table id="table_1CCF7EA2BC9E421F8DEECA5F611E33F6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Atributo </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Finalidad</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager</span> configura esta cookie para asignar un único ID a un visitante del sitio. La cookie <span class="wintitle">demdex</span> ayuda a <span class="keyword">Audience Manager</span> a llevar a cabo diferentes funciones, tales como la identificación del visitante, la sincronización de ID, la segmentación, el modelado, la creación de informes, etc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Contenido</b> </p> </td> 
   <td colname="col2"> <p>La cookie <span class="wintitle">demdex</span> contiene un identificador único universal (UUID) como se muestra en el siguiente ejemplo: </p> <p> <span class="codeph"> 06151304227769720433039235178204449977 </span> </p> <p>Consulte también <a href="https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html" format="https" scope="external">Índice de ID en Audience Manager </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Otros atributos</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_11291DA87C5045E880034E06C863BCDA"> 
      <li id="li_40C30A06A12449A4A8748621223CA71B">Tiempo de vida: la cookie <span class="wintitle">demdex</span> tiene un intervalo de duración (TTL) de 180 días. Este intervalo se restablece 180 días tras cada interacción del usuario con el sitio web del socio. La cookie caduca si el usuario no vuelve a su sitio durante el intervalo de duración. </li> 
      <li id="li_A589EDA2198249829207A183872EF1FF">Exclusión: <span class="keyword">Audience Manager</span> restablece la cookie con una cadena <span class="codeph">Do Not Target</span> si un usuario se excluye de la recopilación de datos. En esto caso, el TTL de la cookie se establece en 10 años. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie dextp {#section-a71050d788d54350adc6b3f6ebf32398}

<table id="table_7343C9C9ADD24D3FA693ECC76E4A4045"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Atributo </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Finalidad</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager</span> establece esta cookie para registrar el último momento en el que realizó una petición de sincronización de datos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Contenido</b> </p> </td> 
   <td colname="col2"> <p>La cookie <span class="wintitle">dextp</span> contiene un nombre de proveedor de datos o ID y una marca de hora UNIX UTC como cadenas delimitadas por una barra vertical. En los ejemplos, <i>la cursiva</i> representa un marcador de posición variable. </p> <p> 
     <ul id="ul_80D0BC3FCF06470991E12712401D784A"> 
      <li id="li_03747A433CEB4756A26CD866E716B89D">Estilo antiguo: <span class="codeph"> <span class="varname"> nombre del proveedor de datos aquí </span>-1490307822097| <span class="varname"> nombre del proveedor de datos aquí </span>-1490307822038 </span> </li> 
      <li id="li_79E7000E82DB4ADA9E9887B017343B2D">Estilo nuevo: <span class="codeph">21-1-1490307821616|544-1-1490307821793|3-1-1490307821852|420-1-1490307822038| </span> </li> 
     </ul> </p> <p>Consulte también la siguiente sección sobre la sintaxis de datos de dextp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Otros atributos</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4922AC2CD55D4C888A6FBEB22F8B889B"> 
      <li id="li_91A68C44E53840379C2ACDED25468735">Duración: la cookie <span class="wintitle">dextp</span> tiene un intervalo de duración (TTL) de 180 días. </li> 
      <li id="li_6B8C674EFAAC4DABA0A640CF29247F99">Exclusión: <span class="keyword">Audience Manager</span> restablece la cookie con una cadena <span class="codeph">Do Not Target</span> si un usuario se excluye de la recopilación de datos. En esto caso, el TTL de la cookie se establece en 10 años. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sintaxis de datos de la cookie dextp**

En la siguiente tabla se enumeran y definen los elementos de una cookie [!DNL dextp] por ubicación en la cadena de datos.

<table id="table_BE00604B97F24F5A94AA4F566063D785"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Posición variable </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Primera o segunda</b> </p> </td> 
   <td colname="col2"> <p>La posición del nombre o ID del proveedor de datos varía dependiendo de si la cookie usa el formato de estilo nuevo o antiguo. </p> <p> <b>Formato de estilo antiguo:</b> </p> <p> 
     <ul id="ul_5BFBF40E3FE849CA859030F2D070FDF6"> 
      <li id="li_E8F4DC0CB15B472ABE9892B3A61D7F77">Sintaxis: <span class="codeph"> <span class="varname"> nombre del proveedor de datos </span> - <span class="varname"> Marca de hora UNIX UTC </span></span> </li> 
      <li id="li_7CD8B101156140F49EA97B18E9591402">Example: <span class="codeph"> dataProvider1 - 1490307822038 </span> </li> 
     </ul> </p> <p>El estilo antiguo de la cookie identifica el proveedor de datos con un nombre legible. </p> <p> <b>Formato de estilo nuevo:</b> </p> <p> 
     <ul id="ul_AC6225CA781746148C125F21DFED1ED9"> 
      <li id="li_29C4B52E398B4EA28944980A15B05A57">Sintaxis: <span class="codeph"> <span class="varname"> ID del proveedor de datos </span> - 1|2 - <span class="varname"> Marca de hora UNIX UTC </span></span> </li> 
      <li id="li_3BF30CA5FED242DF96E0B54AFC64B06F">Ejemplo: <span class="codeph"> 123345 - 1 - 1490307822038 </span> </li> 
     </ul> </p> <p>Estilo nuevo de cookie: </p> <p> 
     <ul id="ul_F05A91A455FA44C7A71186C0C9E31630"> 
      <li id="li_A8C9638173684359BABC4207845A4F48">Reemplaza el nombre legible del proveedor de datos con un ID numérico. </li> 
      <li id="li_28F1E2DB24904E53BE9718AD788CE61E">Identifica el tipo de llamada con ID 1 o ID 2. El ID 1 representa el ID de una de llamada sincronización. El ID 2 representa una llamada obsoleta que ya no se usa. No debería ver varias cookies dextp (o ninguna) con el ID 2.  </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Última</b> </p> </td> 
   <td colname="col2"> <p>La última posición contiene una marca de hora UNIX UTC. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie dst {#section-670ae9e671874576b528b46e8a1d24ac}

<table id="table_83AE9B6350C6408BAECD9FCF33022B98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Atributo </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Finalidad</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager</span> establece esta cookie cuando hay un error en el envío de datos al <a href="https://marketing.adobe.com/resources/help/en_US/aam/c_destinations.html" format="https" scope="external">destino </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Contenido</b> </p> </td> 
   <td colname="col2"> <p> La cookie <span class="wintitle">dst</span> contiene conjuntos de ID de destino y una marca de tiempo UNIX como cadenas separadas por una barra vertical. En los ejemplos, <i>la cursiva</i> representa un marcador de posición variable. </p> <p> 
     <ul id="ul_CE98076A02DA413486C1D341E9806889"> 
      <li id="li_850209D956644749B98C7A208C825C15">Sintaxis: <span class="codeph"><span class="varname"> ID de destino </span> - <span class="varname"> Marca de hora UNIX UTC </span></span> </li> 
      <li id="li_4A22152C70844733982230EBF7B9EB78">Ejemplo: <span class="codeph">067797-1490349684|1010788-1490349692|1067797-1490349692 </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Otros atributos</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_5D13DD701B484B51BF2808A69A919106"> 
      <li id="li_4E665114C63246FBA32A4E19984D2693">Tiempo de vida: la cookie <span class="wintitle">dst</span> tiene un intervalo de duración (TTL) de 180 días. </li> 
      <li id="li_A682B566704F43D2AB72487EFF212474">Exclusión: <span class="keyword">Audience Manager</span> restablece la cookie con una cadena <span class="codeph">Do Not Target</span> si un usuario se excluye de la recopilación de datos. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie _dp{#section-0d1fea09c83249dfa944cc028a8ef840}

Esta es una cookie temporal. [!DNL Audience Manager] intenta configurar [!DNL _dp] la cookie para determinar si puede establecer otras cookies en el dominio demdex. net en un contexto de terceros. When [!DNL _dp] is set it contains a value of 1. [!DNL Audience Manager] lee este valor y elimina inmediatamente la cookie. If the [!DNL _dp] cookie is not present, [!DNL Audience Manager] knows it cannot set cookies.

>[!MORE_LIKE_THIS]
>
>* [Explicación de las llamadas al dominio Demdex](https://marketing.adobe.com/resources/help/en_US/aam/demdex-calls.html)
>* [Centro de privacidad de Adobe](http://www.adobe.com/privacy.html)
>* [Privacidad y seguridad de datos de Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/c_data_security_and_privacy.html)
>* [Preguntas frecuentes sobre la privacidad y retención de datos de Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/faq_privacy.html)

