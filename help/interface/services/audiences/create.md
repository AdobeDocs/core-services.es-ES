---
title: Cómo crear una audiencia en la biblioteca de audiencias
description: Descubra cómo utilizar las reglas de atributos para crear una audiencia que se pueda compartir en la Biblioteca de audiencias. Aprenda a configurar una regla y definir una audiencia compuesta.
solution: Experience Cloud
uuid: 7e622539-296e-4ff3-93b0-ec1c08b35429
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: b65a12f5-fa89-400a-b279-13c381cd6c22
TQID: 'https://experienceleague.adobe.com/-zJW08nRR0XHxI8ink2lZt-R44irL2pMyWdqHsZQoUg'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id:id:
role_v2: id:
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f01d85af42b8f2c27dbada8f73546bc6fe4bf710
workflow-type: tm+mt
source-wordcount: 515
ht-degree: 60%

---

# Crear un público

En [!UICONTROL Audience Library], puede utilizar reglas de atributos para crear una audiencia y definir una audiencia compuesta para compartirla en aplicaciones de CX Enterprise.

Este artículo le ayuda a lo siguiente:

* Crear un público
* Crear una regla
* Usar reglas para definir un público compuesto

El siguiente gráfico representa dos reglas en un público compuesto.

![Dos reglas en un público compuesto](assets/audience_sharing.png)

Cada círculo representa una regla que define el abono al público. Los Visitantes que se califican como miembros en ambas reglas de público se superponen para convertirse en el público compuesto y definido.

>[!NOTE]
>
>El público está completamente definido tras la recopilación de datos una vez completado el periodo especificado.

El siguiente ejemplo muestra cómo crear las reglas para un público compuesto. Este público está compuesto por:

* Sección Hogar y jardín derivada de datos de página o datos de análisis sin procesar.
* Usuarios de Chrome y Safari derivados de un segmento [publicado](overview.md) en [!DNL CX Enterprise].[!DNL Adobe Analytics]

  ![Creación de reglas para un público compuesto](assets/audience_create.png)

**Para crear un público**

1. Haga clic en [!DNL CX Enterprise] aplicaciones (![icono de aplicaciones](assets/apps-icon.png)) y, a continuación, haga clic en **[!UICONTROL People]** > **[!UICONTROL Audience Library].**

1. En la página [!UICONTROL Audiences], haga clic en **[!UICONTROL New]**. ![Nueva audiencia](assets/add_icon_small.png)

   ![Crear un público](assets/audience_create_new.png)

1. En la página [!UICONTROL Create New Audience], complete los campos **[!UICONTROL Title]** y **[!UICONTROL Description]**.
1. En [!UICONTROL Rules], seleccione un grupo de informes de referencia y, a continuación, un origen de atributos:

   * **[!UICONTROL Real-Time Analytics Data:]** (o datos sin procesar) Son datos de atributo derivados de solicitudes de imagen de Real-Time Analytics. Incluye eVars y eventos. Debe seleccionar un grupo de informes al utilizar este origen de atributos y definir la dimensión o el evento que se va a incluir. Esta selección de grupo de informes proporciona la estructura de variables utilizada por el grupo de informes.

     >[!NOTE]
     >
     >Debido al almacenamiento en caché, los grupos de informes eliminados en Analytics tardan 12 horas en desaparecer de CX Enterprise.

   * **[!UICONTROL CX Enterprise:]** datos de atributo derivados de [!DNL CX Enterprise] orígenes. Por ejemplo, pueden ser datos de segmentos de público creados en [!DNL Analytics] o datos de [!DNL Audience Manager].

1. Defina las reglas de audiencia y haga clic en **[!UICONTROL Save].**

**Ejemplo: definir reglas para la audiencia compuesta**

>[!NOTE]
>
>Le recomendamos que se informe sobre las variables de implementación para definir reglas de público.

En [!UICONTROL Rules], defina las selecciones de atributos *`Home & Garden`*:

* **[!UICONTROL Attribute Source:]** datos sin procesar de Analytics
* **[!UICONTROL Report Suite:]** grupo de informes 31
* Dimension = **[!UICONTROL Store (Merch) (v6)]** > **[!UICONTROL Equals]** > **[!UICONTROL Home & Garden]**

![Selecciones de atributos en la biblioteca de públicos](assets/home_garden.png)

Los *Visitantes de Chrome y Safari* son un segmento de público compartido desde Analytics:

* **[!UICONTROL Attribute Source:]** CX Enterprise
* **[!UICONTROL Dimension:]** visitantes de Chrome y Safari

![Visitantes de Chrome y Safari](assets/chrome_safari.png)

Para comparar, podría añadir una regla *OR* para ver todos los visitantes de una sección del sitio como Patio y muebles.

![Regla OR para un público](assets/audiences_rule_patio.png)

La regla resultante es un público definido que incluye a los usuarios de Chrome y Safari que visitaron la sección Hogar y jardín. El segmento Patio y muebles proporciona una perspectiva adicional de todos los visitantes que visitan esa sección del sitio.

![Audiencia definida en CX Enterprise](assets/defined_audience.png)

* **Estimación histórica:** (Círculo con puntos) Representa reglas creadas según datos de [!DNL Analytics].
* **Audiencia real:** (Círculo sólido) cualquier regla creada que tenga 30 días de datos de Audience Manager. Cuando los datos de Audience Manager llegan a los 30 días, la línea se vuelve sólida y representa los números reales.

Una vez que la recopilación de datos se completa para el periodo especificado, los círculos se combinan para mostrar un público definido.

Una vez guardada la audiencia, está disponible para otras aplicaciones de CX Enterprise. Por ejemplo, puede incluir una audiencia compartida en una [actividad](https://experienceleague.adobe.com/es/docs/target/using/activities/activities) de Adobe Target.
