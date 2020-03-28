---
description: Preguntas y respuestas comunes para los administradores de Experience Cloud.
keywords: core services, Experience Cloud, Experience Platform, Analytics, Target, user management.
seo-description: Preguntas y respuestas comunes para los administradores de Experience Cloud.
seo-title: Preguntas más frecuentes sobre los servicios principales de Experience Cloud.
solution: Adobe Experience Cloud
title: Preguntas frecuentes
index: true
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Preguntas más frecuentes sobre Experience Cloud

Preguntas y respuestas comunes para los administradores de Experience Cloud.

## ¿Cómo sé si mis soluciones están habilitadas para los servicios principales?

Si su implementación no se ha aprovisionado para servicios principales, consulte [Habilitar las soluciones para servicios principales](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C), que describe cómo:

1. [Únase a Experience Cloud y conviértase en administrador](../core-services/core-services.md#section_2423F0BD3DF642658103310EE5EA6154)
1. [Implemente el servicio Experience Cloud ID con Experience Platform Launch](https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html).
1. [Asignación de grupos de informes a una organización de Experience Cloud](../core-services/core-services.md#concept_apg_zq2_rw)
1. [(Solo Analytics) Modernizar el código AppMeasurement de Analytics](../core-services/core-services.md#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [(Solo Adobe Destinatario) Modernizar la implementación de Adobe Destinatario](../core-services/core-services.md#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [Verificar la implementación de los servicios principales](../core-services/core-services.md#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [Administración de usuarios y productos](../core-services/core-services.md#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [Empezar a utilizar los servicios principales](../core-services/core-services.md#section_960C06093623462E8EA247B3E97274A1)

Para obtener más ayuda, [póngase en contacto con el servicio de asistencia](https://helpx.adobe.com/marketing-cloud/contact-support.html)de Adobe.

## ¿Cobra Adobe a mi empresa por el acceso a Experience Cloud?

No. Experience Cloud se incluye sin coste adicional. Sin embargo, algunos servicios básicos podrían tener costos adicionales.

## ¿Por qué debe mi empresa iniciar sesión a través de la interfaz de Experience Cloud?

La funcionalidad proporcionada por la interfaz de Experience Cloud añade un nuevo valor a su negocio. También será la ruta estándar para acceder a las soluciones a partir de ahora, reemplazando con el tiempo otros flujos de inicio de sesión de soluciones individuales. El inicio de sesión a través de Experience Cloud facilitará una transición más fluida posteriormente.

## ¿Cómo puedo resolver mis dudas acerca de la migración de mi empresa?

[Póngase en contacto con el servicio de asistencia](https://helpx.adobe.com/marketing-cloud/contact-support.html)de Adobe.

## ¿Qué es el _aprovisionamiento?_

El aprovisionamiento de Experience Cloud significa que:

* Sus usuarios pueden empezar a iniciar sesión en [!DNL Experience Cloud] y a vincular soluciones.
* Pueden empezar a utilizar las funciones disponibles a través de Experience Cloud, como Personas.
* Puede estar preparado para retirar el proceso de inicio de sesión específico de la solución.
* Puede conservar el control de acceso con las soluciones.

## ¿Cómo administro los usuarios y perfiles de producto?

* Consulte la Guía [del usuario de la Consola de](https://helpx.adobe.com/enterprise/administering/user-guide.html) administración para obtener ayuda.

* La administración de autorizaciones y productos de los usuarios se realiza en [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) (vínculo del producto).

* **Importante:** Los administradores de Analytics pueden consultar [Administrar usuarios de Analytics en Admin Console](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html) sobre la migración de ID de usuario de las herramientas de administración de Analytics a Admin Console.

## ¿Qué puedo hacer si alguien no puede iniciar sesión en la interfaz de Experience Cloud?

Los administradores de Admin Console pueden otorgar acceso a los usuarios. Los usuarios reciben correos electrónicos con instrucciones de inicio de sesión.

You might need to [Contact Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) to verify that your company has been fully provisioned.

## ¿Dónde puede ir un usuario para administrar la vinculación de cuentas?

Es posible que algunos usuarios deban vincular su cuenta de solución (Analytics) al Adobe ID o Enterprise ID.

See [Link a solution account to an Adobe ID](../admin-getting-started/organizations.md#task_FD389E78640848919E247AC5E95B8369).

## ¿Cómo administro los perfiles y organizaciones de las cuentas de los usuarios?

Consulte [Administración de cuentas de usuario](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1).

## ¿Qué es una organización?

Una organización de ** es la entidad que permite a un administrador configurar grupos y usuarios, así como para controlar el inicio de sesión único en Experience Cloud. La organización funciona como una empresa de inicio de sesión que abarca todos los productos y soluciones de Experience Cloud. La mayoría de las veces, una organización es su nombre de compañía. Sin embargo, una compañía puede tener muchas organizaciones.

## ¿Dónde puedo encontrar mi ID de organización de IMS?

Consulte [Búsqueda del ID de organización](organizations.md).

El ID de organización se muestra en la página de inicio de Experience Cloud y en [la página de inicio de Admin Console](https://adminconsole.adobe.com).

Alternatively, administrators can log into the Admin console (Navigate to [https://adminconsole.adobe.com](https://adminconsole.adobe.com#)) for a specific organization, and you will be able to see your IMS org ID in the URL.

Por ejemplo, en la siguiente dirección URL:

`https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

el identificador es

`C538193582390300A495CC9@AdobeOrg`

## ¿Qué debo hacer cuando uno de mis usuarios abandona la empresa?

Su acceso deberá ser eliminado de la solución en sí. No podrán acceder al producto desde Experience Cloud ni a través del inicio de sesión directo. También debe eliminarlos en el nivel de Experience Cloud.

## ¿Qué es un Adobe ID?

Consulte Tipos [de identidad](https://helpx.adobe.com/enterprise/help/identity.html).

## ¿Puedo vincular cuentas de solución para mis usuarios?

No. Los usuarios deben vincular sus propias soluciones con sus nombres de usuario y contraseñas.

## ¿Por qué veo Social si mi empresa no lo tiene?

Adobe Social es un producto que se puede vender con Analytics. Por lo tanto, si tiene Analytics, verá esta solución, pero no tendrá acceso a ella a menos que la haya adquirido.
