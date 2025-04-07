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
source-git-commit: 3f1065affe2665bb0867de02e4aef4c755c5f201
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 4%

---

# IA en aplicaciones de Experience Cloud

Esta página le ayuda a comprender cómo las aplicaciones de Experience Cloud utilizan IA generativa y dónde encontrar la información específica de la aplicación. Obtenga información acerca de las clases de preguntas, peticiones de datos y modelos de entrada y salida.

## Acerca de la IA generativa y el asistente de IA

La IA generativa es un tipo de inteligencia artificial que puede _crear_ contenido nuevo y _responder_ a sus afirmaciones y preguntas (indicadores):

* **Crear:** Se refiere a la capacidad de la IA para generar contenido nuevo (texto, imágenes, música o vídeos) desde cero, según su formación y las indicaciones de entrada. Esta capacidad es el aspecto _generativo_ de la IA generativa.

* **Responder:** Hace referencia a la inteligencia artificial que proporciona una respuesta o una reacción a una pregunta, instrucción o petición específica, basándose normalmente en sus conocimientos o capacidades de razonamiento.

Ciertas aplicaciones de Experience Cloud aprovechan la IA generativa, lo que ayuda a los nuevos usuarios a adquirir conocimientos del producto con rapidez y a los usuarios experimentados a descubrir perspectivas operativas en segundos en lugar de horas.

### Asistente de IA

[Asistente de IA](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing) es una herramienta conversacional compatible con Experience Platform y aplicaciones relacionadas. Utilícela para acelerar los flujos de trabajo, mejorar los conocimientos del producto, solucionar problemas o buscar en la información. El asistente de IA le permite descubrir perspectivas operativas en segundos, en lugar de horas.

Todas las respuestas del conocimiento del producto son verificables y se citan con vínculos a la documentación del producto en Experience League. [Obtenga información acerca del Asistente de IA](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) y los tipos de indicadores basados en objetivos para aprovechar al máximo el Asistente de IA.

## Aplicaciones de Experience Cloud que utilizan IA

>[!TIP]
>
>Versión de subtítulo (solo un inicio)...


* [GenStudio for Performance Marketing](#gspm)
* [Experience Manager Sites (Cloud Service)](#aem-sites)
* Más por venir...

### GenStudio for Performance Marketing {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/es/docs/genstudio-for-performance-marketing/user-guide/home) es una plataforma generativa controlada por IA. Infunde al ciclo vital de creación de contenido funciones de IA generativas que transforman la forma en que se crea, revisa, comparte y analiza el contenido de marketing.

_GenStudio for Performance Marketing Create_ aprovecha el poder de Adobe GenAI para permitir que los especialistas en marketing y los equipos distribuidos creen experiencias de alto rendimiento y de marca. Generar contenido para:

* Correos electrónicos
* Meta ads
* Anuncios de LinkedIn
* Mostrar anuncios
* Banners

Puede entrenar a GenStudio for Performance Marketing en su marca mediante ejemplos, descripciones de perfiles y productos de clientes y directrices de marca. [Más información.](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)

**Compatibilidad con Adobe Firefly:** planificada

### Experience Manager Sites {#aem-sites}

AEM Sites usa [Generar variaciones](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). Generar variaciones utiliza IA generativa para crear variaciones de contenido basadas en indicadores. Estas indicaciones las proporciona [Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) o [usuarios](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt) las crean y administran.

Después de crear variaciones, puede utilizar el contenido del sitio web y medir su éxito mediante la funcionalidad Experimentación de Edge Delivery Services.

**Entrada:** Los campos de entrada incluyen:

* Número de variaciones que se van a generar
* Audience Source
* Destino de audiencia
* Contexto adicional
* Mensajes dirigidos por el cliente

**Salida:** Contenido Generado/Copia De Mercado. También tiene la opción de generar imágenes en Adobe Express utilizando las capacidades de IA generativa de Firefly.

Consulte [Generar imagen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image).

**Compatibilidad con Adobe Firefly:** Sí

## Adobe Journey Optimizer

Journey Optimizer usa [AI Assistant](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) con dos clases de preguntas:

**Conocimiento del producto**: consulta los almacenes de datos de Adobe (como la documentación del producto de Experience League) para el producto insight. Este resultado no depende del cliente. Por ejemplo:

* ¿Cuántas actividades en directo puedo tener en una zona protegida de Adobe Journey Optimizer?

**Operational Insights (Beta)**: consulta un almacén de datos de Operational Insights específico del cliente que contiene datos operativos centralizados sobre Recorridos, particionados por la zona protegida del cliente. Extrae metadatos solo de objetos empresariales y no tiene acceso a los datos de la zona protegida.

* ¿Cuántos Recorridos se han creado en los últimos siete días?

La salida de Operational Insights depende de los metadatos extraídos de los objetos comerciales del cliente.

Recorrido es el único objeto disponible para el asistente de IA en Journey Optimizer y los metadatos se extraen de la zona protegida actual.

Consulte [Trabajar con el asistente de IA](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) y [Preparación para el campo](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) para obtener más información.

**Compatibilidad con Adobe Firefly:** No



## Aplicaciones de Experience Cloud que utilizan IA

>[!TIP]
>
>Versión de tabla...


Descubra cómo las aplicaciones de Experience Cloud utilizan IA generativa o AI Assistant y si Adobe Firefly es compatible.

| Aplicación | Uso de la IA generativa | Ejemplos | ¿Adobe Firefly? |
|----------|------------|-----------|----------------|
| GenStudio for Performance Marketing | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/es/docs/genstudio-for-performance-marketing/user-guide/home) es una plataforma generativa controlada por IA. Infunde al ciclo vital de creación de contenido funciones de IA generativas que transforman la forma en que se crea, revisa, comparte y analiza el contenido de marketing.<br>Puede entrenar a GenStudio for Performance Marketing en su marca mediante ejemplos, descripciones de perfiles y productos de clientes y directrices de marca. | _Crear GenStudio for Performance Marketing_ le permite generar contenido para correos electrónicos, meta-anuncios, anuncios de LinkedIn, anuncios para mostrar y banners. <br>**Entradas:** <ul><li>Utilice plantillas para iniciar el proceso de creación de contenido. </li><li>Agregue parámetros como marcas, productos y personas (directrices) y contenido (recursos) para dar forma a la experiencia generada. </li><li>Introduzca mensajes descriptivos que describan el contexto o la experiencia que desea generar. [Más información…](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> | Sí |
| Adobe Experience Manager Sites (Cloud Service) | AEM Sites usa [Generar variaciones](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). <br>Generar variaciones utiliza IA generativa para crear variaciones de contenido basadas en peticiones de datos. Estas indicaciones las proporciona Adobe o las crean y administran los usuarios. | Después de crear variaciones, puede utilizar el contenido del sitio web y medir su éxito mediante la funcionalidad Experimentación de Edge Delivery Services. <br>**Entrada:** Los campos de entrada incluyen el número de variaciones que se van a generar; Audience Source/Audience Target; contexto adicional y mensajes dirigidos por el cliente. <ul><li>[Plantilla de mensajes de Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[Mensaje generado por el usuario](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **Salida:** Contenido Generado/Copia De Mercado. También tiene la opción de generar imágenes en Adobe Express utilizando las capacidades de IA generativa de Firefly. Consulte [Generar imagen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image). | Sí |
| Adobe Journey Optimizer | Journey Optimizer usa [AI Assistant](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) con dos clases de preguntas:<ul><li>**Conocimiento del producto**: consulta los almacenes de datos de Adobe (como la documentación del producto de Experience League) para el producto insight. Este resultado no depende del cliente. </li><li>**Operational Insights (Beta)**: consulta un almacén de datos de Operational Insights específico del cliente que contiene datos operativos centralizados sobre Recorridos, particionados por la zona protegida del cliente. Extrae metadatos solo de objetos empresariales y no tiene acceso a los datos de la zona protegida.</li></ul> | <ul><li>**Entrada de conocimientos del producto:** ¿Cuántas actividades activas puedo tener en una zona protegida de Adobe Journey Optimizer?</li><li>**Salida de conocimiento del producto:** El conocimiento del producto proviene de Experience League (documentación pública). </li><li>**Entrada de perspectivas operativas:** ¿Cuántos Recorridos se han creado en los últimos siete días? </li><li>**Salida de perspectivas operativas:** La salida de perspectivas operativas depende de los metadatos extraídos de los objetos comerciales del cliente. Recorrido es el único objeto disponible en AJO y los metadatos se extraen de la zona protegida actual. </li></ul> Ver [Trabajo con el asistente de IA](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) y [Preparación para el campo](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) | No |
| Journey Optimizer: _Prime_ y _Ultimate_ | [Ayudante de IA para el acelerador de contenido](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) ofrece sugerencias de variación de contenido proactivas para texto e imágenes. Está disponible para canales de correo electrónico, push, web y SMS. Esta nueva funcionalidad proporciona texto basado en peticiones de datos y generación de imágenes. | <ul><li> **Correo electrónico**: genera un correo electrónico completo, solo texto o solo imagen. [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **Notificación push**: genera una notificación push completa, solo texto o solo imagen. [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **SMS**: genera un SMS completo o solo texto. [Más información](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **Página web**: genera imágenes de página web o texto de página web. [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **Contenido**: genere contenido para varias campañas de mensajería. [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **Nota:** La salida del acelerador de contenido en AJO Prime y Ultimate está indemnizada. | Sí |
| Edición B2B de Journey Optimizer | Usa [Asistente de IA](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) con una clase de preguntas: <br> **Conocimiento del producto**: consulta los almacenes de datos de Adobe (como la documentación del producto de Experience League) para el producto insight. Este resultado no depende del cliente. | <ul><li>**Entrada:** ¿Cómo envío un correo electrónico en un recorrido de cuenta?</li><li>**Salida:** El conocimiento del producto proviene de Experience League (documentación pública). [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul> | No |
| Cloud Services administrados de Campaign | [Ayudante de IA para el acelerador de contenido](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) genera automáticamente contenido personalizado, atractivo y efectivo en función del objetivo de marketing, con contenido optimizado para los estilos, diseños, tonos y mucho más descritos de la marca en canales como correo electrónico, SMS y push. | <ul><li> **Correo electrónico**: genera un correo electrónico completo, solo texto o solo imagen. [Más información](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **SMS**: genera solo SMS o texto completos. [Más información…](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **Push**: crea mensajes atractivos y genera contenido. [Más información…](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **Nota:** La salida del acelerador de contenido en Campaign Managed Cloud Services está indemnizada. | Sí |
| Customer Journey Analytics | CJA usa [Asistente de IA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) para ayudarle a descubrir información y conocimientos del producto de Experience League. <br>Por ejemplo, los nuevos usuarios pueden usarlo para aprender conceptos de Customer Journey Analytics e incorporarse a productos y características con los que no esté familiarizado. <br>Los usuarios con experiencia pueden usar el Asistente de IA para presentar casos de uso más avanzados, así como consejos y trucos, y realizar tareas a un ritmo rápido. Comprenda los conceptos, solucione problemas o busque información. [Más información…](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**Entrada de conocimientos del producto:** ¿Cómo se crea una métrica calculada? </li><li> **Salida de conocimiento del producto:** El conocimiento del producto proviene de Experience League (documentación pública). </li></ul> | No |
| Customer Journey Analytics | [Subtítulos inteligentes](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) proporciona información en lenguaje natural para las visualizaciones de líneas en las visualizaciones de Workspace. | <ul><li>**Entrada:** visualizaciones de línea. Los subtítulos se generan automáticamente en función de estas visualizaciones de líneas cuando hace clic en **Subtítulos inteligentes**. </li><li> **Salida:** subtítulos en lenguaje natural generados automáticamente.</li></ul> | No |
| Real-Time CDP | Utiliza [Asistente de IA](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) para ayudarle a descubrir el conocimiento y las perspectivas del producto desde Experience League. Consulta una base de datos y traduce los datos de la base de datos a una respuesta legible en lenguaje natural. Dos clases de preguntas: <br> **Conocimiento del producto**: consulta los almacenes de datos de Adobe (como la documentación del producto de Experience League) para el producto insight. Este resultado no depende del cliente. <br> **Operational Insights (Beta)**: consulta un almacén de datos de perspectivas operacionales específico del cliente que contiene datos operativos centralizados, particionados por la zona protegida de AEP del cliente. Extrae metadatos únicamente de Atributos, Audiencias, Flujos de datos, Conjuntos de datos, Destinos, Esquemas y Fuentes, y no accede a los datos de la zona protegida. <br>Por ejemplo, para una consulta acerca de una audiencia, [!DNL AI Assistant] puede tener acceso al nombre de la audiencia y a otros metadatos asociados, pero no puede tener acceso a los perfiles de esa audiencia. | <ul><li>**Entrada de conocimientos del producto:** ¿Cómo se calcula la riqueza de perfiles? </li><li>**Salida de conocimiento del producto:** El conocimiento del producto proviene de Experience League (documentación pública). </li><li> **Entrada de información operativa:** ¿Cuántos conjuntos de datos tengo? </li><li> **Salida de Operational Insights:** La salida de Operational Insights depende de los metadatos extraídos de los objetos comerciales del cliente (atributos, audiencias, flujos de datos, conjuntos de datos, destinos, esquemas y fuentes), e incluye un vínculo a la página específica de la interfaz de usuario que contiene los datos consultados. </li></ul>Para ver ejemplos, consulte las tablas de entrada _Conocimiento del producto_ y _Perspectivas operativas_ en el [Asistente de IA en Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) | No |
| Marketo | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) crea conversaciones asistidas por IA con preguntas y respuestas personalizadas y aprobadas previamente, así como un resumen de la conversación | <ul><li> **Generar preguntas:** Proporcione las direcciones URL de las cuales se extrae el contenido y se utilizan para generar preguntas/respuestas. </li><li> **Resumen de conversación:** genera un resumen de una conversación de chat. </li></ul> [Más información…](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library) | No |
| Workfront | El [Asistente de IA](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) de Workfront le ayuda a realizar su trabajo al ofrecerle información y sugerencias en la aplicación en una conversación en lenguaje natural. El Asistente de IA ofrece las siguientes funciones: Resume proyectos/tareas/problemas/documentos, proporciona instrucciones o información de referencia extraída de la documentación de Workfront en Experience League, genera o perfecciona fórmulas para campos personalizados calculados. | <ul><li>**Resumir la entrada del proyecto:** Resumir este proyecto </li><li> **Resumir resultados del proyecto:** Devuelve descripciones breves del propósito y el estado del proyecto, proporciona ejemplos de tareas que se han completado y que aún están pendientes, y proporciona algunos detalles y notas adicionales.</li><li> **Generar/Refinar entrada de fórmula:** &quot;Vuelva a escribir esta fórmula para eliminar el error de expresión no válida.&quot; </li><li> **Generar/Refinar salida de fórmula:** Fórmula generada o refinada. </li></ul>**Nota:** El Asistente para IA puede tardar unos momentos en generar la fórmula revisada, según el tamaño y la complejidad de la fórmula. | No |
