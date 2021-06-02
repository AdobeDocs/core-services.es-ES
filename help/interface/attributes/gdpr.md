---
title: 'Cumplimiento de los Atributos del cliente con el Reglamento General de Protección de Datos '
description: Obtenga información sobre la compatibilidad con atributos de cliente con el Reglamento General de Protección de Datos
feature: 'Atributos del cliente '
topic: Administración
role: Administrator
level: Experienced
exl-id: 02417c0c-6780-4699-9470-f1685c3cd25d
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 95%

---

# Cumplimiento de los Atributos del cliente con el Reglamento General de Protección de Datos

Esta página describe cómo [!UICONTROL Customer Attributes] admite el Reglamento General de Protección de Datos (RGPD).

>[!IMPORTANT]
>
>Este documento no contiene material de asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte a su asesor jurídico sobre el RGPD.

El [Reglamento General de Protección de Datos](https://business.adobe.com/privacy/general-data-protection-regulation.html), una ley vigente desde el 25 de mayo de 2018, otorga a todos los individuos (sujetos de datos) dentro de las fronteras de la Unión Europea (UE) el control de sus datos personales. También simplifica el entorno reglamentario de las empresas internacionales. Esta ley se aplica a todas las empresas (responsables de tratamiento de datos) que ofrecen bienes o servicios a personas que se encuentran dentro de los límites de la UE, supervisan o recopilan datos personales de personas de la UE en el momento en que se procesan sus datos personales, independientemente de la ubicación comercial del responsable del tratamiento de datos.

Adobe Experience Cloud actúa como procesador de datos para cualquier dato personal que reciba y almacene en nombre de sus clientes. Como responsable del tratamiento de datos, determinará qué datos personales Adobe Experience Cloud trata y almacena en su nombre.

Este documento describe cómo los [!UICONTROL Atributos del cliente] admiten los derechos de acceso y eliminación de datos del RGPD de los sujetos de datos mediante la API de Adobe Experience Platform Privacy Service y la IU de Privacy Service.

Para obtener más información sobre el significado del RGPD para su empresa, consulte [RGPD y Su empresa](https://business.adobe.com/privacy/general-data-protection-regulation.html).

## Configuración necesaria para enviar solicitudes de [!UICONTROL Atributos del cliente]

Para realizar solicitudes de acceso y eliminación de datos para los [!UICONTROL Atributos del cliente], deberá:

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

## Campos de datos arrojados para las solicitudes de acceso

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
