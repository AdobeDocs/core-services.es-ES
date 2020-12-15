---
description: Obtenga información sobre cómo la compatibilidad con cookies de terceros se ha limitado cada vez más en los distintos exploradores.
keywords: cookies;privacy
solution: Experience Cloud,Analytics,Target
title: 'Cómo los cambios en la compatibilidad con cookies de terceros afectan a los clientes '
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
translation-type: tm+mt
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 92%

---


# Efecto de los cambios en el soporte para las cookies de terceros en los clientes {#how-changes-to-third-party-cookie-support-impacts-customers}

El soporte para las cookies de terceros cada vez es más limitado en los navegadores. Por este motivo, Adobe ha estado trabajando en nuevas soluciones que procuran armonizar las solicitudes de los clientes con los derechos de privacidad del consumidor en las soluciones de Adobe Experience Cloud.

La siguiente lista describe cómo afecta la compatibilidad con cookies de terceros a las implementaciones actuales de las soluciones de Adobe Experience Cloud:

## Adobe Analytics y Adobe Target

* Los clientes con una [implementación propia](/help/interface/cookies/cookies-first-party.md) no se verán muy afectados.
* Los clientes que no utilizan implementación propia pueden implementar el [Servicio Experience Platform ID](https://docs.adobe.com/content/help/es-ES/id-service/using/implementation/implementation-guides.html) para almacenar la cookie de ID como cookie de origen sin una implementación propia.

## Adobe Experience Manager

* Como Adobe Experience Manager funciona en su totalidad en el dominio del cliente, existe una interacción mínima con las cookies de terceros, por lo que el impacto es mínimo.

## Adobe Social

* Social no se vería afectado siempre que el cliente tenga la versión más reciente del código.

## Adobe Advertising Cloud

* Buscar:

   * Cuando la búsqueda se optimiza en función de los datos de Adobe Analytics, la búsqueda se verá afectada de la misma manera que Adobe Analytics.
   * La recopilación de datos de conversión no debe verse afectada.

* Mostrar:

   * La visualización de remarketing hoy depende completamente del uso de cookies de terceros.
   * La visualización también depende en gran medida de la disponibilidad de varias cookies de red de publicidad para la sincronización.
   * Se desconoce el impacto global. Sin embargo, en el primer punto, la visualización se ve más afectada que en otros servicios.
   * Estamos trabajando internamente y con nuestros socios publicitarios para evaluar todo el impacto en el envío publicitario.

* Social:

   * No hay impacto en la publicidad de Facebook.
   * Facebook Exchange (FBX) se verá afectado de la misma manera que el envío de anuncios en pantalla.
