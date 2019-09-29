---
description: Implementación de Experience Cloud y cómo convertirse en administrador. Este proceso moderniza las soluciones para funciones de servicios principales como los atributos del cliente y las audiencias.
keywords: servicios principales;atributos del cliente
seo-description: Implementación de Experience Cloud y cómo convertirse en administrador. Este proceso moderniza las soluciones para funciones de servicios principales como los atributos del cliente y las audiencias.
seo-title: Activación de las soluciones de Experience Cloud en los servicios principales
solution: Experience Cloud
title: Activación de las soluciones en los servicios principales
uuid: 5820060f-9b18-4339-81e0-401d964f7a03
translation-type: tm+mt
source-git-commit: b4809ff0b4546f105ac6270eca1bfce2b6467876

---


# Activación de las soluciones en los servicios principales

Implementación de Experience Cloud y cómo convertirse en administrador. Este proceso moderniza las soluciones para funciones de servicios principales como los atributos del cliente y las audiencias.

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
>For Target, [migrate to at.js from mbox.js](https://marketing.adobe.com/resources/help/en_US/target/ov2/t_target-migrate-atjs.html).


![](assets/step2_icon.png) Modernice su implementación y solicite que un administrador lo aprovisione.


1. Siga los pasos de [Implementación del servicio Experience Cloud ID](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354).
1. Póngase en contacto con su administrador de cuenta y comience el proceso de aprovisionamiento para Experience Cloud.

![](assets/step3_icon.png) Administración de usuarios y productos en Admin Console.

**Acceso de administrador**

Una vez que sea administrador, podrá iniciar sesión en [marketing.adobe.com](https://marketing.adobe.com).

Verá el enlace **[!UICONTROL Administración]** en el menú de navegación de Experience Cloud.

Consulte [Administración de usuarios y productos de Experience Cloud](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909) para obtener ayuda.

**Acceso de usuarios**

Para iniciar sesión en Experience Cloud, los usuarios deben:


1. Tener un Adobe ID.
1. Iniciar sesión en [!DNL marketing.adobe.com].
1. Pertenecer a un grupo de soluciones asignado a un grupo de empresas.
1. Si es necesario, vincule la cuentas de las soluciones a sus Adobe ID (se describe a continuación).

![](assets/step4_icon.png) Opcional: Vincule las cuentas de usuario existentes.

Lo más probable es que tenga usuarios que ya sean miembros de los grupos de soluciones, como un grupo de Analytics que administre en Analytics &gt; Herramientas de administración.

Cuando asigna estos grupos a grupos de empresas de Experience Cloud, esos usuarios deben vincular manualmente sus credenciales de cuenta de solución al Adobe ID.

Consulte [Vinculación de cuentas en Experience Cloud](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

> [!NOTE]
> 
> Una vez asignados los grupos de soluciones de empresa, los nuevos usuarios se vinculan automáticamente. (las credenciales de la solución se crean automáticamente y se vinculan a su Adobe ID).

En las siguientes secciones se describe cómo modernizar la implementación. Modernizar la implementación activa los servicios principales en Experience Cloud.

## Paso 2: Implemente el servicio Experience Cloud ID utilizando Dynamic Tag Manager o Experience Platform Launch {#section_3C9F6DF37C654D939625BB4D485E4354}

El método más sencillo para activar los servicios principales de Experience Cloud es activarlo automáticamente en Analytics y Target con la [herramienta del servicio Experience Cloud ID](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-dtm-implement.html) en Administrador dinámico de etiquetas. (O en Experience Platform Launch).

![](assets/menu-activation-shell.png)

Para obtener más información sobre el servicio Experience Cloud ID (anteriormente conocido como ID de visitante), vaya [aquí](https://marketing.adobe.com/resources/help/en_US/mcvid/).

Además, la herramienta de nueva generación para la administración de etiquetas es [Launch, de Adobe](https://marketing.adobe.com/resources/help/en_US/experience-cloud/launch/).

**¿No utiliza ni la Dynamic Tag Management ni Launch?**

Si no utiliza la Dynamic Tag Management, implemente manualmente el servicio de ID a través de la implementación de JavaScript ([!DNL VisitorAPI.js]) de esta forma:

1. Siga los pasos descritos en [Implementación del servicio de Experience Cloud ID para Analytics](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-analytics.html).

   Adobe también recomienda la configuración de algunos [ID de cliente](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-authenticated-state.html) adicionales. Estos ID se asocian con cada visitante para activar las funciones actuales y futuras en los servicios principales de Experience Cloud.

1. Actualice el [!DNL s_code] existente a la versión H.27.3 o posterior, o su [!DNL AppMeasurement.js] existente a la versión 1.4 o posterior.

   Estos archivos están disponibles para su descarga en el [Administrador de códigos](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=code_manager_admin), en las herramientas del administrador de Analytics.

   La guía de [implementación de JavaScript](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html) está disponible si necesita obtener más información sobre [!DNL AppMeasurement.js].

1. Sincronice el ID de cliente para Analytics. Consulte [Analytics - Sincronización del ID de cliente](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437) (a continuación).

## Analytics y Target: Sincronización del ID de cliente {#section_AD473A6A21C1446498E700363F9A8437}

Como parte de la configuración del servicio Experience Cloud ID, Adobe recomienda (para Analytics y Target) que sincronice los [ID de cliente](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-authenticated-state.html) con Experience Cloud.

En Target, [!DNL mbox3rdpartyid] debe obtener el ID de cliente y enviárselo a Target. (Consulte [Trabajo con atributos del cliente](https://marketing.adobe.com/resources/help/en_US/target/target/c_working-with-customer-attributes.html) en Target).

Cuando un visitante se autentica en su sitio web o se identifica de algún modo, la implementación debe mostrar el ID de cliente de CRM de esa persona a la página o aplicación. A continuación, puede usar la llamada de función apropiada para sincronizar el ID de cliente en Experience Cloud. Esta sincronización almacena el ID de cliente de CRM del visitante y activa esos atributos del cliente para su uso en Experience Cloud.

Por ejemplo, suponga que el ID de cliente de Bob es `52mc210tr42` en su sistema CRM. Cuando Bob se autentifique en su sitio, debe mostrar este ID en la página y utilizar el ID para sincronizarlo de una de las dos formas siguientes:

* Llamar a `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` mediante el servicio de ID del visitante. O bien,
* Rellenar el *`Customer ID (52mc210tr42)`* en una propiedad o eVar.


Se debe establecer el ID de cliente en cada llamada al servidor de [!DNL Analytics] cuando se conozca el ID de cliente.

**SDK para móvil**

Consulte la sección del servicio *de ID de* Experience Cloud para ver ejemplos de sintaxis sobre cómo establecer ID de cliente adicionales en aplicaciones de [Android](https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=methods) e [iOS](https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=methods) Mobile.

**Activación de atributos para datos históricos**

Los datos de atributo del cliente pasan a estar disponibles una vez que los visitantes inician sesión. Si aún no ha implementado el servicio más reciente de Experience Cloud ID y ha registrado históricamente los ID de cliente en una prop o eVar, puede solicitar un proceso que envíe los inicios de sesión históricos a Experience Cloud. Este proceso le permite empezar a utilizar los atributos del cliente inmediatamente.

Póngase en contacto con el servicio de atención al cliente para activar los datos históricos.

## Paso 3. Asignación de grupos de informes a una organización de Experience Cloud {#section_7B08516B01BA421681DF03D0E86CE3BA}

Los servicios de Experience Cloud (como el servicio Experience Cloud ID y People) están asociados a una organización de Experience Cloud, no a un grupo de informes individual. Para asegurar la correcta operación de estos servicios, cada grupo de informes de Analytics debe asignarse a una organización de Experience Cloud.

Consulte [Asignación de grupos de informes a una organización](report-suite-mapping.md).

## Paso 4. (Adobe Analytics) Modernice el código AppMeasurement de Analytics {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Compruebe que está en una colección de datos regionales (RDC). Si el dominio de recopilación de datos es [!DNL omtrdc.net], o si el CNAME está asignado a [!DNL omtrdc.net], usted se encuentra en RDC. Consulte [Transición a RDC](https://marketing.adobe.com/resources/help/en_US/whitepapers/rdc/?f=rdc_transition) para obtener más información. Si utiliza cookies propias, consulte [CNAME y el servicio de ID de visitante](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_cname) para obtener más información acerca de la colección de datos CNAME y el seguimiento interdominio.

Se le recomienda modernizar su implementación de Analytics mediante la actualización de sus bibliotecas de JavaScript, incluido el API de visitante. La forma más sencilla de conseguir esto es añadir una herramienta de [!DNL Adobe Analytics] en Dynamic Tag Management que especifique *`Automatic`* como método de configuración.

En Dynamic Tag Management, haga clic en **[!UICONTROL <Web Property Name>]**&gt;**[!UICONTROL Información general]**&gt;**[!UICONTROL Agregar una herramienta]**&gt;**[!UICONTROL Adobe Analytics]**. Consulte[Configuración de Adobe Analytics](https://marketing.adobe.com/resources/help/en_US/dtm/?f=analytics_dtm)en la Dynamic Tag Management para obtener información de implementación.

## Paso 5. (Adobe Target) Modernice su implementación de Adobe Target {#section_C2F4493C7A36406DAE2266B429A4BD24}

* Es recomendable agregar una [herramienta Adobe Target](https://marketing.adobe.com/resources/help/en_US/dtm/target.html) en la Dynamic Tag Management para que la recuperación de la biblioteca sea automática. En Dynamic Tag Management, haga clic en **[!UICONTROL <Web Property Name>]**&gt;**[!UICONTROL Información general]**&gt;**[!UICONTROL Agregar una herramienta]**&gt;**[!UICONTROL Adobe Target]**.** Nota:**También puede usar la Dynamic Tag Management para implementar el servicio Experience Cloud ID en Target (y otras soluciones). Para que Target use los servicios principales,** se necesita **la actualización del servicio Experience Cloud ID.
* Si no utiliza la Dynamic Tag Management, [actualice la biblioteca mbox](https://marketing.adobe.com/resources/help/en_US/target/ov/?f=t_mbox_download) manualmente.
* Solicite el acceso para utilizar Adobe Analytics como el origen de generación de informes para Adobe Target. Los datos de Target y Analytics se combinan en la misma llamada de servidor durante el procesamiento para que los visitantes se conecten entre las dos soluciones. Consulte [Implementación de Analytics para Target](https://marketing.adobe.com/resources/help/en_US/target/a4t/?f=a4t).
* 
   >[!IMPORTANT]
   >
   >Todos los clientes de Analytics ya se han aprovisionado de servicios principales como los atributos del cliente. Si no es cliente de Analytics, póngase en contacto con la atención al cliente para solicitar que se le aprovisione.

## Paso 6. Verifique la implementación de los servicios principales {#section_E641782A0F4F44AF8C9C91216BE330D5}

Realice este proceso para asegurarse de que el servicio Experience Cloud ID se implementa correctamente en el sitio.

1. Borre las cookies de su sitio para ver la solicitud al servicio Experience Cloud ID (la solicitud se realiza en la primera visita y, a continuación, una vez por visitante y semana).1. Con la ayuda de un analizador de paquetes o el panel de red en un depurador de explorador web, busque una solicitud que se dirija a [!DNL dpm.demdex.net].
1. Compruebe que la respuesta contenga `d_mid` y un valor, por ejemplo: `_setMarketingCloudFields({"d_mid":"4235...`
1. Compruebe que la solicitud de Analytics contiene el parámetro medio (Experience Cloud ID). Durante el período de gracia (si se ha habilitado), también verá un parámetro aid (el ID de visitante de Analytics).

La respuesta esperada que contiene el Experience Cloud ID:

![](assets/mac_id_response.png)

Una solicitud de imagen de Analytics que contiene el Experience Cloud ID (mid):

![](assets/mid.png)

Experience Cloud ID en una solicitud de mbox:

![](assets/mbox_request.png)

**¿Qué es el período de gracia?**

Una vez que haya implementado el servicio de ID de visitante, el servidor de recopilación de datos ya no asignará a los nuevos visitantes un ID de visitante de Analytics. Si hay secciones de su sitio que todavía no hayan implementado el servicio ID de visitante, cuando los visitantes accedan a ellas el Experience Cloud ID no se reconocerá y se asignará un ID de visitante de Analytics heredado a los visitantes. Esto puede causar problemas potenciales, como visitas duplicadas y atribuciones erróneas.

Por ejemplo, si la sección de soporte técnico de su sitio se administra en un CMS independiente, es posible que tenga un archivo JavaScript de Analytics distinto para esta sección. Si implementa el ID de visitante en el sitio principal antes de implementar el servicio de ID de visitante en el sitio de soporte técnico, los visitantes nuevos recibirán un ID de Analytics heredado cuando visiten la sección de soporte, y las visitas que abarquen las dos secciones del sitio se contabilizarán como visitas distintas.

La implementación del servicio de ID de visitante en sitios que utilicen varios archivos JavaScript u otras tecnologías (como Flash) puede producir problemas de coordinación, ya que será necesario habilitar el servicio de ID de visitante en todas las áreas del sitio al mismo tiempo. Si configura un período de gracia, el servicio de ID de visitante seguirá asignando un ID de visitante de Analytics a los nuevos visitantes, de manera que estos se puedan identificar de forma consistente en las secciones del sitio que todavía no utilicen el servicio de ID de visitante.

## Paso 7. Administración de usuarios y productos {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Una vez que esté en funcionamiento, vaya a **[!UICONTROL Administración]** &gt; **[!UICONTROL Iniciar Admin Console]**, donde puede administrar usuarios y perfiles de producto.

![](assets/menu-administration-shell.png)

Consulte [Administración de usuarios y productos de Experience Cloud](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

**Atributos del cliente**

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Target). 
 </note> </p> 
 -->

Los usuarios que se agregan al grupo Atributos del cliente podrán ver el elemento de menú [!UICONTROL Atributos del cliente] a la izquierda de la interfaz de Experience Cloud

## Paso 8. Empezar a utilizar los servicios principales {#section_960C06093623462E8EA247B3E97274A1}

Aproveche las siguientes funciones de servicios principales.

![](assets/menu-audiences-shell.png)

**People &gt; Atributos del cliente**

Si captura los datos del cliente empresarial en una base de datos de administración de la relación con los clientes (CRM), podrá cargar los datos en una fuente de datos de atributos del cliente en Experience Cloud. Una vez cargados, saque el máximo partido de los datos en [!DNL Adobe Analytics] y [!DNL Adobe Target].

Consulte [Atributos del cliente](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

**People &gt; Biblioteca de audiencias**

Audiencias de Experience Cloud es la interfaz que le permite crear audiencias, combinar audiencias existentes para crear audiencias compuestas y ver todas las audiencias compartidas.

Consulte [Audiencias](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

<!-- aam_mc.xml -->

## Información sobre almacenamiento de datos y revelación de información privada

Si utiliza los servicios de perfil de audiencia en tiempo real y otros servicios principales en Adobe [!DNL Experience Cloud], el uso de estos servicios podría determinar en qué centro (y en qué país) se alojan los datos. En concreto, como los servicios principales de Adobe [!DNL Experience Cloud] se sirven de Adobe Audience Manager, los datos utilizados en People deben residir en servidores de Audience Manager en Estados Unidos.

Al utilizar los servicios principales disponibles mediante el servicio principal People, los tipos de datos enviados desde otros productos de Adobe a la gestión de audiencias son los siguientes:

* Pares de clave/valor de [!DNL Analytics] (props, eVars, list vars, etc.). De forma predeterminada, las líneas de registro incluyen direcciones IP, con el último octeto de la dirección IP (suponiendo que esta no fue modificada por la configuración de confusión de IP dentro de Adobe [!DNL Analytics]).
* Características y segmentos para los que los visitantes califican según reglas establecidas en Audience Manager.
* (Opcional) Uno o más de sus ID. Según la implementación del servicio de ID, también podría estar enviando uno o más de sus ID, como ID de CRM o direcciones de correo electrónico con hash. Si estos datos se envían a Adobe [!DNL Analytics], se transfieren a la gestión de audiencias de Adobe. Adobe recomienda no proporcionar datos personales a Adobe [!DNL Analytics]. En lugar de ello, use un hash unidireccional para convertir en seudónimo los datos antes de enviarlos a Adobe.
* Segmentos que se originan en [!DNL Analytics] mediante la función de uso compartido de segmentos del back-end.
* Se instala la cookie de demdex.net si no están bloqueadas las cookies de terceros. La cookie propia `AMCV_###@AdobeOrg` siempre se instala con el Experience Cloud ID (anteriormente, el servicio ID de visitante).


Todos estos elementos de datos se entregan a Adobe Audience Manager en forma de archivos de registro. Audience Manager procesa y almacena estos datos en los Estados Unidos. Audience Manager no proporciona una opción de almacenar o procesar estos datos fuera de los Estados Unidos.

**Cookies y no participaciones**

El uso de perfil de audiencia en tiempo real aprovecha la cookie de Audience Manager, además de las cookies utilizadas para [!DNL Analytics] y [!DNL Target].

Si desea proporcionar la capacidad adecuada de no participación, los visitantes del sitio deben agregar la no participación de Audience Manager a sus procesos de no participación actuales.

Consulte las instrucciones en [Adobe Experience Cloud: Implementación de no participación de Adobe](https://marketing.adobe.com/resources/help/en_US/sc/implement/opt_out.html).

Consulte [CNAME de recopilación de datos y seguimiento interdominio](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_cname) para activar el seguimiento interdominio.
