---
description: Obtenga información sobre cómo configurar CX Enterprise Déclencheur.
solution: Experience Cloud
title: Información general sobre Triggers
uuid: dab536e3-1969-4661-919e-5b15f423fecd
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 9dc26e2f-479b-49a5-93ce-b877559fea43
TQID: https://experienceleague.adobe.com/1R70ZEmKiP9VhhSRVCXHjGoJbOb7Mh8spKRm4FgNRPc
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
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 697
ht-degree: 71%

---

# CX Enterprise Déclencheur

[!UICONTROL Triggers] en CX Enterprise le permite identificar, definir y supervisar los comportamientos clave de los clientes y generar comunicación entre las varias aplicaciones para volver a atraer visitantes. Puede usar Triggers en las decisiones en tiempo real y la personalización.

Por ejemplo:

* Configure el remarketing rápido para abandonos del carro de compras o abandonos del carro de compras con productos eliminados
* Formularios y aplicaciones incompletos
* Cualquier acción o secuencia de acciones en el sitio

![Ejemplo de activador](../assets/trigger-abandonment-2.png)

>[!NOTE]
>
>Encontrará más información sobre el uso de [!UICONTROL Triggers] en [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/using-triggers-in-campaign.html?lang=es).

## Tipos de déclencheur

Generalmente, un Trigger (activador) puede tardar entre 15 y 90 minutos en iniciar una campaña de marketing. Este periodo varía según la implementación de la recopilación de datos, la carga en el canal, la configuración personalizada del activador definido y el flujo de trabajo en Adobe Campaign.

* Abandono: puede crear un activador que se desencadene cuando un visitante vea un producto, pero no agregue nada al carro de compra.**&#x200B;**
* **Acción:** puede crear activadores, por ejemplo, para que se desencadenen después de que los usuarios se suscriban a un boletín, de una suscripción por correo electrónico o cuando se soliciten tarjetas de crédito (confirmaciones). Si tiene un comercio minorista, puede crear un activador para visitantes que se suscriben a un programa de lealtad. Si se dedica al sector de los medios de comunicación y el entretenimiento, cree activadores para visitantes que vean un determinado programa y que podrían estar interesados en responder a una encuesta.
* **Inicio y fin de sesión:** cree un activador para los eventos de inicio y fin de sesión.

## Creación de un déclencheur de CX Enterprise

Cree un activador y configure sus condiciones. Por ejemplo, puede especificar los criterios de las reglas de un activador durante una visita, por ejemplo, métricas como Abandonos del carro de compras, o dimensiones como el nombre del producto. Cuando se cumplen las reglas, se ejecuta el activador.

>[!NOTE]
>
>Actualmente, existe un límite técnico de 100 activadores.

1. En CX Enterprise, haga clic en ![menú](../assets/menu-icon.png) y luego en **[!UICONTROL Data Collection/Launch]**.
1. En la tarjeta [!UICONTROL Triggers], haga clic en **[!UICONTROL Manage Triggers]**.
1. Haga clic en **[!UICONTROL New Trigger]** y luego especifique el tipo de déclencheur:

   ![Resultado de los pasos](../assets/add-trigger.png)

1. Configure el activador rellenando los siguientes campos y arrastrando métricas y dimensiones a los contenedores de la regla:

   | Elemento | Descripción |
   | --- | --- |
   | [!UICONTROL Name] | Nombre alternativo de este activador. |
   | [!UICONTROL Description] | Descripción de este activador, el uso que le dará, etc. |
   | [!UICONTROL Report Suite] | El [grupo de informes](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=es) de Analytics utilizado para este activador (Trigger). Esta configuración identifica los datos de sistema de informes que se van a utilizar. |
   | La visita debe incluir<br>La visita no debe incluir<br>un activador sin una acción posterior<br>Incluir metadatos | Puede definir criterios o comportamientos de los visitantes que quiera que se produzcan, así como comportamientos que no quiere que tengan lugar. Por ejemplo, las reglas de un activador sencillo de abandono del carro de compras podrían ser:<ul><li>La visita debe incluir: [!UICONTROL Cart Addition] (métrica) y [!UICONTROL Exists]. (Puede acotar aún más la regla con una vista de producto específica o con dimensiones como Tipos de explorador).</li><li>La visita no debe incluir: [!UICONTROL Checkout].</li><li>Activar tras no realizar una acción durante: 10 minutos.</li><li>[!UICONTROL Include Meta Data]: le permite agregar una dimensión [!DNL Campaign] en particular o variables que son relevantes para el comportamiento de un visitante. Este campo puede resultar útil para que Adobe Campaign cree el mensaje de correo electrónico adecuado para remarketing.</li></ul><br>Puede especificar la lógica [!UICONTROL Any], [!UICONTROL And] o [!UICONTROL Or] dentro de los contenedores o entre ellos, según los criterios que determine para la regla. |
   | [!UICONTROL Container] | [!UICONTROL Containers] es donde se establecen y almacenan las reglas, condiciones o filtros que definen un déclencheur. Si quiere que haya eventos que tengan lugar al mismo tiempo, póngalos en el mismo contenedor. De este modo, cada contenedor procesa de forma independiente a nivel de visita. Por ejemplo, si tiene dos contenedores unidos por el operador AND, puede esperar que se activen las reglas cuando dos visitas cumplan los requisitos. |
   | Inicie una nueva sesión después | Cree un activador para los eventos de inicio y fin de sesión. |

   {style="table-layout:auto"}

1. Haga clic en **[!UICONTROL Save]**.
1. Utilice Triggers para [realizar remarketing en tiempo real](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/about-adobe-experience-cloud-triggers.html?lang=es) en [!DNL Adobe Campaign].

## Ejemplos de activadores

Ejemplos de Déclencheur de CX Enterprise:

### Déclencheur de abandono del carro

Por ejemplo, en la siguiente página se muestran reglas que podría usar para un déclencheur de [!UICONTROL Cart Abandonment], según los productos que se vieron durante una visita.

![Activador de abandono del carro de compras](../assets/abandonment-trigger.png)

### Déclencheur de referente

El siguiente activador se desencadena cuando se produce una visita con el producto Botas para hombres y el referente de Facebook. Para que los dos criterios (*productos* y *referente*) se evalúen en la misma visita, se deben agregar al mismo contenedor.

![Activador de remitente del reenvío](../assets/fb-boots-promo.png)

