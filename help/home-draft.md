---
description: Obtenga información sobre los componentes de la interfaz central en Experience Cloud. Obtenga ayuda sobre la administración de usuarios y productos en Admin Console y habilite aplicaciones para los servicios de Experience Cloud. Obtenga ayuda sobre la biblioteca de audiencias, los atributos del cliente, Experience Cloud Assets y mucho más.
title: Documentación de la interfaz de Experience Cloud
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 361175f290d73f1637673420700874a2415e3fca
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 81%

---

# Información general de la interfaz central de Experience Cloud

[Experience Cloud](https://experience.adobe.com) es la familia integrada de aplicaciones, productos y servicios de marketing digital de Adobe. Desde la intuitiva interfaz, puede acceder rápidamente a sus aplicaciones, funciones de productos y servicios en la nube.

![Experience Cloud](assets/landing.png)

En el encabezado de Experience Cloud encuentra las siguientes funciones:

* Acceda a todas las aplicaciones y servicios de Experience Cloud
* En el menú Ayuda, busque documentación del producto, tutoriales y publicaciones de la comunidad. Ver resultados en Experience League.
* Haga una búsqueda general de objetos empresariales mediante una búsqueda global (solo usuarios de Experience Platform) en el campo Búsqueda.
* Administración de las [preferencias](features/account-preferences.md) de la cuenta (alertas, notificaciones y suscripciones)


Extraído de GSPM:

## Exploración de funcionalidades

<table style="table-layout:fixed">
<tr style="border: 0;">
   <td valign="top">
      <a href="../user-guide/effective-prompts.md">
      <img alt="Corchete derecho" src="../assets/icons/icon-chevronRight.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/effective-prompts.md">
         <strong>Escribir indicadores efectivos</strong>
         </a>
      </div>
      <p>
         <em>Instrucciones descriptivas personalizadas que generan experiencias digitales en la marca.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/create/overview.md">
      <img alt="Pincel" src="../assets/icons/icon-create.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/create/overview.md">
         <strong>Crear experiencias</strong>
         </a>
      </div>
      <p>
         <em>Crear anuncios Meta y correos electrónicos con marca y que tengan un buen rendimiento.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/approvals/overview.md">
      <img alt="Marca de verificación" src="../assets/icons/icon-checkmarkCircle.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/approvals/overview.md">
         <strong>Revisar y aprobar</strong>
         </a>
      </div>
      <p>
         <em>Organice la revisión y aprobación optimizadas de los recursos de marketing.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/content/overview.md">
      <img alt="Cuadrícula" src="../assets/icons/icon-images.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/content/overview.md">
         <strong>Administrar contenido</strong>
         </a>
      </div>
      <p>
         <em>Busque, administre y vuelva a utilizar contenido manteniendo las directrices de marca.</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/insights/overview.md">
      <img alt="Gráfico" src="../assets/icons/icon-dataAnalytics.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/insights/overview.md">
         <strong>Ver información</strong>
         </a>
      </div>
      <p>
         <em>Analizar la eficacia del contenido de los canales de medios pagados.</em>
      </p>
   </td>
</tr>
</table>

## Obtenga información sobre cómo

<table style="table-layout:fixed">
<td valign="top">
   <div>
      <a href="/help/user-guide/guidelines/add-guidelines.md">
      <img alt="Adición de directrices" src="../assets/card-guidelines.png">
      <strong>Agregar directrices</strong>
      </a>
   </div>
   <p>
      <em>Aprenda a agregar directrices (marcas, productos y personas) a GenStudio for Performance Marketing.</em>
   </p>
</td>
<td valign="top">
   <div>
      <a href="/help/user-guide/create/create-email-experience.md">
      <img alt="Ideas, libros, lápiz, ordenador" src="../assets/card-create-assets.png">
      <strong>Crear una experiencia de correo electrónico</strong>
      </a>
   </div>
   <p>
      <em>Aprenda a crear una experiencia de correo electrónico en la marca.</em>
   </p>
</td>
<td valign="top">
   <div>
      <a href="/help/user-guide/create/create-meta-ad.md">
      <img alt="Personas que mueven archivos a una carpeta" src="../assets/card-manage-content.png">
      <strong>Crear una experiencia de Meta ad</strong>
      </a>
   </div>
   <p>
      <em>Aprenda a crear una experiencia de anuncio Meta adaptada a la marca.</em>
   </p>
</td>
</table>


(Fin de GSPM)







## Inicie sesión en Experience Cloud {#signin}

Inicie sesión y verifique que se encuentra en la [organización](administration/organizations.md) correcta.

1. Vaya a [Adobe Experience Cloud](https://experience.adobe.com).
1. Escriba su dirección de correo electrónico de Adobe y haga clic en **[!UICONTROL Continuar]**.
1. Seleccione una cuenta.
1. Escriba la contraseña.
1. Compruebe que se encuentra en la organización correcta.

   ![Compruebe que se encuentra en la organización correcta](assets/organizations-menu.png)

   **Verifique su organización**

   La [organización](administration/organizations.md) se muestra en el encabezado de la interfaz.

   Si su organización utiliza Federated ID, Experience Cloud le permite iniciar sesión con el inicio de sesión único de su organización sin necesidad de escribir su dirección de correo electrónico y contraseña. Agregar `#/sso:@domain` a la dirección URL de Experience Cloud (`https://experience.adobe.com`) para realizar esta tarea.

   Por ejemplo, para una organización con Federated IDs y el dominio `adobecustomer.com`, establezca el vínculo URL en `https://experience.adobe.com/#/sso:@adobecustomer.com`. También puede ir directamente a una aplicación específica marcando esta URL, anexada con la ruta de la aplicación. (Por ejemplo, para Adobe Analytics, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`).

## Acceso a aplicaciones de Experience Cloud {#navigation}

Después de iniciar sesión en Experience Cloud, puede acceder rápidamente a todas sus aplicaciones, servicios y organizaciones desde el encabezado unificado.

Para acceder a las aplicaciones y servicios de Experience Cloud proporcionados por usted dentro de su organización, vaya al ![menú](assets/menu-icon.png) del selector de aplicaciones.

![Acceso a aplicaciones de Experience Cloud](assets/platform-core-services.png)

## Obtener ayuda y asistencia {#support}

Acceda a aprendizaje y ayuda mediante el **[!UICONTROL Centro de Ayuda]** (![activo](assets/help-icon.png)) del encabezado, que incluye contenido de ayuda (documentación, tutoriales y cursos) en [Experience League](https://experienceleague.adobe.com/?lang=es#home), así como recursos adicionales para aplicaciones individuales. También puede enviar comentarios abiertos y crear tickets de asistencia con prioridad.

![Obtener ayuda y asistencia](assets/search-menu.png)

El menú [!UICONTROL Ayuda] también le permite acceder a:

* **[!UICONTROL Asistencia técnica]:** Cree un ticket de asistencia o póngase en contacto con el [!UICONTROL Soporte técnico] mediante Twitter.
* **[!UICONTROL Comentarios]:** Comparta comentarios sobre su experiencia de Experience Cloud. Los comentarios se utilizan para mejorar los productos y servicios de Adobe.
* **[!UICONTROL Estado]:** Vaya a `https://status.adobe.com/experience_cloud` y compruebe el estado operativo del producto y [!UICONTROL Administrar suscripciones].
* **[!UICONTROL Developer Connection]:** Navegación hasta `adobe.io` y búsqueda de documentación para desarrolladores.

## Administrar el perfil de usuario

En el menú [!UICONTROL Perfil] puede hacer lo siguiente:

* Especifique un tema oscuro (no todas las aplicaciones admiten este tema)
* Administrar [Preferencias](features/account-preferences.md) de Experience Cloud
* Seleccione o busque una [organización](administration/organizations.md)
* Ver [!UICONTROL avisos legales]
* Cerrar sesión
* Configurar las preferencias, notificaciones y suscripciones de la cuenta

## Ver notificaciones y anuncios dentro del producto {#notifications}

Haga clic en el icono de la campana para ver las notificaciones y los anuncios. Los anuncios pueden ser actualizaciones relevantes y procesables, entre ellas versiones de productos, avisos de mantenimiento, elementos compartidos y solicitudes de aprobación.

![Notificaciones y anuncios](assets/notifications-menu-small.png)

Para administrar notificaciones y alertas, consulte [Preferencias y notificaciones de la cuenta](features/account-preferences.md)


## Novedades

Obtenga información sobre las mejoras más recientes de los componentes de la interfaz central de Experience Cloud.

>[!BEGINTABS]

>[!TAB Integración de Slack con Experience Cloud]

Puede configurar las preferencias de su cuenta para enviar notificaciones de Experience Cloud a un canal [!DNL Slack].

[!BADGE Beta]{type=Informative url="https://experienceleague.adobe.com/en/docs/core-services/interface/features/account-preferences#notifications" tooltip="Más información sobre Slack"}


>[!TAB Nueva interfaz de usuario web de Campaign]

Experimenta la nueva interfaz de usuario de Adobe Campaign Más moderna, intuitiva y dinámica.

[![Imagen](assets/do-not-localize/learn-more-button.svg)](start/campaign-ui.md#ac-web-ui)


>[!TAB Próximos cambios en el canal de mensajes push]

Algunos cambios importantes en el servicio Android Firebase Cloud Messaging (FCM) se lanzarán en 2024 y pueden afectar a la implementación de Adobe Campaign. Es posible que sea necesario actualizar la configuración de los servicios de suscripción para los mensajes push de Android a fin de que admitan este cambio. Ya puede comprobar y realizar acciones.

[![image](assets/do-not-localize/learn-more-button.svg)](../technotes/upgrades/push-technote.md)



>[!ENDTABS]

## Empiece con lo básico

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
    <a href="start/whats-new.md"><img src="assets/do-not-localize/start-capabilities.png"></a>
    <div><strong>Funcionalidades clave</strong><br/>Explore las funciones clave de Adobe Campaign v8 para la administración de campañas en canales múltiples.</div>
    </td>
    <td>
    <a href="start/connect.md"><img src="assets/do-not-localize/start-connect.jpeg"></a>
    <div><strong>Conéctate a Campaign v8</strong><br/>Aprenda a conectarse a Adobe Campaign v8 y a iniciar el recorrido de administración de campañas instalando y configurando la consola de cliente.</div><br/>
    </td>
    <td>
    <a href="start/create-message.md"><img src="assets/do-not-localize/start-send.jpeg"></a>
    <div><strong>Mensajes de envío</strong><br/>Aprenda a enviar mensajes a través de varios canales, como correo electrónico, SMS, notificaciones push, entre otros.
    </div></td>
    <td>
    <a href="audiences/create-profiles.md"><img src="assets/do-not-localize/start-profiles.png"></a>
    <div><strong>Importación de perfiles</strong><br/>Explore fácilmente la administración de perfiles en la base de datos de la versión 8 de Adobe Campaign. Añade perfiles manualmente o importándolos para refinar los datos de los clientes y personalizar las campañas sin complicaciones.</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="start/whats-new.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/connect.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/create-message.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="audiences/create-profiles.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    </tr>
</table>

## Explore la documentación

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon-start.svg" width="35px">
    <br/>
      <strong>Introducción a</strong><br/><a href="start/campaign-ui.md">la interfaz de usuario</a> - <a href="start/ac-components.md">Componentes y procesos</a> - <a href="start/v7-to-v8.md">De la versión 7 a la 8 de Classic</a> - <a href="start/campaign-faq.md">Preguntas frecuentes</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-experience.svg" width="35px">
    <br/>
      <strong>Experiencia del cliente</strong><br/><a href="../automation/workflow/about-workflows.md" target="_blank">Automatización con flujos de trabajo</a> - <a href="../automation/campaigns/set-up-campaigns.md" target="_blank">Orquestación de campañas</a> - <a href="interaction/interaction.md">Gestión de decisiones</a> - <a href="send/personalize.md">Personalización</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-send.svg" width="35px">
    <br/>
      <strong>Envío de mensajes</strong><br/><a href="start/create-message.md">Introducción</a> - <a href="send/preview-and-proof.md">Previsualización y pruebas</a> - <a href="send/predictive.md">Optimización del tiempo de envío</a> - <a href="reporting/gs-reporting.md">Creación de informes y análisis</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon_profile-audience.svg" width="35px">
    <br/>
      <strong>Perfiles y públicos</strong><br/><a href="audiences/create-profiles.md">Adición de perfiles</a> - <a href="audiences/create-audiences.md">Creación de públicos</a> - <a href="start/subscriptions.md">Administración de suscripciones</a> - <a href="start/privacy.md">Privacidad</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-configure.svg" width="35px">
    <br/>
      <strong>Arquitectura y configuración</strong><br/><a href="architecture/architecture.md">Arquitectura</a> - <a href="start/implement.md">Implementación de Campaign v8</a> - <a href="connect/integration.md">Conexión con otras soluciones</a> - <a href="start/gs-permissions.md">Usuarios y permisos</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-dev.svg" width="35px">
    <br/>
      <strong>Recursos para desarrolladores</strong><br/><a href="dev/datamodel.md">Modelo de datos de Campaign v8</a> - <a href="dev/schemas.md">Esquemas</a> - <a href="dev/api.md">API</a>
    </td>
  </tr>
</table>

## Recursos adicionales

[Descripción del producto Adobe Campaign, versión 8](https://helpx.adobe.com/es/legal/product-descriptions/adobe-campaign-managed-cloud-services.html){target="_blank"} - [Documentación de la interfaz de usuario web de Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-web/v8/campaign-web-home.html?lang=es){target="_blank"} - [Tutoriales](https://experienceleague.adobe.com/docs/campaign-learn/tutorials/overview.html?lang=es){target="_blank"} - [[!DNL Adobe Campaign] Guía de automatización](https://experienceleague.adobe.com/docs/campaign/automation/home.html?lang=es){target="_blank"} - [Panel de control de la versión 8 Campaign](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/key-features.html?lang=es){target="_blank"}

