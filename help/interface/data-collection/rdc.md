---
title: Recopilación de datos regionales
description: Información sobre la recopilación de datos regionales
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
source-git-commit: 2691f0dc91e48a8f817467e334d9028f2e506e70
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 23%

---

# Recopilación de datos regionales

Adobe Experience Cloud utiliza la recopilación de datos regionales (RDC) para que las interacciones entre los visitantes y el Adobe se produzcan lo más cerca posible de los visitantes. Los datos recopilados localmente en un sitio Edge se reenvían de forma segura a un sitio principal para su procesamiento. Una vez procesados, los datos están disponibles para los productos y servicios de Adobe Experience Cloud.

El flujo de trabajo de recopilación de datos regionales ofrece varias ventajas:

* **Rendimiento**: con la recopilación de datos regionales, los visitantes se conectan al sitio Edge más cercano. Esto proporciona el tiempo de respuesta más rápido, lo que da como resultado un seguimiento más preciso y tiempos de carga más rápidos.
* **Redundancia**: si se interrumpe la comunicación entre cualquier sitio perimetral y el sitio principal, la infraestructura de Adobe guarda los datos localmente y los reenvía al sitio principal cuando se restauran las comunicaciones. El Adobe también puede enrutar el tráfico a otros sitios Edge si una ubicación específica experimenta interrupciones.

Actualmente, la recopilación de datos regionales incluye las siguientes ubicaciones (sujetas a cambios):

## Recopilación de datos de origen

| Tipo de RDC | Centros de recopilación de datos |
| --- | --- |
| Global (predeterminado) | Oregón, Virginia, Irlanda, París, Mumbai, Singapur, Tokio, Sydney |
| Global + China* | China*, Oregón, Virginia, Irlanda, París, Bombay, Singapur, Tokio, Sídney |
| Solo América | Oregón, Virginia |
| Solo Europa | Irlanda, París |
| Solo Asia-Pacífico | Mumbai, Singapur, Tokio, Sydney |
| Solo en China* | Pekín |

{style="table-layout:auto"}

_*La recopilación de datos regionales de China requiere el paquete de complementos para la optimización del rendimiento en China y solo se aplica a Adobe Analytics que usa la recopilación de datos de AppMeasurement. No se admiten otros servicios de Experience Cloud ni la recopilación de datos del SDK web. Póngase en contacto con el equipo de su cuenta de Adobe para obtener más información sobre el paquete de complementos de optimización del rendimiento de China._

## Recopilación de datos de terceros

La recopilación de datos de terceros incluye dominios de cookies que no coinciden con el dominio del sitio web. Los ejemplos incluyen `adobedc.net`, `omtrdc.net` y `2o7.net`.

| Tipo de RDC | Centros de recopilación de datos |
| --- | --- |
| Predeterminado | Oregón, Virginia, Irlanda, París, Bombay, Singapur, Tokio, Sídney, China* |

{style="table-layout:auto"}
