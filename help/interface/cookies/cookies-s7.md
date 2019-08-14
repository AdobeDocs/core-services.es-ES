---
description: Scene7 usa cookies para almacenar información útil que se puede usar para la presentar medios dinámicos en el navegador.
keywords: cookies; privacidad
seo-description: Scene7 usa cookies para almacenar información útil que se puede usar para la presentar medios dinámicos en el navegador.
seo-title: Cookies de Scene7
solution: Marketing Cloud, Analytics, Target, Social
title: Cookies de Scene7
uuid: f 9 b 9 d 13 a -17 e 5-4139-8 c 84-6 fe 5 d 22 c 4196
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7137e608ddece5bf2a3983b3b18909ba89d607a6

---


# Cookies de Scene7{#scene-cookies}

Scene7 usa cookies para almacenar información útil que se puede usar para la presentar medios dinámicos en el navegador.

Scene7 almacena información localmente para algunos visores basados en AS2 Flash.

Cookies para los visores AS2:

* El estado de seguimiento de la sesión de un usuario, como la página actual y la imagen vista, el nivel de zoom actual, etc.
* Determina cuánto tiempo ha pasado desde la sesión previa del usuario. El visor utiliza esta información para decidir cuándo continuar con una sesión previa o empezar una nueva. Esta información también se envía a los servidores Scene7, pero no se usa.

Cookies para el visor AS2 Flash eCatalog:

* El contenido de almacenamiento generado por el usuario (especialmente el contenido introducido por el usuario en la función “notas adhesivas” del visor eCatalog). Este contenido se restaura cuando el usuario reanuda una sesión.
* Cuando el usuario empieza un correo electrónico para compartir el ecatalog con otro usuario, el contenido de las notas adhesivas de la segunda viñeta del visor AS2 se copia en nuestros servidores para ofrecerlo al destinatario. Cuando el destinatario inicia la sesión del visor, el contenido de las notas adhesivas se recupera de nuestros servidores y se copia en una cookie. El uso de esta función es bajo, así que no caduca y el contenido antiguo no se elimina. Actualmente persiste en los servidores de manera indefinida.

Los nuevos visores AS3 no implementan la persistencia de sesión.

**Nombre de la cookie: VatLogin.jsp**

| Atributo | Descripción |
|---|---|
| Información almacenada | Establece la cookie de sesión. El AuthFilter incrustado en IPS ImageServer (IS, IR y también los archivos SWF/máscaras y los contextos de vídeo) usa la cookie para la autorización de acceso. Si está presente, permite el paso a través de las peticiones HTTP. De lo contrario, devuelve un valor de falta de autorización. |
| Vencimiento | Esta cookie es una cookie de sesión. El vencimiento de la sesión actual está establecido en 45 minutos en el archivo [!DNL web.xml] de IPS de Scene7. |

**Nombre de la cookie: s 7 js. flyout. infomessage. displayed`assetId`. state**

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
   <td colname="col2"> <p>&lt;assetId&gt; es el nombre del activo con el que trabaja el visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Vencimiento </td> 
   <td colname="col2"> Esta es una cookie de sesión y caduca cuando se cierra el navegador. </td> 
  </tr> 
 </tbody> 
</table>

**Nombre de la cookie: s 7 js. flyout. infomessage. displayed`assetId`_ idx`id`. ant**

Los visores DHTML heredados usan las cookies de navegador para almacenar información de estado y datos de notas permanentes. También las usa el menú flotante DHTML multipantalla para hacer que el indicador de mensaje sea específico de sesión.

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
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt; es el nombre del activo con el que trabaja el visor e &lt;id&gt; es el índice de nota permanente basado en 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Vencimiento </td> 
   <td colname="col2"> Esta es una cookie de sesión y caduca cuando se cierra el navegador. </td> 
  </tr> 
 </tbody> 
</table>

