---
title: Cookies de Adobe Experience Platform Web SDK
description: Descubra cómo Web SDK utiliza cookies aplicables a su implementación.
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
source-git-commit: 97b3db58a9bf25ec0a6dd18c7b62117063e58407
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 1%

---

# Cookies de Adobe Experience Platform Web SDK

Adobe Experience Platform Web SDK utiliza cookies para almacenar valores específicos de la implementación.

| Nombre | Edad máxima | Tamaño | Descripción |
|---|---|---|---|
| **`AMCV_###@AdobeOrg`** | 34128000 (395 días) | 100 a 120 bytes (variable) | Presente cuando [`idMigrationEnabled`](https://experienceleague.adobe.com/es/docs/experience-platform/collection/js/commands/configure/idmigrationenabled) está habilitado. Ayuda al realizar la transición a Web SDK mientras algunas partes del sitio siguen utilizando `visitor.js`. Web SDK lee y escribe en esta cookie durante la migración. |
| **`demdex`** | 15552000 (180 días) | varía | Presente si la sincronización de Audience Manager ID está habilitada. Audience Manager establece esta cookie para asignar un ID único y admitir la sincronización, segmentación, modelado e informes de ID. Ver `demdex` en [cookies de Audience Manager](audience-manager.md). |
| **`kndctr_<orgId>_identity`** | 34128000 (395 días) | 100 a 120 bytes (variable) | Almacena el ECID y otra información relacionada para ese dispositivo. |
| **`kndctr_<orgId>_cluster`** | 1800 (30 minutos) | 3 a 5 bytes | Almacena la región de Edge Network (ubicación) que sirve las solicitudes del usuario actual. La región se utiliza en la ruta URL para que Edge Network pueda enrutar la solicitud a la región correcta. Si un usuario se conecta con una dirección IP diferente dentro de la duración de la cookie, la solicitud se vuelve a enrutar a la región más cercana. |
| **`kndctr_<orgId>_consent`** | 15552000 (180 días) | 10 a 11 bytes | Almacena las preferencias de consentimiento del visitante. Establezca siempre independientemente del consentimiento, ya que almacena las propias preferencias de consentimiento. |
| **`kndctr_<orgId>_consent_check`** | 7200 (2 horas) | | Asistente con ámbito de sesión que indica a Edge Network que vuelva a comprobar el consentimiento del lado del servidor después de que caduque el TTL. Aplica un TTL al consentimiento almacenado en caché. |
| **`kndctr_<orgId>_personalization`** | 34128000 (395 días) | | Almacena la información de sesión que utiliza Adobe Target para personalizar el contenido. |
| **`mbox`** | 63072000 (2 años) | | Presente cuando [`targetMigrationEnabled`](https://experienceleague.adobe.com/es/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) está habilitado. Permite que Web SDK establezca la [cookie de mbox](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) de Target. |
| **`mboxEdgeCluster`** | 1800 (30 minutos) | | Presente cuando [`targetMigrationEnabled`](https://experienceleague.adobe.com/es/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) está habilitado. Permite que Web SDK comunique el clúster perimetral correcto a `at.js` para que los perfiles de Target puedan permanecer sincronizados a medida que los usuarios navegan por un sitio. |
| **`s_ecid`** | 63115200 (2 años) | ~45 bytes | Contiene una copia del Experience Cloud ID (ECID/MID) con el formato `s_ecid=MCMID\|<ECID>`. Actúa como una copia de seguridad de origen de ECID, principalmente para escenarios CNAME (de origen). |

Edge Network establece todas las cookies con los atributos `secure` y `sameSite="none"`. Si actualmente tiene secciones seguras y no seguras en el sitio web, la identificación del usuario puede ser inexacta. Cuando un usuario navega de una sección segura del sitio a una sección no segura, Edge Network genera un nuevo(a) `ECID` con la solicitud.
