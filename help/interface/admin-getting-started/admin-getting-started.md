---
description: Obtenga información sobre el inicio de sesión en Adobe Admin Console, y la administración de permisos de usuarios, perfiles de productos y compatibilidad de exploradores en Experience Cloud.
keywords: Experience Cloud services
solution: Experience Cloud
title: 'Información sobre la administración de usuarios y productos '
index: true
translation-type: ht
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: ht
source-wordcount: '1432'
ht-degree: 100%

---


# Administración de usuarios y productos de Experience Cloud {#topic_3FCB4099640647E3B2411ADBFCE81909}

Obtenga más información sobre el inicio de sesión en Admin Console y la administración de permisos de usuarios, perfiles de producto y compatibilidad de exploradores en Experience Cloud.

>[!IMPORTANT]
>
>La administración de usuarios en Admin Console introduce interfaces, opciones de navegación y términos nuevos. En la siguiente información se describen estos cambios y se proporcionan vínculos a recursos de ayuda adicionales. Esta ayuda complementa la información de la [Guía del usuario de administración de Enterprise](https://helpx.adobe.com/es/enterprise/managing/user-guide.html) para todos los productos de la nube de Adobe.

## Novedades en la administración de usuarios de Experience Cloud {#concept_06A0A13362F644FB90F947238407637A}

Descubra las últimas funciones de la administración de usuarios en Experience Cloud.

<!-- ### Business ID type

Adobe is introducing an identity type called Business ID. This identity type improves the control of user and product management. Adobe is migrating all Adobe IDs (owned by individuals) that are used for business to the new enterprise Business IDs owned by your organization.

If you are an existing Experience Cloud customer, Adobe will migrate all your users with Adobe IDs in the Admin Console to Business IDs. If you are a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID.

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a user was a member of multiple organizations before the migration.)

Beginning May 2020, enterprise administrators cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM-->

### Herramienta de administración

Los administradores pueden ver una lista de los usuarios de Experience Cloud que pueden ordenar y filtrar y sus detalles en la herramienta de administración. Consulte [Vista de los usuarios de Experience Cloud en la herramienta de administración](admin-tool-experience-cloud.md).

## Inicio de sesión en Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

Los administradores ya no administran usuarios en las soluciones. La administración de usuarios y productos para Experience Cloud ahora se realiza en Admin Console.

Para iniciar sesión en Admin Console:

1. Vaya a [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. Escriba su [Adobe ID o Enterprise ID](https://helpx.adobe.com/es/enterprise/help/identity.html) y contraseña.

En el menú Experience Cloud (![](assets/menu-icon.png)), también puede hacer clic en **[!UICONTROL Administración]** > **[!UICONTROL Iniciar Admin Console]**.

**Ayuda relacionada**

[Guía del usuario de administración](https://helpx.adobe.com/es/enterprise/using/users.html) de Creative Cloud y Document Cloud. Algunos datos son relevantes para la administración de usuarios de Experience Cloud, como la [administración de tipos de identidad](https://helpx.adobe.com/es/enterprise/help/identity.html).

[Inicie sesión y administre la configuración de perfil](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0) para administrar contraseñas, organizaciones y notificaciones.

## Perfiles y grupos de productos {#section_AB50558124D541CF80A0D3D76D35A4BF}

Añadir perfiles de productos marca un cambio con respecto a cómo se administraban anteriormente los productos y servicios de la solución (mediante grupos). En Admin Console, los permisos se basan en perfiles de productos, que son grupos de productos y servicios que puede asignar a los usuarios.

Por ejemplo, en Analytics puede configurar una colección de herramientas de creación de informes, como Analysis Workspace y el Report Builder, además de grupos de informes, métricas, dimensiones, etc. Puede autorizar a los usuarios a un perfil de productos agregándolos al perfil. Consulte [Asignación de permisos de acceso de Analytics a un perfil de producto](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**Ayuda relacionada**

[Delegación de privilegios limitados de administración](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

Administre los permisos de usuarios y productos de Analytics en Admin Console.

[Asigne permisos de acceso de Analytics a un perfil de producto](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) (en esta página).

**Migración de cuentas de usuario**

Hay disponible una herramienta de migración de ID de usuario de Analytics para ayudar a los administradores a migrar cuentas de Administración de usuarios de Analytics a [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/).

La migración de cuentas se está poniendo a disposición de los clientes por fases. Adobe le avisará y ayudará cuando le llegue el momento de migrar las cuentas de usuario existentes desde **[!UICONTROL Herramientas de administración]** > **[!UICONTROL Administración de usuarios]** a Admin Console.

Tras la migración, los usuarios iniciarán sesión con su Adobe ID (o Enterprise ID) y se autenticarán en sus soluciones y servicios de Experience Cloud en [experiencecloud.adobe.com](https://experiencecloud.adobe.com). Si los usuarios intentan iniciar sesión con los accesos heredados ([!DNL my.omniture.com] y [!DNL sc.omniture.com]), se los redirigirá a [!DNL experiencecloud.adobe.com].

**Ayuda relacionada**

[Migración de ID de usuario de Analytics](https://docs.adobe.com/content/help/es-ES/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Adobe Target: Perfiles de producto vs. Espacios de trabajo {#section_3860AF177C9E4C7E9C390D36A414F353}

En Adobe Target, un espacio de trabajo es un perfil de producto. Permite que una organización asigne un conjunto de usuarios específico a un conjunto de propiedades concretas. En muchos aspectos, un espacio de trabajo es parecido a un grupo de informes en Adobe Analytics.

Consulte:

* [Permisos de usuario de Enterprise](https://docs.adobe.com/content/help/es-ES/target/using/administer/manage-users/enterprise/property-channel.html)
* [Administrar productos y perfiles](https://helpx.adobe.com/es/enterprise/using/manage-products-and-profiles.html)
* Vídeo: [Configurar espacios de trabajo de Adobe Target en Adobe Admin Console](https://helpx.adobe.com/es/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Campaign: Perfiles de producto, inquilinos y grupos de seguridad {#section_09CDF75366444CF5810CF321B7C712F3}

Un *inquilino* en Campaign se muestra como un *producto* en la página Productos de Admin Console.

El *grupo de seguridad* se muestra como un perfil de producto.

Consulte [Administración de grupos y usuarios](https://docs.adobe.com/content/help/es-ES/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html) para obtener información sobre los grupos de seguridad y la asignación de usuarios a los grupos de seguridad.

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Launch se muestra en la página Productos de Admin Console. Puede incluir otras soluciones y servicios en un perfil de productos de Launch.

Consulte [Administración de usuarios](https://docs.adobe.com/content/help/es-ES/launch/using/reference/admin/user-permissions.html) para obtener información sobre los permisos de usuario en Admin Console y configurar opciones específicas de Launch, incluida la asignación de derechos a perfiles.

## Experience Manager as a Cloud Service

Los clientes de Adobe Enterprise están representados como organizaciones de IMS en Adobe Admin Console. Es el portal que utilizan los clientes de Adobe para administrar las asignaciones de productos para sus usuarios y grupos. Los clientes de AEM pueden utilizar Adobe Admin Console para administrar sus derechos de producto y la autenticación IMS en AEM as a Cloud Service.

[Compatibilidad de IMS con AEM as a Cloud Service](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/security/ims-support.html#managing-products-and-user-access-in-admin-console).

## Administrador dinámico de etiquetas {#section_3A41CF2BD5994B9891537D063571D4ED}

Invite a usuarios a la Dynamic Tag Management, asigne funciones de usuario y añada usuarios a grupos.

Consulte [Usuarios y permisos](https://docs.adobe.com/content/help/es-ES/dtm/using/admin/users.html) para obtener información sobre cómo invitar a usuarios a Dynamic Tag Management, asignar funciones de usuario y agregar usuarios a grupos.

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Cree usuarios de Audience Manager y asígnelos a grupos. También puede establecer límites de vista (características, segmentos, destinos y [!DNL AlgoModel]).

Consulte [Administración](https://docs.adobe.com/content/help/es-ES/dtm/using/admin/users.html) en la ayuda de Audience Manager.

## Administración de productos de Experience Cloud {#task_16335111C52D40E9BAC73D0699584DBF}

Cree un perfil de producto y asígnelo a un grupo de permisos.

Al invitar a un usuario a una organización, puede darle acceso a productos y perfiles de productos. También puede delegar permisos administrativos limitados en un usuario. Del mismo modo, puede crear grupos de usuarios y luego agregar el grupo a un perfil de productos para habilitar el acceso.

1. En [Admin Console](https://adminconsole.adobe.com/enterprise/), haga clic en **[!UICONTROL Productos]**.
1. Haga clic en **[!UICONTROL Nuevo perfil]**.
1. Configure los detalles del perfil y, después, haga clic en **[!UICONTROL Siguiente]**.
1. Haga clic en **[!UICONTROL Finalizado]**.

Encontrará más ayuda en:

* [Administrar productos y perfiles](https://helpx.adobe.com/es/enterprise/using/manage-products-and-profiles.html)
* [Permisos de usuario de Enterprise](https://docs.adobe.com/content/help/es-ES/target/using/administer/manage-users/enterprise/property-channel.html) en la ayuda de Adobe Target para obtener más información.
* Vídeo: [Configurar espacios de trabajo de Adobe Target en Adobe Admin Console](https://helpx.adobe.com/es/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Asignación de permisos de acceso de Analytics a un perfil de producto {#task_040673FE3E3E429B9531FBCB8B6A4391}

Asigne permisos de acceso a informes de Analytics (grupos de informes, métricas, dimensiones, etc.) a un perfil de producto.

Por ejemplo, puede crear un perfil de producto que contenga varias herramientas de Analytics ([!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics] y [!UICONTROL Report Builder]), con permiso para métricas y dimensiones concretas (incluidas eVars) y funciones como la creación de segmentos o métricas calculadas.

1. Inicie sesión en [Admin Console](https://adminconsole.adobe.com/enterprise) y, a continuación, haga clic en **[!UICONTROL Productos]** (o haga clic en el nombre de su producto).
1. En el perfil de producto, haga clic en **[!UICONTROL Permisos]** (disponible solo para administradores).
1. Configure los permisos del perfil:

| Elemento | Descripción |
|--- |--- |
| Grupos de informes | Habilite permisos para grupos de informes específicos. |
| Métricas | Habilite permisos para tráfico, conversión, eventos personalizados, eventos de soluciones, reconocimiento de contenido, etc. |
| Dimensiones | Personalice el acceso de usuarios a nivel granular con eVars, informes de tráfico, informes de soluciones e informes de rutas. |
| Herramientas de grupos de informes | Habilite permisos de usuario para Servicios web, Administración de grupos de informes, Herramientas e informes y Elementos de tablero. |
| Herramientas de Analytics | Habilite permisos de usuario para elementos generales (facturación, registros, etc.), administración de la empresa, herramientas, acceso a servicios web, Report Builder e integración de Data Connectors. Las configuraciones de empresa de la categoría Personalizar Admin Console se han trasladado a las herramientas de Analytics. |

## Delegación de funciones administrativas en usuarios {#task_3A072C4AA9734BC59FFA7E015271BC7E}

En Admin Console, puede delegar derechos administrativos limitados en otros miembros de la organización. Las funciones delegadas permiten a los usuarios administrar el acceso al software de los usuarios finales, proporcionar capacidades de implementación de acceso y funcionar como delegados de asistencia.

Por ejemplo, puede:

* Permita que su director creativo conceda acceso a Creative Cloud.
* Permita que su director de marketing conceda acceso a Experience Cloud.
* Mantenga estas dos funciones separadas para que no puedan solapar las funciones de cada uno.

Al utilizar estas funciones, puede delegar la administración a otros sin proporcionar más capacidad de la que necesitan.

1. En Admin Console, haga clic en **[!UICONTROL Usuarios]** y, a continuación, haga clic en el nombre del usuario.
1. Haga clic en **[!UICONTROL Editar derechos de administrador]**.
1. Configure los derechos de administración del usuario.
1. Haga clic en **[!UICONTROL Siguiente]** para revisar la configuración y, a continuación, haga clic en **[!UICONTROL Guardar]**.

## Navegadores compatibles y requisitos del sistema {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Exploradores admitidos en Experience Cloud.

* [!DNL Microsoft Edge] (Microsoft ha [dejado de ofrecer asistencia](https://www.microsoft.com/es-es/WindowsForBusiness/End-of-IE-support) para Internet Explorer 8, 9 y 10. Debido a esto, Adobe no corregirá los problemas notificados en relación con estas versiones específicas de Internet Explorer).
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Nota:** Aunque la interfaz de Experience Cloud admite estos exploradores, es posible que las soluciones individuales no los admitan a todos. (Por ejemplo, [Analytics](https://docs.adobe.com/content/help/es-ES/analytics/admin/sys-reqs.html) no es compatible con [!DNL Opera] y [ Adobe Target](https://docs.adobe.com/help/es-ES/target/using/implement-target/before-implement/supported-browsers.html) no es compatible con [!DNL Safari]).

### Soluciones y requisitos del producto

* [Analytics](https://docs.adobe.com/content/help/es-ES/analytics/admin/sys-reqs.html)
* [Report Builder ](https://docs.adobe.com/content/help/es-ES/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/es-ES/target/using/implement-target/before-implement/supported-browsers.html)
