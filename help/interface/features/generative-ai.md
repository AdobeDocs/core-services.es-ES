---
title: IA en aplicaciones de Experience Cloud
description: Obtenga información sobre la IA generativa y cómo las aplicaciones de Experience Cloud utilizan genAI y AI Assistant.
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: a5d595fc8ee9b76ee1bf4a24364674a3af447b2a
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 4%

---

# IA en productos de Experience Cloud

La IA generativa es un tipo de inteligencia artificial que hace más que simplemente responder preguntas. _Crea_ contenido y _responde_ a tus _preguntas_ (preguntas e instrucciones).

* **Crear:** Se refiere a la capacidad de la IA para generar contenido nuevo (texto, imágenes, música o vídeos) desde cero, según su formación y las indicaciones de entrada. Esta capacidad es el aspecto _generativo_ de la IA generativa.

* **Responder:** Hace referencia a la IA que proporciona una respuesta o una reacción a un mensaje específico, basándose normalmente en sus conocimientos o capacidades de razonamiento.

Si es nuevo en Experience Cloud, puede utilizar IA generativa para obtener conocimientos del producto rápidamente. Como usuario experimentado, puede descubrir perspectivas operativas en segundos en lugar de horas.

**Acerca del Asistente de IA**

El asistente de IA es una herramienta conversacional compatible con Experience Platform y aplicaciones relacionadas. Utilícela para acelerar los flujos de trabajo, mejorar los conocimientos del producto, solucionar problemas o buscar en la información. En determinadas aplicaciones, el asistente de IA le permite descubrir perspectivas operativas inmediatamente.

Las respuestas de conocimiento de productos de Experience League son verificables y se citan con vínculos. Obtenga información acerca de los tipos de [mensajes basados en objetivos](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) para aprovechar al máximo el Asistente para IA.

[Más información](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

<!-- **Your data remains yours**

In AI Assistant, security is the priority:

* Customer data is not used to train language models.
* AI Assistant looks at only the documents that you tell it to. You are in control.
* Your people can use AI Assistant only on documents they can access.
* It's audit-ready: Responses are attributable to source documents.
* Enterprise controls are in place to manage who has AI access in the company. -->

## Disponibilidad de IA en productos de Experience Cloud

Obtenga información acerca de la compatibilidad con la IA generativa o el asistente de IA en los productos de Experience Cloud y si Adobe Firefly es compatible.

* [GenStudio for Performance Marketing](#gspm)
* [Generación de variaciones en Experience Manager Sites](#aem-sites)
* [Asistente de IA en Journey Optimizer](#journey-optimizer)
* [Asistente de IA en Journey Optimizer Prime y Ultimate](#ajo-prime-ultimate)
* [Asistente de IA en Journey Optimizer B2B edition](#ajo-b2b)
* [Asistente de IA en la interfaz de usuario web de Campaign v8](#campaign-cs)
* [Asistente de IA en Customer Journey Analytics](#cja)
* [Subtítulos inteligentes en Customer Journey Analytics](#cja-captions)
* [Asistente de IA en Real-Time CDP](#rtcdp)
* [Dynamic Chat en Marketo](#marketo)
* [Asistente de IA en Workfront](#workfront)

## GenStudio for Performance Marketing {#gspm}

GenStudio for Performance Marketing es una plataforma impulsada por IA que le permite generar y administrar contenido de marketing que se adhiera a los estándares de su marca y cumpla con las políticas de su empresa. Genere contenido para correos electrónicos, meta anuncios, anuncios de LinkedIn, anuncios de visualización y banners.

También puede entrenar a GenStudio for Performance Marketing en su marca mediante ejemplos, descripciones de perfiles y productos de clientes y directrices de marca.

[Más información](https://experienceleague.adobe.com/es/docs/genstudio-for-performance-marketing/user-guide/home)

Compatibilidad con Adobe Firefly: **Planificado**

## Generación de variaciones en Experience Manager Sites {#aem-sites}

Generar variaciones en AEM Sites utiliza IA generativa para crear variaciones de contenido basadas en mensajes. Estas indicaciones las proporciona Adobe o usted las crea y gestiona.

Después de crear variaciones, puede utilizar el contenido del sitio web y medir su éxito mediante la función Experimentación en Edge Delivery Services. También tiene la opción de generar imágenes en Adobe Express utilizando las capacidades de IA generativa de Firefly.

[Más información](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations)

Compatibilidad con Adobe Firefly: **Sí**

## Asistente de IA en Journey Optimizer {#journey-optimizer}

En Journey Optimizer, utilice el asistente de IA para obtener conocimientos del producto y perspectivas operativas. Por ejemplo, pregunte _¿Cuántas actividades en directo puedo tener en una zona protegida de Journey Optimizer?_ Recibirá inmediatamente su respuesta de Experience League y otros almacenes de datos de Adobe.

El asistente de IA también ayuda con las perspectivas operativas (beta). Por ejemplo, puede saber rápidamente cuántos Recorridos se han creado en los últimos siete días.

Para obtener información operativa, el asistente de IA consulta un almacén de datos específico del cliente. El almacén de datos contiene datos operativos centralizados sobre [!UICONTROL Recorridos]. Esta función no depende del cliente y extrae metadatos solo de objetos empresariales. No accede a los datos de su zona protegida.

[Más información](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant).

Compatibilidad con Adobe Firefly: **No**

## Asistente de IA en Journey Optimizer Prime y Ultimate {#ajo-prime-ultimate}

Journey Optimizer Prime y Ultimate utilizan el asistente de IA para el acelerador de contenido para ofrecer sugerencias de variación de contenido proactivas para texto e imágenes.

Esta función está disponible para correo electrónico, notificaciones push, página web, contenido y canales SMS. Proporciona texto basado en mensajes y generación de imágenes. La salida del acelerador de contenido en AJO Prime y Ultimate está indemnizada.

[Más información](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Compatibilidad con Adobe Firefly: **Sí**

## Asistente de IA en Journey Optimizer B2B edition {#ajo-b2b}

Journey Optimizer B2B edition utiliza el asistente de IA para ayudarle con el conocimiento del producto.

[Más información](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Compatibilidad con Adobe Firefly: **No**

## Asistente de IA en la IU web de Campaign v8  {#campaign-cs}

Campaign Managed Cloud Services utiliza el asistente de IA para el acelerador de contenido. Esta función le permite generar automáticamente contenido personalizado, atractivo y eficaz en función de su objetivo de marketing, con contenido optimizado para estilos, diseños, tonos y mucho más definidos por la marca. Puede utilizarlo en varios canales, como correo electrónico, SMS y push.

**Nota:** La salida del acelerador de contenido en Campaign Managed Cloud Services está indemnizada.

[Más información](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Compatibilidad con Adobe Firefly: **Sí**

## Asistente de IA en Customer Journey Analytics {#cja}

Customer Journey Analytics utiliza el asistente de IA para ayudarle a descubrir el conocimiento y las perspectivas del producto desde Experience League. Si es un usuario nuevo, aprenda rápidamente los conceptos de Customer Journey Analytics e incorpore productos y funciones.

Los usuarios con experiencia obtienen casos de uso avanzados o aprenden estrategias para realizar tareas a un ritmo rápido. Comprenda los conceptos, solucione problemas o busque información.

[Más información](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

Compatibilidad con Adobe Firefly: **No**

## Subtítulos inteligentes en Customer Journey Analytics {#cja-captions}

Los subtítulos inteligentes en Customer Journey Analytics proporcionan perspectivas en lenguaje natural para las visualizaciones de Workspace más utilizadas. Los subtítulos inteligentes son ideales para los analistas que necesitan narrativas y contexto para compartirlos con otros usuarios. Los usuarios empresariales pueden utilizarla para descubrir rápidamente los conocimientos básicos de alto nivel.

[Más información](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

Compatibilidad con Adobe Firefly: **No**

## Asistente de IA en Real-Time CDP {#rtcdp}

Real-Time CDP utiliza el asistente de IA para ayudarle con los conocimientos del producto de Experience League. También ofrece perspectivas operativas (en versión beta). El asistente de IA consulta un almacén de datos de perspectivas operativas específicas del cliente que contiene datos operativos centralizados, particionados en su zona protegida de AEP. El sistema extrae metadatos únicamente de Atributos, Audiencias, Flujos de datos, Conjuntos de datos, Destinos, Esquemas y Fuentes, y no accede a los datos de la zona protegida.

Por ejemplo, si realiza una consulta sobre una audiencia, [!DNL AI Assistant] puede tener acceso al nombre de la audiencia y a otros metadatos asociados, pero no puede tener acceso a los perfiles de esa audiencia.

[Más información](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home)

Compatibilidad con Adobe Firefly: **No**

## Dynamic Chat en Marketo {#marketo}

Las funciones generativas impulsadas por IA de Adobe Dynamic Chat le permiten optimizar la productividad de sus agentes de ventas, obtener información sobre las intenciones de los visitantes de su sitio web y responder a las preguntas de los visitantes de forma segura. Puede aprobar previamente las preguntas, respuestas y el resumen de la conversación.

[Más información](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Compatibilidad con Adobe Firefly: **No**

## Asistente de IA en Workfront {#workfront}

El asistente de IA de Workfront le ayuda a realizar su trabajo al ofrecerle información y sugerencias dentro de la aplicación. Puede hacer lo siguiente:

* Obtenga resúmenes de algunos objetos, lo que le proporciona una vista de alto nivel de la intención o los detalles del objeto.
* Haz preguntas y deja que [!DNL AI Assistant] encuentre respuestas en Experience League.
* Obtenga fórmulas generadas en función de sus peticiones de datos. También puede resolver errores en las expresiones personalizadas no válidas en los campos calculados.
* Busque proyectos, tareas y problemas.

[Más información](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Compatibilidad con Adobe Firefly: **No**
