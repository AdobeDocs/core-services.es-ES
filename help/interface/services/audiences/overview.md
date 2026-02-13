---
title: '[!DNL Audience Library]'
description: Descubra cómo administrar la traducción de datos sobre visitantes en segmentación de público en Experience Cloud [!DNL Audience Library].
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
TQID: https://experienceleague.adobe.com/QEAfCWPNI-JhDw-HjZwBGv0TlqyctIqSwz8eVQqS6Gg
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 0d253888322194189fea6d492ae19cf248357960
workflow-type: tm+mt
source-wordcount: 684
ht-degree: 71%

---

# Públicos de Experience Cloud

[!DNL Audience Library] muestra audiencias en Experience Cloud. Los públicos son recopilaciones de visitantes (una lista de ID de [!DNL Experience Cloud]). Puede administrar la traducción de los datos de visitantes en la segmentación del público. De este modo, la creación y gestión de audiencias es similar a la creación y uso de segmentos. También puede compartir el segmento de público con productos y servicios de [!DNL Experience Cloud].

![Públicos de Experience Cloud](assets/audiences.png)

Los públicos pueden crearse o derivarse desde distintos orígenes como:

* Se crearon nuevas en [!DNL Experience Cloud]
* [!DNL Analytics] segmentos publicados en [!DNL Experience Cloud]
* [!DNL Audience Manager]

**Públicos en tiempo real vs. públicos históricos**

Todos los públicos, independientemente de su origen, son accesibles para los casos de uso de segmentación en tiempo real. Sin embargo, las audiencias compartidas desde Analytics en Audience Manager no se pueden utilizar para los procesos de segmentación en tiempo real. El sistema evalúa los públicos de dos maneras:

* Los públicos históricos de Analytics se evalúan cada cuatro horas. El tiempo total para procesar y compartir puede llevar hasta ocho horas. Los públicos históricos siempre incluyen los visitantes de retorno.
* Estos públicos provienen de Públicos de Experience Cloud y se evalúan en tiempo real.

## Cómo utilizan las aplicaciones los públicos

En la tabla siguiente se describe cómo se utilizan los públicos en las aplicaciones de Experience Cloud:

| Solución | Descripción |
|--- |--- |
| Públicos de Experience Cloud | Cree, administre y comparta audiencias de forma nativa con la Biblioteca de audiencias. Puede hacer lo siguiente:<ul><li>Utilice audiencias en tiempo real con atributos de análisis sin procesar.</li><li>Combine audiencias para crear composiciones, uniendo datos históricos y en tiempo real.</li><li>Consulte vistas gráficas del tamaño estimado de audiencias.</li></ul><br>Para obtener sugerencias sobre el tipo de público que desea crear, consulte [Opciones de creación de público](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=es). |
| Analytics | En la segmentación puede crear un segmento, combinarlo con un grupo de informes y, a continuación, publicar el segmento en Experience Cloud. Al publicar el segmento, aparece en Experience Cloud en la página [!DNL Audience Library]. (Consulte [Publicar segmentos en Experience Cloud](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=es) en la ayuda de [!DNL Analytics] para obtener más información). La audiencia también está disponible como audiencia de destino para una experiencia de campaña suministrada por [!DNL Adobe Target] y en [!DNL Audience Manager]. Después de compartir una audiencia de [!DNL Adobe Analytics] y seleccionarla para usarla en una campaña activa, los perfiles de visitantes que cumplen los criterios de definición de segmento de los últimos 90 días se envían a [!UICONTROL Audience Services]. El límite de públicos compartidos se ha aumentado a 75. Los públicos compartidos en Experience Cloud desde [!DNL Analytics] no pueden superar los 20 millones de miembros únicos. Además, debido al almacenamiento en caché, los grupos de informes que se eliminan en Analytics tardan 12 horas en desaparecer de Experience Cloud. |
| Mobile Services | Analice el tráfico móvil mediante la visualización radial en el informe [!UICONTROL Device Types]. |
| [!DNL Target] | El [servicio de ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=es) unifica el ID y los datos de los visitantes en un único perfil que se puede activar para utilizarlo en todas las aplicaciones. La casilla de verificación [!UICONTROL Publish to Experience Cloud] durante el proceso de creación de segmentos en Adobe Analytics permite que el segmento esté disponible en la biblioteca de audiencias personalizada de Adobe Target. Un segmento creado en [!DNL Analytics] o [!DNL Audience Manager] puede utilizarse para actividades en [!DNL Target]. Por ejemplo, puede crear actividades de campaña basadas en las métricas de conversión de [!DNL Analytics] y segmentos de públicos creados en [!DNL Analytics]. |
| [!DNL Audience Manager] | Los públicos compartidos están disponibles en la segmentación de [!DNL Audience Manager]. Todos los públicos de Experience Cloud están disponibles de forma nativa en [!DNL Audience Manager], que proporciona lo siguiente:<ul><li>Automatización integrada sobre cómo se comparten y consumen los flujos de trabajo de la aplicación</li><li>Destinos fuera del sitio</li><li>Modelado similar</li></ul> |
| Campaign | <ul><li>Importación de públicos compartidos de diferentes aplicaciones de Adobe Experience Cloud en Adobe Campaign.</li><li>Exportación de listas de destinatarios como públicos compartidos. Estos públicos compartidos pueden utilizarse con las diferentes aplicaciones de Adobe Experience Cloud que use.</li></ul> |
| Advertising Cloud | Utilice el público como destinatarios. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Una vez que un visitante se califica para el público compartido desde Analytics, deben pasar de 4 a 8 horas antes de que pueda realizarse alguna acción sobre esa información en [!DNL Target], Ad Cloud y Campaign Standard.

## Elementos de la interfaz de la biblioteca de públicos

[!DNL Experience Cloud] proporciona una biblioteca para crear y administrar audiencias, con identificación de audiencia nativa y en tiempo real.

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Audience Library]**

![Adición de un público en la biblioteca de públicos](assets/audience_library.png)


| Elemento | Descripción |
|--- |--- |
| Nuevo | [Crear un público](https://experienceleague.adobe.com/es/docs/core-services/interface/services/audiences/create). |
| Título y descripción | Un encabezado de columna que identifica y describe el público. |
| Autor | La persona que creó el segmento de público. |
| Fuente | Identifica dónde se creó el público.<ul><li>**Analytics:** Un segmento creado en Adobe Analytics y publicado en Experience Cloud.</li><li>**Experience Cloud:** público nuevo [creado en Públicos de Experience Cloud](https://experienceleague.adobe.com/es/docs/core-services/interface/services/audiences/create).</li><li>**Audience Manager:** los públicos creados en Audience Manager se muestran automáticamente en Públicos de Experience Cloud.</li></ul> |
| Tamaño actual | El tamaño de público actual. |
| Activo | El estado activo del segmento. |

{style="table-layout:auto"}

## Publicar audiencias desde Adobe Analytics

Consulte [Publicar segmentos en Experience Cloud](https://experienceleague.adobe.com/en/docs/analytics/components/segmentation/segmentation-workflow/seg-publish) en la documentación de Adobe Analytics para obtener más información.
