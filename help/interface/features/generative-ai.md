---
title: IA generativa en aplicaciones de Experience Cloud
description: Obtenga información sobre la IA generativa (GenAI) y cómo las aplicaciones de Experience Cloud utilizan GenAI y [!UICONTROL AI Assistant].
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 52cf2d91dbbde503869f5f6e2fc8d5f1eb8fae15
workflow-type: tm+mt
source-wordcount: '1784'
ht-degree: 3%

---

# IA generativa en productos de Experience Cloud

La IA generativa (genAI) de Experience Cloud le ayuda a automatizar tareas creativas y cognitivas y a mejorar la productividad. En esta página se describe dónde admiten las aplicaciones de Experience Cloud las funciones genAI y AI Assistant, y se proporcionan vínculos para obtener más información sobre estas funciones.

**¿Qué es genAI?**

La IA generativa es un tipo de IA que puede crear contenido original. Por ejemplo, puede crear texto, imágenes, vídeo, audio o código de software en respuesta a la petición o el requerimiento de un usuario.

* **Crear:** La capacidad para generar contenido (texto, imágenes, música o vídeos) desde cero, en función de su formación y de las indicaciones de entrada. Esta capacidad es el aspecto _generativo_ de la IA generativa.

* **Generar una respuesta:** AI proporciona una respuesta o una reacción a una solicitud, basándose normalmente en los datos disponibles y en los repositorios de conocimientos.

**¿Qué es el [!UICONTROL Asistente de IA]?**

[!UICONTROL Asistente de IA] es una herramienta conversacional compatible con Experience Platform y aplicaciones relacionadas. Utilícelo para obtener rápidamente _conocimiento del producto_ y _información operativa_ en los productos compatibles.

* **Conocimiento del producto:** El conocimiento del producto hace referencia a conceptos y temas basados en la documentación de Experience League. Aprenda a crear [indicadores eficaces basados en objetivos](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home) para sacar el máximo partido a [!UICONTROL AI Assistant]. Todas las respuestas de Experience League son verificables y se citan con vínculos.

* **Perspectivas operativas:** [Perspectivas operativas](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/questions#objects-questions) se refieren a respuestas generadas sobre objetos de metadatos (atributos, audiencias, flujos de datos, conjuntos de datos, etc.). Con [!UICONTROL Asistente de IA], puede lograr en segundos lo que de otra manera podría tomar horas o días.

El Asistente para IA también incluye características de IA del agente de conversación (conocidas como _IA auténtica_) en las aplicaciones compatibles:

* **Soporte técnico del producto:** El [Agente de soporte técnico](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/new-features/customer-support) es una capacidad de depuración y solución de problemas de autoservicio del [!UICONTROL Asistente de IA] que puede usar para las características y aplicaciones de Experience Platform. Solucione los problemas de soporte sin salir de sus flujos de trabajo, cree vales de soporte al cliente y rastree el progreso de los casos con el Asistente de IA.

[Más información sobre el Asistente de IA](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/landing)

## Disponibilidad de GenAI en productos de Experience Cloud {#products}

Las siguientes aplicaciones de Experience Cloud admiten IA generativa o [!UICONTROL Asistente de IA]. La compatibilidad con Adobe Firefly también se indica por producto.

Actualizado: **6 de junio de 2025**

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager]](#aem)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign] Managed Cloud Services](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing] es una aplicación de IA generativa diseñada para ayudar a los equipos de marketing empresarial a crear, activar y optimizar el contenido de las campañas de marca en canales como medios de pago, correo electrónico y anuncios en pantalla.

Los especialistas en marketing de rendimiento pueden utilizar indicaciones en lenguaje natural para generar recursos personalizados y compatibles con la marca. GenStudio for Performance Marketing acelera la ejecución de campañas, escala la producción de contenido sin poner en riesgo la integridad de la marca y proporciona análisis de rendimiento para mejorar el retorno de la inversión general.

[Más información](https://experienceleague.adobe.com/es/docs/genstudio-for-performance-marketing/user-guide/home)

Compatibilidad con Adobe Firefly: **Sí**

## [!DNL Experience Manager] {#aem}

En las secciones siguientes se describe brevemente la IA generativa en aplicaciones de AEM.

### Experience Manager Sites

En AEM Sites, puede usar _[!UICONTROL Generar variaciones]_. Esta función utiliza inteligencia artificial generativa para crear variaciones de contenido basadas en los mensajes de entrada. Adobe proporciona los indicadores o usted los crea y administra.

Después de crear variaciones, puede usar el contenido de su sitio web y medir su éxito mediante la característica [Experimentación](https://www.aem.live/docs/experimentation) de Edge Delivery Services. También tiene la opción de generar imágenes en Adobe Express utilizando las capacidades de IA generativa de Firefly.

**Ejemplos de entrada y salida**

Los campos de entrada incluyen:

* Número de variaciones que se van a generar
* Audience Source
* Destino de audiencia
* Contexto adicional
* Mensajes dirigidos por el cliente

La salida es contenido generado o copia de mercado.

Compatibilidad con Adobe Firefly: **Sí**

[Más información](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

### Sites Optimizer {#sites-optimizer}

AEM Sites Optimizer utiliza IA generativa para analizar y mejorar el rendimiento y la eficacia de las experiencias web. Estas perspectivas se agrupan en áreas de oportunidades clave: Participación, Adquisición de tráfico, Postura de seguridad y Estado del sitio. Cada categoría destaca formas específicas de mejorar el sitio, ya sea aumentando la interacción del visitante, mejorando la capacidad de detección, reforzando la seguridad o manteniendo la estabilidad del sitio. [Más información](https://experienceleague.adobe.com/es/docs/experience-manager-sites-optimizer/content/opportunity-types/overview)

### Experience Manager Assets {#aem-assets}

En los AEM Assets, puede usar IA generativa en **Content Hub** y **etiquetas inteligentes generadas por IA**.

Compatibilidad con Adobe Firefly: **Sí**

**Content Hub**

[!UICONTROL Content Hub] está disponible como parte de [!DNL Experience Manager Assets as a Cloud Service] para democratizar el acceso al contenido de la marca para las organizaciones y sus socios comerciales. Se centra en la distribución de recursos para su activación a escala y la creación de variantes de contenido en la marca para mejorar la agilidad del marketing.

En Content Hub, puede crear contenido con Adobe Express (si tiene derechos de Adobe Express). Puede editar el contenido existente con herramientas sencillas, producir variaciones de marca con plantillas y elementos de marca y crear contenido con las capacidades más recientes de GenAI de [!DNL Adobe Firefly]. [Más información](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview)

**Etiquetas inteligentes**

En lugar de depender de la entrada manual, la IA puede asignar automáticamente etiquetas descriptivas a los recursos digitales. Estas etiquetas generadas por IA mejoran la calidad de los metadatos, lo que facilita la búsqueda, la categorización y la recomendación de recursos.

Por ejemplo, si el recurso es una imagen, la IA puede identificar objetos, escenas, emociones o incluso logotipos de marca. Puede generar etiquetas relevantes como _puesta de sol_, _playa_, _vacaciones_ o _sonriendo_. [Más información](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/manage/smart-tags#ai-smart-tags)

## Adobe [!DNL Journey Optimizer] {#journey-optimizer}

En [!DNL Journey Optimizer] (AJO), puede usar [Asistente de IA](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/get-started/ai-assistant) para obtener _conocimiento del producto_ y _información operativa_ (beta).

### Ejemplos del uso del Asistente de IA en AJO

A continuación se muestra un ejemplo de entrada para el conocimiento del producto:

* _¿Cuántas actividades activas puedo tener en una zona protegida de Journey Optimizer?_

  El resultado se genera desde Experience League y otros almacenes de datos de Adobe.

A continuación se muestra un ejemplo de entrada para perspectivas operativas:

* _¿Cuántos Recorridos se han creado en los últimos siete días?_

  Para los resultados, el asistente de IA consulta un almacén de datos específico del cliente. El almacén de datos contiene datos operativos centralizados sobre [!UICONTROL Recorridos]. Esta función no depende del cliente y extrae metadatos solo de objetos empresariales. No accede a los datos de su zona protegida.

[Más información](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/get-started/ai-assistant)

Compatibilidad con Adobe Firefly: **No**

### Asistente de IA para la generación de contenido (AJO Prime y Ultimate) {#ajo-prime}

En AJO _Prime_ y _Ultimate_, puede usar [generación de contenido](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) para generar contenido y así ofrecer sugerencias de variación de contenido proactivas para texto e imágenes.

Esta función está disponible para correo electrónico, notificaciones push, página web, contenido y canales SMS. Proporciona texto basado en mensajes y generación de imágenes. La salida de la generación de contenido en AJO Prime y Ultimate está indemnizada.

[Más información](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Compatibilidad con Adobe Firefly: **Sí**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition usa [!UICONTROL Asistente de IA] para ayudarle con el conocimiento del producto.

Entrada de ejemplo:

* _¿Cómo envío un correo electrónico en un recorrido de cuenta?_

  La salida de conocimientos del producto se extrae de Experience League.

[Más información](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Compatibilidad con Adobe Firefly: **No**

## [!DNL Campaign] Managed Cloud Services {#campaign-cs}

Campaign Managed Cloud Services usa [!UICONTROL Asistente de IA] para la generación de contenido. Esta función le permite generar automáticamente contenido personalizado, atractivo y eficaz en función de su objetivo de marketing, con contenido optimizado para estilos, diseños, tonos y mucho más definidos por la marca. Puede utilizarlo en varios canales, como correo electrónico, SMS y push.

**Nota:** La salida de la generación de contenido en Cloud Services administrados de Campaign está indemnizada.

[Más información](https://experienceleague.adobe.com/es/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Compatibilidad con Adobe Firefly: **Sí**

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analytics permite utilizar la IA generativa o el AI Assistant de las siguientes maneras:

* [Ayudante de IA](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant) para obtener información sobre el producto.
* [Agente de soporte técnico](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/new-features/customer-support) para crear tickets de soporte al cliente, con detalles de contexto y sesión de sus interacciones con el Asistente de IA.
* [Data Insights Agent](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) para obtener respuestas a preguntas sobre tus datos. Crea visualizaciones relevantes en Analysis Workspace utilizando componentes de la vista de datos y utilizando los datos reales.
* [Subtítulos inteligentes](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) para proporcionar información clave sobre las visualizaciones de Workspace que se usan con más frecuencia en lenguaje natural.
* [Content Analytics](https://experienceleague.adobe.com/es/docs/analytics-platform/using/content-analytics/report/report#template) para asignar los metadatos de cada recurso automáticamente.

Compatibilidad con Adobe Firefly: **No**

**Asistente de IA**

Descubra el conocimiento del producto de Experience League. Si es un usuario nuevo, aprenda rápidamente los conceptos de Customer Journey Analytics e incorpore productos y funciones. Por ejemplo:

* _¿Cómo envío un correo electrónico en un recorrido de cuenta?_

Los usuarios con experiencia obtienen casos de uso avanzados o aprenden estrategias para realizar tareas a un ritmo rápido. Puede comprender rápidamente los conceptos, solucionar problemas o buscar información.

[Más información](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

**Subtítulos inteligentes**

Puede usar _Subtítulos inteligentes_ en [!DNL Customer Journey Analytics] para obtener información en lenguaje natural de las visualizaciones de Workspace que se usan con más frecuencia. Los subtítulos inteligentes son ideales para los analistas que necesitan narrativas y contexto para compartirlos con otros usuarios. Los usuarios empresariales pueden utilizarla para descubrir rápidamente los conocimientos básicos de alto nivel.

Por ejemplo:

* **Entrada:** En CJA, ejecute una visualización compatible (que incluye líneas, áreas, gráficos de barras, flujos o visitas en el orden previsto) y, a continuación, haga clic en **[!UICONTROL Subtítulos inteligentes]**.

* **Salida:** vea subtítulos en lenguaje natural generados automáticamente que muestran el contexto y las claves que se obtienen. A continuación, puede realizar acciones en los datos generados, como revisarlos, copiarlos y compartirlos con su organización. [Ver cómo](https://video.tv.adobe.com/v/3420131/?quality=12&learn=on#_blank)

[Más información](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

**Content Analytics**

Content Analytics utiliza IA y GenAI para asignar automáticamente los metadatos de cada recurso, como temas, escenas, colores de primer plano, etc. Un atributo es una etiqueta de metadatos asignada por IA que describe lo que hay en un recurso o experiencia.

Por ejemplo: el primer plano `color: red` es un atributo asignado automáticamente. Las visualizaciones le ayudan a identificar qué atributos de sus recursos contribuyen en mayor medida a la conversión. [Más información](https://experienceleague.adobe.com/es/docs/analytics-platform/using/content-analytics/report/report#template)

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP usa el [!UICONTROL Asistente de IA] para ayudarle con los conocimientos del producto de Experience League. También ofrece perspectivas operativas (en versión beta). [!UICONTROL Asistente de IA] consulta un almacén de datos de perspectivas operacionales específico del cliente que contiene datos operativos centralizados, particionados en su zona protegida de AEP. El sistema extrae metadatos únicamente de Atributos, Audiencias, Flujos de datos, Conjuntos de datos, Destinos, Esquemas y Fuentes, y no accede a los datos de la zona protegida.

Por ejemplo, si realiza una consulta sobre una audiencia, [!UICONTROL AI Assistant] puede acceder al nombre de la audiencia y a otros metadatos asociados, pero no puede acceder a los perfiles de esa audiencia.

[Más información](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home)

Compatibilidad con Adobe Firefly: **No**

## [!DNL Marketo] {#marketo}

En Marketo, la IA generativa está disponible en los seminarios web interactivos y en Dynamic Chat.

**Seminarios Web Interactivos**

Genere automáticamente capítulos y resúmenes para sus seminarios web grabados, lo que los hace más accesibles y fáciles de navegar para su audiencia. Las funciones incluyen:

* Generación automática de capítulos
* Resumen de texto generado por IA
* Contenido editable: modificar capítulos y resúmenes generados
* Fácil integración: añada capítulos y resúmenes a sus páginas de destino copiando el código HTML en el editor de páginas web que elija

[Más información](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai)

**Dynamic Chat**

Las funciones generativas impulsadas por IA de Adobe Dynamic Chat le permiten optimizar la productividad de sus agentes de ventas, obtener información sobre las intenciones de los visitantes de su sitio web y responder a las preguntas de los visitantes de forma segura. Puede aprobar previamente las preguntas, respuestas y el resumen de la conversación. Dynamic Chat incluye una versión gratuita y una versión premium.

[Más información](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Compatibilidad con Adobe Firefly: **No**

## [!DNL Workfront] {#workfront}

[!UICONTROL Ayudante de IA] en [!DNL Workfront] le ayuda a realizar su trabajo al ofrecerle información y sugerencias dentro de la aplicación. Puede hacer lo siguiente:

* Obtenga resúmenes de algunos objetos, lo que le proporciona una vista de alto nivel de la intención o los detalles del objeto.
* Haz preguntas y deja que [!UICONTROL AI Assistant] encuentre respuestas en Experience League.
* Obtenga fórmulas generadas en función de sus peticiones de datos. También puede resolver errores en las expresiones personalizadas no válidas en los campos calculados.
* Busque proyectos, tareas y problemas.

[Más información](https://experienceleague.adobe.com/es/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Compatibilidad con Adobe Firefly: **No**

## Recursos adicionales

* [Recursos de IA responsables en el Centro de confianza](https://www.adobe.com/trust/responsible-ai.html)<!-- * [Customer AI Propensity Scoring Model Card](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/model-cards/ai-model-cards/customer-ai) -->

**Descargo de responsabilidad:** La información de esta página es solo para fines informativos generales. Nuestro objetivo es mantenerla precisa y actualizada, pero las funciones de software y de IA pueden cambiar con frecuencia. No garantizamos la integridad o fiabilidad de la información en todo momento. Compruebe cualquier detalle importante antes de tomar decisiones basadas en este contenido.
