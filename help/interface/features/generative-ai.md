---
title: IA en aplicaciones de Experience Cloud
description: Obtenga información acerca de IA generativa y cómo las aplicaciones de Experience Cloud utilizan genAI y  [!DNL AI Assistant].
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 835bcd684384d1c8809fba062c9e9d8edd4de535
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 3%

---

# IA en productos de Experience Cloud

Esta página le ayuda a conocer qué productos admiten IA generativa, [!DNL AI Assistant], y si Adobe Firefly es compatible. También puede encontrar vínculos a recursos de ayuda específicos del producto sobre cómo utilizar la IA en Experience Cloud.

**Acerca de la IA generativa**

La IA generativa es un tipo de inteligencia artificial que hace más que simplemente responder preguntas. Puede _crear_ contenido y _generar una respuesta_ a sus preguntas o declaraciones (conocidas como _peticiones de datos_).

* **Crear:** Capacidad de IA para generar contenido (texto, imágenes, música o vídeos) desde cero, según su formación y las indicaciones de entrada. Esta capacidad es el aspecto _generativo_ de la IA generativa.

* **Generar una respuesta:** AI proporciona una respuesta o una reacción a un mensaje, basándose normalmente en los datos disponibles y en los repositorios de conocimientos.

Con la IA generativa, puede obtener conocimientos sobre productos rápidamente si es su primera vez en Experience Cloud. Los usuarios experimentados pueden descubrir información operativa en segundos en lugar de horas.

**¿Qué es [!DNL AI Assistant]?**

[!DNL AI Assistant] es una herramienta de conversación compatible con Experience Platform y aplicaciones relacionadas. Estas aplicaciones lo utilizan de manera similar, pero con ventajas específicas del producto. Utilícelo para acelerar sus flujos de trabajo, mejorar sus conocimientos sobre productos, solucionar problemas o buscar información y encontrar perspectivas operativas. En ciertas aplicaciones, [!DNL AI Assistant] le permite descubrir información operativa inmediatamente.

**Conocimiento del producto:** El conocimiento del producto hace referencia a conceptos y temas basados en la documentación de Experience League. Las respuestas de Experience League son verificables y se citan con vínculos. Obtenga información acerca de los tipos de [mensajes basados en objetivos](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) para aprovechar al máximo [!DNL AI Assistant].

**Perspectivas operativas:** Las perspectivas operativas se refieren a respuestas que genera AI Assistant sobre los objetos de metadatos (atributos, audiencias, flujos de datos, conjuntos de datos, destinos, recorridos, esquemas y fuentes), incluidos recuentos, búsquedas y el impacto en el linaje.

[Más información](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

<!-- **Your data remains yours**

In AI Assistant, security is the priority:

* Customer data is not used to train language models.
* AI Assistant looks at only the documents that you tell it to. You are in control.
* Your people can use AI Assistant only on documents they can access.
* It's audit-ready: Responses are attributable to source documents.
* Enterprise controls are in place to manage who has AI access in the company. -->

## Disponibilidad de IA en productos de Experience Cloud

Obtenga información acerca de la compatibilidad con IA generativa o [!DNL AI Assistant] en los productos de Experience Cloud y si Adobe Firefly es compatible.

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager Sites]](#aem-sites)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] Prime y Ultimate](#ajo-prime-ultimate)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [Interfaz de usuario web de [!DNL Campaign] v8](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Customer Journey Analytics]](#cja-captions)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing] es una plataforma impulsada por IA que le permite generar y administrar contenido de marketing que se adhiera a los estándares de su marca y cumpla con las políticas de su empresa. Genere contenido para correos electrónicos, meta anuncios, anuncios de LinkedIn, anuncios de visualización y banners.

También puede entrenar a GenStudio for Performance Marketing en su marca mediante ejemplos, descripciones de perfiles y productos de clientes y directrices de marca.

[Más información](https://experienceleague.adobe.com/es/docs/genstudio-for-performance-marketing/user-guide/home)

Compatibilidad con Adobe Firefly: **Sí**

## [!DNL Experience Manager Sites] {#aem-sites}

En AEM Sites, puede usar [!UICONTROL Generar variaciones] para crear variaciones de contenido basadas en peticiones de datos. Estas indicaciones las proporciona Adobe o usted las crea y gestiona.

Después de crear variaciones, puede utilizar el contenido del sitio web y medir su éxito mediante la función Experimentación en Edge Delivery Services. También tiene la opción de generar imágenes en Adobe Express utilizando las capacidades de IA generativa de Firefly.

[Más información](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

Compatibilidad con Adobe Firefly: **Sí**

## [!DNL Journey Optimizer] {#journey-optimizer}

En [!DNL Journey Optimizer], use [!DNL AI Assistant] para obtener conocimientos del producto y perspectivas operativas. Por ejemplo, pregunte _¿Cuántas actividades en directo puedo tener en una zona protegida de Journey Optimizer?_ Recibirá inmediatamente su respuesta de Experience League y otros almacenes de datos de Adobe.

[!DNL AI Assistant] también ayuda con perspectivas operacionales (beta). Por ejemplo, puede saber rápidamente cuántos Recorridos se han creado en los últimos siete días.

Para obtener información operativa, [!DNL AI Assistant] consulta un almacén de datos específico del cliente. El almacén de datos contiene datos operativos centralizados sobre [!UICONTROL Recorridos]. Esta función no depende del cliente y extrae metadatos solo de objetos empresariales. No accede a los datos de su zona protegida.

[Más información](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant).

Compatibilidad con Adobe Firefly: **No**

## [!DNL Journey Optimizer] Prime y Ultimate {#ajo-prime-ultimate}

[!DNL Journey Optimizer] Prime y Ultimate usan [!DNL AI Assistant] para la generación de contenido a fin de ofrecer sugerencias de variación de contenido proactivas para texto e imágenes.

Esta función está disponible para correo electrónico, notificaciones push, página web, contenido y canales SMS. Proporciona texto basado en mensajes y generación de imágenes. La salida de la generación de contenido en AJO Prime y Ultimate está indemnizada.

[Más información](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Compatibilidad con Adobe Firefly: **Sí**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition usa [!DNL AI Assistant] para ayudarle con el conocimiento del producto.

[Más información](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Compatibilidad con Adobe Firefly: **No**

## IU web de [!DNL Campaign] v8 {#campaign-cs}

Campaign Managed Cloud Services usa [!DNL AI Assistant] para la generación de contenido. Esta función le permite generar automáticamente contenido personalizado, atractivo y eficaz en función de su objetivo de marketing, con contenido optimizado para estilos, diseños, tonos y mucho más definidos por la marca. Puede utilizarlo en varios canales, como correo electrónico, SMS y push.

**Nota:** La salida de la generación de contenido en Cloud Services administrados de Campaign está indemnizada.

[Más información](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Compatibilidad con Adobe Firefly: **Sí**

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analytics usa [!DNL AI Assistant] para ayudarle a descubrir el conocimiento y la información del producto de Experience League. Si es un usuario nuevo, aprenda rápidamente los conceptos de Customer Journey Analytics e incorpore productos y funciones.

Los usuarios con experiencia obtienen casos de uso avanzados o aprenden estrategias para realizar tareas a un ritmo rápido. Comprenda los conceptos, solucione problemas o busque información.

[Más información](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

Compatibilidad con Adobe Firefly: **No**

## [!DNL Customer Journey Analytics] {#cja-captions}

Los subtítulos inteligentes de [!DNL Customer Journey Analytics] proporcionan información en lenguaje natural sobre las visualizaciones de Workspace que se usan con más frecuencia. Los subtítulos inteligentes son ideales para los analistas que necesitan narrativas y contexto para compartirlos con otros usuarios. Los usuarios empresariales pueden utilizarla para descubrir rápidamente los conocimientos básicos de alto nivel.

[Más información](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

Compatibilidad con Adobe Firefly: **No**

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP usa [!DNL AI Assistant] para ayudarle con los conocimientos del producto de Experience League. También ofrece perspectivas operativas (en versión beta). [!DNL AI Assistant] consulta un almacén de datos de perspectivas operacionales específico del cliente que contiene datos operativos centralizados, particionados en su zona protegida de AEP. El sistema extrae metadatos únicamente de Atributos, Audiencias, Flujos de datos, Conjuntos de datos, Destinos, Esquemas y Fuentes, y no accede a los datos de la zona protegida.

Por ejemplo, si realiza una consulta sobre una audiencia, [!DNL AI Assistant] puede tener acceso al nombre de la audiencia y a otros metadatos asociados, pero no puede tener acceso a los perfiles de esa audiencia.

[Más información](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home)

Compatibilidad con Adobe Firefly: **No**

## [!DNL Marketo] {#marketo}

Las funciones generativas impulsadas por IA de Adobe Dynamic Chat le permiten optimizar la productividad de sus agentes de ventas, obtener información sobre las intenciones de los visitantes de su sitio web y responder a las preguntas de los visitantes de forma segura. Puede aprobar previamente las preguntas, respuestas y el resumen de la conversación.

[Más información](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Compatibilidad con Adobe Firefly: **No**

## [!DNL Workfront] {#workfront}

[!DNL AI Assistant] en [!DNL Workfront] le ayuda a realizar su trabajo al ofrecerle información y sugerencias dentro de la aplicación. Puede hacer lo siguiente:

* Obtenga resúmenes de algunos objetos, lo que le proporciona una vista de alto nivel de la intención o los detalles del objeto.
* Haz preguntas y deja que [!DNL AI Assistant] encuentre respuestas en Experience League.
* Obtenga fórmulas generadas en función de sus peticiones de datos. También puede resolver errores en las expresiones personalizadas no válidas en los campos calculados.
* Busque proyectos, tareas y problemas.

[Más información](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Compatibilidad con Adobe Firefly: **No**
