---
title: 'Cumplimiento de atributos del cliente con la Ley de Privacidad del Consumidor de California '
description: Conozca el cumplimiento de atributos del cliente con la Ley de privacidad del consumidor de California.
feature: 'Atributos del cliente '
topic: Administración
role: Administrator
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: b968ca3a2751ab9af27e86595447f84f3cb20d68
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 66%

---

# Cumplimiento de atributos del cliente con la Ley de Privacidad del Consumidor de California

Esta página describe la compatibilidad de los [!UICONTROL Atributos del cliente] con la Ley de Privacidad del Consumidor de California (CCPA, por sus siglas en inglés).

>[!IMPORTANT]
>
>El contenido de este documento no constituye asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte con su asesor jurídico para obtener asesoramiento sobre la CCPA.

La CCPA es la nueva ley de privacidad de California que entró en vigor el 1 de enero de 2020. La CCPA otorga a los residentes de California nuevos derechos con respecto a su información personal e impone responsabilidades de protección de datos a ciertas entidades que hacen negocios en California. La CCPA otorga a los consumidores el derecho de acceder a su información personal y eliminarla, así como el derecho de exclusión de determinadas actividades que pueden considerarse &quot;vendedoras&quot; de información personal a terceros.

Como empresa, usted determina los datos personales que Adobe Experience Cloud procesa y almacena en su nombre.

Como proveedor de servicios, Adobe Experience Cloud proporciona asistencia a su empresa para que cumpla con las obligaciones que le impone la CCPA y que son aplicables al uso de productos y servicios de Experience Cloud. Esta compatibilidad incluye la administración de solicitudes de acceso y eliminación de información personal.

Este documento describe cómo [!UICONTROL Cliente                   derechos de acceso y eliminación de datos de la CCPA de sus interesados mediante la API de Adobe Experience Platform Privacy Service y la IU del Privacy Service.

Para obtener más información sobre los servicios de privacidad de Adobe para la CCPA, consulte el [Centro de privacidad de Adobe](https://www.adobe.com/privacy/ccpa.html).

## Configuración necesaria para enviar solicitudes de [!UICONTROL Atributos del cliente]

Para realizar solicitudes de acceso y eliminación de datos para [!UICONTROL Atributos del cliente], debe:

1. Identificar lo siguiente:

   * ID de organización IMS
   * ID de alias de la fuente de datos de CRS en la que desea actuar
   * ID de CRM del perfil en el que desea actuar

   Un ID de organización de IMS es una cadena alfanumérica de 24 caracteres anexada a @AdobeOrg. Si el equipo de marketing o el administrador interno del sistema de Adobe no conocen el ID de organización de IMS de su organización, póngase en contacto con el servicio de atención al cliente de Adobe a la dirección gdprsupport@adobe.com. Necesitará el ID de organización de IMS para enviar solicitudes a la API de privacidad.

1. En [!UICONTROL Privacy Service], puede enviar solicitudes de acceso y eliminación a los Atributos del cliente y comprobar el estado de las solicitudes existentes.

## Valores de campo requeridos en solicitudes JSON de [!UICONTROL Atributos del cliente]

&quot;contexto de compañía&quot;:

* &quot;área de nombres&quot;: **imsOrgID**
* &quot;valor&quot;: &lt;*su valor de ID de organización de IMS*>

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

```
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

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
