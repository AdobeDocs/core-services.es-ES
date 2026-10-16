---
title: Enrutar la recopilación de datos a través de una CDN
description: Aprenda a configurar una red de entrega de contenido (CDN) para reenviar solicitudes de recopilación de datos a Adobe sin afectar a la calidad de los datos.
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: e1185eeafc809b036b10955880536db7a576ca0b
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%
---
# Enrutar la recopilación de datos a través de una CDN

Algunas organizaciones enrutan solicitudes de recopilación de datos a través de su red de entrega de contenido (CDN) en lugar de enviarlas directamente a Adobe. Algunas razones comunes son la protección del cortafuegos de aplicaciones web (WAF), las políticas corporativas que requieren que todo el tráfico del sitio web pase a través de una CDN y la capacidad de inspeccionar el tráfico enviado a Adobe. La CDN recibe solicitudes en un nombre de host que posee su organización y las reenvía a un nombre de host de recopilación de datos de Adobe, denominado origin.

>[!IMPORTANT]
>
>Adobe no puede revisar ni validar la configuración de CDN. Su organización y su proveedor de CDN son responsables de configurar la CDN correctamente. Para obtener ayuda sobre la configuración de la CDN, póngase en contacto con su proveedor de CDN. Las CDN configuradas incorrectamente pueden causar la pérdida de datos.

## Elija un tipo de origen. {#origin-type}

| | Origen de terceros (recomendado) | Origen de origen |
| --- | --- | --- |
| **Nombre de host de origen** | Su subdominio de ID de inquilino de `data.adobedc.net`, como `example.data.adobedc.net` | Su nombre de host de origen, como `data.example.com` |
| **Certificado en servidores de Adobe** | Certificado de Adobe (`*.data.adobedc.net`) | [Certificado administrado por el cliente](customer-managed-cert.md) |
| **Renovaciones de certificados** | Ninguno obligatorio | Su organización renueva el certificado y lo proporciona a Adobe antes de cada caducidad |
| **RDC [bloqueadas por región](rdc.md)** | No compatible | Admitido |
| **Cuándo usar** | Todas las implementaciones de CDN, a menos que su organización requiera un origen de origen | La directiva de seguridad requiere un control directo del certificado de origen o su organización requiere un tipo de RDC con bloqueo por región |

>[!NOTE]
>
>El [programa de certificados administrado por Adobe](adobe-managed-cert.md) no admite implementaciones de CDN. Adobe no puede validar la propiedad del dominio ni renovar los certificados para los nombres de host que apuntan a su CDN. Use un origen de terceros o un origen de origen con un [certificado administrado por el cliente](customer-managed-cert.md).

## Requisitos para todas las implementaciones de CDN {#requirements}

Las bibliotecas de recopilación de datos de Adobe, como AppMeasurement y Web SDK, incluyen todo lo que Adobe necesita en cada solicitud. Configure su CDN para que reenvíe estas solicitudes a Adobe sin cambiarlas.

>[!IMPORTANT]
>
>Nunca cambie el extremo ni nada que determine adónde van los datos, incluido el ID del grupo de informes (AppMeasurement) o el ID del conjunto de datos (Web SDK). Si cambia estos valores, se perderán datos.

La configuración de CDN debe:

* Reenviar el método de solicitud, la ruta URL, la cadena de consulta y el cuerpo sin cambios.
* No modifique el encabezado `Host`.
* Deje el dominio en el que se configuran las cookies de Adobe sin cambiar.
* Mantenga todas las cookies enumeradas en la [sección de cookies](cookies/overview.md) de esta guía.
* Agregue el encabezado `X-Forwarded-For` que contiene la dirección IP del visitante. Adobe utiliza este encabezado para la geolocalización. Sin ella, los datos de geolocalización reflejan la ubicación de los servidores de CDN en lugar de los visitantes.
* Devolver las respuestas de Adobe al explorador sin cambios.

La configuración de CDN puede:

* Elimine las cookies que Adobe no utilice, como las de otros sistemas del sitio. Las cookies no relacionadas agregan sobrecarga a cada solicitud.
* Utilice WAF, el filtrado de bots o los servicios de eliminación de datos personales, siempre que no cambien nada de lo mencionado anteriormente. Pruebe estos servicios con un grupo de informes de desarrollo o un conjunto de datos antes de aplicarlos al tráfico de producción. Un filtrado excesivamente agresivo puede eliminar datos suficientes como para que los informes no se puedan utilizar.

La configuración de CDN no debe:

* Almacenar en caché solicitudes o respuestas de recopilación de datos. Cada solicitud debe llegar a Adobe.
* Apunte a un nombre de host de origen que no exista.
* Acepte certificados caducados o fije un certificado específico desde el origen. Adobe no admite la entrega de certificados caducados y puede eliminarlos en cualquier momento.

## Configuración de una CDN con un origen de terceros {#third-party-origin}

Un origen de terceros utiliza el certificado propio de Adobe, por lo que su organización no necesita mantener un certificado en los servidores de Adobe.

1. Busque el ID de inquilino de su organización. Ver [Encuentra tu ID de inquilino](collection-domain.md#tenant-id).
1. En la configuración de CDN, establezca el nombre de host de origen en el subdominio de ID de inquilino de `data.adobedc.net`. Por ejemplo, `example.data.adobedc.net`.
1. Habilite la Indicación de nombre de servidor (SNI) para el origen. Establezca el nombre de host SNI en el nombre de host de origen (por ejemplo, `example.data.adobedc.net`), no en el nombre de host del sitio web.
1. Configure su CDN para que cumpla los [requisitos de todas las implementaciones de CDN](#requirements) anteriores.
1. Si cambia el nombre de host al que su implementación envía datos, [actualice su implementación](collection-domain.md#update-implementation). Si mantiene el mismo nombre de host, no es necesario realizar cambios en la implementación.

>[!WARNING]
>
>No establezca su origen en el nombre de host que Adobe proporcionó como destino CNAME, como `hiodsibxvip01.data.adobedc.net`. Ese nombre de host está vinculado al certificado de origen y puede dejar de funcionar cuando se elimina el certificado.

Los orígenes de terceros siempre usan el tipo predeterminado [RDC](rdc.md), de modo que los datos se puedan recopilar en cualquier ubicación de recopilación de datos de Adobe.

## Configuración de una CDN con un origen de origen {#first-party-origin}

Utilice un origen de origen solo si su organización lo requiere. Las razones comunes incluyen:

* La directiva de seguridad requiere un control directo del certificado de origen. Por ejemplo, su organización debe poder revocar el certificado a través de su propia autoridad de certificación.
* Su organización requiere un tipo de RDC [bloqueado por regiones](rdc.md).

1. Póngase en contacto con el Servicio de atención al cliente de Adobe para configurar un [certificado administrado por el cliente](customer-managed-cert.md) para su nombre de host de origen, como `data.example.com`. Si su organización requiere un tipo de RDC bloqueado por regiones, especifíquelo en la solicitud.
1. En la configuración de CDN, establezca el nombre de host de origen en el nombre de host de origen.
1. Habilite la Indicación de nombre de servidor (SNI) para el origen. Establezca el nombre de host SNI en su nombre de host de origen y configure su CDN para esperar que el certificado de origen proceda del origen.
1. Configure su CDN para que cumpla los [requisitos de todas las implementaciones de CDN](#requirements) anteriores.
1. Si cambia el nombre de host al que su implementación envía datos, [actualice su implementación](collection-domain.md#update-implementation). Si mantiene el mismo nombre de host, no es necesario realizar cambios en la implementación.

>[!IMPORTANT]
>
>Su organización es responsable de renovar el certificado administrado por el cliente y proporcionárselo al Servicio de atención al cliente de Adobe antes de que caduque. Si el certificado de los servidores de Adobe caduca, su CDN puede rechazar la conexión y descartar los datos sin notificárselo. Consulte [Renovar su certificado](customer-managed-cert.md#renewals).

## Mover una implementación propia existente a una CDN {#migrate}

Si su organización envía actualmente datos directamente a un nombre de host de origen con un certificado alojado por Adobe, siga los siguientes pasos para pasar a una CDN:

1. Identifique todas las implementaciones que envían datos a su nombre de host de origen, en todos los productos de Adobe. Otros productos, como Adobe Target o Adobe Journey Optimizer, pueden utilizar el mismo nombre de host y un solo certificado puede cubrir muchos nombres de host.
1. Elija un [tipo de origen](#origin-type). Si elige un origen propio, póngase en contacto con el Servicio de atención al cliente de Adobe para convertir el certificado en un [certificado administrado por el cliente](customer-managed-cert.md) antes de que caduque.
1. Configure su CDN. Mantenga su nombre de host existente para que no necesite actualizar sus implementaciones.
1. Antes de que caduque el certificado, señale su nombre de host a la CDN y cambie todas las implementaciones para utilizarlo.
1. [Compruebe sus datos](#check).
1. Si elige un origen de terceros, póngase en contacto con el Servicio de atención al cliente de Adobe para marcar el certificado de origen que desea eliminar.

Una vez que el nombre de host señala a la CDN, Adobe no puede renovar el certificado de origen. Si alguna implementación aún depende del certificado cuando caduca, se pierden datos de esa implementación. Ponerse en contacto con el Servicio de atención al cliente de Adobe permite a su organización controlar cuándo se elimina el certificado.

## Compruebe sus datos {#check}

Adobe no puede validar la configuración de CDN. Después de enrutar la recopilación de datos a través de su CDN, compare los datos antes y después del cambio:

* Los datos siguen llegando en los grupos de informes, flujos de datos o conjuntos de datos esperados con el volumen habitual.
* Los informes de geolocalización muestran las ubicaciones de los visitantes, no un número pequeño de ciudades donde se encuentran los servidores de CDN.
* Los recuentos de visitantes únicos no aumentan de forma inesperada.
* En las herramientas para desarrolladores del navegador, las solicitudes de recopilación de datos para su nombre de host se realizan correctamente y las cookies de Adobe se establecen en el mismo dominio que antes.

## Configuraciones erróneas comunes

Se sabe que los siguientes problemas causan problemas de calidad de datos o pérdida de datos. Esta lista no es exhaustiva.

| Síntoma | Causa probable |
| --- | --- |
| Los datos dejan de llegar a un grupo de informes o flujo de datos | La CDN cambia la dirección URL de la solicitud o el nombre de host de origen no existe |
| Los datos dejan de llegar después de que caduque un certificado | La CDN espera un certificado de origen del origen y ese certificado ha caducado |
| Los datos de geolocalización solo muestran unas pocas ciudades | La CDN no agrega el encabezado `X-Forwarded-For` |
| La cantidad de visitantes únicos aumenta inesperadamente | La red de distribución de contenido (CDN) elimina las cookies de Adobe, cambia el encabezado `Host` o cambia el dominio de la cookie |
| A los informes les faltan grandes cantidades de datos | La eliminación de datos personales o las reglas de WAF eliminan demasiadas solicitudes |

## Preguntas frecuentes

+++¿Se aplica esta página a otros productos que no sean Adobe Analytics?

Sí. Esta página se aplica a todos los productos de Adobe que utilizan la recopilación de datos de Adobe, incluidos Customer Journey Analytics, Adobe Experience Platform, Adobe Target y Adobe Journey Optimizer.

+++

+++¿Puede Adobe rechazar los datos que no llegan a través de mi CDN?

No. Actualmente, Adobe no ofrece una forma de restringir la recopilación de datos a solicitudes de su CDN.

+++

+++¿Adobe puede proporcionar o validar una configuración para mi CDN?

No. Las opciones de configuración de CDN difieren entre los proveedores y cambian con el tiempo. Póngase en contacto con su proveedor de CDN para obtener ayuda con la configuración de su CDN y consulte [Comprobar sus datos](#check) para ver formas de identificar problemas con su configuración.

+++
