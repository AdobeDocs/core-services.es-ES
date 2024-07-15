---
description: Obtenga información sobre las cookies de Adobe Analytics en Adobe Experience Cloud.
solution: Experience Cloud,Analytics,Target
title: Cookies de Adobe Analytics
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
source-git-commit: e7c4085f41c674826ddc097a01a24ff9ab6aae2c
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 16%

---

# Cookies de Adobe Analytics

Adobe Analytics utiliza cookies para diferenciar las solicitudes de distintos navegadores y almacenar información útil que una aplicación puede utilizar posteriormente. También se pueden utilizar para asociar la información de navegación con los registros de clientes.

Analytics utiliza cookies para definir nuevos visitantes de forma anónima, analizar los datos del flujo de navegación y realizar un seguimiento de la actividad histórica en el sitio web, como la respuesta a campañas concretas o la duración del ciclo de ventas.

| Nombre de la cookie | Vencimiento | Tamaño | Ubicación | Descripción |
| --- | --- | --- | --- | --- |
| **`s_ecid`** | 2 años | 45 bytes | Datos de origen | Almacena el ID del Experience Cloud (ECID) o MID. Establecido por respuesta HTTP. El MID se almacena en formato `s_ecid=MCMID`. Se establece después de que el cliente establezca la cookie AMCV. Permite el seguimiento continuado del ID de origen y se utiliza como ID de referencia si caduca la cookie de AMCV. Esta cookie no se aplica a las implementaciones de cookies de terceros. `SameSite` está establecido en &quot;Lax&quot;. |
| **`s_cc`** | Session | 4 bytes | Datos de origen | Determina si las cookies están habilitadas. La establece JavaScript. |
| **`s_sq`** | Session | 100 a 200 bytes | Datos de origen | Utilizado por el Activity Map. Contiene información sobre el vínculo anterior en el que el visitante hizo clic. La establece JavaScript. |
| **`s_vi`** | 2 años | 44 bytes | De origen o `*.omtrdc.net` (de terceros) | Almacena una ID de visitante y una marca de tiempo únicos. Establecido por respuesta HTTP. Cada ID de visitante está asociado con un perfil del visitante en los servidores de Adobe. Los perfiles de visitante se eliminan tras un año de inactividad, independientemente de la caducidad de cualquier cookie del ID del visitante. El indicador `Secure` se establece cuando `SameSite` es &quot;None&quot; y la conexión es HTTPS. `SameSite` es &quot;Lax&quot; de forma predeterminada para las cookies de origen. `SameSite` es &quot;Ninguno&quot; cuando se usan cookies de terceros, como en `omtrdc.net` o `2o7.net`. Establezca `SameSite` como &quot;Ninguno&quot; cuando utilice un solo CNAME para rastrear varios dominios o propiedades. |
| **`s_fid`** | 2 años | 33 bytes | Datos de origen | Almacena el ID único de visitante de reserva y la marca de tiempo. La establece JavaScript si no se puede establecer la cookie estándar `s_vi` debido a restricciones de cookies de terceros. No se utiliza en implementaciones de cookies de origen. |
| **`s_ac`** | Inmediato | 1 byte | Datos de origen | Ayuda a determinar el dominio correcto para establecer cookies de AppMeasurement. Contiene el valor estático `"1"`. Una vez configurada esta cookie, se elimina inmediatamente. |

{style="table-layout:auto"}

## Cookies establecidas por complementos

Algunas implementaciones utilizan complementos, que son fragmentos de código que proporcionan funcionalidad adicional para Analytics. Estos complementos pueden configurar cookies que no se han enumerado anteriormente. Consulte la [descripción general de los complementos de Analytics](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/plugins/impl-plugins) para obtener una lista de los complementos disponibles y las cookies que configuran.
