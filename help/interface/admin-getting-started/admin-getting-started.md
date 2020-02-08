---
description: Obtenga información sobre cómo iniciar sesión en Admin Console, administrar los permisos de usuario y perfiles de producto de Experience Cloud y la compatibilidad con navegadores.
keywords: core services
seo-description: Obtenga información sobre cómo iniciar sesión en Admin Console, administrar los permisos de usuario y perfiles de producto de Experience Cloud y la compatibilidad con navegadores.
seo-title: Administración de usuarios y productos de Experience Cloud
solution: Experience Cloud
title: Administración de usuarios y productos de Experience Cloud
uuid: aea4e4c3-f543-4e8d-b553-d838418477d6
translation-type: tm+mt
source-git-commit: 02b0163b95c24eb58bf2379c3e0d9f5f31c40925

---


# Administración de usuarios y productos de Experience Cloud {#topic_3FCB4099640647E3B2411ADBFCE81909}

Obtenga información sobre cómo iniciar sesión en Admin Console, administrar los permisos de usuario y perfiles de producto de Experience Cloud y la compatibilidad con navegadores.

>[!IMPORTANT]
>
>La administración de usuarios en Admin Console introduce interfaces, opciones de navegación y términos nuevos. En la siguiente información se describen estos cambios y se proporcionan vínculos a recursos de ayuda adicionales. Esta ayuda complementa la información de la [Guía del usuario de administración de Enterprise](https://helpx.adobe.com/enterprise/managing/user-guide.html) para todos los productos de nube de Adobe.

## Novedades en la administración de usuarios de Experience Cloud {#concept_06A0A13362F644FB90F947238407637A}

Descubra las últimas funciones de la administración de usuarios en Experience Cloud.

## Inicio de sesión en Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

Los administradores ya no administran usuarios en las soluciones. Ahora, la administración de usuarios y productos para Experience Cloud se realiza en Admin Console.

**Para iniciar sesión en Admin Console**

1. Navigate to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. Escriba su [Adobe ID o Enterprise ID](https://helpx.adobe.com/enterprise/help/identity.html) y su contraseña.

En el menú Experience Cloud (![](assets/menu-icon.png)), también puede hacer clic en **[!UICONTROL Administración]** > **[!UICONTROL Iniciar Admin Console]**.

**Ayuda relacionada**

[Guía del usuario de administración](https://helpx.adobe.com/enterprise/using/users.html) para Creative Cloud y Document Cloud. Hay cierta información relevante para la administración de usuarios de Experience Cloud, como la [administración de los tipos de identidad](https://helpx.adobe.com/enterprise/help/identity.html).

Consulte [Inicio de sesión y administración de la configuración de perfil](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0) para administrar las contraseñas, las organizaciones y las notificaciones.

## Perfiles y grupos de productos  {#section_AB50558124D541CF80A0D3D76D35A4BF}

La llegada de los perfiles de producto marca un cambio respecto a la anterior administración (mediante grupos) de los productos y servicios de las soluciones. En Admin Console, los permisos se basan en perfiles de producto, que son grupos de productos y servicios que usted asigna a los usuarios.

Por ejemplo, en Analytics puede configurar una colección de herramientas de creación de informes, como Analysis Workspace y el Report Builder, además de grupos de informes, métricas, dimensiones, etc. Puede otorgar a los usuarios permiso para un perfil de producto añadiéndolos a dicho perfil. Consulte [Asignación de permisos de acceso de Analytics a un perfil de producto](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**Ayuda relacionada**

[Delegación de privilegios limitados de administración](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

Administre los permisos de usuarios y productos de Analytics en Admin Console.

[Asigne permisos de acceso de Analytics a un perfil de producto](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) (en esta página).

**Migración de cuentas de usuario**

Hay disponible una herramienta de migración de ID de usuario de Analytics para ayudar a los administradores a migrar cuentas de Administración de usuarios de Analytics a [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/).

La migración de cuentas se está poniendo a disposición de los clientes por fases. Adobe le avisará y ayudará cuando le llegue el momento de migrar las cuentas de usuario existentes de **[!UICONTROL Herramientas de administración]** > **[!UICONTROL Administración de usuarios]** a Admin Console.

After the migration, users sign in using their Adobe ID (or Enterprise ID) and authenticate to their Experience Cloud solutions and services at [experiencecloud.adobe.com](https://experiencecloud.adobe.com). Si los usuarios intentan iniciar sesión con los accesos heredados ([!DNL my.omniture.com] y [!DNL sc.omniture.com]), se los redirigirá a [!DNL experiencecloud.adobe.com].

**Ayuda relacionada**

[Migración de ID de usuario de Analytics](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Target: Perfiles de producto vs. Espacios de trabajo {#section_3860AF177C9E4C7E9C390D36A414F353}

En Target, un espacio de trabajo es un perfil de producto. Permite que una organización asigne un conjunto de usuarios específico a un conjunto de propiedades concretas. En muchos aspectos, un espacio de trabajo es parecido a un grupo de informes en Adobe Analytics.

Consulte:
* [Permisos de usuario de Enterprise](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)
* [Administración de productos y perfiles](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* Vídeo: [Cómo se configuran espacios de trabajo de Target en Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Campaign: Perfiles de producto, inquilinos y grupos de seguridad {#section_09CDF75366444CF5810CF321B7C712F3}

Un *inquilino* en Campaign se muestra como un *producto* en la página Productos de Admin Console.

Un *grupo de seguridad* se muestra como un perfil de producto.

Consulte [Administración de grupos y usuarios](https://helpx.adobe.com/campaign/standard/administration/using/managing-groups-and-users.html) para obtener información sobre los grupos de seguridad y la asignación de usuarios a los grupos de seguridad.

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Launch, se muestra en la página Productos de Admin Console. Puede incluir otras soluciones y servicios en un perfil de producto de Launch.

See [User Management](https://docs.adobelaunch.com/launch-reference/administration/user-permissions) for information about user permissions in the Admin Console and set up Launch-specific options, including assigning rights to profiles.

## Administrador dinámico de etiquetas {#section_3A41CF2BD5994B9891537D063571D4ED}

Invite a usuarios a la Dynamic Tag Management, asigne funciones de usuario y añada usuarios a grupos.

See [Users and Permissions](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) for information about how to invite users to Dynamic Tag Management and assign user roles and add users to groups.

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

Cree usuarios de Audience Manager y asígnelos a grupos. También puede ver los límites (características, segmentos, destinos y AlgoModel).

Consulte [Administración](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) en la ayuda de Audience Manager.

## Administración de productos de Experience Cloud {#task_16335111C52D40E9BAC73D0699584DBF}

Cree un perfil de producto y asígnelo a un grupo de permisos.

Al invitar a un usuario a una organización, puede darle acceso a productos y perfiles de producto. También puede delegar en un usuario permisos administrativos limitados. Del mismo modo, puede crear grupos de usuarios y, después, añadir el grupo a un perfil de producto para habilitar el acceso.

1. En [Admin Console](https://adminconsole.adobe.com/enterprise/), haga clic en **[!UICONTROL Productos]**.
1. Haga clic en **[!UICONTROL Nuevo perfil]**.
1. Configure los detalles del perfil y, después, haga clic en **[!UICONTROL Siguiente]**.
1. Haga clic en **[!UICONTROL Finalizado]**.

Dispone de más ayuda aquí:

* [Administración de productos y perfiles](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* [Permisos de usuarios Enterprise](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html), en la ayuda de Target, para obtener más información.
* Vídeo: [Cómo se configuran espacios de trabajo de Target en Adobe Admin Console](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Asignación de permisos de acceso de Analytics a un perfil de producto {#task_040673FE3E3E429B9531FBCB8B6A4391}

Asigne permisos de acceso a informes de Analytics (grupos de informes, métricas, dimensiones, etc.) a un perfil de producto.

Por ejemplo, puede crear un perfil de producto que contenga varias herramientas de Analytics ([!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics] y [!UICONTROL Report Builder]), con permiso para métricas y dimensiones concretas (incluidas eVars) y funciones como la creación de segmentos o métricas calculadas.

1. Inicie sesión en [Admin Console](https://adminconsole.adobe.com/enterprise) y, a continuación, haga clic en **[!UICONTROL Productos]** (o haga clic en el nombre de su producto).
1. En el perfil de producto, haga clic en **[!UICONTROL Permisos]** (disponible solo para administradores).
1. Configure los permisos del perfil:

| Elemento | Descripción |
|--- |--- |
| Grupos de informes | Habilite permisos para grupos de informes específicos. |
| Métricas | Habilite permisos para tráfico, conversiones, eventos personalizados, eventos de soluciones, reconocimiento de contenido, etc. |
| Dimensiones | Personalice el acceso de usuarios a nivel granular con eVars, informes de tráfico, informes de soluciones e informes de rutas. |
| Herramientas de grupos de informes | Habilite permisos de usuario para servicios web, administración de grupos de informes, herramientas e informes, y elementos de tablero. |
| Herramientas de Analytics | Habilite permisos de usuario para elementos generales (facturación, registros, etc.), administración de la empresa, herramientas, acceso a servicios web, Report Builder e integración de Data Connectors. Las configuraciones de empresa de la categoría Personalizar Admin Console se han trasladado a las herramientas de Analytics. |

## Delegación de funciones administrativas en usuarios {#task_3A072C4AA9734BC59FFA7E015271BC7E}

Admin Console le permite delegar derechos administrativos limitados en otros miembros de su organización. Las funciones delegadas permiten a los usuarios administrar el acceso al software de los usuarios finales, proporcionar capacidades de implementación de acceso y funcionar como delegados de soporte.

Por ejemplo, puede:

* Permitir al director creativo otorgar acceso a Creative Cloud.
* Permitir al director de marketing otorgar acceso a Experience Cloud.
* Mantener separadas estas dos funciones para que no puedan solaparse las funciones de ambos.

Al utilizar estas funciones, puede delegar la administración de forma simultánea en otras personas sin tener que proporcionar más capacidades de las necesarias.

1. En Admin Console, haga clic en **[!UICONTROL Usuarios]** y, a continuación, haga clic en el nombre del usuario.
1. Haga clic en **[!UICONTROL Editar derechos de administrador]**.
1. Configure los derechos de administración del usuario.
1. Haga clic en **[!UICONTROL Siguiente]** para revisar la configuración y, a continuación, haga clic en **[!UICONTROL Guardar]**.

## Navegadores compatibles y requisitos del sistema {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Navegadores compatibles con Experience Cloud.

Los exploradores admitidos por Experience Cloud incluyen:

* [!DNL Microsoft Edge] (Microsoft [ha dejado de ofrecer soporte](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) para Internet Explorer 8, 9 y 10. Por este motivo, Adobe no corregirá los problemas notificados en relación con estas versiones específicas de Internet Explorer).
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**Nota:** Aunque la interfaz de Experience Cloud admite estos exploradores, es posible que las soluciones individuales no los admitan a todos. (Por ejemplo, [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html) no es compatible con [!DNL Opera] y [Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html) no es compatible con [!DNL Safari]).

**Soluciones y requisitos del producto**

* [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html)
* [Report Builder ](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html)
