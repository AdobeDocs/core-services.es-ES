---
description: El soporte para las cookies de terceros cada vez es más limitado en los navegadores. Por este motivo, Adobe ha estado trabajando en nuevas soluciones que procuran armonizar las solicitudes de los clientes con los derechos de privacidad del consumidor en las soluciones de Adobe Experience Cloud.
keywords: cookies; privacidad
seo-description: El soporte para las cookies de terceros cada vez es más limitado en los navegadores. Por este motivo, Adobe ha estado trabajando en nuevas soluciones que procuran armonizar las solicitudes de los clientes con los derechos de privacidad del consumidor en las soluciones de Adobe Experience Cloud.
seo-title: Cómo afectan los cambios en el soporte para las cookies de terceros a los clientes
solution: Marketing Cloud, Analytics, Target, Social
title: Cómo afectan los cambios en el soporte para las cookies de terceros a los clientes
uuid: 27332 e 0 d -6932-4 a 6 e-b 97 b -0 adeced 0 b 050
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 426c1fecf16e1cf83cd28971e4de6fdb66b0e10d

---


# Cómo afectan los cambios en el soporte para las cookies de terceros a los clientes{#how-changes-to-third-party-cookie-support-impacts-customers}

El soporte para las cookies de terceros cada vez es más limitado en los navegadores. Por este motivo, Adobe ha estado trabajando en nuevas soluciones que procuran armonizar las solicitudes de los clientes con los derechos de privacidad del consumidor en las soluciones de Adobe Experience Cloud.

En la siguiente lista se describe cómo afecta el soporte para las cookies de terceros a las implementaciones actuales de las soluciones de Adobe Experience Cloud:

**Adobe Analytics y Target**

* Sigue sin afectar a los clientes con una implementación propia. 
* Customers that are not using first-party implementation can implement the [Experience Platform ID Service](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html) to store the ID cookie as a first-party cookie without a first-party implementation.

**Adobe Experience Manager**

* Como Adobe Experience Manager funciona en su totalidad en el dominio del cliente, existe una interacción mínima con las cookies de terceros, por lo que el impacto es mínimo. 

**Adobe Social**

* Social no se vería afectado siempre que el cliente tenga la versión más reciente del código.

**Adobe Media Optimizer**

* Buscar:

   * Cuando se optimiza la búsqueda según los datos de Adobe Analytics, esta se verá afectada en la misma medida que Adobe Analytics.
   * La recopilación de los datos de conversión no debería verse afectada.

* Visualización:

   * Actualmente, la visualización de remarketing depende totalmente de los usos de las cookies de terceros.
   * La visualización también depende en gran medida de la disponibilidad de diferentes cookies de la red de anuncios para la sincronización.
   * Se desconoce el impacto global. No obstante, según el primer punto, la visualización se verá más afectada que otros servicios.
   * Estamos trabajando internamente y en colaboración con nuestros socios publicitarios para evaluar el alcance total del impacto sobre el envío de anuncios.

* Social:

   * No hay ningún impacto en los anuncios de Mercado de Facebook.
   * Se verá afectado Facebook Exchange (FBX) en la misma medida que la visualización y el envío.

