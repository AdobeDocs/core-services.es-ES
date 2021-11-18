---
description: Conozca cuáles son los requisitos y qué esperar al actualizar a Analytics Premium.
keywords: Actualización de Adobe Analytics Premium
solution: Experience Cloud
title: 'Actualización a Analytics Premium y Experience Cloud '
topic: Administration
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
feature: Admin Console
role: Admin
level: Experienced
exl-id: 746d396d-9629-42db-8c55-07d2d24e4611
source-git-commit: ae14748aa7b0f0d803d48fe980a6743f53d996ab
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 86%

---

# Actualización a Analytics Premium y Experience Cloud

Los administradores pueden obtener información sobre los requisitos, qué encontrarán al actualizar a Analytics Premium y dónde encontrar ayuda como administradores de Experience Cloud.

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

Al actualizar a Adobe Analytics Premium obtiene todas las funciones o productos disponibles en Analytics Standard, entre los que se incluyen Data Warehouse, Ad Hoc Analysis, Report Builder y Data Connectors.

Analytics Premium le ofrece:

* Acceso a 250 variables de conversión (eVars)
* [Análisis de aplicaciones móviles](https://experienceleague.adobe.com/docs/mobile-services/using/home.html?lang=es)
* Data Workbench (consulta de datos visual, atribución basada en reglas, análisis en canales múltiples)

>[!NOTE]
>
>No es necesario realizar ninguna migración al actualizar, pero hay que tener en cuenta algunas consideraciones:
>
>* Las eVars 76-250 y 100-250 (Standard) están visibles en las herramientas de administración, pero no están habilitadas.
>* Adobe activa el Análisis de contribución. No cambia la ubicación (aún está disponible en la página Detección de anomalías), pero empieza a analizar automáticamente todos los puntos de datos.


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

En Analytics Premium Complete, obtiene todas las funciones de [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), además de las siguientes mejoras:

| Producto | Actualizaciones |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[Análisis de contribución](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=es)</li><li>[Atributos del cliente](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (hasta 200)</li></ul> |
| Data Workbench | <ul><li>Atribución algorítmica</li><li>Espacios de trabajo creados previamente</li></ul> |
| Plataforma de Analytics | [Transmisión en directo](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/index.md) (datos sin procesar, paneles, activadores) |

{style=&quot;table-layout:auto&quot;}

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

La actualización a Predictive Intelligence habilita [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) además de:

| Producto | Actualizaciones |
|---|---|
| Informes y análisis | [Análisis de contribución](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=en) |
| Data Workbench | Espacios de trabajo creados previamente para cualificaciones de audiencia y marketing predictivo. |
| Plataforma de Analytics | Reproducción en directo (tableros y Triggers) |

{style=&quot;table-layout:auto&quot;}

## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

La actualización a Customer 360 incluye [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) además de:

| Producto | Actualizaciones |
|--- |--- |
| [Atributos del cliente](attributes.md) | Atributos del cliente (uso compartido de análisis y segmentos) |
| Data Workbench | <ul><li>Atributos del cliente derivados</li><li>Espacios de trabajo creados previamente para la detección de audiencias</li></ul> |
| Plataforma de Analytics | [Atributos del cliente](attributes.md) |

{style=&quot;table-layout:auto&quot;}

## Atribución avanzada {#section_9E4986A8389946CCAA7D003268343296}

La Atribución avanzada permite disfrutar de [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507), además de Atribución algorítmica en Data Workbench (25% del volumen de llamadas al servidor).

## Requisitos de Data Workbench {#section_D959CA68D6DB42C38707F8E0CA3654CC}

Los usuarios con asistencia técnica pueden solicitar que todas las licencias de cliente se actualicen para que reflejen el software Premium enviando `dwb@adobe.com` por correo electrónico. Esta actualización habilita características como Atribución algorítmica.

TechOps revisa el compromiso de su contrato y determinará la infraestructura administrada adecuada, aumentando o reduciendo la capacidad, y luego se coordina con usted, a través del administrador de cuentas o consultor, para implementar cualquier cambio.

Cualquier software que se ejecute on-premise debe desactivarse. Este software incluye sensores, lo que significa que debe garantizar un seguimiento adecuado mediante etiquetas de [!DNL Analytics].

## Experience Cloud: Administración de usuarios y productos {#section_6471C54454024301B2E0B687F79F6738}

Los servicios principales y de Experience Cloud están disponibles para los usuarios de Analytics Standard y Premium si ha realizado la modernización de la implementación descrita en [Introducción: Habilite las aplicaciones para los servicios principales](core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C). (Este proceso le ayuda a modernizar las implementaciones y le permite convertirse en administrador en Experience Cloud).

Una vez que se una a Experience Cloud, podrá iniciar sesión en Experience Cloud en [!DNL experience.adobe.com] y comenzar a usar los servicios principales, incluidos los Atributos del cliente, las audiencias y los análisis de aplicaciones móviles.

### Administrar usuarios y grupos

La administración de usuarios se realiza en [Adobe Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html) (vínculo del producto).

Puede configurar una asignación individual entre un grupo creado en Adobe Admin Console y un grupo de soluciones (como Adobe Analytics). A continuación, un nuevo usuario agregado al grupo de Admin Console asignado tiene una cuenta de aplicación de Analytics creada automáticamente y vinculada al Adobe ID del usuario. (Los usuarios existentes deben vincular manualmente sus credenciales de cuenta de la aplicación para acceder a las aplicaciones mediante el inicio de sesión del Experience Cloud).

>[!NOTE]
>
>Puede asignar varios grupos de aplicaciones a un grupo de Admin Console. Sin embargo, Adobe recomienda la asignación individual. Al asignar los grupos con antelación, puede invitar, crear, autorizar y agregar varios usuarios cargando un CSV.
