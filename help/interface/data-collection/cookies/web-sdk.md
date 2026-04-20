---
title: Cookies de Adobe Experience Platform Web SDK
description: Descubra cómo Web SDK utiliza cookies aplicables a su implementación.
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
TQID: https://experienceleague.adobe.com/jysQ5m7o0cI3ECKz2RWZB4Kt3own7XAPm04pr4yLh-k
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a42153ba5a885509e7735e7407e38586fcabb0ad
workflow-type: tm+mt
source-wordcount: 484
ht-degree: 1%

---

# Cookies de Adobe Experience Platform Web SDK

Adobe Experience Platform Web SDK utiliza cookies para almacenar valores específicos de la implementación.

| Nombre | Edad máxima | Tamaño | Descripción |
| --- | --- | --- | --- |
| **`AMCV_###@AdobeOrg`** | 34128000 (395 días) | 100 a 120 bytes (variable) | Presente cuando [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled) está habilitado. Ayuda al realizar la transición a Web SDK mientras algunas partes del sitio siguen utilizando `visitor.js`. Web SDK lee y escribe en esta cookie durante la migración. |
| **`com.adobe.alloy.getTld`** | Ninguno (eliminado inmediatamente) | N/A | Cookie de ayuda temporal utilizada internamente por Web SDK para determinar el dominio de nivel superior del sitio actual. Una vez establecido el dominio de nivel superior, se elimina la cookie. No almacena datos de comportamiento o de perfil. |
| **`demdex`** | 15552000 (180 días) | varía | Presente si la sincronización de Audience Manager ID está habilitada. Audience Manager establece esta cookie para asignar un ID único y admitir la sincronización, segmentación, modelado e informes de ID. Ver `demdex` en [cookies de Audience Manager](audience-manager.md). |
| **`kndctr_<orgId>_identity`** | 34128000 (395 días) | 100 a 120 bytes (variable) | Almacena el ECID y otra información relacionada para ese dispositivo. |
| **`kndctr_<orgId>_cluster`** | 1800 (30 minutos) | 3 a 5 bytes | Almacena la región de Edge Network (ubicación) que sirve las solicitudes del usuario actual. La región se utiliza en la ruta URL para que Edge Network pueda enrutar la solicitud a la región correcta. Si un usuario se conecta con una dirección IP diferente dentro de la duración de la cookie, la solicitud se vuelve a enrutar a la región más cercana. |
| **`kndctr_<orgId>_consent`** | 15552000 (180 días) | 10 a 11 bytes | Almacena las preferencias de consentimiento del visitante. Establezca siempre independientemente del consentimiento, ya que almacena las propias preferencias de consentimiento. |
| **`kndctr_<orgId>_consent_check`** | 7200 (2 horas) | | Asistente con ámbito de sesión que indica a Edge Network que vuelva a comprobar el consentimiento del lado del servidor después de que caduque el TTL. Aplica un TTL al consentimiento almacenado en caché. |
| **`kndctr_<orgId>_personalization`** | 34128000 (395 días) | | Almacena la información de sesión que utiliza Adobe Target para personalizar el contenido. |
| **`mbox`** | 63072000 (2 años) | | Presente cuando [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) está habilitado. Permite que Web SDK establezca la [cookie de mbox](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) de Target. |
| **`mboxEdgeCluster`** | 1800 (30 minutos) | | Presente cuando [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) está habilitado. Permite que Web SDK comunique el clúster perimetral correcto a `at.js` para que los perfiles de Target puedan permanecer sincronizados a medida que los usuarios navegan por un sitio. |
| **`s_ecid`** | 63115200 (2 años) | ~45 bytes | Contiene una copia del CX Enterprise ID (ECID/MID) con el formato `s_ecid=MCMID\|<ECID>`. Actúa como una copia de seguridad de origen de ECID, principalmente para escenarios CNAME (de origen). |

Edge Network establece todas las cookies con los atributos `secure` y `sameSite="none"`. Si actualmente tiene secciones seguras y no seguras en el sitio web, la identificación del usuario puede ser inexacta. Cuando un usuario navega de una sección segura del sitio a una sección no segura, Edge Network genera un nuevo(a) `ECID` con la solicitud.
