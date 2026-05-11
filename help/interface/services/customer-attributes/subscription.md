---
description: Obtenga información sobre cómo configurar suscripciones en  [!DNL Customer Attributes]  para Analytics y Target y activar una fuente de datos.
solution: Experience Cloud
title: Configurar suscripciones en  [!DNL Customer Attributes]
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
TQID: 'https://experienceleague.adobe.com/SVDhQ4Y2-CIJ7pVhapEqhu1gRkYSrPjmSI8-NejBddI'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id:id:
role_v2: id:
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f01d85af42b8f2c27dbada8f73546bc6fe4bf710
workflow-type: tm+mt
source-wordcount: 408
ht-degree: 47%

---

# Configurar suscripciones de atributos del cliente

Las suscripciones de [!DNL Customer Attributes] habilitan el flujo de datos de atributos del cliente entre CX Enterprise y las aplicaciones ([!DNL Analytics] y [!DNL Target]).

Por ejemplo, la suscripción de Adobe Analytics permite los datos de atributos en los informes. Si usa [!DNL Adobe Target], puede cargar atributos del cliente para el direccionamiento y la segmentación.

**Para configurar suscripciones y activar el origen de datos**

1. Busque el origen de datos en [!DNL Customer Attributes] para su edición:

   En [!DNL CX Enterprise], haga clic en **[!UICONTROL Apps]** ![menú](assets/menu-icon.png) > **[!DNL Customer Attributes]**.

1. En [!UICONTROL Edit Customer Attribute Source], haga clic en **[!UICONTROL File Upload]**.

1. Haga clic en **[!UICONTROL Configure Subscriptions]**.

   ![Configurar suscripciones en CX Enterprise](assets/configure-subscriptions.png)

1. Para activar el origen de atributos del cliente, haga clic en **[!UICONTROL Active]** y luego en **[!UICONTROL Save]**.

1. Para configurar una suscripción a [!DNL Analytics] o [!DNL Target], haga clic en **[!UICONTROL Configure]**.

   El ejemplo siguiente muestra una suscripción de [!DNL Target]:

   ![Resultado de los pasos](assets/subscription-target.png)

   | Elemento | Descripción |
   | --- | --- |
   | Solución | **Adobe Analytics**<br> Seleccione [!DNL Analytics], especifique los grupos de informes a los que desea recibir datos de atributos y los atributos que desea incluir.<br>**Adobe Target**<br> Puede cargar atributos del cliente para el direccionamiento y la segmentación. Esta característica es útil si desea establecer como objetivo una prueba basada en datos de atributos o hacer que los datos estén disponibles para la segmentación en Analytics.<br>Los datos de atributos del cliente cargados para un visitante están disponibles al iniciar sesión, en **[!DNL Target]** > **Audiencias**.<br>Se admiten múltiples fuentes de datos. Cuando configure ID de clientes en su sitio web, compruebe que al menos uno de los alias esté suscrito a [!DNL Target]. |
   | Grupo de informes (Adobe Analytics) | Los grupos de informes de Analytics.<br>No puede agregar más de un total de 10 grupos de informes a las suscripciones de Analytics dentro de un único origen de atributos. Al elegir qué grupos de informes incluir, tenga en cuenta las siguientes sugerencias:<ul><li>Elija grupos de informes que tengan un conjunto común de clientes autenticados. Si los clientes autenticados en un grupo de informes no se superponen con los clientes autenticados en otro grupo de informes, separe estos grupos de informes en diferentes fuentes de atributos.</li><li>Si es posible, los grupos de informes incluidos en un origen de atributos deben tener un volumen de tráfico similar.</li></ul><br>Si tiene más de 10 grupos de informes que tienen un conjunto de clientes autenticados en común, puede configurar orígenes de atributos del cliente adicionales, cada uno con hasta 10 grupos de informes. |
   | Atributos para incluir (Analytics y [!DNL Target]) | Atributos que desea enviar a la aplicación. <br>Al configurar suscripciones y seleccionar atributos, aplican los límites siguientes _por grupos de informes,_ según las aplicaciones que tenga:<ul><li>Foundation: 0</li><li>Select: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 en total</li><li>Premium: 200 por grupo de informes</li><li>[!DNL Target] Standard: 5</li><li>[!DNL Target] Premium: 200</li></ul><br>**Nota:** Cuando actualice a Analytics Premium, no podrá disponer de los atributos adicionales hasta haber transcurrido 24 horas. Durante este periodo, puede aparecer el error Máximas suscripciones a atributos. |

1. Haga clic en **[!UICONTROL Save]**.
