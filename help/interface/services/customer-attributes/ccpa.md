---
title: '[!DNL Customer Attributes] Cumplimiento de la Ley de Privacidad del Consumidor de California'
description: Más información sobre [!DNL Customer Attributes] compatibilidad con la Ley de privacidad del consumidor de California
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
TQID: https://experienceleague.adobe.com/YPl1rlZRciwN6GM7mtkqMKjPsW-H1ueMG4zqbH8auho
product_v2: id: e1971122-7081-4556-9222-8a31bd71800c
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 402
ht-degree: 52%

---

# Compatibilidad de [!DNL Customer Attributes] con la Ley de Privacidad del Consumidor de California

Esta página describe la compatibilidad de [!DNL Customer Attributes] con la Ley de Privacidad del Consumidor de California (CCPA).

>[!IMPORTANT]
>
>El contenido de este documento no constituye asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte con su asesor jurídico para obtener asesoramiento sobre la CCPA.

La CCPA es la nueva ley de privacidad de California que entró en vigor el 1 de enero de 2020. La CCPA otorga a los residentes de California nuevos derechos con respecto a su información personal e impone responsabilidades de protección de datos a ciertas entidades que hacen negocios en California. La CCPA otorga a los consumidores el derecho de acceder a sus datos personales y suprimirlos, así como el derecho de exclusión de determinadas actividades que pueden considerarse &quot;vendedoras&quot; de información personal a terceros.

Como empresa, determina los datos personales que Adobe CX Enterprise procesa y almacena en su nombre.

Como proveedor de servicios, Adobe CX Enterprise proporciona asistencia a su empresa para que cumpla con las obligaciones que le impone CCPA y que son aplicables al uso de los productos y servicios de CX Enterprise. Esta compatibilidad incluye la administración de solicitudes de acceso y la eliminación de información personal.

Este documento describe cómo [!DNL Customer Attributes] admite los derechos de acceso y eliminación de datos de la CCPA de los sujetos de datos mediante la API de Adobe Experience Platform Privacy Service y la IU de Privacy Service.

Para obtener más información sobre los servicios de privacidad de Adobe para la CCPA, consulte el [Centro de privacidad de Adobe](https://www.adobe.com/privacy/ccpa.html).

## Configuración necesaria para enviar solicitudes de [!DNL Customer Attributes]

Para realizar solicitudes de acceso y eliminación de datos para los [!DNL Customer Attributes], deberá hacer lo siguiente:

1. Identificar lo siguiente:

   * [ID de organización](../../administration/organizations.md)
   * ID de alias de la fuente de datos de CRS en la que desea actuar
   * ID de CRM del perfil en el que desea actuar

   Su ID de organización es una cadena alfanumérica de 24 caracteres anexada a @AdobeOrg. Necesita el ID de organización para enviar solicitudes a la API de Privacidad. Póngase en contacto con el servicio de atención al cliente de Adobe en `gdprsupport@adobe.com` si no encuentra el ID.

1. En [!UICONTROL Privacy Service], puede enviar solicitudes de acceso y eliminación a los Atributos del cliente y comprobar el estado de las solicitudes existentes.

## Valores de campo requeridos en [!DNL Customer Attributes] solicitudes JSON

&quot;contexto de compañía&quot;:

* &quot;espacio de nombres&quot;: **imsOrgID**
* &quot;valor&quot;: &lt;*su valor de ID de organización*>

&quot;usuarios&quot;:

* &quot;clave&quot;: &lt;*generalmente, el nombre del cliente*>
* &quot;acción&quot;: ya sea **acceso** (access) o **eliminación** (delete)
* &quot;ID de usuario&quot;:
   * &quot;espacio de nombres&quot;: &lt;*ID de alias de la fuente de datos CRS*>
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
