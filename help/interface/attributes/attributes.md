---
description: Información general y requisitos previos sobre la carga de atributos del cliente en Experience Cloud.
keywords: servicios principales; atributos del cliente
seo-description: Información general y requisitos previos sobre la carga de atributos del cliente en Experience Cloud.
seo-title: Atributos del cliente
solution: Experience Cloud
title: Atributos del cliente
uuid: 1621402 d -990 f -46 f 9-981 a -473280559069
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# Atributos del cliente

## Información general  

La [!UICONTROL función de atributos] del cliente en Experience Cloud se encuentra aquí.

**[!UICONTROL Personas]** &gt; **[!UICONTROL Atributos del cliente]**

Si captura los datos del cliente empresarial en una base de datos de administración de la relación con los clientes (CRM), podrá cargar los datos en un origen de datos de atributos del cliente en Experience Cloud. Una vez cargados, aproveche los datos en [!DNL Adobe Analytics] y [!DNL Adobe Target].

![](assets/custom_reports.png)

## Requisitos previos para la carga de atributos del cliente {#section_BD38693AFBF34926BA28E964963B4EA0}


* **Activación de la solución:**[Habilite las soluciones para los servicios principales](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C).

* **Pertenencia a grupo:** Para cargar datos de atributos del cliente, los usuarios deben ser miembros del grupo Atributos [del cliente](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9). También debe pertenecer a un grupo de Adobe Analytics o de Adobe Target.

   Para saber si su empresa tiene acceso a los atributos del cliente, [!DNL Experience Cloud] su administrador debe iniciar sesión en [!DNL Experience Cloud]. Vaya **[!UICONTROL a Administración]** &gt; **[!UICONTROL Iniciar Admin Console]** &gt; **[!UICONTROL Grupos]**. Si *los atributos del cliente* se muestran como uno de los grupos, estará listo para empezar.

   Los usuarios que se agregan al grupo Atributos del cliente podrán ver el elemento de menú [!UICONTROL Atributos del cliente] a la izquierda de la interfaz de Experience Cloud.

* **Mbox de Target:** para los atributos del cliente se necesita la versión 58 o posterior de mbox.js.


   Consulte [Implementación de Mbox.js](https://marketing.adobe.com/resources/help/en_US/target/ov/t_mbox_download.html).

* **at.js:** cualquier versión.




## ¿Qué son los datos de clientes empresariales? {#section_6F34C29F11414842AA57D2B1248FA3C6}

Los datos empresariales residen en otros sistemas. Pueden resultar complejos y significan cosas distintas para cada persona. Estos datos pueden incluir información como afiliaciones, nivel de lealtad, edad, género, productos propios, intereses y valor de duración.

La siguiente imagen es un ejemplo de un archivo de datos que muestra los datos del suscriptor de productos, incluidos los ID de miembro, los productos con licencia, los productos más ejecutados y demás.

![](assets/01_crs_usecase.png)

Después de crear el archivo de datos, puede cargarlo en el origen de atributos del cliente que cree en **[!UICONTROL Experience Cloud]** &gt; **[!UICONTROL Atributos del cliente]**.

Consulte [Cargar datos de atributos del cliente](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78) para conocer este flujo de trabajo.

## Casos de uso de la solución {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

Una vez los datos se encuentren en Experience Cloud, podrá personalizarlos y compartirlos con soluciones para la creación de informes, segmentación, actividades y campañas.

Por ejemplo:

| Solución | Ventajas y casos de uso |
|--- |--- |
| Adobe Analytics | Los comerciantes y analistas sabrán:<ul><li>Qué campañas en línea son más eficaces con los clientes de nivel oro.</li><li>Qué productos buscan los clientes de nivel oro en comparación con los productos que buscan los clientes de nivel platino.</li><li>Si el rediseño de su sitio tiene una influencia positiva en las tasas de conversión de los clientes más antiguos.</li><li>Qué productos tienden a buscar en el sitio los clientes con un valor de duración bajo.</li></ul> |
| Adobe Target | Los datos de atributos permiten a los clientes de Target:<ul><li>Mostrar a los miembros del club de fidelidad descuentos y ofertas especiales.</li><li>Recomendar productos de mayor precio a los clientes de lujo.</li><li>Para los clientes que ya reciban correo electrónico, mostrar una oferta de mayor precio en el espacio reservado normalmente para los registros de correo electrónico.</li></ul> |
