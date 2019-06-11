---
description: Cómo configurar Experience Cloud Triggers.
keywords: integraciones; Desencadenadores
seo-description: Cómo configurar Experience Cloud Triggers.
seo-title: Triggers
solution: Marketing Cloud
title: Triggers
uuid: dab 536 e 3-1969-4661-919 e -5 b 15 f 423 fecd
translation-type: tm+mt
source-git-commit: 8ec57774743e8c32a17f18ae6dfe98c0767297a6

---


# Triggers

## Información general de activadores {#topic_4F21FCE9A64E46E8B6D51F494FA652A7}

*Los activadores* le permiten identificar, definir y supervisar comportamientos clave de consumidores, y luego generar comunicación entre soluciones para volver a involucrar a los visitantes. Puede usar activadores en las decisiones en tiempo real y la personalización.

* Configurar remarketing rápido para abandonos del carrito, con o sin productos eliminados
* Formularios y solicitudes incompletos
* Cualquier acción o secuencia de acciones en el sitio

![](assets/trigger-abandonment-2.png)

**Tipos de activadores**

Generalmente, un activador puede tardar entre 15 y 90 minutos en iniciar una campaña de marketing. Esto varía según la implementación de la recopilación de datos, la carga en el canal, la configuración personalizada del activador definido y el flujo de trabajo en Adobe Campaign.

* **Abandono:** puede crear un activador que se desencadene cuando un visitante vea un producto, pero no agregue nada al carro de compra. Configurar [la puntuación de tendencia](../activation/triggers.md#concept_A506150674AD45DB98D3CC07E560D334) para comprender la tendencia de los clientes a no abandonar un carro de compras.
* **Acción:** puede crear activadores, por ejemplo, para que se desencadenen después de que los usuarios se suscriban a un boletín, de una suscripción por correo electrónico o cuando se soliciten tarjetas de crédito (confirmaciones). Si tiene un comercio minorista, puede crear un activador para visitantes que se suscriben a un programa de fidelidad. Si se dedica al sector de los medios de comunicación y el entretenimiento, cree activadores para visitantes que vean un determinado programa y que podrían estar interesados en responder a una encuesta.
* **Inicio y fin de sesión:** cree un activador para los eventos de inicio y fin de sesión.

## Crear un activador de Experience Cloud {#task_821F37183AC045E5AC8EED20317598FE}

Cree un activador de abandono y configure las condiciones del activador y de la puntuación de tendencia. Por ejemplo, puede especificar los criterios de las reglas de un activador durante una visita, por ejemplo, métricas como Abandonos del carro de compras, o dimensiones como el nombre del producto. Cuando se cumplen las reglas, se ejecuta el activador.

<!-- t_create-trigger.xml -->

>[!NOTE]
>
>Actualmente existe un límite técnico de 100 activadores.

1. En Experience Cloud, haga clic en ![](assets/menu-icon.png)y luego en **[!UICONTROL Activation]**.
1. Localice la tarjeta [!UICONTROL Activadores]**y después haga clic en[!UICONTROL Launch]**.

   ![Resultado de paso](assets/activation-triggers.png)

1. Haga clic **[!UICONTROL en Nuevo activador]** y, a continuación, especifique el tipo de activador:

   ![Resultado de paso](assets/add-trigger.png)

1. Configure el activador rellenando los siguientes campos y arrastrando métricas y dimensiones a los contenedores de la regla:

   | Elemento | Descripción |
   |--- |--- |
   | Nombre | Nombre alternativo de este activador. |
   | Descripción | Descripción de este activador, el uso que le dará, etc. |
   | Report Suite | El [grupo de informes](https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/report-suites.html) de Analytics utilizado para este activador. Este ajuste identifica los datos de informes que se van a utilizar. |
   | Visit must include<br>Visit must not includrawigger<br>after no actioninclude<br>meta data | Puede definir criterios o comportamientos de los visitantes que quiera que se produzcan, así como comportamientos que no quiere que tengan lugar.  Por ejemplo, las reglas de un activador sencillo de abandono del carro de compras podrían ser:<ul><li>La visita debe incluir: Adición al carro de compras (métrica) y Existe. (Puede acotar aún más la regla con una vista de producto específica o con dimensiones como Tipos de explorador).</li><li>La visita no debe incluir: Cierre de compra.</li><li>Activar después de ninguna acción para: 10 minutos.</li><li>Include Meta Data: le permite agregar una dimensión de Campaign determinada o variables que resultan relevantes para el comportamiento de un visitante. Este campo puede resultar útil para que Adobe Campaign cree el mensaje de correo electrónico adecuado para remarketing.</li></ul><br>Puede especificar Cualquier lógica, Y o O, dentro o entre contenedores, según los criterios que determine para la regla. |
   | Contenedor | Los contenedores se encuentran en el lugar donde se establecen y almacenan las reglas, condiciones o filtros que definen un activador. Si quiere que haya eventos que tengan lugar al mismo tiempo, póngalos en el mismo contenedor. De este modo, cada contenedor procesa de forma independiente a nivel de visita.  Por ejemplo, si tiene dos contenedores unidos por el operador Y, puede esperar que las reglas se califiquen cuando dos visitas cumplan los requisitos. |
   | Iniciar nueva sesión después de | Cree un activador para los eventos de inicio y fin de sesión. |

1. (Opcional) En los activadores de abandono, puede aplicar [Puntuación de tendencia](../activation/triggers.md#concept_A506150674AD45DB98D3CC07E560D334).

   ![Resultado de paso](assets/propensity-scoring.png)

1. Haga clic en **[!UICONTROL Guardar]**.
1. Utilice activadores para [remercadotecnia en tiempo real](https://docs.campaign.adobe.com/doc/standard/en/EMA_Transactional_messaging_Marketing_Cloud_Triggers.html) en [!DNL Adobe Campaign].

### Ejemplos de activadores

**Activador de abandono del carro de compras**

Por ejemplo, en la siguiente página se muestran reglas que podría usar para un activador de abandono del carro de compras en función de los productos que se han visto durante una visita.

![](assets/abandonment-trigger.png)

**Activador referente**

El siguiente activador se dispara cuando se produce una visita con el producto Botas para hombres y el referente de Facebook. Para que los dos criterios ( *productos* y *referente*) para evaluarlos en la misma visita, deben agregarse al mismo contenedor.

![](assets/fb-boots-promo.png)

## Puntuación de tendencia {#concept_A506150674AD45DB98D3CC07E560D334}

<!-- propensity-scoring.xml -->

Comprenda la tendencia de los clientes a regresar después de haber abandonado un carro de compras. La puntuación de tendencia está integrada en Experience Cloud Triggers y se encuentra disponible para los activadores de abandono.

![Resultado de paso](assets/propensity-scoring.png)

Por ejemplo, algunos clientes abandonan los carros de compras para aprovechar los incentivos que reciben por correo electrónico para regresar al carro de compras. Para reducir la pérdida de ingresos, el algoritmo de Puntuación de tendencia ayuda a identificar a los usuarios relevantes que abandonan los carros de compras y probablemente no regresarían de no ser por el incentivo.

Puede:

* Evitar la sobreexposición de los clientes al remarketing.
* Identificar a los usuarios adecuados que abandonaron el carro de compras y asignar su actividad al mensaje adecuado.
* Aumentar los ingresos determinando qué clientes regresarán y cuáles no.

## El valor de la puntuación de tendencia {#section_CA99874A25434CC0BF01D0DA61608889}

Puede realizar una búsqueda de datos para identificar comportamientos o patrones ocultos en los datos. En concreto, la puntuación de tendencia le ayuda a identificar grupos de clientes similares que utilizan medios más específicos y objetivos en lugar de una segmentación o filtrado sencillos. Además, la puntuación de tendencia le permite crear funciones de predicción para identificar el comportamiento de clientes de gran valor para su empresa.

Una vez identificado el público de gran valor, puede motivarlo a participar para conseguir el máximo efecto. Por ejemplo, si su empresa presta servicios a otras empresas, podría tener posibles clientes a los que realizar llamadas comerciales para, posteriormente, puntuar a dichos posibles clientes e identificar la probabilidad de convertir sin conexión. Dado que todos los posibles clientes generan un aumento de costes, crear un incentivo para identificar a los clientes potenciales que muestran la mayor probabilidad de convertir una venta es la forma más eficaz y económica de concentrar sus recursos.

La puntuación de tendencia permite identificar los factores más importantes a la hora de predecir una puntuación concreta o aumentar la probabilidad de que se produzca un evento, pero también se puede aplicar para responder a preguntas específicas:

* ¿El cliente va a realizar una conversión?
* ¿El cliente va a responder a un correo electrónico?
* ¿El cliente va a volver a comprar?

La puntuación de tendencia le permite responder a estas preguntas e identificar a aquellos visitantes que muestren una inclinación a realizar una acción que posteriormente se podrá elaborar y puntuar.
