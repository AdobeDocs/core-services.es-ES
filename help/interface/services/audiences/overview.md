---
title: “[!DNL Audience Library]”
description: Descubra cómo administrar la traducción de datos sobre visitantes en segmentación de público en Experience Cloud [!DNL Audience Library].
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
source-git-commit: b257260bdbb7870dd6da807bceddfcddd2aef779
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 94%

---

# Públicos de Experience Cloud {#topic_679810123CAA4E0CA4FA3417FB0100C7}

La [!DNL Audience Library] muestra los públicos en Experience Cloud. Los públicos son recopilaciones de visitantes (una lista de ID de [!DNL Experience Cloud]). Puede administrar la traducción de los datos de visitantes en la segmentación del público. Como tal, crear y administrar públicos es similar a crear y utilizar segmentos. También puede compartir el segmento de público con productos y servicios de [!DNL Experience Cloud].

![Públicos de Experience Cloud](assets/audiences.png)

Los públicos pueden crearse o derivarse desde distintos orígenes como:

* Las nuevas se crean en [!DNL Experience Cloud]
* Segmentos de [!DNL Analytics] publicados en [!DNL Experience Cloud]
* [!DNL Audience Manager]

**Públicos en tiempo real vs. públicos históricos**

Todos los públicos, independientemente de su origen, son accesibles para los casos de uso de segmentación en tiempo real. Sin embargo, las audiencias compartidas desde Analytics en Audience Manager no se pueden utilizar para los procesos de segmentación en tiempo real. El sistema evalúa los públicos de dos maneras:

* Los públicos históricos de Analytics se evalúan cada cuatro horas. El tiempo total para procesar y compartir puede llevar hasta ocho horas. Los públicos históricos siempre incluyen los visitantes de retorno.
* Estos públicos provienen de Públicos de Experience Cloud y se evalúan en tiempo real.

## Cómo utilizan las aplicaciones los públicos {#concept_01EB9345C5344597BC94A864EDD38EE1}

En la tabla siguiente se describe cómo se utilizan los públicos en las aplicaciones de Experience Cloud:

| Solución | Descripción |
|--- |--- |
| Públicos de Experience Cloud | Cree, administre y comparta audiencias de forma nativa con la Biblioteca de audiencias. Puede:<ul><li>Usar públicos en tiempo real mediante atributos de análisis sin procesar</li><li>Combinar públicos para crear composiciones, uniendo datos históricos y en tiempo real</li><li>Ver vistas gráficas del tamaño estimado de públicos</li></ul><br>Para obtener sugerencias sobre el tipo de público que desea crear, consulte [Opciones de creación de público](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=es). |
| Analytics | En la segmentación puede crear un segmento, combinarlo con un grupo de informes y, a continuación, publicar el segmento en Experience Cloud. Al publicar el segmento, aparece en Experience Cloud en la página [!DNL Audience Library]. (Consulte [Publicar segmentos en Experience Cloud](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=es) en la ayuda de [!DNL Analytics] para obtener más información). El público también está disponible como público objetivo para una experiencia de campaña suministrada por [!DNL Adobe Target] y en [!DNL Audience Manager]. Después de compartir un público de [!DNL Adobe Analytics] y seleccionarlo para usarlo en una campaña activa, los perfiles de visitantes que cumplan los criterios de definición de segmento de los últimos 90 días se envían a [!UICONTROL Audience Services]. El límite de públicos compartidos se ha aumentado a 75. Los públicos compartidos en Experience Cloud desde [!DNL Analytics] no pueden superar los 20 millones de miembros únicos. Además, debido al almacenamiento en caché, los grupos de informes que se eliminan en Analytics tardan 12 horas en desaparecer de Experience Cloud. |
| Mobile Services | Analice el tráfico móvil mediante la visualización radial en el informe [!UICONTROL Tipos de dispositivos]. |
| [!DNL Target] | El [servicio de ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=es) unifica el ID y los datos de los visitantes en un único perfil que se puede activar para utilizarlo en todas las aplicaciones. Marcar la casilla [!UICONTROL Publicar en Experience Cloud] durante el proceso de creación de segmentos en Adobe Analytics permite que el segmento esté disponible en la biblioteca de públicos personalizada de Adobe Target. Un segmento creado en [!DNL Analytics] o [!DNL Audience Manager] puede utilizarse para actividades en [!DNL Target]. Por ejemplo, puede crear actividades de campaña basadas en las métricas de conversión de [!DNL Analytics] y segmentos de públicos creados en [!DNL Analytics]. |
| [!DNL Audience Manager] | Los públicos compartidos están disponibles en la segmentación de [!DNL Audience Manager]. Todos los públicos de Experience Cloud están disponibles de forma nativa en [!DNL Audience Manager], que proporciona lo siguiente:<ul><li>Automatización integrada sobre cómo se comparten y consumen los flujos de trabajo de la aplicación</li><li>Destinos fuera del sitio</li><li>Modelado similar</li></ul> |
| Campaign | <ul><li>Importación de públicos compartidos de diferentes aplicaciones de Adobe Experience Cloud en Adobe Campaign.</li><li>Exportación de listas de destinatarios como públicos compartidos. Estos públicos compartidos pueden utilizarse con las diferentes aplicaciones de Adobe Experience Cloud que use.</li></ul> |
| Advertising Cloud | Utilice el público como destinatarios. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Una vez que un visitante se califica para el público compartido desde Analytics, deben pasar de 4 a 8 horas antes de que pueda realizarse alguna acción sobre esa información en [!DNL Target], Ad Cloud y Campaign Standard.

## Elementos de la interfaz de la biblioteca de públicos {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] proporciona una biblioteca para la creación y administración de públicos, con identificación de público nativa y en tiempo real.

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Biblioteca de públicos]**

![Adición de un público en la biblioteca de públicos](assets/audience_library.png)


| Elemento | Descripción |
|--- |--- |
| Nuevo | [Crear un público](create.md). |
| Título y descripción | Un encabezado de columna que identifica y describe el público. |
| Autor | La persona que creó el segmento de público. |
| Fuente | Identifica dónde se creó el público.<ul><li>**Analytics:** Un segmento creado en Adobe Analytics y publicado en el Experience Cloud.</li><li>**Experience Cloud:** público nuevo [creado en Públicos de Experience Cloud](create.md).</li><li>**Audience Manager:** los públicos creados en Audience Manager se muestran automáticamente en Públicos de Experience Cloud.</li></ul> |
| Tamaño actual | El tamaño de público actual. |
| Activo | El estado activo del segmento. |

{style="table-layout:auto"}

## Audiencias de Publish de Adobe Analytics

Consulte [Segmentos de Publish para el Experience Cloud](https://experienceleague.adobe.com/en/docs/analytics/components/segmentation/segmentation-workflow/seg-publish) en la documentación de Adobe Analytics para obtener más información.
