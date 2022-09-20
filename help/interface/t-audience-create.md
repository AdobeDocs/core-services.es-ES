---
description: Obtenga información sobre cómo utilizar las reglas de atributos para crear una audiencia y definir una audiencia compuesta en Adobe Experience Cloud.
keywords: servicios principales
solution: Experience Cloud
title: Crear una audiencia
uuid: 7e622539-296e-4ff3-93b0-ec1c08b35429
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: b65a12f5-fa89-400a-b279-13c381cd6c22
source-git-commit: cb0f1fcfe0334f64ee38b659a0d4ef5c8dd3ab1e
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 100%

---

# Crear una audiencia

Obtenga información sobre cómo utilizar las reglas de atributos para crear una audiencia y definir una audiencia compuesta en Experience Cloud.

Este artículo le ayuda a lo siguiente:

* Crear una audiencia
* Crear una regla
* Usar reglas para definir una audiencia compuesta

El siguiente gráfico representa dos reglas en una audiencia compuesta.

![Dos reglas en una audiencia compuesta](assets/audience_sharing.png)

Cada círculo representa una regla que define la pertenencia a la audiencia. Los Visitantes que se califican como miembros en ambas reglas de audiencia se superponen para convertirse en la audiencia compuesta y definida.

>[!NOTE]
>
>La audiencia está completamente definida tras la recopilación de datos una vez completado el periodo especificado.

El siguiente ejemplo muestra cómo crear las reglas para una audiencia compuesta. Esta audiencia está compuesta por:

* Sección Hogar y jardín derivada de datos de página o datos de análisis sin procesar.
* Usuarios de Chrome y Safari derivados de un segmento de [!DNL Adobe Analytics] [publicado](audience-library.md#task_32FEEFE0B32E4E388CD4D892D727282A) en [!DNL Experience Cloud].

   ![Creación de reglas para una audiencia compuesta](assets/audience_create.png)

**Para crear una audiencia**

1. En [!DNL Experience Cloud], en [!DNL Experience Platform], seleccione **[!UICONTROL Personas]** > **[!UICONTROL Biblioteca de audiencias].**
1. En la página [!UICONTROL Audiencias], seleccione **[!UICONTROL Nuevo]**. ![Agregue](assets/add_icon_small.png)

   ![Resultado de los pasos](assets/audience_create_new.png)

1. En la página [!UICONTROL Crear audiencia], especifique un título y una descripción.
1. Dentro de [!UICONTROL Reglas], seleccione una fuente de atributos:

   * **[!UICONTROL Datos de Real-Time Analytics:]** datos de atributo derivados de solicitudes de imagen de Real-Time Analytics; incluyen datos tales como eVars y eventos. Debe seleccionar un grupo de informes al utilizar este origen de atributos y definir la dimensión o el evento que se va a incluir. Esta selección de grupo de informes proporciona la estructura de variables utilizada por el grupo de informes.
   >[!NOTE]
   >
   >Debido al almacenamiento en caché, los grupos de informes que se eliminan en Analytics tardan 12 horas en desaparecer de Experience Cloud.

   * **[!UICONTROL Experience Cloud:]** datos de atributos derivados a partir de los orígenes de [!DNL Experience Cloud]. Por ejemplo, pueden ser datos de segmentos de audiencia creados en [!DNL Analytics] o datos de [!DNL Audience Manager].

1. Defina las reglas de audiencia y seleccione **[!UICONTROL Guardar].**

>[!NOTE]
>
>Le recomendamos que se informe sobre las variables de implementación para definir reglas de audiencia.

En [!UICONTROL Reglas], defina las selecciones de atributos de *`Home & Garden`*:

* **[!UICONTROL Fuente de atributos:]** Datos de Analytics sin procesar
* **[!UICONTROL Grupo de informes:]** Grupo de informes 31
* Dimensión = **[!UICONTROL Tienda (Merch) (v6)]** > **[!UICONTROL igual a]** > **[!UICONTROL Hogar y jardín]**

![Selecciones de atributos en la biblioteca de audiencias](assets/home_garden.png)

Los *Visitantes de Chrome y Safari* son un segmento de audiencia compartido desde Analytics:

* **[!UICONTROL Fuente de atributos:]** Experience Cloud
* **[!UICONTROL Dimensión:]** Visitantes de Chrome y Safari

![Visitantes de Chrome y Safari](assets/chrome_safari.png)

Para comparar, podría añadir una regla *OR* para ver todos los visitantes de una sección del sitio como Patio y muebles.

![Regla OR para una audiencia](assets/audiences_rule_patio.png)

La regla resultante es una audiencia definida que incluye a los usuarios de Chrome y Safari que visitaron la sección Hogar y jardín. El segmento Patio y muebles proporciona una perspectiva adicional de todos los visitantes que visitan esa sección del sitio.

![Audiencia definida en Experience Cloud](assets/defined_audience.png)

* **Estimación histórica:** (Círculo con puntos) Representa reglas creadas según datos de [!DNL Analytics].
* **Audiencia real:** (Círculo sólido) cualquier regla creada que tenga 30 días de datos de Audience Manager. Cuando los datos de Audience Manager llegan a los 30 días, la línea se vuelve sólida y representa los números reales.

Una vez que la recopilación de datos se completa para el periodo especificado, los círculos se combinan para mostrar una audiencia definida.

Una vez guardada la audiencia, está disponible para otras aplicaciones. Por ejemplo, puede incluir una audiencia compartida en una actividad de Adobe Target.
