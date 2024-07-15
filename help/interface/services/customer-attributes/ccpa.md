---
title: Cumplimiento de atributos del cliente con la Ley de Privacidad del Consumidor de California
description: Conozca el cumplimiento de atributos del cliente con la Ley de privacidad del consumidor de California.
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 82%

---

# Cumplimiento de atributos del cliente con la Ley de Privacidad del Consumidor de California

Esta página describe la compatibilidad de [!UICONTROL Atributos del cliente] con la Ley de Privacidad del Consumidor de California (CCPA).

>[!IMPORTANT]
>
>El contenido de este documento no constituye asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte con su asesor jurídico para obtener asesoramiento sobre la CCPA.

La CCPA es la nueva ley de privacidad de California que entró en vigor el 1 de enero de 2020. La CCPA otorga a los residentes de California nuevos derechos con respecto a su información personal e impone responsabilidades de protección de datos a ciertas entidades que hacen negocios en California. La CCPA otorga a los consumidores el derecho de acceder a sus datos personales y suprimirlos, así como el derecho de exclusión de determinadas actividades que pueden considerarse &quot;vendedoras&quot; de información personal a terceros.

Como empresa, determina los datos personales que Adobe Experience Cloud procesa y almacena en su nombre.

Como proveedor de servicio, Adobe Experience Cloud proporciona asistencia a su empresa para que cumpla con las obligaciones que le impone CCPA y que son aplicables al uso de los productos y servicios de Experience Cloud. Esta compatibilidad incluye la administración de solicitudes de acceso y la eliminación de información personal.

Este documento describe cómo los [!UICONTROL Atributos del cliente] admiten los derechos de acceso y eliminación de datos de la CCPA de los sujetos de datos mediante la API de Adobe Experience Platform Privacy Service y la IU de Privacy Service.

Para obtener más información sobre los servicios de privacidad de Adobe para la CCPA, consulte el [Centro de privacidad de Adobe](https://www.adobe.com/privacy/ccpa.html).

## Configuración necesaria para enviar solicitudes de [!UICONTROL Atributos del cliente]

Para realizar solicitudes de acceso y eliminación de datos para los [!UICONTROL Atributos del cliente], deberá:

1. Identificar lo siguiente:

   * [ID de organización](../../administration/organizations.md)
   * ID de alias de la fuente de datos de CRS en la que desea actuar
   * ID de CRM del perfil en el que desea actuar

   Su ID de organización es una cadena alfanumérica de 24 caracteres anexada a @AdobeOrg. Necesita el ID de organización para enviar solicitudes a la API de Privacidad. Póngase en contacto con el servicio de atención al cliente de Adobe en `gdprsupport@adobe.com` si no encuentra el ID.

1. En [!UICONTROL Privacy Service], puede enviar solicitudes de acceso y eliminación a los Atributos del cliente y comprobar el estado de las solicitudes existentes.

## Valores de campo requeridos en solicitudes JSON de [!UICONTROL Atributos del cliente]

&quot;contexto de compañía&quot;:

* &quot;área de nombres&quot;: **imsOrgID**
* &quot;valor&quot;: &lt;*su valor de ID de organización*>

&quot;usuarios&quot;:

* &quot;clave&quot;: &lt;*generalmente, el nombre del cliente*>
* &quot;acción&quot;: ya sea **acceso** (access) o **eliminación** (delete)
* &quot;ID de usuario&quot;:
   * &quot;área de nombres&quot;: &lt;*ID de alias de la fuente de datos CRS*>
   * &quot;tipo&quot;: **integrationCode**
   * &quot;valor&quot;: &lt;*ID de CRM*>
* &quot;incluir&quot;: **CRS** (que es el producto de Adobe que se aplica a la solicitud)
* &quot;regulación&quot;: **ccpa** (que es la norma de privacidad que se aplica a la solicitud)

## Ejemplo de solicitud JSON

```json
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "<IMS_ORG_ID>"
    }
  ],
  "users": [
    {
      "key": "<KEY>",
      "action": [
        "<access/delete>"
      ],
      "userIDs": [
        {
          "namespace": "<Alias ID of CRS Data Source>",
          "type": "integrationCode",
          "value": "<CRM ID>"
        }
      ]
    }
  ],
  "regulation": "<gdpr/ccpa/pdpa>",
  "include": [
    "CRS"
  ]
}
```

## Campos de datos arrojados para las solicitudes de acceso

```json
attributes:
{
"value": "<*value*>",
"key": "<*key*>",
"displayName": "<*displayName*>"
}
```
