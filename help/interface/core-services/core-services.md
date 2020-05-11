---
description: Implemente Experience Cloud y conviértase en administrador. Este proceso moderniza sus soluciones para funciones como Atributos y audiencias del cliente.
keywords: core services;Customer Attributes
seo-description: Implemente Experience Cloud y conviértase en administrador. Este proceso moderniza sus soluciones para funciones como Atributos y audiencias del cliente.
seo-title: Activación de las soluciones de Experience Cloud en los servicios principales
solution: Experience Cloud
title: Activación de las soluciones en los servicios principales
index: true
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '2358'
ht-degree: 30%

---


# Activación de las soluciones en los servicios principales

Para los clientes existentes, descubra cómo modernizar las implementaciones de soluciones e implementar Experience Cloud para que pueda utilizar funciones como Atributos y audiencias del cliente. Para lograrlo, deberá:

1. [Únase a Experience Cloud y conviértase en administrador](#section_2423F0BD3DF642658103310EE5EA6154)
1. [Implementación del servicio Experience Cloud ID](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [Asignación de grupos de informes a una organización de Experience Cloud](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [Actualización del código de AppMeasurement para Analytics](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [Actualice la implementación de Adobe Destinatario](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [Verifique la implementación de los servicios principales](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [Administración de usuarios y productos](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [Comenzar a utilizar los servicios principales](#section_960C06093623462E8EA247B3E97274A1)

## Paso 1. Únase a Experience Cloud y conviértase en administrador {#section_2423F0BD3DF642658103310EE5EA6154}

Le explicamos lo que debe hacer para unirse a Experience Cloud:

![](assets/step1_icon.png) Asegúrese de que cuenta con los SKU correspondientes de Adobe Analytics o Adobe Target.

* **Adobe Analytics:** Standard o Premium (no el [!DNL SiteCatalyst] SKU heredado).
* **Adobe Destinatario:** Standard o Premium.

>[!NOTE]
>
>Por [!DNL Target]ejemplo, migre a at.js desde [!DNL mbox.js]. See [Upgrading from at.js 1. x to at.js 2. x](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/upgrading-from-atjs-1x-to-atjs-20.html).

![](assets/step2_icon.png) Modernice su implementación y solicite que un administrador lo aprovisione.

1. Siga los pasos a continuación en [Implementación del servicio [!UICONTROL de ID de]](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)Experience Cloud.
1. Póngase en contacto con su administrador de cuentas y inicio para conocer el proceso de aprovisionamiento de Experience Cloud.

![](assets/step3_icon.png)[!UICONTROL  Administración de usuarios y productos en Admin Console].

### Inicio de sesión de administrador

After you are an administrator, you can log in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

Verá el enlace **[!UICONTROL Administración]** en el menú de navegación de Experience Cloud.

Consulte [Administración de usuarios y productos de Experience Cloud](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909) para obtener ayuda.

### Inicio de sesión de usuario

Para iniciar sesión en Experience Cloud, los usuarios deben:

1. Tenga un Adobe ID (o Enterprise ID para su compañía).
1. Sign in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. Pertenecer a un grupo de soluciones asignado a un grupo de empresas.
1. Si es necesario, vincule sus cuentas de soluciones a su Adobe ID (descrito a continuación).

![](assets/step4_icon.png) Opcional: Vincule las cuentas de usuario existentes.

Lo más probable es que tenga usuarios que ya sean miembros de grupos de soluciones, como un grupo de Analytics que haya gestionado anteriormente en [!UICONTROL Analytics] > Herramientas [!UICONTROL de administración].

Al asignar estos grupos a grupos empresariales de Experience Cloud, estos usuarios deben vincular manualmente sus credenciales de cuenta de la solución a su Adobe ID.

Consulte [Vinculación de cuentas en Experience Cloud](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

>[!NOTE]
>
>Una vez asignados los grupos de soluciones de empresa, los nuevos usuarios se vinculan automáticamente. (Las credenciales de la solución se crean automáticamente y se vinculan a su Adobe ID).

Las siguientes secciones describen cómo modernizar la implementación. La modernización de la implementación habilita los servicios principales en Experience Cloud.

## Paso 2: Implementación del servicio [!UICONTROL de ID de] Experience Cloud mediante [!UICONTROL Experience Platform Launch]o administración [!UICONTROL dinámica de etiquetas] {#section_3C9F6DF37C654D939625BB4D485E4354}

El servicio [!UICONTROL de ID de] Experience Cloud proporciona un ID común para la integración entre soluciones. Proporciona identificación de visitantes entre dominios y una ruta para la segmentación y personalización entre dispositivos y navegadores en función de los datos CRM cargados mediante Atributos del cliente.

El método más sencillo para activar los servicios principales de Experience Cloud es activarlo automáticamente para Analytics y Adobe Destinatario mediante la extensión [del servicio](https://docs.adobe.com/content/help/es-ES/launch/using/implement/solutions/idservice-save.html) Experience Cloud ID en [!UICONTROL Experience Platform Launch]o mediante la herramienta ECID en la administración dinámica de etiquetas. (Se recomienda encarecidamente Experience Platform Launch).

![](assets/menu-activation-shell.png)

Para obtener la ayuda completa del servicio Experience Cloud ID (anteriormente, ID de visitante), vaya [aquí](https://docs.adobe.com/content/help/es-ES/id-service/using/home.html).

**¿No utiliza[!UICONTROL Experience Platform Launch]o administracióndinámica de etiquetas?**

If you are not using [!UICONTROL Experience Platform Launch] or [!UICONTROL Dynamic Tag Management], manually implement the ID service via the JavaScript Deployment ([!DNL VisitorAPI.js]), as follows:

| Tarea | Descripción |
| -----------| ---------- |  
| [Implementación del servicio de Experience Cloud ID para Analytics](https://docs.adobe.com/content/help/en/id-service/using/implementation/setup-analytics.html) | Adobe también recomienda configurar ID [de cliente](https://docs.adobe.com/content/help/es-ES/id-service/using/reference/authenticated-state.html)adicionales. Estos ID están asociados a cada visitante y habilitan la funcionalidad actual y futura en Experience Cloud. |
| Actualice el [!DNL s_code] existente a la versión H.27.3 o posterior, o su [!DNL AppMeasurement.js] existente a la versión 1.4 o posterior. | Estos archivos están disponibles para su descarga en el Administrador [de](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/code-manager-admin.html) códigos de las herramientas de administración de Analytics.  (La guía de implementación [de](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) JavaScript está disponible si necesita más información sobre [!DNL AppMeasurement.js]). |
| Sincronizar el ID de cliente para Analytics | See [Analytics - synching the customer ID](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437) (below). |

## Analytics &amp; Adobe Target - synching the customer ID {#section_AD473A6A21C1446498E700363F9A8437}

As a part of setting up the Experience Cloud ID Service, Adobe recommends for Analytics and [!DNL Target] that you synchronize your [customer IDs](https://docs.adobe.com/content/help/es-ES/id-service/using/reference/authenticated-state.html) with the Experience Cloud.

In Adobe Target, the `mbox3rdpartyid` needs to get the customer ID and send it to [!DNL Target]. (Consulte [Uso de atributos](https://docs.adobe.com/content/help/es-ES/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) de cliente en la [!DNL Target]).

Cuando un visitante se autentica en su sitio web o se identifica a sí mismo de otra manera, su implementación debe exponer el ID de cliente de CRM de esa persona a la página o aplicación. A continuación, puede utilizar la llamada de función adecuada para sincronizar su ID de cliente con Experience Cloud. Esta sincronización almacena el ID de cliente de CRM de visitante en Experience Cloud y activa los atributos de cliente para su uso en Experience Cloud.

Por ejemplo, suponga que el ID de cliente de Bob es `52mc210tr42` en su sistema CRM. Cuando Bob se autentifique en su sitio, debe mostrar este ID en la página y utilizar el ID para sincronizarlo de una de las dos formas siguientes:

* Llamar a `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` mediante el servicio de ID del visitante. O,
* Rellene la *`Customer ID (52mc210tr42)`* variable en una propiedad o eVar.

Se debe establecer el ID de cliente en cada llamada al servidor de [!DNL Analytics] cuando se conozca el ID de cliente.

### SDK para móvil

Consulte la sección Servicio *de ID de* Experience Cloud para ver ejemplos de sintaxis sobre cómo establecer ID de cliente adicionales en aplicaciones de [Android](https://docs.adobe.com/content/help/es-ES/mobile-services/android/overview.html) e [iOS](https://docs.adobe.com/content/help/es-ES/mobile-services/ios/overview.html) Mobile.

### Activación de atributos para datos históricos

Los datos de atributos del cliente están disponibles después de que los visitantes inicien sesión. Si todavía no ha implementado el servicio de ID de Experience Cloud más reciente y ha estado realizando un seguimiento histórico de los ID de cliente en una prop o eVar, puede solicitar un proceso que envíe los inicios de sesión históricos a Experience Cloud. Este proceso le permite empezar a utilizar Atributos del cliente inmediatamente.

Póngase en contacto con el Servicio de atención al cliente para habilitar los datos históricos.

## Paso 3. Map report suites to an Experience Cloud Organization {#section_7B08516B01BA421681DF03D0E86CE3BA}

Los servicios de Experience Cloud (como el servicio [!UICONTROL Experience Cloud ID y el servicio]Personas) están asociados a una organización de Experience Cloud en lugar de a un grupo de informes de Analytics individual. Para garantizar que estos servicios funcionen correctamente, cada grupo de informes de Analytics debe asignarse a una organización de Experience Cloud.

Consulte [Asignación de grupos de informes a una organización](report-suite-mapping.md).

## Paso 4. (Adobe Analytics) Update your Analytics AppMeasurement code {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Compruebe que está en una colección de datos regionales (RDC). Si el dominio de recopilación de datos es [!DNL omtrdc.net], o si el CNAME está asignado a [!DNL omtrdc.net], usted se encuentra en RDC. Consulte [Transición a RDC](https://docs.adobe.com/content/help/en/analytics/technotes/rdc/regional-data-collection.html) para obtener más información. Si utiliza cookies de origen, consulte [CNAME y el servicio](https://docs.adobe.com/content/help/es-ES/id-service/using/reference/analytics-reference/cname.html) de ID de Experience Cloud para obtener información sobre los CNAME de recopilación de datos y el seguimiento entre dominios.

Se le recomienda modernizar su implementación de Analytics mediante la actualización de sus bibliotecas de JavaScript, incluido el API de visitante. La forma más sencilla de conseguir esto es añadir una herramienta de [!DNL Adobe Analytics] en Dynamic Tag Management que especifique *`Automatic`* como método de configuración.

In [!UICONTROL Dynamic Tag Management], click **[!UICONTROL <Web Property Name>]**>**[!UICONTROL  Información general ]**>**[!UICONTROL  Añadir una herramienta ]**>**[!UICONTROL  Adobe Analytics ]**. Consulte Configuración[de](https://docs.adobe.com/content/help/en/dtm/using/tools/analytics-dtm.html)Adobe Analytics en la administración dinámica de etiquetas para obtener información sobre la implementación.

## Paso 5. (Adobe Target) Update your Adobe Target implementation {#section_C2F4493C7A36406DAE2266B429A4BD24}

* Se recomienda agregar una Extensión de grupo de destinatarios [de](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html) Adobe en [!UICONTROL Experience Platform Launch]para que la recuperación de la biblioteca sea automática. También puede configurar la extensión [del servicio](https://docs.adobe.com/content/help/es-ES/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html) Experience Cloud ID para Adobe Destinatario (y otras soluciones) mediante [!UICONTROL Experience Platform Launch]. La actualización del servicio [!UICONTROL de ID de] Experience Cloud **es necesaria** para que Adobe Destinatario utilice los servicios principales. (Si utiliza la administración [!UICONTROL dinámica de etiquetas], agregue una herramienta [de](https://docs.adobe.com/content/help/en/dtm/using/tools/target.html)Adobe Destinatario. También puede utilizar la administración  dinámica de etiquetas para implementar el servicio Experience Cloud ID en Adobe Destinatario).
* Si no utiliza [!UICONTROL Experience Platform Launch] o Administración dinámica de etiquetas, [actualice la biblioteca](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html) de mbox manualmente.
* Solicite el acceso para utilizar Adobe Analytics como el origen de generación de informes para [!DNL Adobe Target]. [!DNL Target]Los datos de y se combinan en la misma llamada de servidor durante el procesamiento para que los visitantes se conecten entre las dos soluciones. [!DNL Analytics] See [Analytics for Target Implementation](https://docs.adobe.com/content/help/es-ES/target/using/integrate/a4t/a4t.html).

   >[!IMPORTANT]
   >
   >Todos los clientes de Analytics ya están aprovisionados para servicios principales como Atributos del cliente. Si no es cliente de Analytics, póngase en contacto con la atención al cliente para solicitar que se le aprovisione.

## Paso 6. Verifique la implementación de los servicios principales {#section_E641782A0F4F44AF8C9C91216BE330D5}

Realice el siguiente proceso para asegurarse de que el servicio Experience Cloud ID se implementa correctamente en el sitio.

1. Borre las cookies de su sitio para poder ver la solicitud al servicio Experience Cloud ID (la solicitud se realiza en la primera visita y, a continuación, una vez por visitante y semana aproximadamente).
1. Con la ayuda de un analizador de paquetes o el panel de red en un depurador de explorador web, busque una solicitud que se dirija a [!DNL dpm.demdex.net].
1. Compruebe que la respuesta contenga `d_mid` y un valor, por ejemplo: `_setMarketingCloudFields({"d_mid":"4235...`
1. Compruebe que la solicitud de Analytics contiene el `mid` parámetro (Experience Cloud ID). Durante el período de gracia (si está activado), también debería ver un `aid` parámetro (el ID de visitante de Analytics).

Respuesta esperada que contiene el ID de Experience Cloud:

![](assets/mac_id_response.png)

Solicitud de imagen de Analytics que contiene el ID de Experience Cloud (también conocido como `mid` o ID _de_ visitante):

![](assets/mid.png)

Experience Cloud ID en la solicitud de mbox:

![](assets/mbox_request.png)

### ¿Cuál es el período de gracia?

Después de implementar el servicio Experience Cloud ID, los nuevos visitantes ya no reciben un ID de Experience Cloud de Analytics desde su servidor de recopilación de datos. Si secciones del sitio aún no han implementado el servicio Experience Cloud ID, cuando los visitantes accedan a estas secciones, el ID de Experience Cloud no se reconocerá y se asignará un ID de visitante de Analytics heredado a los visitantes. Esto puede causar problemas potenciales, como visitas al duplicado y atribución incorrecta.

Por ejemplo: si la sección de asistencia técnica de su sitio se administra en un CMS independiente, puede tener un archivo JavaScript de Analytics diferente para esta sección. Si implementa el ID de Experience Cloud en el sitio principal antes de implementar el servicio de ID en el sitio de asistencia, los nuevos visitantes recibirán un ID de Analytics heredado cuando visiten la sección de asistencia y las visitas que abarquen ambas secciones del sitio se registrarán como visitas diferentes.

La implementación del servicio Experience Cloud ID en sitios que utilizan varios archivos JavaScript u otras tecnologías (como Flash) puede provocar problemas de coordinación, ya que debe habilitar el servicio Experience Cloud ID en todas las partes del sitio al mismo tiempo. Al configurar un período de gracia, los nuevos visitantes seguirán recibiendo un ID de visitante de Analytics del servicio de ID, de modo que los visitantes se puedan identificar de forma coherente en las secciones del sitio que no se hayan actualizado para utilizar el servicio de ID de visitante.

## Paso 7. Administración de usuarios y productos {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Once you are up and running, navigate to the [Admin Console](https://adminconsole.adobe.com/), where you can manage users and product profiles.

![](assets/menu-administration-shell.png)

Consulte [Administración de usuarios y productos de Experience Cloud](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

### Atributos del cliente

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Adobe Target). 
 </note> </p> 
 -->

Users that are added to the [!UICONTROL Customer Attributes] group will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface.

## Paso 8. Begin using core services {#section_960C06093623462E8EA247B3E97274A1}

Aproveche las siguientes funciones.

![](assets/menu-audiences-shell.png)

### [!UICONTROL Personas] > Atributos [!UICONTROL del cliente]

Si captura los datos del cliente empresarial en una base de datos de administración de la relación con los clientes (CRM), podrá cargar los datos en una fuente de datos de atributos del cliente en Experience Cloud. Una vez cargados, saque el máximo partido de los datos en [!DNL Adobe Analytics] y [!DNL Adobe Target].

Consulte [Atributos del cliente](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

### [!UICONTROL Personas] > Biblioteca [!UICONTROL de Audiencias]

Experience Cloud [!UICONTROL Audiences] is the interface that lets you create audiences, combine existing audiences to create composite audiences, and view all shared audiences.

Consulte [Audiencias](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

## almacenamiento de datos y revelación de privacidad

Si utiliza los servicios de perfil de audiencia en tiempo real y otros servicios principales en Adobe [!DNL Experience Cloud], el uso de estos servicios podría determinar en qué centro (y en qué país) se alojan los datos. Specifically, because the core services of the Adobe [!DNL Experience Cloud] leverage Adobe Audience Manager, data used within the [!UICONTROL People] service must reside within Audience Manager servers in the United States.

When leveraging core services made available via the [!UICONTROL People] service, the types of data sent from other Adobe products to audience management are:

* Pares de clave/valor de [!DNL Analytics] (props, eVars, list vars, etc.). De forma predeterminada, las líneas de registro incluyen direcciones IP, con el último octeto de la dirección IP (suponiendo que esta no fue modificada por la configuración de confusión de IP dentro de Adobe [!DNL Analytics]).
* Características y segmentos para los que los visitantes cumplen los requisitos según las reglas configuradas en el Administrador de Audiencias.
* (Opcional) Uno o más de sus ID. Según la implementación del servicio de ID, también podría estar enviando uno o más de sus ID, como ID de CRM o direcciones de correo electrónico con hash. Si estos datos se envían a Adobe [!DNL Analytics], se transfieren a la gestión de audiencias de Adobe. Adobe recomienda no proporcionar datos personales a Adobe [!DNL Analytics]. En su lugar, utilice un hash unidireccional para enmascarar los datos antes de enviarlos a Adobe.
* Segmentos que se originan en [!DNL Analytics] mediante la función de uso compartido de segmentos del back-end.
* Se instala la cookie de demdex.net si no están bloqueadas las cookies de terceros. The `AMCV_###@AdobeOrg` first-party cookie is always set with the Experience Cloud ID Service.

Todos estos elementos de datos se entregan a Adobe Audiencia Manager en forma de archivos de registro. El Administrador de Audiencias procesa y almacena estos datos dentro de los Estados Unidos. El Administrador de Audiencias no proporciona una opción para almacenar o procesar estos datos fuera de Estados Unidos.

### Cookies y no participaciones

El uso de perfil de audiencia en tiempo real aprovecha la cookie de Audience Manager, además de las cookies utilizadas para [!DNL Analytics] y [!DNL Target].

Si desea proporcionar la capacidad adecuada de no participación, los visitantes del sitio deben agregar la no participación de Audience Manager a sus procesos de no participación actuales.

Consulte [Adobe Experience Cloud: Implementación de exclusiones](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/data-collection/opt-out.html) de Adobe para obtener instrucciones.

Consulte CNAME de recopilación [de datos y seguimiento](https://docs.adobe.com/content/help/es-ES/id-service/using/reference/analytics-reference/cname.html) entre dominios para habilitar el seguimiento entre dominios.
