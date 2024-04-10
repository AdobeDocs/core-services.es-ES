---
title: "[!DNL Audience Library]"
description: Obtenga información sobre cómo administrar la traducción de datos sobre visitantes en segmentación de audiencia en Experience Cloud [!DNL Audience Library].
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
source-git-commit: 064f3c981b921fd5aec9b252b839d8b7f59b3dee
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 60%

---

# Públicos de Experience Cloud {#topic_679810123CAA4E0CA4FA3417FB0100C7}

El [!DNL Audience Library] muestra las audiencias en Experience Cloud. Las audiencias son recopilaciones de visitantes (una lista de [!DNL Experience Cloud] ID). Puede administrar la traducción de datos sobre visitantes en segmentación de audiencia. Como tal, crear y administrar públicos es similar a crear y utilizar segmentos. También puede compartir el segmento de público con productos y servicios de [!DNL Experience Cloud].

![Públicos de Experience Cloud](assets/audiences.png)

Los públicos pueden crearse o derivarse desde distintos orígenes como:

* Las nuevas se crean en [!DNL Experience Cloud]
* Segmentos de [!DNL Analytics] publicados en [!DNL Experience Cloud]
* [!DNL Audience Manager]

**Públicos en tiempo real vs. públicos históricos**

Todos los públicos, independientemente de su origen, son accesibles para los casos de uso de segmentación en tiempo real. Sin embargo, las audiencias compartidas desde Analytics en Audience Manager no se pueden utilizar para los procesos de segmentación en tiempo real. El sistema evalúa los públicos de dos maneras:

* Los públicos históricos de Analytics se evalúan cada cuatro horas. El tiempo total para procesar y compartir puede llevar hasta ocho horas. Los públicos históricos siempre incluyen visitantes de retorno.
* Las audiencias en tiempo real provienen de Audiencias de Experience Cloud y se evalúan en tiempo real.

## Cómo utilizan las aplicaciones los públicos {#concept_01EB9345C5344597BC94A864EDD38EE1}

En la tabla siguiente se describe cómo se utilizan los públicos en las aplicaciones de Experience Cloud:

| Solución | Descripción |
|--- |--- |
| Públicos de Experience Cloud | Cree, administre y comparta audiencias de forma nativa con [[!DNL Audience Library]](audience-library.md). Puede:<ul><li>Usar públicos en tiempo real mediante atributos de análisis sin procesar</li><li>Combinar públicos para crear composiciones, uniendo datos históricos y en tiempo real</li><li>Ver vistas gráficas del tamaño estimado de públicos</li></ul><br>Para obtener sugerencias sobre el tipo de audiencia que desea crear, consulte [Opciones de creación de audiencias](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=es). |
| Analytics | En la segmentación puede crear un segmento, combinarlo con un grupo de informes y luego publicarlo en el Experience Cloud. Al publicar el segmento, aparece en la [!DNL Audience Library] página en el Experience Cloud. (Consulte [Publicación de segmentos en el Experience Cloud](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=es) in [!DNL Analytics] ayuda para obtener más información). La audiencia también está disponible como audiencia de destino para una experiencia de campaña suministrada por [!DNL Adobe Target], y en [!DNL Audience Manager]. Después de compartir una audiencia de [!DNL Adobe Analytics]y seleccionarlo para utilizarlo en una campaña activa, los perfiles de visitantes que cumplen los criterios de definición de segmento de los últimos 90 días se envían a [!UICONTROL Servicios de audiencia]. El límite de públicos compartidas se ha aumentado a 75. Audiencias compartidas con el Experience Cloud desde [!DNL Analytics] no puede superar los 20 millones de miembros únicos. Además, debido al almacenamiento en caché, los grupos de informes que se eliminan en Analytics tardan 12 horas en desaparecer de Experience Cloud. |
| Mobile Services | Analice el tráfico móvil mediante la visualización radial en el informe [!UICONTROL Tipos de dispositivos]. |
| [!DNL Target] | El [servicio de ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=es) unifica el ID y los datos de los visitantes en un único perfil que se puede activar para utilizarlo en todas las aplicaciones. El [Publicar en Experience Cloud](audience-library.md) durante el proceso de creación de segmentos en Adobe Analytics, esta casilla de verificación permite que el segmento esté disponible en la biblioteca de audiencias personalizada de Adobe Target. Un segmento creado en [!DNL Analytics] o [!DNL Audience Manager] se puede usar para actividades en [!DNL Target]. Por ejemplo, puede crear actividades de campaña basadas en [!DNL Analytics] métricas de conversión de y segmentos de públicos creados en [!DNL Analytics]. |
| [!DNL Audience Manager] | Las audiencias compartidas están disponibles en [!DNL Audience Manager] segmentación. Todas las audiencias de los Experience Cloud están disponibles de forma nativa en [!DNL Audience Manager], que proporciona:<ul><li>Automatización integrada sobre cómo se comparten y consumen los flujos de trabajo de la aplicación</li><li>Destinos fuera del sitio</li><li>Modelado similar</li></ul> |
| Campaign | <ul><li>Importación de públicos compartidos de diferentes aplicaciones de Adobe Experience Cloud en Adobe Campaign.</li><li>Exportación de listas de destinatarios como públicos compartidos. Estos públicos compartidos pueden utilizarse con las diferentes aplicaciones de Adobe Experience Cloud que use.</li></ul> |
| Advertising Cloud | Utilice el público como destinatarios. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Una vez que un visitante se califica para el público compartido desde Analytics, deben pasar de 4 a 8 horas antes de que pueda realizarse alguna acción sobre esa información en [!DNL Target], Ad Cloud y Campaign Standard.

## Más ayuda: preguntas, sugerencias y casos de uso {#section_C7F151644D8A45F7B6FC54F58845635D}

| Ayuda con | Recurso |
|--- |--- |
| ¿No puede encontrar Públicos? | Compruebe que está aprovisionado. Consulte [Introducción: Activación de las aplicaciones en los servicios principales](core-services.md).<br>Vaya [aquí](https://adobe.allegiancetech.com/cgi-bin/qwebcorporate.dll?idx=X8SVES) para solicitar acceso a Perfiles y Públicos (formulario de aprovisionamiento de integraciones). |
| Foro | El [Foro de públicos](https://experienceleaguecommunities.adobe.com/t5/Adobe-Experience-Cloud-Audiences/ct-p/experience-cloud-audiences-community) es otro recurso para obtener ayuda con los públicos. |

{style="table-layout:auto"}

## Elementos de la interfaz de la biblioteca de públicos {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] proporciona una biblioteca para la creación y administración de públicos, con identificación de público nativa y en tiempo real.

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Biblioteca de públicos]**

![Adición de un público en la biblioteca de públicos](assets/audience_library.png)

| Elemento | Descripción |
|--- |--- |
| Nuevo | [Crear un público](audience-library.md). |
| Título y descripción | Un encabezado de columna que identifica y describe el público. |
| Autor | La persona que creó el segmento de público. |
| Fuente | Identifica dónde se creó el público.<ul><li>**Analytics:** Un segmento creado en Adobe Analytics, [publicado en el Experience Cloud](audience-library.md).</li><li>**Experience Cloud:** público nuevo [creado en Públicos de Experience Cloud](audience-library.md).</li><li>**Audience Manager:** Las audiencias creadas por Audience Manager se muestran automáticamente en Audiencias de Experience Cloud.</li></ul> |
| Tamaño actual | El tamaño de público actual. |
| Activo | El estado activo del segmento. |

{style="table-layout:auto"}
