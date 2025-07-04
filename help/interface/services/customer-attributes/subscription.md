---
description: Obtenga más información acerca de las fuentes de datos de soluciones y de la configuración de suscripciones. Las suscripciones habilitan el flujo de datos de atributos del cliente entre Experience Cloud y las aplicaciones (Analytics y Target).
solution: Experience Cloud
title: Configuración de suscripciones
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 75%

---

# Configuración de suscripciones en Experience Cloud

Obtenga más información acerca de las fuentes de datos de aplicaciones y de la configuración de suscripciones. Las suscripciones habilitan el flujo de datos [!DNL customer attribute] entre Experience Cloud y las aplicaciones ([!DNL Analytics] y [!DNL Target]).

Por ejemplo, la suscripción de Adobe Analytics permite los datos de atributos en los informes. Si usa Adobe Target, puede cargar atributos del cliente para el direccionamiento y la segmentación.

**[!UICONTROL atributo del cliente Source]** > **[!UICONTROL Crear nuevo atributo del cliente Source]** > **[!UICONTROL Nuevo]**

![Configuración de suscripciones en Experience Cloud](assets/configure_subscription_page.png)

| Elemento | Descripción |
|--- |--- |
| Solución | **Adobe Analytics**<br> Seleccione [!DNL Analytics], especifique los grupos de informes a los que desea recibir datos de atributos y los atributos que desea incluir.<br>**Adobe Target**<br> Puede cargar atributos del cliente para el direccionamiento y la segmentación. Esta función es útil si desea direccionar una prueba basándose en los datos de atributos o hacer que los datos estén disponibles para la segmentación en Analytics.<br>Los datos de atributos del cliente cargados para un visitante están disponibles al iniciarse la sesión, en **[!DNL Target]** > **Públicos**.<br>Es posible utilizar múltiples orígenes de datos. Cuando configure ID de clientes en su sitio web, compruebe que al menos uno de los alias esté suscrito a [!DNL Target]. |
| Grupo de informes (Adobe Analytics) | Los grupos de informes de Analytics.<br>Como máximo puede agregar un total de 10 grupos de informes en suscripciones de Analytics desde un único origen de atributos. Al elegir qué grupos de informes incluir, tenga en cuenta las siguientes sugerencias:<ul><li>Elija grupos de informes que tengan un conjunto común de clientes autenticados. Si los clientes autenticados en un grupo de informes no se superponen con los clientes autenticados en otro grupo de informes, separe estos grupos de informes en diferentes fuentes de atributos.</li><li>Si es posible, los grupos de informes incluidos en un origen de atributos deben tener un volumen de tráfico similar.</li></ul><br>Si tiene más de 10 grupos de informes que tienen un conjunto de clientes autenticados en común, puede configurar orígenes de atributos del cliente adicionales, cada uno con hasta 10 grupos de informes. |
| atributos para incluir (Analytics y [!DNL Target]) | Atributos que desea enviar a la aplicación. <br>Al configurar suscripciones y seleccionar atributos, aplican los límites siguientes _por grupos de informes,_ según las aplicaciones que tenga:<ul><li>Foundation: 0</li><li>Select: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 en total</li><li>Premium: 200 por grupo de informes</li><li>[!DNL Target] Standard: 5</li><li>[!DNL Target] Premium: 200</li></ul><br>**Nota:** Cuando actualice a Analytics Premium, no podrá disponer de los atributos adicionales hasta haber transcurrido 24 horas. Durante este periodo, puede aparecer el error Máximas suscripciones a atributos. |

{style="table-layout:auto"}
