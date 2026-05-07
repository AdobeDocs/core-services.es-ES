---
description: Descubra cómo los términos de la interfaz y del producto de Adobe difieren entre CX Enterprise, las soluciones de Experience Cloud, Creative Cloud, Experience League y otras experiencias de soporte.
solution: Experience Cloud
title: Terminología
feature-set: Experience Cloud Services
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: 3799f806-2794-43ab-9e70-06ee693871e7
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: bdea9bc8-5600-45db-b85e-d74bb59dfcff
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 504cdc98f97b744efa27d3c09cd69cf7f81412a4
workflow-type: tm+mt
source-wordcount: 692
ht-degree: 5%

---

# Terminología

<!--
TQID: https://experienceleague.adobe.com/6wm7HcuAbaV1iV3AgN55dY5WR---BnMM7lJgN0HZDsk
-->

Utilice esta tabla cuando la misma palabra aparezca en diferentes experiencias de Adobe (CX Enterprise, aplicaciones de marketing, aplicaciones de diseño o sitios de asistencia). No es un glosario completo; consulte la ayuda específica del producto en [Experience League](https://experienceleague.adobe.com/es) para obtener definiciones detalladas.

| Término | En CX Enterprise y esta guía | Otro uso común de Adobe |
| --- | --- | --- |
| **Adobe CX Enterprise** | La experiencia web unificada en `experience.adobe.com` donde abre aplicaciones de marketing, establece preferencias y notificaciones y llega a servicios de interfaz compartida (por ejemplo, Atributos del cliente y [Biblioteca de audiencias](../services/audiences/overview.md)). Anteriormente *Adobe Experience Cloud*. | No es el mismo producto que **Adobe Experience Platform** (infraestructura de datos del cliente, zonas protegidas, conjuntos de datos). No **Adobe Creative Cloud** (aplicaciones de diseño y multimedia). |
| **Adobe Experience Platform** | Aparece cuando conecta agentes de recopilación de datos, identidad o plataforma a sus soluciones; algunas funciones de búsqueda de navegación e IA están respaldadas por Platform. | Una plataforma de datos y orquestación. No utilice &quot;Experience Platform&quot; cuando se refiera al shell de CX Enterprise o a la página de inicio. |
| **Experience League** | Donde los vínculos de ayuda y del producto le envían **documentación**, **tutoriales**, listas de reproducción de aprendizaje, notas de la versión y contexto de comunidad para soluciones de Adobe. Comience en [Experience League home](https://experienceleague.adobe.com/es). | Complementa el **[Centro de ayuda de Adobe](https://helpx.adobe.com/es/support.html)**, que hace hincapié en la **cuenta**, el **plan**, la **facturación**, las descargas y la solución de problemas entre productos para particulares y equipos. Utilice el Centro de ayuda para restablecer contraseñas, planificar cambios y tareas similares; utilice Experience League para el contenido de procedimientos del producto. |
| **Ayudante de IA/IA auténtica** | Asistentes del producto y agentes organizados descritos en los temas de IA de esta guía; el acceso y los créditos dependen de los derechos del producto. | Otras superficies de Adobe (por ejemplo, **Firefly** o **Express**) utilizan características de &quot;IA&quot; con diferentes ámbitos y directivas. |
| **Organización** | Su **organización IMS**: el límite para las licencias empresariales, los directorios de usuario, el SSO y la administración de Admin Console en CX Enterprise. Ver [Organizaciones y vinculación de cuentas](../administration/organizations.md). | No es un *grupo de informes* de Analytics, una *propiedad* de Target ni una *zona protegida* de Experience Platform (son contenedores específicos de productos). |
| **Admin Console** | Plano de control empresarial en `adminconsole.adobe.com` para usuarios, perfiles de producto e identidad; vinculado desde los temas de CX Enterprise **Administration**. Consulte [Administración de usuarios y productos](../administration/admin-console.md). | Diferente de **administrador del producto** dentro de cada aplicación (por ejemplo, las pantallas de herramientas de administración de Analytics o de permisos de Journey Optimizer). |
| **Perfil del producto** | Paquete de licencias en Admin Console que concede acceso a un producto o una funcionalidad; los usuarios deben pertenecer a un perfil para tener derecho a él. Consulte [Administración de productos y perfiles](https://helpx.adobe.com/es/enterprise/using/manage-products.html). | No intercambiables con cada nombre de &quot;espacio de trabajo&quot;, &quot;contenedor&quot; o &quot;propiedad&quot; del producto; varían según la solución. |
| **Vinculación de cuentas** | Conexión de un inicio de sesión de aplicación (por ejemplo, credenciales de Analytics o Target) a su Adobe ID para la organización, de modo que los servicios reconozcan a un usuario. Ver [Organizaciones y vinculación de cuentas](../administration/organizations.md). | No es lo mismo que la configuración de **sincronización de directorios**, **SSO** o **federación** (esas son decisiones de identidad de toda la organización en Admin Console). |
| **Servicio de Experience Cloud ID / ECID** | El identificador de visitante persistente que se utiliza en todas las soluciones y que a menudo se implementa con etiquetas o Web SDK. Todavía se hace referencia comúnmente como **Experience Cloud ID** o **MID** en discusiones anteriores de Analytics. Consulte la [descripción general del servicio de ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=es). | Distinguen del nombre de cookie heredado de una sola aplicación o de los conceptos de gráfico de identidad de **Experience Platform**, aunque pueden relacionarse en una implementación. |
| **Atributos del cliente** | Atributos de CRM o empresariales que se cargan y asignan para su uso en Analytics, Target y flujos de trabajo relacionados a través del servicio People. Consulte los temas [Atributos del cliente](../services/customer-attributes/attributes.md). | No se equipare con **rasgos de Audience Manager** por sí solo o con cada campo de perfil de **Real-Time CDP** sin comprobar el límite del producto. |
| **Biblioteca de públicos** | IU de CX Enterprise para componer y compartir audiencias entre aplicaciones integradas. | **Audience Manager** y **Target** también usan &quot;audiencias&quot;, pero las reglas y los destinos de segmentación difieren según el producto. |
| **Segmento** (Analytics) | Una definición de audiencia basada en reglas que puede crear en Adobe Analytics y, cuando se admite, publicar para audiencias compartidas. | En **Audience Manager**, los segmentos combinan **rasgos**; los nombres se superponen, pero la implementación no es idéntica. En **Target**, las &quot;audiencias&quot; reemplazaron etiquetas de &quot;segmento&quot; antiguas en muchos lugares. |
| **Assets (Experience Cloud Assets)** | Carpetas y archivos compartidos para la colaboración entre los flujos de trabajo de marketing de CX Enterprise y **usuarios de Creative Cloud** aprobados. Ver [descripción general de Assets](../services/assets/experience-cloud-assets.md). | En **Creative Cloud**, &quot;recursos&quot; suele significar archivos de diseño (PSD, AI, INDD). La misma palabra, diferentes modelos de compartir y gobernanza. |

{style="table-layout:auto"}

