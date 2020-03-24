---
description: Administrar la traducción de datos de visitantes en la segmentación de audiencias.
seo-description: Administrar la traducción de datos de visitantes en la segmentación de audiencias.
seo-title: Audiencias
solution: Experience Cloud
title: Audiencias
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
translation-type: tm+mt
source-git-commit: 14d6e0ae15b023ad4dd3f8aca0606f26b39a21e9

---


# Audiencias {#topic_679810123CAA4E0CA4FA3417FB0100C7}

Las Audiencias son colecciones de visitantes (una lista de ID de visitante). Los servicios de audiencia de Adobe administran la traducción de datos de visitante en segmentación de audiencias. De este modo, la creación y gestión de audiencias es similar a la creación y uso de segmentos, con la capacidad añadida de compartir segmentos de audiencia en [!DNL Experience Cloud].

![](assets/audiences.png)

Las audiencias pueden crearse o derivarse desde distintos orígenes como:

* Las nuevas se crean en [!DNL Experience Cloud]
* A partir de segmentos de [!DNL Analytics] publicados en [!DNL Experience Cloud]
* De [!DNL Audience Manager]

**Audiencias en tiempo real o históricas**

Todas las audiencias, independientemente de su origen, son accesibles para los casos de uso de segmentación en tiempo real. Sin embargo, las audiencias compartidas desde Analytics a Audience Manager no se pueden utilizar para los procesos de segmentación en tiempo real. El sistema evalúa las audiencias de dos maneras:

* Las audiencias históricas de Analytics se evalúan cada 4 horas. El tiempo total para procesar y compartir puede tardar hasta 8 horas.  Las audiencias históricas siempre incluyen visitantes de retorno.
* Estas audiencias provienen de Experience Cloud Audiences y se evalúan en tiempo real.

## Cómo utilizan las soluciones las audiencias {#concept_01EB9345C5344597BC94A864EDD38EE1}

En la tabla siguiente se describe cómo se utilizan las audiencias en las soluciones de Experience Cloud:

| Solución | Descripción |
|--- |--- |
| Audiencias de Experience Cloud | Cree, administre y comparta audiencias de forma nativa con la interfaz de [Biblioteca de audiencias](../audience-library/audience-library.md). Puede:<ul><li>Usar audiencias en tiempo real mediante atributos de análisis sin procesar</li><li>Combinar audiencias para crear composiciones, uniendo datos históricos y en tiempo real</li><li>Ver vistas gráficas del tamaño estimado de audiencias</li></ul><br>Para obtener sugerencias sobre el tipo de audiencia que desea crear, consulte: Audiencias [de Experience Cloud](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html). |
| Analytics | En la segmentación puede crear un segmento, combinarlo con un grupo de informes y, a continuación,  [publicarlo en Experience Cloud](../audience-library/audience-library.md). Los segmentos publicados se muestran en la página [Audiencias](../audience-library/audience-library.md). La audiencia también está disponible como audiencia de destino para una experiencia de campaña suministrada por Adobe Target y en Audience Manager. Once an audience is shared from Analytics, and selected for use in an active campaign, all the visitor profiles who met the segment definition criteria for the past 90 days are sent to the Experience Cloud [!UICONTROL Audience Services] platform. El límite de audiencias compartidas se ha aumentado a 75. Las Audiencias compartidas en Experience Cloud desde Analytics no pueden superar los 20 millones de miembros únicos. Además, debido al almacenamiento en caché, los grupos de informes eliminados en Analytics tardan 12 horas en desaparecer de Experience Cloud. |
| Mobile Services | Analice el tráfico móvil mediante la visualización radial en el informe Tipos [!UICONTROL de] dispositivos. |
| Target | The [ID service](https://docs.adobe.com/content/help/en/id-service/using/home.html) unifies visitor IDs and data into a single, actionable profile for use across solutions. Marcar la casilla [Publicar en Experience Cloud](../audience-library/audience-library.md) durante el proceso de creación de segmentos en Adobe Analytics permite que el segmento esté disponible en la biblioteca de audiencias personalizada de Adobe Target. Un segmento creado en Analytics o Audience Manager puede utilizarse para actividades en Target.  Por ejemplo, puede crear actividades de campaña basadas en métricas de conversión de Analytics y segmentos de audiencias creados en Analytics. |
| Audience Manager | Las audiencias compartidas están disponibles en la segmentación del Administrador de Audiencias. Todas las audiencias de Experience Cloud están disponibles de forma nativa en Audience Manager, que proporciona lo siguiente:<ul><li>Automatización integrada sobre cómo se comparten y consumen los flujos de trabajo de la solución</li><li>Destinos fuera del sitio</li><li>Modelado similar</li></ul> |
| Campaign | <ul><li>Importar audiencias compartidas de diferentes soluciones de Adobe Experience Cloud en Adobe Campaign.</li><li>Exportar listas de destinatario en forma de audiencias compartidas. Estas audiencias compartidas se pueden usar en las distintas soluciones de Adobe Experience Cloud que utilice.</li></ul> |
| Media Optimizer | Utilice la audiencia como destinatarios. |

>[!IMPORTANT]
>
>Una vez que un visitante cumple los requisitos para la audiencia compartida desde Analytics, se produce un retraso de 4 a 8 horas antes de que la información se pueda procesar en Destinatario, Ad Cloud y Campaign Standard.

## Más ayuda: preguntas, sugerencias y casos de uso {#section_C7F151644D8A45F7B6FC54F58845635D}

| Ayuda con | Recurso |
|--- |--- |
| ¿No puede encontrar Audiencias? | Compruebe que está aprovisionado. Consulte  [Introducción: Habilite sus soluciones para los servicios principales](../core-services/core-services.md).<br>Haga clic [aquí](https://www.adobe.com/go/audiences) para solicitar acceso a Perfiles y Audiencias (formulario de aprovisionamiento de integraciones). |
| Casos de uso | Para obtener más información sobre la solución que se debe utilizar, vaya a Opciones [de creación de](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html) Audiencias en la Base de conocimiento. |
| Foro | The [Audiences forum](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences) is an additional resource to get help with audiences. |

## Elementos de la interfaz de la biblioteca de audiencias {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] proporciona una biblioteca para la creación y administración de audiencias, con identificación de audiencia nativa y en tiempo real.

**[!UICONTROL Experience Cloud]** > Plataforma **** de experiencias > **[!UICONTROL Personas]** > Biblioteca de **[!UICONTROL Audiencias]**

![](assets/audience_library.png)

| Elemento | Descripción |
|--- |--- |
| Nuevo | [Crear una audiencia](../audience-library/audience-library.md). |
| Título y descripción | Un encabezado de columna que identifica y describe la audiencia. |
| Autor | La persona que creó el segmento de audiencia. |
| Fuente | Identifica dónde se creó la audiencia.<ul><li>**Analytics:** Un segmento creado en Reports &amp; Analytics o Ad Hoc Analysis que más tarde [se publicará en Experience Cloud](../audience-library/audience-library.md).</li><li>**Experience Cloud:** audiencia nueva [creada en Audiencias de Experience Cloud](../audience-library/audience-library.md).</li><li>**Audience Manager:** las audiencias creadas en Audience Manager se muestran automáticamente en Audiencias de Experience Cloud.</li></ul> |
| Tamaño actual | El tamaño de audiencia actual. |
| Activo | El estado activo del segmento. |
