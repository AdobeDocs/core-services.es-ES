---
description: Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imagen y sesiones del navegador.
keywords: cookies; privacidad
seo-description: Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imagen y sesiones del navegador.
seo-title: Cookies de terceros
solution: Experience Cloud, Analytics
title: Cookies de terceros
index: y
snippet: y
translation-type: tm+mt
source-git-commit: 2bdc4b7287ccacfc4d968278b2c3ffdaeddfc105

---


# Acerca de las cookies de origen

Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imagen y sesiones del navegador. Estas cookies son inofensivas y se originan en un dominio hospedado por Adobe; se denominan cookies de origen.

Muchos exploradores y aplicaciones antispyware están diseñados para rechazar y eliminar cookies de terceros, incluidos los utilizados en la recopilación de datos de Analytics. Para evitar las limitaciones de seguimiento impuestas por los exploradores y programas, puede implementar cookies de origen.

Hay dos opciones disponibles para implementar cookies individuales

* El servicio Experience Platform ID. El servicio de ID puede establecer la cookie en el contexto de origen mediante JavaScript.
* Entradas DNS en el servidor DNS de las empresas.
* Si su sitio tiene páginas seguras mediante `https:` el protocolo y no utiliza el servicio Experience Platform ID, puede trabajar con Adobe para obtener un certificado SSL con el fin de implementar cookies de origen

El proceso de publicación de certificados SSL puede resultar confuso y requerir mucho tiempo. Como resultado, Adobe estableció una sociedad con digicert, una autoridad certificadora líder del sector (CA), y desarrolló un proceso integrado por el cual la compra y administración de estos certificados es automatizada.

Con su permiso, trabajará con nuestra CA para emitir, implementar y administrar un nuevo certificado SHA -2 SSL. Adobe seguirá administrando este certificado y asegúrese de que el problema de caducidad, revocación o seguridad no afecte a la disponibilidad de la colección segura de las organizaciones.

## Programa de certificados administrados de Adobe

El programa de certificados administrados de Adobe es el proceso recomendado para implementar un nuevo certificado SSL de origen para cookies de origen.

El programa Certificados administrados de Adobe permite implementar un nuevo certificado SSL de origen para cookies de origen sin costes adicionales. Si tiene su propio certificado SSL administrada por el cliente, hable con el Servicio de atención al cliente de Adobe acerca de la migración al programa de certificados administrados de Adobe.

### Implementación

Así se implementa un nuevo certificado SSL de origen para cookies de origen:

1. Complete el formulario ![de solicitud](assets/FPC_Request_Form.xlsx) y abra un ticket con el Servicio de atención al cliente solicitando la configuración de cookies de origen en el programa Administrado de Adobe. Cada campo se describe dentro del documento con ejemplos.

1. Cree registros CNAME (consulte las instrucciones más abajo). Una vez recibidos el ticket, un especialista de FPSSL deberá proporcionarle un par de registros CNAME. Estos registros deben configurarse en el servidor DNS de su empresa antes de que Adobe pueda adquirir el certificado en su nombre. Los CNAMES serán similares a los siguientes.

* **Proteger** : Por ejemplo, el nombre de host `smetrics.example.com` apunta a: `example.com.ssl.d1.omtrdc.net`.
* **No seguro** : por ejemplo, el nombre de host `metrics.example.com` apunta a: `example.com.d1.omtrdc.net`.

1. Cuando estos CNAMES estén en su sitio, Adobe trabajará con digicert para adquirir e instalar un certificado en los servidores de producción de Adobe. Si tiene una implementación existente, debe considerar la migración de visitantes para mantener a los visitantes existentes. Una vez que el certificado se haya insertado en el entorno de producción de Adobe, podrá actualizar las variables del servidor de seguimiento a los nuevos nombres de host. Es decir, si el sitio no es seguro (https), actualice `s.trackingServer`el. Si el sitio es seguro (https), actualice ambos `s.trackingServer``s.trackingServerSecure` y variables.

1. Ping el nombre de host (véase más abajo).

1. Actualizar código de implementación (véase más abajo).

### Mantenimiento y renovaciones

Los certificados SSL caducan cada año, lo que significa que Adobe debe adquirir un certificado nuevo para cada implementación por año. Todos los usuarios de asistencia técnica de su organización recibirán una notificación por correo electrónico cada vez que una implementación esté cercana a caducidad. Para que Adobe renueve su nombre de host, un usuario de asistencia técnica deberá responder al correo electrónico de Adobe e indicar que desea continuar utilizando el nombre de host caducidad para la recopilación de datos. En ese momento, Adobe compra e instala automáticamente un nuevo certificado.

### Preguntas frecuentes

| Pregunta | Respuesta |
|---|---|
| **¿Es seguro este proceso?** | Sí, el programa Administrado de Adobe es más seguro que nuestro método heredado, ya que ningún certificado o clave privada se transfiere fuera de Adobe y la autoridad emisora de certificados. |
| **¿Cómo puede adquirir Adobe un certificado para nuestro dominio?** | El certificado solo se puede comprar cuando se ha apuntado el nombre de host especificado (por ejemplo, smetrics.example.com) a un nombre de host de Adobe propiedad. Básicamente está delegando este nombre de host a Adobe y permite que Adobe compre el certificado en su nombre. |
| **¿Puedo solicitar que se revoque el certificado?** | Sí, como propietario del dominio, tiene derecho a solicitar el certificado revocado. Solo tendrá que abrir un ticket con el Servicio de atención al cliente para que esto se complete. |
| **¿Utilizará este certificado el cifrado SHA -2?** | Sí, Adobe trabajará con digicert para emitir un certificado SHA -2. |
| **¿Esto supone un costo adicional?** | No, Adobe ofrece este servicio a todos los clientes actuales de Analytics sin costes adicionales. |

## Creación de registros CNAME

El equipo de operaciones de red de su organización debe configurar los servidores DNS creando nuevos registros CNAME. Cada nombre de host envía datos a los servidores de recopilación de datos de Adobe.

El especialista de FPC le proporciona los nombres de host configurados y los CNAME a los que se van a apuntar. Por ejemplo:

* **Nombre del host SSL**:`smetrics.mysite.com`
* **CNAME SSL**:`mysite.com.ssl.d1.sc.omtrdc.net`
* **Nombre del host no SSL**:`metrics.mysite.com`
* **CNAME no SSL**:`mysite.com.d1.sc.omtrdc.net`

Siempre que no se modifique el código de implementación, este paso no afectará la recopilación de datos y se puede realizar en cualquier momento después de actualizar el código de implementación.

>[!Note:] El servicio ID de visitante de Experience Cloud proporciona una alternativa para configurar un CNAME para habilitar cookies de origen.

## Ping del nombre de host

Haga ping en el nombre de host para garantizar el reenvío correcto. Todos los nombres de host deben responder a un ping para evitar la pérdida de datos.

Después de configurar correctamente los registros CNAME y de que Adobe haya confirmado la instalación del certificado, abra un símbolo del sistema y haga ping en los nombres de host. Using `mysite.com` as an example: `ping metrics.mysite.com`

Si todo está configurado correctamente, devolverá un resultado similar a:

```Pinging mysite.com.112.2o7.net [66.235.132.232] with 32 bytes of data:
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246

Ping statistics for 66.235.132.232: Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds: Minimum = 19ms, Maximum = 19ms, Average = 19ms
```

Si los registros CNAME no están configurados correctamente o no están activos, devolverá lo siguiente:

`Ping request could not find the host. Please check the name and try again.`

>[!Note:] Si está utilizando `https:// protocol`, ping solo responderá después de la fecha de carga especificada por el especialista de FPC. Además, asegúrese de ping el nombre de host seguro y el nombre de host no seguro para asegurarse de que ambos funcionan correctamente antes de actualizar la implementación.

## Actualizar el código de implementación

Antes de editar el código del sitio para utilizar cookies de origen, complete estos requisitos previos:

* Solicite un certificado SSL, tal como se describe en Pasos de implementación para el Programa de certificados administrados de Adobe.
* Cree registros CNAME.
* Ping el nombre de host.

Después de comprobar que los nombres de host responden y redirigen a los servidores de recopilación de datos de Adobe, puede modificar su implementación para que señale a sus propios nombres de host de recopilación de datos.

1. Open your core JavaScript file (`s_code.js/AppMeasurement.js`).
1. Si desea actualizar su versión del código, sustituya todo el archivo `s_code.js/AppMeasurement.js` por la versión más reciente y reemplace todos los plugins o personalizaciones (si hay). **O bien**, si desea actualizar el código solo pertinente a cookies de origen, busque las variables s. trackingserver y s. trackingserversecure (si utiliza SSL) y agréguelas a los nuevos nombres de host de recopilación de datos. Using mysite.com as an example:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Cargue el archivo javascript principal actualizado en el sitio.
1. Si pasa a cookies de origen de una implementación antigua o cambia a otro nombre de host de colección de origen, recomendamos migrar visitantes del dominio anterior al nuevo dominio.

Consulte [Migración de visitantes](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) en la Guía de implementación de Analytics.

Después de cargar el archivo JavaScript, todo está configurado para la recopilación de datos de cookies personales. Le recomendamos que supervise los informes de Analytics durante las siguientes horas para asegurarse de que la recopilación de datos continúa con normalidad. Si no lo hace, verifique que se hayan completado todos los pasos anteriores y que uno de los usuarios de asistencia técnica de su organización se ponga en contacto con el Servicio de atención al cliente.
