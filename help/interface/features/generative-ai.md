---
title: IA en aplicaciones de Experience Cloud
description: Descubra cómo las aplicaciones de Experience Cloud utilizan IA generativa y el asistente de IA.
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
hide: false
hidefromtoc: true
index: n
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 4f51bc948f3d109f8c1211fda44adee17cc05170
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 6%

---

# IA en aplicaciones de Experience Cloud

Esta página le ayuda a comprender la IA generativa y cómo puede utilizarla en aplicaciones de Experience Cloud. Descubra qué funciones del producto utilizan IA generativa, AI Assistant y si Adobe Firefly es compatible.

## Acerca de la IA generativa y el asistente de IA

La IA generativa es un tipo de inteligencia artificial que hace más que simplemente responder preguntas. _Crea_ contenido y _responde_ a tus _preguntas_ (preguntas e instrucciones).

* **Crear:** Se refiere a la capacidad de la IA para generar contenido nuevo (texto, imágenes, música o vídeos) desde cero, según su formación y las indicaciones de entrada. Esta capacidad es el aspecto _generativo_ de la IA generativa.

* **Responder:** Hace referencia a la inteligencia artificial que proporciona una respuesta o una reacción a una pregunta, instrucción o petición específica, basándose normalmente en sus conocimientos o capacidades de razonamiento.

Ciertas aplicaciones de Experience Cloud aprovechan la IA generativa, lo que ayuda a los nuevos usuarios a adquirir conocimientos del producto con rapidez y a los usuarios experimentados a descubrir perspectivas operativas en segundos en lugar de horas.

### Asistente de IA

[Asistente de IA](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing) es una herramienta conversacional compatible con Experience Platform y aplicaciones relacionadas. Utilícela para acelerar los flujos de trabajo, mejorar los conocimientos del producto, solucionar problemas o buscar en la información. El asistente de IA le permite descubrir perspectivas operativas en segundos, en lugar de horas.

Todas las respuestas del conocimiento del producto son verificables y se citan con vínculos a la documentación del producto en Experience League. [Obtenga información acerca del Asistente de IA](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) y los tipos de indicadores basados en objetivos para aprovechar al máximo el Asistente de IA.

## Aplicaciones de Experience Cloud que utilizan IA

* [Adobe GenStudio for Performance Marketing](#gspm)
* [Adobe Experience Manager Sites (Cloud Service)](#aem-sites)
* [Adobe Journey Optimizer](#journey-optimizer)
* [ADOBE JOURNEY OPTIMIZER PRIME y ULTIMATE](#ajo-prime-ultimate)
* [Edición B2B de Journey Optimizer](#ajo-b2b)

### GenStudio for Performance Marketing {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/es/docs/genstudio-for-performance-marketing/user-guide/home) es una plataforma generativa impulsada por IA que le permite crear, entregar y optimizar recursos de campaña. Sus capacidades generativas de IA transforman la forma en que se crea, revisa, comparte y analiza el contenido de marketing.

La función _GenStudio for Performance Marketing Create_ (o simplemente _Create_) permite a los especialistas en marketing y a los equipos distribuidos crear experiencias de alto rendimiento y sin marca. Puede generar contenido para:

* Correos electrónicos
* Meta ads
* Anuncios de LinkedIn
* Mostrar anuncios
* Banners

También puede entrenar a GenStudio for Performance Marketing en su marca mediante ejemplos, descripciones de perfiles y productos de clientes y directrices de marca. [Más información…](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)

**Compatibilidad con Adobe Firefly:** planificada

### Experience Manager Sites {#aem-sites}

AEM Sites usa [Generar variaciones](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). Generar variaciones utiliza IA generativa para crear variaciones de contenido basadas en indicadores. Estas indicaciones las proporciona [Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) o [usuarios](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt) las crean y administran.

Después de crear variaciones, puede utilizar el contenido del sitio web y medir su éxito mediante la función Experimentación en Edge Delivery Services.

**Entrada:** Los campos de entrada incluyen:

* Número de variaciones que se van a generar
* Audience Source
* Destino de audiencia
* Contexto adicional
* Mensajes dirigidos por el cliente

**Salida:** Contenido Generado/Copia De Mercado. También tiene la opción de generar imágenes en Adobe Express utilizando las capacidades de IA generativa de Firefly.

Consulte [Generar imagen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image).

**Compatibilidad con Adobe Firefly:** Sí

## Journey Optimizer {#journey-optimizer}

Journey Optimizer usa [AI Assistant](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) con dos clases de preguntas:

**Conocimiento del producto**: consulta los almacenes de datos de Adobe (como la documentación del producto de Experience League) para el producto insight. Este resultado no depende del cliente. Por ejemplo:

* ¿Cuántas actividades en directo puedo tener en una zona protegida de Adobe Journey Optimizer?

**Operational Insights (Beta)**: consulta un almacén de datos de Operational Insights específico del cliente que contiene datos operativos centralizados sobre Recorridos, particionados por la zona protegida del cliente. Extrae metadatos solo de objetos empresariales y no tiene acceso a los datos de la zona protegida.

* ¿Cuántos Recorridos se han creado en los últimos siete días?

La salida de Operational Insights depende de los metadatos extraídos de los objetos comerciales del cliente.

Recorrido es el único objeto disponible para el asistente de IA en Journey Optimizer y los metadatos se extraen de la zona protegida actual.

Consulte [Trabajar con el asistente de IA](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) y [Preparación para el campo](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) para obtener más información.

**Compatibilidad con Adobe Firefly:** No

## JOURNEY OPTIMIZER PRIME y ULTIMATE {#ajo-prime-ultimate}

Journey Optimizer Prime y Ultimate usan el [Asistente de IA para el acelerador de contenido](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) para ofrecer sugerencias de variación de contenido proactivas para texto e imágenes.

Esta función está disponible para canales de correo electrónico, push, web y SMS. Proporciona texto basado en mensajes y generación de imágenes.

**Correo electrónico**: genera un correo electrónico completo, solo texto o solo imagen. [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email)

**Notificación push**: genera una notificación push completa, solo texto o solo imagen. [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push)

**SMS**: genera un SMS completo o solo texto. [Más información](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms)

**Página web**: genera imágenes de página web o texto de página web. [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web)

**Contenido**: genere contenido para varias campañas de mensajería. [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)

**Nota:** La salida del acelerador de contenido en AJO Prime y Ultimate está indemnizada.

**Compatibilidad con Adobe Firefly:** Sí

## Edición B2B de Journey Optimizer {#ajo-b2b}

Utiliza [Ayudante de IA](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) para las solicitudes de información del producto.

**Conocimiento del producto**: consulta los almacenes de datos de Adobe (como la documentación del producto de Experience League) para el producto insight. Este resultado no depende del cliente. | <ul><li>**Entrada:** ¿Cómo envío un correo electrónico en un recorrido de cuenta?</li><li>**Salida:** El conocimiento del producto proviene de Experience League (documentación pública). [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul>   | No   |

<!-- ## Experience Cloud applications that use AI

Learn how Experience Cloud applications use generative AI or AI Assistant, and whether Adobe Firefly is supported. 

| Application | How Generative AI Is Used | Examples | Adobe Firefly? |
|----------|------------|-----------|----------------|
| GenStudio for Performance Marketing | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) is a generative AI-driven platform. It infuses the content creation lifecycle with generative AI capabilities that transform how marketing content is created, reviewed, shared, and analyzed.<br>You can train GenStudio for Performance Marketing on your brand using examples, descriptions of customer personas and products, and brand guidelines. |_GenStudio for Performance Marketing Create_ lets you generate content for emails, Meta ads, LinkedIn ads, display ads, and banners. <br>**Inputs:** <ul><li>Use templates to start the content creation process. </li><li>Add parameters like Brands, Products, and Personas (guidelines) and Content (assets) to shape the generated experience. </li><li>Enter descriptive prompts that describe the context or experience you intend to generate. [Learn more...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> |Yes |
|Adobe Experience Manager Sites (Cloud Service)  | AEM Sites uses [Generate Variations](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). <br>Generate Variations uses generative AI to create content variations based on prompts. These prompts are either provided by Adobe or created and managed by users. |After creating variations, you can use the content on your website and measure its success using the Experimentation functionality of Edge Delivery Services. <br>**Input:** Input fields include Number of Variations to generate; Audience Source / Audience Target; Additional Context, and customer-driven prompts. <ul><li>[Adobe prompt template](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[User generated prompt](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **Output:** Generated Content / Market Copy. You also have the option to generate images in Adobe Express using the generative AI capabilities of Firefly. See [Generate Image](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image). | Yes|
| Adobe Journey Optimizer |Journey Optimizer uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) with two classes of questions:<ul><li>**Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. </li><li>**Operational Insights (Beta)** - queries a customer-specific operational insights data store that contains centralized operational data about Journeys, partitioned by the customer's sandbox. Pulls metadata only from business objects and does not access data within the sandbox.</li></ul>|<ul><li>**Product Knowledge Input:** How many live activities can I have in one Adobe Journey Optimizer sandbox?</li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li>**Operational Insights Input:** How many Journeys have been created in the last seven days? </li><li>**Operational Insights Output:** Operational Insights output depends on metadata pulled from customer's business objects. Journeys is the only object available in AJO, and metadata is pulled from the current sandbox. </li></ul> See [Work with the AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) and [Field Readiness](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) | No |
| Journey Optimizer: _Prime_ and _Ultimate_  | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) brings proactive content variation suggestions for text and images. It is available for email, push, web and SMS channels. This new capability provides prompt-based text and image generation. |<ul><li> **Email** - generate a full email, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **Push Notification** - Generate a full push notification, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **SMS** - Generate a full SMS, or text only. [Learn more](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **Webpage** - Generate web page images or web page text. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **Content** - Generate content for various messaging campaigns. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **Note:** Output from Content Accelerator in AJO Prime and Ultimate is indemnified. | Yes   |
| Journey Optimizer B2B Edition  | Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) with one class of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. | <ul><li>**Input:** How do I send an email in an account journey?</li><li>**Output:** Product Knowledge pulls from Experience League (public documentation). [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul>   | No   |
| Campaign Managed Cloud Services | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) auto-generates personalized, engaging, and effective content based on the marketing objective with content optimized for brand outlined styles, layouts, tone, and more across channels like Email, SMS, Push. |<ul><li> **Email** - Generate a full email, text only or image only. [Learn more](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **SMS** - Generate full SMS or text only. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **Push** - Craft compelling messaging and generate content. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **Note:** Output from Content Accelerator in Campaign Managed Cloud Services is indemnified. | Yes  |
| Customer Journey Analytics   | CJA uses [AI Assistant](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) to help you discover product knowledge and insights from Experience League. <br>For example, new users can use it to learn Customer Journey Analytics concepts and onboard yourself to products and features that you are unfamiliar with. <br>Experienced users can use AI Assistant to present more advanced use cases or tips and tricks and perform tasks at a fast pace. Understand concepts, troubleshoot problems, or search for information. [Learn more...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**Product Knowledge Input:** How do I build a calculated metric? </li><li> **Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li></ul> | No |
| Customer Journey Analytics    | [Intelligent Captions](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) provides natural-language insights for line visualizations in Workspace visualizations.| <ul><li>**Input:** Line visualizations. Captions are auto-generated based on such line visualizations when you click **Intelligent captions**. </li><li> **Output:** Auto-generated natural-language captions.</li></ul>  | No             |
| Real-Time CDP |Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) to help you discover product knowledge and insights from Experience League. It queries a database and translates data from the database into a human-readable answer. Two classes of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. <br> **Operational Insights (Beta)** - Queries a customer-specific operational insights data store that contains centralized operational data, partitioned by the customer's AEP sandbox. Pulls metadata only from Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources, and does not access data within the sandbox. <br>For example, for a query about an audience [!DNL AI Assistant] can access the name of the audience and other associated metadata but cannot access the profiles within that audience. | <ul><li>**Product Knowledge Input:** How is profile richness calculated? </li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li> **Operational Insights Input:** How many datasets do I have? </li><li> **Operational Insights Output:** Operational Insights output depends on metadata pulled from Customer's business objects (Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources), and includes a link to specific UI page containing queried data. </li></ul>For examples, see the _Product Knowledge_ and _Operational Insights_ input tables in [AI Assistant in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)  | No |
| Marketo  | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) creates AI-assisted conversations with customized and pre-approved questions and answers, as well as conversation summary |<ul><li> **Generate Questions:** Provide URLs from which content is extracted and used to generate questions / responses. </li><li> **Conversation Summary:** Generates a summary of a chat conversation. </li></ul> [Learn more...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library)  | No |
| Workfront | [AI Assistant](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) in Workfront helps you accomplish your work by offering in-app information and suggestions in a natural-language conversation. AI Assistant offers the following functionality: Summarizes projects/tasks/issues/documents, provides instructions or reference information pulled from the Workfront documentation on Experience League, generates or refines formulas for calculated custom fields.  | <ul><li>**Summarize Project Input:** Summarize this project </li><li> **Summarize Project Output:** Returns brief descriptions of the project's purpose and status, gives examples of tasks that are completed and that are still pending, and provides some additional details and notes.</li><li> **Generate/Refine Formula Input:** "Rewrite this formula to remove the invalid expression error." </li><li> **Generate/Refine Formula Output:** Generated or refined formula. </li></ul>**Note:** AI Assistant may take a few moments to generate the revised formula, depending on the size and complexity of the formula. | No  | -->
