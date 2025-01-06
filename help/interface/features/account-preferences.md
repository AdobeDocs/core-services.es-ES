---
title: Preferencias y notificaciones de cuenta
description: Obtenga información acerca de los perfiles de usuario, las preferencias de cuenta y los datos de uso del producto en Experience Cloud. Suscríbase a las notificaciones de productos para correo electrónico y  [!DNL Slack], y configure alertas de productos.
solution: Experience Cloud
feature: Account Preferences, Notifications, Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 1e34c6b2-a792-41c4-adb7-583de596237f
source-git-commit: eddbda54bc3f1cbbc98d7a993d0b477e05c5b01c
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 3%

---

# Preferencias y notificaciones de cuenta {#preferences}

Para encontrar las preferencias de Experience Cloud, haz clic en **[!UICONTROL Perfil]** ![preferencias](../assets/preferences-icon-sm.png) en el encabezado y luego haz clic en **[!UICONTROL Preferencias]**.

![preferencias](../assets/preferences-navigation.png){width="100" zoomable="yes"}

En la página [!UICONTROL preferencias de Experience Cloud], puede administrar las siguientes características de la cuenta:

| Función | Descripción |
|--- |--- |
| [!UICONTROL Perfil] | Actualice su [perfil de cuenta de Adobe](https://account.adobe.com/profile). <p>La fotografía y el nombre del perfil aparecen al iniciar sesión en Adobe.com, productos y servicios de Adobe y en sitios públicos como [!DNL Behance]. |
| [!UICONTROL General] | Seleccione una [organización](../administration/organizations.md).<p>Esta organización es la predeterminada que se utiliza al iniciar sesión en Experience Cloud. |
| [!UICONTROL Datos de uso del producto] | Puede controlar qué datos de uso del producto se comparten con el Adobe al utilizar aplicaciones de Experience Cloud. Se trata de datos sobre cómo utiliza nuestros productos, no del contenido de su organización ni de los propios datos. Adobe utiliza esta información para ayudar a mejorar nuestros productos, proporcionarle un soporte mejorado del producto y personalizar su experiencia y comunicaciones con nosotros. <p>Para obtener más información, consulte [Datos de uso del producto](#product-usage-data) (en esta página). |
| [!UICONTROL Notificaciones] | Configure cómo y cuándo desea las [notificaciones](#subscribe-to-notifications-in-experience-cloud) y alertas del producto: <ul><li>Seleccione los productos a los que desea suscribirse para recibir alertas</li><li>Configure el tipo de notificación ([!UICONTROL en la aplicación], [!UICONTROL correo electrónico] o [Slack](#slack-notifications))</li><li>Especifique la frecuencia con la que desea recibir los correos electrónicos de notificación. (No enviado, instantáneo, diario o semanal).</li><li>Determine la prioridad de la alerta. Las alertas en la aplicación aparecen en la esquina superior derecha de la ventana durante unos segundos. O bien, puede especificar si las alertas deben mostrarse hasta que las descarte.</li></ul> |

## [!UICONTROL Datos de uso del producto] {#product-usage-data}

Los datos de uso del producto que decide compartir con Adobe incluyen los siguientes tipos de información sobre cómo utiliza e interactúa con las aplicaciones de Adobe:

* Información del explorador y del dispositivo, como el modelo del dispositivo y el sistema operativo, información de software y hardware, configuración del explorador y del dispositivo, identificadores únicos (como la dirección IP, el ID de cookie o el ID del dispositivo), cantidad de memoria instalada, configuración de idioma y resolución de pantalla.
* Cómo interactúa con las aplicaciones de Adobe Experience Cloud, incluidas las funciones que utiliza y las opciones que selecciona;
* información del producto de Adobe, como el número de versión;
* Información sobre el contenido y los documentos, como el número de páginas y los identificadores únicos, pero no el contenido en sí;
* Información de uso del contenido, como cuántas veces accede al contenido y cómo interactúa con el contenido dentro de la aplicación.
* Registros de errores y bloqueos.

Adobe utiliza esta información para ayudar a mejorar nuestros productos, proporcionarle asistencia tanto en el producto como a través del servicio de atención al cliente, y para personalizar su experiencia y comunicaciones con nosotros. Más información sobre [experiencias personalizadas](personalized-learning.md).

## Suscripción a notificaciones en Experience Cloud {#notifications}

Puede seleccionar los productos y las categorías a los que desea suscribirse. Las notificaciones aparecen en la ventana emergente [!UICONTROL Notificaciones] (en la aplicación), en tu correo electrónico o en [Slack](#slack-notifications) (según tus suscripciones).

Las notificaciones por correo electrónico y al Slack son útiles en situaciones en las que no ha iniciado sesión en Experience Cloud.

### Suscripción a notificaciones en la aplicación y por correo electrónico

1. Vaya al Experience Cloud [preferencias](https://experience.adobe.com/preferences).

1. En **[!UICONTROL Notificaciones]**, habilite **[!UICONTROL En la aplicación]** o **[!UICONTROL Correo electrónico]**.

   Los cambios en las notificaciones se guardan automáticamente.

### Suscribirse a [!DNL Slack] notificaciones {#slack}

Puede configurar las preferencias de su cuenta para enviar notificaciones al Experience Cloud a un canal [!DNL Slack].

**Requisitos previos**

* Debe tener una cuenta de Experience Cloud.
* Debe tener una cuenta de [!DNL Slack]. El administrador de [!DNL Slack] habilita la integración del Experience Cloud con [!DNL Slack].
* Debe formar parte de al menos un espacio de trabajo de [!DNL Slack].

**Para suscribirse a [!DNL Slack] notificaciones**

1. Vaya al Experience Cloud [Preferencias](https://experience.adobe.com/preferences).

1. Busque [!DNL Slack] y haga clic en **[!UICONTROL Agregar al Slack]**.

   ![Agregar al Slack](../assets/add-to-slack.png)

   Si [!DNL Slack] está instalado, la aplicación se abrirá y aparecerá un mensaje de solicitud de permiso. Si Slack no está instalado, debe [solicitar permiso](#slack-troubleshoot).

1. Haga clic en **[!UICONTROL Permitir]**.

1. En **[!UICONTROL Notificaciones]**, habilite [!DNL Slack] notificaciones para los productos y categorías que desee.

   ![Notificaciones al Slack](../assets/slack.png)

   Las actualizaciones de las notificaciones se guardan automáticamente.

### Solicitar permiso en [!DNL Slack] (solución de problemas) {#slack-troubleshoot}

Si [!DNL Slack] no está instalado, aparece el mensaje _[!UICONTROL Solicitud de instalación]_ cuando el Slack se abre después de hacer clic en **[!UICONTROL Agregar al Slack]**. Por ejemplo:

![Solicitar integración de Slack](../assets/slack-workspace.png)

**Para solicitar permisos en el Slack**

1. En [!DNL Slack], seleccione el área de trabajo en el menú **[!UICONTROL Workspace]** (esquina superior derecha).

1. Para solicitar la aprobación de la aplicación para el administrador de área de trabajo [!DNL Slack], haga clic en **[!UICONTROL Enviar]**.

1. Recibirá una notificación en [!DNL Slack] después de que se apruebe la solicitud de la aplicación.

1. Una vez que reciba la aprobación de [!DNL Slack], regrese al Experience Cloud **[!UICONTROL Notificaciones]** y siga los pasos para [suscribirse al Slack](#slack-notifications) (descritos anteriormente).

### Lo que verá en [!DNL Slack]

Después de integrar correctamente [!DNL Slack], las notificaciones de [!DNL Slack] muestran la siguiente información:

* El mensaje personal se recibirá del nombre de la aplicación _Adobe[!DNL Experience Cloud]_.
* El mensaje incluye el logotipo del producto para la aplicación en particular, como el Adobe [!DNL Experience Platform], el Adobe [!DNL Experience Manager], etc.
* Un vínculo para ver todas las notificaciones en el Experience Cloud.
* Un vínculo para administrar las preferencias de notificación del Experience Cloud.

## Ver [!UICONTROL notificaciones] y anuncios en el Experience Cloud {#view-notifications}

En el encabezado [!DNL Experience Cloud], puede ver las notificaciones a las que se ha [suscrito](#notifications), así como los anuncios.

1. Haga clic en el icono de campana del encabezado. ![Notificaciones y anuncios](../assets/bell-icon.png)

1. Haga clic en **[!UICONTROL Notificaciones]** o en **[!UICONTROL Anuncios]**.

   En esta ubicación recibirá información importante sobre los productos, su colaboración con otros usuarios y otras actualizaciones relevantes. Las actualizaciones incluyen versiones de productos, avisos de mantenimiento, elementos compartidos y solicitudes de aprobación.
