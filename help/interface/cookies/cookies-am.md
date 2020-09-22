---
description: Audience Manager depende de una serie de cookies simples para realizar diferentes funciones. Estas incluyen la asignación de ID, el registro de llamadas de datos, el seguimiento de errores y la prueba para ver si se pueden configurar cookies. Esta sección incluye y describe las distintas cookies configuradas por Audience Manager.
keywords: cookies
seo-description: Audience Manager depende de una serie de cookies simples para realizar diferentes funciones. Estas incluyen la asignación de ID, el registro de llamadas de datos, el seguimiento de errores y la prueba para ver si se pueden configurar cookies. Esta sección incluye y describe las distintas cookies configuradas por Audience Manager.
seo-title: Cookies de Audience Manager
solution: Experience Cloud, Audience Manager
title: Cookies de Audience Manager
uuid: 8b384c38-b85a-4e93-b00e-41a9d3ae2b21
translation-type: tm+mt
source-git-commit: 11ce83401a12c25853cd6412413b8abf98dd6612
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 100%

---


# Cookies de Audience Manager {#audience-manager-cookies}

Audience Manager depende de una serie de cookies simples para realizar diferentes funciones. Estas incluyen la asignación de ID, el registro de llamadas de datos, el seguimiento de errores y la prueba para ver si se pueden configurar cookies. Esta sección incluye y describe las distintas cookies configuradas por Audience Manager.

**Cookie demdex**

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
   <td colname="col2"> <p>La cookie <span class="wintitle">demdex</span> contiene un identificador único universal (UUID) como se muestra en el siguiente ejemplo: </p> <p> <span class="codeph"> 06151304227769720433039235178204449977 </span> </p> <p>Consulte también <a href="https://docs.adobe.com/content/help/es-ES/audience-manager/user-guide/reference/ids-in-aam.html" format="https" scope="external">Índice de ID en Audience Manager </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Otros atributos</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_11291DA87C5045E880034E06C863BCDA"> 
      <li id="li_40C30A06A12449A4A8748621223CA71B">Tiempo de vida: la cookie <span class="wintitle">demdex</span> tiene un intervalo de duración (TTL) de 180 días. El TTL se restablece a 180 días tras cada interacción del usuario con un sitio web del socio. La cookie expira si un usuario no regresa a su sitio dentro del intervalo TTL. </li> 
      <li id="li_A589EDA2198249829207A183872EF1FF">Exclusión: <span class="keyword">Audience Manager</span> restablece la cookie con una cadena <span class="codeph">Do Not Adobe Target</span> si un usuario se excluye de la recopilación de datos. En esto caso, el TTL de la cookie se establece en 10 años. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Cookie dextp**

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
     </ul> </p> <p>Consulte también la sección de sintaxis de datos dextp a continuación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Otros atributos</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4922AC2CD55D4C888A6FBEB22F8B889B"> 
      <li id="li_91A68C44E53840379C2ACDED25468735">Duración: la cookie <span class="wintitle">dextp</span> tiene un intervalo de duración (TTL) de 180 días. </li> 
      <li id="li_6B8C674EFAAC4DABA0A640CF29247F99">Exclusión: <span class="keyword">Audience Manager</span> restablece la cookie con una cadena <span class="codeph">Do Not Adobe Target</span> si un usuario se excluye de la recopilación de datos. En esto caso, el TTL de la cookie se establece en 10 años. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Sintaxis de datos de la cookie dextp:

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
   <td colname="col1"> <p> <b>Primero o segundo</b> </p> </td> 
   <td colname="col2"> <p>La posición del nombre o ID del proveedor de datos varía en función de si la cookie utiliza el formato de estilo nuevo o antiguo. </p> <p> <b>Formato de estilo antiguo:</b> </p> <p> 
     <ul id="ul_5BFBF40E3FE849CA859030F2D070FDF6"> 
      <li id="li_E8F4DC0CB15B472ABE9892B3A61D7F77">Sintaxis: <span class="codeph"><span class="varname"> nombre del proveedor de datos </span> - <span class="varname"> Marca de tiempo UNIX UTC </span> </span> </li> 
      <li id="li_7CD8B101156140F49EA97B18E9591402">Ejemplo: <span class="codeph">dataProvider1 – 1490307822038 </span> </li> 
     </ul> </p> <p>La cookie de estilo antigua identifica al proveedor de datos con un nombre legible. </p> <p> <b>Nuevo formato de estilo:</b> </p> <p> 
     <ul id="ul_AC6225CA781746148C125F21DFED1ED9"> 
      <li id="li_29C4B52E398B4EA28944980A15B05A57">Sintaxis: <span class="codeph"><span class="varname"> ID del proveedor de datos </span> - 1 2 - <span class="varname"> Marca de tiempo UNIX UTC </span> </span> </li> 
      <li id="li_3BF30CA5FED242DF96E0B54AFC64B06F">Ejemplo: <span class="codeph"> 123345 - 1 - 1490307822038 </span> </li> 
     </ul> </p> <p>Nueva cookie de estilo: </p> <p> 
     <ul id="ul_F05A91A455FA44C7A71186C0C9E31630"> 
      <li id="li_A8C9638173684359BABC4207845A4F48">Reemplaza el nombre legible del proveedor de datos por un ID numérico. </li> 
      <li id="li_28F1E2DB24904E53BE9718AD788CE61E">Identifica el tipo de llamada con ID 1 o ID 2. El ID 1 representa una llamada de sincronización de ID. El ID 2 representa una llamada obsoleta que ya no se utiliza. No debería ver varias cookies dextp (o ninguna) con el ID 2. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Última posición</b> </p> </td> 
   <td colname="col2"> <p>La última posición contiene una marca de tiempo UNIX UTC. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Cookie dst**

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
   <td colname="col2"> <p> <span class="keyword"> Audience Manager</span> establece esta cookie cuando hay un error en el envío de datos al <a href="https://docs.adobe.com/content/help/es-ES/audience-manager/user-guide/features/destinations/destinations.html#purposes" format="https" scope="external">destino </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Contenido</b> </p> </td> 
   <td colname="col2"> <p> La cookie <span class="wintitle">dst</span> contiene conjuntos de ID de destino y una marca de tiempo UNIX como cadenas separadas por una barra vertical. En los ejemplos, <i>la cursiva</i> representa un marcador de posición variable. </p> <p> 
     <ul id="ul_CE98076A02DA413486C1D341E9806889"> 
      <li id="li_850209D956644749B98C7A208C825C15">Sintaxis: <span class="codeph"> <span class="varname"> ID de destino </span> - <span class="varname"> Marca de tiempo UNIX UTC </span> </span> </li> 
      <li id="li_4A22152C70844733982230EBF7B9EB78">Ejemplo: <span class="codeph">067797-1490349684|1010788-1490349692|1067797-1490349692 </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Otros atributos</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_5D13DD701B484B51BF2808A69A919106"> 
      <li id="li_4E665114C63246FBA32A4E19984D2693">Tiempo de vida: la cookie <span class="wintitle">dst</span> tiene un intervalo de duración (TTL) de 180 días. </li> 
      <li id="li_A682B566704F43D2AB72487EFF212474">Exclusión: <span class="keyword">Audience Manager</span> restablece la cookie con una cadena <span class="codeph">Do Not Adobe Target</span> si un usuario se excluye de la recopilación de datos. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Cookie _dp**

Esta es una cookie temporal. [!DNL Audience Manager] intenta establecer la cookie [!DNL _dp] para determinar si puede establecer otras cookies en el dominio demdex.net en un contexto de terceros. Cuando se ha establecido [!DNL _dp], este tiene un valor de 1. [!DNL Audience Manager] lee este valor y elimina de manera inmediata la cookie. Si la cookie [!DNL _dp] no está presente, [!DNL Audience Manager] sabe que no puede establecer cookies.