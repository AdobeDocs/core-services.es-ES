---
description: Obtenga información sobre cómo configurar suscripciones de atributos del cliente a Analytics y Target y activar una fuente de datos.
solution: Experience Cloud
title: Configuración de suscripciones
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
source-git-commit: fc60b49af0839769fdd8d18fd61863c8b28bbd57
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 65%

---

# Configurar suscripciones y activar la fuente de datos

Las suscripciones habilitan el flujo de datos de atributos del cliente entre Experience Cloud y las aplicaciones ([!DNL Analytics] y [!DNL Target]).

Por ejemplo, la suscripción de Adobe Analytics permite los datos de atributos en los informes. Si usa Adobe Target, puede cargar atributos del cliente para el direccionamiento y la segmentación.

**Para configurar suscripciones y activar el origen de datos**

1. Busque el origen de atributos del cliente para editarlo:

   En [!DNL Experience Cloud], haga clic en **[!UICONTROL Aplicaciones]** ![menú](assets/menu-icon.png) > **[!DNL Customer Attributes]**.

1. En [!UICONTROL Editar atributo del cliente Source], haga clic en **[!UICONTROL Cargar archivo]**.

1. Haga clic en **[!UICONTROL Configurar suscripciones]**.

   ![Configuración de suscripciones en Experience Cloud](assets/configure-subscriptions.png)

1. Para activar el origen de atributos del cliente, haga clic en **[!UICONTROL Activo]** y luego haga clic en **[!UICONTROL Guardar]**.

1. Para configurar una suscripción a [!DNL Analytics] o [!DNL Target], haga clic en **[!UICONTROL Configurar]**.

   El ejemplo siguiente muestra una suscripción de [!DNL Target]:

   ![Resultado de los pasos](assets/subscription-target.png)

   | Elemento | Descripción |
   |--- |--- |
   | Solución | **Adobe Analytics**<br> Seleccione [!DNL Analytics], especifique los grupos de informes a los que desea recibir datos de atributos y los atributos que desea incluir.<br>**Adobe Target**<br> Puede cargar atributos del cliente para el direccionamiento y la segmentación. Esta función es útil si desea direccionar una prueba basándose en los datos de atributos o hacer que los datos estén disponibles para la segmentación en Analytics.<br>Los datos de atributos del cliente cargados para un visitante están disponibles al iniciarse la sesión, en **[!DNL Target]** > **Públicos**.<br>Es posible utilizar múltiples orígenes de datos. Cuando configure ID de clientes en su sitio web, compruebe que al menos uno de los alias esté suscrito a [!DNL Target]. |
   | Grupo de informes (Adobe Analytics) | Los grupos de informes de Analytics.<br>Como máximo puede agregar un total de 10 grupos de informes en suscripciones de Analytics desde un único origen de atributos. Al elegir qué grupos de informes incluir, tenga en cuenta las siguientes sugerencias:<ul><li>Elija grupos de informes que tengan un conjunto común de clientes autenticados. Si los clientes autenticados en un grupo de informes no se superponen con los clientes autenticados en otro grupo de informes, separe estos grupos de informes en diferentes fuentes de atributos.</li><li>Si es posible, los grupos de informes incluidos en un origen de atributos deben tener un volumen de tráfico similar.</li></ul><br>Si tiene más de 10 grupos de informes que tienen un conjunto de clientes autenticados en común, puede configurar orígenes de atributos del cliente adicionales, cada uno con hasta 10 grupos de informes. |
   | Atributos para incluir (Analytics y [!DNL Target]) | Atributos que desea enviar a la aplicación. <br>Al configurar suscripciones y seleccionar atributos, aplican los límites siguientes _por grupos de informes,_ según las aplicaciones que tenga:<ul><li>Foundation: 0</li><li>Select: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 en total</li><li>Premium: 200 por grupo de informes</li><li>[!DNL Target] Standard: 5</li><li>[!DNL Target] Premium: 200</li></ul><br>**Nota:** Cuando actualice a Analytics Premium, no podrá disponer de los atributos adicionales hasta haber transcurrido 24 horas. Durante este periodo, puede aparecer el error Máximas suscripciones a atributos. |

1. Haga clic en **[!UICONTROL Guardar]**.
