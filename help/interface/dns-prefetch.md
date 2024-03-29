---
description: Aprenda a implementar la búsqueda previa de DNS para ayudar a reducir los tiempos de carga de la página con diferentes aplicaciones y servicios en Experience Cloud.
solution: Experience Cloud
title: Uso de la precarga de DNS con diferentes aplicaciones y servicios
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
source-git-commit: 57f4925616c5accbe605aa96f926335abaf9aebd
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 95%

---

# Uso de la precarga de DNS con diferentes aplicaciones y servicios

Implemente la precarga de DNS para ayudar a reducir el tiempo de la carga de las páginas con distintas aplicaciones y servicios.

## Explicación de la precarga de DNS {#section_772BF9CB7C4141DE9B0355146E2CD962}

Los navegadores utilizan la precarga de DNS para resolver automáticamente los nombres de dominio vinculados en una página web con sus correspondientes direcciones IP. El proceso de precarga comienza cuando el explorador carga una página web. A modo de ejemplo, supongamos que su página contiene un vínculo que se puede seleccionar a `www.adobe.com`. Cuando un navegador carga esta página, utiliza el [sistema DNS](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/) para buscar el nombre de dominio vinculado y resolverlo en una dirección IP numérica correspondiente. La precarga de DNS ayuda a mejorar el rendimiento de la página porque el nombre de dominio ya está resuelto en una dirección IP antes de que un visitante del sitio haga clic en ese vínculo o botón. El proceso de precarga de DNS es transparente para los usuarios.

## Precarga de DNS y aplicaciones de Adobe Experience Cloud {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

La precarga de DNS funciona automáticamente con vínculos estáticos incrustados en una página. Esto también significa que la precarga de DNS automática no funciona con dominios diferentes [!UICONTROL Experience Cloud] aplicaciones y servicios porque:

* Cada aplicación o servicio de Experience Cloud genera llamadas DNS de forma dinámica a medida que se carga la página.
* El explorador no puede resolver nombres de dominio en direcciones IP antes de realizar estas llamadas.

Sin embargo, puede implementar manualmente la precarga de DNS con sus aplicaciones de Experience Cloud. Para ello, agregue la etiqueta HTML `<dns-prefetch>` a la sección `<head>` del código de la página, como se muestra a continuación. Cuando se implementa apropiadamente, la precarga de DNS puede ayudar a recortar el tiempo de carga de una página en algunos milisegundos.

## Ejemplos de código de precarga de DNS {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

Los siguientes ejemplos muestran cómo se consigue que la precarga de DNS realice llamadas a distintas aplicaciones y servicios de [!DNL Experience Cloud]. Algunas llamadas de precarga requieren el identificador de su organización de [!DNL Adobe] o el seguimiento de información de servidores. En estos ejemplos, el código en *cursiva* representa un marcador de posición de variable. Dicho código se sustituye con su propio ID de socio de [!DNL Adobe], su código de cliente o su información de servidor de seguimiento, etcétera.

* **Analytics:** `<link rel="dns-prefetch" href="//insert tracking server name here">`.

  Agregue una etiqueta separada para cada nombre DNS si utiliza servidores de seguimiento seguros y no seguros.

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Servicio de Experience Cloud ID:** `<link rel="dns-prefetch" href="//fast. *`insertar ID de socio aquí`*.demdex.net">`

* **Dynamic Tag Manager** (DTM): No obligatorio. Los vínculos de DTM están disponibles cuando se carga la página.

* **Advertising Cloud:**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`

* **[!DNL Target]:** `<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* [Precarga de DNS](https://www.chromium.org/developers/design-documents/dns-prefetching)
