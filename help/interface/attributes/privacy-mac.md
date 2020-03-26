---
description: Consideraciones y prácticas recomendadas con respecto a información de identificación personal (PII) cargada y utilizada en Adobe Experience Cloud.
keywords: customer attributes;core services
seo-description: Consideraciones y prácticas recomendadas con respecto a información de identificación personal (PII) cargada y utilizada en Adobe Experience Cloud.
seo-title: 'Consideraciones sobre la privacidad: atributos del cliente'
solution: Experience Cloud
title: 'Consideraciones sobre la privacidad: atributos del cliente'
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Consideraciones sobre la privacidad: atributos del cliente

Consideraciones y prácticas recomendadas con respecto a información de identificación personal (PII) cargada y utilizada en Adobe Experience Cloud.


<!-- <p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> -->


* Nombre y apellidos
* Domicilio u otra dirección física
* Correo electrónico Dirección
* Número de teléfono
* Número de seguridad social
* Otro identificador que permite el contacto físico o en línea de un individuo. (Varía por ubicación. Verifique y cumpla con las leyes y regulaciones locales relacionadas con la privacidad y PII para todos los lugares donde usted hace negocios).


Adobe proporciona herramientas que permiten a los anunciantes recopilar información sobre el comportamiento de los consumidores que visitan sus sitios o utilizan sus aplicaciones. Adobe también proporciona herramientas que permiten a los anunciantes mejorar esta información con registros de clientes externos o sin conexión que el anunciante pueda tener en otros sistemas de administración de la información.

Un motivo común por el cuales los anunciantes hacen esto es para mejorar la información disponible cuando toman decisiones de publicidad y marketing adecuada para el cliente. Adobe Analytics y Destinatario permiten a los anunciantes cargar información de identificación personal (PII), como direcciones de correo electrónico, solo después de haber pasado el hash para que sea imposible utilizarla para ponerse en contacto con el individuo. La información con hash puede seguir utilizándose para análisis y para fines de marketing. Como recordatorio, Adobe prohíbe a los anunciantes enviar información personal confidencial a Adobe, como registros médicos, información de cuentas financieras e información sobre menores.

Adobe es consciente de que estos tipos de decisiones de marketing y publicidad pueden tener implicaciones para la privacidad del consumidor, por lo que Adobe ha incorporado controles de privacidad para ayudar a los anunciantes a satisfacer las expectativas de sus consumidores. Adobe recomienda a sus anunciantes que consideren cuidadosamente qué información es apropiada para usar con fines de marketing y en qué circunstancias el anunciante tiene permiso para utilizar dicha información.

**Prácticas recomendadas**

Al cargar PII en Adobe Analytics o Adobe Destinatario, Adobe recomienda que el cliente introduzca hash en PII antes de cargarlo en Adobe. La información con hash puede seguir utilizándose para análisis y para fines de marketing. Como recordatorio, Adobe prohíbe a los anunciantes enviar información personal confidencial a Adobe Analytics y Adobe Destinatario, como registros médicos, información de cuentas financieras e información sobre menores.

Adobe recomienda a sus anunciantes que consideren cuidadosamente qué información es apropiada para usar con fines de marketing y en qué circunstancias el anunciante tiene permiso para utilizar dicha información.

Dado que la legislación de privacidad del consumidor sigue en constante cambio, Adobe recomienda que los anunciantes respeten tres principios comunes:

1. Haga lo que diga (en su política de privacidad).
1. Diga lo que hace (en su política de privacidad).
1. No sorprenda a sus consumidores.

Teniendo en cuenta estas expectativas, Adobe recomienda que cuando un anunciante asocia actividades de exploración a PII, el anunciante proporcione avisos o personalización que indiquen que el consumidor está autenticado. Un ejemplo de esto es incluir un saludo en el encabezado del sitio web. Adobe también recomienda que los anunciantes describan en su política de privacidad qué tipo de información de navegación asocia con PII y en qué circunstancias la información de navegación está asociada con PII. Por último, Adobe recomienda encarecidamente a los anunciantes que revisen las opciones de exclusión que proporcionan a sus clientes para saber si pueden utilizar la información de perfil no autenticada después de exclusión y cómo pueden hacerlo.

<!-- <p> <b>Vinay Geol</b> should help craft privacy regarding how all MAC uses privacy/cookies. Privacy implications around each part of the workflow. Moving from CRM to MAC. Can it include PII? What is PII? What isn't PII? </p> 
<p>CRM data is Known Data or Info. Going to combine with activity that occurs when visitor was not authenticated. PII wiki: </p> 
<p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> 
<p>Refactoring of implementation docs as it relates to privacy and cookies. </p> 
<p>Add content to t-publish-audience-segment, as follows: </p> 
<p> Audiences are not filtered based on the authentication state of a visitor. If a visitor can browse your site in un-authenticated and authenticated states, actions that occur when a visitor is un-authenticated can still cause a visitor to be included in an audience. Please review <link> to understand the full privacy implications of audience sharing. </p> 
<p>That "link" goes to a topic dedicated to PII, with this text: </p> 
<p> - Adobe Analytics allows its advertisers to upload personally identifiable information (PII) such as email addresses. When uploading PII to Adobe Analytics, Adobe recommends that the customer should hash PII prior to uploading it to Adobe. Hashed information can still be used for analysis and for marketing purposes. As a reminder, Adobe prohibits advertisers from sending sensitive personal information to Adobe Analytics, such as medical records, financial account information, and information about minors. </p> 
<p> - Adobe recommends its advertisers carefully consider which information is appropriate to use for marketing purposes and in which circumstances the advertiser has permission to use such information. </p> 
<p> - As consumer privacy law remains in flux, Adobe recommends that advertisers respect three common tenets: 1) Do what you say (in your privacy policy); 2) Say what you do (in your privacy policy); and 3) Don't surprise your consumers. </p> 
<p> - With these expectations in mind, Adobe recommends that when an advertiser associates browsing activities to PII, the advertiser provide notices/personalization indicating that the consumer is authenticated. An example of this is including a 'Hello, Jane' greeting within the header of the website. Adobe also recommends that advertisers describe in its privacy policy what type of browsing information it associates with PII and under what circumstances browsing information is associated with PII. Lastly, Adobe strongly recommends advertisers review the opt out choices they provide their consumers to understand whether and how they can use unauthenticated profile information post opt out. </p> 
<p>Possibly revamp the cookies to include privacy, with best practices: https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-privacy.html </p> -->
