---
description: Información general sobre nuevas funciones y actualizaciones de Experience Cloud.
keywords: servicios principales
seo-description: Información general sobre nuevas funciones y actualizaciones de Experience Cloud.
seo-title: Novedades de Experience Cloud
solution: Experience Cloud
title: 'Novedades de Experience Cloud '
uuid: bc1b1542-1a37-4da1-bcfd-fc86af881642
source-git-commit: ebefd433e96da422674e7ee71c8988d4011fed11
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 89%

---


# Novedades de Experience Cloud

Información general sobre nuevas funciones y actualizaciones de Experience Cloud.

## Agosto de 2018 {#section_7388CDAB723B49809AABEFEE85CF6378}

Correcciones y mejoras para la versión de agosto de 2018.

* Se han realizado mejoras en la sincronización de comentarios de recursos entre Creative Cloud y Experience Cloud. (CORE-15971)
* Se ha agregado una marca para controlar la sincronización de recursos entre Experience Cloud y Creative Cloud. (CORE-15938)
* Se han realizado mejoras en la creación de segmentos de audiencia, incluida una mejor experiencia de búsqueda y listado. (CORE-5833, CORE-14278)
* Se ha corregido un problema de alta prioridad que bloqueaba el uso compartido de carpetas desde Experience Cloud a Creative Cloud. (CORE-16677)

## 19 de julio de 2018 {#section_EBB549EBABB7480884A180237ADCCD02}

Correcciones y mejoras para julio de 2018.

* Se ha implementado una capacidad back-end para controlar el uso compartido de recursos entre Experience Cloud y AEM, y Experience Cloud y Creative Cloud. (CORE-14386)
* Se ha corregido un problema que bloqueaba el aprovisionamiento de nuevos inquilinos en algunos entornos. (CORE-15509)
* Se ha corregido un problema que redireccionaba a los usuarios a [!DNL experiencecloud.adobe.com] al acceder a [!DNL experiencecloud.adobe.com] a través de [!DNL http] en lugar de [!DNL https] (protegido). (CORE-15587)
* Se ha corregido un problema que bloqueaba las notificaciones de algunos inquilinos nuevos. (CORE-15240)

## 14 de junio de 2018 {#section_7ABC327992CB46B0B8E4A631B8B68899}

Correcciones y mejoras para junio de 2018.

* Se habilitó un vínculo al acceso de RGPD para administradores. (CORE-11731)
* Se ha actualizado la función de comentarios beta para restringir los tipos de archivo que se pueden adjuntar a los comentarios. (CORE-10474)
* Se ha corregido un problema con la eliminación de audiencias de la biblioteca de audiencias. (CORE-12792)
* Se ha solucionado un problema que provocaba la aparición de una pantalla en blanco al acceder a enlaces de Workspace con Federated ID. (CORE-11620)

## 10 de mayo de 2018  {#section_498AF78DA17C4720AA0F32B51493E550}

Nuevas características y correcciones de la interfaz de [!DNL Adobe Experience Cloud].

| Función | Descripción |
|--- |--- |
| Nueva página de aterrizaje de administración | Al iniciar sesión en Experience Cloud y navegar a la página Administración, hay una nueva interfaz intuitiva que le ayudará a acceder rápidamente a sus soluciones de Experience Cloud y a los servicios principales. |

**Correcciones**

* Se corrigió un problema en el cual la carga de imágenes fallaba debido a una actualización de Scene7. (CORE-12746)
* Se han realizado actualizaciones para dejar de admitir el protocolo TLS 1.0, según lo dispuesto por PCI para eliminar la vulnerabilidad de seguridad. (CORE-7695)

## 26 de octubre de 2017 {#section_11195859B4094177A939C0561428B525}

**Problema conocido**

Muchas de las notificaciones de mantenimiento relacionadas con el mantenimiento programado o las actualizaciones de productos no aparecen en el resumen de notificaciones por correo electrónico. Estamos trabajando para garantizar que todas las notificaciones de mantenimiento se incluyan en el compendio de correo electrónico.

## 8 de agosto de 2017  {#section_2313A875454044F490B418506DD24593}

| Función | Descripción |
|--- |--- |
| Notificaciones: Configuración granular | Puede activar notificaciones para eventos y actividades de productos y soluciones, incluida la notificación de la actividad de carga de [Atributos de cliente](attributes.md). |
| Notificaciones: Notificaciones de mantenimiento | En la configuración de Notificaciones, puede activar las notificaciones de mantenimiento para productos y soluciones. |
| Admin Console para soluciones de Experience Cloud | Los nuevos clientes de Experience Cloud pueden empezar a utilizar Admin Console, una ubicación central para administrar las autorizaciones de Adobe en toda la organización.<br>La migración a Admin Console para la administración de usuarios se realizará en oleadas. Adobe se pone en contacto con usted (administradores del sistema) cuando es hora de migrar.<br>Los administradores de Analytics pueden consultar [Migración de Analytics](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=en). |

## 22 de mayo de 2017 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| Función | Descripción |
|--- |--- |
| Asignación de grupos de informes en lotes | En  Administración  >  Report Suite Mapping, ahora es posible seleccionar varios grupos de informes y asignarlos a una organización. (Anteriormente, había que hacerlo de forma individual).  <br>[Asignar grupos de informes](core-services.md) a una sola organización ayuda a habilitar en Experience Cloud funciones y servicios entre soluciones. |
| Actualizaciones en las audiencias de Experience Cloud | **Aplicación de conjuntos de informes**<br> Ahora puede aplicar un grupo de informes a todas sus [reglas de audiencia](t-audience-create.md). (Anteriormente, había que especificar un grupo de informes en cada definición de regla). <br>**Props y variables**<br> Ahora puede incluir props y variables predeterminadas de Analytics (además de eVars y eventos) en las audiencias en tiempo real. |

## 8 de noviembre de 2016: 16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| Función | Descripción |
|--- |--- |
| Actualizar a Perfiles y contraseñas | Los usuarios ya no pueden editar los datos del perfil de usuario de IMS en Datos personales en Editar perfil > Perfil y contraseñas. Ahora se les redirige a `accounts.adobe.com`. Esta actualización se aplica a todos los tipos de identidad (Adobe ID, Enterprise y Federated). |

**Correcciones**

* Se ha corregido un problema con las contraseñas técnicas que provocaba un error al compartir carpetas entre Creative Cloud y Experience Cloud. (MAC-31067, MAC-32014)
* Se ha corregido un problema con la carga de algunos tipos de archivos, incluido PDF, que surgía tras la versión de octubre en el servicio principal de Assets. (MAC-32517)
