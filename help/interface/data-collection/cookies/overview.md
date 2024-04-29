---
description: Obtenga información sobre cómo usan cookies las soluciones y los servicios de Adobe Experience Cloud.
title: Uso de cookies en Experience Cloud
uuid: 4255a13a-917b-4b5f-a7d4-4b2e7521d189
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 58%

---


# Cookies utilizadas en Experience Cloud

Muchos servicios de Adobe Experience Cloud usan cookies. Una cookie es un pequeño fragmento de datos que un sitio Web presenta a un explorador Web. El explorador almacena este fragmento de datos, lo que permite a un sitio web hacer referencia a sus datos cuando es necesario. Esta acción se realiza con cada solicitud posterior de páginas e imágenes.

Las cookies se proporcionan para mantener la información durante las visitas a un sitio web y, a veces, entre ellas. Las cookies permiten que los dispositivos se diferencien de forma exclusiva de otros exploradores que visitan el sitio.

Las leyes, regulaciones y principios de autorregulación le obligan a obtener el consentimiento de los visitantes para poder almacenar o recuperar información en un ordenador u otro dispositivo conectado a Internet. El Adobe le sugiere que revise con el asesor legal de su organización qué leyes, regulaciones y principios controlan su uso de cookies.

## Acerca de las cookies de origen

Los servicios de Adobe Experience Cloud utilizan cookies para proporcionar información sobre variables y componentes que no persisten entre solicitudes de imagen y sesiones del explorador. Cuando es posible, el Adobe de utiliza cookies de origen para registrar las actividades del sitio. Para registrar la actividad en distintos sitios, como otros de sus dominios, se requieren cookies de terceros.

Muchos exploradores y aplicaciones antispyware están diseñados para rechazar y eliminar las cookies de terceros. El Adobe garantiza que las cookies siempre se puedan configurar, incluso si las de terceros están bloqueadas. El comportamiento específico varía en función de si utiliza el servicio de identidad de Experience Platform (servicio ECID) o los identificadores heredados de Analytics (como el `s_vi` cookie):

* El [Servicio de identidad del Experience Platform (servicio ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=es) establece automáticamente cookies de origen independientemente de si el dominio de recopilación coincide con el del sitio. Si no coinciden, el servicio de identidad utiliza JavaScript para establecer las cookies en el dominio del sitio.
* Si utiliza [Identificadores heredados de Analytics](analytics.md) (como el `s_vi` ), depende de cómo haya configurado su servidor de recopilación de datos. Si el servidor de recopilación de datos coincide con el dominio del sitio, las cookies se establecen como cookies de origen. Si el servidor de recopilación no coincide con su dominio actual, las cookies se establecen como de terceros. En este caso, si se bloquean las cookies de terceros, Analytics establece un identificador de reserva (`s_fid`) en lugar del estándar `s_vi` cookie.

Si desea asegurarse de que el servidor de recopilación coincida con el dominio del sitio, puede utilizar una implementación CNAME que permita el reenvío de un dominio personalizado especificado en su implementación CNAME a los servidores de recopilación de Adobe. Esta tarea implica cambios en la configuración DNS de su compañía para configurar un alias CNAME que señale a un dominio alojado de Adobe. Tenga en cuenta que, aunque varios productos de Adobe admiten el uso de un CNAME, en todos los casos se utiliza el CNAME para crear un punto final de confianza para un cliente específico y es propiedad de dicho cliente. Si controla varios dominios, pueden utilizar un único extremo CNAME para rastrear a los usuarios en sus dominios, pero siempre que el dominio del sitio no coincida con las cookies de dominio CNAME se establecen como de terceros.

>[!NOTE]
>
>Independientemente de si el dominio de recopilación coincide con el del sitio, el programa Intelligent Tracking Prevention (ITP) de Apple crea las cookies de origen configuradas por el Adobe de corta duración en exploradores que se rigen por ITP, que incluyen Safari en macOS y todos en iOS y iPadOS. A partir de noviembre de 2020, las cookies configuradas mediante CNAME también tienen la misma caducidad que las configuradas mediante JavaScript. Esta caducidad está sujeta a cambios.

## Cookies y privacidad

El mantenimiento de la privacidad del cliente y la seguridad de los datos son prioridades esenciales en Adobe. Adobe participa en varias organizaciones de privacidad y coopera con los reguladores de privacidad y los principios de autorregulación. Esta cooperación incluye el programa AdChoices de Digital Advertising Alliance para proporcionar a los clientes información sobre cómo se utiliza su información y las opciones sobre su uso.

La mayoría de las cookies establecidas por los productos de Experience Cloud no contienen información personal. Estas cookies y los datos asociados son seguros y se utilizan solamente para los informes de su compañía y para proporcionar contenido y anuncios relevantes. Los datos no están disponibles para terceros ni para otros clientes de Adobe, a menos que se utilicen en informes del sector agregados. Por ejemplo, el informe [!DNL Digital Marketing Insight Report] analiza los datos agregados y anónimos de los comerciantes.

Adobe no combina la información a nivel de navegador entre distintas empresas. Para proteger la privacidad y seguridad de los datos de los clientes, algunos de los servicios de la oferta de Experience Cloud cuentan con la capacidad de usar un conjunto de cookies distinto para cada sitio rastreado. Algunas ofertas también permiten a los clientes utilizar su propio nombre de dominio como propietario de la cookie. Esta práctica crea una capa adicional de privacidad y seguridad, ya que hace que las cookies de Experience Cloud sean *cookies de origen*, que pertenecen de forma permanente al sitio de la compañía.

Las cookies pueden almacenar y proporcionar solamente la información que se había depositado anteriormente en ellas. No pueden ejecutar código ni acceder a otra información almacenada en el equipo. Además, los exploradores web restringen el acceso a los datos de cookies. Los navegadores aplican una directiva de seguridad de cookies que hace que todos los datos de las cookies estén disponibles únicamente para el sitio Web que originalmente configuró la información.

Por ejemplo, los datos contenidos en las cookies configuradas desde el sitio web Adobe.com no se pueden ver en ningún otro sitio web que no sea Adobe.com.

El diagrama siguiente ilustra el uso de cookies para una solicitud de imagen estándar:

![Uso de cookies para una solicitud de imagen estándar](assets/CookiesProcessGraphic-01.png)

El diagrama siguiente ilustra el uso de cookies para una solicitud de imagen habitual (utilizado en situaciones en las que no se carga un archivo JS):

![Uso de cookies para una solicitud de imagen recta](assets/CookiesProcessGraphic2.png)
