---
title: Cookies de Adobe Experience Platform Web SDK
description: Descubra cómo Web SDK utiliza cookies aplicables a su implementación.
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
source-git-commit: e63dd988abba199049da2b3620eed9ebf51043d1
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---

# Cookies de Adobe Experience Platform Web SDK

Adobe Experience Platform Web SDK utiliza cookies para almacenar valores específicos de la implementación.

| Nombre | Edad máxima | Tamaño | Descripción |
|---|---|---|---|
| **kndctr_&lt;ORG_ID>_identity** | 34128000 (395 días) | 100 a 120 bytes (variable) | Almacena el ECID, así como otra información relacionada con el ECID. |
| **kndctr_&lt;ORG_ID>_permission** | 15552000 (180 días) | 10 a 11 bytes | Almacena la preferencia de consentimiento del usuario para el sitio web. |
| **kndctr_&lt;ORG_ID>_cluster** | 1800 (30 minutos) | 3 a 5 bytes | Almacena la región de Edge Network que sirve las solicitudes del usuario actual. La región se utiliza en la ruta URL para que Edge Network pueda enrutar la solicitud a la región correcta. Si un usuario se conecta con una dirección IP diferente o en una sesión diferente, la solicitud se vuelve a dirigir a la región más cercana. |
| **mbox** | 63072000 (2 años) | | Presente cuando la configuración de migración de Target se establece en verdadera. Permite que Web SDK establezca la [cookie de mbox](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) de Target. |
| **mboxEdgeCluster** | 1800 (30 minutos) | | Presente cuando la configuración de migración de Target se establece en verdadera. Permite que Web SDK comunique el clúster perimetral correcto a `at.js` para que los perfiles de Target puedan permanecer sincronizados a medida que los usuarios navegan por un sitio. |
| **AMCV_###@AdobeOrg** | 34128000 (395 días) | | Presente cuando [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/idmigrationenabled) está habilitado. Ayuda al realizar la transición a Web SDK mientras algunas partes del sitio siguen utilizando `visitor.js`. |

Edge Network establece todas las cookies con los atributos `secure` y `sameSite="none"`. Si actualmente tiene secciones seguras y no seguras en el sitio web, la identificación del usuario puede ser inexacta. Cuando un usuario navega de una sección segura del sitio a una sección no segura, Edge Network genera un nuevo(a) `ECID` con la solicitud.

