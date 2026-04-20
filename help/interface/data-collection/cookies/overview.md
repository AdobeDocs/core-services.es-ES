---
description: Descubra cómo utilizan cookies las soluciones y los servicios de Adobe CX Enterprise.
title: Uso de cookies en Experience Cloud
uuid: 4255a13a-917b-4b5f-a7d4-4b2e7521d189
exl-id: 60f1a89e-d989-461b-a6a3-c1df022cd30b
TQID: https://experienceleague.adobe.com/GH5WHcI9440NKYpUzizHlhOMlBSf-Y0WQ5GDBaSvqNI
product_v2: id: e1971122-7081-4556-9222-8a31bd71800c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 624
ht-degree: 8%

---

# Uso de cookies en CX Enterprise

Adobe CX Enterprise usa cookies. Una cookie es un pequeño fragmento de datos que un sitio web envía a su explorador, que lo almacena para su uso posterior. Las cookies ayudan al sitio web a recordar cosas cuando usted visita de nuevo o se mueve entre páginas. Las cookies ayudan a rastrear las visitas y a diferenciar un dispositivo de otro.

Las leyes a menudo requieren que obtenga permiso antes de almacenar o usar cookies en el dispositivo de alguien. Adobe recomienda consultar con su equipo legal para comprender las reglas que se aplican.

## Acerca de las cookies de origen

Adobe CX Enterprise usa cookies para rastrear información que no dura entre vistas de página o sesiones del explorador. Cuando es posible, Adobe utiliza cookies de origen (vinculadas a su propio sitio web). Para rastrear la actividad en varios sitios o dominios de su propiedad, se necesitan cookies de terceros.

Algunos exploradores y herramientas antispyware bloquean las cookies de terceros. Adobe tiene maneras de asegurarse de que las cookies siguen funcionando aunque estén bloqueadas. El modo en que esto funcione depende de si utiliza el servicio de identidad de Experience Platform (ECID) o cookies de Analytics más antiguas (como la cookie `s_vi`):

* [Servicio de identidad de CX Enterprise](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview): El servicio ECID siempre establece cookies de origen, independientemente de si el dominio de recopilación coincide con el del sitio. Utiliza JavaScript para colocar la cookie en el dominio del sitio.

* [Identificadores heredados de Analytics](analytics.md) (como la cookie `s_vi`): Depende de la configuración si las cookies son de origen o de terceros:

   * Si el servidor de recopilación de datos coincide con el dominio del sitio, las cookies son de origen.
   * Si no coincide, las cookies son de terceros. Si las cookies de terceros están bloqueadas, Adobe establece una cookie de reserva (`s_fid`) en lugar de la habitual.

Para asegurarse de que el servidor de recopilación coincida con el dominio del sitio, puede usar una configuración **CNAME**. Esto implica actualizar la configuración de DNS para que dirija un dominio personalizado (el suyo) a los servidores de Adobe. Esto hace que la cookie de seguimiento aparezca como de origen. Aunque un CNAME puede funcionar en varios dominios, cualquier dominio que no coincida con el CNAME establecerá cookies de terceros.

>[!NOTE]
>
>La prevención inteligente del seguimiento (ITP) de Apple limita el tiempo que duran las cookies de origen de Adobe, incluso si el dominio de recopilación coincide con el del sitio. ITP afecta a Safari en macOS y a todos los exploradores en iOS y iPadOS. Desde noviembre de 2020, las cookies configuradas con CNAME caducan tan rápido como las configuradas con JavaScript. Este plazo puede cambiar en el futuro.

Esta es una versión simplificada del texto:

## Cookies y privacidad

Adobe se toma muy en serio la privacidad y la seguridad de los datos. Funciona con organizaciones de privacidad, reguladores y programas como AdChoices para dar a las personas control sobre cómo se utilizan sus datos.

La mayoría de las cookies de Adobe CX Enterprise no almacenan información personal. Son seguros y solo los utiliza su empresa, para la creación de informes, contenido y publicidad. Adobe no comparte estos datos con otros clientes o terceros, excepto en informes anónimos de todo el sector (como los informes de Digital Marketing Insight).

Adobe no combina los datos de los exploradores en empresas diferentes. Para proteger la privacidad, algunas herramientas de Adobe permiten que cada sitio web utilice su propio conjunto de cookies. Algunos también permiten el uso de su propio dominio para las cookies, lo que las hace de origen y más seguras.

Las cookies solo pueden almacenar información que se haya guardado anteriormente en ellas. No pueden ejecutar código ni leer otros datos en el dispositivo. Además, los navegadores web solo permiten que el sitio web que los establece lea las cookies. Por ejemplo, solo Adobe.com puede leer las cookies que establece.

El diagrama siguiente ilustra el uso de cookies para una solicitud de imagen estándar:

![Uso de cookies para una solicitud de imagen estándar](assets/CookiesProcessGraphic-01.png)

El diagrama siguiente ilustra el uso de cookies para una solicitud de imagen habitual (utilizado en situaciones en las que no se carga un archivo JS):

![Uso de cookies para una solicitud de imagen recta](assets/CookiesProcessGraphic2.png)

