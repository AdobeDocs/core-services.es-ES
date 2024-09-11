---
title: Preferencias y notificaciones de cuenta
description: Obtenga información sobre los perfiles de usuario y las preferencias de cuenta en Experience Cloud. Suscríbase a las notificaciones de productos para correo electrónico y  [!DNL Slack], y configure alertas de productos.
solution: Experience Cloud
feature: Account Preferences, Notifications, Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 1e34c6b2-a792-41c4-adb7-583de596237f
source-git-commit: 0b2cae6b7aec7e91ac4b46de4d844dd2269095a9
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 21%

---

# Preferencias y notificaciones de cuenta {#preferences}

Las [preferencias](https://experience.adobe.com/preferences) del Experience Cloud incluyen notificaciones (en la aplicación, correo electrónico y [!DNL Slack]), suscripciones y alertas.

En las preferencias, puede:

* Buscar [Organizaciones](../administration/organizations.md)
* Especifique un tema oscuro (no todas las aplicaciones admiten este tema).
* Configure las preferencias, notificaciones y suscripciones de la cuenta para los usuarios.
* Cerrar sesión de Experience Cloud.

## Administrar preferencias

Para administrar las preferencias, seleccione **[!UICONTROL Preferencias]** en el menú ![preferencias](../assets/preferences-icon-sm.png) de su cuenta.

En [!UICONTROL preferencias de Experience Cloud], puede configurar las siguientes funciones:

| Función | Descripción |
|--- |--- |
| Organización [predeterminada](../administration/organizations.md) | Seleccione la organización que desea ver al iniciar Experience Cloud. |
| [!UICONTROL Recopilación de datos del producto] | Seleccione qué tecnologías puede utilizar Adobe para recopilar datos sobre cómo aprovechar sus productos. |
| [Notificaciones](#notifications-and-announcements) | Habilitar las notificaciones [!UICONTROL en la aplicación], [!UICONTROL correo electrónico] o [Slack](#slack-notifications). |
| [!UICONTROL Recomendaciones y promociones de formación personalizadas] | Seleccione dónde desea recibir [ayuda personalizada](personalized-learning.md) para sus productos de Adobe. Esta ayuda está disponible por correo electrónico, en el producto y en las comunidades de Experience League. |
| [!UICONTROL Suscripciones] | Seleccione los productos y las categorías a los que desea suscribirse. Notificaciones en la ventana emergente [!UICONTROL Notificaciones] y en su correo electrónico. |
| [!UICONTROL Prioridad] | Seleccione las categorías que desea que se consideren de alta prioridad. Estas categorías están marcadas con la etiqueta [!UICONTROL High] y pueden configurarse para su envío como alertas. |
| [!UICONTROL Alertas] | Seleccione las notificaciones de las que desea ver las alertas mostradas en el explorador. Las alertas aparecen en la esquina superior derecha de la ventana durante unos segundos. |
| Correos electrónicos | Especifique la frecuencia con la que desea recibir los correos electrónicos de notificación. (No enviado, instantáneo, diario o semanal). |

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