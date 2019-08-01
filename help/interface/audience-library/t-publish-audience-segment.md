---
description: Publique un segmento de audiencia de Analytics en Experience Cloud y Adobe Target para actividades de marketing para audiencias.
keywords: servicios principales
seo-description: Publique un segmento de audiencia de Analytics en Experience Cloud y Adobe Target para actividades de marketing para audiencias.
seo-title: Publicación de un segmento de audiencia de Analytics
solution: Experience Cloud
title: Publicación de un segmento de audiencia de Analytics
uuid: 4201dc22-4b79-457c-a614-949bba087617
translation-type: tm+mt
source-git-commit: b74e0a08b43dfa8e5b35c5a650d159a58485883c

---


# Publicación de un segmento de audiencia de Analytics

Publique un segmento de audiencia de Analytics en Experience Cloud y Adobe Target para actividades de marketing para audiencias.

1. En Analytics, [cree un segmento](https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_build.html).
1. On the Segment Builder, enable the **[!UICONTROL Publish this segment to the Experience Cloud]** option.

   ![](assets/ec_audience_example.png)

   | Elemento | Descripción |
   |--- |---|
   | Publicar este segmento en Experience Cloud (para &lt; nombre del grupo de informes &gt;) | Publica este segmento en Experience Cloud. Puede utilizar la audiencia para actividades de segmentación y marketing en Adobe Target, Audience Manager, Advertising Cloud, Campaign y Audience Analytics.<br>Los campos Título y Descripción son obligatorios para que se publique el segmento.<br>Cuando esta opción está activada, el título y la definición del segmento de audiencia se comparten, pero no los datos en sí. Cuando dicha audiencia está asociada con una actividad en Target, Analytics comienza a enviar ID para los visitantes que son aptos para esta audiencia de Experience Cloud y Target. En este punto, el nombre de audiencia y los datos correspondientes empiezan a mostrarse en la página de Audiencias de Experience Cloud.<br>Las audiencias compartidas en Experience Cloud desde Analytics no pueden superar los 20 millones de miembros de audiencia.<br>Debido al almacenamiento en caché, los grupos de informes que se eliminan en Analytics tardan 12 horas en desaparecer de Experience Cloud.<br>Para eliminar un segmento publicado en Experience Cloud, tiene que cancelarlo primero. To unpublish a segment, just **unclick** the checkbox that you used to publish it. **No puede** cancelar la publicación de un segmento que esté actualmente en uso por ninguna de las siguientes soluciones de Adobe: [!DNL Analytics] (en [!DNL Audience Analytics]), [!DNL Campaign]( [!DNL Advertising Cloud] para [!DNL Core Service] &amp; [!DNL Audience Manager] clientes) y todos los demás socios externos (para [!DNL Audience Manager] clientes). **** Puede cancelar la publicación de un segmento en uso [!DNL Target].<br>Una vez que un visitante se califica para la audiencia compartida desde Analytics, deben pasar de 24 a 48 horas antes de que pueda realizarse alguna acción sobre esa información en Target, Advertising Cloud y Campaign.Las audiencias de <br>**privacidad de los datos**<br> no se filtran según el estado de autenticación de un visitante. Si un visitante puede navegar por su sitio en los estados de autenticado y no autenticado, las acciones que se dan cuando un visitante no está autenticado todavía pueden hacer que un visitante se incluya en una audiencia. Consulte la [Información general de privacidad de Analytics](https://marketing.adobe.com/resources/help/en_US/reference/?f=c_Privacy_Overview) para comprender las implicaciones de privacidad completas del uso compartido de audiencias. |
   | Selección del periodo para la creación de audiencias | Tenga en cuenta que este es un periodo de tiempo **periódico**, no es fijo. |

1. Haga clic en **[!UICONTROL Guardar]**.
1. Vaya a [!DNL Adobe Target], haga clic en [!UICONTROL Audiencias].
1. En la página [!UICONTROL Audiencias], busque la audiencia procedente de Experience Cloud.

   Estas audiencias están disponibles para su uso en actividades.
