---
description: Información general sobre nuevas funciones y actualizaciones de Experience Cloud.
keywords: servicios principales
seo-description: Información general sobre nuevas funciones y actualizaciones de Experience Cloud.
seo-title: Novedades de Experience Cloud
solution: Experience Cloud
title: Novedades de Experience Cloud
uuid: bc 1 b 1542-1 a 37-4 da 1-bcfd-fc 86 af 881642
translation-type: tm+mt
source-git-commit: af5339fe58ce884345804574c209907d6504a483

---


# Novedades de Experience Cloud

Información general sobre nuevas funciones y actualizaciones de Experience Cloud.

## Agosto de 2018 {#section_7388CDAB723B49809AABEFEE85CF6378}

Correcciones y mejoras para agosto de 2018.

* Se han realizado mejoras en la sincronización de comentarios de activos entre Creative Cloud y Experience Cloud. (CORE-15971)
* Se ha añadido un indicador de función para controlar la sincronización de recursos de Experience Cloud-Creative Cloud. (CORE-15938)
* Se han realizado mejoras en la creación de segmentos de audiencias, incluida una mejor experiencia de búsqueda y listado. (CORE-5833, CORE-14278)
* Se ha corregido un problema de alta prioridad que bloqueaba el uso compartido de carpetas desde MAC a Creative Cloud. (CORE-16677)

## 19 de julio de 2018 {#section_EBB549EBABB7480884A180237ADCCD02}

Correcciones y mejoras para julio de 2018.

* Se ha implementado una capacidad back-end para controlar el uso compartido de activos entre Experience Cloud y AEM, y Experience Cloud y Creative Cloud. (CORE-14386)
* Se ha arreglado un problema que bloqueaba en algunos entornos el aprovisionamiento de nuevos inquilinos. (CORE-15509)
* Se ha corregido un problema que redireccionaba a los usuarios a [!DNL marketing.adobe.com] al acceder a [!DNL experiencecloud.adobe.com] a través de [!DNL http] en lugar de [!DNL https] (protegido). (CORE-15587)
* Se ha arreglado un problema que bloqueaba las notificaciones para algunos inquilinos nuevos. (CORE-15240)

## 14 de junio de 2018 {#section_7ABC327992CB46B0B8E4A631B8B68899}

Correcciones y mejoras para la versión de junio de 2018.

* Se ha habilitado un enlace para acceder al RGPD para los administradores. (CORE-11731)
* Se ha actualizado la función Beta Feedback para restringir los tipos de archivo que se pueden adjuntar a los comentarios. (CORE-10474)
* Se ha solucionado un problema que se producía al eliminar audiencias de la Biblioteca de audiencias. (CORE-12792)
* Se ha solucionado un problema que provocaba la aparición de una pantalla en blanco al acceder a enlaces de Workspace con Federated IDs. (CORE-11620)

## 10 de mayo de 2018 {#section_498AF78DA17C4720AA0F32B51493E550}

Nuevas características y correcciones de la interfaz de [!DNL Adobe Experience Cloud].

| Función | Descripción |
|--- |--- |
| Nueva página de aterrizaje de administración | Cuando inicia sesión en Experience Cloud y va a la página de administración, tiene a su disposición una nueva interfaz intuitiva para ayudarle a acceder rápidamente a las soluciones y servicios principales de Experience Cloud. |
**Correcciones**

* Se ha corregido un problema que provocaba que la imagen no se cargase debido a una actualización de Scene7. (CORE-12746)
* Se han efectuado actualizaciones a fin de retirar la compatibilidad con el protocolo TLS 1.0, como indica PCI, para eliminar una vulnerabilidad de seguridad. (CORE-7695)

## 26 de octubre de 2017 {#section_11195859B4094177A939C0561428B525}

**Problema conocido**

Muchas de las notificaciones de mantenimiento relativas a mantenimientos programados y actualizaciones de productos no aparecen en el resumen de notificaciones por correo electrónico. Estamos trabajando para asegurar que todas las notificaciones de mantenimiento se incluyan en el resumen por correo electrónico.

## 8 de agosto de 2017 {#section_2313A875454044F490B418506DD24593}

| Función | Descripción |
|--- |--- |
| Notificaciones: ajustes granulares | Puede activar notificaciones para eventos y actividades de productos y soluciones, incluida la notificación de la actividad de carga de [ Atributos de cliente ](../attributes/attributes.md).        |
| Notificaciones relativas al mantenimiento | En la configuración de Notificaciones, puede activar las notificaciones relativas al mantenimiento para productos y soluciones. |
| Admin Console para soluciones de Experience Cloud | Los nuevos clientes de Experience Cloud pueden comenzar a usar Admin Console, una ubicación centralizada para la administración de autorizaciones para toda la organización.<br>La migración a Admin Console para la administración de usuarios se realizará en oleadas. Adobe se pondrá en contacto (con los administradores del sistema) cuando sea el momento de la migración.<br>Los administradores de Analytics deben consultar [Migración de Analytics](https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/). |

## 22 de mayo de 2017 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| Función | Descripción |
|--- |--- |
| Asignación de grupos de informes por lotes | En  Administración  &gt;  Report Suite Mapping , ahora es posible seleccionar varios grupos de informes y asignarlos a una organización. (Anteriormente, había que hacerlo de forma individual).  <br>[Asignar grupos de informes](../core-services/core-services.md) a una sola organización ayuda a habilitar en Experience Cloud funciones y servicios entre soluciones. |
| Actualizaciones en las audiencias de Experience Cloud | **Aplicación de suitesahora**<br>puede aplicar un grupo de informes a todas las [reglas de audiencia](../audience-library/t-audience-create.md). (Anteriormente, había que especificar un grupo de informes en cada definición de regla). <br>**Propiedades y variablesahora**<br>puede incluir props y variables predeterminadas de Analytics (además de evars y eventos) en audiencias en tiempo real. |

## 8 de noviembre de 2016 - 16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| Función | Descripción |
|--- |--- |
| Actualización de Perfil y contraseñas | Los usuarios ya no pueden editar los datos del perfil de usuario de IMS en Datos personales en Editar perfil &gt; Perfil y contraseñas. En su lugar, se redirige a los usuarios `accounts.adobe.com`. Esto se aplica a todos los tipos de identidad (Adobe ID, empresa y federada).        |

**Correcciones**

* Se ha corregido un problema con las contraseñas técnicas que provocaba un error al compartir carpetas entre Creative Cloud y Experience Cloud. (MAC-31067, MAC-32014)
* Se ha corregido un problema con la carga de algunos tipos de archivos, incluido PDF, que surgía tras la versión de octubre en Assets Core Service. (MAC-32517)

