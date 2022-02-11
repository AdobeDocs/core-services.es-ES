---
title: Administración de usuarios y productos
description: Obtenga información sobre cómo iniciar sesión en el Admin Console y administrar los permisos de usuario y los perfiles de producto del Experience Cloud. Obtenga información acerca de la delegación de derechos administrativos a usuarios de Experience Cloud y sobre la compatibilidad del explorador con Experience Cloud.
solution: Admin
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: af9eda5b-d984-44b7-a7b3-52dfc4e03d8f
source-git-commit: f03a0702b1f95dd8dfafbe84afc85e48f2aa9e5c
workflow-type: tm+mt
source-wordcount: '1567'
ht-degree: 69%

---

# Administración de usuarios y productos de Experience Cloud

Obtenga información sobre cómo iniciar sesión en el Admin Console, administrar los permisos de usuario y los perfiles de producto del Experience Cloud y la compatibilidad con el explorador.

>[!IMPORTANT]
>
>La siguiente información está diseñada específicamente para aplicaciones de Experience Cloud. Esta información complementa la información administrativa más general de la [Guía del usuario de administración de Enterprise](https://helpx.adobe.com/es/enterprise/admin-guide.html) para todos los productos en la nube de Adobe.

Puede ver una lista, que puede ordenarse y filtrarse, de todos los usuarios de Experience Cloud y sus detalles en la herramienta de administración. Consulte [Vista de los usuarios de Experience Cloud en la herramienta de administración](admin-tool-experience-cloud.md).

## Autenticación de usuarios Experience Cloud (migración planificada){#migration}

A partir de febrero de 2022, el Adobe está actualizando su sistema de gestión de perfiles para permitir a las organizaciones administrar mejor los derechos empresariales a perfiles individuales. Como tal, todos los usuarios con un Perfil personal, que corresponde a un Adobe ID individual (Tipo1), se migrarán a un nuevo Perfil comercial. Este perfil corresponde a un _ID empresarial_ (Type2e).

Consulte [Tipos de identidad en Adobe Admin Console](https://helpx.adobe.com/es/enterprise/using/identity.html) para obtener información sobre los tipos de identidad.

### Proceso de migración

Cuando sea el momento de la migración, los administradores de la organización recibirán un mensaje de correo electrónico de notificación 30 días antes de la migración.

* La migración se programará entre las 22:00. - 6 a.m., según la zona horaria principal de la organización o el fin de semana.
* Durante la migración, la aplicación de Experience Cloud puede estar inaccesible durante aproximadamente 15 minutos y el Admin Console puede estar inaccesible hasta 30 minutos. De lo contrario, esta migración se realizará sin problemas.

### Cambios después de la migración

Admin Console

* Los administradores con varias cuentas pueden ver un selector de perfil al iniciar sesión [!UICONTROL Admin Console].
* Los usuarios individuales de Adobe ID se actualizarán a Business ID.
* El directorio de ID de negocio se agregará en **[!UICONTROL Configuración]** > **[!UICONTROL Identidad]** > **[!UICONTROL Directorios]**.

   ![Identidad de Admin Console: ID de empresa](assets/identity-home.png)

### Inicio de sesión después de la migración

La experiencia de inicio de sesión no cambia con esta actualización:

1. Iniciar sesión en `experience.adobe.com` usando las mismas credenciales.

1. Se crea un nuevo perfil asociado al ID de negocio. Se le pedirá que **[!UICONTROL Unirse ahora]** o **[!UICONTROL Omitir]**.

1. Al tomar una de las opciones, se crea una experiencia de página de aterrizaje existente.

1. Un perfil de Adobe está asociado a cada plan de negocio y proporciona la capacidad de organizar los recursos creados a partir de ofertas adicionales de Adobe Cloud (Creative Cloud y Document Cloud).

Para obtener más información, consulte [Presentación de perfiles de Adobe](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html).

## ¿Qué es un perfil de producto? {#section_AB50558124D541CF80A0D3D76D35A4BF}

Los _[!UICONTROL perfiles de producto]_ son grupos de productos y servicios que puede asignar a los usuarios. En Experience Cloud, los permisos se basan en el perfil de un producto, no en el usuario. (Sin embargo, puede delegar derechos administrativos a usuarios específicos).

Por ejemplo, en Analytics puede configurar una colección de herramientas de creación de informes, como Analysis Workspace y Report Builder, además de grupos de informes, métricas y dimensiones. Puede conceder permiso para un perfil de producto agregando usuarios al perfil.

* Consulte [Asignación de permisos de acceso de Analytics a un perfil de producto](admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) en esta página.
* Consulte [Delegación de funciones administrativas en usuarios](#delegate-rights) en esta página.

## Administrar perfiles de producto del Experience Cloud {#task_16335111C52D40E9BAC73D0699584DBF}

Puede crear un perfil de producto y asignarlo a un grupo de permisos.

Al invitar a un usuario a una organización, puede darle acceso a productos y perfiles de producto. También puede delegar permisos administrativos limitados en un usuario. Del mismo modo, puede crear grupos de usuarios y luego agregar el grupo a un perfil de producto para habilitar el acceso.

1. En [Admin Console](https://adminconsole.adobe.com/enterprise/), seleccione **[!UICONTROL Productos]**.
1. Seleccione el nombre de su organización.
1. Seleccione **[!UICONTROL Nuevo perfil]**.
1. Configure los detalles del perfil y seleccione **[!UICONTROL Guardar]**.

Para obtener más información (y ayuda sobre la administración de productos de Creative Cloud y Document Cloud), consulte [Identidad](https://helpx.adobe.com/es/enterprise/admin-guide.html/es/enterprise/using/identity.ug.html) en la [Guía del usuario de administración](https://helpx.adobe.com/es/enterprise/admin-guide.html/es/enterprise/using/users.ug.html).

**Ayuda relacionada**

* [Administre productos y perfiles](https://helpx.adobe.com/es/enterprise/admin-guide.html/es/enterprise/using/manage-products.ug.html) en la Guía del usuario de administración.
* [Permisos de usuario de Enterprise](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=es) en la ayuda de Adobe Target para obtener más información.
* Vídeo: [Configurar espacios de trabajo de Adobe Target en Adobe Admin Console](https://helpx.adobe.com/es/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Delegación de funciones administrativas en usuarios {#delegate-rights}

En Admin Console, puede delegar derechos administrativos limitados en otros miembros de la organización. Las funciones delegadas permiten a los usuarios administrar el acceso al software de los usuarios finales, proporcionar capacidades de implementación de acceso y funcionar como delegados de asistencia.

Por ejemplo, puede:

* Permita que su director creativo conceda acceso a Creative Cloud.
* Permita que su director de marketing conceda acceso a Experience Cloud.
* Mantenga estas dos funciones separadas para que no puedan solapar las funciones de cada uno.

Al utilizar estas funciones, puede delegar la administración a otros sin proporcionar más capacidad de la que necesitan.

1. En Admin Console, seleccione **[!UICONTROL Usuarios]** y luego el nombre del usuario.

   ![Derechos administrativos en Admin Console](assets/edit-admin-rights.png)

1. Seleccione **[!UICONTROL Editar derechos de administrador]**.

   ![Editar derechos administrativos en Admin Console](assets/edit-admin-rights-page.png)

1. Especifique los derechos de administración del usuario.
1. Seleccione **[!UICONTROL Guardar]**.

## Administración de usuarios y productos de Analytics {#section_97DE101F92CD494AB073893680992F1A}

Puede asignar permisos de acceso a informes de Analytics (grupos de informes, métricas, dimensiones, etc.) a un perfil de producto.

Por ejemplo, puede crear un perfil de producto que contenga varias herramientas de Analytics ([!UICONTROL Analysis Workspace], [!UICONTROL Informes y análisis]y [!UICONTROL Report Builder]). Estos perfiles contienen permisos para métricas y dimensiones específicas (incluyendo eVars), así como funciones como la creación de segmentos o métricas calculadas.

1. Inicie sesión en [Admin Console](https://adminconsole.adobe.com/enterprise) y seleccione **[!UICONTROL Productos]**.
1. En la página [!UICONTROL Productos], seleccione su producto y después **[!UICONTROL Permisos]** (disponible solo para administradores).
1. Configure los permisos del perfil:

| Elemento | Descripción |
|--- |--- |
| Grupos de informes | Habilite permisos para grupos de informes específicos. |
| Métricas | Habilite permisos para tráfico, conversión, eventos personalizados, eventos de aplicaciones, reconocimiento de contenido, etc. |
| Dimensiones | Personalice el acceso de usuario a nivel granular con eVars, informes de tráfico, informes de aplicaciones e informes de rutas. |
| Herramientas de grupos de informes | Habilite permisos de usuario para Servicios web, Administración de grupos de informes, Herramientas e informes y Elementos de tablero. |
| Herramientas de Analytics | Habilite permisos de usuario para elementos generales (facturación, registros, etc.), administración de la compañía, herramientas, acceso a servicios web, Report Builder e integración de Data Connectors. Las configuraciones de empresa de la categoría Personalizar Admin Console se han trasladado a las herramientas de Analytics. |

**Migración de cuentas de usuario**

Hay disponible una herramienta de migración de ID de usuario de Analytics para ayudar a los administradores a migrar cuentas de Administración de usuarios de Analytics a [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/).

La migración de cuentas se está poniendo a disposición de los clientes por fases. Adobe le avisará y ayudará cuando le llegue el momento de migrar las cuentas de usuario existentes desde **[!UICONTROL Herramientas de administración]** > **[!UICONTROL Administración de usuarios]** a Admin Console.

Tras la migración, los usuarios iniciarán sesión con su Adobe ID (o Enterprise ID) y se autenticarán en sus aplicaciones y servicios de Experience Cloud en [experience.adobe.com](https://experience.adobe.com). Si los usuarios intentan iniciar sesión con accesos heredados ([!DNL my.omniture.com], [!DNL sc.omniture.com] y [!DNL experiencecloud.adobe.com]), se los redirigirá a [!DNL experience.adobe.com].

**Ayuda relacionada**

* [Analytics en Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/home.html?lang=en)
* [Migración de ID de usuario de Analytics](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/migrate-users/c-migration-tool.html?lang=es)

## Administrar Adobe Target: Perfiles de producto vs. Espacios de trabajo {#section_3860AF177C9E4C7E9C390D36A414F353}

En Adobe Target, un espacio de trabajo es un perfil de producto. Permite que una organización asigne un conjunto de usuarios específico a un conjunto de propiedades concretas. En muchos aspectos, un espacio de trabajo es parecido a un grupo de informes en Adobe Analytics.

Consulte:

* [Permisos de usuario de Enterprise](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en)
* [Administrar productos y perfiles](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html)
* Vídeo: [Configurar espacios de trabajo de Adobe Target en Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Administrar perfiles de producto, inquilinos y grupos de seguridad de Campaign {#section_09CDF75366444CF5810CF321B7C712F3}

Un *inquilino* en Campaign se muestra como un *producto* en la página Productos de Admin Console.

*Grupo de seguridad* se muestra como un perfil de producto.

Consulte [Administración de grupos y usuarios](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html?lang=es) para obtener información sobre los grupos de seguridad y la asignación de usuarios a los grupos de seguridad.

## Administración de la recopilación de datos de Experience Platform (Launch) {#section_F2DA6778DD2D48AA8F794041971EE6B1}

La [!UICONTROL recopilación de datos] de Experience Platform ([!UICONTROL Launch]) se muestra en la página [!UICONTROL Productos] en [!UICONTROL Admin Console]. Puede incluir otras aplicaciones y servicios en un perfil de producto de Launch.

Invite a los usuarios a [!UICONTROL Platform Launch], y asigne funciones y derechos de usuario.

Consulte [Permisos de usuario](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html?lang=es) para obtener información sobre los permisos de usuario en Admin Console y configurar opciones específicas de Launch, incluida la asignación de derechos a perfiles.

## Experience Manager as a Cloud Service

Los clientes de Adobe Enterprise están representados como organizaciones en Adobe [!UICONTROL Admin Console]. Los clientes de Experience Manager pueden utilizar Adobe [!UICONTROL Admin Console] para administrar sus derechos de producto y la autenticación IMS en Experience Manager as a [!UICONTROL Cloud Service].

Consulte la [Compatibilidad de IMS con Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=es).

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Cree usuarios de Audience Manager y asígnelos a grupos. También puede establecer límites de vista (características, segmentos, destinos y [!DNL AlgoModel]).

Consulte [Administración](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/administration/administration-overview.html?lang=es) en la ayuda de Audience Manager.

## Exploradores admitidos en Experience Cloud

* [!DNL Microsoft® Edge] (Microsoft® ha [dejado de ofrecer soporte](https://www.microsoft.com/es-es/WindowsForBusiness/End-of-IE-support) a Internet Explorer 8, 9 y 10. Debido a esto, Adobe no corrige los problemas notificados en relación con estas versiones específicas de Internet Explorer).
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Nota:** Aunque la interfaz de Experience Cloud admite estos exploradores, es posible que las aplicaciones individuales no los admitan todos. (Por ejemplo, [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=es) no es compatible con [!DNL Opera] y [ Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=es) no es compatible con [!DNL Safari]).

### Soluciones y requisitos del producto

* [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en)
* [Report Builder ](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/report-builder-setup/system-requirements.html?lang=es)
* [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en)
