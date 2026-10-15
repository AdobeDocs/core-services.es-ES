---
description: Obtenga información sobre cómo configurar certificados seguros para utilizarlos con cookies de origen de Adobe CX Enterprise.
solution: Experience Cloud,Analytics
title: Programa de certificados administrados por Adobe
index: true
snippet: 'y'
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
autotag-review: '2026-09-09T20:12:24.943Z'
TQID: 'https://experienceleague.adobe.com/8CSBLQaw3KOByyxxCYr1By4gyAQsDIhiofOdAzn38dg'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
  - id: c8add8f2-4250-4fd9-9cde-9707036c567d
    internal-label: Methods
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
  - id: e992d880-33bc-4949-a648-aa7d410276cd
    internal-label: Validation
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 18fd590d6f0fd1800e3d5c62851453aa91d9db5f
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 2%
---
# Programa de certificados administrados por Adobe

El programa de certificados administrado por Adobe es el proceso recomendado para configurar certificados de origen necesarios para una implementación CNAME. El programa está completamente automatizado una vez configurado. Renueva los certificados a tiempo para que la recopilación de datos no se vea afectada por los certificados caducados. El programa es gratuito para sus primeros 100 CNAME.

El programa de certificados administrado por Adobe no admite la recopilación de datos de enrutamiento a través de una red de entrega de contenido (CDN). Si usa una CDN, consulte [Enrutar la recopilación de datos a través de una CDN](cdn.md). Las organizaciones que necesiten administrar sus propios certificados pueden usar [certificados administrados por el cliente](customer-managed-cert.md) en su lugar. Si actualmente administra sus propios certificados y desea pasar al programa de certificados administrado por Adobe, póngase en contacto con el Servicio de atención al cliente de Adobe.

## Implementación

Para implementar un nuevo certificado para la recopilación de datos de origen, siga estos pasos:

1. Descargue y rellene el [formulario de solicitud de dominio de origen](cookies/assets/First_Party_Domain_Request_Form.xlsx)
1. Abra un ticket con el Servicio de atención al cliente de Adobe solicitando la configuración de recopilación de datos de origen en el programa de certificados administrados de Adobe. Si su organización tiene requisitos de conformidad o residencia de datos, especifique el [tipo de RDC](rdc.md) que desee en su solicitud.
1. Una vez recibida la incidencia, el representante de Adobe le proporcionará un registro CNAME. Este registro debe configurarse en el servidor DNS de su empresa antes de que Adobe pueda adquirir el certificado en su nombre. Por ejemplo, el nombre de host `data.example.com` señala a `hiodsibxvip01.data.adobedc.net`. Si su organización utiliza registros de autorización de autoridad de certificación (CAA) de DNS, asegúrese de que los registros de CAA permiten a DigiCert emitir certificados. Consulte [Mantenimiento y renovaciones](#renewals).
1. Cuando se establezca el registro CNAME en los servidores de su organización, Adobe colaborará con DigiCert para adquirir e instalar un certificado en los servidores de recopilación de datos de Adobe.
1. Si necesita actualizar el archivo `robots.txt` cuando Adobe lo hospeda con CNAME por motivos de origen, póngase en contacto con el Servicio de atención al cliente con una solicitud. Esta solicitud es relevante cuando desea actualizar el archivo `robots.txt` para evitar que Google rastree los subdominios.

## Validar reenvío de nombre de host

Una vez que Adobe ha instalado el certificado, puede utilizar uno de los siguientes métodos para validar que funciona.

+++**Validación del explorador**

Puede utilizar cualquier explorador para validar que un certificado está instalado correctamente. Escriba su CNAME con `_check` como ruta de acceso a la barra de direcciones. Por ejemplo:

`data.example.com/_check`

Si todo funciona, el explorador mostrará `SUCCESS`. Si el certificado no está instalado correctamente, recibirá una advertencia de seguridad.

+++

+++**Línea de comandos (`curl`)**

La mayoría de los sistemas operativos modernos ya tienen [`curl`](https://curl.se) instalado.

Escriba lo siguiente en la línea de comandos:

```sh
curl data.example.com/_check
```

Si todo funciona correctamente, la consola devolverá `SUCCESS`.

>[!TIP]
>
>Puede usar el indicador `-k` para deshabilitar la advertencia de seguridad y solucionar problemas.

+++

+++**Línea de comandos (`nslookup`)**

Escriba lo siguiente en la línea de comandos:

```sh
nslookup data.example.com
```

Si todo funciona correctamente, se devuelven los servidores de recopilación de datos de Adobe:

```text
Server: hiodsibxvip01.corp.adobe.com
Address: 10.50.112.247

Name: example.com.ssl.d1.sc.omtrdc.net
Addresses: 63.140.37.126
    63.140.37.206
    63.140.36.51
    63.140.36.145
Aliases: data.example.com
```

+++

## Actualización del código de implementación

Para utilizar su nuevo nombre de host CNAME, actualice la implementación de Adobe una vez que haya validado que el certificado funciona correctamente. Consulte [Actualizar su implementación](collection-domain.md#update-implementation).

## Mantenimiento y renovaciones {#renewals}

Adobe renueva el certificado automáticamente. Treinta días antes de que caduque el certificado, Adobe valida que el CNAME sigue siendo válido y está en uso y, a continuación, renueva el certificado en su nombre. Para que las renovaciones sigan funcionando, evite los siguientes cambios de DNS:

* **Quitar o volver a señalar el registro CNAME**: si el registro CNAME se quita o ya no señala al nombre de host seguro de Adobe, Adobe no puede renovar el certificado. Esta condición incluye el reenvío del registro CNAME a una red de entrega de contenido (CDN). Si planea usar una CDN, consulte [Mover una implementación de origen existente a una CDN](cdn.md#migrate) antes de cambiar los registros DNS.
* **Adición de registros CAA que no autorizan DigiCert**: Las autoridades de certificación comprueban los registros de autorización de autoridad de certificación (CAA) en su nombre de host y sus dominios principales. Si usa registros de CAA, incluya `digicert.com` como emisor autorizado. Por ejemplo, `example.com. IN CAA 0 issue "digicert.com"`.
* **Restricción de la emisión de DigiCert a una cuenta específica**: La característica de bloqueo de dominios de DigiCert agrega un parámetro `account=` a un registro de CA, como `example.com. IN CAA 0 issue "digicert.com; account=<token>"`. Este parámetro restringe la emisión a la cuenta DigiCert de su organización, incluso si `digicert.com` está autorizado, lo que impide que Adobe obtenga un certificado. Si su organización requiere el bloqueo de dominios DigiCert, use [certificados administrados por el cliente](customer-managed-cert.md) en su lugar. Los bloqueos de dominio establecidos en el registrador de dominios, a veces denominados bloqueos de transferencia, no están relacionados y no afectan a los certificados administrados por Adobe.

>[!IMPORTANT]
>
>Si el registro CNAME ya no apunta al nombre de host seguro de Adobe, la entrada del sistema de Adobe se marca para su eliminación sin más comunicación.

## Preguntas frecuentes

+++¿Es seguro este proceso?

Sí. El programa de certificados administrados por Adobe es más seguro que [certificados administrados por el cliente](customer-managed-cert.md). No se transfiere ningún certificado o clave privada fuera de Adobe ni de la autoridad emisora de certificados.

+++

+++¿Cómo puede adquirir Adobe un certificado para nuestro dominio?

El certificado solo se puede adquirir si ha señalado el nombre de host especificado a un nombre de host de Adobe. Delega este nombre de host en Adobe y permite que Adobe compre el certificado en su nombre.

+++

+++¿Puedo solicitar que se revoque el certificado?

Sí. Como propietario del dominio, tiene derecho a solicitar que se revoque el certificado. Póngase en contacto con el Servicio de atención al cliente de Adobe para iniciar este proceso.

+++

+++¿Qué tipo de cifrado se utiliza?

Adobe trabaja con DigiCert para emitir un certificado SHA-2.

+++

+++¿Este programa incurre en algún costo adicional?

Adobe ofrece este programa a todos los clientes de Adobe CX Enterprise sin coste adicional para los primeros 100 CNAME.

+++

+++¿Qué niveles de seguridad de cifrado ofrece Adobe?

Adobe ofrece dos niveles de seguridad de cifrado para satisfacer las distintas necesidades de seguridad de los clientes en la recopilación de datos de origen. Estos niveles determinan qué algoritmos de cifrado son compatibles con las conexiones HTTPS con servidores de Adobe. Adobe revisa y actualiza regularmente el conjunto de algoritmos admitidos en función de las prácticas de seguridad actuales. Para cambiar la configuración de seguridad de cifrado, póngase en contacto con el Servicio de atención al cliente.

* **Estándar** requiere TLS 1.2 o posterior y cifrado de al menos 128 bits. Está diseñado para proporcionar la mayor compatibilidad de dispositivos al tiempo que mantiene el cifrado seguro.
* **Alta** requiere TLS 1.2 o posterior y elimina la compatibilidad con cifrados más débiles. Está diseñado para los clientes que desean el cifrado más potente. Los clientes publicados antes de 2015 no suelen poder conectarse cuando la seguridad de cifrado está establecida en **Alta**.

+++

+++¿Qué tipos de certificados HTTPS son compatibles?

Adobe admite certificados RSA y ECC, y los clientes modernos admiten ambos tipos de certificados. Los certificados ECC requieren menos procesamiento tanto en el servidor como en el cliente. Para los certificados administrados por Adobe, Adobe proporciona certificados RSA y ECC. Para [certificados administrados por el cliente](customer-managed-cert.md), se requiere RSA y se recomienda ECC.

+++

