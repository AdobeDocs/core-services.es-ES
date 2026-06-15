---
description: Aprenda a implementar la precarga de DNS para ayudar a reducir los tiempos de carga de la página con diferentes aplicaciones y servicios en CX Enterprise.
solution: Experience Cloud
title: Usar precarga de DNS
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
TQID: https://experienceleague.adobe.com/oAe81mw-qFetDM0zky2eS6DNf-XZ67H68Qw-Sa8mk0Y
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 76%

---

# Use la precarga de DNS

Implemente la precarga de DNS para ayudar a reducir el tiempo de la carga de las páginas con distintas aplicaciones y servicios.

## Explicación de la precarga de DNS

Los navegadores utilizan la precarga de DNS para resolver automáticamente los nombres de dominio vinculados en una página web con sus correspondientes direcciones IP. El proceso de precarga comienza cuando el explorador carga una página web. A modo de ejemplo, supongamos que su página contiene un vínculo que se puede seleccionar a `www.adobe.com`. Cuando un navegador carga esta página, utiliza el _sistema DNS_ para buscar el nombre de dominio vinculado y resolverlo en una dirección IP numérica correspondiente. La precarga de DNS ayuda a mejorar el rendimiento de la página porque el nombre de dominio ya está resuelto en una dirección IP antes de que un visitante del sitio haga clic en ese vínculo o botón. El proceso de precarga de DNS es transparente para los usuarios.

## Precarga de DNS y aplicaciones empresariales de Adobe CX

La precarga de DNS funciona automáticamente con vínculos estáticos incrustados en una página. Esto también significa que la precarga de DNS automática no funciona con diferentes aplicaciones y servicios de [!UICONTROL CX Enterprise] porque:

* Cada aplicación o servicio de CX Enterprise genera llamadas DNS de forma dinámica a medida que se carga la página.
* El explorador no puede resolver nombres de dominio en direcciones IP antes de realizar estas llamadas.

Sin embargo, puede implementar manualmente la precarga de DNS con sus aplicaciones de CX Enterprise. Para ello, agregue la etiqueta HTML `<dns-prefetch>` a la sección `<head>` del código de la página, como se muestra a continuación. Cuando se implementa apropiadamente, la precarga de DNS puede ayudar a recortar el tiempo de carga de una página en algunos milisegundos.

## Ejemplos de código de precarga de DNS

Los siguientes ejemplos muestran cómo se consigue que la precarga de DNS realice llamadas a distintas aplicaciones y servicios de [!DNL CX Enterprise]. Algunas llamadas de precarga requieren el identificador de su organización de [!DNL Adobe] o el seguimiento de información de servidores. En estos ejemplos, el código en *cursiva* representa un marcador de posición de variable. Dicho código se sustituye con su propio ID de socio de [!DNL Adobe], su código de cliente o su información de servidor de seguimiento, etcétera.

* **Analytics:** `<link rel="dns-prefetch" href="//data.example.com">`.

  Agregue una etiqueta separada para cada nombre DNS si utiliza servidores de seguimiento seguros y no seguros.

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Servicio Enterprise ID CX:** `<link rel="dns-prefetch" href="//fast.examplepartnerid.demdex.net">`

* **Advertising Cloud:**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttech.net">`

* **[!DNL Target]:** `<link rel="dns-prefetch" href="//example.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* [Precarga de DNS](https://www.chromium.org/developers/design-documents/dns-prefetching) en Chromium

