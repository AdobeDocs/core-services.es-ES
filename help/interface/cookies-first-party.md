---
description: Obtenga información sobre cómo Adobe Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imágenes y sesiones de explorador.
keywords: cookies,privacidad
solution: Experience Cloud,Analytics
title: '"Cookies de origen "'
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 1e7c4c02b08a17b2666afc7a82ea44d598675b3c
workflow-type: ht
source-wordcount: '1614'
ht-degree: 100%

---

# Acerca de las cookies de origen

Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imagen y sesiones del navegador. Si es posible, Adobe utiliza cookies de origen para registrar las actividades del sitio. Para registrar la actividad en distintos sitios, como otros de sus dominios, se requieren cookies de terceros.

Muchos exploradores y aplicaciones antispyware están diseñados para rechazar y eliminar las cookies de terceros. Adobe garantiza que las cookies siempre se puedan configurar, aunque las de terceros estén bloqueadas. El comportamiento específico varía en función de si utiliza el servicio de identidad de Experience Platform (servicio ECID) o los identificadores heredados de Analytics (también conocidos como cookie s_vi):

* El [servicio de identidad de Experience Platform (servicio ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=es) configurará automáticamente las cookies de origen independientemente de si el dominio de recopilación coincide con el del sitio. Si no coinciden, el servicio de identidad utilizará JavaScript para configurar las cookies en el dominio del sitio.
* Si utiliza [identificadores heredados de Analytics](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=es) (también conocidos como cookie `s_vi`), depende de cómo haya configurado su servidor de recopilación de datos. Si el servidor de recopilación de datos coincide con el dominio del sitio, las cookies se establecen como cookies de origen. Si el servidor de colección no coincide con su dominio actual, las cookies se configuran como de terceros. En este caso, si se bloquean las cookies de terceros, Analytics establece un [identificador de reserva (s_fid)](cookies-analytics.md) de origen en lugar de la cookie “s_vi” estándar.

Si desea asegurarse de que el servidor de recopilación coincida con el dominio de su sitio, puede utilizar una implementación CNAME que habilitará el reenvío de un dominio personalizado especificado en su implementación CNAME a los servidores de recopilación de Adobe. Esto implica cambios en la configuración DNS de su compañía para configurar un alias CNAME que señale a un dominio alojado de Adobe. Tenga en cuenta que, aunque varios productos de Adobe admiten el uso de un CNAME, en todos los casos se utiliza el CNAME para crear un punto final de confianza para un cliente específico y es propiedad de dicho cliente. Si controla varios dominios, pueden utilizar un único extremo CNAME para rastrear a los usuarios en sus dominios, pero siempre que el dominio del sitio no coincida con las cookies de dominio CNAME se establece como de terceros.

>[!NOTE]
>
>Independientemente de si el dominio de recopilación coincide con el del sitio, el programa Intelligent Tracking Prevention (ITP) de Apple crea las cookies de origen configuradas por Adobe de corta duración en exploradores que se rigen por ITP, que incluyen Safari en macOS y todos en iOS y iPadOS. A partir de noviembre de 2020, las cookies configuradas mediante CNAME también tienen la misma caducidad que las configuradas mediante JavaScript. Esta caducidad está sujeta a cambios.

Si desea establecer un CNAME para la recopilación de datos y si el sitio tiene páginas seguras mediante el protocolo HTTPS, puede trabajar con Adobe para obtener un certificado SSL.

El proceso de publicación de certificados SSL puede resultar confuso y requerir mucho tiempo. Por ello, Adobe estableció una sociedad con DigiCert, una autoridad certificadora (AC) líder en su sector, y desarrolló un proceso integrado por el cual la compra y administración de estos certificados está automatizada.

Con su permiso, trabajamos con nuestra AC para emitir, implementar y administrar un nuevo certificado SHA-2 SSL para usted. Adobe sigue administrando este certificado y asegurándose de que el problema de caducidad, revocación o seguridad no afecte a la disponibilidad de la colección de las organizaciones.

## Programa de certificados administrados por Adobe

El programa de certificados administrados de Adobe es el proceso recomendado para configurar el certificado SSL de origen necesario para una implementación CNAME que garantiza que el servidor de recopilación de Adobe coincida con el dominio del sitio.

El programa de certificados administrados por Adobe le permite implementar un nuevo certificado SSL de origen sin coste adicional (para sus primeros 100 CNAME). Si tiene su propio certificado SSL administrado por el cliente, hable con el Servicio de atención al cliente de Adobe acerca de la migración al programa de Certificados administrados de Adobe.

### Implementación

Así se implementa un nuevo certificado SSL de origen para la recopilación de datos de origen:

1. Complete el [Formulario de solicitud de dominio de origen](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx) y abra una incidencia con el Servicio de atención al cliente al solicitar la configuración de recopilación de datos de origen en el programa administrado por Adobe. Cada campo se describe dentro del documento con ejemplos.

2. Cree registros CNAME (consulte las instrucciones más abajo).

   Una vez recibida la incidencia, un especialista del Servicio de atención al cliente le proporcionará un par de registros CNAME. Estos registros deben configurarse en el servidor DNS de su empresa antes de que Adobe pueda adquirir el certificado en su nombre. Los CNAME presentan un aspecto similar al siguiente:

   **Seguro**: Por ejemplo, el nombre de host `smetrics.example.com` señala a `example.com.adobedc.net`.

>[!NOTE]
> En el pasado, Adobe recomendaba a los clientes que configurasen dos CNAME: uno para HTTPS y otro para HTTP. Dado que es una práctica recomendada cifrar el tráfico y que la mayoría de los exploradores desaconsejan enormemente la función HTTP, ya no se recomienda configurar un CNAME para HTTP. Si lo necesita, tendría este aspecto:
>    **No seguro**: el nombre de host `metrics.example.com` apunta a `example.com.adobedc.net`.

1. Cuando se establezca el CNAME, Adobe colaborará con DigiCert para adquirir e instalar un certificado en los servidores de producción de Adobe.

   Si tiene una implementación existente, debe considerar la migración de visitantes para mantener a los existentes. Una vez que el certificado se haya insertado en el entorno de producción de Adobe, podrá actualizar las variables del servidor de seguimiento a los nuevos nombres de host. Es decir, si el sitio no es seguro (HTTP), actualice el `s.trackingServer`. Si el sitio es seguro (HTTPS), actualice ambos `s.trackingServer` y las variables de `s.trackingServerSecure`.

2. [Valide el reenvío de nombres de host](#validate) (como aparece más abajo).

3. [Actualizar código de implementación](#update) (como aparece más abajo).

### Mantenimiento y renovaciones

Los certificados SSL expiran cada año, lo que significa que Adobe debe adquirir un certificado nuevo para cada implementación por año. Todos los usuarios admitidos de su organización reciben una notificación por correo electrónico cada vez que una implementación esté cerca de expirar. Para que Adobe renueve su nombre de host, un usuario admitido deberá responder al correo electrónico de Adobe e indicar que desea continuar utilizando el nombre de host expirado para la recopilación de datos. En ese momento, Adobe compra e instala automáticamente un nuevo certificado.

### Preguntas frecuentes

| Pregunta | Respuesta |
|---|---|
| **¿Es seguro este proceso?** | Sí, el programa administrado de Adobe es más seguro que nuestro método heredado, ya que ningún certificado o clave privada se transfiere fuera de Adobe y la autoridad emisora de certificados. |
| **¿Cómo puede adquirir Adobe un certificado para nuestro dominio?** | El certificado solo se puede adquirir si ha señalado el nombre de host especificado (por ejemplo, `telemetry.example.com`) a un nombre de host de Adobe. Básicamente, delega este nombre de host a Adobe y permite que Adobe compre el certificado en su nombre. |
| **¿Puedo solicitar que se revoque el certificado?** | Sí, como propietario del dominio, tiene derecho a solicitar que se revoque el certificado. Solo tendrá que abrir una incidencia con el Servicio de atención al cliente para completarlo. |
| **¿Utilizará este certificado el cifrado SHA-2?** | Sí, Adobe trabajará con DigiCert para emitir un certificado SHA-2. |
| **¿Supone un costo adicional?** | No, Adobe ofrece este servicio a todos los clientes actuales de Adobe Digital Experience sin coste adicional. |

{style=&quot;table-layout:auto&quot;}

## Creación de registros CNAME

El equipo de operaciones de red de su organización debe configurar los servidores DNS creando registros CNAME. Cada nombre de host envía datos a los servidores de recopilación de datos de Adobe.

El especialista de FPC le proporciona los nombres de host configurados y los CNAME a los que se va a señalar. Por ejemplo:

* **Nombre del host SSL**: `smetrics.mysite.com`
* **CNAME de SSL**: `mysite.com.adobedc.net`

>[!NOTE]
> Si sigue utilizando el método no seguro, el aspecto será este:
> * **Nombre del host no SSL**: `metrics.mysite.com`
> * **CNAME no de SSL**: `mysite.com.adobedc.net`


Mientras no se modifique el código de implementación, este paso no afectará a la recopilación de datos y se puede llevar a cabo en cualquier momento después de la implementación del código.

## Validar reenvío de nombre de host {#validate}

Los siguientes métodos están disponibles para la validación:

### Validación mediante un explorador

Si tiene un CNAME configurado y el certificado instalado, puede utilizar el explorador para la validación:

`https://smetrics.adobe.com/_check`

>[!NOTE]
>
>Verá una advertencia de seguridad si no hay un certificado instalado.

### Validar mediante [!DNL curl]

Adobe recomienda utilizar [[!DNL curl]](https://curl.se/) desde la línea de comandos. (Los usuarios de [!DNL Windows] pueden instalar [!DNL curl] desde: <https://curl.se/windows/>)

Si tiene un CNAME pero no hay ningún certificado instalado, ejecute:
`curl -k https://smetrics.adobe.com/_check`
Respuesta: `SUCCESS`

(El valor `-k` desactiva la advertencia de seguridad.)

Si tiene un CNAME configurado y el certificado está instalado, ejecute:
`curl https://smetrics.adobe.com/_check`
Respuesta: `SUCCESS`

### Validar mediante [!DNL nslookup]

Puede utilizar `nslookup` para la validación. Con `smetrics.adobe.com`a modo de ejemplo, abra un símbolo del sistema y escriba `nslookup smetrics.adobe.com`

Si todo está configurado correctamente, verá un resultado similar al siguiente:

```
nslookup smetrics.adobe.com
Server:             10.30.7.247
Address:     10.30.7.247#53

smetrics.adobe.com    canonical name = adobe.com.ssl.d1.sc.omtrdc.net.
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.218.180.161
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 52.39.8.230
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.187.216.46
```

## Actualización del código de implementación {#update}

Antes de editar el código del sitio para utilizar recopilación de datos de origen, complete estos requisitos previos:

* Solicite un certificado SSL siguiendo los pasos descritos anteriormente en la sección *Implementación* del [Programa de certificados administrados de Adobe](#adobe-managed-certificate-program).
* Cree registros CNAME (consultar más arriba).
* Valide los nombres de host (consultar más arriba).

Después de comprobar que sus nombres de host responden y redirigen a los servidores de recopilación de datos, puede modificar su implementación de modo que señale a sus propios nombres de host de recopilación de datos.

1. Abra su archivo principal de JavaScript (`s_code.js/AppMeasurement.js`).
1. Si desea actualizar su versión del código, sustituya todo el archivo `s_code.js/AppMeasurement.js` por la versión más reciente y reemplace todos los plugins o personalizaciones (si hay). **O bien**, si desea actualizar el código en relación con la recopilación de datos de origen, busque las variables s.trackingServer y s.trackingServerSecure (si utiliza SSL) y diríjalas a los nuevos nombres de host de recopilación de datos. Uso de mysite.com como ejemplo:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Cargue en su sitio el archivo principal de JavaScript actualizado.

1. Si está migrando a recopilación de datos de origen desde una implementación antigua, o cambiando a otro nombre de host de recopilación de origen, Adobe le recomienda migrar a los visitantes del dominio anterior al nuevo dominio.

Consulte [Migración de visitantes](https://experienceleague.adobe.com/docs/analytics/technotes/visitor-migration.html?lang=es) en la Guía de implementación de Analytics.

Después de haber cargado el archivo de JavaScript, ya estará todo configurado para la recopilación de datos de origen. Adobe le recomienda que monitorice los informes de Analytics durante las siguientes horas para asegurarse de que la recopilación de datos continúa con normalidad. Si no es así, compruebe que se han realizado todos los pasos anteriores e indique a uno de los usuarios admitidos en su organización que contacte con el servicio de atención al cliente.
