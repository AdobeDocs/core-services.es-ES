---
description: Modernice sus aplicaciones de Adobe Analytics y Adobe Target para servicios entre aplicaciones. Aprenda a empezar a utilizar los servicios empresariales de CX.
solution: Experience Cloud
title: Introducción a los servicios de Experience Cloud
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: 48e79e23-b339-4143-b3b1-969c370efeff
TQID: https://experienceleague.adobe.com/5SyRdqyQkymJJygKeQ9FXIYoVe70br51DY2VKmqSC0E
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: dab36b01-8bfa-48f3-8392-626455a058e6id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: bdea9bc8-5600-45db-b85e-d74bb59dfcffid: d27b1945-f442-4607-91bd-537a0b16e687id: eb7e29b9-c5e9-4ed0-8e4b-6465dabb3cb1id: ecb4a972-6786-444c-a014-abc528b9407aid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7bfc22e90d727d1743c2b6b7bc645033d5d38f1b
workflow-type: tm+mt
source-wordcount: 2083
ht-degree: 40%

---

# Introducción a CX Enterprise

Si ha implementado recientemente CX Enterprise con [Experience Platform tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home), ya ha configurado [Atributos del cliente](../services/overview.md) y CX Enterprise [Audiences](../services/audiences/overview.md). También puede administrar usuarios y productos en [Admin Console](../administration/admin-console.md).

Los clientes existentes pueden modernizar las implementaciones de sus aplicaciones e implementar CX Enterprise. Al hacerlo, puede usar los atributos del cliente y las funciones de Audiencia en Adobe Analytics, Audience Manager y Adobe Target.

## Iniciar sesión como administrador {#admin-sign-in}

Una vez que sea administrador, podrá iniciar sesión en [experiencecloud.adobe.com](https://experience.adobe.com).

El vínculo **[!UICONTROL Admin Console]** está disponible en el menú de navegación de CX Enterprise para administrar usuarios y licencias de productos.

### Opcional: Vincule las cuentas de usuario existentes {#link-accounts}

Lo más probable es que tenga usuarios que ya sean miembros de grupos de aplicaciones, como un grupo de Analytics que haya administrado anteriormente en [!UICONTROL Analytics] > [!UICONTROL Herramientas de administración].

Al asignar estos grupos a grupos empresariales de CX, estos usuarios deben vincular manualmente sus credenciales de cuenta de la aplicación a su Adobe ID.

Ver [Vincular cuentas en CX Enterprise](https://experienceleague.adobe.com/es/docs/core-services/interface/administration/organizations)

>[!NOTE]
>
>Una vez asignados los grupos de aplicaciones y de empresa, los nuevos usuarios se vinculan automáticamente. (Las credenciales de la solución se crean automáticamente y se vinculan a su Adobe ID).

Las siguientes secciones describen cómo modernizar la implementación. La modernización de la implementación habilita los servicios principales en CX Enterprise.

## Iniciar sesión como usuario {#user-sign-in}

Para iniciar sesión en CX Enterprise, los usuarios deben:

* Tener un Adobe ID (o Enterprise ID para su compañía).
* Iniciar sesión en [experiencecloud.adobe.com](https://experience.adobe.com).
* Pertenecer a un grupo de aplicaciones asignado a un grupo de empresas.
* Si es necesario, vincule sus cuentas de aplicaciones a su Adobe ID (descrito a continuación).

## Requisitos de Adobe Analytics y Adobe Target para CX Enterprise {#experience-cloud-requirements}

Requisitos de [!DNL Analytics] y [!DNL Adobe Target] para usar CX Enterprise:

1. Asegúrese de que cuenta con los SKU correspondientes de Adobe Analytics o Adobe Target.

   * **Adobe Analytics:** Standard o Premium (no el SKU de [!DNL SiteCatalyst] heredado).
   * **Adobe Target:** Standard o Premium.

     >[!NOTE]
     >
     >Para [!DNL Target], migre a at.js desde `mbox.js`. Ver [Actualización de at.js 1. x a at.js 2. x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/upgrading-from-atjs-1x-to-atjs-20.html?lang=es).

1. [Administrar usuarios y productos](../administration/admin-console.md) en [!UICONTROL Admin Console].

**Relacionado:** [Analytics y Target: Sincronizar los ID de cliente](#sync-ids) (en esta página)

## Implementación del servicio de ID de visitante

El servicio de ID de visitante proporciona un ID común para la integración entre aplicaciones. Proporciona identificación de visitantes entre dominios y una ruta para la segmentación y personalización entre dispositivos y exploradores en función de los datos de CRM cargados a través de [!DNL Customer Attributes].

El método más sencillo para activar los servicios principales de CX Enterprise es activarlos automáticamente para Analytics y Adobe Target mediante la extensión de etiquetas [[!UICONTROL Experience Cloud ID Service]](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html), que implementa el servicio de ID de visitante.

Para obtener la ayuda completa del Servicio de ID de visitante, consulte [Introducción al Servicio de ID de visitante](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html#intro).


**No se están usando las [!UICONTROL etiquetas Experience Platform]?**

Si no usa [!UICONTROL Experience Platform tags], implemente manualmente el servicio de ID de visitante mediante la implementación de JavaScript (`VisitorAPI.js`), de la siguiente manera:

| Tarea | Descripción |
| --- | --- |
| [Implementar el servicio de identificación de visitante (`VisitorAPI.js`) para Analytics](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/overview) | Adobe también recomienda configurar algunos [ID de cliente](https://experienceleague.adobe.com/en/docs/id-service/using/reference/authenticated-state) adicionales. Estos ID se asocian con cada visitante para activar las funciones actuales y futuras en CX Enterprise. |
| Actualice el `s_code` existente a la versión H.27.3 o posterior, o su `AppMeasurement.js` existente a la versión 1.4 o posterior. | Estos archivos están disponibles para su descarga en el [Administrador de códigos](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html) de las herramientas de administración de Analytics. (La guía de [implementación de JavaScript](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview#js) está disponible si necesita más información sobre `AppMeasurement.js`). |

### Analytics y Adobe Target: Sincronización de ID de cliente {#sync-ids}

Como parte de la configuración del servicio de ID de visitante, Adobe recomienda (para Analytics y [!DNL Target]) que sincronice los [ID de cliente](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) con CX Enterprise.

En Adobe Target, `mbox3rdpartyid` debe obtener el ID de cliente y enviárselo a [!DNL Target]. (Consulte [Uso de Atributos del cliente](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html?lang=es) en [!DNL Target]).

Cuando un visitante se autentica en su sitio web o se identifica a sí mismo de otra manera, su implementación debe exponer el ID de cliente de CRM de esa persona a la página o aplicación. A continuación, puede utilizar la llamada de función adecuada para sincronizar su ID de cliente con CX Enterprise. Esta sincronización almacena el ID de cliente de CRM de visitante en CX Enterprise y activa los atributos de cliente para su uso en CX Enterprise.

Por ejemplo, suponga que el ID de cliente de Bob es `52mc210tr42` en su sistema CRM. Cuando Bob se autentifique en su sitio, debe mostrar este ID en la página y utilizar el ID para sincronizarlo de una de las dos formas siguientes:

* Llamar a `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` mediante el servicio de ID de visitante. O,
* Rellene la variable *`Customer ID (52mc210tr42)`* en una propiedad o eVar.

Se debe establecer el ID de cliente en cada llamada al servidor de [!DNL Analytics] cuando se conozca el ID de cliente.

#### Analytics: sincronización del ID de cliente con el método de relleno de Data Warehouse

Cuando los Atributos del cliente aparecieron por primera vez, algunos clientes aún no habían implementado el Servicio de ID de visitante y no podían utilizar fácilmente los Atributos del cliente. Para ayudar a resolver este problema, Adobe ha creado un medio para rellenar las sincronizaciones de ID mediante Data Warehouse de Adobe Analytics. Esta función se conoce como relleno de Data Warehouse. Ahora, el relleno de Data Warehouse no suele ser necesario, por lo que se dejó de utilizar en octubre de 2022.

### SDK para móvil

Consulte la sección *Servicio de ID de visitante* para ver ejemplos de sintaxis sobre cómo establecer ID de cliente adicionales en las aplicaciones móviles de [Android™](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=es) y [iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=es).

### Habilitar atributos para datos históricos

Los datos de atributos del cliente están disponibles después de que los visitantes inicien sesión. Si todavía no ha implementado el servicio de ID de visitante y ha estado realizando un seguimiento histórico de los ID de cliente en una propiedad o eVar, puede solicitar un proceso que envíe los inicios de sesión históricos a CX Enterprise. Este proceso le permite empezar a usar los Atributos del cliente inmediatamente.

Póngase en contacto con Asistencia para habilitar los datos históricos.

## Actualice el código de AppMeasurement para Analytics

Si usa cookies de origen, consulte el [programa de certificados administrados por Adobe](/help/interface/data-collection/adobe-managed-cert.md) para obtener información sobre los CNAME de recopilación de datos y el seguimiento entre dominios.

Se le recomienda modernizar su implementación de Analytics mediante la actualización de sus bibliotecas de JavaScript, incluido el API de visitante. La manera más sencilla de lograrlo es añadir una [extensión de Adobe Analytics](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html) en la recopilación de datos de Experience Platform.

## Actualice la implementación de Adobe Target

* Se recomienda agregar una [extensión de Adobe Target](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target-v2/overview.html) en las etiquetas [!UICONTROL Experience Platform] para que la recuperación de la biblioteca sea automática. También puede configurar la extensión de etiquetas [[!UICONTROL Experience Cloud ID Service]](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html), que implementa el servicio de ID de visitante para Adobe Target (y otras aplicaciones) mediante etiquetas. Esta extensión de etiqueta es **obligatoria** para que Adobe Target use los servicios Personas.
* Si no usas las etiquetas [!UICONTROL Experience Platform], [actualiza tu biblioteca mbox](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/implement-target-for-client-side-web.html) manualmente.
* Solicite el acceso para utilizar Adobe Analytics como el origen de generación de informes para [!DNL Adobe Target]. Los datos de [!DNL Target] y [!DNL Analytics] se combinan en la misma llamada de servidor durante el procesamiento para que los visitantes se conecten entre las dos aplicaciones. Consulte [Implementación de Analytics for Target](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html).

  >[!IMPORTANT]
  >
  >Todos los clientes de Analytics ya se han aprovisionado de servicios principales como los Atributos del cliente. Si no es cliente de Analytics, póngase en contacto con la atención al cliente para solicitar que se le aprovisione.

## Verificar la implementación

Realice el siguiente proceso para asegurarse de que el servicio de ID de visitante se implementa correctamente en el sitio.

1. Borre las cookies de su sitio para poder ver la solicitud al Servicio de ID de visitante (la solicitud se realiza en la primera visita y, a continuación, una vez por visitante y semana).
1. Con la ayuda de un analizador de paquetes o el panel de red en un depurador de explorador web, busque una solicitud que se dirija a [!DNL dpm.demdex.net].
1. Compruebe que la respuesta contenga `d_mid` y un valor, por ejemplo: `_setMarketingCloudFields({"d_mid":"4235...`
1. Compruebe que la solicitud de Analytics contiene el parámetro `mid` (el ECID). Durante el periodo de gracia (si está habilitado), también debería ver un parámetro `aid` (el ID de visitante de Analytics).

Respuesta esperada que contiene el ECID:

![Respuesta esperada que contiene el ECID](../assets/mac_id_response.png)

Solicitud de imagen de Analytics que contiene el ECID (también conocido como `mid` o _ID de visitante_):

![Solicitud de imagen de Analytics que contiene el ECID](../assets/mid.png)

ECID en la solicitud de mbox:

![ECID en la solicitud de mbox](../assets/mbox_request.png)

### ¿Qué es el periodo de gracia?

Una vez que haya implementado el Servicio de ID de visitante, los nuevos visitantes ya no recibirán un ID de Analytics (`aid`). Si hay secciones de su sitio que todavía no hayan implementado el Servicio de ID de visitante, cuando los visitantes accedan a ellas, el ECID (`mid`) no se reconocerá y se asignará un ID de Analytics heredado (`aid`) a los visitantes. Esta configuración puede causar posibles problemas, como visitas duplicadas y atribución incorrecta.

Por ejemplo: Si la sección de asistencia técnica de su sitio se administra en un CMS independiente, puede tener un archivo JavaScript de Analytics diferente para esta sección. Si implementa el ECID en el sitio principal antes de implementar el servicio de ID de visitante en el sitio de asistencia, los nuevos visitantes recibirán un ID de Analytics heredado cuando visiten la sección de asistencia. Las visitas que abarcan ambas secciones del sitio se registran como visitas diferentes.

La implementación del servicio de ID de visitante en sitios que utilicen varios archivos JavaScript u otras tecnologías (como Flash) puede producir problemas de coordinación. Estos problemas se producen porque debe habilitar el Servicio de ID de visitante en todas las áreas del sitio al mismo tiempo. Si configura un período de gracia, se seguirá asignando un ID de visitante de Analytics a los nuevos visitantes, a fin de que puedan seguir recibiendo ese ID desde el servicio de ID de visitante. Los visitantes se pueden identificar de forma consistente en las secciones del sitio que no se han actualizado para utilizar el servicio de ID de visitante.

## Administración de usuarios y productos

Una vez que esté en funcionamiento, vaya a [Admin Console](https://adminconsole.adobe.com/), donde puede administrar usuarios y perfiles de producto.

![Acceso a Admin Console](../assets/menu-administration-shell.png)

### Atributos del cliente

Los usuarios que se agregan al grupo [!DNL Customer Attributes] pueden ver el elemento de menú [!DNL Customer Attributes] a la izquierda de CX Enterprise.

## Iniciar el uso compartido de datos de atributos y públicos

Aproveche las siguientes funciones.

### [!UICONTROL Atributos del cliente]

Si captura los datos del cliente empresarial en una base de datos de administración de la relación con los clientes (CRM), podrá cargar los datos en una fuente de datos de atributos del cliente en CX Enterprise. Una vez cargados, use los datos en [!DNL Adobe Analytics] y [!DNL Adobe Target].

Consulte [Atributos del cliente](https://experienceleague.adobe.com/en/docs/core-services/interface/services/customer-attributes/attributes) para obtener más información.

### [!UICONTROL Personas] > [!UICONTROL Biblioteca de audiencias]

CX Enterprise [!UICONTROL Audiences] es la interfaz que le permite crear audiencias, combinar audiencias existentes para crear audiencias compuestas y ver todas las audiencias compartidas.

Consulte [Audiencias](https://experienceleague.adobe.com/es/docs/core-services/interface/services/audiences/overview) para obtener más información.

## Almacenamiento de datos y revelación de información privada

Si utiliza los servicios de perfil de público en tiempo real y otros servicios principales en Adobe [!DNL CX Enterprise], el uso de estos servicios podría determinar en qué centro (y en qué país) se alojan los datos. En concreto, como [!DNL CX Enterprise] utiliza Audience Manager, los datos utilizados en el servicio [!UICONTROL People] deben residir en servidores de Audience Manager en Estados Unidos.

Al utilizar los servicios disponibles mediante el servicio [!UICONTROL People], los tipos de datos enviados desde otros productos de Adobe a la gestión de público son los siguientes:

* Pares de clave/valor de [!DNL Analytics] (props, eVars, list vars, etc.). De forma predeterminada, las líneas de registro incluyen direcciones IP, con el último octeto de la dirección IP (suponiendo que esta no fue modificada por la configuración de confusión de IP dentro de Adobe [!DNL Analytics]).
* Características y segmentos para los que los visitantes cumplen los requisitos según las reglas configuradas en Audience Manager.
* (Opcional) Uno o más de sus ID. Según la implementación del Servicio de ID de visitante, también podría enviar uno o más de sus ID, como ID de CRM o direcciones de correo electrónico con hash. Si estos datos se envían a Adobe Analytics, se transfieren a Adobe Audience Manager. Adobe recomienda no proporcionar datos personales a Adobe Analytics. En lugar de ello, use un hash unidireccional para cifrar los datos antes de enviarlos a Adobe.
* Segmentos que se originan en [!DNL Analytics] mediante la función de uso compartido de segmentos del back-end.
* La cookie `demdex.net` se establece si las cookies de terceros no están bloqueadas. La cookie de origen `AMCV_###@AdobeOrg` siempre se establece con el servicio de ID de visitante.

Todos estos elementos de datos se entregan a Adobe Audience Manager en forma de archivos de registro. Audience Manager procesa y almacena estos datos dentro de Estados Unidos. Audience Manager no proporciona una opción para almacenar o procesar estos datos fuera de Estados Unidos.
