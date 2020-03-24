---
description: Obtenga información sobre cómo iniciar sesión en Admin Console, administrar los permisos de usuario y perfiles del producto de Experience Cloud, y la compatibilidad con navegadores.
keywords: core services
seo-description: Obtenga información sobre cómo iniciar sesión en Admin Console, administrar los permisos de usuario y perfiles del producto de Experience Cloud, y la compatibilidad con navegadores.
seo-title: Administración de usuarios y productos de Experience Cloud
solution: Experience Cloud
title: Administración de usuarios y productos de Experience Cloud
uuid: aea4e4c3-f543-4e8d-b553-d838418477d6
translation-type: tm+mt
source-git-commit: b6bd75d92ce96e852a6e548362988a9b4d529fb9

---


# Administración de usuarios y productos de Experience Cloud {#topic_3FCB4099640647E3B2411ADBFCE81909}

Obtenga información sobre cómo iniciar sesión en Admin Console, administrar los permisos de usuario y perfiles del producto de Experience Cloud, y la compatibilidad con navegadores.

>[!IMPORTANT]
>
>La administración de usuarios en Admin Console introduce interfaces, opciones de navegación y términos nuevos. En la siguiente información se describen estos cambios y se proporcionan vínculos a recursos de ayuda adicionales. This help supplements the information in the [Enterprise Administration User Guide](https://helpx.adobe.com/enterprise/managing/user-guide.html) for all Adobe cloud products.

## Novedades en la administración de usuarios de Experience Cloud {#concept_06A0A13362F644FB90F947238407637A}

Descubra las últimas funciones de la administración de usuarios en Experience Cloud.

<!--

### Business ID type

Adobe is now introducing a new identity type: **Business ID**. This identity type, improves the control of user and product management, and content, while increasing the flexibility of Experience Cloud and Creative Cloud storage usage among your team. With the introduction of this new identity type, Adobe is migrating all Adobe IDs (owned by the individual) used for business to the new Business IDs (owned by the organization).

If you're an existing Creative Cloud for enterprise or teams customer, Adobe will migrate all your users on the Admin Console with Adobe IDs to Business IDs. If you're a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID. 

Beginning May 89, 2020, enterprise admins cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a users was a member of multiple organizations before the migration.)
-->

### Herramienta de administración

Los administradores pueden realizar la vista de una lista ordenable y filtrable de todos los usuarios de Experience Cloud y sus detalles en la herramienta de administración. Consulte [Vista de los usuarios de Experience Cloud en la herramienta](admin-tool-experience-cloud.md)de administración.

## Inicio de sesión en Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

Los administradores ya no administran usuarios en las soluciones. La administración de usuarios y productos para Experience Cloud ahora se realiza en Admin Console.

**Para iniciar sesión en Admin Console**

1. Navigate to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. Escriba su [Adobe ID o Enterprise ID](https://helpx.adobe.com/enterprise/help/identity.html) y contraseña.

Alternatively, from the Experience Cloud menu ( ![](assets/menu-icon.png)), click **[!UICONTROL Administration]** > **[!UICONTROL Launch Admin Console]**.

**Ayuda relacionada**

[Guía](https://helpx.adobe.com/enterprise/using/users.html) del usuario de administración de Creative Cloud y Documento Cloud. Algunos datos son relevantes para la administración de usuarios de Experience Cloud, como la [administración de tipos](https://helpx.adobe.com/enterprise/help/identity.html)de identidad.

[Inicie sesión y administre la configuración](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0) de perfil para administrar contraseñas, organizaciones y notificaciones.

## Perfiles y grupos de productos  {#section_AB50558124D541CF80A0D3D76D35A4BF}

La adición de perfiles de productos marca un cambio con respecto a cómo se administraban anteriormente los productos y servicios de la solución (mediante grupos). En Admin Console, los permisos se basan en perfiles de productos, que son grupos de productos y servicios que puede asignar a los usuarios.

Por ejemplo, en Analytics puede configurar una colección de herramientas de creación de informes, como Analysis Workspace y el Report Builder, además de grupos de informes, métricas, dimensiones, etc. Puede autorizar a los usuarios a un perfil de productos agregándolos al perfil. See [Assign Analytics access permissions to a product profile](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**Ayuda relacionada**

[Delegación de privilegios limitados de administración](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

Administre los permisos de usuarios y productos de Analytics en Admin Console.

[Asigne permisos de acceso de Analytics a un perfil de producto](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) (en esta página).

**Migración de cuentas de usuario**

Hay disponible una herramienta de migración de ID de usuario de Analytics para ayudar a los administradores a migrar cuentas de Administración de usuarios de Analytics a [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/).

La migración de cuentas se está poniendo a disposición de los clientes por fases. Adobe will notify and assist you when it is your time to migrate existing user accounts from **[!UICONTROL Admin Tools]** > **[!UICONTROL User Management]** to the Admin Console.

After the migration, users sign in using their Adobe ID (or Enterprise ID) and authenticate to their Experience Cloud solutions and services at [experiencecloud.adobe.com](https://experiencecloud.adobe.com). Si los usuarios intentan iniciar sesión con los accesos heredados ([!DNL my.omniture.com] y [!DNL sc.omniture.com]), se los redirigirá a [!DNL experiencecloud.adobe.com].

**Ayuda relacionada**

[Migración de ID de usuario de Analytics](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Target: Perfiles de producto vs. Espacios de trabajo {#section_3860AF177C9E4C7E9C390D36A414F353}

En Destinatario, un espacio de trabajo es un perfil de producto. Permite que una organización asigne un conjunto específico de usuarios a un conjunto específico de propiedades. En muchos aspectos, un espacio de trabajo es parecido a un grupo de informes en Adobe Analytics.

Consulte:
* [Permisos de usuario de Enterprise](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)
* [Administrar productos y perfiles](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* Vídeo: [Cómo configurar espacios de trabajo de Destinatario en Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Campaign: Perfiles de producto, inquilinos y grupos de seguridad {#section_09CDF75366444CF5810CF321B7C712F3}

Un *inquilino* en Campaña se muestra como un *producto* en la página Productos de la Consola de administración.

*El grupo* de seguridad se muestra como un perfil de producto.

Consulte [Administración de grupos y usuarios](https://helpx.adobe.com/campaign/standard/administration/using/managing-groups-and-users.html) para obtener información sobre los grupos de seguridad y la asignación de usuarios a los grupos de seguridad.

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Launch se muestra en la página Productos de la Consola de administración. Puede incluir otras soluciones y servicios en un perfil de productos de Launch.

Consulte Administración [de usuarios](https://docs.adobelaunch.com/launch-reference/administration/user-permissions) para obtener información sobre los permisos de usuario en Admin Console y configurar opciones específicas de Launch, incluida la asignación de derechos a perfiles.

## Administrador dinámico de etiquetas {#section_3A41CF2BD5994B9891537D063571D4ED}

Invite a usuarios a la Dynamic Tag Management, asigne funciones de usuario y añada usuarios a grupos.

See [Users and Permissions](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) for information about how to invite users to Dynamic Tag Management and assign user roles and add users to groups.

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Cree usuarios del Administrador de Audiencias y asígnelos a grupos. También puede establecer límites de vista (características, segmentos, destinos y AlgoModel).

Consulte [Administración](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) en la ayuda del Administrador de Audiencias.

## Administración de productos de Experience Cloud {#task_16335111C52D40E9BAC73D0699584DBF}

Cree un perfil de producto y asígnelo a un grupo de permisos.

Al invitar a un usuario a una organización, puede darle acceso a productos y perfiles de productos. También puede delegar permisos administrativos limitados en un usuario. Del mismo modo, puede crear grupos de usuarios y luego agregar el grupo a un perfil de productos para habilitar el acceso.

1. In the [Admin Console](https://adminconsole.adobe.com/enterprise/), click **[!UICONTROL Products]**.
1. Haga clic en **[!UICONTROL Nuevo perfil]**.
1. Configure los detalles del perfil y, después, haga clic en **[!UICONTROL Siguiente]**.
1. Haga clic en **[!UICONTROL Finalizado]**.

Encontrará más ayuda en:

* [Administrar productos y perfiles](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* [Permisos](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html) de usuario de Enterprise en la ayuda de Destinatario para obtener más información.
* Vídeo: [Cómo configurar espacios de trabajo de Destinatario en Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Asignación de permisos de acceso de Analytics a un perfil de producto {#task_040673FE3E3E429B9531FBCB8B6A4391}

Asigne permisos de acceso a informes de Analytics (grupos de informes, métricas, dimensiones, etc.) a un perfil de producto.

Por ejemplo, puede crear un perfil de producto que contenga varias herramientas de Analytics ([!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics] y [!UICONTROL Report Builder]), con permiso para métricas y dimensiones concretas (incluidas eVars) y funciones como la creación de segmentos o métricas calculadas.

1. Sign in to the [Admin Console](https://adminconsole.adobe.com/enterprise), then click **[!UICONTROL Products]** (or click your product name).
1. En el perfil de producto, haga clic en **[!UICONTROL Permisos]** (disponible solo para administradores).
1. Configure los permisos del perfil:

| Elemento | Descripción |
|--- |--- |
| Grupos de informes | Habilite permisos para grupos de informes específicos. |
| Métricas | Habilite permisos para tráfico, conversión, eventos personalizados, eventos de soluciones, reconocimiento de contenido, etc. |
| Dimensiones | Personalice el acceso de usuarios a nivel granular con eVars, informes de tráfico, informes de soluciones e informes de rutas. |
| Herramientas de grupos de informes | Habilite permisos de usuario para Servicios Web, Administración de grupos de informes, Herramientas e informes y Elementos de Panel. |
| Herramientas de Analytics | Habilite permisos de usuario para elementos generales (facturación, registros, etc.), administración de la empresa, herramientas, acceso a servicios web, Report Builder e integración de Data Connectors. Las configuraciones de empresa de la categoría Personalizar Admin Console se han trasladado a las herramientas de Analytics. |

## Delegación de funciones administrativas en usuarios {#task_3A072C4AA9734BC59FFA7E015271BC7E}

En Admin Console, puede delegar derechos administrativos limitados en otros miembros de la organización. Las funciones delegadas permiten a los usuarios administrar el acceso al software a los usuarios finales, proporcionar capacidades de implementación de acceso y funcionar como delegados de asistencia.

Por ejemplo, puede:

* Permita que su director creativo conceda acceso a Creative Cloud.
* Permita que su director de marketing conceda acceso a Experience Cloud.
* Mantenga estas dos funciones separadas para que no puedan superar las funciones de cada uno.

Al utilizar estas funciones, puede delegar la administración a otros sin proporcionar más capacidad de la que necesitan.

1. En Admin Console, haga clic en **[!UICONTROL Usuarios]** y, a continuación, haga clic en el nombre del usuario.
1. Haga clic en **[!UICONTROL Editar derechos de administrador]**.
1. Configure los derechos de administración del usuario.
1. Haga clic en **[!UICONTROL Siguiente]** para revisar la configuración y, a continuación, haga clic en **[!UICONTROL Guardar]**.

## Navegadores compatibles y requisitos del sistema {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Exploradores admitidos en Experience Cloud.

Los exploradores admitidos por Experience Cloud incluyen:

* [!DNL Microsoft Edge] (Microsoft ha [finalizado la compatibilidad](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) con Internet Explorer 8, 9 y 10. Como tal, Adobe no corregirá los problemas notificados con estas versiones específicas de Internet Explorer).
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Nota:** Aunque la interfaz de Experience Cloud admite estos exploradores, es posible que las soluciones individuales no los admitan a todos. (Por ejemplo, [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html) no es compatible con [!DNL Opera] y [Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html) no es compatible con [!DNL Safari]).

**Soluciones y requisitos del producto**

* [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html)
* [Report Builder ](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html)
