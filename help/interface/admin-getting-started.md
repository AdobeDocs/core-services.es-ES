---
title: Administrar usuarios y productos
description: Inicie sesión en el Admin Console y administre los permisos y productos de usuario de Experience Cloud (perfiles de producto). Obtenga información acerca de la delegación de derechos administrativos a usuarios de Experience Cloud y sobre la compatibilidad del explorador con Experience Cloud.
solution: Admin
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: af9eda5b-d984-44b7-a7b3-52dfc4e03d8f
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: tm+mt
source-wordcount: '1582'
ht-degree: 74%

---

# Administración de usuarios y productos en [!DNL Experience Cloud]

Obtenga más información sobre el inicio de sesión en Admin Console y la administración de permisos de usuarios, perfiles de producto y compatibilidad de exploradores en Experience Cloud.

>[!IMPORTANT]
>
>La siguiente información está diseñada específicamente para aplicaciones de Experience Cloud. Esta información complementa la información administrativa más general de la [Guía del usuario de administración de Enterprise](https://helpx.adobe.com/es/enterprise/admin-guide.html) para todos los productos en la nube de Adobe.

Puede ver una lista, que puede ordenarse y filtrarse, de todos los usuarios de Experience Cloud y sus detalles en la herramienta de administración. Consulte [Vista de los usuarios de Experience Cloud en la herramienta de administración](admin-tool-experience-cloud.md).

## Aviso de actualización de aprovisionamiento{#provisioning}

Actualizado el **20 de julio de 2022**

>[!IMPORTANT]
>
>Revise el siguiente aviso sobre el aprovisionamiento de Experience Cloud.

Adobe está actualizando su aprovisionamiento para proporcionar a todos los clientes Experience Cloud acceso a las funcionalidades básicas que ayudan a la interoperabilidad entre algunos productos Experience Cloud. Los usuarios tendrán Adobe Experience Platform como un nuevo derecho añadido a sus organizaciones Experience Cloud, con [!UICONTROL Recopilación de datos] como servicio incluido.

Adobe Experience Platform [!UICONTROL Recopilación de datos] incluye [etiquetas](https://experienceleague.adobe.com/en/docs/tags) para una administración universal de etiquetas simplificada, y ofrece una infraestructura de datos de streaming fiable, sólida y completa. Las etiquetas simplifican la recopilación de datos de experiencias del cliente y optimizan la entrega de experiencias.

**Cambios en la[!DNL Admin Console]**

Los administradores pueden ver cambios o adiciones en el [!DNL Admin Console] como sigue:

* La tarjeta de producto de Adobe Experience Platform del Admin Console incluye:

   * Places
   * Assurance
   * Área de nombres de identidad
   * Zonas protegidas
   * Modelo de datos de experiencia
   * Esquemas
   * Corrientes de datos
   * ID de visitante

  Para las organizaciones que actualmente no utilizan Experience Platform, ahora verá el _Adobe Experience Platform_ producto en la [!DNL Admin Console], incluidas las funcionalidades enumeradas anteriormente.

  Para organizaciones que actualmente utilizan Experience Platform, _Places_ ahora se consolidará en la tarjeta de Experience Platform.

* La recopilación de datos de Adobe Experience Platform (anteriormente, Launch) y la privacidad seguirán apareciendo como tarjetas de producto independientes de las demás funciones de Experience Platform.

Para obtener más información sobre las nuevas funciones, visite sus páginas respectivas en Experience League:

* [Recopilación de datos](https://experienceleague.adobe.com/docs/discontinued/using/reports-and-analytics.html?lang=es)
* [Places](https://experienceleague.adobe.com/en/docs/places/using/home)
* [Assurance](https://experienceleague.adobe.com/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance.html?lang=es)
* [Área de nombres de identidad](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=es)
* [Zonas protegidas](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=es)
* [Modelo de datos de experiencia](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es)
* [Esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=es)
* [Corrientes de datos](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=es)
* [ID de visitante](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html?lang=es#section_3C9F6DF37C654D939625BB4D485E4354)
* [Privacidad](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=es)

## Autenticación de usuarios de Experience Cloud (migración planificada){#migration}

A partir de febrero de 2022, Adobe actualiza su sistema de administración de perfiles para permitir a las organizaciones administrar mejor los derechos empresariales a perfiles individuales. Como tal, todos los usuarios con un perfil personal, que corresponde a un Adobe ID individual (Type1), se migrarán a un nuevo perfil comercial. Este perfil corresponde a un _ID empresarial_ (Type2e).

Consulte [Tipos de identidad en el Adobe [!DNL Admin Console]](https://helpx.adobe.com/es/enterprise/using/identity.html) para obtener información sobre los tipos de identidad.

### Proceso de migración

Cuando sea el momento de migrar, los administradores de la organización recibirán un mensaje de correo electrónico como notificación 30 días antes de la migración.

* La migración se programará entre las 22:00 h y las 6:00 h, según la zona horaria principal de la organización, o en fin de semana.
* Durante la migración, es posible que la aplicación del Experience Cloud no sea accesible durante unos 15 minutos y [!DNL Admin Console] puede ser inaccesible hasta 30 minutos. Por lo demás, esta migración se realizará sin problemas.

### Cambios después de la migración

[!DNL Admin Console]

* Los administradores con varias cuentas pueden ver un selector de perfil al iniciar sesión en [!DNL Admin Console].
* Los usuarios individuales de Adobe ID se actualizan a un ID empresarial.
* El directorio de ID empresariales se agrega en **[!UICONTROL Configuración]** > **[!UICONTROL Identidad]** > **[!UICONTROL Directorios]**.

  ![[!DNL Admin Console] Identidad: ID empresarial](assets/identity-home.png)

### Inicio de sesión después de la migración

La experiencia de inicio de sesión no cambia con esta actualización:

1. Inicie sesión en `experience.adobe.com` usando las mismas credenciales.

1. Se crea un nuevo perfil asociado al ID empresarial. Se le pedirá **[!UICONTROL Unirse ahora]** u **[!UICONTROL Omitir]**.

1. Al elegir una de las opciones, se le lleva a una experiencia de página de aterrizaje existente.

1. Un perfil de Adobe está asociado a cada plan empresarial y proporciona la capacidad de organizar los recursos creados a partir de ofertas de nube de Adobe adicionales (Creative Cloud y Document Cloud).

Para obtener más información, consulte [Presentación de perfiles de Adobe](https://helpx.adobe.com/es/enterprise/kb/introducing-adobe-profiles.html).

## ¿Qué es un perfil de producto? {#section_AB50558124D541CF80A0D3D76D35A4BF}

_[!UICONTROL Perfiles de producto]_ son grupos de productos y servicios que puede asignar a los usuarios. En Experience Cloud, los permisos se basan en el perfil de un producto, no en el usuario. (Sin embargo, puede delegar derechos administrativos a usuarios específicos).

Por ejemplo, en Analytics puede configurar una colección de herramientas de creación de informes, como Analysis Workspace y Report Builder, además de grupos de informes, métricas y dimensiones. Puede dar permiso a los usuarios para acceder a un perfil de producto añadiéndolos a este.

* Consulte [Asignar permisos de acceso de Analytics a un perfil de producto](admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) en esta página.
* Consulte [Delegación de funciones administrativas en usuarios](#delegate-rights) en esta página.

## Administración de perfiles de producto de Experience Cloud {#task_16335111C52D40E9BAC73D0699584DBF}

Puede crear un perfil de producto y asignarlo a un grupo de permisos.

Al invitar a un usuario a una organización, puede darle acceso a productos y perfiles de productos. También puede delegar permisos administrativos limitados en un usuario. Del mismo modo, puede crear grupos de usuarios y luego agregar el grupo a un perfil de productos para habilitar el acceso.

1. En el [[!DNL Admin Console]](https://adminconsole.adobe.com/enterprise/), seleccione **[!UICONTROL Productos]**.
1. Seleccione el nombre de su organización.
1. Seleccione **[!UICONTROL Nuevo perfil]**.
1. Configure los detalles del perfil y seleccione **[!UICONTROL Guardar]**.

Para obtener más información (y ayuda sobre la administración de productos de Creative Cloud y Document Cloud), consulte [Identidad](https://helpx.adobe.com/es/enterprise/using/identity.html) en la [Guía del usuario de administración](https://helpx.adobe.com/es/enterprise/using/users.html).

**Ayuda relacionada**

* [Administrar usuarios](https://helpx.adobe.com/es/enterprise/using/users.html) in [!DNL Admin Console]
* [Administración de productos y perfiles](https://helpx.adobe.com/es/enterprise/using/manage-products.html) in [!DNL Admin Console].
* [Permisos de usuario de Enterprise](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=es) en la ayuda de Adobe Target para obtener más información.
* Vídeo: [Configuración de espacios de trabajo de Adobe Target en Adobe [!DNL Admin Console]](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-17521.html?lang=es)

## Delegación de funciones administrativas en usuarios {#delegate-rights}

Entrada [!DNL Admin Console], puede delegar derechos administrativos limitados en otros miembros de su organización. Las funciones delegadas permiten a los usuarios administrar el acceso al software de los usuarios finales, proporcionar capacidades de implementación de acceso y funcionar como delegados de asistencia.

Por ejemplo, puede:

* Permita que su director creativo conceda acceso a Creative Cloud.
* Permita que su director de marketing conceda acceso a Experience Cloud.
* Mantenga estas dos funciones separadas para que no puedan solapar las funciones de cada uno.

Al utilizar estas funciones, puede delegar la administración a otros sin proporcionar más capacidad de la que necesitan.

1. En el [!DNL Admin Console], seleccione **[!UICONTROL Usuarios]** y, a continuación, seleccione el nombre del usuario.

   ![Derechos administrativos en [!DNL Admin Console]](assets/edit-admin-rights.png)

1. Seleccione **[!UICONTROL Editar derechos de administrador]**.

   ![Edición de derechos administrativos en [!DNL Admin Console]](assets/edit-admin-rights-page.png)

1. Especifique los derechos de administración del usuario.
1. Seleccione **[!UICONTROL Guardar]**.

## Administración de usuarios y productos de Analytics {#section_97DE101F92CD494AB073893680992F1A}

Puede asignar permisos de acceso a informes de Analytics (grupos de informes, métricas, dimensiones, etc.) a un perfil de producto.

Por ejemplo, puede crear un perfil de producto que contenga varias herramientas de Analytics ([!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics] y [!UICONTROL Report Builder]). Estos perfiles contienen permisos para métricas y dimensiones específicas (incluyendo eVars), así como funciones como la creación de segmentos o métricas calculadas.

1. Inicie sesión en [[!DNL Admin Console]](https://adminconsole.adobe.com/enterprise), luego seleccione **[!UICONTROL Productos]**.
1. En la página [!UICONTROL Productos], seleccione su producto y después **[!UICONTROL Permisos]** (disponible solo para administradores).
1. Configure los permisos del perfil:

| Elemento | Descripción |
|--- |--- |
| Grupos de informes | Habilite permisos para grupos de informes específicos. |
| Métricas | Habilite permisos para tráfico, conversión, eventos personalizados, eventos de aplicaciones, reconocimiento de contenido, etc. |
| Dimensiones | Personalice el acceso de usuario a nivel granular con eVars, informes de tráfico, informes de aplicaciones e informes de rutas. |
| Herramientas de grupos de informes | Habilite permisos de usuario para Servicios web, Administración de grupos de informes, Herramientas e informes y Elementos de tablero. |
| Herramientas de Analytics | Habilite permisos de usuario para elementos generales (facturación, registros, etc.), administración de la compañía, herramientas, acceso a servicios web, Report Builder e integración de Data Connectors. Configuración de compañía desde el menú Personalizar [!DNL Admin Console] se han movido a las herramientas de Analytics. |

**Migración de cuentas de usuario**

Hay disponible una herramienta de migración de ID de usuario de Analytics para ayudar a los administradores a migrar cuentas de Administración de usuarios de Analytics a [Adobe [!DNL Admin Console]](https://adminconsole.adobe.com/enterprise/).

La migración de cuentas se está poniendo a disposición de los clientes por fases. El Adobe le avisará y ayudará cuando le llegue el momento de migrar las cuentas de usuario existentes de **[!UICONTROL Herramientas de administración]** > **[!UICONTROL Administración de usuarios]** a la [!DNL Admin Console].

Tras la migración, los usuarios iniciarán sesión con su Adobe ID (o Enterprise ID) y se autenticarán en sus aplicaciones y servicios de Experience Cloud en [experience.adobe.com](https://experience.adobe.com). Si los usuarios intentan iniciar sesión con accesos heredados ([!DNL my.omniture.com], [!DNL sc.omniture.com] y [!DNL experiencecloud.adobe.com]), se los redirigirá a [!DNL experience.adobe.com].

**Ayuda relacionada**

* [Analytics en la [!DNL Admin Console]](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=es)
* [Migración de ID de usuario de Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/user-product-management/migrate-users/c-migration-tool.html?lang=es)

## Administración de Adobe Target: perfiles de producto frente a espacios de trabajo {#section_3860AF177C9E4C7E9C390D36A414F353}

En Adobe Target, un espacio de trabajo es un perfil de producto. Permite que una organización asigne un conjunto de usuarios específico a un conjunto de propiedades concretas. En muchos aspectos, un espacio de trabajo es parecido a un grupo de informes en Adobe Analytics.

Consulte:

* [Permisos de usuario de Enterprise](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=es)
* [Administrar productos y perfiles](https://helpx.adobe.com/es/enterprise/using/manage-products.html)
* Vídeo: [Configuración de espacios de trabajo de Adobe Target en Adobe [!DNL Admin Console]](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-17521.html?lang=es)

## Administración de perfiles de producto, inquilinos y grupos de seguridad de Campaign {#section_09CDF75366444CF5810CF321B7C712F3}

Un *inquilino* en Campaign se muestra como un *producto* en la página Productos de Admin Console.

El *grupo de seguridad* se muestra como un perfil de producto.

Consulte [Administración de grupos y usuarios](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html?lang=es) para obtener información sobre los grupos de seguridad y la asignación de usuarios a los grupos de seguridad.

## Gestionar recopilación de datos de Experience Platform {#section_F2DA6778DD2D48AA8F794041971EE6B1}

La [!UICONTROL recopilación de datos] de Experience Platform se muestra en la página [!UICONTROL Productos] en [!UICONTROL Admin Console]. Puede incluir otras aplicaciones y servicios en un perfil de producto de recopilación de datos.

Invite a los usuarios a [!UICONTROL Recopilación de datos de Platform], y asigne funciones y derechos de usuario.

Consulte [Permisos de usuario](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html?lang=es) para obtener información sobre los permisos de usuario en [!DNL Admin Console] y sobre la configuración de derechos en perfiles.

## Experience Manager as a Cloud Service

Los clientes de Adobe Enterprise están representados como organizaciones en el Adobe [!DNL Admin Console]. Los clientes Experience Manager pueden utilizar el Adobe [!DNL Admin Console] para administrar las autorizaciones de productos y la autenticación IMS en Experience Manager as a [!UICONTROL Cloud Service].

Consulte la [Compatibilidad de IMS con Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/security/ims-support.html?lang=es).

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Cree usuarios de Audience Manager y asígnelos a grupos. También puede establecer límites de vista (características, segmentos, destinos y [!DNL AlgoModel]).

Consulte [Administración](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/administration/administration-overview.html?lang=es) en la ayuda de Audience Manager.

## Navegadores admitidos en Experience Cloud

* [!DNL Microsoft® Edge] (Microsoft® ha [dejado de ofrecer soporte](https://www.microsoft.com/es-es/WindowsForBusiness/End-of-IE-support) a Internet Explorer 8, 9 y 10. Debido a esto, Adobe no corrige los problemas notificados en relación con estas versiones específicas de Internet Explorer).
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Nota:** Aunque la interfaz de Experience Cloud admite estos exploradores, es posible que las aplicaciones individuales no los admitan todos. (Por ejemplo, [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/sys-reqs.html?lang=es) no es compatible con [!DNL Opera] y [!DNL Adobe Target] no es compatible con [!DNL Safari]).

### Soluciones y requisitos del producto

* [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/sys-reqs.html?lang=es)
* [Report Builder ](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/report-builder-setup/system-requirements.html?lang=es)
