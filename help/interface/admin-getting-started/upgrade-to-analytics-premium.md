---
description: Los administradores pueden obtener información sobre los requisitos, qué encontrarán al actualizar a Analytics Premium y dónde encontrar ayuda como administradores de Experience Cloud.
keywords: actualización
seo-description: Los administradores pueden obtener información sobre los requisitos, qué encontrarán al actualizar a Analytics Premium y dónde encontrar ayuda como administradores de Experience Cloud.
seo-title: Actualización a Analytics Premium y Experience Cloud
solution: Experience Cloud
title: Actualización a Analytics Premium y Experience Cloud
topic: Premium
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
translation-type: ht
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# Actualización a Analytics Premium y Experience Cloud

Los administradores pueden obtener información sobre los requisitos, qué encontrarán al actualizar a Analytics Premium y dónde encontrar ayuda como administradores de Experience Cloud.


## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

Al actualizar a Adobe Analytics Premium obtiene todas las funciones o productos disponibles en Analytics Standard, entre los que se incluyen Data Warehouse, Ad Hoc Analysis, Report Builder y Data Connectors (estos productos se vendían por separado a los cliente mediante la solución puntual, SiteCatalyst).

Analytics Premium ofrece

* Acceso a 250 variables de conversión (eVars)
* [Análisis de aplicaciones móviles](https://marketing.adobe.com/resources/help/es_ES/mobile/)
* Data Workbench (consulta de datos visual, atribución basada en reglas, análisis en canales múltiples)



>[!NOTE]
>
>No es necesario realizar ninguna migración al realizar la actualización, pero hay algunos aspectos que se deben tener en cuenta:
>
>* Las eVars 76-250 (SiteCatalyst) y 100-250 (Standard) estarán visibles en Herramientas de administración, pero todavía no estarán habilitadas.&gt;
>* Adobe activa el Análisis de contribución. No cambiará la ubicación (aún está disponible en la página Detección de anomalías), pero ahora comenzará a analizar automáticamente todos los puntos de datos.&gt;


En las secciones siguientes se describe dónde puede encontrar ayuda, en función de las características que ha comprado:

* [Analytics Premium Complete](../admin-getting-started/upgrade-to-analytics-premium.md#section_BFAD815EDF364845A52B340B2FD5B64C)
* [Predictive Intelligence](../admin-getting-started/upgrade-to-analytics-premium.md#section_B407932C07A7476F83FB0275C3FB63DC)
* [Customer 360](../admin-getting-started/upgrade-to-analytics-premium.md#section_3B2AC245388248688067DC9A48957AFB)
* [Atribución avanzada](../admin-getting-started/upgrade-to-analytics-premium.md#section_9E4986A8389946CCAA7D003268343296)
* [Requisitos de Data Workbench](../admin-getting-started/upgrade-to-analytics-premium.md#section_D959CA68D6DB42C38707F8E0CA3654CC)
* [Experience Cloud](../admin-getting-started/upgrade-to-analytics-premium.md#section_6471C54454024301B2E0B687F79F6738)



## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

En Analytics Premium Complete, obtiene todas las funciones de [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), así como las siguientes actualizaciones:

| Producto | Actualizaciones |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[Análisis de contribución](https://marketing.adobe.com/resources/help/es_ES/analytics/contribution/)</li><li>[Atributos del cliente](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (hasta 200)</li></ul> |
| Data Workbench | <ul><li>Atribución algorítmica</li><li>Espacios de trabajo creadas previamente</li></ul> |
| Plataforma de análisis | [Reproducción en directo](https://marketing.adobe.com/developer/documentation/analytics-live-stream/overview-1)   (datos sin procesar, tableros, desencadenadores) |


## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

Al actualizar a Predictive Intelligence se habilita [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), además de:

| Producto | Actualizaciones |
|---|---|
| Reports &amp; Analytics | [Análisis de contribución](https://marketing.adobe.com/resources/help/es_ES/analytics/contribution/) |
| Data Workbench | Espacios de trabajo creadas previamente para cualificaciones de audiencia y marketing predictivo. |
| Plataforma de análisis | Reproducción en directo (tableros y Triggers) |


## Customer 360  {#section_3B2AC245388248688067DC9A48957AFB}

Al actualizar a Customer 360 se ofrece [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), además de:

| Producto | Actualizaciones |
|--- |--- |
| [Atributos del cliente](../attributes/attributes.md) | Atributos del cliente (uso compartido de análisis y segmentos) |
| Data Workbench | <ul><li>Atributos derivados del cliente</li><li>Espacios de trabajo creadas previamente para detección de audiencias</li></ul> |
| Plataforma de análisis | [Atributos del cliente](../attributes/attributes.md) |


## Atribución avanzada {#section_9E4986A8389946CCAA7D003268343296}

Atribución avanzada ofrece acceso a [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), además de Atribución algorítmica en el Data Workbench (25 % de volumen de llamadas al servidor).

## Requisitos de Data Workbench  {#section_D959CA68D6DB42C38707F8E0CA3654CC}

Los usuarios con asistencia técnica pueden solicitar que todas las licencias de cliente se actualicen para que reflejen el software Premium enviando `dwb@adobe.com` por correo electrónico. De este modo, se habilitan las características como Atribución algorítmica.

Los TechOps revisan el compromiso contractual y determinan cuál es la infraestructura más adecuada, ya sea aumentando o reduciendo la capacidad y, a continuación, se coordinan con usted, por medio del Administrador de cuenta o consultoría, para implementar cualquier cambio.

Cualquier software que se ejecute de forma local debe desactivarse, incluidos los sensores, lo que significa que deberá asegurarse de realizar un seguimiento adecuado de las etiquetas de Analytics.

**Premium Complete** y **Atribución avanzada**

Para la atribución basada en reglas de plantillas creadas previamente, consulte: [Atribución basada en reglas](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_rules_attrib).

Para la Atribución algorítmica, consulte [Atribución óptima](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_attrib_algorithmic)

**Predictive Intelligence**

Predictive Intelligence en Data Workbench incluye las visualizaciones siguientes:

* [Puntuación de tendencia de audiencias](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_visitor_propensity)
* [Agrupación de visitantes](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_visitor_cluster)
* [Análisis de correlación](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_correlation_analysis)


**Customer 360** y **Atribución avanzada**

Consulte la atribución basada en reglas de Analytics en plantillas creadas previamente en [Atribución basada en reglas](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_rules_attrib).

Consulte las plantillas de Atribución algorítmica en [Atribución óptima](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_attrib_algorithmic).

## Experience Cloud: Administración de usuarios y productos {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloud y los servicios principales están disponibles para los usuarios de Analytics Standard y Premium, siempre y cuando hayan realizado la modernización de la implementación descrita en [Introducción: habilite sus soluciones para utilizar los servicios principales](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C). (Este proceso le ayuda a modernizar las implementaciones y le permite convertirse en administrador en Experience Cloud).

Una vez que se una a Experience Cloud, podrá iniciar sesión en Experience Cloud en [!DNL marketing.adobe.com] y comenzar a usar los servicios principales, incluidos los atributos del cliente, las audiencias y los análisis de aplicaciones móviles.

**Administrar usuarios y grupos**

La administración de usuarios se realiza en [Adobe Admin Console](https://helpx.adobe.com/es/enterprise/help/aedash.html) (vínculo del producto).

Puede configurar una asignación 1:1 entre un grupo creado en Adobe Admin Console y un grupo de soluciones (como, por ejemplo, Adobe Analytics). A continuación, para cada nuevo usuario que se agregue al grupo de Admin Console, se creará y vinculará automáticamente a su Adobe ID una cuenta de soluciones de Analytics. (Los usuarios existentes deben vincular manualmente las credenciales de la cuenta de su solución para acceder a las soluciones mediante el inicio de sesión de Experience Cloud).


>[!NOTE]
>
>Se pueden asignar varios grupos de soluciones a un grupo de Admin Console. Sin embargo, Adobe recomienda una asignación 1:1. La asignación de grupos por anticipado permite invitar, crear, autorizar y agregar varios usuarios cargando un CSV.

