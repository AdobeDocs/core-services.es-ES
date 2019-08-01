---
description: Target usa cookies para ofrecer a los administradores de sitios Web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.
keywords: cookies; privacidad
seo-description: Target usa cookies para ofrecer a los administradores de sitios Web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.
seo-title: Cookies de Target
solution: Marketing Cloud, Analytics, Target, Social
title: Cookies de Target
uuid: 44 f 7 e 32 e -8 d 99-4682-8 b 54-8364 d 001 b 403
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Cookies de Target{#target-cookies}

Target usa cookies para ofrecer a los administradores de sitios Web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.

En caso necesario, puede modificar esta configuración a excepción de la duración de la cookie. Acuda al representante de la cuenta cuando vaya a cambiar la configuración de la cookie.

>[!NOTE]
>
>Los usuarios de Target también pueden crear cookies de terceros personalizadas.

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
   <td colname="col2"> <p> <span class="filepath"> clientcode.tt.omtrdc.net</span>, que usa el código de cliente para la cuenta de Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Duración de la cookie </p> </td> 
   <td colname="col2"> <p>La cookie permanece en el navegador del visitante dos semanas desde la última vez que inició sesión. La duración de la cookie no se puede cambiar. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If any of your domain names include a country code, such as [!DNL mycompany.co.uk], work with your Client Services to configure your [!DNL mbox.js] to support this.

La cookie conserva una serie de valores para administrar la experiencia de los clientes con las campañas de Target:

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
   <td colname="col2"> <p>Identificador exclusivo de una sesión de usuario. De manera predeterminada, tiene una duración de 30 minutos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pc ID</span> </p> </td> 
   <td colname="col2"> <p>Identificador semipermanente del navegador de un visitante. Dura hasta que las cookies se eliminan manualmente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> check</span> </p> </td> 
   <td colname="col2"> <p>Sencillo valor de prueba que sirve para averiguar si un visitante admite cookies. Se establece cada vez que un visitante solicita una página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> disable</span> </p> </td> 
   <td colname="col2"> <p>Se establece si el tiempo de carga de un visitante supera el tiempo de espera fijado en el archivo <span class="filepath">mbox.js</span>. De manera predeterminada, tiene una duración de 1 hora. </p> </td> 
  </tr> 
 </tbody> 
</table>

