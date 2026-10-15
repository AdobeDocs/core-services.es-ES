---
title: Elija un dominio de recopilación de datos.
description: Obtenga información sobre los dominios que puede utilizar para enviar datos a Adobe y cómo encontrar el ID de inquilino de su organización.
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: e1185eeafc809b036b10955880536db7a576ca0b
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 3%
---
# Elija un dominio de recopilación de datos.

El dominio de recopilación de datos es el nombre de host al que la implementación envía datos. Todos los productos de Adobe CX Enterprise que utilizan la recopilación de datos de Adobe (como Adobe Analytics, Customer Journey Analytics, Adobe Experience Platform, Adobe Target y Adobe Journey Optimizer) dependen de este dominio.

## Opciones de dominio de recopilación de datos

| Opción | Dominio de implementación | [RDC](rdc.md) bloqueadas por región | Mantenimiento del certificado |
| --- | --- | --- | --- |
| [Dominio de terceros](#third-party) | `example.data.adobedc.net` | No compatible | Ninguno |
| Dominio de origen con [certificado administrado por Adobe](adobe-managed-cert.md) | `data.example.com` | Admitido | Ninguno (Adobe renueva el certificado automáticamente) |
| Dominio de origen con [certificado administrado por el cliente](customer-managed-cert.md) | `data.example.com` | Admitido | Su organización renueva el certificado y lo proporciona a Adobe |
| [Red de entrega de contenido (CDN) con un origen de terceros](cdn.md#third-party-origin) | `data.example.com` | No compatible | Ninguno |
| [CDN con origen propio](cdn.md#first-party-origin) | `data.example.com` | Admitido | Su organización renueva el certificado y lo proporciona a Adobe |

## Dominio de recopilación de datos de terceros {#third-party}

Si no usa un dominio de origen, envíe datos a un subdominio de `data.adobedc.net`. Adobe recomienda usar el [ID de inquilino](#tenant-id) de su organización como subdominio. Por ejemplo, `example.data.adobedc.net`. Este dominio también es el origen recomendado cuando [enruta la recopilación de datos a través de una CDN](cdn.md).

* Los dominios de terceros siempre usan el tipo predeterminado [RDC](rdc.md#third-party-data-collection).
* No utilice subdominios más profundos que `example.data.adobedc.net`. Por ejemplo, `custom.example.data.adobedc.net` no es un dominio de recopilación de datos válido.
* Las implementaciones más antiguas pueden utilizar dominios como `sc.omtrdc.net` o `2o7.net`. Aunque estos dominios siguen siendo válidos, Adobe recomienda usar `data.adobedc.net` siempre que sea posible.

### Buscar el ID de inquilino {#tenant-id}

1. Inicie sesión en [Adobe CX Enterprise](https://experience.adobe.com) con sus credenciales de Adobe ID.
1. En cualquier lugar de la interfaz de CX Enterprise, presione `[Cmd]` + `[I]` (macOS) o `[Ctrl]` + `[I]` (Windows).
1. Aparece un **[!UICONTROL depurador de datos de usuario]**. Seleccione la ficha **[!UICONTROL Organizaciones asignadas]**.
1. Expanda la organización IMS deseada.
1. Busque el campo **[!UICONTROL Inquilino]**. Este valor es su ID de inquilino.

Su ID de inquilino es diferente del ID de organización de IMS, que termina en `@AdobeOrg`. Cada organización de IMS tiene un ID de inquilino. Si su empresa utiliza varias organizaciones IMS, cada organización tiene su propio ID de inquilino.

## Actualice la implementación {#update-implementation}

Cuando cambie el dominio de recopilación de datos, actualice todas las implementaciones que envíen datos a Adobe:

* **Extensión de etiquetas Web SDK**: actualice el campo [[!UICONTROL Dominio de Edge]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/general) al configurar la extensión.
* **Web SDK (aleación)**: actualice la propiedad [`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/edgedomain) dentro del comando `configure`.
* **Extensión de Adobe Analytics**: Actualice el campo [[!UICONTROL Servidor de seguimiento SSL]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/analytics/overview) al configurar la extensión. Asegúrese de tener también instalada la extensión de etiqueta [Servicio de ID de visitante](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/id-service/overview). Consulte [Identificación de visitante con la extensión de etiquetas de Analytics](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/analytics-extension) para obtener más información.
* **AppMeasurement**: Actualice la variable de configuración [`trackingServerSecure`](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/config-vars/trackingserversecure). Asegúrese de que también ha implementado el [Servicio de identificación del visitante](https://experienceleague.adobe.com/es/docs/id-service/using/home) mediante `VisitorAPI.js`. Consulte [Identificación de visitante con AppMeasurement](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/appmeasurement) para obtener más información.
* **Otras implementaciones**: actualice el dominio de recopilación de datos en cualquier otra implementación que envíe datos a Adobe, como aplicaciones móviles o implementaciones del lado del servidor.

Si su implementación no utiliza el servicio de ID de visitante ni el SDK web, al cambiar el dominio de recopilación de datos se cambia el dominio de las cookies de los visitantes, y los visitantes que regresan se pueden contabilizar como nuevos visitantes.

Si su sitio utiliza varios métodos de implementación y no puede actualizarlos todos simultáneamente, considere la posibilidad de configurar un periodo de gracia. Consulte [Consideraciones sobre la migración del servicio de ID de visitante](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/migration) para ver pasos adicionales sobre cómo evitar que los visitantes se contabilicen como nuevos visitantes en el sitio.
