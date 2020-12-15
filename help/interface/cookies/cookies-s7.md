---
description: Cómo utiliza Adobe Scene7 las cookies para almacenar información útil que puede utilizarse para el envío de medios dinámicos al explorador.
keywords: cookies;privacy
solution: Experience Cloud,Analytics,Target
title: 'Cookies de Scene7 '
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
translation-type: tm+mt
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 95%

---


# Cookies de Scene7 {#scene-cookies}

Scene7 usa cookies para almacenar información útil que se puede usar para la presentar medios dinámicos en el navegador.

Scene7 almacena información localmente para algunos visores basados en Flash AS2 más antiguos.

Para los visores AS2, las cookies:

* Rastrean el estado de la sesión de un usuario, como la página actual y la imagen vista, el nivel de zoom actual, etc.
* Determinan cuánto tiempo ha transcurrido desde la sesión anterior del usuario. El visor utiliza esta información para decidir si desea continuar con una sesión anterior o iniciar una nueva. Esta información también se envía a los servidores de Scene7, pero no se utiliza.

Para el visor de catálogos electrónicos AS2 Flash, las cookies:

* Almacenan el contenido generado por el usuario (especialmente el contenido introducido por el usuario en la función “notas adhesivas” del visor eCatalog). Este contenido se restaura cuando el usuario reanuda una sesión.
* Cuando el usuario inicia un correo electrónico para compartir el catálogo electrónico con otro usuario, el contenido de las notas adhesivas de la segunda viñeta del visor AS2 se copia en nuestros servidores para proporcionárselo al destinatario. Cuando el destinatario inicia la sesión del visor, el contenido de las notas adhesivas se recupera del servidor y se copia en una cookie. Esta función no se utiliza mucho, por lo que no caduca y el contenido antiguo no se elimina. En este momento persiste en los servidores indefinidamente.

Los nuevos visores AS3 no implementan la persistencia de la sesión.

**Nombre de la cookie: VatLogin.jsp**

| Atributo | Descripción |
|---|---|
| Información almacenada | Establece la cookie de sesión. El AuthFilter incrustado en IPS ImageServer (IS, IR y también los archivos SWF/apariencias y contextos de vídeo) utiliza la cookie para la autorización de acceso. Si está presente, permite que las solicitudes HTTP pasen. De lo contrario, devuelve el valor “no autorizado”. |
| Vencimiento | Esta cookie es una cookie de sesión. El vencimiento de la sesión actual está establecido en 45 minutos en el archivo [!DNL web.xml] de IPS de Scene7. |

**Nombre de la cookie: s7js.flyout.InfoMessage.displayed`assetId`.state**

<table id="table_6835D64C5D464A049F576621F2BE3FAD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Atributo </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Información almacenada </td> 
   <td colname="col2"> <p>&lt;assetId&gt; es el nombre del recurso con el que trabaja el visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Vencimiento </td> 
   <td colname="col2"> Esta cookie es una cookie de sesión y caduca cuando se cierra el explorador. </td> 
  </tr> 
 </tbody> 
</table>

**Nombre de la cookie: s7js.flyout.InfoMessage.displayed`assetId`_idx`id`.ant**

Los visores DHTML heredados utilizan las cookies del explorador para almacenar información de estado y datos de notas adhesivas. También los utiliza el menú flotante DHTML multipantalla para hacer que el indicador de mensaje sea específico para cada sesión.

<table id="table_8F6CC83D32D54BEE99884318AD126C98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Atributo </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Información almacenada </td> 
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt; es el nombre del recurso con el que trabaja el visor e &lt;id&gt; es el índice de notas adhesivas basado en 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Vencimiento </td> 
   <td colname="col2"> Esta cookie es una cookie de sesión y caduca cuando se cierra el explorador. </td> 
  </tr> 
 </tbody> 
</table>

