---
description: Adobe Experience Cloud usa cookies para almacenar un ID de visitante utilizado en las soluciones de Experience Cloud.
keywords: cookies;privacy
seo-description: Adobe Experience Cloud usa cookies para almacenar un ID de visitante utilizado en las soluciones de Experience Cloud.
seo-title: Cookies de Experience Cloud
solution: Experience Cloud,Analytics,Target
title: Cookies de Experience Cloud
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
translation-type: tm+mt
source-git-commit: 7bd5b20d24d6ed1bcf2ea8cd1555af217013127e
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 100%

---


# Cookies de Experience Cloud {#experience-cloud-cookies}

Adobe Experience Cloud usa cookies para almacenar un ID de visitante utilizado en las soluciones de Experience Cloud.

**Nombre de cookie: s_ecid**

<table id="table_FF4C70D3D4CC425BA65162D5A9504F7D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Información almacenada </p> </td> 
   <td colname="col2"> <p> Contiene una copia del Experience Cloud ID (ECID) o MID. El MID se almacena en un par de clave-valor que sigue esta sintaxis, s_ecid=MCMID|&lt;ECID&gt; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Vencimiento </p> </td> 
   <td colname="col2"> <p>2 años </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Uso </p> </td> 
   <td colname="col2"> <p>El dominio del cliente establece esta cookie después de que el cliente establezca la cookie AMCV. El propósito de esta cookie es permitir el seguimiento continuado del ID en el estado de origen y se utiliza como ID de referencia si la cookie de AMCV ha expirado. Para obtener más detalles, consulte la cookie AMCV aquí. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ubicación </p> </td> 
   <td colname="col2"> <p>Solo clientes CNAME. No aplicable a escenarios de terceros. La cookie se almacena en su dominio, el mismo dominio utilizado por CNAME y su solicitud de imagen de Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Tamaño </p> </td> 
   <td colname="col2"> <p>45 bytes </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> SameSite=Lax </p> </td> 
   <td colname="col2"> <p>Las cookies con esta configuración solo se envían cuando el dominio que aparece en la dirección URL del explorador coincide con el dominio de la cookie. Esta es la nueva opción predeterminada para las cookies en Chrome.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Nombre de la cookie: AMCV_###@AdobeOrg**

El [Servicio de Experience Platform ID](https://docs.adobe.com/content/help/es-ES/id-service/using/home.html) utiliza JavaScript para almacenar un ID de visitante único en una cookie `AMCV_###@AdobeOrg` en el dominio del sitio web actual, donde `###` representa una cadena aleatoria de caracteres, `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg.`

Consulte también la información relativa a las [Cookies y el servicio de ID](https://docs.adobe.com/content/help/es-ES/id-service/using/intro/cookies.html).

<table id="table_1883C0836C1E4AF5A262FBF5000C1B11"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Información almacenada </p> </td> 
   <td colname="col2"> <p> ID de visitante únicos utilizados por las soluciones de Experience Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Vencimiento </p> </td> 
   <td colname="col2"> <p> 2 años </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Uso </p> </td> 
   <td colname="col2"> <p> Esta cookie se usa para identificar a un visitante único </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ubicación </p> </td> 
   <td colname="col2"> <p> Esta cookie se almacena en el dominio del sitio web (no en el dominio de la solicitud de imagen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Tamaño </p> </td> 
   <td colname="col2"> <p> Varía, la mayoría de los clientes pueden esperar que esta cookie tenga una longitud de aproximadamente 200 bytes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>No se ha agregado ningún valor. Chrome se usará de forma predeterminada como Lax. </p> </td> 
   <td colname="col2"> <p> Las cookies con esta configuración solo se envían cuando el dominio que aparece en la dirección URL del explorador coincide con el dominio de la cookie. Esta es la nueva opción predeterminada para las cookies en Chrome. </p> </td> 
  </tr> 
 </tbody> 
</table>
