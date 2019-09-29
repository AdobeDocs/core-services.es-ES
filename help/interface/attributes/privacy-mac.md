---
description: Consideraciones y prácticas recomendadas con respecto a información de identificación personal (PII) cargada y utilizada en Adobe Experience Cloud.
keywords: atributos del cliente;servicios principales
seo-description: Consideraciones y prácticas recomendadas con respecto a información de identificación personal (PII) cargada y utilizada en Adobe Experience Cloud.
seo-title: 'Consideraciones sobre la privacidad: atributos del cliente'
solution: Experience Cloud
title: 'Consideraciones sobre la privacidad: atributos del cliente'
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# Consideraciones sobre la privacidad: atributos del cliente

Consideraciones y prácticas recomendadas con respecto a información de identificación personal (PII) cargada y utilizada en Adobe Experience Cloud.


<!-- <p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> -->


* Nombre y apellidos
* Dirección doméstica o cualquier otra dirección física
* La dirección de correo electrónico
* Número de teléfono
* Número de la seguridad social
* Otros identificadores que permitan el contacto físico o en línea con un individuo. Varía en función de la ubicación. Compruebe y cumpla con la legislación y regulaciones locales relativas a la privacidad y PII de todas las regiones donde lleve a cabo su actividad).


Adobe proporciona herramientas que permiten a los anunciantes recopilar información sobre el comportamiento de los consumidores que visitan sus sitios o utilizan sus aplicaciones. Adobe también proporciona herramientas para permitir que los anunciantes mejoren esta información con registros de cliente sin conexión o externos que los anunciantes pueden tener en otros sistemas de gestión.

Un motivo común por el cuales los anunciantes hacen esto es para mejorar la información disponible cuando toman decisiones de publicidad y marketing adecuada para el cliente. Adobe Analytics y Target permiten a los anunciantes cargar información de identificación personal (PII), como direcciones de correo electrónico, únicamente una vez que se ha pasado a hash para que sea imposible utilizarla para contactar con el individuo. La información con hash puede seguir utilizándose con propósitos de marketing y análisis. Como recordatorio, Adobe prohíbe a los anunciantes enviar información personal delicada a Adobe, como registros médicos, información de cuentas financieras y datos acerca de menores.

Adobe es consciente de que este tipo de decisiones de marketing y publicidad pueden tener implicaciones de privacidad, por lo que Adobe cuenta con controles de privacidad incorporados que ayudan a los anunciantes a satisfacer las expectativas de sus clientes. Adobe recomienda a sus anunciantes que consideren cuidadosamente qué información es adecuada para su uso en marketing y en qué circunstancias los anunciantes cuentan con permisos para utilizar dicha información.

**Prácticas recomendadas**

Cuando se carga PII en Adobe Analytics o Target, Adobe recomienda que el cliente tenga la PII con hash antes de cargarla en Adobe. La información con hash puede seguir utilizándose con propósitos de marketing y análisis. Como recordatorio, Adobe prohíbe a los anunciantes enviar información personal delicada a Adobe Analytics y Target, como registros médicos, información de cuentas financieras y datos acerca de menores.

Adobe recomienda a sus anunciantes que consideren cuidadosamente qué información es adecuada para su uso en marketing y en qué circunstancias los anunciantes cuentan con permisos para utilizar dicha información.

Como la legislación de privacidad del consumidor está en constante cambio, Adobe recomienda que los anunciantes respeten tres principios comunes:

1. Haga lo que dice (en su política de privacidad).
1. Diga lo que hace (en su política de privacidad).
1. No sorprenda a sus consumidores.

Con estas expectativas en mente, Adobe recomienda que cuando un anunciante asocia las actividades de exploración con PII, el anunciante proporciona avisos o personalización que indica que el cliente ha sido autenticado. Un ejemplo de esto es la inclusión de una bienvenida en el encabezado del sitio web. Adobe además recomienda que los anunciantes describan en su política de privacidad qué tipo de información de navegación asocia con PII y bajo qué circunstancias la información de navegación se asocia con PII. En último lugar, Adobe recomienda encarecidamente que los anunciantes revisen las opciones de renuncia que proporcionan a sus clientes para que comprendan si y cómo pueden utilizar información de perfil no autenticada tras la renuncia.

<!-- <p> <b>Vinay Geol</b> should help craft privacy regarding how all MAC uses privacy/cookies. Privacy implications around each part of the workflow. Moving from CRM to MAC. Can it include PII? What is PII? What isn't PII? </p> 
<p>CRM data is Known Data or Info. Going to combine with activity that occurs when visitor was not authenticated. PII wiki: </p> 
<p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> 
<p>Refactoring of implementation docs as it relates to privacy and cookies. </p> 
<p>Add content to https://marketing.adobe.com/resources/help/en_US/mcloud/t-publish-audience-segment.html, as follows: </p> 
<p> Audiences are not filtered based on the authentication state of a visitor. If a visitor can browse your site in un-authenticated and authenticated states, actions that occur when a visitor is un-authenticated can still cause a visitor to be included in an audience. Please review <link> to understand the full privacy implications of audience sharing. </p> 
<p>That "link" goes to a topic dedicated to PII, with this text: </p> 
<p> - Adobe Analytics allows its advertisers to upload personally identifiable information (PII) such as email addresses. When uploading PII to Adobe Analytics, Adobe recommends that the customer should hash PII prior to uploading it to Adobe. Hashed information can still be used for analysis and for marketing purposes. As a reminder, Adobe prohibits advertisers from sending sensitive personal information to Adobe Analytics, such as medical records, financial account information, and information about minors. </p> 
<p> - Adobe recommends its advertisers carefully consider which information is appropriate to use for marketing purposes and in which circumstances the advertiser has permission to use such information. </p> 
<p> - As consumer privacy law remains in flux, Adobe recommends that advertisers respect three common tenets: 1) Do what you say (in your privacy policy); 2) Say what you do (in your privacy policy); and 3) Don't surprise your consumers. </p> 
<p> - With these expectations in mind, Adobe recommends that when an advertiser associates browsing activities to PII, the advertiser provide notices/personalization indicating that the consumer is authenticated. An example of this is including a 'Hello, Jane' greeting within the header of the website. Adobe also recommends that advertisers describe in its privacy policy what type of browsing information it associates with PII and under what circumstances browsing information is associated with PII. Lastly, Adobe strongly recommends advertisers review the opt out choices they provide their consumers to understand whether and how they can use unauthenticated profile information post opt out. </p> 
<p>Possibly revamp the cookies to include privacy, with best practices: https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/ </p> -->
