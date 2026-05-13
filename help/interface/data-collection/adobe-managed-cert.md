---
description: Obtenga información sobre cómo configurar certificados seguros para utilizarlos con cookies de origen de Adobe CX Enterprise.
solution: Experience Cloud,Analytics
title: Programa de certificados administrados por Adobe
index: true
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
TQID: https://experienceleague.adobe.com/LWbjh-jXKmY6mcl047uzA1ZkhZlAmeNpt9JRg3Ynt9E
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7aid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: c8add8f2-4250-4fd9-9cde-9707036c567did: d2311670-43bd-4c2e-bc98-1da2aaba9cefid: e992d880-33bc-4949-a648-aa7d410276cdid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 1243
ht-degree: 2%

---

# Programa de certificados administrados por Adobe

El programa de certificados administrado por Adobe es el proceso recomendado para configurar certificados de origen necesarios para una implementación CNAME. El programa está completamente automatizado una vez configurado. Renueva los certificados a tiempo para que la recopilación de datos no se vea afectada por los certificados caducados. El programa es gratuito para sus primeros 100 CNAME.

Si administra actualmente sus propios certificados, es responsable de adquirir, mantener y proporcionar un certificado a Adobe para el uso de cookies de origen. Puede ponerse en contacto con el Servicio de atención al cliente de Adobe para hablar sobre la migración al programa de certificados administrados por Adobe.

## Implementación

Siga estos pasos para implementar un nuevo certificado para la recopilación de datos de origen:

1. Descargue y rellene el [formulario de solicitud de dominio de origen](cookies/assets/First_Party_Domain_Request_Form.xlsx)
1. Abra un ticket con el Servicio de atención al cliente de Adobe solicitando la configuración de recopilación de datos de origen en el programa de certificados administrados de Adobe. Si su organización tiene requisitos de conformidad o residencia de datos, especifique el [tipo de RDC](rdc.md) que desee en su solicitud.
1. Una vez recibida la incidencia, el representante de Adobe le proporcionará un registro CNAME. Este registro debe configurarse en el servidor DNS de su empresa antes de que Adobe pueda adquirir el certificado en su nombre. Por ejemplo, el nombre de host `data.example.com` señala a `hiodsibxvip01.data.adobedc.net`.
1. Cuando se establezca el registro CNAME en los servidores de su organización, Adobe colaborará con DigiCert para adquirir e instalar un certificado en los servidores de recopilación de datos de Adobe.

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

Una vez validado que el certificado funciona correctamente, puede actualizar la implementación de Adobe para utilizar el nuevo nombre de host CNAME.

* **Extensión de etiqueta Web SDK**: actualice el campo [[!UICONTROL Edge domain]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/general) al configurar la extensión.
* **Web SDK (aleación)**: actualice la propiedad [`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/edgedomain) dentro del comando `configure`.
* **Extensión de Adobe Analytics**: actualice el campo [[!UICONTROL SSL Tracking Server]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/analytics/overview) al configurar la extensión. Asegúrese de tener también instalada la extensión de etiqueta [Servicio de ID de visitante](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/id-service/overview). Consulte [Identificación de visitante con la extensión de etiquetas de Analytics](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/analytics-extension) para obtener más información.
* **AppMeasurement**: Actualice la variable de configuración [`trackingServerSecure`](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/config-vars/trackingserversecure). Asegúrese de que también ha implementado el [Servicio de identificación del visitante](https://experienceleague.adobe.com/es/docs/id-service/using/home) mediante `VisitorAPI.js`. Consulte [Identificación de visitante con AppMeasurement](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/appmeasurement) para obtener más información.

Si su sitio utiliza varios métodos de implementación y no puede actualizarlos todos simultáneamente, considere la posibilidad de configurar un periodo de gracia. Consulte [Consideraciones sobre la migración del servicio de ID de visitante](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/migration) para ver pasos adicionales sobre cómo evitar que los visitantes se contabilicen como nuevos visitantes en el sitio.

## Mantenimiento y renovaciones

Treinta días antes de que caduque el certificado de origen, Adobe valida si el CNAME sigue siendo válido y está en uso. Si es así, Adobe supone que desea seguir utilizando el servicio y renueva automáticamente el certificado en su nombre.

>[!IMPORTANT]
>
>Si el registro CNAME de su organización se elimina o ya no se asigna al nombre de host seguro de Adobe proporcionado, Adobe no podrá renovar el certificado. La entrada en el sistema de Adobe está marcada para su eliminación sin más comunicación.

## Preguntas frecuentes

+++¿Es seguro este proceso?

Sí. El programa de certificados administrado por Adobe es más seguro que su organización que proporciona un certificado a Adobe. Ningún certificado o clave privada se transfiere fuera de Adobe y de la autoridad emisora de certificados.

+++

+++¿Cómo puede adquirir Adobe un certificado para nuestro dominio?

El certificado solo se puede adquirir si ha señalado el nombre de host especificado a un nombre de host de Adobe. Básicamente, delega este nombre de host a Adobe y permite que Adobe compre el certificado en su nombre.

+++

+++¿Puedo solicitar que se revoque el certificado?

Sí. Como propietario del dominio, tiene derecho a solicitar que se revoque el certificado. Póngase en contacto con el Servicio de atención al cliente de Adobe para iniciar este proceso.

+++

+++¿Qué tipo de cifrado se utiliza?

Adobe trabaja con DigiCert para emitir un certificado SHA-2.

+++

+++¿Este programa incurre en algún costo adicional?

No. Adobe ofrece este servicio a todos los clientes de Adobe CX Enterprise sin coste adicional.

+++

+++¿Qué niveles de seguridad de cifrado ofrece Adobe?

Adobe ofrece dos niveles de seguridad de cifrado para satisfacer las distintas necesidades de seguridad de los clientes en la recopilación de datos de origen. Estos niveles determinan qué algoritmos de cifrado son compatibles con las conexiones HTTPS con servidores de Adobe. Adobe revisa y actualiza regularmente el conjunto de algoritmos admitidos en función de las prácticas de seguridad actuales. Si desea cambiar la configuración de seguridad de cifrado, póngase en contacto con el Servicio de atención al cliente.

* **Estándar** requiere TLS 1.2 o posterior y cifrado de al menos 128 bits. Está diseñado para proporcionar la mayor compatibilidad de dispositivos al tiempo que mantiene el cifrado seguro.
* **Alta** requiere TLS 1.2 o posterior y elimina la compatibilidad con cifrados más débiles. Está diseñado para los clientes que desean el cifrado más potente y no les preocupa la compatibilidad con dispositivos más antiguos.

Se sabe que los siguientes clientes no pueden conectarse con la seguridad de cifrado establecida en **High**:

* Windows 8.1 y anteriores (última actualización en 2018)
* Windows Phone 8.1 y anteriores (última actualización en 2016)
* OS X 10.10 y anteriores (última actualización en 2017)
* iOS 8.4 y anteriores (última actualización en 2015)

+++

+++¿Qué tipos de certificados HTTPS son compatibles?

Adobe admite tipos de certificados RSA y ECC para satisfacer las distintas necesidades de los clientes. Los certificados RSA son más compatibles con los clientes, pero los certificados ECC utilizan menos procesamiento tanto en el servidor como en el lado del cliente. Para los certificados administrados por Adobe, se proporcionan RSA y ECC. Para los certificados administrados por el cliente, se requiere RSA y se recomienda ECC. Los clientes modernos admiten RSA y ECC. Los siguientes clientes solo suelen admitir certificados RSA:

* Windows Vista y versiones anteriores (última actualización en 2012)
* Windows Phone 8.0 y anteriores (última actualización en 2014)
* OS X 10.8 y anteriores (última actualización en 2013)
* iOS 5.1 y anteriores (última actualización en 2012)
* Android 4.3 y anteriores (última actualización en 2013)

+++

+++¿Puedo administrar mis propios certificados en su lugar?

Sí. Sin embargo, si administra sus propios certificados, es responsabilidad suya renovar los suyos y proporcionárselos a Adobe cada vez que los renueve. Este proceso es menos seguro y puede provocar lagunas en la recopilación de datos si su organización olvida renovar un certificado a tiempo. Adobe recomienda utilizar el programa de certificados administrados en lugar de administrar los certificados usted mismo, especialmente debido a las reducciones en la duración máxima del certificado TLS. Consulte [6.3.2 Períodos operativos del certificado y períodos de uso del par de claves](https://cabforum.org/working-groups/server/baseline-requirements/requirements/#632-certificate-operational-periods-and-key-pair-usage-periods) en los Requisitos de línea de base del certificado del servidor de CA/Browser Forum para obtener más información.
+++

