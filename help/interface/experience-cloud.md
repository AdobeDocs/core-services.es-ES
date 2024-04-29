---
description: Obtenga información sobre los componentes de la interfaz central en Experience Cloud. La ayuda incluye la administración de usuarios y productos en Admin Console, lo que permite crear aplicaciones para los servicios de Experience Cloud y recibir ayuda en la biblioteca de públicos, los atributos del cliente, los activos de Experience Cloud, etc.
title: Documentación y temas de ayuda sobre la interfaz de Experience Cloud
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: a4e0461791cd676365857c2dd4ef28c0e40c3430
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 99%

---

# Introducción a la interfaz central de Experience Cloud

[Experience Cloud](https://experience.adobe.com) es la familia integrada de aplicaciones, productos y servicios de marketing digital de Adobe. Desde la intuitiva interfaz, puede acceder rápidamente a sus aplicaciones, funciones de productos y servicios en la nube.

![Experience Cloud](assets/landing.png)

En el encabezado de Experience Cloud encuentra las siguientes funciones:

* Acceso a sus aplicaciones y servicios
* En el menú Ayuda, busque documentación del producto, tutoriales y publicaciones de la comunidad. Ver resultados en Experience League.
* Haga una búsqueda general de objetos empresariales mediante una búsqueda global (solo usuarios de Experience Platform) en el campo Búsqueda.
* Administración de las preferencias de la cuenta (alertas, notificaciones y suscripciones)

## Inicie sesión en Experience Cloud {#signin}

Inicie sesión y verifique que se encuentra en la [organización](administration/organizations.md) correcta.

1. Vaya a [Adobe Experience Cloud](https://experience.adobe.com).
1. Escriba su dirección de correo electrónico de Adobe y seleccione **[!UICONTROL Continuar]**.
1. Seleccione una cuenta.
1. Escriba la contraseña.
1. Compruebe que se encuentra en la organización correcta.

   ![Compruebe que se encuentra en la organización correcta](assets/organizations-menu.png)

   **Verifique su organización**

   Para comprobar que ha iniciado sesión en la [organización](administration/organizations.md) correcta, haga clic en el avatar de perfil para ver el nombre de la organización. Si tiene acceso a más de una organización, también puede ver y cambiar a otra organización directamente en la barra de encabezado.

   Si su organización utiliza Federated ID, Experience Cloud le permite iniciar sesión con el inicio de sesión único de su organización sin necesidad de escribir su dirección de correo electrónico y contraseña. Agregar `#/sso:@domain` a la dirección URL de Experience Cloud (`https://experience.adobe.com`) para realizar esta tarea.

   Por ejemplo, para una organización con Federated IDs y el dominio `adobecustomer.com`, establezca el vínculo URL en `https://experience.adobe.com/#/sso:@adobecustomer.com`. También puede ir directamente a una aplicación específica marcando esta URL, anexada con la ruta de la aplicación. (Por ejemplo, para Adobe Analytics, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`).

## Acceso a aplicaciones de Experience Cloud {#navigation}

Después de iniciar sesión en Experience Cloud, puede acceder rápidamente a todas sus aplicaciones, servicios y organizaciones desde el encabezado unificado.

Para acceder a las aplicaciones y servicios de Experience Cloud proporcionados por usted dentro de su organización, vaya al ![menú](assets/menu-icon.png) del selector de aplicaciones.

![Acceso a aplicaciones de Experience Cloud](assets/platform-core-services.png)

## Obtener ayuda y asistencia {#support}

Acceda a aprendizaje y ayuda mediante el icono de Ayuda (![recurso](assets/help-icon.png)) del encabezado, que incluye contenido de ayuda (documentación, tutoriales y cursos) en [Experience League](https://experienceleague.adobe.com/?lang=es#home), así como recursos adicionales para aplicaciones individuales. También puede enviar comentarios abiertos y crear tickets de asistencia con prioridad.

![Obtener ayuda y asistencia](assets/search-menu.png)

El menú [!UICONTROL Ayuda] también le permite acceder a:

* **[!UICONTROL Asistencia técnica]:** Cree un ticket de asistencia o póngase en contacto con el [!UICONTROL Soporte técnico] mediante Twitter.
* **[!UICONTROL Comentarios]:** Comparta comentarios sobre su experiencia de Experience Cloud. Los comentarios se utilizan para mejorar los productos y servicios de Adobe.
* **[!UICONTROL Estado]:** Vaya a `https://status.adobe.com/experience_cloud` y compruebe el estado operativo del producto y [!UICONTROL Administrar suscripciones].
* **[!UICONTROL Developer Connection]:** Navegación hasta `adobe.io` y búsqueda de documentación para desarrolladores.

## Perfil de usuario y preferencias de cuenta {#preferences}

Las preferencias de Experience Cloud incluyen notificaciones, suscripciones y alertas. En el menú de preferencias de cuenta, puede hacer lo siguiente:

* Especifique un tema oscuro (no todas las aplicaciones admiten este tema)
* Buscar [Organizaciones](administration/organizations.md)
* Cerrar sesión
* Configurar las preferencias, notificaciones y suscripciones de la cuenta

Para administrar las preferencias, seleccione **[!UICONTROL Preferencias]** en el menú ![preferencias](assets/preferences-icon-sm.png) de su cuenta.

![Perfil de usuario y preferencias de cuenta](assets/preferences-page.png)

En [!UICONTROL preferencias de Experience Cloud], puede configurar las siguientes funciones:

| Función | Descripción |
|--- |--- |
| Organización [predeterminada](administration/organizations.md) | Seleccione la organización que desea ver al iniciar Experience Cloud. |
| [!UICONTROL Recopilación de datos del producto] | Seleccione qué tecnologías puede utilizar Adobe para recopilar datos sobre cómo aprovechar sus productos. |
| [!UICONTROL Recomendaciones y promociones de formación personalizadas] | Seleccione dónde desea recibir ayuda personalizada para sus productos de Adobe. Esta ayuda está disponible por correo electrónico, en el producto y en las comunidades de Experience League. [Más información.](features/personalized-learning.md) |
| [!UICONTROL Suscripciones] | Seleccione los productos y las categorías a los que desea suscribirse. Notificaciones en la ventana emergente [!UICONTROL Notificaciones] y en el correo electrónico. |
| [!UICONTROL Prioridad] | Seleccione las categorías que desea que se consideren de alta prioridad. Estas categorías están marcadas con la etiqueta High y pueden configurarse para entregarlas como alertas. |
| [!UICONTROL Alertas] | Seleccione las notificaciones de las que desea ver las alertas mostradas en el explorador. Las alertas aparecen en la esquina superior derecha de la ventana durante unos segundos. |
| Correos electrónicos | Especifique la frecuencia con la que desea recibir los correos electrónicos de notificación. (No enviado, instantáneo, diario o semanal). |

{style="table-layout:auto"}

## Notificaciones y anuncios {#notifications}

Seleccione **[!UICONTROL Notificaciones]** para recibir alertas acerca de actualizaciones relevantes y disponibles, incluidas versiones de productos, avisos de mantenimiento, elementos compartidos y solicitudes de aprobación.

![Notificaciones y anuncios](assets/notifications-menu-small.png)
