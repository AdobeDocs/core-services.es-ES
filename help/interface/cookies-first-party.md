---
description: Obtenga información sobre cómo Adobe Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imágenes y sesiones de explorador.
keywords: cookies;privacidad
solution: Experience Cloud,Analytics
title: '"Cookies de origen "'
index: y
snippet: y
feature: Cookies
topic: Administración
role: Administrator
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 145040facf70c6bde5c6c3fae9c7ed7f520c188d
workflow-type: tm+mt
source-wordcount: '1579'
ht-degree: 60%

---

# Acerca de las cookies de origen

Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imagen y sesiones del navegador. Si es posible, Adobe utiliza cookies de origen para registrar las actividades del sitio. Para registrar la actividad en distintos sitios, como otros de sus dominios, se requieren cookies de terceros.

Muchos navegadores y aplicaciones antispyware están diseñados para rechazar y eliminar las cookies de terceros, incluidas las cookies utilizadas en la recopilación de datos [!DNL Analytics]. Para admitir el seguimiento de cómo los visitantes interactúan con el sitio web, debe configurar la recopilación de datos para que utilice cookies de origen:

Hay dos opciones disponibles para implementar cookies de origen:

* Si utiliza el servicio de identidad de Experience Platform (servicio ECID), establece cookies automáticamente en el contexto de origen mediante JavaScript.
* Si utiliza [!DNL Analytics] identificadores heredados (también conocidos como la cookie `s_vi` ), dependerá de cómo haya configurado el servidor de recopilación de datos. Si el servidor de recopilación de datos coincide con el dominio del sitio, las cookies se establecen como propias. Si el servidor de recopilación no coincide con su dominio actual, las cookies se establecen como terceros. En este caso, si se bloquean las cookies de terceros, [!DNL Analytics] establece un [id de reserva (s_fid)](cookies-analytics.md) de origen en lugar de la cookie estándar &quot;s_vi&quot;.

Para asegurarse de que el servidor de recopilación coincide con el dominio del sitio, puede utilizar una implementación CNAME en la que las cookies se puedan configurar en un contexto de origen. Esto implica cambios en la configuración DNS de su compañía para configurar un alias CNAME que señale a un dominio alojado de Adobe. Tenga en cuenta que, aunque varios productos de Adobe admiten el uso de un CNAME, en todos los casos se utiliza el CNAME para crear un punto final de confianza para un cliente específico y es propiedad de dicho cliente. Si controla varios dominios, pueden utilizar un único extremo CNAME para rastrear a los usuarios en sus dominios, pero siempre que el dominio del sitio no coincida con las cookies de dominio CNAME esté establecido como terceros.

>[!NOTE]
>
>Para ambas opciones, el programa Intelligent Tracking Prevention (ITP) de Apple hace que las cookies de origen tengan una duración corta en los navegadores que se rigen por ITP, que incluyen Safari en macOS y todos los navegadores en iOS y iPadOS. A partir de noviembre de 2020, ambos tipos de cookies tienen una caducidad de siete días. Esta caducidad está sujeta a cambios.

En la segunda opción, si el sitio tiene páginas seguras mediante el protocolo HTTPS, puede trabajar con Adobe para obtener un certificado SSL a fin de implementar cookies de origen. Adobe recomienda usar HTTPS exclusivamente para la recopilación de datos, ya que el Adobe dejará de admitir la recopilación de HTTP en el segundo semestre de 2020.

El proceso de publicación de certificados SSL puede resultar confuso y requerir mucho tiempo. Como resultado, Adobe estableció una asociación con DigiCert, una autoridad certificadora (CA) líder del sector, y desarrolló un proceso integrado mediante el cual la compra y gestión de estos certificados es automatizada.

Con su permiso, trabajamos con CA para emitir, implementar y administrar un nuevo certificado SHA-2 SSL para usted. Adobe continúa administrando este certificado y asegurándose de que un problema inesperado de caducidad, revocación o seguridad no afecte a la disponibilidad de la colección segura de su organización.

## Programa de certificados administrados por Adobe

El programa de certificados administrados de Adobe es el proceso recomendado para implementar un nuevo certificado SSL de origen para cookies de origen.

El programa de certificados administrados le permite implementar un nuevo certificado SSL de origen para cookies de origen sin coste adicional (para sus primeros 100 CNAME). Si actualmente tiene su propio certificado SSL administrado por el cliente, hable con el Servicio de atención al cliente de Adobe sobre la migración al Programa de certificados administrados por el Adobe.

### Implementación

Así se implementa un nuevo certificado SSL de origen para cookies de origen:

1. Complete el [Formulario de solicitud de cookies de origen](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx) y abra un ticket con el Servicio de atención al cliente solicitando la configuración de cookies de origen en el programa administrado por Adobe. Cada campo se describe dentro del documento con ejemplos.

2. Cree registros CNAME (consulte las instrucciones más abajo).

   Una vez recibida la incidencia, un especialista del Servicio de atención al cliente le proporcionará un par de registros CNAME. Estos registros deben configurarse en el servidor DNS de su empresa antes de que Adobe pueda adquirir el certificado en su nombre. El CNAME es similar al siguiente:

   **Seguro**: Por ejemplo, el nombre de host `smetrics.example.com` señala a `example.com.adobedc.net`.

>[!NOTE]
> En el pasado, Adobe recomendó que los clientes configuraran dos CNAME, uno para HTTPS y otro para HTTP. Dado que es una práctica recomendada encriptar el tráfico y que la mayoría de los exploradores desaconsejan enormemente la función HTTP, ya no se recomienda configurar un CNAME para HTTP. Si lo necesita, tendría este aspecto:
>    **No seguro**: el nombre de host `metrics.example.com` apunta a `example.com.adobedc.net`.

1. Cuando se establece el CNAME, Adobe trabaja con DigiCert para adquirir e instalar un certificado en los servidores de producción de Adobe.

   Si tiene una implementación existente, debe considerar la migración de visitantes para mantener a los existentes. Una vez que el certificado se haya insertado en el entorno de producción de Adobe, podrá actualizar las variables del servidor de seguimiento a los nuevos nombres de host. Es decir, si el sitio no es seguro (HTTP), actualice el `s.trackingServer`. Si el sitio es seguro (HTTPS), actualice ambos `s.trackingServer` y las variables de `s.trackingServerSecure`.

2. [Valide el reenvío de nombres de host](#validate) (como aparece más abajo).

3. [Actualizar código de implementación](#update) (como aparece más abajo).

### Mantenimiento y renovaciones

Los certificados SSL expiran cada año, lo que significa que Adobe debe adquirir un certificado nuevo para cada implementación por año. Todos los usuarios con asistencia técnica de su organización reciben una notificación por correo electrónico cada vez que una implementación está cerca de caducar. Para que Adobe renueve su nombre de host, un usuario admitido deberá responder al correo electrónico de Adobe e indicar que desea continuar utilizando el nombre de host expirado para la recopilación de datos. En ese momento, Adobe compra e instala automáticamente un nuevo certificado.

### Preguntas frecuentes

| Pregunta | Respuesta |
|---|---|
| **¿Es seguro este proceso?** | Sí, el programa administrado por Adobe es más seguro que nuestro método heredado, ya que ningún certificado o clave privada cambia de manos fuera del Adobe y de la autoridad emisora de certificados. |
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
> Si sigue utilizando no seguro, tendrá este aspecto:
> * **Nombre del host no SSL**: `metrics.mysite.com`
> * **CNAME no de SSL**: `mysite.com.adobedc.net`


Mientras no se modifique el código de implementación, este paso no afectará a la recopilación de datos y se puede llevar a cabo en cualquier momento después de la implementación del código.

>[!NOTE]
>
>El servicio ID de visitante de Experience Cloud proporciona una alternativa para configurar un CNAME para habilitar cookies de origen.

## Validar reenvío de nombre de host {#validate}

Los siguientes métodos están disponibles para la validación:

### Validación mediante un explorador

Si tiene un CNAME configurado y el certificado instalado, puede utilizar el explorador para la validación:

`https://smetrics.adobe.com/_check`

>[!NOTE]
>
>Se le envía una advertencia de seguridad si no hay un certificado instalado.

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

Puede utilizar `nslookup` para la validación. Con `smetrics.adobe.com` a modo de ejemplo, abra un símbolo del sistema y escriba `nslookup smetrics.adobe.com`

Si todo está configurado correctamente, verá un resultado similar a:

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

Antes de editar el código del sitio para usar cookies de origen, complete estos requisitos previos:

* Solicite un certificado SSL siguiendo los pasos descritos anteriormente en la sección *Implementar* del [Programa de certificados administrados por Adobe](#adobe-managed-certificate-program).
* Cree registros CNAME (consultar más arriba).
* Valide los nombres de host (consulte más arriba).

Después de comprobar que sus nombres de host responden y redirigen a servidores de recopilación de datos de Adobe, puede modificar su implementación para que apunte a sus propios nombres de host de recopilación de datos.

1. Abra su archivo principal de JavaScript (`s_code.js/AppMeasurement.js`).
1. Si desea actualizar su versión del código, sustituya todo el archivo `s_code.js/AppMeasurement.js` por la versión más reciente y reemplace todos los plugins o personalizaciones (si hay). **O bien**, si desea actualizar el código en relación con las cookies de origen, busque las variables s.trackingServer y s.trackingServerSecure (si utiliza SSL) y agréguelas a los nuevos nombres de host de recopilación de datos. Uso de mysite.com como ejemplo: `s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Cargue en su sitio el archivo principal de JavaScript actualizado.

1. Si está migrando a cookies de origen desde una implementación antigua, o cambiando a un nombre de host de recopilación de origen diferente, Adobe recomienda migrar los visitantes del dominio anterior al nuevo dominio.

Consulte [Migración de visitantes](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/visitor-migration.html?lang=en) en la Guía de implementación de Analytics.

Después de haber cargado el archivo de JavaScript, ya estará todo configurado para la recopilación de datos de cookies de origen. Adobe recomienda supervisar los informes de Analytics durante las siguientes horas para garantizar que la recopilación de datos continúe con normalidad. Si no es así, compruebe que se han realizado todos los pasos anteriores e indique a uno de los usuarios admitidos en su organización que contacte con el servicio de atención al cliente.
