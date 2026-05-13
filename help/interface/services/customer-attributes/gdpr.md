---
title: '[!DNL Customer Attributes] Compatibilidad con el Reglamento General de Protección de Datos'
description: Obtenga información sobre la compatibilidad de Atributos del cliente con el Reglamento General de Protección de Datos
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 02417c0c-6780-4699-9470-f1685c3cd25d
TQID: https://experienceleague.adobe.com/wU6Y5XK5Fs9-w7Jl7THXjturzTVrsB7eh7GdExsS2TQ
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 407
ht-degree: 82%

---

# Cumplimiento del Reglamento general de protección de datos de [!DNL Customer Attributes]

Esta página describe cómo los [!DNL Customer Attributes] cumplen con el Reglamento general de protección de datos (RGPD).

>[!IMPORTANT]
>
>Este documento no contiene material de asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte a su asesor jurídico sobre el RGPD.

El [Reglamento General de Protección de Datos](https://business.adobe.com/es/privacy/general-data-protection-regulation.html), una ley vigente desde el 25 de mayo de 2018, otorga a todos los individuos (sujetos de datos) dentro de las fronteras de la Unión Europea (UE) el control de sus datos personales. También simplifica el entorno reglamentario de las empresas internacionales. Esta ley se aplica a todas las empresas (responsables de tratamiento de datos) que ofrecen bienes o servicios a personas que se encuentran dentro de los límites de la UE, monitorizan o recopilan datos personales de personas de la UE en el momento en que se procesan sus datos personales, independientemente de la ubicación comercial del responsable del tratamiento de datos.

Adobe CX Enterprise actúa como procesador de datos para cualquier dato personal que reciba y almacene en nombre de sus clientes. Como responsable del tratamiento de datos, determinará qué datos personales Adobe CX Enterprise trata y almacena en su nombre.

Este documento describe cómo los [!DNL Customer Attributes] admiten los derechos de acceso y eliminación de datos del RGPD de los sujetos de datos mediante la API de Adobe Experience Platform Privacy Service y la IU de Privacy Service.

Para obtener más información sobre el significado del RGPD para su empresa, consulte [RGPD y Su empresa](https://business.adobe.com/es/privacy/general-data-protection-regulation.html).

## Configuración necesaria para enviar solicitudes de [!DNL Customer Attributes]

Para realizar solicitudes de acceso y eliminación de datos para los [!DNL Customer Attributes], deberá hacer lo siguiente:

1. Identificar lo siguiente:

   * [ID de organización](../../administration/organizations.md)
   * ID de alias de la fuente de datos de CRS en la que desea actuar
   * ID de CRM del perfil en el que desea actuar

   Su [ID de organización](../../administration/organizations.md) es una cadena alfanumérica de 24 caracteres anexada a @AdobeOrg. Necesita el ID de organización para enviar solicitudes a la API de Privacidad. Póngase en contacto con el servicio de atención al cliente de Adobe en `gdprsupport@adobe.com` si no encuentra el ID.

1. En [!UICONTROL Privacy Service], puede enviar solicitudes de Acceso y Eliminación a [!DNL Customer Attributes] y comprobar el estado de las solicitudes existentes.

## Valores de campo requeridos en solicitudes JSON de [!DNL Customer Attributes]

&quot;contexto de compañía&quot;:

* &quot;espacio de nombres&quot;: **imsOrgID**
* &quot;valor&quot;: &lt;*su valor de ID de organización de IMS*>

&quot;usuarios&quot;:

* &quot;clave&quot;: &lt;*generalmente, el nombre del cliente*>
* &quot;acción&quot;: ya sea **acceso** (access) o **eliminación** (delete)
* &quot;ID de usuario&quot;:
   * &quot;espacio de nombres&quot;: &lt;*ID de alias de la fuente de datos CRS*>
   * &quot;tipo&quot;: **integrationCode**
   * &quot;valor&quot;: &lt;*ID de CRM*>
* &quot;incluir&quot;: **CRS** (que es el producto de Adobe que se aplica a la solicitud)
* &quot;regulación&quot;: **rgpd** (que es la norma de privacidad que se aplica a la solicitud)

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
