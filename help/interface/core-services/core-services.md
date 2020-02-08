---
description: Implementación de Experience Cloud y cómo convertirse en administrador. Este proceso moderniza las soluciones para funciones de servicios principales como los atributos del cliente y las audiencias.
keywords: core services;customer attributes
seo-description: Implementación de Experience Cloud y cómo convertirse en administrador. Este proceso moderniza las soluciones para funciones de servicios principales como los atributos del cliente y las audiencias.
seo-title: Activación de las soluciones de Experience Cloud en los servicios principales
solution: Experience Cloud
title: Activación de las soluciones en los servicios principales
uuid: 5820060f-9b18-4339-81e0-401d964f7a03
translation-type: tm+mt
source-git-commit: 02b0163b95c24eb58bf2379c3e0d9f5f31c40925

---


# Activación de las soluciones en los servicios principales

Para los clientes existentes, descubra cómo modernizar las implementaciones de soluciones e implementar Experience Cloud para que pueda usar funciones como atributos del cliente y audiencias. Para lograrlo, deberá:

1. [Únase a Experience Cloud y conviértase en administrador](#section_2423F0BD3DF642658103310EE5EA6154)
1. [Implementación del servicio Experience Cloud ID](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [Asignación de grupos de informes a una organización de Experience Cloud](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [Actualización del código de AppMeasurement para Analytics](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [Actualice la implementación de Adobe Target](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [Verifique la implementación de los servicios principales](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [Administración de usuarios y productos](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [Comenzar a utilizar los servicios principales](#section_960C06093623462E8EA247B3E97274A1)

<!-- <p>https://marketing-beta.adobe.com/resources/help/core/core-services.html </p> 
<p>https://adobe.sharepoint.com/sites/AGSConsulting/CoreServices/PA/_layouts/15/start.aspx#/ </p> -->

<!-- Core services architecture and data flow wiki: https://wiki.corp.adobe.com/pages/viewpage.action?pageId=1004285689 -->

## Paso 1. Únase a Experience Cloud y conviértase en administrador {#section_2423F0BD3DF642658103310EE5EA6154}

Le explicamos lo que debe hacer para unirse a Experience Cloud:

![](assets/step1_icon.png) Asegúrese de que cuenta con los SKU correspondientes de Adobe Analytics o Adobe Target.

* **Adobe Analytics:** Standard o Premium (no el SKU heredado de SiteCatalyst).
* **Adobe Target:** Standard o Premium.

>[!NOTE]
>
>Para Target, migre a at.js desde mbox.js. Consulte [Actualización desde at.js 1. x a at.js 2. x](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/upgrading-from-atjs-1x-to-atjs-20.html).

![](assets/step2_icon.png) Modernice su implementación y solicite que un administrador lo aprovisione.

1. Siga los pasos de [Implementación del servicio Experience Cloud ID](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354).
1. Póngase en contacto con su administrador de cuenta y comience el proceso de aprovisionamiento para Experience Cloud.

![](assets/step3_icon.png)[!UICONTROL  Administración de usuarios y productos en Admin Console].

**Acceso de administrador**

After you are an administrator, you can log in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

Verá el enlace **[!UICONTROL Administración]** en el menú de navegación de Experience Cloud.

Consulte [Administración de usuarios y productos de Experience Cloud](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909) para obtener ayuda.

**Acceso de usuarios**

Para iniciar sesión en Experience Cloud, los usuarios deben:

1. Tener un Adobe ID.
1. Sign in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. Pertenecer a un grupo de soluciones asignado a un grupo de empresas.
1. Si es necesario, vincule la cuentas de las soluciones a sus Adobe ID (se describe a continuación).

![](assets/step4_icon.png) Opcional: Vincule las cuentas de usuario existentes.

Most likely, you have users who are already members of solution groups, such an Analytics group that you previously managed in [!UICONTROL Analytics] > [!UICONTROL Admin Tools].

Cuando asigna estos grupos a grupos de empresas de Experience Cloud, esos usuarios deben vincular manualmente sus credenciales de cuenta de la solución al Adobe ID.

Consulte [Vinculación de cuentas en Experience Cloud](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

> [!NOTE]
> 
> Una vez asignados los grupos de soluciones de empresa, los nuevos usuarios se vinculan automáticamente. (las credenciales de la solución se crean automáticamente y se vinculan a su Adobe ID).

En las siguientes secciones se describe cómo modernizar la implementación. Modernizar la implementación activa los servicios principales en Experience Cloud.

## Paso 2: Implementación del servicio [!UICONTROL de ID de] Experience Cloud mediante el lanzamiento [!UICONTROL de la plataforma]Experience Cloud o la administración  dinámica de etiquetas {#section_3C9F6DF37C654D939625BB4D485E4354}

El servicio [!UICONTROL de ID de] Experience Cloud proporciona un ID común para la integración entre soluciones. Proporciona identificación de visitantes entre dominios y una ruta para la segmentación y personalización entre dispositivos y exploradores en función de los datos de CRM cargados mediante Atributos del cliente.

El método más sencillo para activar los servicios principales de Experience Cloud es activarlo automáticamente para Analytics y Target a través de la extensión [del servicio](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) Experience Cloud ID en el lanzamiento [!UICONTROL de la plataforma de]experiencia o a través de la herramienta ECID en la administración dinámica de etiquetas. (Se recomienda encarecidamente Iniciar la plataforma de experiencia).

![](assets/menu-activation-shell.png)

For complete Experience Cloud ID Service help (formerly, visitor ID), go [here](https://docs.adobe.com/content/help/en/id-service/using/home.html).

**¿No utiliza[!UICONTROL Experience Platform Launch]o[!UICONTROL Dynamic Tag Management]?**

If you are not using [!UICONTROL Experience Platform Launch] or [!UICONTROL Dynamic Tag Management], manually implement the ID service via the JavaScript Deployment ([!DNL VisitorAPI.js]), as follows:

| Tarea | Descripción |
| -----------| ---------- |  
| [Implementación del servicio de Experience Cloud ID para Analytics](https://docs.adobe.com/content/help/en/id-service/using/implementation/setup-analytics.html) | Adobe también recomienda la configuración de algunos [ID de cliente](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) adicionales. Estos ID están asociados a cada visitante y habilitan la funcionalidad actual y futura en Experience Cloud. |
| Actualice el [!DNL s_code] existente a la versión H.27.3 o posterior, o su [!DNL AppMeasurement.js] existente a la versión 1.4 o posterior. | Estos archivos están disponibles para su descarga en el [Administrador de códigos](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/code-manager-admin.html), en las herramientas del administrador de Analytics.  La guía de [implementación de JavaScript](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) está disponible si necesita obtener más información sobre [!DNL AppMeasurement.js]. |
| Sincronice el ID de cliente para Analytics | Consulte [Analytics - Sincronización del ID de cliente](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437) (a continuación). |

## Analytics y Target: Sincronización del ID de cliente {#section_AD473A6A21C1446498E700363F9A8437}

As a part of setting up the Experience Cloud ID Service, Adobe recommends for Analytics and [!DNL Target] that you synchronize your [customer IDs](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) with the Experience Cloud.

In Adobe Target, the `mbox3rdpartyid` needs to get the customer ID and send it to [!DNL Target]. (Consulte [Trabajo con atributos del cliente](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) en [!DNL Target].)

Cuando un visitante se autentica en su sitio web o se identifica de algún modo, la implementación debe mostrar el ID de cliente de CRM de esa persona a la página o aplicación. A continuación, puede usar la llamada de función apropiada para sincronizar el ID de cliente en Experience Cloud. Esta sincronización almacena el ID de cliente de CRM del visitante y activa esos atributos del cliente para su uso en Experience Cloud.

Por ejemplo, suponga que el ID de cliente de Bob es `52mc210tr42` en su sistema CRM. Cuando Bob se autentifique en su sitio, debe mostrar este ID en la página y utilizar el ID para sincronizarlo de una de las dos formas siguientes:

* Llamar a `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` mediante el servicio de ID del visitante. O bien,
* Rellenar el *`Customer ID (52mc210tr42)`* en una propiedad o eVar.

Se debe establecer el ID de cliente en cada llamada al servidor de [!DNL Analytics] cuando se conozca el ID de cliente.

### SDK para móvil

Consulte la sección Servicio *de ID de* Experience Cloud para ver ejemplos de sintaxis sobre cómo establecer ID de cliente adicionales en aplicaciones de [Android](https://docs.adobe.com/content/help/en/mobile-services/android/overview.html) e [iOS](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html) Mobile.

### Activación de atributos para datos históricos

Los datos de atributo del cliente pasan a estar disponibles una vez que los visitantes inician sesión. Si todavía no ha implementado el servicio de ID de Experience Cloud más reciente y ha estado realizando un seguimiento histórico de los ID de cliente en una prop o eVar, puede solicitar un proceso que envíe los inicios de sesión históricos a Experience Cloud. Este proceso le permite empezar a utilizar los atributos del cliente inmediatamente.

Póngase en contacto con el servicio de atención al cliente para activar los datos históricos.

## Paso 3. Map report suites to an Experience Cloud Organization {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloud services (such as Experience Cloud ID Service and the [!UICONTROL People service]) are associated with an Experience Cloud organization instead of an individual Analytics report suite. Para asegurar la correcta operación de estos servicios, cada grupo de informes de Analytics debe asignarse a una organización de Experience Cloud.

Consulte [Asignación de grupos de informes a una organización](report-suite-mapping.md).

## Paso 4. (Adobe Analytics) Update your Analytics AppMeasurement code {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Compruebe que está en una colección de datos regionales (RDC). Si el dominio de recopilación de datos es [!DNL omtrdc.net], o si el CNAME está asignado a [!DNL omtrdc.net], usted se encuentra en RDC. Consulte [Transición a RDC](https://docs.adobe.com/content/help/en/analytics/technotes/rdc/regional-data-collection.html) para obtener más información. If you are using first-party cookies, refer to [CNAME and the Experience Cloud ID Service](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) for information about data collection CNAMEs and cross-domain tracking.

Se le recomienda modernizar su implementación de Analytics mediante la actualización de sus bibliotecas de JavaScript, incluido el API de visitante. La forma más sencilla de conseguir esto es añadir una herramienta de [!DNL Adobe Analytics] en Dynamic Tag Management que especifique *`Automatic`* como método de configuración.

In [!UICONTROL Dynamic Tag Management], click **[!UICONTROL <Web Property Name>]**>**[!UICONTROL  Información general ]**>**[!UICONTROL  Agregar una herramienta ]**>**[!UICONTROL  Adobe Analytics ]**. Consulte[Configuración de Adobe Analytics](https://docs.adobe.com/content/help/en/dtm/using/tools/analytics-dtm.html)en la Dynamic Tag Management para obtener información de implementación.

## Paso 5. (Adobe Target) Update your Adobe Target implementation {#section_C2F4493C7A36406DAE2266B429A4BD24}

* It is recommended that you add an [Adobe Target extension](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html) in [!UICONTROL Experience Platform Launch], so that your library retrieval is automatic. También puede configurar la extensión [del servicio de ID de](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html) Experience Cloud para Target (y otras soluciones) mediante Inicio [!UICONTROL de plataforma de]experiencia. The [!UICONTROL Experience Cloud ID Service] update **is required** for [!UICONTROL Target] to use core services. (Si utiliza la administración dinámica de etiquetas, agregue una herramienta [de](https://docs.adobe.com/content/help/en/dtm/using/tools/target.html)Adobe Target. You can also use [!UICONTROL Dynamic Tag Management] to deploy the Experience Cloud ID Service for Target.)
* Si no utiliza Inicio [!UICONTROL de plataforma de] experiencia o Administración dinámica de etiquetas, [actualice la biblioteca](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html) de mbox manualmente.
* Solicite el acceso para utilizar Adobe Analytics como el origen de generación de informes para [!DNL Adobe Target]. [!DNL Target]Los datos de y se combinan en la misma llamada de servidor durante el procesamiento para que los visitantes se conecten entre las dos soluciones. [!DNL Analytics] Consulte [Implementación de Analytics para Target](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t.html).

   >[!IMPORTANT]
   >
   >Todos los clientes de Analytics ya están aprovisionados para servicios principales como los atributos del cliente. Si no es cliente de Analytics, póngase en contacto con la atención al cliente para solicitar que se le aprovisione.

## Paso 6. Verifique la implementación de los servicios principales {#section_E641782A0F4F44AF8C9C91216BE330D5}

Realice el siguiente proceso para asegurarse de que el servicio Experience Cloud ID se implementa correctamente en el sitio.

1. Borre las cookies del sitio para poder ver la solicitud al servicio Experience Cloud ID (la solicitud se realiza en la primera visita y, a continuación, una vez por visitante y semana aproximadamente).
1. Con la ayuda de un analizador de paquetes o el panel de red en un depurador de explorador web, busque una solicitud que se dirija a [!DNL dpm.demdex.net].
1. Compruebe que la respuesta contenga `d_mid` y un valor, por ejemplo: `_setMarketingCloudFields({"d_mid":"4235...`
1. Verify that the Analytics request contains the `mid` parameter (the Experience Cloud ID). During the grace period (if it is enabled), you should also see an `aid` parameter (the Analytics visitor ID).

La respuesta esperada que contiene el Experience Cloud ID:

![](assets/mac_id_response.png)

Solicitud de imagen de Analytics que contiene el ID de Experience Cloud (también conocido como `mid` o ID _de_ visitante):

![](assets/mid.png)

Experience Cloud ID en una solicitud de mbox:

![](assets/mbox_request.png)

**¿Qué es el período de gracia?**

Después de implementar el servicio Experience Cloud ID, los nuevos visitantes ya no reciben un ID de Experience Cloud de Analytics desde su servidor de recopilación de datos. Si secciones del sitio aún no han implementado el servicio Experience Cloud ID, cuando los visitantes accedan a estas secciones, el ID de Experience Cloud no se reconocerá y se asignará un ID de visitante de Analytics heredado a los visitantes. Esto puede causar problemas potenciales, como visitas duplicadas y atribuciones erróneas.

Por ejemplo, si la sección de soporte técnico de su sitio se administra en un CMS independiente, es posible que tenga un archivo JavaScript de Analytics distinto para esta sección. Si implementa el ID de Experience Cloud en el sitio principal antes de implementar el servicio de ID en el sitio de asistencia, los visitantes nuevos recibirán un ID de Analytics heredado cuando visiten la sección de asistencia y las visitas que abarquen ambas secciones del sitio se registrarán como visitas diferentes.

La implementación del servicio Experience Cloud ID en sitios que utilizan varios archivos JavaScript u otras tecnologías (como Flash) puede provocar problemas de coordinación, ya que debe habilitar el servicio Experience Cloud ID en todas las partes del sitio al mismo tiempo. Al configurar un período de gracia, los nuevos visitantes seguirán recibiendo un ID de visitante de Analytics desde el servicio de ID, de modo que los visitantes se puedan identificar de forma coherente en las secciones del sitio que no se hayan actualizado para utilizar el servicio de ID de visitante.

## Paso 7. Administración de usuarios y productos {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Once you are up and running, navigate to the [Admin Console](https://adminconsole.adobe.com/), where you can manage users and product profiles.

![](assets/menu-administration-shell.png)

Consulte [Administración de usuarios y productos de Experience Cloud](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

**Atributos del cliente**

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Target). 
 </note> </p> 
 -->

Users that are added to the [!UICONTROL Customer Attributes] group will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface

## Paso 8. Begin using core services {#section_960C06093623462E8EA247B3E97274A1}

Aproveche las siguientes funciones de servicios principales.

![](assets/menu-audiences-shell.png)

**[!UICONTROL Personas]> Atributos[!UICONTROdel cliente]**

Si captura los datos del cliente empresarial en una base de datos de administración de la relación con los clientes (CRM), podrá cargar los datos en una fuente de datos de atributos del cliente en Experience Cloud. Una vez cargados, saque el máximo partido de los datos en [!DNL Adobe Analytics] y [!DNL Adobe Target].

Consulte [Atributos del cliente](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

**[!UICONTROL Personas]> Biblioteca[!UICONTROL de audiencias]**

Experience Cloud [!UICONTROL Audiences] is the interface that lets you create audiences, combine existing audiences to create composite audiences, and view all shared audiences.

Consulte [Audiencias](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

<!-- aam_mc.xml -->

## Almacenamiento de datos y divulgación de información privada

Si utiliza los servicios de perfil de audiencia en tiempo real y otros servicios principales en Adobe [!DNL Experience Cloud], el uso de estos servicios podría determinar en qué centro (y en qué país) se alojan los datos. Specifically, because the core services of the Adobe [!DNL Experience Cloud] leverage Adobe Audience Manager, data used within the [!UICONTROL People] service must reside within Audience Manager servers in the United States.

When leveraging core services made available via the [!UICONTROL People] service, the types of data sent from other Adobe products to audience management are:

* Pares de clave/valor de [!DNL Analytics] (props, eVars, list vars, etc.). De forma predeterminada, las líneas de registro incluyen direcciones IP, con el último octeto de la dirección IP (suponiendo que esta no fue modificada por la configuración de confusión de IP dentro de Adobe [!DNL Analytics]).
* Características y segmentos para los que los visitantes califican según reglas establecidas en Audience Manager.
* (Opcional) Uno o más de sus ID. Según la implementación del servicio de ID, también podría estar enviando uno o más de sus ID, como ID de CRM o direcciones de correo electrónico con hash. Si estos datos se envían a Adobe [!DNL Analytics], se transfieren a la gestión de audiencias de Adobe. Adobe recomienda no proporcionar datos personales a Adobe [!DNL Analytics]. En lugar de ello, use un hash unidireccional para convertir en seudónimo los datos antes de enviarlos a Adobe.
* Segmentos que se originan en [!DNL Analytics] mediante la función de uso compartido de segmentos del back-end.
* Se instala la cookie de demdex.net si no están bloqueadas las cookies de terceros. The `AMCV_###@AdobeOrg` first-party cookie is always set with the Experience Cloud ID Service.

Todos estos elementos de datos se entregan a Adobe Audience Manager en forma de archivos de registro. Audience Manager procesa y almacena estos datos en los Estados Unidos. Audience Manager no proporciona una opción de almacenar o procesar estos datos fuera de los Estados Unidos.

**Cookies y no participaciones**

El uso de perfil de audiencia en tiempo real aprovecha la cookie de Audience Manager, además de las cookies utilizadas para [!DNL Analytics] y [!DNL Target].

Si desea proporcionar la capacidad adecuada de no participación, los visitantes del sitio deben agregar la no participación de Audience Manager a sus procesos de no participación actuales.

Consulte las instrucciones en [Adobe Experience Cloud: Implementación de no participación de Adobe](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/data-collection/opt-out.html).

Consulte [CNAME de recopilación de datos y seguimiento interdominio](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) para activar el seguimiento interdominio.
