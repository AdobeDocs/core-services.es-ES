---
description: Obtenga información sobre cómo configurar certificados seguros para utilizarlos con cookies de origen de Adobe Experience Cloud.
solution: Experience Cloud,Analytics
title: programa de certificados administrado por Adobe
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 028b11dfbcfc0c5c9f6fd1c69350574f81f2846b
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 11%

---

# programa de certificados administrado por Adobe

El programa de certificados administrados por Adobe es el proceso recomendado para configurar los certificados de origen necesarios para una implementación CNAME. El programa está completamente automatizado una vez configurado. Renueva los certificados a tiempo para que la recopilación de datos no se vea afectada por los certificados caducados. El programa es gratuito para sus primeros 100 CNAME.

Si administra actualmente sus propios certificados, es responsable de comprar, mantener y proporcionar un certificado para el Adobe para el uso de cookies de origen. Puede ponerse en contacto con el Servicio de atención al cliente de Adobe para discutir la migración al programa de certificados administrados de Adobe.

## Implementación

Siga estos pasos para implementar un nuevo certificado para la recopilación de datos de origen:

1. Descargue y rellene el [Formulario de solicitud de dominio de origen](cookies/assets/First_Party_Domain_Request_Form.xlsx)

1. Abra un ticket con el Servicio de atención al cliente de Adobe solicitando configurar la recopilación de datos de origen en el programa de certificados administrados de Adobe.

1. Una vez recibida la incidencia, el representante del Adobe le proporcionará un registro CNAME. Estos registros deben configurarse en el servidor DNS de su empresa antes de que Adobe pueda adquirir el certificado en su nombre. Por ejemplo, el nombre de host `data.example.com` apunta a `hiodsibxvip01.data.adobedc.net`.

1. Cuando se establezca el registro CNAME en los servidores de su organización, Adobe colaborará con DigiCert para adquirir e instalar un certificado en los servidores de recopilación de datos de Adobe.

## Validar reenvío de nombre de host {#validate}

Una vez que el Adobe ha instalado el certificado, puede utilizar uno de los siguientes métodos para validar que funciona.

+++**Validación del explorador**

Puede utilizar cualquier explorador para validar que un certificado está instalado correctamente. Escriba su CNAME con `_check` como la ruta a la barra de direcciones. Por ejemplo:

`data.example.com/_check`

Si todo funciona, se muestra el explorador `SUCCESS`. Si el certificado no está instalado correctamente, recibirá una advertencia de seguridad.

+++

+++**Línea de comandos (`curl`)**

La mayoría de los sistemas operativos modernos ya tienen [`curl`](https://curl.se) instalado.

Escriba lo siguiente en la línea de comandos:

```sh
curl data.example.com/_check
```

Si todo funciona correctamente, la consola vuelve `SUCCESS`.

>[!TIP]
>
>Puede usar el complemento `-k` Indicador para desactivar la advertencia de seguridad y ayudar a solucionar problemas.

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
Aliases: smetrics.example.com
```

+++

## Actualización del código de implementación {#update}

Una vez que haya validado que el certificado funciona correctamente, puede actualizar la implementación de Adobe para utilizar estos valores.

* Para implementaciones de AppMeasurement de Adobe Analytics, actualice el [`trackingServer`](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/config-vars/trackingserver) variable de configuración. Si tiene una implementación existente, consulte [Migración de visitantes](https://experienceleague.adobe.com/en/docs/analytics/technotes/visitor-migration) para ver pasos adicionales sobre cómo evitar que los visitantes existentes se cuenten como visitantes nuevos.
* Para implementaciones de SDK web, actualice el [`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/edgedomain) dentro de la propiedad [`configure`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview) comando.

## Mantenimiento y renovaciones

Treinta días antes de que caduque el certificado de origen, el Adobe valida si el CNAME sigue siendo válido y está en uso. Si es así, Adobe supone que desea seguir utilizando el servicio y renueva automáticamente el certificado en su nombre.

>[!IMPORTANT]
>
>Si el registro CNAME de su organización se elimina o ya no se asigna al nombre de host seguro de Adobe proporcionado, el Adobe no puede renovar el certificado. La entrada en el sistema del Adobe está marcada para su eliminación sin necesidad de más comunicación.

## Preguntas frecuentes

+++¿Es seguro este proceso?

Sí. El programa de certificados administrados por Adobe es más seguro que su organización que proporciona el Adobe de un certificado. Ningún certificado o clave privada se transfiere fuera del Adobe y de la autoridad emisora de certificados.

+++

+++¿Cómo puede adquirir Adobe un certificado para nuestro dominio?

El certificado solo se puede adquirir si ha señalado el nombre de host especificado a un nombre de host de propiedad del Adobe. Básicamente, delega este nombre de host al Adobe y permite que el Adobe compre el certificado en su nombre.

+++

+++¿Puedo solicitar que se revoque el certificado?

Sí. Como propietario del dominio, tiene derecho a solicitar que se revoque el certificado. Póngase en contacto con el Servicio de atención al cliente de Adobe para iniciar este proceso.

+++

+++¿Qué tipo de cifrado se utiliza?

Adobe funciona con DigiCert para emitir un certificado SHA-2.

+++

+++¿Este programa incurre en algún costo adicional?

No. Adobe ofrece este servicio a todos los clientes de Adobe Experience Cloud sin coste adicional.

+++

+++¿Qué niveles de seguridad de cifrado ofrece el Adobe?

Adobe ofrece dos niveles de seguridad de cifrado para satisfacer las distintas necesidades de seguridad de los clientes en la recopilación de datos de origen. Estos niveles determinan qué algoritmos de cifrado son compatibles con las conexiones HTTPS con servidores de Adobe. El Adobe de revisa y actualiza regularmente el conjunto de algoritmos admitidos en función de las prácticas de seguridad actuales. Si desea cambiar la configuración de seguridad de cifrado, póngase en contacto con el Servicio de atención al cliente.

* **Standard** requiere TLS 1.2 o posterior y cifrado de al menos 128 bits. Está diseñado para proporcionar la mayor compatibilidad de dispositivos al tiempo que mantiene el cifrado seguro.
* **Alta** el nivel de seguridad de cifrado requiere TLS 1.2 o posterior y elimina la compatibilidad con cifrados más débiles. Está diseñado para los clientes que desean el cifrado más potente y no les preocupa la compatibilidad con dispositivos más antiguos.

Se sabe que los siguientes clientes no pueden conectarse con la seguridad de cifrado establecida en **Alta**:

* Windows 8.1 y versiones anteriores (última actualización en 2018)
* Windows Phone 8.1 y versiones anteriores (última actualización en 2016)
* OS X 10.10 y versiones anteriores (última actualización en 2017)
* iOS 8.4 y versiones anteriores (última actualización en 2015)

+++

+++¿Qué tipos de certificados HTTPS son compatibles?

El Adobe admite tipos de certificados RSA y ECC para satisfacer las distintas necesidades de los clientes. Los certificados RSA son más compatibles con los clientes, pero los certificados ECC utilizan menos procesamiento tanto en el servidor como en el lado del cliente. Para los certificados administrados por el Adobe, se proporcionan RSA y ECC. Para los certificados administrados por el cliente, se requiere RSA y se recomienda ECC. Los clientes modernos admiten RSA y ECC. Los siguientes clientes solo suelen admitir certificados RSA:

* Windows Vista y versiones anteriores (última actualización en 2012)
* Windows Phone 8.0 y versiones anteriores (última actualización en 2014)
* OS X 10.8 y versiones anteriores (última actualización en 2013)
* iOS 5.1 y versiones anteriores (última actualización en 2012)
* Android 4.3 y anteriores (última actualización en 2013)

+++
