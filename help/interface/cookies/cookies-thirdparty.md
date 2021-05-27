---
description: Obtenga información sobre cómo la compatibilidad con cookies de terceros se ha limitado cada vez más en los distintos exploradores.
keywords: cookies,privacidad
solution: Experience Cloud,Analytics,Target
title: 'Impacto en los clientes de los cambios en la compatibilidad con cookies de terceros '
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
feature: Cookies
topic: Administración
role: Administrator
level: Experienced
exl-id: 3d12a1b1-c952-4b42-815d-f64b31429cec
source-git-commit: ef6196c3096ac7b26633eb4b1b9b2db26237732a
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 84%

---

# Efecto de los cambios en el soporte para las cookies de terceros en los clientes {#how-changes-to-third-party-cookie-support-impacts-customers}

El soporte para las cookies de terceros cada vez es más limitado en los navegadores. Por este motivo, Adobe ha estado trabajando en nuevas soluciones que procuran armonizar las solicitudes de los clientes con los derechos de privacidad del consumidor en las soluciones de Adobe Experience Cloud.

La siguiente lista describe cómo afecta la compatibilidad con cookies de terceros a las implementaciones actuales de las soluciones de Adobe Experience Cloud:

## Adobe Analytics y Adobe Target

* Analytics y Target no se verán muy afectados, ya que la misma actividad del sitio solo depende de cookies de origen. Las cookies de terceros son necesarias para comprender la actividad de los usuarios en los distintos dominios. En los exploradores en los que las cookies de terceros están bloqueadas, el seguimiento entre dominios no será posible mediante cookies.

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
