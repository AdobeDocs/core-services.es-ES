---
title: Certificados administrados por el cliente
description: Aprenda cuándo utilizar un certificado administrado por el cliente para la recopilación de datos de origen y las responsabilidades de su organización para renovarlo.
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
source-git-commit: 18fd590d6f0fd1800e3d5c62851453aa91d9db5f
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 1%
---
# Certificados administrados por el cliente

Con un certificado administrado por el cliente, su organización obtiene el certificado para el nombre de host de recopilación de datos de origen y lo proporciona a Adobe. Adobe aloja el certificado en sus servidores de recopilación de datos. Su organización es responsable de renovar el certificado y proporcionar cada certificado renovado a Adobe antes de que caduque el certificado actual.

>[!TIP]
>
>Adobe recomienda el [programa de certificados administrado por Adobe](adobe-managed-cert.md) para la mayoría de las implementaciones de origen. Es más seguro y renueva los certificados automáticamente. Utilice un certificado administrado por el cliente solo cuando su organización lo requiera.

## Cuándo utilizar un certificado administrado por el cliente

* **La recopilación de datos se enruta a través de una red de distribución de contenido (CDN) con un origen propio**: el [programa de certificados administrados por Adobe](adobe-managed-cert.md) no admite implementaciones de CDN. Consulte [Configurar una red de distribución de contenido (CDN) con un origen propio](cdn.md#first-party-origin).
* **Su directiva de seguridad requiere control directo del certificado**: Por ejemplo, su organización debe poder revocar el certificado a través de su propia autoridad de certificación, en lugar de solicitar la revocación a través del Servicio de atención al cliente de Adobe.
* **Su organización requiere una entidad emisora de certificados específica o un tipo de certificado**: El programa de certificados administrado por Adobe usa certificados emitidos por DigiCert.

## Comparar métodos de certificado

| | Certificado administrado por Adobe | Certificado administrado por el cliente |
| --- | --- | --- |
| **Quién obtiene el certificado** | Adobe, a través de DigiCert | Su organización, a través de una autoridad de certificación comercial de su elección |
| **Renovaciones** | Adobe renueva el certificado automáticamente | Su organización renueva el certificado y lo proporciona a Adobe antes de cada caducidad |
| **Tipos de certificados** | Adobe proporciona certificados RSA y ECC | Se requiere RSA; se recomienda ECC |
| **Compatible con una red de distribución de contenido (CDN)** | No | Sí, como origen de origen |

## Configurar un certificado administrado por el cliente

1. Póngase en contacto con el Servicio de atención al cliente de Adobe para solicitar la recopilación de datos de origen con un certificado administrado por el cliente. Incluya su nombre de host de origen, como `data.example.com`. Si su organización tiene requisitos de conformidad o residencia de datos, especifique el [tipo de RDC](rdc.md) que desee en su solicitud.
1. El Servicio de atención al cliente de Adobe proporciona una solicitud de firma de certificado (CSR) para su nombre de host. Adobe genera y mantiene la clave privada para que su organización nunca la gestione. Adobe requiere un certificado RSA y recomienda un certificado ECC. Cada tipo de certificado requiere su propio CSR, por lo que si desea un certificado ECC, solicite al Servicio de atención al cliente de Adobe un CSR ECC.
1. Envíe cada CSR a la autoridad de certificación comercial deseada para obtener un certificado firmado. No se admiten los servicios de certificados gratuitos. Proporcione los certificados emitidos a Adobe según las instrucciones del Servicio de atención al cliente.
1. Una vez que Adobe instale el certificado, dirija el tráfico del nombre de host a Adobe:
   * **Sin una CDN**: Actualice los registros DNS de su organización según las instrucciones del Servicio de atención al cliente de Adobe.
   * **Con una CDN**: establezca el origen de la CDN en el nombre de host de origen. Consulte [Configurar una red de distribución de contenido (CDN) con un origen propio](cdn.md#first-party-origin).
1. Si su implementación aún no envía datos a este nombre de host, [actualice su implementación](collection-domain.md#update-implementation).

## Renovar el certificado {#renewals}

Su organización es responsable de renovar su certificado y de proporcionar el certificado renovado al Servicio de atención al cliente de Adobe antes de que caduque el certificado actual.

Si caduca el certificado en los servidores de Adobe, los exploradores y CDN rechazan las conexiones con el nombre de host y se pierden datos de esas solicitudes. Una CDN puede descartar estos datos sin notificárselo.

La duración máxima de los certificados está disminuyendo, lo que hace que las renovaciones sean más frecuentes. Consulte [6.3.2 Períodos operativos del certificado y períodos de uso del par de claves](https://cabforum.org/working-groups/server/baseline-requirements/requirements/#632-certificate-operational-periods-and-key-pair-usage-periods) en los Requisitos de línea de base del certificado del servidor de CA/Browser Forum para obtener más información. Para evitar lagunas en la recopilación de datos:

* Rastree la fecha de caducidad de cada certificado que proporcione a Adobe.
* Asigne un propietario para renovaciones y documente el proceso de renovación para que continúe con los cambios de personal.

Adobe está explorando actualmente un proceso de renovación de certificados de autoservicio.

## Dejar de usar un certificado administrado por el cliente

* **Para pasar al programa de certificados administrado por Adobe**: Póngase en contacto con el Servicio de atención al cliente de Adobe. El programa de certificados administrado por Adobe requiere que el nombre de host apunte directamente a Adobe, no a una CDN.
* **Para dejar de usar el nombre de host propio**: Actualice todas las implementaciones que usan el nombre de host y, a continuación, póngase en contacto con el Servicio de atención al cliente de Adobe para quitar el certificado de los servidores de Adobe.
* **Para pasar a una CDN con un origen de terceros**: Consulte [Mover una implementación de origen existente a una CDN](cdn.md#migrate).
