---
description: Obtenga información acerca de las cookies de Adobe Advertising para asignar eventos de participación de anuncios a eventos de conversión y, posiblemente, utilice esa información para optimizar las ofertas de anuncios.
title: Cookies de Adobe Advertising
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
source-git-commit: 4d2dc1e6126e26f61475efbd33efe98bd47153d5
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 13%

---

# Cookies de Adobe Advertising

Adobe Advertising (anteriormente Adobe Advertising Cloud) usa cookies para asignar eventos de participación de anuncios a eventos de conversión y, posiblemente, para utilizar esa información con el fin de optimizar las ofertas de anuncios.

>[!NOTE]
>
>La Adobe Advertising beta JavaScript que usa el servicio [Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=es) crea cookies de origen [Experience Cloud](experience-cloud.md) `s_ecid`, no cookies de Adobe Advertising.

| Nombre de la cookie | Vencimiento | Tamaño | Ubicación | Descripción |
| --- | --- | --- | --- | --- |
| **`_lcc`** | 15 minutos | 52 bytes | `everesttech.net` | Almacena ID y marcas de tiempo de clics en pantalla. Determina si un evento de clic en un anuncio en pantalla se aplica a una visita de Adobe Analytics. |
| **`_tmae`** | 1 año | 1 KB | `everesttech.net` | DSP Almacena ID codificados y marcas de tiempo para participaciones publicitarias mediante el seguimiento de la. Incluye la participación del usuario en anuncios como los que se vieron por última vez |
| **`_tmid`** | 1 año | ~20 bytes | `everesttech.net` | Almacena el ID del Demand Side Platform DSP de Adobe Advertising (). Corresponde al ID de visitante en la cookie `everest_g_v2`. |
| **`adcloud`** | 1 año | 50 a 150 bytes | Datos de origen | Las marcas de tiempo de la última visita del visitante a su sitio web y el último clic de búsqueda del visitante. También almacena el(la) `ef_id` que se creó cuando el visitante hizo clic en un anuncio. Vincula el ID de visitante con segmentos de audiencia y conversiones relevantes. Ayuda a optimizar los tiempos de carga de la página al evitar solicitudes innecesarias al Adobe. |
| **`ev_sync_*`** |  | 8 bytes | `everesttech.net` | La fecha en la que se realiza la sincronización en formato `yyymmdd`. Sincroniza el ID de visitante de Adobe Advertising con el intercambio de anuncios de socios. Se crea para nuevos visitantes y envía una solicitud de sincronización cuando caduca. Incluye las cookies `ev_sync_ax`, `ev_sync_bk`, `ev_sync_dd`, `ev_sync_fs`, `ev_sync_ix`, `ev_sync_nx`, `ev_sync_ox`, `ev_sync_pm`, `ev_sync_rc`, `ev_sync_tm` y `ev_sync_yh`. |
| **`everest_g_v2`** | 1 año | ~27 bytes | `everesttech.net` | Almacena el explorador y el ID de visitante. Se crea después de que un usuario haga clic en un anuncio. Se utiliza para asignar los clics actuales y posteriores con otros eventos del sitio web. |
| **`everest_session_v2`** | Session | ~16 bytes | `everesttech.net` | Almacena el ID de sesión actual. |
| **`id_adcloud`** | 91 días | 16 bytes | Datos de origen | Almacena el ID de visitante. |

{style="table-layout:auto"}
