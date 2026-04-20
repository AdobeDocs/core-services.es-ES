---
title: Recopilación de datos regionales
description: Obtenga información acerca de la recopilación de datos regionales en CX Enterprise.
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
TQID: https://experienceleague.adobe.com/hjHQDRoNOP2e6pKhKHB9DZaII2o8eJVzL5wjRzaMFwM
product_v2: id: e1971122-7081-4556-9222-8a31bd71800c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 0%

---

# Recopilación de datos regionales

Adobe CX Enterprise utiliza la recopilación de datos regionales (RDC) para que las interacciones entre los visitantes y Adobe se produzcan lo más cerca posible de los visitantes. Los datos recopilados localmente en un sitio Edge se reenvían de forma segura a un sitio principal para su procesamiento. Una vez procesados, los datos están disponibles para los productos y servicios de Adobe CX Enterprise.

El flujo de trabajo de recopilación de datos regionales ofrece varias ventajas:

* **Rendimiento**: con RDC, los visitantes se conectan al sitio Edge más cercano. Esta optimización proporciona el tiempo de respuesta más rápido, lo que da como resultado un seguimiento más preciso y tiempos de carga más rápidos.
* **Redundancia**: si se interrumpe la comunicación entre cualquier sitio perimetral y el sitio principal, la infraestructura de Adobe guarda los datos localmente y los reenvía al sitio principal cuando se restauran las comunicaciones. Adobe también puede enrutar el tráfico a otros sitios Edge si una ubicación específica experimenta interrupciones.

Actualmente, la recopilación de datos regionales incluye las siguientes ubicaciones (sujetas a cambios):

## Recopilación de datos de origen

| Tipo de RDC | Centros de recopilación de datos |
| --- | --- |
| Global (predeterminado) | Oregón, Virginia, Irlanda, París, Bombay, Singapur, Tokio, Sídney |
| Global + China* | Pekín*, Oregón, Virginia, Irlanda, París, Bombay, Singapur, Tokio, Sídney |
| Solo América | Oregón, Virginia |
| Solo Europa | Irlanda, París |
| Solo Asia-Pacífico | Mumbai, Singapur, Tokio, Sydney |
| Solo en China* | Pekín |

{style="table-layout:auto"}

_*La recopilación de datos regionales de China requiere el paquete de complementos de optimización del rendimiento de China y solo se aplica a Adobe Analytics que usa la recopilación de datos de AppMeasurement. No se admiten otros servicios de CX Enterprise ni la recopilación de datos de Web SDK. Póngase en contacto con el equipo de su cuenta de Adobe para obtener más información acerca del paquete de complementos para la optimización del rendimiento en China._

## Recopilación de datos de terceros

La recopilación de datos de terceros incluye dominios de cookies que no coinciden con el dominio del sitio web. Algunos ejemplos son `adobedc.net`, `omtrdc.net` y `2o7.net`.

| Tipo de RDC | Centros de recopilación de datos |
| --- | --- |
| Predeterminado | Oregón, Virginia, Irlanda, París, Bombay, Singapur, Tokio, Sídney |
| Predeterminado + China* | Pekín*, Oregón, Virginia, Irlanda, París, Bombay, Singapur, Tokio, Sídney |

{style="table-layout:auto"}

