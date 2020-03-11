---
description: Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imagen y sesiones del navegador.
keywords: cookies;privacy
seo-description: Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imagen y sesiones del navegador.
seo-title: Cookies de terceros
solution: Experience Cloud,Analytics
title: Cookies de terceros
index: y
snippet: y
translation-type: tm+mt
source-git-commit: 2b44385e32752c7d80322de092d1ac230edfcd01

---


# Acerca de las cookies de origen

Analytics utiliza cookies para ofrecer información sobre variables y componentes que no se mantienen entre solicitudes de imagen y sesiones del navegador. Estas cookies inofensivas, que se originan en un dominio alojado por Adobe, se conocen como cookies de terceros.

Muchos navegadores y aplicaciones antispyware están diseñados para rechazar y eliminar las cookies de terceros, incluidas las que se usan en la recogida de datos de Analytics. Para admitir el seguimiento de la forma en que los visitantes interactúan con el sitio web, puede implementar cookies de origen.

Hay dos opciones disponibles para implementar cookies de origen:

* El servicio Experience Platform ID. El servicio de ID puede establecer la cookie en el contexto de origen a través de JavaScript.
* Entradas DNS en el servidor DNS de su empresa para configurar un alias CNAME en un dominio alojado de Adobe. Tenga en cuenta que, aunque varios productos de Adobe admiten el uso de un CNAME, en todos los casos se utiliza el CNAME para crear un punto final de confianza para un cliente específico y es propiedad de dicho cliente. Si ese cliente controla varios dominios, puede usar un único extremo CNAME para rastrear a los usuarios en sus dominios, pero como esto requiere cookies de terceros para todos los dominios fuera del dominio de CNAME, no funciona cuando las cookies de terceros están bloqueadas y por lo tanto no se recomienda. Los CNAME de Adobe nunca se utilizan para realizar el seguimiento de un individuo o dispositivo entre dominios propiedad de distintos clientes.

Incluso cuando se utiliza la primera opción con el servicio Experience Cloud ID, el ITP de Apple hará que las cookies de origen tengan una duración corta, por lo que es mejor usarlas junto con la segunda opción.

En la segunda opción, si el sitio tiene páginas seguras mediante el protocolo HTTPS, puede trabajar con Adobe para obtener un certificado SSL a fin de implementar cookies de origen. Adobe recomienda utilizar HTTPS exclusivamente para la recopilación de datos, ya que en el segundo semestre de 2020 dejaremos de admitir la recopilación de HTTP.

El proceso de publicación de certificados SSL puede resultar confuso y requerir mucho tiempo. Por ello, Adobe estableció una sociedad con DigiCert, una autoridad certificadora (AC) líder en su sector, y desarrolló un proceso integrado por el cual la compra y administración de estos certificados está automatizada.

Con su permiso, trabajaremos con nuestra AC para emitir, implementar y administrar un nuevo certificado SHA-2 SSL para usted. Adobe seguirá administrando este certificado y asegurándose de que una caducidad, revocación o seguridad inesperada no amenace la disponibilidad de la colección segura de su organización.

## Programa de certificados administrados de Adobe

El programa de certificados administrados de Adobe es el proceso recomendado para implementar un nuevo certificado SSL de origen para cookies de origen.

El programa de certificados administrados le permite implementar un nuevo certificado SSL de origen para cookies de origen sin coste adicional. Si tiene su propio certificado SSL administrado por el cliente, hable con el Servicio de atención al cliente de Adobe acerca de la migración al programa de Certificados administrados de Adobe.

### Implementación

Así se implementa un nuevo certificado SSL de origen para cookies de origen:

1. Complete el [Formulario de solicitud de cookies de origen](/help/interface/cookies/assets/FPC_Request_Form.xlsx) y abra una incidencia con el Servicio de atención al cliente solicitando la configuración de cookies de origen en el programa administrado de Adobe. Cada campo se describe dentro del documento con ejemplos.

1. Cree registros CNAME (consulte las instrucciones más abajo).

   Al recibir el billete, un representante de atención al cliente debe proporcionarle un par de registros CNAME. Estos registros deben configurarse en el servidor DNS de su empresa antes de que Adobe pueda adquirir el certificado en su nombre. El CNAMES será similar al siguiente:

   **Seguro** : por ejemplo, el nombre de host `smetrics.example.com` apunta a: `example.com.ssl.d1.omtrdc.net`.

   **No seguro**: Por ejemplo, el nombre de host `metrics.example.com` señala a `example.com.d1.omtrdc.net`.

1. Cuando se establezcan estos CNAMES, Adobe trabajará con DigiCert para adquirir e instalar un certificado en los servidores de producción de Adobe.

   Si ya tiene una implementación, debe considerar la migración de visitantes para mantener los visitantes existentes. Una vez que el certificado se haya insertado en el entorno de producción de Adobe, puede actualizar las variables del servidor de seguimiento a los nuevos nombres de host. Meaning, if the site is not secure (HTTP), update the `s.trackingServer`. If the site is secure (HTTPS), update both `s.trackingServer` and `s.trackingServerSecure` variables.

1. [Valide el reenvío](#validate) de nombres de host (consulte a continuación).

1. [Actualizar el código](#update) de implementación (ver más abajo).

### Mantenimiento y renovaciones

Los certificados SSL expiran cada año, lo que significa que Adobe debe adquirir un certificado nuevo para cada implementación por año. Todos los usuarios admitidos de su organización recibirán una notificación por correo electrónico cada vez que una implementación esté cerca de expirar. Para que Adobe renueve el nombre de host, un usuario de asistencia técnica debe responder al correo electrónico de Adobe e indicar que tiene previsto seguir utilizando el nombre de host caducado para la recopilación de datos. En ese momento, Adobe compra e instala automáticamente un nuevo certificado.

### Preguntas frecuentes

| Pregunta | Respuesta |
|---|---|
| **¿Es seguro este proceso?** | Sí, el programa administrado de Adobe es más seguro que nuestro método heredado, ya que ningún certificado o clave privada se transfiere fuera de Adobe y la autoridad emisora de certificados. |
| **¿Cómo puede adquirir Adobe un certificado para nuestro dominio?** | El certificado solo se puede adquirir si ha señalado el nombre de host especificado (por ejemplo, smetrics.example.com) a un nombre de host en propiedad de Adobe. Básicamente, delega este nombre de host a Adobe y permite que Adobe compre el certificado en su nombre. |
| **¿Puedo solicitar que se revoque el certificado?** | Sí, como propietario del dominio, tiene derecho a solicitar que se revoque el certificado. Solo tendrá que abrir una incidencia con el Servicio de atención al cliente para completarlo. |
| **¿Utilizará este certificado el cifrado SHA-2?** | Sí, Adobe trabajará con DigiCert para emitir un certificado SHA-2. |
| **¿Supone un costo adicional?** | No, Adobe ofrece este servicio a todos los clientes actuales de Adobe Digital Experience sin ningún coste adicional. |

## Creación de registros CNAME

El equipo de operaciones de red de su organización debe configurar los servidores DNS creando nuevos registros CNAME. Cada nombre de host envía datos a los servidores de recopilación de datos de Adobe.

El especialista de FPC le proporciona los nombres de host configurados y los CNAME a los que se va a señalar. Por ejemplo:

* **Nombre del host SSL**:`smetrics.mysite.com`
* **CNAME de SSL**:`mysite.com.ssl.sc.omtrdc.net`
* **Nombre del host no SSL**:`metrics.mysite.com`
* **CNAME no de SSL**:`mysite.com.sc.omtrdc.net`

Mientras no se modifique el código de implementación, este paso no afectará a la recopilación de datos y se puede llevar a cabo en cualquier momento después de la implementación del código.

>[!NNota:]
>El servicio de ID de visitante de Experience Cloud ofrece una alternativa a la configuración de un CNAME para habilitar las cookies de origen, pero debido a los recientes cambios de ITP de Apple, se recomienda asignar un CNAME incluso cuando se utilice el servicio de ID de Experience Cloud.

## Validar reenvío de nombre de host {#validate}

Los siguientes métodos están disponibles para la validación:

**Validación del explorador**

Si tiene un CNAME configurado y el certificado instalado, puede utilizar el explorador para la validación:

<https://sstats.adobe.com/_check>.

Nota: Verá una advertencia de seguridad si no hay un certificado instalado.

**Validar mediante[!DNL curl]**

Adobe recomienda utilizar [!DNL [curl](https://curl.haxx.se/)] desde la línea de comandos. ([!DNL Windows] los usuarios pueden instalar [!DNL curl] desde: <https://curl.haxx.se/windows/>)

Si tiene un CNAME pero no hay ningún certificado instalado, ejecute:
`curl -k https://sstats.adobe.com/_check`Respuesta: `SUCCESS`

(El `-k` valor desactiva la advertencia de seguridad).

Si tiene un CNAME configurado y el certificado está instalado, ejecute:
`curl https://sstats.adobe.com/_check`Respuesta: `SUCCESS`

**Validar mediante[!DNL nslookup]**

Puede utilizarlo `nslookup` para la validación. A `mysite.com`modo de ejemplo, abra un símbolo del sistema y escriba `nslookup metrics.mysite.com`

Si todo está configurado correctamente, verá un retorno similar a:

```
nslookup metrics.mysite.com
Server:  hiodsibxvip01.corp.adobe.com
Address:  10.50.112.247

Non-authoritative answer:
Name:    metrics.mysite.com
Address:  64.136.20.37
```

## Actualización del código de implementación {#update}

Antes de editar el código del sitio para utilizar cookies de origen, complete estos requisitos previos:

* Solicite un certificado SSL siguiendo los pasos descritos anteriormente en la sección *Implementar* del Programa de certificados administrados de [Adobe](#adobe-managed-certificate-program).
* Cree registros CNAME (consultar más arriba).
* Valide los nombres de host (véase más arriba).

Después de comprobar que sus nombres de host responden y redirigen a los servidores de recopilación de datos, puede modificar su implementación de modo que señale a sus propios nombres de host de recopilación de datos.

1. Abra su archivo principal de JavaScript (`s_code.js/AppMeasurement.js`).
1. Si desea actualizar su versión del código, sustituya todo el archivo `s_code.js/AppMeasurement.js` por la versión más reciente y reemplace todos los plugins o personalizaciones (si hay). **O bien**, si desea actualizar el código en relación con las cookies de origen, busque las variables s.trackingServer y s.trackingServerSecure (si utiliza SSL) y agréguelas a los nuevos nombres de host de recopilación de datos. Uso de mysite.com como ejemplo:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. Cargue en su sitio el archivo principal de JavaScript actualizado.

1. Si está migrando a cookies de origen desde una implementación antigua, o cambiando a otro nombre de host de recopilación de origen, le recomendamos migrar a los visitantes del dominio anterior al nuevo dominio.

Consulte Migración [de](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) visitantes en la Guía de implementación de Analytics.

Después de haber cargado el archivo de JavaScript, ya estará todo configurado para la recopilación de datos de cookies de origen. Le recomendamos que monitorice los informes de Analytics durante las siguientes horas para asegurarse de que la recopilación de datos continúa con normalidad. Si no es así, compruebe que se han realizado todos los pasos anteriores e indique a uno de los usuarios admitidos en su organización que contacte con el servicio de atención al cliente.
