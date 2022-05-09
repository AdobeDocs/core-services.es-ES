---
description: Obtenga información sobre la compatibilidad de exploradores, y consulte las preguntas frecuentes y sus respuestas para administradores de Adobe Experience Cloud.
keywords: servicios principales, Experience Cloud, Experience Platform, Analytics, Target, administración de usuarios.
solution: Experience Cloud
title: 'Preguntas frecuentes sobre Experience Cloud '
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 062576da-328e-4b46-9e71-5a25733d607a
source-git-commit: 55c81003b94b7e033cddb6854b5c1f1c1ffa199c
workflow-type: ht
source-wordcount: '776'
ht-degree: 100%

---

# Preguntas frecuentes sobre Experience Cloud

Obtenga información sobre la compatibilidad del explorador y las preguntas frecuentes y respuestas para los administradores de Experience Cloud.

## ¿Qué exploradores son compatibles con Experience Cloud?

* Microsoft® Edge (versión actual y dos versiones anteriores)
* Google Chrome (versión actual y dos versiones anteriores)
* Mozilla Firefox (versión actual y dos versiones anteriores)
* Safari (versión actual y dos versiones anteriores)
* Opera (versión actual y dos versiones anteriores)

## ¿Cómo sé si mis aplicaciones están habilitadas para los servicios principales?

Si su implementación no se ha aprovisionado para servicios principales, consulte [Habilitación de las aplicaciones para servicios principales](core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C), que describe cómo:

1. [Únase a Experience Cloud y conviértase en administrador](core-services.md#section_2423F0BD3DF642658103310EE5EA6154)
1. [Implementar el Servicio de Experience Cloud ID con Experience Platform Launch](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html?lang=es).
1. [Asigne grupos de informes a una organización de Experience Cloud](core-services.md#concept_apg_zq2_rw)
1. [(Solo Analytics) Modernizar el código AppMeasurement de Analytics](core-services.md#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [(Solo para Adobe Target) Modernizar la implementación de Adobe Target](core-services.md#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [Verificar la implementación](core-services.md#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [Administración de usuarios y productos](core-services.md#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [Empezar a utilizar los servicios principales](core-services.md#section_960C06093623462E8EA247B3E97274A1)

Para obtener más ayuda, [póngase en contacto con el Servicio de atención al cliente de Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;lang=es#support).

## ¿Cobra Adobe a mi empresa por el acceso a Experience Cloud?

No. Experience Cloud se incluye sin coste adicional. Sin embargo, algunos servicios básicos podrían conllevar costes adicionales.

## ¿Por qué debe mi empresa iniciar sesión a través de la interfaz de Experience Cloud?

La funcionalidad proporcionada por la interfaz de Experience Cloud añade un nuevo valor a su negocio. También es la ruta estándar para acceder a las aplicaciones a partir de ahora y, con el tiempo, reemplazará otros flujos de inicio de sesión de aplicaciones individuales. El inicio de sesión a través de Experience Cloud facilita una transición más fluida posteriormente.

## ¿Cómo puedo resolver mis dudas acerca de la migración de mi empresa?

[Póngase en contacto con el Servicio de atención al cliente de Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;lang=es#support).

## ¿Cómo se puede [!DNL Adobe Support] acceder a mi entorno de nube de Adobe para solucionar un problema?

[!DNL Adobe Support] puede enviar una solicitud de suplantación para la que recibirá un correo electrónico de marca Adobe (ejemplo abajo) en el que solicite su autorización explícita. El acceso se concede por tiempo limitado. Una vez concedido, usted puede revocarlo en cualquier momento. Adobe registra todas las acciones realizadas por los representantes de Adobe.

![Caso de soporte de Adobe](assets/support-email.png)

## ¿Qué es el _aprovisionamiento?_

El aprovisionamiento de Experience Cloud significa que:

* Sus usuarios pueden empezar a iniciar sesión en [!DNL Experience Cloud] y a vincular aplicaciones.
* Pueden empezar a utilizar las funcionalidades disponibles a través de Experience Cloud, como Usuarios.
* Puede prepararse para abandonar el proceso de inicio de sesión basado en cada aplicación.
* Puede conservar el control de acceso a las distintas aplicaciones.

## ¿Cómo administro los usuarios y perfiles de producto?

* Consulte la [Guía del usuario de Admin Console](https://helpx.adobe.com/es/enterprise/admin-guide.html) para obtener ayuda.

* La administración de autorizaciones y productos de los usuarios se realiza en [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) (vínculo del producto).

* **Importante:** Los administradores de Analytics pueden consultar [Administrar usuarios de Analytics en Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/migrate-users/c-migration-tool.html?lang=es) para saber más sobre la migración de ID de usuarios de las herramientas de administración de Analytics a Admin Console.

## ¿Qué puedo hacer si alguien no puede iniciar sesión en la interfaz de Experience Cloud?

Los administradores de Admin Console pueden otorgar acceso a los usuarios. Los usuarios reciben correos electrónicos con instrucciones de inicio de sesión.

Es posible que deba [ponerse en contacto con el equipo de atención al cliente de Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;lang=es#support) para verificar que su empresa esté plenamente aprovisionada.

## ¿Dónde puede ir un usuario para administrar la vinculación de cuentas?

Es posible que algunos usuarios deban vincular su cuenta de aplicaciones (Analytics) al Adobe ID o Enterprise ID.

Consulte [Vinculación de una cuenta de aplicaciones a un Adobe ID](organizations.md#task_FD389E78640848919E247AC5E95B8369).

## ¿Cómo administro los perfiles y organizaciones de las cuentas de los usuarios?

Consulte [Administración de cuentas de usuario](organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1).

## ¿Qué es una organización?

Una [organización](organizations.md) es la entidad que permite a un administrador configurar grupos y usuarios, así como controlar el inicio de sesión único en Experience Cloud. La organización funciona como una empresa de inicio de sesión que abarca todos los productos y aplicaciones de Experience Cloud. La mayoría de las veces, la organización es el nombre de empresa. Sin embargo, una empresa puede tener muchas organizaciones.

## ¿Dónde puedo encontrar mi ID de organización de IMS?

Consulte [Visualización del ID de la organización](organizations.md) para obtener más información.

## ¿Qué debo hacer cuando uno de mis usuarios abandona la empresa?

Su acceso deberá ser eliminado de la aplicación en sí. No podrán acceder al producto desde Experience Cloud ni a través del inicio de sesión directo. También debe eliminarlos en el nivel de Experience Cloud.

## ¿Qué es un Adobe ID?

Consulte [Tipos de identidad](https://helpx.adobe.com/es/enterprise/using/identity.html).

## ¿Puedo vincular cuentas de aplicación para mis usuarios?

No. Los usuarios deben vincular sus propias aplicaciones con sus nombres de usuario y contraseñas.

## ¿Por qué veo Social si mi empresa no lo tiene?

Adobe Social es un producto que se puede vender con Analytics. Por lo tanto, si tiene Analytics, verá esta aplicación, pero no tendrá acceso a ella a menos que la haya adquirido.
