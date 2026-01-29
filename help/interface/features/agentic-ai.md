---
title: Inteligencia artificial aplicada a la agencia en aplicaciones Experience Cloud
description: Descubra dónde está disponible la IA auténtica en las aplicaciones de Experience Cloud.
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
source-git-commit: 7eb6c6e463102ca445093c69797619202202b35e
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 3%

---

# Inteligencia artificial aplicada a la agencia en Adobe Experience Cloud

Actualizado: **29 de enero de 2026**

Los agentes de Adobe Experience Platform cuentan con la tecnología [Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/home) para habilitar las capacidades de IA auténtica en las aplicaciones de Experience Cloud.

Estos agentes ayudan a automatizar tareas, ofrecer perspectivas más rápido y optimizar los flujos de trabajo. Como resultado, los equipos pueden trabajar de forma más eficiente y obtener más valor de Experience Cloud.

El acceso a los agentes de IA en Experience Cloud está disponible en:

* [Aplicaciones de Experience Cloud existentes](#existing-apps)
* [Aplicaciones de Experience Cloud con prioridad de IA](#ai-first-apps)

Las secciones siguientes describen estas dos formas de habilitar la IA auténtica en Experience Cloud.

## Aplicaciones de Experience Cloud existentes {#existing-apps}

En las aplicaciones existentes, puede usar lenguaje natural para instruir a los agentes de Adobe Experience Platform a través de la interfaz conversacional de [AI Assistant](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/home). El asistente de IA está disponible en las vistas de pantalla completa y carril derecho.

Los agentes se pueden habilitar en aplicaciones de Experience Cloud existentes para clientes de una de las siguientes categorías:

* Ha adquirido una licencia de Adobe Experience Platform Agents AI Credit
* Se le incluye en una prueba sujeta a uso (se proporcionan créditos de IA limitados)
* Ha realizado transacciones con el SKU de promoción de Agent Orchestrator (licencia de prueba con tiempo limitado)

El uso de agentes de IA para realizar _trabajos de agente_ consume créditos de IA. Obtenga más información acerca de los trabajos del agente y los créditos de IA en _[Trabajos del agente y consumo de crédito de IA](/help/interface/features/ai-credit-consumption.md)_.

Los agentes de IA siguen _sus_ entradas, supervisión y respetan los controles de acceso de nivel de producto. Solo puede realizar trabajos o acceder a datos que esté autorizado a utilizar en la aplicación de Experience Cloud subyacente.

### Agentes de IA en aplicaciones de Experience Cloud existentes {#existing-apps-table}

En la tabla siguiente se enumeran los agentes de Experience Platform disponibles en las aplicaciones de Experience Cloud existentes.

| Nombre del agente | Competencias | Aplicaciones compatibles |
|---|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | Habilite a sus equipos para que creen, administren y optimicen audiencias utilizando indicaciones de lenguaje natural para una mayor facilidad, eficiencia y velocidad de comercialización. | <ul><li>Real-Time CDP (ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (ediciones B2B y B2C)</li></ul> |
| **Agente de Asesor de contenido** | <ul><li>[Descubrimiento de contenido](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/discovery/overview): acelere la creación y mejore la detección con mensajes simplificados en lenguaje natural para buscar y mostrar instantáneamente contenido de Experience Manager en imágenes, vídeos, documentos basados en texto, fragmentos de contenido y formularios.</li><li>[Optimización de contenido](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-optimization/overview): Simplifique la creación de variantes de contenido visual a partir de recursos de origen utilizando indicaciones en lenguaje natural.</li><li>[Producción de experiencias](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/production/overview): automatiza tareas de alto esfuerzo y gran volumen en CMS. Este agente convierte los procesos manuales y largos en flujos de trabajo rápidos y asistidos por IA que mantienen todas las experiencias actualizadas y coherentes, lo que ayuda a su empresa a lograr sus objetivos.</li></ul> | <ul><li>Adobe Experience Manager (detección de contenido)</li></ul><ul><li>Adobe Experience Manager con Dynamic Media con OpenAPI (optimización de contenido)</li></ul><ul><li>Adobe Experience Manager Cloud Services y Edge Delivery Services (producción de experiencias) </li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | Responde rápidamente a preguntas sobre sus datos. Crea visualizaciones relevantes en Analysis Workspace utilizando componentes de la vista de datos y sus datos reales. | <ul><li>Customer Journey Analytics (Ediciones B2B y B2C)</li></ul> |
| **Agente de experiencia de marca** | [Soporte de implementación](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/development/overview): ayuda a los desarrolladores y administradores técnicos de AEM CS a solucionar errores de pasos de compilación en la canalización de Cloud Manager analizando la causa raíz y sugiriendo correcciones. | <ul><li>Asistente de IA en AEM Cloud Service y Adobe Managed Services</li></ul> |
| **Agente de control de marca*** | [Administración de marcas](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview): proteja la integridad y el cumplimiento de la marca mediante la aplicación de políticas de seguridad, normativas y de marca en Experience Manager. Este agente aplica el control de marca para mantener los estándares visuales y de mensajería. Utiliza permisos granulares para administrar los cambios de acceso y contenido, e incorpora DRM para cumplir las restricciones de licencia y uso. | <ul><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Forms</li></ul> |
| [Journey Agent](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze) | Permita que sus equipos creen, analicen y optimicen rápidamente recorridos de clientes multitáctiles a escala. | <ul><li>Adobe Journey Optimizer (ediciones B2B y B2C)</li></ul> |
| [Agente de soporte técnico](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/new-features/customer-support) | Solucione los problemas de soporte sin salir de sus flujos de trabajo, cree vales de soporte al cliente y rastree el progreso de los casos con el Asistente de IA. | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (Ediciones B2B y B2C)</li><li>Customer Journey Analytics (Ediciones B2B y B2C)</li><li>Adobe Experience Manager</li></ul> |

Asterisco (*): Los clientes del programa Explorer pueden acceder a este agente. El programa Explorer es un programa de solo invitación que proporciona acceso anticipado a las últimas funciones agénticas de Adobe. Póngase en contacto con el representante de su cuenta para obtener más información.

## Aplicaciones de Experience Cloud con prioridad de IA {#ai-first-apps}

Las aplicaciones de IA-First se crean con Al generativo o agéntico en el núcleo. Utilizan Al generativo o agéntico para tareas clave, y las funciones agénticas ya están incluidas en la licencia de aplicación Al-first. Como tal, no requieren la licencia de Experience Platform Agent Orchestrator.

En la tabla siguiente se enumeran los agentes de Experience Platform disponibles como aplicaciones All-first. Se habilitan mediante la licencia de estas aplicaciones iniciales:

| Nombre del agente | Competencias | Aplicaciones compatibles |
|---|----------|----------|
| [Experimentation Agent](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | Automatice, analice y sintetice perspectivas para que pueda identificar rápidamente experimentos de alto impacto y oportunidades de crecimiento desde un espacio de trabajo centralizado, todo ello reduciendo al mismo tiempo los procesos manuales. | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [Agente de optimización LLM](https://experienceleague.adobe.com/es/docs/llm-optimizer/using/home) | Mejore la visibilidad, precisión e influencia en entornos de búsqueda impulsados por IA, proporcione perspectivas sobre la presencia de la marca en respuestas generadas por IA, ofrezca recomendaciones de contenido prescriptivo y automatice correcciones de optimización. | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/es/docs/experience-manager-sites-optimizer/content/home) | Maximice el impacto en la empresa detectando e implementando automáticamente las mejoras en el sitio web. Con la IA generativa y varias tecnologías de monitorización, puede aumentar la adquisición de tráfico del sitio, la participación y mucho más | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/en/docs/brand-concierge/content/documentation/overview) | Impulse la conversión y la participación mediante la detección inteligente de productos según el contexto y adaptados a las preferencias y los comportamientos individuales. | <ul><li>Adobe Brand Concierge</li></ul> |

## Más ayuda sobre este tema

* [Trabajos del agente y consumo de crédito de IA](/help/interface/features/ai-credit-consumption.md)
* Inicio de la documentación de [AI en Experience Cloud](https://experienceleague.adobe.com/es/docs/ai)
* [Información general de agentes en AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE Más información en Adobe for Business]{type=Informative url="https://business.adobe.com/products/experience-platform/agent-orchestrator.html" tooltip="Vaya a Business.adobe.com"}
