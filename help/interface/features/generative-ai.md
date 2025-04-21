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
source-git-commit: c6285bb87885d020275c6c0b4c003e912026ad20
workflow-type: tm+mt
source-wordcount: '1314'
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
* [Asistente de IA en Journey Optimizer Prime y Ultimate](#ajo-prime-ultimate)
* [Asistente de IA en Journey Optimizer B2B edition](#ajo-b2b)
* [Asistente de IA en Campaign Managed Cloud Services](#campaign-cs)
* [Asistente de IA en Customer Journey Analytics](#cja)
* [Subtítulos inteligentes en Customer Journey Analytics](#cja-captions)
* [Asistente de IA en Real-Time CDP](#rtcdp)
* [Dynamic Chat en Marketo](#marketo)
* [Asistente de IA en Workfront](#workfront)

### GenStudio for Performance Marketing {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/es/docs/genstudio-for-performance-marketing/user-guide/home) no es una característica, sino una plataforma generativa controlada por IA. Sus capacidades generativas de IA transforman la forma en que se crea, revisa, comparte y analiza el contenido de marketing.

En la página de inicio [Crear](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview), puede crear experiencias de alto rendimiento sin marca. Generar contenido para:

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

Los campos de entrada incluyen:

* Número de variaciones que se van a generar
* Audience Source
* Destino de audiencia
* Contexto adicional
* Mensajes dirigidos por el cliente

La salida es contenido generado o copia de mercado.

También tiene la opción de generar imágenes en Adobe Express utilizando las capacidades de IA generativa de Firefly. [Más información…](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image)

**Compatible con Adobe Firefly:** Sí

## Asistente de IA en Journey Optimizer {#journey-optimizer}

En Journey Optimizer, el asistente de IA puede ayudarle a obtener conocimientos del producto y perspectivas operativas.

**Conocimiento del producto:** El Asistente de IA consulta los almacenes de datos de Adobe (como la documentación del producto de Experience League) para el producto insight. El resultado no depende del cliente.

Por ejemplo:

* _¿Cuántas actividades activas puedo tener en una zona protegida de Adobe Journey Optimizer?_

**Operational Insights (Beta)**: el Asistente de IA consulta un almacén de datos de perspectivas operacionales específico del cliente que contiene datos operativos centralizados sobre Recorridos, particionados por la zona protegida del cliente. Esta función extrae metadatos solo de objetos empresariales y no accede a los datos de la zona protegida.

Mensaje de ejemplo:

* _¿Cuántos Recorridos se han creado en los últimos siete días?_

La salida de Operational Insights depende de los metadatos extraídos de los objetos comerciales del cliente. Este resultado no depende del cliente.

_Recorridos_ es el único objeto disponible para el Asistente de IA en Journey Optimizer y los metadatos se extraen de la zona protegida actual. [Más información...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant).

**Compatible con Adobe Firefly:** No

## Asistente de IA en Journey Optimizer Prime y Ultimate {#ajo-prime-ultimate}

Journey Optimizer Prime y Ultimate usan el [Asistente de IA para el acelerador de contenido](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) para ofrecer sugerencias de variación de contenido proactivas para texto e imágenes.

Esta característica está disponible para los canales [correo electrónico](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email), [notificaciones push](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push), [página web](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web), [contenido](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation) y [SMS](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms). Proporciona texto basado en mensajes y generación de imágenes.

**Nota:** La salida del acelerador de contenido en AJO Prime y Ultimate está indemnizada.

**Compatible con Adobe Firefly:** Sí

## Asistente de IA en Journey Optimizer B2B edition {#ajo-b2b}

Journey Optimizer B2B edition usa el [Asistente de IA](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview) para ayudarle con el conocimiento del producto, según las indicaciones del conocimiento del producto.

**Conocimiento del producto**: consulta los almacenes de datos de Adobe (como la documentación del producto de Experience League) para el producto insight. Este resultado no depende del cliente.

* **Entrada:** ¿Cómo envío un correo electrónico en un recorrido de cuenta?

* **Salida:** El conocimiento del producto proviene de Experience League (documentación pública). [Más información…](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/question-guidance)

**Compatible con Adobe Firefly:** No

## Asistente de IA en Campaign Managed Cloud Services {#campaign-cs}

Campaign Managed Cloud Services usa el [Asistente de IA para el acelerador de contenido](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs). Esta función le permite generar automáticamente contenido personalizado, atractivo y eficaz en función de su objetivo de marketing, con contenido optimizado para estilos, diseños, tonos y mucho más definidos por la marca. Puede usarlo en varios canales como [correo electrónico](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content), [SMS](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) y [push](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push).

**Nota:** La salida del acelerador de contenido en Campaign Managed Cloud Services está indemnizada.

**Compatible con Adobe Firefly:** Sí

## Asistente de IA en Customer Journey Analytics {#cja}

Customer Journey Analytics usa [Asistente de IA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant) para ayudarle a descubrir información y conocimientos del producto de Experience League.

**Mensaje de ejemplo:** ¿Cómo se genera una métrica calculada?

Los nuevos usuarios pueden utilizarlo para aprender los conceptos de Customer Journey Analytics e incorporarse a los productos y las funciones con los que no está familiarizado.

Los usuarios con experiencia pueden utilizar el Asistente de IA para presentar casos de uso o sugerencias y trucos más avanzados y realizar tareas a un ritmo rápido. Comprenda los conceptos, solucione problemas o busque información. [Más información…](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge)

**Compatible con Adobe Firefly:** No

## Subtítulos inteligentes en Customer Journey Analytics {#cja-captions}

[Subtítulos inteligentes](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) en Customer Journey Analytics proporcionan información en lenguaje natural sobre las visualizaciones de Workspace más utilizadas.

**Compatible con Adobe Firefly:** No

## Asistente de IA en Real-Time CDP {#rtcdp}

Real-Time CDP usa [Asistente de IA](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) para ayudarle a descubrir información y conocimientos del producto de Experience League. [Recibe sugerencias](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/questions) al hacer preguntas.

También ofrece perspectivas operativas (en versión beta). El asistente de IA consulta un almacén de datos de perspectivas operativas específicas del cliente que contiene datos operativos centralizados, particionados por la zona protegida de AEP del cliente. Extrae metadatos solamente de Atributos, Audiencias, Flujos de datos, Conjuntos de datos, Destinos, Esquemas y Fuentes, y no accede a los datos dentro del espacio aislado.

Por ejemplo, para una consulta sobre una audiencia, [!DNL AI Assistant] puede tener acceso al nombre de la audiencia y a otros metadatos asociados, pero no puede tener acceso a los perfiles de esa audiencia.

Por ejemplo:

* Entrada: _¿Cuántos conjuntos de datos tengo?_

* Respuesta: El resultado de Operational Insights depende de los metadatos extraídos de los objetos comerciales del cliente (atributos, audiencias, flujos de datos, conjuntos de datos, destinos, esquemas y fuentes), e incluye un vínculo a la página específica de la interfaz de usuario que contiene los datos consultados.

Para obtener más ejemplos, consulte las tablas de entrada _Conocimiento del producto_ y _Perspectivas operativas_ en el [Asistente de IA en Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home)

**Compatible con Firefly:** No

## Dynamic Chat en Marketo {#marketo}

Las funciones generativas impulsadas por IA de Adobe Dynamic Chat le permiten optimizar la productividad de sus agentes de ventas, obtener información sobre las intenciones de los visitantes de su sitio web y responder a las preguntas de los visitantes de forma segura. Puede aprobar previamente las preguntas, respuestas y el resumen de la conversación. [Más información…](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

**Compatible con Firefly:** No

## Asistente de IA en Workfront {#workfront}

El asistente de IA de Workfront le ayuda a realizar su trabajo al ofrecerle información y sugerencias dentro de la aplicación. Puede hacer lo siguiente:

* Obtenga resúmenes de algunos objetos, lo que le proporciona una vista de alto nivel de la intención o los detalles del objeto.
* Haz preguntas y deja que [!DNL AI Assistant] encuentre respuestas en Experience League.
* Obtenga fórmulas generadas en función de sus peticiones de datos. También puede resolver errores en las expresiones personalizadas no válidas en los campos calculados.
* Busque proyectos, tareas y problemas.

[Más información…](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

**Compatible con Firefly:** No
