---
description: Obtenga más información sobre las fuentes de datos de soluciones y de la configuración de suscripciones. Las Suscripciones habilitan el flujo de datos de atributos del cliente entre Experience Cloud y las soluciones (Analytics y Target).
keywords: Customer Attributes;core services
seo-description: Obtenga más información sobre las fuentes de datos de soluciones y de la configuración de suscripciones. Las Suscripciones habilitan el flujo de datos de atributos del cliente entre Experience Cloud y las soluciones (Analytics y Target).
seo-title: Configurar suscripciones
solution: Experience Cloud
title: Configurar suscripciones
uuid: f74a8155-0a21-46b3-9b1e-4c838f72f24f
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 93%

---


# Configurar suscripciones

Obtenga más información sobre las fuentes de datos de soluciones y de la configuración de suscripciones. Las Suscripciones habilitan el flujo de datos de atributos del cliente entre Experience Cloud y las soluciones (Analytics y [!DNL Target]).

Por ejemplo, la suscripción de Adobe Analytics permite los datos de atributos en los informes. Si utiliza Adobe Target, puede cargar Atributos del cliente para objetivos y segmentación.

**[!UICONTROL Origen de atributos del cliente]** > **[!UICONTROL Crear un nuevo origen de atributos del cliente]** > **[!UICONTROL Nuevo]**

![](assets/configure_subscription_page.png)

| Elemento | Descripción |
|--- |--- |
| Solución | **Adobe Analytics **<br>Seleccione Analytics, especifique los grupos de informes sobre los que quiere recibir datos de atributos y los atributos que desea incluir.<br>**Adobe**<br>TargetPuede cargar atributos de cliente para segmentación y segmentación. Esta función es útil si desea direccionar una prueba basándose en los datos de atributos o hacer que los datos estén disponibles para la segmentación en Analytics.<br>Los datos de atributos del cliente cargados para un visitante están disponibles al iniciarse la sesión, en **[!DNL Target]**>** Audiencias **.<br>Es posible utilizar múltiples orígenes de datos. Cuando [configure ID de clientes](../core-services/core-services.md) en su sitio web, compruebe que al menos uno de los alias esté suscrito a [!DNL Target]. |
| Grupo de informes (Analytics) | Los grupos de informes de Analytics.<br>Como máximo puede agregar un total de 10 grupos de informes en suscripciones de Analytics desde un único origen de atributos. Al elegir qué grupos de informes incluir, tenga en cuenta las siguientes sugerencias:<ul><li>Elija grupos de informes que tengan un conjunto común de clientes autenticados. Si los clientes autenticados en un grupo de informes no se superponen con los clientes autenticados en otro grupo de informes, separe estos grupos de informes en diferentes fuentes de atributos.</li><li>Si es posible, los grupos de informes incluidos en un origen de atributos deben tener un volumen de tráfico similar.</li></ul><br>Si tiene más de 10 grupos de informes que tienen un conjunto de clientes autenticados en común, puede configurar orígenes de atributos del cliente adicionales, cada uno con hasta 10 grupos de informes. |
| Atributos para incluir (Analytics y [!DNL Target]) | Atributos que desea enviar a la solución. <br>Al configurar suscripciones y seleccionar atributos grupo de informes, aplican los límites siguientes _por grupos de informes_, según la solución:<ul><li>Foundation: 0</li><li>Select: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 en total</li><li>Premium: 200 por grupo de informes</li><li>[!DNL Target] Standard: 5</li><li>[!DNL Target] Premium: 200</li></ul><br>**Nota:** Cuando actualice a Analytics Premium, no podrá disponer de los atributos adicionales hasta haber transcurrido 24 horas. Durante este periodo, puede aparecer el error Máximas suscripciones a atributos. |
