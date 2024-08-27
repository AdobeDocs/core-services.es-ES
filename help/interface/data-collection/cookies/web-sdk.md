---
title: Cookies del SDK web de Adobe Experience Platform
description: Descubra cómo el SDK web utiliza cookies aplicables a su implementación.
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
source-git-commit: 2a80851c0a7d4ef7dbcc2565177b239f3e063164
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# Cookies del SDK web de Adobe Experience Platform

El SDK web de Adobe Experience Platform utiliza cookies para almacenar valores específicos de la implementación.

| Nombre | Edad máxima | Descripción |
|---|---|---|
| **kndct_orgid_identity** | 34128000 (395 días) | Almacena el ECID, así como otra información relacionada con el ECID. |
| **kndctr_orgid_permission_check** | 7200 (2 horas) | Indica al servidor que busque las preferencias de consentimiento del lado del servidor. |
| **kndctr_orgid_permission** | 15552000 (180 días) | Almacena la preferencia de consentimiento del usuario para el sitio web. |
| **kndctr_orgid_cluster** | 1800 (30 minutos) | Almacena la región del Edge Network que sirve las solicitudes del usuario actual. La región se utiliza en la ruta URL para que el Edge Network pueda enrutar la solicitud a la región correcta. Si un usuario se conecta con una dirección IP diferente o en una sesión diferente, la solicitud se vuelve a dirigir a la región más cercana. |
| **mbox** | 63072000 (2 años) | Presente cuando la configuración de migración de Target se establece en verdadera. Permite que el SDK web establezca la cookie [mbox](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) de Target. |
| **mboxEdgeCluster** | 1800 (30 minutos) | Presente cuando la configuración de migración de Target se establece en verdadera. Permite al SDK web comunicar el clúster perimetral correcto a `at.js` para que los perfiles de Target puedan permanecer sincronizados a medida que los usuarios navegan por un sitio. |
| **AMCV_###@AdobeOrg** | 34128000 (395 días) | Presente cuando [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/idmigrationenabled) está habilitado. Ayuda al realizar la transición al SDK web mientras algunas partes del sitio siguen utilizando `visitor.js`. |

El Edge Network establece todas las cookies con los atributos `secure` y `sameSite="none"`. Si actualmente tiene secciones seguras y no seguras en el sitio web, la identificación del usuario puede ser inexacta. Cuando un usuario navega de una sección segura del sitio a una sección no segura, el Edge Network genera un nuevo(a) `ECID` con la solicitud.
