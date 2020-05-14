---
title: Customer Attributes Support for California Consumer Privacy Act (Compatibilidad con atributos del cliente)
description: Customer Attributes Support for California Consumer Privacy Act (Compatibilidad con atributos del cliente)
translation-type: tm+mt
source-git-commit: 4223f9260865756842ad43b99d2509908f4d6572
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 4%

---


# Compatibilidad de Atributos del cliente con la Ley de privacidad del consumidor de California

Esta página describe la compatibilidad de Atributos [!UICONTROL del cliente con la Ley de privacidad del consumidor de California (CCPA, por sus siglas en inglés)] .

>[!IMPORTANT]
>
>El contenido de este documento no constituye asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte con su asesor jurídico para obtener asesoramiento sobre el (CCPA).

La CCPA es la nueva ley de privacidad de California, que entrará en vigor el 1 de enero de 2020. CCPA proporciona a los residentes de California nuevos derechos con respecto a su información personal e impone responsabilidades de protección de datos a ciertas entidades que realizan negocios en California. La CCPA otorga a los consumidores el derecho de acceder a sus datos personales y de suprimirlos, así como el derecho de exclusión determinadas actividades que pueden considerarse &quot;vendedoras&quot; de información personal a terceros.

Como empresa, determinará los datos personales que Adobe Experience Cloud procesa y almacena en su nombre.

Como proveedor de servicio, Adobe Experience Cloud proporciona asistencia a su empresa para que cumpla con las obligaciones que le impone CCPA y que son aplicables al uso de los productos y servicios de Experience Cloud, incluida la gestión de solicitudes de acceso y eliminación de información personal.

Este documento describe cómo los atributos [!UICONTROL del] cliente admiten los derechos de acceso y eliminación de datos CCPA de los sujetos de datos mediante la API de servicio de privacidad de Adobe Experience Platform y la interfaz de usuario de Privacy Service.

Para obtener más información sobre los servicios de privacidad de Adobe para CCPA, consulte [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Configuración necesaria para enviar solicitudes de atributos [!UICONTROL del cliente]

Para realizar solicitudes de acceso y eliminación de datos para Atributos [!UICONTROL de]cliente, deberá:

1. Identifique lo siguiente:

   * ID de organización IMS
   * ID de alias de la fuente de datos de CRS en la que desea actuar
   * ID de CRM del perfil en el que desea actuar
   Un ID de organización de IMS es una cadena alfanumérica de 24 caracteres anexada a @AdobeOrg. Si el equipo de marketing o el administrador interno del sistema de Adobe no conocen el ID de organización de IMS de su organización, póngase en contacto con el servicio de atención al cliente de Adobe en gdprsupport@adobe.com. Necesitará el ID de organización de IMS para enviar solicitudes a la API de privacidad.

1. En [!UICONTROL Privacy Service], puede enviar solicitudes de acceso y eliminación a Atributos del cliente y comprobar el estado de las solicitudes existentes.

## Valores de campo requeridos en solicitudes JSON de atributos  del cliente

&quot;Contexto de compañía&quot;:

* &quot;Área de nombres&quot;: **imsOrgID**
* &quot;value&quot;: &lt;*su valor* de ID de organización de IMS>

&quot;usuarios&quot;:

* &quot;key&quot;: &lt;*generalmente el nombre del cliente*>

* &quot;action&quot;: ya sea **acceso** o **eliminación**

* &quot;ID de usuario&quot;:

   * &quot;Área de nombres&quot;: &lt;ID *de alias de la fuente* de datos CRS>

   * &quot;type&quot;: **integrationCode**

   * &quot;value&quot;: &lt;ID *de CRM*>

* &quot;include&quot;: **CRS** (que es el producto de Adobe que se aplica a la solicitud)

* &quot;regulación&quot;: **ccpa** (que es la regulación de privacidad que se aplica a la solicitud)

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

## Campos de datos devueltos para solicitudes de acceso

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
