---
description: Obtenga información sobre cómo iniciar sesión y los componentes de la interfaz central en Experience Cloud. Obtenga información sobre la búsqueda global, las preferencias de su cuenta y cómo navegar por la interfaz y obtener ayuda.
solution: Experience Cloud
title: Componentes de la IU central de Experience Cloud
feature: Central Interface Components
topic: Administration
role: Admin, User
level: Beginner, Intermediate, Experienced
source-git-commit: 63d5c080a7282c78eb7a66c5a54c69b5597545ab
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 78%

---

# Componentes de la interfaz central de Experience Cloud

Los componentes de la interfaz central de Experience Cloud incluyen funciones que le permiten lo siguiente:

* Inicio de sesión y acceso a sus aplicaciones y servicios
* Búsqueda de la ayuda del producto y los objetos empresariales mediante búsqueda global
* Administración de las preferencias de la cuenta (alertas, notificaciones y suscripciones)

## Compatibilidad con exploradores en Experience Cloud

Para obtener el mejor rendimiento, Experience Cloud está optimizado para los exploradores más populares, incluida la versión más reciente, además de las dos versiones anteriores.

* Chrome
* Edge
* Firefox
* Opera
* Safari

Si el explorador no aparece en la lista, puede que sea compatible, pero se recomienda que utilice uno de los exploradores enumerados.

>[!NOTE]
>
>No todas las aplicaciones que se ejecutan en el dominio de Experience Cloud admiten todos los exploradores. Si no está seguro, consulte la documentación de la aplicación específica.

## Compatibilidad de idiomas en Experience Cloud

Experience Cloud admite los idiomas preferidos para cada usuario, tal como se establecen en las preferencias de cuenta de usuario de Adobe. Actualmente se admiten los siguientes idiomas:

* Chino
* Inglés
* Francés
* Alemán
* Italiano
* Japonés
* Coreano
* Portugués
* Español
* Taiwanés

Aunque todos los equipos de aplicaciones están comprometidos con el soporte de idiomas global, no todas las aplicaciones se ofrecen en todos los idiomas mencionados anteriormente. Si el idioma principal no es compatible con una aplicación de Experience Cloud, también puede establecer un idioma secundario de forma predeterminada cuando corresponda. Esto se puede hacer en [preferencias de usuario de Experience Cloud](https://experience.adobe.com/preferences).

## Inicie sesión en Experience Cloud

Inicie sesión y compruebe que se encuentra en la organización correcta.

1. Vaya a [Adobe Experience Cloud](https://experience.adobe.com).
1. Haga clic en **[!UICONTROL Sign in with an Adobe ID]**.
1. Compruebe que se encuentra en la organización correcta.

   ![Verifique su organización](assets/organizations-menu.png)

   Para comprobar que ha iniciado sesión en su organización correcta, haga clic en **[!UICONTROL Profile]** para ver el nombre de la organización. Si tiene acceso a más de una organización, también puede ver y cambiar a otra organización mediante el selector **[!UICONTROL Organization]**.

   Si su organización utiliza Federated ID, Experience Cloud le permite iniciar sesión con el inicio de sesión único de su organización sin necesidad de escribir su dirección de correo electrónico y contraseña. Agregar `#/sso:@domain` a la dirección URL de Experience Cloud (`https://experience.adobe.com`) para realizar esta tarea.

   Por ejemplo, para una organización con Federated IDs y el dominio `adobecustomer.com`, establezca el vínculo URL en `https://experience.adobe.com/#/sso:@adobecustomer.com`. También puede ir directamente a una aplicación específica marcando esta URL, anexada con la ruta de la aplicación. (Por ejemplo, para Adobe Analytics, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`).

## Acceso a aplicaciones de Experience Cloud

Después de iniciar sesión en Experience Cloud, puede acceder rápidamente a todas sus aplicaciones, servicios y organizaciones desde el encabezado unificado.

Haga clic en el selector de aplicaciones ![menu](assets/menu-icon.png) para acceder a los servicios de Experience Cloud que posee.

![Acceso a aplicaciones de Experience Cloud](assets/platform-core-services.png)

## Búsqueda y asistencia en Experience Cloud

La búsqueda de Experience Cloud le permite buscar ayuda (documentación, tutoriales y cursos) en [Experience League](https://experienceleague.adobe.com/?lang=es#home).

![Búsqueda y asistencia en Experience Cloud](assets/search-menu.png)

El menú [!UICONTROL Help] también le da acceso a:

* **[!UICONTROL Support]:** Cree una incidencia de soporte técnico o un contacto [!UICONTROL Support] mediante Twitter.
* **[!UICONTROL Feedback]:** Póngase en contacto con Adobe para hacernos saber sus comentarios.
* **[!UICONTROL Status]:** Vaya a `https://status.adobe.com/experience_cloud` y compruebe el estado operativo del producto y [!UICONTROL Manage Subscriptions].
* **[!UICONTROL Developer Connection]:** Navegación a `adobe.io` y búsqueda de documentación para desarrolladores.

## Preferencias de cuenta

En el menú de preferencias de cuenta, puede hacer lo siguiente:

* Especifique un tema oscuro (no todas las aplicaciones admiten este tema)
* Buscar organizaciones
* Cerrar sesión
* Configurar las [preferencias, notificaciones y suscripciones de la cuenta](#preferences)

### Administrar Experience Cloud [!UICONTROL Preferences]

Las preferencias de Experience Cloud incluyen notificaciones, suscripciones y alertas.

* Haga clic en **[!UICONTROL Preferences]** en el menú de su cuenta ![preferencias](assets/preferences-icon-sm.png) para administrar las preferencias.

![Administración de Experience Cloud](assets/preferences-page.png)

En [!UICONTROL Experience Cloud preferences], puede configurar las siguientes características:

| Función | Descripción |
|--- |--- |
| Organización predeterminada | Seleccione la organización que desea ver al iniciar Experience Cloud. |
| [!UICONTROL Subscriptions] | Seleccione los productos y las categorías a los que desea suscribirse. Notificaciones en la ventana emergente [!UICONTROL Notifications] y en el correo electrónico. |
| [!UICONTROL Priority] | Seleccione las categorías que desea que se consideren de alta prioridad. Estas categorías están marcadas con la etiqueta High y pueden configurarse para entregarlas como alertas. |
| [!UICONTROL Alerts] | Seleccione las notificaciones de las que desea ver las alertas mostradas en el explorador. Las alertas aparecen en la esquina superior derecha de la ventana durante unos segundos. |
| Correos electrónicos | Especifique la frecuencia con la que desea recibir los correos electrónicos de notificación. (No enviado, instantáneo, diario o semanal). |

{style="table-layout:auto"}

## Notificaciones y anuncios

Haga clic en **[!UICONTROL Notifications]** para ver las notificaciones que son importantes para usted y los anuncios de Adobe.

![Notificaciones y anuncios](assets/notifications-menu-small.png)

Puede configurar las notificaciones en [preferencias de Experience Cloud](#preferences).
