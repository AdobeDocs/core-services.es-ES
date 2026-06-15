---
description: Obtenga información acerca de las cookies de Adobe Advertising para asignar eventos de participación de anuncios a eventos de conversión y, posiblemente, utilice esa información para optimizar las ofertas de anuncios.
title: Cookies de Adobe Advertising
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
TQID: 'https://experienceleague.adobe.com/jr9RwaF63elDUN-XewIdrPNsGb6T5wo98vktP5U6jIM'
product_v2: id: e1971122-7081-4556-9222-8a31bd71800cid: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: dab36b01-8bfa-48f3-8392-626455a058e6id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: eb7e29b9-c5e9-4ed0-8e4b-6465dabb3cb1
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 25446910430bf15dcfa0fc70e25e0681f9faeb95
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 15%

---

# Cookies de Adobe Advertising

Adobe Advertising (anteriormente, Adobe Advertising Cloud) utiliza cookies para asignar eventos de participación de anuncios a eventos de conversión y, posiblemente, para utilizar esa información con el fin de optimizar las ofertas de publicidad.

>[!NOTE]
>
>La etiqueta beta Adobe Advertising Javascript que usa el servicio [Adobe CX Enterprise ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=es) crea cookies [CX Enterprise](experience-cloud.md) `s_ecid` de origen, no cookies de Adobe Advertising.

| Nombre de la cookie | Caducidad | Tamaño | Ubicación | Descripción |
| --- | --- | --- | --- | --- |
| **`_lcc`** | 15 minutos | 52 bytes | `everesttech.net` | Almacena ID y marcas de tiempo de clics en pantalla. Determina si un evento de clic en un anuncio en pantalla se aplica a una visita de Adobe Analytics. |
| **`_tmae`** | 1 año | 1 KB | `everesttech.net` | Almacena ID codificados y marcas de tiempo para participaciones publicitarias mediante el seguimiento de DSP. Incluye la participación del usuario en anuncios como los que se vieron por última vez |
| **`_tmid`** | 1 año | ~20 bytes | `everesttech.net` | Almacena el ID de Adobe Advertising Demand Side Platform (DSP). Corresponde al ID de visitante en la cookie `everest_g_v2`. |
| **`adcloud`** | 1 año | 50 a 150 bytes | Datos de origen | Las marcas de tiempo de la última visita del visitante a su sitio web y el último clic de búsqueda del visitante. También almacena el(la) `ef_id` que se creó cuando el visitante hizo clic en un anuncio. Vincula el ID de visitante con segmentos de audiencia y conversiones relevantes. Ayuda a optimizar los tiempos de carga de la página al evitar solicitudes innecesarias a Adobe. |
| **`ev_sync_*`** |  | 8 bytes | `everesttech.net` | La fecha en la que se realiza la sincronización en formato `yyymmdd`. Sincroniza el ID de visitante de Adobe Advertising con el intercambio de anuncios de socios. Se crea para nuevos visitantes y envía una solicitud de sincronización cuando caduca. Incluye las cookies `ev_sync_ax`, `ev_sync_bk`, `ev_sync_dd`, `ev_sync_fs`, `ev_sync_ix`, `ev_sync_nx`, `ev_sync_ox`, `ev_sync_pm`, `ev_sync_rc`, `ev_sync_tm` y `ev_sync_yh`. |
| **`everest_g_v2`** | 1 año | ~27 bytes | `everesttech.net` | Almacena el explorador y el ID de visitante. Se crea después de que un usuario haga clic en un anuncio. Se utiliza para asignar los clics actuales y posteriores con otros eventos del sitio web. |
| **`everest_session_v2`** | Session | ~16 bytes | `everesttech.net` | Almacena el ID de sesión actual. |
| **`id_adcloud`** | 91 días | 16 bytes | Datos de origen | Almacena el ID de visitante. |

{style="table-layout:auto"}

