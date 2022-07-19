---
description: 'Obtenga información sobre cómo iniciar sesión y los componentes de la interfaz central en Experience Cloud. Obtenga información sobre la búsqueda global, las preferencias de su cuenta y cómo navegar por la interfaz y obtener ayuda. '
solution: Experience Cloud
title: 'Componentes de la IU central de Experience Cloud '
feature: Central Interface Components
topic: Administration
role: Admin, User
level: Beginner, Intermediate, Experienced
source-git-commit: 00a6aa791dd08c2907cd09c17b7e2a1e62b060c1
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 94%

---

# Temas de ayuda sobre la interfaz de Experience Cloud

Los componentes de la interfaz central de Experience Cloud incluyen funciones que le permiten lo siguiente:

* Inicio de sesión y acceso a sus aplicaciones y servicios
* Búsqueda de la ayuda del producto y los objetos empresariales mediante búsqueda global
* Administración de las preferencias de la cuenta (alertas, notificaciones y suscripciones)

## Compatibilidad con exploradores en Experience Cloud {#browser}

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

## Compatibilidad de idiomas en Experience Cloud {#languages}

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

## Inicie sesión en Experience Cloud {#signin}

Inicie sesión y verifique que se encuentra en la [organización](organizations.md) correcta.

1. Vaya a [Adobe Experience Cloud](https://experience.adobe.com).
1. Seleccione **[!UICONTROL Iniciar sesión con un Adobe ID]**.
1. Compruebe que se encuentra en la organización correcta.

   ![Verifique su organización](assets/organizations-menu.png)

   Para comprobar que ha iniciado sesión en la [organización](organizations.md) correcta, haga clic en el avatar de perfil para ver el nombre de la organización. Si tiene acceso a más de una organización, también puede ver y cambiar a otra organización directamente en la barra de encabezado.

   Si su organización utiliza Federated ID, Experience Cloud le permite iniciar sesión con el inicio de sesión único de su organización sin que se le pida que introduzca su dirección de correo electrónico y contraseña. Agregar `#/sso:@domain` a la dirección URL del Experience Cloud (`https://experience.adobe.com`) para realizar esta tarea.

   Por ejemplo, para una organización con Federated IDs y el dominio `adobecustomer.com`, establezca el vínculo URL en `https://experience.adobe.com/#/sso:@adobecustomer.com`. También puede ir directamente a una aplicación específica marcando esta URL, anexada con la ruta de la aplicación. (Por ejemplo, para Adobe Analytics, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`).

## Acceso a aplicaciones de Experience Cloud {#navigation}

Después de iniciar sesión en Experience Cloud, puede acceder rápidamente a todas sus aplicaciones, servicios y organizaciones desde el encabezado unificado.

Seleccione el selector de aplicaciones ![](assets/menu-icon.png) para acceder a los servicios de Experience Cloud que posee.

![Acceso a aplicaciones de Experience Cloud](assets/platform-core-services.png)

## Búsqueda y asistencia en Experience Cloud {#search-support}

La búsqueda de Experience Cloud le permite buscar ayuda (documentación, tutoriales y cursos) en [Experience League](https://experienceleague.adobe.com/?lang=es#home).

![Búsqueda y asistencia en Experience Cloud](assets/search-menu.png)

El menú [!UICONTROL Ayuda] también le permite acceder a:

* **[!UICONTROL Asistencia técnica]:** Cree un ticket de asistencia o póngase en contacto con el [!UICONTROL Soporte técnico] mediante Twitter.
* **[!UICONTROL Comentarios]:** Póngase en contacto con Adobe para hacernos saber sus comentarios.
* **[!UICONTROL Estado]:** Vaya a `https://status.adobe.com/experience_cloud` y compruebe el estado operativo del producto y [!UICONTROL Administrar suscripciones].
* **[!UICONTROL Developer Connection]:** Navegación hasta `adobe.io` y búsqueda de documentación para desarrolladores.

## Preferencias de cuenta {#account-menu}

En el menú de preferencias de cuenta, puede hacer lo siguiente:

* Especifique un tema oscuro (no todas las aplicaciones admiten este tema)
* Buscar [Organizaciones](organizations.md)
* Cerrar sesión
* Configurar las [preferencias, notificaciones y suscripciones de la cuenta](#preferences)

### Administrar [!UICONTROL Preferencias] de Experience Cloud {#preferences}

Las preferencias de Experience Cloud incluyen notificaciones, suscripciones y alertas.

Seleccione **[!UICONTROL Preferencias]** en el menú de la cuenta ![](assets/preferences-icon-sm.png) para administrar las preferencias.

![Administración de Experience Cloud](assets/preferences-page.png)

En [!UICONTROL preferencias de Experience Cloud], puede configurar las siguientes funciones:

| Función | Descripción |
|--- |--- |
| Organización [predeterminada](organizations.md) | Seleccione la organización que desea ver al iniciar Experience Cloud. |
| [!UICONTROL Suscripciones] | Seleccione los productos y las categorías a los que desea suscribirse. Notificaciones en la ventana emergente [!UICONTROL Notificaciones] y en el correo electrónico. |
| [!UICONTROL Prioridad] | Seleccione las categorías que desea que se consideren de alta prioridad. Estas categorías están marcadas con la etiqueta High y pueden configurarse para entregarlas como alertas. |
| [!UICONTROL Alertas] | Seleccione las notificaciones de las que desea ver las alertas mostradas en el explorador. Las alertas aparecen en la esquina superior derecha de la ventana durante unos segundos. |
| Correos electrónicos | Especifique la frecuencia con la que desea recibir los correos electrónicos de notificación. (No enviado, instantáneo, diario o semanal). |

{style=&quot;table-layout:auto&quot;}

## Notificaciones y anuncios {#notifications}

Seleccione **[!UICONTROL Notificaciones]** para ver las notificaciones que son importantes para usted y los anuncios de Adobe.

![Notificaciones y anuncios](assets/notifications-menu-small.png)

Puede configurar las notificaciones en [preferencias de Experience Cloud](#preferences).
