---
description: Target usa cookies para ofrecer a los administradores de sitios Web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.
keywords: cookies;privacy
seo-description: Target usa cookies para ofrecer a los administradores de sitios Web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.
seo-title: Cookies de Target
solution: Experience Cloud,Analytics,Target,Social
title: Cookies de Target
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
translation-type: tm+mt
source-git-commit: 11ce83401a12c25853cd6412413b8abf98dd6612
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 100%

---


# Cookies de Adobe Target {#target-cookies}

Adobe Target usa cookies para ofrecer a los administradores de sitios Web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.

Puede cambiar esta configuración si es necesario, con la excepción de la duración de la cookie. Póngase en contacto con el representante de la cuenta cuando cambie la configuración de la cookie.

>[!NOTE]
>
>Los usuarios de Adobe Target también pueden crear cookies de terceros personalizadas.

<table id="table_54B402C6E19C4A70B1E27BC9DFF776EB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Configuración </th> 
   <th colname="col2" class="entry"> Información </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nombre de la cookie </p> </td> 
   <td colname="col2"> <p>mbox. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dominio de la cookie </p> </td> 
   <td colname="col2"> <p>Niveles segundo y superior de los dominios desde los que se proporciona el mbox. Dado que se proporciona desde el dominio de la compañía, se trata de una cookie de origen. Ejemplo: <span class="filepath">mycompany.com</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dominio del servidor </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> clientcode.tt.omtrdc.net</span>, que usa el código de cliente para la cuenta de Adobe Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Duración de la cookie </p> </td> 
   <td colname="col2"> <p>La cookie permanece en el explorador del visitante dos años después de su último inicio de sesión. No puede cambiar la duración de la cookie. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Si alguno de los nombres de dominio incorpora un código de país (como [!DNL mycompany.co.uk]), colabore con los servicios de cliente para configurar [!DNL mbox.js] de forma que lo admita.

La cookie conserva una serie de valores para administrar la forma en que los visitantes viven las campañas de Adobe Target:

<table id="table_5245F72A2D5A4322B40ABB10B7DFB338"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Valor </th> 
   <th colname="col2" class="entry"> Definición </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> session ID</span> </p> </td> 
   <td colname="col2"> <p>ID exclusivo para una sesión de usuario. De manera predeterminada, tiene una duración de 30 minutos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pc ID</span> </p> </td> 
   <td colname="col2"> <p>Un ID semipermanente para el explorador de un visitante. Dura hasta que las cookies se eliminan manualmente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> check</span> </p> </td> 
   <td colname="col2"> <p>Un valor de prueba simple utilizado para determinar si un visitante admite cookies. Se establece cada vez que un visitante solicita una página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> disable</span> </p> </td> 
   <td colname="col2"> <p>Se establece si el tiempo de carga de un visitante supera el tiempo de espera fijado en el archivo <span class="filepath">mbox.js</span>. De manera predeterminada, tiene una duración de 1 hora. </p> </td> 
  </tr> 
 </tbody> 
</table>

