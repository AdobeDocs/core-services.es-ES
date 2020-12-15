---
description: Los administradores pueden obtener información sobre los requisitos, qué encontrarán al actualizar a Analytics Premium y dónde encontrar ayuda como administradores de Experience Cloud.
keywords: Adobe Analytics Premium upgrade
solution: Experience Cloud
title: 'Cómo actualizar a Analytics Premium y al Experience Cloud '
topic: Premium
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
translation-type: tm+mt
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 98%

---


# Actualización a Analytics Premium y Experience Cloud

Los administradores pueden obtener información sobre los requisitos, qué encontrarán al actualizar a Analytics Premium y dónde encontrar ayuda como administradores de Experience Cloud.

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

Al actualizar a Adobe Analytics Premium obtiene todas las funciones o productos disponibles en Analytics Standard, entre los que se incluyen Data Warehouse, Ad Hoc Analysis, Report Builder y Data Connectors (Estos productos se vendieron por separado a los clientes que utilizan la solución clave, SiteCatalyst).

Analytics Premium le ofrece:

* Acceso a 250 variables de conversión (eVars)
* [Análisis de aplicaciones móviles](https://docs.adobe.com/content/help/es-ES/mobile-services/using/home.html)
* Data Workbench (consulta de datos visual, atribución basada en reglas, análisis en canales múltiples)

>[!NOTE]
>
>No es necesario realizar ninguna migración al actualizar, pero hay que tener en cuenta algunas consideraciones:
>
>* Las eVars 76-250 (SiteCatalyst) y 100-250 (Standard) estarán visibles en las Herramientas de administración, pero no estarán habilitadas por defecto.>
>* Adobe activa el Análisis de contribución. No cambiará la ubicación (aún está disponible en la página Detección de anomalías), pero ahora analizará automáticamente en inicio todos los puntos de datos.>


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

En Analytics Premium Complete, obtiene todas las funciones de [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), además de las siguientes mejoras:

| Producto | Actualizaciones |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[Análisis de contribución](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html)</li><li>[Atributos del cliente](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (hasta 200)</li></ul> |
| Data Workbench | <ul><li>Atribución algorítmica</li><li>Espacios de trabajo creados previamente</li></ul> |
| Plataforma de Analytics | [Transmisión en directo](https://helpx.adobe.com/es/analytics/kb/getting-started-with-livestream-api.html) (datos sin procesar, paneles, activadores) |

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

La actualización a Predictive Intelligence habilita [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) además de:

| Producto | Actualizaciones |
|---|---|
| Reports &amp; Analytics | [Análisis de contribución](https://docs.adobe.com/content/help/es-ES/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Data Workbench | Espacios de trabajo creados previamente para cualificaciones de audiencia y marketing predictivo |
| Plataforma de Analytics | Reproducción en directo (tableros y Triggers) |

## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

La actualización a Customer 360 incluye [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) además de:

| Producto | Actualizaciones |
|--- |--- |
| [Atributos del cliente](../attributes/attributes.md) | Atributos del cliente (uso compartido de análisis y segmentos) |
| Data Workbench | <ul><li>Atributos del cliente derivados</li><li>Espacios de trabajo creados previamente para la detección de audiencias</li></ul> |
| Plataforma de Analytics | [Atributos del cliente](../attributes/attributes.md) |

## Atribución avanzada {#section_9E4986A8389946CCAA7D003268343296}

La Atribución avanzada permite disfrutar de [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), además de Atribución algorítmica en Data Workbench (25% del volumen de llamadas al servidor).

## Requisitos de Data Workbench {#section_D959CA68D6DB42C38707F8E0CA3654CC}

Los usuarios con asistencia técnica pueden solicitar que todas las licencias de cliente se actualicen para que reflejen el software Premium enviando `dwb@adobe.com` por correo electrónico. Esto habilita características como Atribución algorítmica.

TechOps revisará el compromiso de su contrato y determinará la infraestructura administrada adecuada, aumentando o reduciendo la capacidad, y luego se coordinará con usted, a través del administrador de cuentas o consultor, para implementar cualquier cambio.

Cualquier software que se ejecute on-premise debe desactivarse. Esto incluye los sensores, lo que significa que deberá garantizar un seguimiento adecuado mediante etiquetas de Analytics.

## Experience Cloud: Administración de usuarios y productos {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloud y los servicios principales están disponibles para los usuarios de Analytics Standard y Premium, siempre y cuando hayan realizado la modernización de la implementación descrita en [Introducción: habilite sus soluciones para utilizar los servicios principales](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C). (Este proceso le ayuda a modernizar las implementaciones y le permite convertirse en administrador en Experience Cloud).

Una vez que se una a Experience Cloud, podrá iniciar sesión en Experience Cloud en [!DNL experiencecloud.adobe.com] y comenzar a usar los servicios principales, incluidos los Atributos del cliente, las audiencias y los análisis de aplicaciones móviles.

### Administrar usuarios y grupos

La administración de usuarios se realiza en [Adobe Admin Console](https://helpx.adobe.com/es/enterprise/help/aedash.html) (vínculo del producto).

Puede configurar una asignación individual entre un grupo creado en Adobe Admin Console y un grupo de soluciones (como Adobe Analytics). A partir de entonces, un nuevo usuario agregado al grupo de Admin Console asignado tendrá una cuenta de la solución Analytics creada automáticamente y vinculada al Adobe ID del usuario. (Los usuarios existentes deben vincular manualmente sus credenciales de cuenta de la solución para acceder a las soluciones mediante el inicio de sesión de Experience Cloud).

>[!NOTE]
>
>Se pueden asignar varios grupos de soluciones a un grupo de Admin Console. Sin embargo, Adobe recomienda la asignación individual. Al asignar los grupos con antelación, puede invitar, crear, autorizar y agregar varios usuarios cargando un CSV.
