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
source-git-commit: c98084e3960e40ae28e55050ce0727abce94ba0c
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 65%

---

# Crear un público

En [!UICONTROL Biblioteca de audiencias], puede usar reglas de atributos para crear una audiencia y definir una audiencia compuesta para compartir en aplicaciones de Experience Cloud.

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
* Usuarios de Chrome y Safari derivados de un segmento [!DNL Adobe Analytics]publicado[ en ](overview.md).[!DNL Experience Cloud]

  ![Creación de reglas para un público compuesto](assets/audience_create.png)

**Para crear un público**

1. Haga clic en [!DNL Experience Cloud] aplicaciones (![Icono de aplicaciones](assets/apps-icon.png)) y, a continuación, haga clic en **[!UICONTROL Personas]** > **[!UICONTROL Biblioteca de audiencias].**

1. En la página [!UICONTROL Audiencias], haga clic en **[!UICONTROL Nuevo]**. ![Nueva audiencia](assets/add_icon_small.png)

   ![Crear un público](assets/audience_create_new.png)

1. En la página [!UICONTROL Crear nueva audiencia], complete los campos **[!UICONTROL Título]** y **[!UICONTROL Descripción]**.
1. En [!UICONTROL Reglas], seleccione un grupo de informes de referencia y, a continuación, un origen de atributos:

   * **[!UICONTROL Datos de Real-Time Analytics:]** (o datos sin procesar) Estos son datos de atributo derivados de solicitudes de imagen de Real-Time Analytics. Incluye eVars y eventos. Debe seleccionar un grupo de informes al utilizar este origen de atributos y definir la dimensión o el evento que se va a incluir. Esta selección de grupo de informes proporciona la estructura de variables utilizada por el grupo de informes.

   >[!NOTE]
   >
   >Debido al almacenamiento en caché, los grupos de informes que se eliminan en Analytics tardan 12 horas en desaparecer de Experience Cloud.

   * **[!UICONTROL Experience Cloud:]** datos de atributo derivados de [!DNL Experience Cloud] orígenes. Por ejemplo, pueden ser datos de segmentos de público creados en [!DNL Analytics] o datos de [!DNL Audience Manager].

1. Defina las reglas de público y haga clic en **[!UICONTROL Guardar].**

**Ejemplo: definir reglas para la audiencia compuesta**

>[!NOTE]
>
>Le recomendamos que se informe sobre las variables de implementación para definir reglas de público.

En [!UICONTROL Reglas], defina las selecciones de atributos de *`Home & Garden`*:

* **[!UICONTROL Fuente de atributos:]** Datos de Analytics sin procesar
* **[!UICONTROL Grupo de informes:]** Grupo de informes 31
* Dimensión = **[!UICONTROL Tienda (Merch) (v6)]** > **[!UICONTROL igual a]** > **[!UICONTROL Hogar y jardín]**

![Selecciones de atributos en la biblioteca de públicos](assets/home_garden.png)

Los *Visitantes de Chrome y Safari* son un segmento de público compartido desde Analytics:

* **[!UICONTROL Fuente de atributos:]** Experience Cloud
* **[!UICONTROL Dimensión:]** Visitantes de Chrome y Safari

![Visitantes de Chrome y Safari](assets/chrome_safari.png)

Para comparar, podría añadir una regla *OR* para ver todos los visitantes de una sección del sitio como Patio y muebles.

![Regla OR para un público](assets/audiences_rule_patio.png)

La regla resultante es un público definido que incluye a los usuarios de Chrome y Safari que visitaron la sección Hogar y jardín. El segmento Patio y muebles proporciona una perspectiva adicional de todos los visitantes que visitan esa sección del sitio.

![Público definido en Experience Cloud](assets/defined_audience.png)

* **Estimación histórica:** (Círculo con puntos) Representa reglas creadas según datos de [!DNL Analytics].
* **Audiencia real:** (Círculo sólido) cualquier regla creada que tenga 30 días de datos de Audience Manager. Cuando los datos de Audience Manager llegan a los 30 días, la línea se vuelve sólida y representa los números reales.

Una vez que la recopilación de datos se completa para el periodo especificado, los círculos se combinan para mostrar un público definido.

Una vez guardada la audiencia, está disponible para otras aplicaciones de Experience Cloud. Por ejemplo, puede incluir una audiencia compartida en una [actividad](https://experienceleague.adobe.com/en/docs/target/using/activities/activities) de Adobe Target.
