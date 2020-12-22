---
description: Configuración de Triggers en Experience Cloud.
keywords: integrations;Triggers
seo-description: Configuración de Triggers en Experience Cloud.
seo-title: Triggers
solution: Experience Cloud
title: 'Información general sobre los activadores '
uuid: dab536e3-1969-4661-919e-5b15f423fecd
translation-type: tm+mt
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 99%

---


# Activadores

## Información general sobre Triggers {#topic_4F21FCE9A64E46E8B6D51F494FA652A7}

Triggers le permite identificar, definir y supervisar los comportamientos clave de los clientes y generar comunicación entre las varias soluciones para volver a atraer visitantes. Puede usar Triggers en las decisiones en tiempo real y la personalización.

* Configure el remarketing rápido para abandonos del carro de compras o abandonos del carro de compras con productos eliminados
* Formularios y aplicaciones incompletos
* Cualquier acción o secuencia de acciones en el sitio

![](assets/trigger-abandonment-2.png)

### Tipos de Triggers

Generalmente, un Trigger (activador) puede tardar entre 15 y 90 minutos en iniciar una campaña de marketing. Esto varía según la implementación de la recopilación de datos, la carga en el canal, la configuración personalizada del Trigger definido y el flujo de trabajo en Adobe Campaign.

* **Abandono:** puede crear un Trigger que se desencadene cuando un visitante vea un producto, pero no agregue nada al carro de compra.
* **Acción:** puede crear Triggers, por ejemplo, para que se desencadenen después de que los usuarios se suscriban a un boletín, de una suscripción por correo electrónico o cuando se soliciten tarjetas de crédito (confirmaciones). Si tiene un comercio minorista, puede crear un Trigger para visitantes que se suscriben a un programa de fidelidad. Si se dedica al sector de los medios de comunicación y el entretenimiento, cree Triggers para visitantes que vean un determinado programa y que podrían estar interesados en responder a una encuesta.
* **Inicio y fin de sesión:** cree un Trigger para los eventos de inicio y fin de sesión.

## Crear un Trigger de Experience Cloud {#task_821F37183AC045E5AC8EED20317598FE}

Cree un activador y configure sus condiciones. Por ejemplo, puede especificar los criterios de las reglas de un Trigger durante una visita, por ejemplo, métricas como Abandonos del carro de compras, o dimensiones como el nombre del producto. Cuando se cumplen las reglas, se ejecuta el Trigger.

>[!NOTE]
>
>Actualmente, existe un límite técnico de 100 Triggers.

1. En Experience Cloud, haga clic en ![](assets/menu-icon.png) y, a continuación, en **[!UICONTROL Launch]**.
2. Localice la tarjeta [!UICONTROL Triggers] y después haga clic en **[!UICONTROL Manage Triggers]**.
3. Haga clic en **[!UICONTROL Nuevo Trigger]** y después especifique el tipo de Trigger:

   ![Resultado de los pasos](assets/add-trigger.png)

4. Configure el Trigger rellenando los siguientes campos y arrastrando métricas y dimensiones a los contenedores de la regla:

   | Elemento | Descripción |
   |--- |--- |
   | Nombre | Nombre alternativo de este Trigger. |
   | Descripción | Descripción de este Trigger, el uso que le dará, etc. |
   | Grupo de informes | El [grupo de informes](https://docs.adobe.com/content/help/es-ES/analytics/admin/manage-report-suites/report-suites-admin.html) de Analytics utilizado para este activador (Trigger). Esta configuración identifica los datos de sistema de informes que se van a utilizar. |
   | La visita debe incluir<br>La visita no debe incluir<br>un Trigger sin una acción posterior<br>Incluir metadatos | Puede definir criterios o comportamientos de los visitantes que quiera que se produzcan, así como comportamientos que no quiere que tengan lugar.  Por ejemplo, las reglas de un Trigger sencillo de abandono del carro de compras podrían ser:<ul><li>La visita debe incluir: Adición al carro (métrica) y Existe. (Puede acotar aún más la regla con una vista de producto específica o con dimensiones como Tipos de explorador).</li><li>La visita no debe incluir: Cierre de compra.</li><li>Activar tras no realizar una acción durante: 10 minutos.</li><li>Include Meta Data: le permite agregar una dimensión de Campaign determinada o variables que resultan relevantes para el comportamiento de un visitante. Este campo puede resultar útil para que Adobe Campaign cree el mensaje de correo electrónico adecuado para remarketing.</li></ul><br>Puede especificar una lógica Cualquiera (Any), Y (And) u O (Or) entre contenedores, según los criterios que determine para la regla. |
   | Contenedor | Los contenedores se encuentran en el lugar donde se establecen y almacenan las reglas, condiciones o filtros que definen un Trigger. Si quiere que haya eventos que tengan lugar al mismo tiempo, póngalos en el mismo contenedor. De este modo, cada contenedor procesa de forma independiente a nivel de visita.  Por ejemplo, si tiene dos contenedores unidos por el operador Y, puede esperar que se activen las reglas cuando dos visitas cumplan los requisitos. |
   | Inicie una nueva sesión después | Cree un Trigger para los eventos de inicio y fin de sesión. |

5. Haga clic en **[!UICONTROL Guardar]**.
6. Utilice Triggers para [realizar remarketing en tiempo real](https://docs.adobe.com/content/help/es-ES/campaign-standard/using/integrating-with-adobe-cloud/working-with-campaign-and-triggers/about-adobe-experience-cloud-triggers.html) en [!DNL Adobe Campaign].

### Ejemplos de Triggers

Ejemplos de Triggers de Experience Cloud:

#### Trigger de abandono del carro de compras

Por ejemplo, en la siguiente página se muestran reglas que podría usar para un Trigger de abandono del carro de compras en función de los productos que se han visto durante una visita.

![](assets/abandonment-trigger.png)

#### Trigger referente

El siguiente Trigger se dispara cuando se produce una visita con el producto Botas para hombres y el referente de Facebook. Para que los dos criterios (*productos* y *remitente del reenvío*) se evalúen en la misma visita, se deben agregar al mismo contenedor.

![](assets/fb-boots-promo.png)
