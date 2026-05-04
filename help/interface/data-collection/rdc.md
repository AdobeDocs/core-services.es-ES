---
title: Recopilación de datos regionales
description: Obtenga información acerca de la recopilación de datos regionales en CX Enterprise.
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
TQID: https://experienceleague.adobe.com/hjHQDRoNOP2e6pKhKHB9DZaII2o8eJVzL5wjRzaMFwM
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 233d1554de9e37fccd5cf47fec2c4222d7a5e807
workflow-type: tm+mt
source-wordcount: 361
ht-degree: 0%

---

# Recopilación de datos regionales

Adobe CX Enterprise utiliza la recopilación de datos regionales (RDC) para que las interacciones entre sus visitantes y Adobe se produzcan lo más cerca posible de sus visitantes. Los datos recopilados localmente en un sitio Edge se reenvían de forma segura a un sitio principal para su procesamiento. Una vez procesados, los datos están disponibles para los productos y servicios empresariales de Adobe CX.

El flujo de trabajo de recopilación de datos regionales ofrece varias ventajas:

* **Rendimiento**: con RDC, los visitantes se conectan al sitio Edge más cercano. Esta optimización proporciona el tiempo de respuesta más rápido, lo que da como resultado un seguimiento más preciso y tiempos de carga más rápidos.
* **Redundancia**: si se interrumpe la comunicación entre cualquier sitio perimetral y el sitio principal, la infraestructura de Adobe guarda los datos localmente y los reenvía al sitio principal cuando se restauran las comunicaciones. Adobe también puede enrutar el tráfico a otros sitios Edge si una ubicación específica experimenta interrupciones.

## Recopilación de datos de origen

La recopilación de datos de origen utiliza una implementación CNAME para enrutar datos a Adobe a través de su propio dominio. El tipo de RDC se ha seleccionado como parte del proceso de configuración del [Programa de certificados administrados por Adobe](adobe-managed-cert.md). Para comprobar o actualizar el tipo de RDC, póngase en contacto con el equipo de cuenta de Adobe. Están disponibles los siguientes tipos de RDC y centros de datos asociados:

| Tipo de RDC | Centros de recopilación de datos |
| --- | --- |
| Global (predeterminado) | Oregón, Virginia, Irlanda, París, Bombay, Singapur, Tokio, Sídney |
| Global + China* | Pekín*, Oregón, Virginia, Irlanda, París, Bombay, Singapur, Tokio, Sídney |
| Solo América | Oregón, Virginia |
| Solo Europa | Irlanda, París |
| Solo Asia-Pacífico | Mumbai, Singapur, Tokio, Sydney |
| Solo en China* | Pekín |

_*La recopilación de datos regionales de China requiere el paquete de complementos de optimización del rendimiento de China y solo se aplica a Adobe Analytics que usa la recopilación de datos de AppMeasurement. No se admiten otros servicios de CX Enterprise ni la recopilación de datos de Web SDK. Póngase en contacto con el equipo de su cuenta de Adobe para obtener más información acerca del paquete de complementos para la optimización del rendimiento en China._

## Recopilación de datos de terceros

La recopilación de datos de terceros utiliza dominios de cookies que no coinciden con el dominio del sitio web. Algunos ejemplos son `adobedc.net`, `omtrdc.net` y `2o7.net`.

| Tipo de RDC | Centros de recopilación de datos |
| --- | --- |
| Predeterminado | Oregón, Virginia, Irlanda, París, Bombay, Singapur, Tokio, Sídney |
| Predeterminado + China* | Pekín*, Oregón, Virginia, Irlanda, París, Bombay, Singapur, Tokio, Sídney |

_*Requiere el paquete de complementos para la optimización del rendimiento en China. Consulte la sección de recopilación de datos de origen anterior para obtener más información._
