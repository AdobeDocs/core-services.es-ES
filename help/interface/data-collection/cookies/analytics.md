---
description: Obtenga información sobre las cookies de Adobe Analytics en Adobe Experience Cloud.
solution: Analytics
title: Cookies de Adobe Analytics
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
TQID: https://experienceleague.adobe.com/H-N88ygcQUcUIej1Kkwlv9UmIe1qPDYwo-qF3TdDqHg
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d253888322194189fea6d492ae19cf248357960
workflow-type: tm+mt
source-wordcount: 545
ht-degree: 11%

---

# Cookies de Adobe Analytics

Adobe Analytics utiliza cookies para diferenciar las solicitudes de distintos navegadores y almacenar información útil que una aplicación puede utilizar posteriormente. También se pueden utilizar para asociar la información de navegación con los registros de clientes.

Analytics utiliza cookies para definir nuevos visitantes de forma anónima, analizar los datos del flujo de navegación y realizar un seguimiento de la actividad histórica en el sitio web, como la respuesta a campañas concretas o la duración del ciclo de ventas.

| Nombre de la cookie | Caducidad | Tamaño | Ubicación | Descripción |
| --- | --- | --- | --- | --- |
| **`s_ecid`** | 13 meses | 45 bytes | Datos de origen | Almacena el Experience Cloud ID (ECID) o MID. Establecido por respuesta HTTP. El MID se almacena en formato `s_ecid=MCMID`. Se establece después de que el cliente establezca la cookie AMCV. Permite el seguimiento continuado del ID de origen y se utiliza como ID de referencia si caduca la cookie de AMCV. `SameSite` está establecido en &quot;Lax&quot;. Si utiliza Web SDK para implementar Adobe Analytics, la caducidad de la cookie se establece en dos años; sin embargo, la mayoría de los exploradores modernos truncan la caducidad a trece meses. |
| **`s_cc`** | Session | 4 bytes | Datos de origen | Determina si las cookies están habilitadas. La establece JavaScript. |
| **`s_sq`** | Session | 100 a 200 bytes | Datos de origen | Utilizado por Activity Map. Contiene información sobre el vínculo anterior en el que el visitante hizo clic. La establece JavaScript. |
| **`s_vi`** | 2 años | 44 bytes | De origen o `*.omtrdc.net` (de terceros) | Almacena una ID de visitante y una marca de tiempo únicos. Establecido por respuesta HTTP. Cada ID de visitante está asociado con un perfil del visitante en los servidores de Adobe. Los perfiles de visitante se eliminan tras un año de inactividad, independientemente de la caducidad de cualquier cookie del ID del visitante. El indicador `Secure` se establece cuando `SameSite` es &quot;None&quot; y la conexión es HTTPS. `SameSite` es &quot;Lax&quot; de forma predeterminada para las cookies de origen. `SameSite` es &quot;Ninguno&quot; cuando se usan cookies de terceros, como en `omtrdc.net` o `2o7.net`. Establezca `SameSite` como &quot;Ninguno&quot; cuando utilice un solo CNAME para rastrear varios dominios o propiedades. |
| **`s_fid`** | 2 años | 33 bytes | Datos de origen | Almacena el ID único de visitante de reserva y la marca de tiempo. La establece JavaScript si no se puede establecer la cookie estándar `s_vi` debido a restricciones de cookies de terceros. No se utiliza en implementaciones de cookies de origen. |
| **`s_ac`** | Inmediato | 1 byte | Datos de origen | Ayuda a determinar el dominio correcto para establecer las cookies de AppMeasurement. Contiene el valor estático `"1"`. Una vez configurada esta cookie, se elimina inmediatamente. |

Consulte [Identificación de visitantes en Adobe Analytics](https://experienceleague.adobe.com/es/docs/analytics/implementation/id/overview) para obtener más información sobre cómo Adobe Analytics identifica a los visitantes que utilizan cookies.

## Cookies establecidas por complementos

Algunas implementaciones utilizan complementos, que son fragmentos de código que proporcionan funcionalidad adicional para Analytics. Estos complementos pueden configurar cookies que no se han enumerado anteriormente. Consulte la [descripción general de los complementos de Analytics](https://experienceleague.adobe.com/es/docs/analytics/implementation/vars/plugins/impl-plugins) para obtener una lista de los complementos disponibles y las cookies que configuran.

## Consecuencias de la eliminación de cookies de Analytics

Si un visitante elimina sus cookies de Analytics, tenga en cuenta lo siguiente:

* **Se ha perdido la identificación del visitante:** Cuando se eliminan las cookies, Adobe Analytics no puede reconocer a los visitantes que regresan. La próxima vez que el usuario visite el sitio, se contará como un visitante nuevo.
* **Se ha interrumpido la continuidad de la sesión:** Cualquier análisis basado en sesión o de varias visitas (como el seguimiento de atribución o conversión) se interrumpe. El mismo usuario no puede vincular los eventos y las conversiones que se produzcan tras la eliminación de una cookie a actividades anteriores.
* **Personalization y la segmentación se ven afectados:** Los segmentos o experiencias personalizadas basadas en el historial o el comportamiento del visitante se restablecen, ya que los datos anteriores ya no están asociados con su visita actual.
* **Se ha interrumpido el seguimiento entre dominios:** Para las cookies de terceros, eliminarlas impide que Adobe Analytics vincule la actividad del usuario entre varios de sus dominios.

