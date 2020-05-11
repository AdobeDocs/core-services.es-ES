---
title: Compatibilidad de atributos del cliente con el Reglamento general de protección de datos
description: Compatibilidad de atributos del cliente con el Reglamento general de protección de datos
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 1%

---


# Compatibilidad de atributos del cliente con el Reglamento general de protección de datos

Esta página describe cómo los atributos del cliente admiten el Reglamento General de Protección de Datos (RGPD).

>[!IMPORTANT]
>
>El contenido del presente documento no es asesoramiento jurídico ni tiene por objeto sustituir al asesoramiento jurídico. Consulte con su asesor jurídico sobre el RGPD.

El Reglamento [](https://www.adobe.com/privacy/general-data-protection-regulation/what-is-gdpr.html)General de Protección de Datos, una ley vigente el 25 de mayo de 2018, otorga a todos los individuos (sujetos de datos) dentro de las fronteras de la Unión Europea (UE) el control de sus datos personales. También simplifica el entorno reglamentario de las empresas internacionales. Esta ley se aplica a todas las empresas (responsables de tratamiento de datos) que oferta bienes o servicios a personas que se encuentren dentro de los límites de la UE, supervisen o recopilen datos personales de personas que se encuentren dentro de los límites de la UE en el momento en que se procesen sus datos personales, independientemente de la ubicación comercial del responsable del tratamiento de datos.

Adobe Experience Cloud actúa como procesador de datos para cualquier dato personal que reciba y almacene en nombre de sus clientes. Como controlador de datos, usted determina los datos personales que Adobe Experience Cloud procesa y almacena en su nombre.

Este documento describe cómo los atributos [!UICONTROL del] cliente admiten los derechos de acceso y eliminación de datos del RGPD de los sujetos de datos mediante la API de servicio de privacidad de Adobe Experience Platform y la interfaz de usuario de Privacy Service.

Para obtener más información sobre el significado del RGPD para su empresa, consulte [RGPD y Su empresa](https://www.adobe.com/es/privacy/general-data-protection-regulation.html).

## Configuración requerida para enviar solicitudes de atributos [!UICONTROL del cliente]

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

* &quot;regulación&quot;: **gdpr** (que es la norma de privacidad que se aplica a la solicitud)

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
