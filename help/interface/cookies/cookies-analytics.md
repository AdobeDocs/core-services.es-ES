---
description: Adobe Analytics usa cookies para diferenciar las solicitudes de distintos navegadores y almacenar información útil que una aplicación puede usar posteriormente. También se pueden usar para asociar la información de navegación a registros de cliente.
keywords: cookies,privacidad
seo-description: Adobe Analytics usa cookies para diferenciar las solicitudes de distintos navegadores y almacenar información útil que una aplicación puede usar posteriormente. También se pueden usar para asociar la información de navegación a registros de cliente.
seo-title: Cookies de Analytics
solution: Experience Cloud,Analytics,Target,Social
title: Cookies de Analytics
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
index: y
internal: n
snippet: y
translation-type: ht
source-git-commit: f59badcd3423ada51a3fe0c605158a009d5b1d64

---


# Cookies de Analytics{#analytics-cookies}

Adobe Analytics usa cookies para diferenciar las solicitudes de distintos navegadores y almacenar información útil que una aplicación puede usar posteriormente. También se pueden usar para asociar la información de navegación a registros de cliente.

En concreto, usa las cookies para definir de forma anónima a los nuevos visitantes, ayudar en el análisis de los datos de flujo de navegación y realizar un seguimiento de la actividad histórica del sitio web, como por ejemplo la respuesta a ciertas campañas o la duración del ciclo de ventas.

* [Nombre de cookie: s_ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Nombre de la cookie: AMCV_###@AdobeOrg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Nombre de la cookie: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Nombre de la cookie: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Nombre de la cookie: s_sq](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Nombre de la cookie: s_vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Nombre de la cookie: s_fid](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [Cookies establecidas por complementos](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

Consulte más información sobre las [cookies propias](/help/interface/cookies/cookies-first-party.md) en la ayuda de Analytics.

## Nombre de cookie: s_ ecid {#section-32fd753c3fa54452acd62b021434919a}

| Atributo | Descripción |
|--- |--- |
| Información almacenada | Contiene una copia del Experience Cloud ID (ECID) o MID. El MID se almacena en un par de clave-valor que sigue esta sintaxis, s_ecid=MCMID | <ECID> |
| Vencimiento | 2 años |
| Uso | El dominio del cliente establece esta cookie después de que el cliente establezca la cookie AMCV. El propósito de esta cookie es permitir el seguimiento continuado del ID en el estado de origen y se utiliza como ID de referencia si la cookie de AMCV ha expirado. Para obtener más detalles, consulte la cookie AMCV aquí. |
| Ubicación | Solo clientes CNAME. No aplicable a escenarios de terceros. La cookie se almacena en su dominio, el mismo dominio utilizado por CNAME y su solicitud de imagen de Analytics. |
| Tamaño | 45 bytes |

## Nombre de la cookie: s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| Atributo | Descripción |
|--- |--- |
| Información almacenada | El código JavaScript establece y lee esta cookie para determinar si las cookies están habilitadas (se configura como “True”) |
| Vencimiento | Esta es una cookie de sesión y caduca cuando se cierra el navegador |
| Uso | Una sola cookie para todas las cuentas |
| Ubicación | Esta cookie se almacena en el dominio de la página |
| Tamaño | 4 bytes |

## Nombre de la cookie: s_sq  {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| Atributo | Descripción |
|--- |--- |
| Información almacenada | El código JavaScript establece y lee esta cookie cuando están habilitadas las funcionalidades ClickMap y Activity Map. Contiene información sobre el vínculo anterior en el que el usuario hizo clic. |
| Vencimiento | Esta es una cookie de sesión y caduca cuando se cierra el navegador |
| Uso | Una sola cookie para todas las cuentas |
| Ubicación | Esta cookie se almacena en el dominio de la página |
| Tamaño | Varía según el tamaño de la dirección URL de la página, pero normalmente de 100 a 200 bytes |

## Nombre de la cookie: s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| Atributo | Descripción |
|--- |--- |
| Información almacenada | Marca de fecha y hora del identificador de visitante único |
| Vencimiento | 2 años |
| Uso | Esta cookie se usa para identificar a un visitante único |
| Ubicación | Esta cookie se almacena en el dominio de la petición de imagen, que suele ser 2O7.net si usa cookies de terceros o su dominio si usa cookies de origen |
| Tamaño | 44 bytes |

>[!NOTE]
>
>Cada ID de visitante de Analytics está asociado con un perfil del visitante en los servidores de Adobe. Los perfiles de visitante se borran tras un año de inactividad, independientemente de la caducidad de cualquier cookie del ID del visitante.

## Nombre de la cookie: s_fid  {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| Atributo | Descripción |
|--- |--- |
| Información almacenada | Marca de fecha y hora del ID de visitante único alternativo |
| Vencimiento | 5 años |
| Uso | Esta cookie se usa para identificar a un visitante único  si la cookie estándar s_vi no está disponible debido a las restricciones de cookies de terceros. No se usa para las implementaciones que utilizan cookies propias. |
| Ubicación | Esta cookie está almacenada en su dominio como una cookie propia. |
| Tamaño | 33 bytes |

## Cookies establecidas por complementos  {#section-a6b1cae8454945fab9eea5c7884c40fc}

Se pueden establecer cookies adicionales según el uso de los complementos de Analytics. Estas cookies son fragmentos de código disponibles para el cliente para su uso en varias circunstancias distintas, entre las que se incluyen las siguientes: recuperar valores de URL, concatenar valores para pasarlos a Analytics, capturar el abandono de formularios, etc. Para obtener información concreta sobre las cookies establecidas por cada complemento, póngase en contacto con ClientCare. Un ejemplo sería la cookie [!DNL s_vh], que se usa con los complementos *Configurar una vez por* y *Configurar y obtener el último valor*.

Las variables de conversión (eVarX) pasadas en una petición de imagen sin JavaScript (como, por ejemplo, un código ubicado en un correo electrónico) solo se atribuirán correctamente si el cliente de correo electrónico y el navegador Web comparten el mismo espacio de cookie.
