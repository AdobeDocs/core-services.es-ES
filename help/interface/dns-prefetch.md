---
description: Implemente la precarga de DNS para ayudar a reducir el tiempo de la carga de las páginas con distintas soluciones y servicios.
seo-description: Implemente la precarga de DNS para ayudar a reducir el tiempo de la carga de las páginas con distintas soluciones y servicios.
seo-title: Uso de la precarga de DNS con diferentes soluciones y servicios
solution: Experience Cloud
title: Uso de la precarga de DNS con diferentes soluciones y servicios
uuid: 4220 e 223-e 00 e -46 b 1-8 bde -52248913 bea 1
translation-type: tm+mt
source-git-commit: af5339fe58ce884345804574c209907d6504a483

---


# Uso de la precarga de DNS con diferentes soluciones y servicios

Implemente la precarga de DNS para ayudar a reducir el tiempo de la carga de las páginas con distintas soluciones y servicios.

## Explicación de la precarga de DNS {#section_772BF9CB7C4141DE9B0355146E2CD962}

Los navegadores utilizan la precarga de DNS para resolver automáticamente nombres de dominio vinculados en una página web en sus direcciones IP correspondientes. El proceso de precarga se inicia cuando el navegador carga una página web. Como ejemplo, supongamos que su página contiene un vínculo donde se puede hacer clic `www.adobe.com`. Cuando un navegador carga esta página, utiliza el [sistema DNS](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/) para buscar el nombre de dominio vinculado y resolverlo en una dirección IP numérica correspondiente. La precarga de DNS ayuda a mejorar el rendimiento de la página porque el nombre de dominio ya está resuelto en una dirección IP antes de que un visitante haga clic en el vínculo o botón. El proceso de precarga de DNS es transparente para el usuario.

## Precarga de DNS y soluciones de Adobe Experience Cloud {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

La precarga de DNS trabaja de forma automática con los vínculos estáticos incrustados en una página. Esto también significa que la precarga de DNS automática no funciona con distintas soluciones y servicios de [!UICONTROL Experience Cloud] porque:

* Cada solución o servicio de Experience Cloud genera llamadas DNS de forma dinámica al cargarse la página.
* El navegador no puede resolver nombres de dominio en direcciones IP antes de que se realicen estas llamadas.

Sin embargo, puede implementar de forma manual la precarga de DNS con sus soluciones de Experience Cloud. Para ello, agregue la etiqueta HTML `<dns-prefetch>` a la `<head>` sección del código de página, como se muestra a continuación. Cuando se implementa apropiadamente, la precarga de DNS puede ayudar a recortar el tiempo de carga de una página en algunos milisegundos.

## Muestras de código de precarga de DNS {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

Los siguientes ejemplos muestran cómo se consigue que la precarga de DNS realice llamadas a distintas soluciones y servicios de [!DNL Experience Cloud]. Algunas llamadas de precarga requieren el identificador de su organización de [!DNL Adobe] o el seguimiento de información de servidores. En estos ejemplos, el código en *cursiva* representa un marcador de posición de variable. Dicho código se sustituye con su propio ID de socio de [!DNL Adobe], su código de cliente o su información de servidor de seguimiento, etcétera.

* **Analytics:** `<link rel="dns-prefetch" href="//insert tracking server name here">`.

   Agregue una etiqueta separada para cada nombre DNS si utiliza servidores de seguimiento seguros y no seguros.

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Servicio Experience Cloud ID:**`<link rel="dns-prefetch" href="//fast. *`insert partner ID here`*.demdex.net">`

* **Administrador dinámico de etiquetas** (DTM): No obligatorio. Los vínculos DTM están disponibles en cuanto la página se carga.

* **Media Optimizer (Ad Cloud):**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`


* **Target:** `<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORE_ LIKE_ THIS]
>
>* [Precarga de DNS](https://www.chromium.org/developers/design-documents/dns-prefetching)

