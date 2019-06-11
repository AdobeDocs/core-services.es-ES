---
description: Publique un segmento de audiencia de Analytics en Experience Cloud y Adobe Target para actividades de marketing para audiencias.
keywords: servicios principales
seo-description: Publique un segmento de audiencia de Analytics en Experience Cloud y Adobe Target para actividades de marketing para audiencias.
seo-title: Publicación de un segmento de audiencia de Analytics
solution: Experience Cloud
title: Publicación de un segmento de audiencia de Analytics
uuid: 4201 dc 22-4 b 79-457 c-a 614-949 bba 087617
translation-type: tm+mt
source-git-commit: 85879d92104d8b6d739fb4d17dc8cfb7483a9343

---


# Publicación de un segmento de audiencia de Analytics

Publique un segmento de audiencia de Analytics en Experience Cloud y Adobe Target para actividades de marketing para audiencias.

1. En Analytics, [cree un segmento](https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_build.html).
1. En el Generador de segmentos, active **[!UICONTROL la opción Convertir en audiencia]** de Experience Cloud.

   ![](assets/ec_audience_example.png)

   | Elemento | Descripción |
   |--- |---|
   | Conversión de audiencias a audiencias de Experience Cloud (para &lt;nombre del grupo de informes&gt;) | Publica este segmento en Experience Cloud. Puede utilizar la audiencia para actividades de marketing en Adobe Target y la segmentación en Audience Manager.<br>Los campos Título y Descripción son obligatorios para que se publique el segmento.<br>Cuando esta opción está activada, el título y la definición del segmento de audiencia se comparten, pero no los datos en sí. Cuando dicha audiencia está asociada con una actividad en Target, Analytics comienza a enviar ID para los visitantes que son aptos para esta audiencia de Experience Cloud y Target. En este punto, el nombre de audiencia y los datos correspondientes empiezan a mostrarse en la página de Audiencias de Experience Cloud.<br>Las audiencias compartidas en Experience Cloud desde Analytics no pueden superar los 20 millones de miembros de la audiencia.<br>Debido al almacenamiento en caché, los grupos de informes eliminados en Analytics tardan 12 horas en desaparecer de Experience Cloud.<br>En Analytics, puede editar o eliminar un segmento publicado. Si el segmento se encuentra en uso, aparece un mensaje de advertencia al editar un segmento. No puede eliminar un segmento publicado que Adobe Target esté usando.<br>Cuando un visitante cumple los requisitos de la audiencia compartida desde Analytics, hay un retraso de 24 a 48 horas antes de que dicha información sea procesable en Target, Advertising Cloud y Campaign.<br>**Privaciónlas audiencias**<br>no se filtran según el estado de autenticación de un visitante. Si un visitante puede navegar por su sitio en los estados de autenticado y no autenticado, las acciones que se dan cuando un visitante no está autenticado todavía pueden hacer que un visitante se incluya en una audiencia. Consulte la [Información general de privacidad de Analytics](https://marketing.adobe.com/resources/help/en_US/reference/?f=c_Privacy_Overview) para comprender las implicaciones de privacidad completas del uso compartido de audiencias. |
   | Selección del periodo para la creación de audiencias | Tenga en cuenta que este es un periodo de tiempo **periódico**, no es fijo. |

1. Haga clic en **[!UICONTROL Guardar]**.
1. Acceso [!DNL Adobe Target], haga clic [!UICONTROL en Audiencias].
1. En la página [!UICONTROL Audiencias] , ubique la audiencia procedente de Experience Cloud.

   Estas audiencias están disponibles para su uso en actividades.
