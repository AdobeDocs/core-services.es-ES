---
title: Preferencias y notificaciones de cuenta
description: Obtenga información sobre los perfiles de usuario, las preferencias de cuenta y los datos de uso del producto en CX Enterprise. Suscríbase a las notificaciones de productos para correo electrónico y  [!DNL Slack], y configure alertas de productos.
solution: Experience Cloud
feature: Account Preferences, Notifications, Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 1e34c6b2-a792-41c4-adb7-583de596237f
TQID: https://experienceleague.adobe.com/2IL6hUlA1oNxJIFMwbVQUbxEGkJoghVUTyMi5wSRBsE
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: e1eba07e-ab89-466f-9ab5-ceb891d7a67d
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: bdea9bc8-5600-45db-b85e-d74bb59dfcff
  - id: dc42f745-24d2-44a4-99c3-dece518fa4bc
  - id: eaef3029-0844-43fe-9e1c-7666a24f4d03
  - id: eb1ae5c4-ef16-4998-851c-73cc9f0b7f06
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 802
ht-degree: 5%

---

# Preferencias y notificaciones de la cuenta

Para encontrar las preferencias de CX Enterprise, haga clic en **[!UICONTROL Profile]** ![preferencias](../assets/preferences-icon-sm.png) en el encabezado y luego haga clic en **[!UICONTROL Preferences]**.

![preferencias](../assets/preferences-navigation.png){width="100" zoomable="yes"}

En la página [!UICONTROL CX Enterprise preferences], puede administrar las siguientes características de la cuenta:

| Función | Descripción |
| --- | --- |
| [!UICONTROL Profile] | Actualice su [perfil de cuenta de Adobe](https://account.adobe.com/profile). <p>La fotografía y el nombre de su perfil aparecen al iniciar sesión en Adobe.com, en los productos y servicios de Adobe y en sitios públicos como [!DNL Behance]. |
| [!UICONTROL General] | Seleccione una [organización](../administration/organizations.md).<p>Esta organización es la predeterminada que se utiliza al iniciar sesión en CX Enterprise. |
| [!UICONTROL Product usage data] | Puede controlar qué datos de uso del producto se comparten con Adobe al utilizar aplicaciones de CX Enterprise. Se trata de datos sobre cómo utiliza nuestros productos, no del contenido de su organización ni de los propios datos. Adobe utiliza esta información para ayudar a mejorar nuestros productos, proporcionarle un soporte mejorado del producto y personalizar su experiencia y comunicaciones con nosotros. <p>Para obtener más información, consulte [Datos de uso del producto](#product-usage-data) (en esta página). |
| [!UICONTROL Notifications] | Configure cómo y cuándo desea las [notificaciones](#subscribe-to-notifications-in-experience-cloud) y alertas del producto: <ul><li>Seleccione los productos a los que desea suscribirse para recibir alertas</li><li>Configurar el tipo de notificación ([!UICONTROL in-app], [!UICONTROL email] o [Slack](#slack-notifications))</li><li>Especifique la frecuencia con la que desea recibir los correos electrónicos de notificación. (No enviado, instantáneo, diario o semanal).</li><li>Determine la prioridad de la alerta. Las alertas en la aplicación aparecen en la esquina superior derecha de la ventana durante unos segundos. O bien, puede especificar si las alertas deben mostrarse hasta que las descarte.</li></ul> |

## [!UICONTROL Product usage data]

Los datos de uso del producto que decide compartir con Adobe incluyen los siguientes tipos de información sobre cómo utiliza e interactúa con las aplicaciones de Adobe:

* Información del explorador y del dispositivo, como el modelo del dispositivo y el sistema operativo, información de software y hardware, configuración del explorador y del dispositivo, identificadores únicos (como la dirección IP, el ID de cookie o el ID del dispositivo), cantidad de memoria instalada, configuración de idioma y resolución de pantalla.
* Cómo interactúa con las aplicaciones de Adobe CX Enterprise, incluidas las funciones que utiliza y las opciones que selecciona;
* información del producto de Adobe, como el número de versión;
* Información sobre el contenido y los documentos, como el número de páginas y los identificadores únicos, pero no el contenido en sí;
* Información de uso del contenido, como cuántas veces accede al contenido y cómo interactúa con el contenido dentro de la aplicación.
* Registros de errores y bloqueos.

Adobe utiliza esta información para ayudar a mejorar nuestros productos, proporcionarle asistencia tanto en el producto como a través del servicio de atención al cliente, y para personalizar su experiencia y comunicaciones con nosotros. Más información sobre [experiencias personalizadas](personalized-learning.md).

## Suscripción a notificaciones en CX Enterprise

Puede seleccionar los productos y las categorías a los que desea suscribirse. Las notificaciones aparecen en la ventana emergente [!UICONTROL Notifications] (en la aplicación), en tu correo electrónico o en [Slack](#slack-notifications) (según tus suscripciones).

Las notificaciones por correo electrónico y Slack son útiles cuando no ha iniciado sesión en CX Enterprise.

### Suscripción a notificaciones en la aplicación y por correo electrónico

1. Vaya a CX Enterprise [preferencias](https://experience.adobe.com/preferences).

1. En **[!UICONTROL Notifications]**, habilite **[!UICONTROL In-app]** o **[!UICONTROL Email]**.

   Los cambios en las notificaciones se guardan automáticamente.

### Suscribirse a [!DNL Slack] notificaciones

Puede configurar las preferencias de su cuenta para enviar notificaciones de CX Enterprise a un canal [!DNL Slack].

**Requisitos previos**

* Debe tener una cuenta de CX Enterprise.
* Debe tener una cuenta de [!DNL Slack]. Su administrador de [!DNL Slack] habilita la integración de CX Enterprise con [!DNL Slack].
* Debe formar parte de al menos un espacio de trabajo de [!DNL Slack].

**Para suscribirse a [!DNL Slack] notificaciones**

1. Vaya a [Preferencias](https://experience.adobe.com/preferences) de CX Enterprise.

1. Busque [!DNL Slack] y haga clic en **[!UICONTROL Add to Slack]**.

   ![Agregar a Slack](../assets/add-to-slack.png)

   Si [!DNL Slack] está instalado, la aplicación se abrirá y aparecerá un mensaje de solicitud de permiso. Si Slack no está instalado, debe [solicitar permiso](#slack-troubleshoot).

1. Haga clic en **[!UICONTROL Allow]**.

1. En **[!UICONTROL Notifications]**, habilite [!DNL Slack] notificaciones para los productos y las categorías que desee.

   ![Notificaciones de Slack](../assets/slack.png)

   Las actualizaciones de las notificaciones se guardan automáticamente.

### Solicitar permiso en [!DNL Slack] (solución de problemas)

Si [!DNL Slack] no está instalado, aparecerá un mensaje _[!UICONTROL Request to install]_&#x200B;cuando Slack se abra después de hacer clic en **[!UICONTROL Add to Slack]**. Por ejemplo:

![Solicitar integración de Slack](../assets/slack-workspace.png)

**Para solicitar permisos en Slack**

1. En [!DNL Slack], seleccione el área de trabajo en el menú **[!UICONTROL Workspace]** (esquina superior derecha).

1. Para solicitar la aprobación de la aplicación para el administrador de área de trabajo [!DNL Slack], haga clic en **[!UICONTROL Submit]**.

1. Recibirá una notificación en [!DNL Slack] después de que se apruebe la solicitud de la aplicación.

1. Después de recibir la aprobación de [!DNL Slack], vuelva a CX Enterprise **[!UICONTROL Notifications]** y siga los pasos para [suscribirse a Slack](#slack-notifications) (descritos anteriormente).

### Lo que verá en [!DNL Slack]

Después de integrar correctamente [!DNL Slack], las notificaciones de [!DNL Slack] muestran la siguiente información:

* El mensaje personal se recibirá del nombre de la aplicación _Adobe[!DNL CX Enterprise]_.
* El mensaje incluye el logotipo del producto para la aplicación en particular, como Adobe [!DNL Experience Platform], Adobe [!DNL Experience Manager], etc.
* Un enlace para ver todas las notificaciones en CX Enterprise.
* Un vínculo para administrar las preferencias de notificación en CX Enterprise.

## Ver [!UICONTROL notifications] y anuncios en CX Enterprise

En el encabezado [!DNL CX Enterprise], puede ver las notificaciones a las que se ha [suscrito](#notifications), así como los anuncios.

1. Haga clic en el icono de campana del encabezado. ![Notificaciones y anuncios](../assets/bell-icon.png)

1. Haga clic **[!UICONTROL Notifications]** o **[!UICONTROL Announcements]**.

   En esta ubicación recibirá información importante sobre los productos, su colaboración con otros usuarios y otras actualizaciones relevantes. Las actualizaciones incluyen versiones de productos, avisos de mantenimiento, elementos compartidos y solicitudes de aprobación.

