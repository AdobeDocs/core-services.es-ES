---
title: Cookies de Adobe Experience Platform Web SDK
description: Descubra cómo Web SDK utiliza cookies aplicables a su implementación.
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
TQID: 'https://experienceleague.adobe.com/jysQ5m7o0cI3ECKz2RWZB4Kt3own7XAPm04pr4yLh-k'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
    internal-label: Getting started
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 7b12d5debfccd62ab7b416e9a6fe278d251a4ca5
workflow-type: tm+mt
source-wordcount: '984'
ht-degree: 0%
---
# Cookies de Adobe Experience Platform Web SDK

Adobe Experience Platform Web SDK utiliza cookies para almacenar valores específicos de la implementación.

| Nombre | Edad máxima | Tamaño | Descripción |
| --- | --- | --- | --- |
| **`AMCV_###@AdobeOrg`** | 33696000 (390 días) cuando lo escribe Web SDK | 44 bytes cuando se escribe en Web SDK (`MCMID\|<ECID>`); mayor cuando se escribe en `VisitorAPI.js` | Presente cuando [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled) está habilitado, que es el valor predeterminado. Ayuda al realizar la transición a Web SDK mientras algunas partes del sitio siguen utilizando `VisitorAPI.js`. Web SDK lee esta cookie para reutilizar un ECID existente. Una vez que Edge Network devuelve un ECID, Web SDK lo escribe en esta cookie si falta la cookie o si contiene un ECID diferente. |
| **`com.adobe.alloy.getTld`** | Ninguno (cookie de sesión, eliminada inmediatamente) | 22 bytes | Cookie de ayuda temporal utilizada internamente por Web SDK para determinar el dominio de nivel superior del sitio actual. Web SDK escribe y elimina esta cookie cuando se carga la biblioteca, antes de que se ejecute el comando `configure` y antes de que se evalúe el consentimiento, de modo que los analizadores de cookies pueden informar de ella tal como se ha establecido antes del consentimiento. La cookie contiene únicamente su propio nombre y no almacena datos de comportamiento o de perfil. |
| **`demdex`** | 15552000 (180 días) | varía | Cookie de terceros en el dominio `demdex.net`. Presente cuando [`thirdPartyCookiesEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/thirdpartycookiesenabled) está habilitado (el valor predeterminado) y el explorador permite las cookies de terceros de forma predeterminada, como Chrome o Edge. En ese caso, Web SDK envía solicitudes de identidad a `adobedc.demdex.net`, que establece esta cookie. Audience Manager utiliza esta cookie para asignar un ID único y admitir la sincronización, segmentación, modelado e informes de ID. Ver `demdex` en [cookies de Audience Manager](audience-manager.md). |
| **`kndctr_<orgId>_identity`** | 34128000 (395 días) | 100 a 120 bytes (variable) | Almacena el ECID y otra información relacionada para ese dispositivo. |
| **`kndctr_<orgId>_cluster`** | 1800 (30 minutos) | 3 a 5 bytes | Almacena la región de Edge Network (ubicación) que sirve las solicitudes del usuario actual. La región se utiliza en la ruta URL para que Edge Network pueda enrutar la solicitud a la región correcta. Si un usuario se conecta con una dirección IP diferente dentro de la duración de la cookie, la solicitud se vuelve a enrutar a la región más cercana. |
| **`kndctr_<orgId>_consent`** | 15552000 (180 días) | 10 a 11 bytes | Almacena las preferencias de consentimiento del visitante. Establezca siempre independientemente del consentimiento, ya que almacena las propias preferencias de consentimiento. |
| **`kndctr_<orgId>_consent_check`** | 7200 (2 horas) | | Asistente con ámbito de sesión que indica a Edge Network que vuelva a comprobar el consentimiento del lado del servidor después de que caduque el TTL. Aplica un TTL al consentimiento almacenado en caché. |
| **`kndctr_<orgId>_personalization`** | 34128000 (395 días) | | Almacena la información de sesión que utiliza Adobe Target para personalizar el contenido. |
| **`kndctr_<orgId>_advertising`** | 31622400 (366 días), renovado cada vez que se actualiza la cookie | De 80 bytes a 1 KB (variable) | Presente cuando el componente Adobe Advertising (beta) se incluye en la compilación de Web SDK y el consentimiento del visitante es `in`. Web SDK escribe esta cookie cuando la dirección URL de la página contiene parámetros de clic de Adobe Advertising (`s_kwcid` o `ef_id`) o cuando los anunciantes de [Adobe Advertising DSP](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising) están configurados. Almacena JSON con codificación URL que puede incluir datos de clics de búsqueda (`_les_lsc`), una dirección IP con hash, un sobre RampID de LiveRamp (cuando se configura una ruta de JavaScript RampID) y marcas de tiempo de conversión utilizadas para acelerar conversiones duplicadas. En los exploradores que permiten cookies de terceros de forma predeterminada, también se almacena el identificador de internauta de Adobe Advertising y se muestran los datos de clics (`ev_lcc`). Esta cookie solo se establece en el nombre de host actual. El componente también carga recursos de `pixel.everesttech.net`, `www.everestjs.net` (cuando se configura un identificador de socio ID5) y su ruta RampID `ats.js`. Estos recursos pueden configurar sus propias cookies, que no aparecen en esta página. |
| **`kndctr_<orgId>_bc_session_id`** | Ninguno (cookie de sesión) | | Presente cuando se utiliza el componente Brand Concierge (beta). Almacena el ID de sesión de chat de Brand Concierge. Web SDK solo lee esta cookie cuando [`stickyConversationSession`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/conversation) está habilitado, de modo que las sesiones de chat persisten al cargar la página. |
| **`mbox`** | 63072000 (2 años) | | Presente cuando [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) está habilitado. Permite que Web SDK establezca la [cookie de mbox](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) de Target. |
| **`mboxEdgeCluster`** | 1800 (30 minutos) | | Presente cuando [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled) está habilitado. Permite que Web SDK comunique el clúster perimetral correcto a `at.js` para que los perfiles de Target puedan permanecer sincronizados a medida que los usuarios navegan por un sitio. Cuando la cookie `kndctr_<orgId>_cluster` no está presente, Web SDK también lee esta cookie para enrutar solicitudes a la región de Edge Network correspondiente. |
| **`s_ecid`** | 63115200 (2 años) | ~45 bytes | Contiene una copia del CX Enterprise ID (ECID/MID) con el formato `s_ecid=MCMID\|<ECID>`. Actúa como una copia de seguridad de origen de ECID, principalmente para escenarios CNAME (de origen). Cuando [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled) está habilitado, Web SDK lee esta cookie para reutilizar un ECID existente. |
| **Destinos de cookies de Audience Manager** (el nombre varía) | 864000 (10 días), a menos que el destino especifique una duración diferente | varía | Presente cuando Edge Network devuelve un Audience Manager [destino de la cookie](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/destinations/custom-destinations/create-cookie-destination) para el visitante. Web SDK escribe una cookie de origen utilizando el nombre, el valor y el dominio de la cookie definidos en el destino. Los valores tienen codificación URL, coherente con Audience Manager Data Integration Library (DIL). |

Edge Network establece todas sus cookies con los atributos `secure` y `sameSite="none"`. Si actualmente tiene secciones seguras y no seguras en el sitio web, la identificación del usuario puede ser inexacta. Cuando un usuario navega de una sección segura del sitio a una sección no segura, Edge Network genera un nuevo(a) `ECID` con la solicitud.

Las cookies que crea Web SDK por su cuenta, en lugar de hacerlo bajo la dirección de Edge Network, utilizan atributos diferentes. La cookie `AMCV_###@AdobeOrg` y los destinos de cookies de Audience Manager incluyen los atributos `secure` y `sameSite="none"` solo en páginas HTTPS. Las cookies `com.adobe.alloy.getTld` y `kndctr_<orgId>_advertising` utilizan los atributos predeterminados del explorador.
