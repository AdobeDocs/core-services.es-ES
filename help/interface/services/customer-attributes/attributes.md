---
title: “[!DNL Customer Attributes]”
description: Más información acerca de  [!DNL Customer Attributes]  en Experience Cloud. Descubra cómo cargar los datos de atributos de cliente para utilizarlos en Adobe Analytics y Adobe Target.
solution: Experience Cloud,Target,Analytics
feature: Customer Attributes
role: Admin
topic: Administration
level: Experienced
exl-id: fe8ad013-76da-49f8-aa51-dc5f6c1b1d79
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 96%

---

# [!DNL Customer Attributes] en Experience Cloud

Los [!DNL Customer Attributes] de Experience Cloud le permiten cargar los datos empresariales recogidos desde una base de datos de administración de la relación con los clientes (CRM). Puede cargar los datos en una fuente de datos de atributos de cliente de Experience Cloud y, a continuación, utilizar los datos en [!DNL Adobe Analytics] y [!DNL Adobe Target].

## Busque la función [!DNL Customer Attributes]

1. Inicie sesión en Experience Cloud.

1. Vaya a **[!DNL Experience Platform]** > **[!UICONTROL Usuarios]** > **[!UICONTROL Atributos del cliente]**.

![Información general sobre Atributos del cliente](assets/custom_reports.png)

## Requisitos previos para la carga de [!DNL Customer Attributes] {#section_BD38693AFBF34926BA28E964963B4EA0}

* **Pertenencia a un grupo:** Para cargar datos de atributos del cliente, los usuarios deben ser miembros del grupo Atributos del cliente. También debe pertenecer a un grupo de Adobe Analytics o de Adobe Target.

  Para saber si su empresa tiene acceso a los atributos del cliente, su administrador de [!DNL Experience Cloud]debe iniciar sesión en [Experience Cloud](https://experience.adobe.com). Vaya a **[!UICONTROL Administración]** > **[!UICONTROL Admin Console]** > **[!UICONTROL Productos]**. Si *[!DNL Customer Attributes]* se muestra como uno de los [!UICONTROL perfiles de producto], está listo para empezar.

  Los usuarios que se agregan a [!DNL Customer Attributes] pueden ver el elemento de menú [!UICONTROL Atributos del cliente] a la izquierda de la interfaz de Experience Cloud.

* Se requiere **Adobe Target** `at.js` (cualquier versión) o `mbox.js` versión 58 o posterior para los Atributos del cliente.

  Consulte [Cómo implementar at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html?lang=es)

## ¿Qué son los datos del cliente empresariales? {#section_6F34C29F11414842AA57D2B1248FA3C6}

Los datos empresariales residen en otros sistemas. Puede ser complejo y significar cosas diferentes para diferentes personas. Estos datos pueden incluir información como suscripciones, nivel de lealtad, edad, sexo, productos propios, intereses y valor a largo plazo.

La siguiente imagen es un ejemplo de un archivo de datos que muestra los datos del suscriptor de productos, incluidos los ID de miembro, los productos con derechos, los productos más utilizados, etc.

![¿Qué son los datos del cliente empresariales?](assets/01_crs_usecase.png)

Tras crear el archivo de datos, puede cargarlo en el origen de atributos del cliente que cree en **[!UICONTROL Experience Cloud]** > **[!UICONTROL Atributos del cliente]**.

Consulte [Carga de datos del atributo del cliente](t-crs-usecase.md) para obtener información sobre este flujo de trabajo.

## Ejemplos de atributos del cliente de Analytics y Target {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

Una vez que los datos se encuentren en Experience Cloud, podrá personalizarlos y compartirlos con soluciones para la creación de informes, segmentación, actividades y campañas.

Por ejemplo:

| Solución | Ventajas y casos de uso |
|--- |--- |
| Adobe Analytics | Los especialistas en marketing y analistas pueden comprender:<ul><li>Las campañas en línea más efectivas con sus clientes de nivel oro.</li><li>Los productos que buscan los clientes de nivel oro en comparación con los productos que buscan los clientes de nivel platino.</li><li>Si el rediseño del sitio está teniendo un impacto positivo en las tasas de conversión para los clientes más antiguos.</li><li>Los productos que tienden a buscar en el sitio los clientes con un valor bajo a largo plazo.</li></ul> |
| Adobe Target | Los datos de atributos permiten a los usuarios de Adobe Target:<ul><li>Mostrar descuentos y ofertas especiales para miembros del club de fidelidad.</li><li>Recomendar productos más caros a sus clientes de lujo.</li><li>Para los clientes que ya reciben correos electrónicos, permite mostrar una oferta de “up-sell” en el espacio reservado normalmente para los registros por correo electrónico.</li></ul> |

{style="table-layout:auto"}
