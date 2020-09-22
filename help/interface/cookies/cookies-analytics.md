---
description: Adobe Analytics utiliza cookies para diferenciar las solicitudes de distintos navegadores y almacenar información útil que una aplicación puede utilizar posteriormente. También se pueden utilizar para asociar la información de navegación a los registros de clientes.
keywords: cookies;privacy
seo-description: Adobe Analytics utiliza cookies para diferenciar las solicitudes de distintos navegadores y almacenar información útil que una aplicación puede utilizar posteriormente. También se pueden utilizar para asociar la información de navegación a los registros de clientes.
seo-title: Cookies de Analytics
solution: Experience Cloud,Analytics,Target
title: Cookies de Analytics
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
translation-type: tm+mt
source-git-commit: c9d9a69193a877c553db73d230723f1c24dbfed6
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 100%

---


# Cookies de Analytics {#analytics-cookies}

Adobe Analytics utiliza cookies para diferenciar las solicitudes de distintos navegadores y almacenar información útil que una aplicación puede utilizar posteriormente. También se pueden utilizar para asociar la información de navegación a los registros de clientes.

En particular, Analytics utiliza cookies para definir de forma anónima nuevos visitantes, analizar los datos del flujo de navegación y realizar un seguimiento de la actividad histórica en el sitio web, como la respuesta a campañas concretas o la duración del ciclo de ventas.

* [Nombre de cookie: s_ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Nombre de la cookie: AMCV_###@AdobeOrg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Nombre de la cookie: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Nombre de la cookie: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Nombre de la cookie: s_sq ](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Nombre de la cookie: s_vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Nombre de la cookie: s_fid ](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [Cookies establecidas por complementos ](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

Encontrará más información en la ayuda de Analytics sobre las cookies de [origen](/help/interface/cookies/cookies-first-party.md).

## Nombre de cookie: s_ ecid {#section-32fd753c3fa54452acd62b021434919a}

| Atributo | Descripción |
|--- |--- |
| Información almacenada | Contiene una copia del Experience Cloud ID (ECID) o MID. El MID se almacena en un par de clave-valor que sigue esta sintaxis, s_ecid=MCMID | `<ECID>` |
| Vencimiento | 2 años |
| Uso | El dominio del cliente establece esta cookie después de que el cliente establezca la cookie AMCV. El propósito de esta cookie es permitir el seguimiento continuado del ID en el estado de origen y se utiliza como ID de referencia si la cookie de AMCV ha expirado. Para obtener más detalles, consulte la cookie AMCV aquí. |
| Ubicación | Solo clientes CNAME. No aplicable a escenarios de terceros. La cookie se almacena en su dominio, el mismo dominio utilizado por CNAME y su solicitud de imagen de Analytics. |
| Tamaño | 45 bytes |

## Nombre de la cookie: s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| Atributo | Descripción |
|--- |--- |
| Información almacenada | JavaScript se encarga de configurar y leer esta cookie para determinar si las cookies están habilitadas (si tienen el valor “True”) |
| Vencimiento | Esta cookie es una cookie de sesión y caduca cuando se cierra el explorador |
| Uso | Solo una cookie para todas las cuentas |
| Ubicación | Esta cookie se almacena en el dominio de la página |
| Tamaño | 4 bytes |

## Nombre de la cookie: s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| Atributo | Descripción |
|--- |--- |
| Información almacenada | El código JavaScript establece y lee esta cookie cuando la funcionalidad ClickMap o la funcionalidad de Activity Map están habilitadas. Además, contiene información sobre el vínculo anterior en el que el usuario hizo clic |
| Vencimiento | Esta cookie es una cookie de sesión y caduca cuando se cierra el explorador |
| Uso | Solo una cookie para todas las cuentas |
| Ubicación | Esta cookie se almacena en el dominio de la página |
| Tamaño | Varía según el tamaño de la dirección URL de la página, pero normalmente de 100 a 200 bytes |

## Nombre de la cookie: s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| Atributo | Descripción |
|--- |--- |
| Información almacenada | Marca de fecha y hora del ID de visitante único |
| Vencimiento | 2 años |
| Uso | Esta cookie se usa para identificar a un visitante único |
| Ubicación | Esta cookie se almacena en el dominio de la solicitud de imagen, por lo general un subdominio específico del cliente bajo 2o7.net u omtrdc.net si utiliza cookies de terceros o si su dominio utiliza cookies de origen |
| Tamaño | 44 bytes |

>[!NOTE]
>
>Cada ID de visitante de Analytics está asociado con un perfil del visitante en los servidores de Adobe. Los perfiles de visitante se borran tras un año de inactividad, independientemente de la caducidad de cualquier cookie del ID del visitante.

## Nombre de la cookie: s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| Atributo | Descripción |
|--- |--- |
| Información almacenada | Marca de fecha y hora del ID de visitante único de reserva |
| Vencimiento | 2 años |
| Uso | Esta cookie se usa para identificar a un visitante único si la cookie estándar `s_vi` no está disponible debido a las restricciones de cookies de terceros. No se utiliza en implementaciones que utilizan cookies de origen |
| Ubicación | Esta cookie se almacena en su dominio como una cookie de origen |
| Tamaño | 33 bytes |

## Indicadores de cookie

En la tabla siguiente se describen los indicadores de las cookies de Analytics:

| Cookie (establecida por) | httpOnly | Secure | SameSite |
|--- |--- |--- |--- |
| s_vi   (respuesta http) | No | Sí cuando SameSite tiene el valor “None” y la conexión utiliza HTTPS | “Lax” de forma predeterminada al utilizar CNAME. “None” al usar 2o7.net u omtrdc.net |
| s_ecid   (respuesta http) | No | No | &quot;Laxo&quot; |
| s_fid (Javascript) | No | No | Sin configurar |
| s_cc (Javascript) | No | No | Sin configurar |
| s_sq (Javascript) | No | No | Sin configurar |

>[!NOTE]
>
>Si se utiliza un solo CNAME para realizar el seguimiento en varios dominios o propiedades, se debe configurar SameSite como “None” para `s_vi`. Para obtener ayuda para cambiar la configuración de cookies de Analytics, póngase en contacto con el Servicio de atención al cliente.

## Cookies establecidas por complementos {#section-a6b1cae8454945fab9eea5c7884c40fc}

Se pueden configurar cookies adicionales en función del uso de complementos de Analytics. Estas cookies son fragmentos de código disponibles para el cliente para su uso en diversas circunstancias. Estas circunstancias incluyen: recuperar valores de la dirección URL; concatenar valores para pasarlos a Analytics; capturar el abandono de formularios, etc. Para obtener información concreta sobre las cookies establecidas por cada complemento, póngase en contacto con ClientCare. Un ejemplo sería la cookie [!DNL s_vh], que se usa con los complementos *Configurar una vez por* y *Configurar y obtener el último valor*.

Las variables de conversión (eVarX) pasadas en una petición de imagen sin JavaScript (como, por ejemplo, un código ubicado en un correo electrónico) solo se atribuirán correctamente si el cliente de correo electrónico y el navegador Web comparten el mismo espacio de cookie.
