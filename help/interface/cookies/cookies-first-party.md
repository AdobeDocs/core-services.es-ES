---
description: Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imagen y sesiones del navegador.
keywords: cookies,privacidad
seo-description: Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imagen y sesiones del navegador.
seo-title: Cookies de terceros
solution: Experience Cloud,Analytics
title: Cookies de terceros
index: y
snippet: y
translation-type: ht
source-git-commit: 2bdc4b7287ccacfc4d968278b2c3ffdaeddfc105

---


# Acerca de las cookies de origen

Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imagen y sesiones del navegador. Estas cookies son inofensivas y se originan en un dominio hospedado por Adobe; se denominan cookies de origen.

Muchos navegadores y aplicaciones antispyware están diseñados para rechazar y eliminar las cookies de terceros, incluidas las que se usan en la recogida de datos de Analytics. Puede implementar cookies de origen para evitar las limitaciones de seguimiento impuestas por los navegadores y programas.

Hay dos opciones disponibles para implementar cookies individuales

* El servicio Experience Platform ID. El servicio de ID puede establecer la cookie en el contexto de origen a través de JavaScript.
* Las entradas DNS en el servidor DNS de sus empresas.
* Si su sitio tiene páginas seguras que utilizan el protocolo `https:` y usted no utiliza el servicio Experience Platform ID, puede trabajar con Adobe para obtener un certificado SSL con el fin de implementar cookies de origen

El proceso de publicación de certificados SSL puede resultar confuso y requerir mucho tiempo. Por ello, Adobe estableció una sociedad con DigiCert, una autoridad certificadora (AC) líder en su sector, y desarrolló un proceso integrado por el cual la compra y administración de estos certificados está automatizada.

Con su permiso, trabajaremos con nuestra AC para emitir, implementar y administrar un nuevo certificado SHA-2 SSL para usted. Adobe seguirá administrando este certificado y asegurándose de que el problema de caducidad, revocación o seguridad no afecte a la disponibilidad de la colección de las organizaciones.

## Programa de certificados administrados de Adobe

El programa de certificados administrados de Adobe es el proceso recomendado para implementar un nuevo certificado SSL de origen para cookies de origen.

El programa de certificados administrados le permite implementar un nuevo certificado SSL de origen para cookies de origen sin coste adicional. Si tiene su propio certificado SSL administrado por el cliente, hable con el Servicio de atención al cliente de Adobe acerca de la migración al programa de Certificados administrados de Adobe.

### Implementación

Así se implementa un nuevo certificado SSL de origen para cookies de origen:

1. Complete el [Formulario de solicitud de cookies de origen](/help/interface/cookies/assets/FPC_Request_Form.xlsx) y abra una incidencia con el Servicio de atención al cliente solicitando la configuración de cookies de origen en el programa administrado de Adobe. Cada campo se describe dentro del documento con ejemplos.

1. Cree registros CNAME (consulte las instrucciones más abajo). Una vez recibido la incidencia, un especialista de FPSSL deberá proporcionarle un par de registros CNAME. Estos registros deben configurarse en el servidor DNS de su empresa antes de que Adobe pueda adquirir el certificado en su nombre. Los CNAMES serán similares a los siguientes: **Proteger**: Por ejemplo, el nombre de host `smetrics.example.com` señala a `example.com.ssl.d1.omtrdc.net`. **No seguro**: Por ejemplo, el nombre de host `metrics.example.com` señala a `example.com.d1.omtrdc.net`.

1. Cuando se establezcan estos CNAMES, Adobe trabajará con DigiCert para adquirir e instalar un certificado en los servidores de producción de Adobe. Si tiene una implementación existente, debe considerar la migración de visitantes para mantener a los existentes. Una vez que el certificado se haya insertado en el entorno de producción de Adobe, podrá actualizar las variables del servidor de seguimiento a los nuevos nombres de host. Es decir, si el sitio no es seguro (https), actualice el `s.trackingServer`. Si el sitio es seguro (https), actualice ambos `s.trackingServer` y las variables de `s.trackingServerSecure`.

1. Hacer ping al nombre de host (consultar más abajo).

1. Actualizar código de implementación (consultar más abajo).

### Mantenimiento y renovaciones

Los certificados SSL expiran cada año, lo que significa que Adobe debe adquirir un certificado nuevo para cada implementación por año. Todos los usuarios admitidos de su organización recibirán una notificación por correo electrónico cada vez que una implementación esté cerca de expirar. Para que Adobe renueve su nombre de host, un usuario admitido deberá responder al correo electrónico de Adobe e indicar que desea continuar utilizando el nombre de host expirado para la recopilación de datos. En ese momento, Adobe compra e instala automáticamente un nuevo certificado.

### Preguntas frecuentes

| Pregunta | Respuesta |
|---|---|
| **¿Es seguro este proceso?** | Sí, el programa administrado de Adobe es más seguro que nuestro método heredado, ya que ningún certificado o clave privada se transfiere fuera de Adobe y la autoridad emisora de certificados. |
| **¿Cómo puede adquirir Adobe un certificado para nuestro dominio?** | El certificado solo se puede adquirir si ha señalado el nombre de host especificado (por ejemplo, smetrics.example.com) a un nombre de host en propiedad de Adobe. Básicamente, delega este nombre de host a Adobe y permite que Adobe compre el certificado en su nombre. |
| **¿Puedo solicitar que se revoque el certificado?** | Sí, como propietario del dominio, tiene derecho a solicitar que se revoque el certificado. Solo tendrá que abrir una incidencia con el Servicio de atención al cliente para completarlo. |
| **¿Utilizará este certificado el cifrado SHA-2?** | Sí, Adobe trabajará con DigiCert para emitir un certificado SHA-2. |
| **¿Supone un costo adicional?** | No, Adobe ofrece este servicio a todos los clientes actuales de Analytics sin coste adicional. |

## Creación de registros CNAME

El equipo de operaciones de red de su organización debe configurar los servidores DNS creando nuevos registros CNAME. Cada nombre de host envía datos a los servidores de recopilación de datos de Adobe.

El especialista de FPC le proporciona los nombres de host configurados y los CNAME a los que se va a señalar. Por ejemplo:

* **Nombre del host SSL**:`smetrics.mysite.com`
* **CNAME de SSL**:`mysite.com.ssl.d1.sc.omtrdc.net`
* **Nombre del host no SSL**:`metrics.mysite.com`
* **CNAME no de SSL**:`mysite.com.d1.sc.omtrdc.net`

Mientras no se modifique el código de implementación, este paso no afectará a la recopilación de datos y se puede llevar a cabo en cualquier momento después de la implementación del código.

>[!NNota:] El servicio ID de visitante de Experience Cloud proporciona una alternativa para configurar un CNAME para habilitar cookies de origen.

## Hacer ping en el nombre de host

Hacer ping en el nombre de host para garantizar un reenvío exitoso. Todos los nombres de host deben responder a un ping para evitar la pérdida de datos.

Después de configurar correctamente los registros CNAME y de que Adobe haya confirmado la instalación del certificado, abra un símbolo del sistema y haga ping en los nombres de host. Con `mysite.com`, por ejemplo: `ping metrics.mysite.com`

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

>[!NNota:] Si está utilizando `https:// protocol`, el ping solo responderá a partir de la fecha de carga que indique el especialista de FPC. Tampoco olvide hacer ping en el nombre de host seguro y en el no seguro para comprobar que ambos funcionan correctamente antes de actualizar su implementación.

## Actualización del código de implementación

Antes de editar el código del sitio para utilizar cookies de origen, complete estos requisitos previos:

* Solicite un certificado SSL, tal como se describe anteriormente en los pasos de implementación para el programa de certificados administrados de Adobe.
* Cree registros CNAME (consultar más arriba).
* Haga ping al nombre de host (consultar más arriba).

Después de comprobar que sus nombres de host responden y redirigen a los servidores de recopilación de datos, puede modificar su implementación de modo que señale a sus propios nombres de host de recopilación de datos.

1. Abra su archivo principal de JavaScript (`s_code.js/AppMeasurement.js`).
1. Si desea actualizar su versión del código, sustituya todo el archivo `s_code.js/AppMeasurement.js` por la versión más reciente y reemplace todos los plugins o personalizaciones (si hay). **O bien**, si desea actualizar el código en relación con las cookies de origen, busque las variables s.trackingServer y s.trackingServerSecure (si utiliza SSL) y agréguelas a los nuevos nombres de host de recopilación de datos. Uso de mysite.com como ejemplo:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Cargue en su sitio el archivo principal de JavaScript actualizado.

1. Si está migrando a cookies de origen desde una implementación antigua, o cambiando a otro nombre de host de recopilación de origen, le recomendamos migrar a los visitantes del dominio anterior al nuevo dominio.

Consulte [Migración de visitantes](https://docs.adobe.com/content/help/es-ES/analytics/implementation/javascript-implementation/visitor-migration.translate.html) en la Guía de implementación de Analytics.

Después de haber cargado el archivo de JavaScript, ya estará todo configurado para la recopilación de datos de cookies de origen. Le recomendamos que monitorice los informes de Analytics durante las siguientes horas para asegurarse de que la recopilación de datos continúa con normalidad. Si no es así, compruebe que se han realizado todos los pasos anteriores e indique a uno de los usuarios admitidos en su organización que contacte con el servicio de atención al cliente.
