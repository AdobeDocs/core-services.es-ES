---
title: Inteligencia artificial aplicada a la agencia en aplicaciones Experience Cloud
description: Descubra dónde está disponible la IA auténtica en las aplicaciones empresariales de CX.
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
last-update: '2026-05-21T00:00:00.000Z'
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
feature_v2:
  - id: f84b2906-3ce9-4ef0-86f6-cda249273937
source-git-commit: 5b2b81c029b81b9f0689a012cb2a9ca8714c0b40
workflow-type: tm+mt
source-wordcount: 1130
ht-degree: 10%

---

# Inteligencia artificial aplicada a la agencia en Adobe CX Enterprise

Los agentes de Adobe Experience Platform cuentan con la tecnología [Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/home) para habilitar las capacidades de IA auténtica en las aplicaciones empresariales de CX.

Estos agentes ayudan a automatizar tareas, ofrecer perspectivas más rápido y optimizar los flujos de trabajo. Como resultado, los equipos pueden trabajar de forma más eficiente y obtener más valor de CX Enterprise.

El acceso a los agentes de IA en CX Enterprise está disponible en:

* [Aplicaciones empresariales de CX existentes](#existing-apps)
* [Aplicaciones empresariales de CX con IA por primera vez](#ai-first-apps)

Las secciones siguientes describen estas dos formas de habilitar la IA auténtica en CX Enterprise.

## Aplicaciones empresariales de CX existentes {#existing-apps}

En las aplicaciones existentes, puede usar lenguaje natural para instruir a los agentes de Adobe Experience Platform a través de la interfaz conversacional de [AI Assistant](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/home). El asistente de IA está disponible en las vistas de pantalla completa y carril derecho.

Los agentes se pueden habilitar en aplicaciones de CX Enterprise existentes para clientes de una de las siguientes categorías:

* Ha adquirido una licencia de Adobe Experience Platform Agents AI Credit
* Se le incluye en una prueba sujeta a uso (se proporcionan créditos de IA limitados)
* Ha realizado transacciones con el SKU de promoción de Agent Orchestrator (licencia de prueba con tiempo limitado)

El uso de agentes de IA para realizar _trabajos de agente_ consume créditos de IA. Obtenga más información acerca de los trabajos del agente y los créditos de IA en _[Trabajos del agente y consumo de crédito de IA](/help/interface/features/ai-credit-consumption.md)_.

Los agentes de IA siguen _sus_ entradas, supervisión y respetan los controles de acceso de nivel de producto. Solo puede realizar trabajos o acceder a datos que esté autorizado a utilizar en la aplicación CX Enterprise subyacente.

### Agentes de IA en aplicaciones empresariales de CX existentes {#existing-apps-table}

En la tabla siguiente se enumeran los agentes de Experience Platform disponibles en las aplicaciones empresariales de CX existentes.

| Nombre del agente | Competencias | Aplicaciones compatibles | Datos de estado/preparados para HIPAA |
|---|----------|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | Habilite a sus equipos para que administren y optimicen audiencias utilizando indicaciones de lenguaje natural para que sean más fáciles, eficientes y rápidas de comercializar. | <ul><li>Real-Time CDP (ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (ediciones B2B y B2C)</li></ul> | |
| [Agente de Asesor de contenido](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-advisor/overview) | <ul><li>Ayuda a los equipos a encontrar rápidamente el contenido más relevante en toda la empresa mediante el uso de lenguaje natural, lo que reduce el tiempo empleado en la búsqueda y permite decisiones y ejecución más rápidas.</li><li>Simplifique la creación de variantes de contenido visual a partir de recursos de origen utilizando indicaciones de lenguaje natural.</li></ul> | <ul><li>Adobe Experience Manager Assets</li></ul><ul><li>Dynamic Media (Cloud Services)</li></ul> | |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | Responde rápidamente a preguntas sobre sus datos. Crea visualizaciones relevantes en Analysis Workspace utilizando componentes de la vista de datos y sus datos reales. | <ul><li>Customer Journey Analytics (Ediciones B2B y B2C)</li></ul> | Sí |
| [Brand Experience Agent](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/overview) | <ul><li>Acelera la migración y modernización de las experiencias digitales mediante la reestructuración, el enriquecimiento y la validación automáticos de los sitios existentes, de modo que los equipos puedan pasar más rápido a experiencias modernas y preparadas para IA con menos riesgos y esfuerzo manual.</li><li>Asume la creación y las actualizaciones de experiencias de gran volumen, lo que reduce considerablemente el esfuerzo manual y el tiempo de ciclo para que los equipos puedan moverse más rápido sin sacrificar la calidad o la coherencia.</li><li>Acelera la creación de formularios optimizados y de marca al generar, estructurar y validar experiencias de formulario automáticamente, lo que permite a los equipos iniciar más rápido y capturar datos de mayor calidad con un esfuerzo manual mínimo.</li><li>Ayuda a los desarrolladores y administradores técnicos de AEM CS a solucionar errores en los pasos de compilación de la canalización de Cloud Manager mediante el análisis de la causa raíz y la sugerencia de correcciones.</li></ul> | <ul><li>Adobe Experience Manager Sites Cloud Services (modernización de experiencias)</li></ul><ul><li>Adobe Experience Manager Sites (producción de experiencias)</li></ul><ul><li>Adobe Experience Manager Forms (Creación de formularios)</li></ul><ul><li>Todas las aplicaciones de Adobe Experience Manager basadas en la nube (compatibilidad con desarrollo)</li></ul> | |
| [Agente de control de marca](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview) | Proteja la integridad de la marca y el cumplimiento de las políticas de marca automatizadas: comprobaciones, permisos e inteligencia para admitir DRM con administración en tiempo real. | <ul><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Sites (Política de marca)</li></ul> | |
| [Journey Agent](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent) | Permita que sus equipos analicen y optimicen rápidamente los recorridos de clientes multitáctiles a escala. | <ul><li>Adobe Journey Optimizer (ediciones B2B y B2C)</li></ul> | |
| [Agente de soporte técnico](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/product-support) | Solucione los problemas de soporte sin salir de sus flujos de trabajo, cree vales de soporte al cliente y rastree el progreso de los casos con el Asistente de IA. | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (Ediciones B2B y B2C)</li><li>Customer Journey Analytics (Ediciones B2B y B2C)</li><li>Adobe Experience Manager</li></ul> | |
| [Adobe Marketing Agent para Microsoft 365 Copilot](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/agents/ama-ms) | Conecta Experience Platform directamente a Microsoft 365 Copilot. Puede hacer preguntas en lenguaje natural dentro de las aplicaciones de Microsoft 365, como Teams, Word, Powerpoint y Excel, para recuperar instantáneamente la información de marketing de Experience Platform sin interrumpir el flujo de trabajo. | <ul><li> Adobe Agent Orchestrator compatible con Audience Agent, Journey Agent, Customer Journey Analytics Data Insights y Experience Platform Operational Insights</li></ul> | |

## Aplicaciones empresariales de CX con IA por primera vez {#ai-first-apps}

Las aplicaciones de IA-First se crean con Al generativo o agéntico en el núcleo. Utilizan Al generativo o agéntico para tareas clave, y las funciones agénticas ya están incluidas en la licencia de aplicación Al-first. Como tal, no requieren la licencia de Experience Platform Agent Orchestrator.

En la tabla siguiente se enumeran los agentes de Experience Platform disponibles como aplicaciones All-first. Se habilitan mediante la licencia de estas aplicaciones iniciales:

| Nombre del agente | Competencias | Aplicaciones compatibles |
|---|----------|----------|
| [Experimentation Agent](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | Automatice, analice y sintetice perspectivas para que pueda identificar rápidamente experimentos de alto impacto y oportunidades de crecimiento desde un espacio de trabajo centralizado, todo ello reduciendo al mismo tiempo los procesos manuales. | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [Agente de optimización LLM](https://experienceleague.adobe.com/es/docs/llm-optimizer/using/home) | Mejore la visibilidad, precisión e influencia en entornos de búsqueda impulsados por IA, proporcione perspectivas sobre la presencia de marca en respuestas generadas por IA, ofrezca recomendaciones de contenido prescriptivo y automatice las correcciones de optimización. | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/es/docs/experience-manager-sites-optimizer/content/home) | Maximice el impacto en la empresa detectando e implementando automáticamente las mejoras en el sitio web. Con la IA generativa y varias tecnologías de monitorización, puede aumentar la adquisición de tráfico del sitio, la participación y mucho más | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/en/docs/brand-concierge/content/documentation/overview) | Impulse la conversión y la participación mediante la detección inteligente de productos según el contexto y adaptados a las preferencias y los comportamientos individuales. | <ul><li>Adobe Brand Concierge</li></ul> |

## Más ayuda sobre este tema

* [Trabajos del agente y consumo de crédito de IA](/help/interface/features/ai-credit-consumption.md)
* Inicio de la documentación de [AI en CX Enterprise](https://experienceleague.adobe.com/en/docs/ai)
* [Información general sobre los agentes en AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE Más información en Adobe for Business]{type=Informative url="https://business.adobe.com/products/experience-platform/agent-orchestrator.html" tooltip="Vaya a Business.adobe.com"}
