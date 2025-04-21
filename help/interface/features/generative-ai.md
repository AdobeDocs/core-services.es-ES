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
source-git-commit: fb9d3c45beca38e1ca372b24565946bf1a1da839
workflow-type: tm+mt
source-wordcount: '1392'
ht-degree: 4%

---

# IA en aplicaciones de Experience Cloud

Esta página le ayuda a comprender la IA generativa y cómo puede utilizarla en aplicaciones de Experience Cloud. Descubra qué funciones del producto utilizan IA generativa, AI Assistant y si Adobe Firefly es compatible.

## Acerca de la IA generativa y el asistente de IA

La IA generativa es un tipo de inteligencia artificial que hace más que simplemente responder preguntas. _Crea_ contenido y _responde_ a tus _preguntas_ (preguntas e instrucciones).

* **Crear:** Se refiere a la capacidad de la IA para generar contenido nuevo (texto, imágenes, música o vídeos) desde cero, según su formación y las indicaciones de entrada. Esta capacidad es el aspecto _generativo_ de la IA generativa.

* **Responder:** Hace referencia a la IA que proporciona una respuesta o una reacción a un mensaje específico, basándose normalmente en sus conocimientos o capacidades de razonamiento.

Si es nuevo en Experience Cloud, puede utilizar IA generativa para obtener conocimientos del producto rápidamente. Como usuario experimentado, puede descubrir perspectivas operativas en segundos en lugar de horas.

### Asistente de IA

[Asistente de IA](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing) es una herramienta conversacional compatible con Experience Platform y aplicaciones relacionadas. Utilícela para acelerar los flujos de trabajo, mejorar los conocimientos del producto, solucionar problemas o buscar en la información. En determinadas aplicaciones, el asistente de IA le permite descubrir perspectivas operativas inmediatamente.

Las respuestas de conocimiento de productos de Experience League son verificables y se citan con vínculos. Obtenga información acerca de los tipos de [mensajes basados en objetivos](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) para aprovechar al máximo el Asistente para IA.

## Aplicaciones con funciones compatibles con IA

* [GenStudio for Performance Marketing](#gspm)
* [Generación de variaciones en AEM Sites (Cloud Service)](#aem-sites)
* [Asistente de IA en Journey Optimizer](#journey-optimizer)
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

**Compatible con Adobe Firefly:** planificado

### Generación de variaciones en Experience Manager Sites {#aem-sites}

[Generar variaciones](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations) en AEM Sites usa IA generativa para crear variaciones de contenido basadas en peticiones de datos. Estas indicaciones las proporciona [Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) o [usuarios](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt) las crean y administran.

Después de crear variaciones, puede utilizar el contenido del sitio web y medir su éxito mediante la función Experimentación en Edge Delivery Services.

### Campos de entrada y salida

**Entrada:** Los campos de entrada incluyen:

* Número de variaciones que se van a generar
* Audience Source
* Destino de audiencia
* Contexto adicional
* Mensajes dirigidos por el cliente

**Salida:** Contenido Generado/Copia De Mercado. También tiene la opción de generar imágenes en Adobe Express utilizando las capacidades de IA generativa de Firefly.

Consulte [Generar imagen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image) para obtener más información.

**Compatible con Adobe Firefly:** Sí

## Asistente de IA en Journey Optimizer {#journey-optimizer}

En Journey Optimizer, el asistente de IA puede ayudarle a obtener conocimientos del producto y perspectivas operativas.

**Conocimiento del producto:** El Asistente de IA consulta los almacenes de datos de Adobe (como la documentación del producto de Experience League) para el producto insight. El resultado no depende del cliente.

Por ejemplo:

* _¿Cuántas actividades activas puedo tener en una zona protegida de Adobe Journey Optimizer?_

**Operational Insights (Beta)**: consulta un almacén de datos de perspectivas operacionales específico del cliente que contiene datos operativos centralizados sobre Recorridos, particionados por la zona protegida del cliente. Esta función extrae metadatos solo de objetos empresariales y no accede a los datos de la zona protegida.

Mensaje de ejemplo:

* _¿Cuántos Recorridos se han creado en los últimos siete días?_

La salida de Operational Insights depende de los metadatos extraídos de los objetos comerciales del cliente. Este resultado no depende del cliente.

_Recorridos_ es el único objeto disponible para el Asistente de IA en Journey Optimizer y los metadatos se extraen de la zona protegida actual. [Más información...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant).

**Compatible con Adobe Firefly:** No

## JOURNEY OPTIMIZER PRIME y ULTIMATE {#ajo-prime-ultimate}

Journey Optimizer Prime y Ultimate usan el [Asistente de IA para el acelerador de contenido](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) para ofrecer sugerencias de variación de contenido proactivas para texto e imágenes.

Esta característica está disponible para los canales [correo electrónico](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email), [notificaciones push](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push), [página web](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web), [contenido](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation) y [SMS](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms). Proporciona texto basado en mensajes y generación de imágenes.

**Nota:** La salida del acelerador de contenido en AJO Prime y Ultimate está indemnizada.

**Compatible con Adobe Firefly:** Sí

## Asistente de IA en Journey Optimizer B2B edition {#ajo-b2b}

Journey Optimizer B2B edition usa el [Asistente de IA](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) para ayudarle con el conocimiento del producto, según las indicaciones del conocimiento del producto.

**Conocimiento del producto**: consulta los almacenes de datos de Adobe (como la documentación del producto de Experience League) para el producto insight. Este resultado no depende del cliente.

* **Entrada:** ¿Cómo envío un correo electrónico en un recorrido de cuenta?

* **Salida:** El conocimiento del producto proviene de Experience League (documentación pública). [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)

**Compatible con Adobe Firefly:** No

## Cloud Services administrados de Campaign

Campaign Managed Cloud Services usa el asistente de [IA para el acelerador de contenido](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) que genera automáticamente contenido personalizado, atractivo y efectivo en función del objetivo de marketing, con contenido optimizado para los estilos, diseños, tonos y mucho más descritos por la marca en canales como correo electrónico, SMS y push.

* **Correo electrónico**: genera un correo electrónico completo, solo texto o solo imagen. [Más información](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content)

* **SMS**: genera solo SMS o texto completos. [Más información…](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms)

* **Push**: crea mensajes atractivos y genera contenido. [Más información…](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push)

**Nota:** La salida del acelerador de contenido en Campaign Managed Cloud Services está indemnizada.

**Compatible con Adobe Firefly:** Sí

## Customer Journey Analytics: asistente de IA

CJA usa [Asistente de IA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) para ayudarle a descubrir información y conocimientos del producto de Experience League.

**Mensaje de ejemplo:** ¿Cómo se genera una métrica calculada?

Los nuevos usuarios pueden utilizarlo para aprender los conceptos de Customer Journey Analytics e incorporarse a los productos y las funciones con los que no está familiarizado.

Los usuarios con experiencia pueden utilizar el Asistente de IA para presentar casos de uso o sugerencias y trucos más avanzados y realizar tareas a un ritmo rápido. Comprenda los conceptos, solucione problemas o busque información. [Más información…](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge)

**Compatible con Adobe Firefly:** No

## Customer Journey Analytics: Subtítulos inteligentes

[Subtítulos inteligentes](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) proporciona información en lenguaje natural para las visualizaciones de líneas en las visualizaciones de Workspace.

**Entrada de ejemplo:** visualizaciones de línea. Los subtítulos se generan automáticamente en función de estas visualizaciones de líneas cuando hace clic en **Subtítulos inteligentes**.

**Salida:** subtítulos en lenguaje natural generados automáticamente.

**Compatible con Adobe Firefly:** No

## Real-Time CDP

Real-Time CDP usa [Asistente de IA](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) para ayudarle a descubrir información y conocimientos del producto de Experience League. Consulta una base de datos y traduce los datos de la base de datos a una respuesta legible en lenguaje natural.

Hay dos clases de preguntas disponibles:

**Conocimiento del producto**: consulta los almacenes de datos de Adobe (como la documentación del producto de Experience League) para el producto insight. Este resultado no depende del cliente.

Por ejemplo:

* _¿Cómo se calcula la riqueza de perfiles?_

**Operational Insights (Beta)**: consulta un almacén de datos de perspectivas operacionales específico del cliente que contiene datos operativos centralizados, particionados por la zona protegida de AEP del cliente. Extrae metadatos únicamente de Atributos, Audiencias, Flujos de datos, Conjuntos de datos, Destinos, Esquemas y Fuentes, y no accede a los datos de la zona protegida.

Por ejemplo, para una consulta sobre una audiencia, [!DNL AI Assistant] puede tener acceso al nombre de la audiencia y a otros metadatos asociados, pero no puede tener acceso a los perfiles de esa audiencia.

Por ejemplo:

* Entrada: _¿Cuántos conjuntos de datos tengo?_

* Respuesta: el resultado de _Operational Insights depende de los metadatos extraídos de los objetos comerciales del cliente (atributos, audiencias, flujos de datos, conjuntos de datos, destinos, esquemas y fuentes) e incluye un vínculo a una página de la interfaz de usuario específica que contiene datos consultados._

Para obtener más ejemplos, consulte las tablas de entrada _Conocimiento del producto_ y _Perspectivas operativas_ en el [Asistente de IA en Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home)

**Compatible con Firefly:** No


## Marketo

[Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) crea conversaciones asistidas por IA con preguntas y respuestas personalizadas y aprobadas previamente, así como un resumen de la conversación |<ul><li> **Generar preguntas:** Proporcione las direcciones URL de las cuales se extrae el contenido y se utilizan para generar preguntas/respuestas. </li><li> **Resumen de conversación:** genera un resumen de una conversación de chat. </li></ul> [Más información...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library)  | No |

## Workfront

El [Asistente de IA](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) de Workfront le ayuda a realizar su trabajo al ofrecerle información y sugerencias en la aplicación en una conversación en lenguaje natural. El Asistente de IA ofrece las siguientes funciones: Resume proyectos/tareas/problemas/documentos, proporciona instrucciones o información de referencia extraída de la documentación de Workfront en Experience League, genera o perfecciona fórmulas para campos personalizados calculados.  | <ul><li>**Resumir la entrada del proyecto:** Resumir este proyecto </li><li> **Resumir resultados del proyecto:** Devuelve descripciones breves del propósito y el estado del proyecto, proporciona ejemplos de tareas que se han completado y que aún están pendientes, y proporciona algunos detalles y notas adicionales.</li><li> **Generar/Refinar entrada de fórmula:** &quot;Vuelva a escribir esta fórmula para eliminar el error de expresión no válida.&quot; </li><li> **Generar/Refinar salida de fórmula:** Fórmula generada o refinada. </li></ul>**Nota:** El Asistente para IA puede tardar unos momentos en generar la fórmula revisada, según el tamaño y la complejidad de la fórmula. | No  |


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
