---
description: Modernice sus aplicaciones de Adobe Analytics y Adobe Target para servicios entre aplicaciones. Empiece a utilizar los servicios de Experience Cloud.
solution: Experience Cloud
title: Habilitar las aplicaciones para los servicios entre aplicaciones
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: 48e79e23-b339-4143-b3b1-969c370efeff
source-git-commit: 55b28d6a16f88955d7259a464bb690ee5985540e
workflow-type: tm+mt
source-wordcount: '2191'
ht-degree: 89%

---

# Habilite la implementación para los servicios de Experience Cloud

Si ha implementado recientemente Experience Cloud mediante etiquetas de Experience Platform, ya tiene todo configurado para Atributos del cliente y Audiencias de Experience Cloud. También puede administrar usuarios y productos en Admin Console.

Los clientes existentes pueden modernizar las implementaciones de sus aplicaciones e implementar Experience Cloud. Al hacerlo, puede usar los atributos del cliente y las funciones de audiencia en Adobe Analytics, Audience Manager y Adobe Target. Para lograr esta implementación, deberá hacer lo siguiente:

1. [Únase a Experience Cloud y conviértase en administrador](#section_2423F0BD3DF642658103310EE5EA6154)
1. [Implementación del Servicio de Experience Cloud ID](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [Asigne grupos de informes a una organización de Experience Cloud](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [Actualice el código de AppMeasurement para Analytics](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [Actualice la implementación de Adobe Target](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [Verificar la implementación](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [Administración de usuarios y productos](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [Iniciar el uso compartido de datos de atributos y públicos](#section_960C06093623462E8EA247B3E97274A1)

## Únase a Experience Cloud y conviértase en administrador {#section_2423F0BD3DF642658103310EE5EA6154}

Qué debe hacer para unirse a Experience Cloud:

1. Asegúrese de que cuenta con los SKU correspondientes de Adobe Analytics o Adobe Target.

   * **Adobe Analytics:** Standard o Premium (no el SKU de [!DNL SiteCatalyst] heredado).
   * **Adobe Target:** Standard o Premium.

   >[!NOTE]
   >
   >Para [!DNL Target], migre a at.js desde [!DNL mbox.js]. Consulte [Actualización de at.js 1. x a at.js 2. x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/upgrading-from-atjs-1x-to-atjs-20.html).

1. Modernice su implementación y solicite que un administrador lo aprovisione.

   * Siga los pasos de [Implementar el [!UICONTROL servicio de Experience Cloud ID]](core-services.md#section_3C9F6DF37C654D939625BB4D485E4354) a continuación.
   * Póngase en contacto con su administrador de cuentas e inicie el proceso de aprovisionamiento de Experience Cloud.

1. Administración de usuarios y productos en [!UICONTROL Admin Console].

### Inicio de sesión de administrador

Una vez que sea administrador, podrá iniciar sesión en [experiencecloud.adobe.com](https://experience.adobe.com).

El vínculo **[!UICONTROL Admin Console]** está disponible en la navegación del menú de Experience Cloud.

Consulte [Administración de usuarios y productos de Experience Cloud](admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909) para obtener más información.

### Inicio de sesión de usuario

Para iniciar sesión en Experience Cloud, los usuarios deben:

* Tener un Adobe ID (o Enterprise ID para su compañía).
* Iniciar sesión en [experiencecloud.adobe.com](https://experience.adobe.com).
* Pertenecer a un grupo de aplicaciones asignado a un grupo de empresas.
* Si es necesario, vincule sus cuentas de aplicaciones a su Adobe ID (descrito a continuación).

### Opcional: vincule las cuentas de usuario existentes.

Lo más probable es que tenga usuarios que ya sean miembros de grupos de aplicaciones, como un grupo de Analytics que haya gestionado anteriormente en [!UICONTROL Analytics] > [!UICONTROL Herramientas de administración].

Al asignar estos grupos a grupos empresariales de Experience Cloud, estos usuarios deben vincular manualmente sus credenciales de cuenta de la aplicación a su Adobe ID.

Consulte [Vinculación de cuentas en Experience Cloud](organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

>[!NOTE]
>
>Una vez asignados los grupos de aplicaciones y de empresa, los nuevos usuarios se vinculan automáticamente. (Las credenciales de la solución se crean automáticamente y se vinculan a su Adobe ID).

Las siguientes secciones describen cómo modernizar la implementación. La modernización de la implementación habilita los servicios principales en Experience Cloud.

## Implementación del [!UICONTROL Servicio de Experience Cloud ID] {#section_3C9F6DF37C654D939625BB4D485E4354}

El [!UICONTROL Servicio de Experience Cloud ID] proporciona un ID común para la integración entre aplicaciones. Proporciona identificación de visitantes entre dominios y una ruta para la segmentación y personalización entre dispositivos y navegadores en función de los datos de CRM cargados mediante [!UICONTROL Atributos del cliente].

El método más sencillo para activar los servicios principales de Experience Cloud es activarlos automáticamente para Analytics y Adobe Target mediante la [extensión del Servicio de Experience Cloud ID](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html?lang=es) en [!UICONTROL Experience Platform Launch].

Para obtener la ayuda completa del Servicio de Experience Cloud ID (anteriormente, ID de visitante), vaya [aquí](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=es#intro).

**No se utiliza [!UICONTROL Etiquetas de Experience Platform]?**

Si no está utilizando [!UICONTROL Etiquetas de Experience Platform], implemente manualmente el servicio de ID mediante la implementación de JavaScript (`VisitorAPI.js`), como se indica a continuación:

| Tarea | Descripción |
| -----------| ---------- |  
| [Implemente el Servicio de Experience Cloud ID para Analytics](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=es) | Adobe también recomienda configurar algunos [ID de cliente](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=es) adicionales. Estos ID se asocian con cada visitante para activar las funciones actuales y futuras en Experience Cloud. |
| Actualice el `s_code` existente a la versión H.27.3 o posterior, o su `AppMeasurement.js` existente a la versión 1.4 o posterior. | Estos archivos están disponibles para su descarga en el [Administrador de códigos](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html?lang=es) de las herramientas de administración de Analytics. (La guía de [implementación de JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=es#js) está disponible si necesita más información sobre [!DNL AppMeasurement.js]). |
| Sincronizar el ID de cliente para Analytics | Consulte [Analytics: Sincronización del ID de cliente](core-services.md#section_AD473A6A21C1446498E700363F9A8437) (a continuación). |

{style="table-layout:auto"}

### Analytics y Adobe Target: Sincronización del ID de cliente {#section_AD473A6A21C1446498E700363F9A8437}

Como parte de la configuración del Servicio de Experience Cloud ID, Adobe recomienda (para Analytics y [!DNL Target]) que sincronice los [ID de cliente](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=es) con Experience Cloud.

En Adobe Target, `mbox3rdpartyid` debe obtener el ID de cliente y enviárselo a [!DNL Target]. (Consulte [Uso de Atributos del cliente](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html?lang=es) en [!DNL Target]).

Cuando un visitante se autentica en su sitio web o se identifica a sí mismo de otra manera, su implementación debe exponer el ID de cliente de CRM de esa persona a la página o aplicación. A continuación, puede utilizar la llamada de función adecuada para sincronizar su ID de cliente con Experience Cloud. Esta sincronización almacena el ID de cliente de CRM de visitante en Experience Cloud y activa los atributos del cliente para su uso en Experience Cloud.

Por ejemplo, suponga que el ID de cliente de Bob es `52mc210tr42` en su sistema CRM. Cuando Bob se autentifique en su sitio, debe mostrar este ID en la página y utilizar el ID para sincronizarlo de una de las dos formas siguientes:

* Llamar a `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` mediante el servicio de ID del visitante. O,
* Rellene la variable *`Customer ID (52mc210tr42)`* en una propiedad o eVar.

Se debe establecer el ID de cliente en cada llamada al servidor de [!DNL Analytics] cuando se conozca el ID de cliente.

#### Analytics: Sincronización del ID de cliente con el método de relleno de Data Warehouse

Cuando los Atributos del cliente aparecieron por primera vez, algunos clientes aún no habían implementado el servicio de ID de Experience Cloud y no podían utilizar fácilmente los Atributos del cliente. Para ayudar a aliviar este problema, Adobe ha creado un medio para rellenar las sincronizaciones de ID mediante la Data Warehouse de Adobe Analytics. Esta función se conoce como relleno de Data Warehouse. El relleno de Data Warehouse ahora generalmente no es necesario y, como resultado, ya no estará disponible a partir de octubre de 2022.


### SDK para móvil

Consulte la sección *Servicio de Experience Cloud ID* para ver ejemplos de sintaxis sobre cómo establecer ID de cliente adicionales en aplicaciones móviles de [Android™](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=es) e [iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=es).

### Activación de atributos para datos históricos

Los datos de atributos del cliente están disponibles después de que los visitantes inicien sesión. Si todavía no ha implementado el servicio de ID más reciente y ha estado realizando un seguimiento histórico de los ID de cliente en una prop o eVar, puede solicitar un proceso que envíe los inicios de sesión históricos a Experience Cloud. Este proceso le permite empezar a usar los Atributos del cliente inmediatamente.

Póngase en contacto con el Servicio de atención al cliente para habilitar los datos históricos.

## Asigne grupos de informes a una organización de Experience Cloud {#section_7B08516B01BA421681DF03D0E86CE3BA}

>[!NOTE]
>
>La funcionalidad de asignación de grupos de informes quedará obsoleta en noviembre de 2020. Póngase en contacto con Asistencia al cliente si tiene alguna pregunta.

Los servicios de Experience Cloud (como el Servicio de Experience Cloud ID y el [!UICONTROL servicio People]) están asociados a una organización de Experience Cloud en lugar de a un grupo de informes de Analytics individual. Para que estos servicios funcionen correctamente, cada grupo de informes de Analytics debe asignarse a una organización de Experience Cloud.

## Actualice el código de AppMeasurement para Analytics {#section_1798D9D0F05C47E29816AC4EEB9A0913}

Si utiliza Analytics, asegúrese de que esté en una recopilación de datos regionales (RDC). Si el dominio de recopilación de datos es `omtrdc.net`, o si el CNAME está asignado a `omtrdc.net`, usted se encuentra en RDC. Consulte [Transición a RDC](https://experienceleague.adobe.com/docs/analytics/technotes/rdc/regional-data-collection.html?lang=es) para obtener más información. Si utiliza cookies propias, consulte [CNAME y el servicio de Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html?lang=es) para obtener información sobre los CNAME de recopilación de datos y el seguimiento entre dominios.

Se le recomienda modernizar su implementación de Analytics mediante la actualización de sus bibliotecas de JavaScript, incluido el API de visitante. La manera más sencilla de lograrlo es agregar una [Extensión de Adobe Analytics](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=es) en Recopilación de datos de Experience Platform.

## Actualice la implementación de Adobe Target {#section_C2F4493C7A36406DAE2266B429A4BD24}

* Se recomienda agregar una variable [Extensión de Adobe Target](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target-v2/overview.html?lang=es) in [!UICONTROL Experience Platform] para que la recuperación de la biblioteca sea automática. También puede configurar el [Extensión del servicio de ID de Experience Cloud](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html?lang=es) para Adobe Target (y otras aplicaciones) con [!UICONTROL Experience Platform] etiquetas. El [!UICONTROL Servicio de ID de Experience Cloud] actualizar **es obligatorio** para que Adobe Target utilice los servicios Personas.
* Si no está utilizando [!UICONTROL Experience Platform] etiquetas, [actualizar la biblioteca de mbox](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/implement-target-for-client-side-web.html?lang=es) manualmente.
* Solicite el acceso para utilizar Adobe Analytics como el origen de generación de informes para [!DNL Adobe Target]. Los datos de [!DNL Target] y [!DNL Analytics] se combinan en la misma llamada de servidor durante el procesamiento para que los visitantes se conecten entre las dos aplicaciones. Consulte [Implementación de Analytics for Target](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=es).

  >[!IMPORTANT]
  >
  >Todos los clientes de Analytics ya se han aprovisionado de servicios principales como los Atributos del cliente. Si no es cliente de Analytics, póngase en contacto con la atención al cliente para solicitar que se le aprovisione.

## Verificar la implementación {#section_E641782A0F4F44AF8C9C91216BE330D5}

Realice el siguiente proceso para asegurarse de que el Servicio de ID de Experience Cloud se implementa correctamente en el sitio.

1. Borre las cookies de su sitio para poder ver la solicitud al Servicio de Experience Cloud ID (la solicitud se realiza en la primera visita y, a continuación, una vez por visitante y semana).
1. Con la ayuda de un analizador de paquetes o el panel de red en un depurador de explorador web, busque una solicitud que se dirija a [!DNL dpm.demdex.net].
1. Compruebe que la respuesta contenga `d_mid` y un valor, por ejemplo: `_setMarketingCloudFields({"d_mid":"4235...`
1. Compruebe que la solicitud de Analytics contiene el parámetro `mid` (Experience Cloud ID). Durante el periodo de gracia (si está activado), también debería ver un parámetro `aid` (el ID de visitante de Analytics).

Respuesta esperada que contiene el Experience Cloud ID:

![Respuesta esperada que contiene el Experience Cloud ID](assets/mac_id_response.png)

Solicitud de imagen de Analytics que contiene el Experience Cloud ID (también conocido como `mid` o _ID de visitante_):

![Solicitud de imagen de Analytics que contiene el Experience Cloud ID](assets/mid.png)

Experience Cloud ID en la solicitud de mbox:

![Experience Cloud ID en la solicitud de mbox](assets/mbox_request.png)

### ¿Qué es el periodo de gracia?

Una vez que haya implementado el Servicio de Experience Cloud ID, el servidor de recopilación de datos ya no asignará a los visitantes nuevos un ID de visitante de Analytics Experience Cloud. Si hay secciones de su sitio que todavía no hayan implementado el Servicio de ID, cuando los visitantes accedan a ellas, el Experience Cloud ID no se reconocerá y se asignará un ID de visitante de Analytics heredado a los visitantes. Esto puede causar problemas potenciales, como visitas duplicadas y atribución incorrecta.

Por ejemplo: Si la sección de asistencia técnica de su sitio se administra en un CMS independiente, puede tener un archivo JavaScript de Analytics diferente para esta sección. Si implementa Experience Cloud ID en el sitio principal antes de implementar el servicio de ID en el sitio de asistencia, los nuevos visitantes recibirán un ID de Analytics heredado cuando visiten la sección de asistencia y las visitas que abarquen ambas secciones del sitio se registrarán como visitas diferentes.

La implementación del Servicio de Experience Cloud ID en sitios que utilicen varios archivos JavaScript u otras tecnologías (como Flash) puede causar problemas de coordinación. Estos problemas se producen porque debe habilitar el Servicio de Experience Cloud ID en todas las áreas del sitio al mismo tiempo. Si configura un período de gracia, se seguirá asignando un ID de visitante de Analytics a los nuevos visitantes, de manera que estos se puedan identificar de manera sistemática en las secciones del sitio que todavía no utilicen el servicio de ID de visitante.

## Administración de usuarios y productos {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Una vez que esté en funcionamiento, vaya a [Admin Console](https://adminconsole.adobe.com/), donde puede administrar usuarios y perfiles de producto.

![Acceso a Admin Console](assets/menu-administration-shell.png)

Consulte [Administración de usuarios y productos de Experience Cloud](admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909).

### Atributos del cliente

Los usuarios que se agregan al grupo [!UICONTROL Atributos del cliente] pueden ver el elemento de menú [!UICONTROL Atributos del cliente] a la izquierda de Experience Cloud.

## Iniciar el uso compartido de datos de atributos y públicos {#section_960C06093623462E8EA247B3E97274A1}

Aproveche las siguientes funciones.

### [!UICONTROL People] > [!UICONTROL Atributos del cliente]

Si captura los datos del cliente empresarial en una base de datos de administración de la relación con los clientes (CRM), podrá cargar los datos en una fuente de datos de atributos del cliente en Experience Cloud. Una vez cargados, use los datos en [!DNL Adobe Analytics] y [!DNL Adobe Target].

Consulte [Atributos del cliente](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

### [!UICONTROL People] > [!UICONTROL Biblioteca de públicos]

[!UICONTROL Públicos] de Experience Cloud es la interfaz que le permite crear públicos, combinar públicos existentes para crear públicos compuestos y ver todos los públicos compartidos.

Consulte [Públicos](audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

## Almacenamiento de datos y revelación de información privada

Si utiliza los servicios de perfil de público en tiempo real y otros servicios principales en Adobe [!DNL Experience Cloud], el uso de estos servicios podría determinar en qué centro (y en qué país) se alojan los datos. Específicamente, como [!DNL Experience Cloud] usa Audience Manager, los datos utilizados dentro del servicio [!UICONTROL People] deben residir en servidores de Audience Manager en Estados Unidos.

Al utilizar los servicios disponibles mediante el servicio [!UICONTROL People], los tipos de datos enviados desde otros productos de Adobe a la gestión de público son los siguientes:

* Pares de clave/valor de [!DNL Analytics] (props, eVars, list vars, etc.). De forma predeterminada, las líneas de registro incluyen direcciones IP, con el último octeto de la dirección IP (suponiendo que esta no fue modificada por la configuración de confusión de IP dentro de Adobe [!DNL Analytics]).
* Características y segmentos para los que los visitantes cumplen los requisitos según las reglas configuradas en Audience Manager.
* (Opcional) Uno o más de sus ID. Según la implementación del servicio de ID, también podría estar enviando uno o más de sus ID, como ID de CRM o direcciones de correo electrónico con hash. Si estos datos se envían a Adobe [!DNL Analytics], se transfieren a la gestión de público de Adobe. Adobe recomienda no proporcionar datos personales a Adobe [!DNL Analytics]. En lugar de ello, use un hash unidireccional para cifrar los datos antes de enviarlos a Adobe.
* Segmentos que se originan en [!DNL Analytics] mediante la función de uso compartido de segmentos del back-end.
* Se instala la cookie de demdex.net si no están bloqueadas las cookies de terceros. La cookie propia `AMCV_###@AdobeOrg` siempre se instala con el Servicio de Experience Cloud ID.

Todos estos elementos de datos se entregan a Adobe Audience Manager en forma de archivos de registro. Audience Manager procesa y almacena estos datos dentro de Estados Unidos. Audience Manager no proporciona una opción para almacenar o procesar estos datos fuera de Estados Unidos.

### Cookies y no participaciones

El uso de perfil de audiencia en tiempo real usa la cookie de Audience Manager, además de las cookies utilizadas para [!DNL Analytics] y [!DNL Target].

Si desea proporcionar la capacidad adecuada de no participación, los visitantes del sitio deben agregar la no participación de Audience Manager a sus procesos de no participación actuales.

Consulte [Adobe Experience Cloud: Implementación de exclusiones de Adobe](https://experienceleague.adobe.com/docs/analytics/implementation/js/opt-out.html?lang=es) para obtener instrucciones detalladas.

Consulte [CNAME de recopilación de datos y seguimiento entre dominios](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html?lang=es) para habilitar el seguimiento entre dominios.
