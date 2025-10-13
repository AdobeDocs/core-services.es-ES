---
title: Administración de licencias de usuario y producto
description: Administre licencias de usuario y de producto en Admin Console para aplicaciones de Experience Cloud.
application: Experience Cloud
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: c82821c4-aa5d-48ae-8bef-5937fede8db2
source-git-commit: 6caf1edc5cead3e937f919ac2bb6c829a758d8fd
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 7%

---

# Administración de usuarios y licencias de productos

Puede administrar usuarios y licencias de productos en Adobe [Admin Console](https://adminconsole.adobe.com/enterprise/). Para obtener ayuda general sobre la administración de identidades aplicable a todas las aplicaciones de Adobe, consulte la [Guía de administración de empresas y equipos](https://helpx.adobe.com/es/enterprise/admin-guide.html).

Esta página proporciona información específicamente útil para los administradores de Experience Cloud, define funciones y proporciona vínculos a temas comunes de administración de usuarios y productos en la guía empresarial.

## Funciones administrativas en Admin Console

Admin Console proporciona tres funciones administrativas principales, cada una con niveles específicos de acceso y responsabilidad:

| Función | Descripción |
| ------- | ------- |
| Administrador del sistema | Acceso completo: administra todos los aspectos de la consola. <br>Responsabilidades clave: <br><ul><li>Agregar, quitar y administrar usuarios.</li><li>Asignar y revocar licencias de productos.</li><li>Configuración de la identidad y la autenticación</li><li>Ver y administrar la información de facturación.</li><li>Configure administradores y funciones delegadas adicionales.</li></ul> **Ideal para:** administradores de TI o jefes de equipo que supervisan el entorno de Adobe de toda la organización. |
| Administrador de productos | Administración específica de productos: controla el acceso y los permisos para productos específicos de Adobe.<br>Responsabilidades clave:<ul><li>Asigne y administre licencias para un producto específico.</li><li>Crear y administrar perfiles de producto.</li><li>Agregar o quitar usuarios de los productos asignados.</li></ul>   **Ideal para:** equipos o usuarios que administran software específico como Marketo Engage o Adobe Creative Cloud. |
| Administrador de perfil de producto | Administración granular de funciones: se centra en administrar grupos de usuarios y permisos dentro de un producto.<br>Responsabilidades clave:<ul><li>Crear y administrar perfiles de producto.</li><li>Asigne permisos y acceso a funciones dentro de los perfiles.</li><li>Agregar o quitar usuarios dentro de perfiles.</li></ul> **Ideal para:** Directores de departamento o gerentes de equipo que supervisan grupos más pequeños con necesidades especializadas. Los administradores de <br> pueden combinar funciones para obtener una mayor flexibilidad, según los requisitos de la organización. |

## Admin Console para Experience Cloud

Para administrar licencias de identidad y productos para aplicaciones de Experience Cloud, ve a [Admin Console](https://adminconsole.adobe.com/enterprise/).

Estos son los recursos que puede necesitar al empezar a trabajar como administrador en Admin Console:

### Configuración de recursos

| Vínculo de ayuda | Descripción |
| ------- | ------ |
| [Configurar la identidad y el inicio de sesión único](https://helpx.adobe.com/es/enterprise/using/set-up-identity.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL Configuración]** <br> Aprenda a configurar las cuentas de los usuarios con diferentes tipos de ID con o sin inicio de sesión único (SSO). Configure SSO para el software de Adobe, la configuración de SAML y revise las preguntas y los errores más comunes. |
| [Configurar la organización mediante confianza de directorio](https://helpx.adobe.com/enterprise/using/directory-trust.html) | Autentique a los usuarios con un dominio que ya reclame otra organización. Para obtener información sobre cómo buscar y cambiar de organización, consulte [Organizaciones en Experience Cloud](organizations.md). |
| [Configuración de autenticación (empresarial)](https://helpx.adobe.com/enterprise/using/authentication-settings.html) | Admin Console admite varios niveles y políticas de protección de contraseña para garantizar la seguridad. Puede especificar el uso de un nivel de protección de contraseña para aplicarlo a todos los usuarios de su organización. |
| [Contactos de privacidad y seguridad](https://helpx.adobe.com/enterprise/using/security-contacts.html) | Proteja los datos de su organización y de los usuarios. Si se produce un incidente de seguridad relacionado con nuestras soluciones de software, las notificaciones se envían a los responsables de cumplimiento correspondientes. Las empresas tienen personal cuya función es específica para la protección de datos, la integridad y otras cuestiones de cumplimiento. Por lo tanto, la información de contacto de dicho personal es fundamental para garantizar una notificación rápida en caso de un incidente de seguridad. |

### Administración de usuarios

| Vínculo de ayuda | Descripción |
| ------- | ------- |
| [Restablecer tu Adobe ID](https://helpx.adobe.com/manage-account/kb/account-password-sign-help.html) | Cierre la sesión y haga clic en **[!UICONTROL Obtener ayuda para iniciar sesión]** > **[!UICONTROL Restablecer la contraseña]**. |
| [Administrar varios usuarios](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL Usuarios]** <br>Aprenda a administrar varios usuarios mediante la carga masiva de CSV a Admin Console. |
| [Tipos de identidad](https://helpx.adobe.com/es/enterprise/using/identity.html) | Los tipos de identidad permiten a la organización diferentes niveles de control sobre las cuentas y los datos de los usuarios. La elección del modelo de identidad afecta a la forma en que su organización almacena y comparte recursos. Aunque la organización crea y administra los modelos de Federated ID y Enterprise ID, el individuo crea y administra los Adobe ID. |
| [Herramienta de sincronización de usuarios](https://helpx.adobe.com/enterprise/using/user-sync.html) (UST) | La herramienta de sincronización de usuarios de Adobe es una aplicación de escritorio que se utiliza para automatizar la sincronización de datos de usuario entre el sistema de administración de identidades de una organización (como Active Directory) y Adobe Admin Console. La herramienta permite a los administradores optimizar el aprovisionamiento de usuarios, las actualizaciones y la desactivación en todos los productos de Adobe. |
| [Ver detalles del usuario (Herramienta de administración)](admin-tool-experience-cloud.md) | Vea una lista ordenable y filtrable de todos los usuarios y las directivas de Experience Cloud con detalles en [!UICONTROL Herramienta de administración]. |

### Informes y registros

| Vínculo de ayuda | Descripción |
| ------- |------- |
| [Registro de auditoría](https://helpx.adobe.com/enterprise/using/audit-logs.html) | **[!UICONTROL Información]** > **[!UICONTROL Registros]** > **[!UICONTROL Registro de auditoría]** <br> Rastrea todos los cambios realizados en Admin Console. |


## Recursos específicos de la aplicación

Estos vínculos le ayudan a encontrar información de administración para aplicaciones de Experience Cloud específicas.

<!-- | Application | Link to resource|
| ------- | ------- |
|  [!DNL Analytics] <p>Customer Journey Analytics| [Analytics in the Adobe Admin Console overview](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home) <p>[Administration requirements](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace) |
| [!DNL Audience Manager] | [Audience Manager user migration to Admin Console](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration) |
| [!DNL Campaign] v8 |  [Get started with permissions](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/admin/permissions/gs-permissions) |
| [!DNL Campaign Standard] to [!DNL Campaign v8] | [User access management from Campaign Standard to Campaign V8](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs) |
| [!DNL Commerce] | [Configure the Commerce Admin Integration with Adobe ID](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config) |
| [!DNL Dynamic Media Classic] | [Administration setup](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration) |
| [!DNL Experience Manager as a Cloud Service] |  [Accessing the Admin Console](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console) |
| [!DNL Experience Platform] <p>[!DNL Data Collection] | [Access control UI overview](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview) <p>[Permission management for data collection in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)|
| [!DNL GenStudio for Performance Marketing] | [Provision Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning) |
| [!DNL Journey Optimizer] | [Manage users and roles](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions) |
| [!DNL Journey Optimizer B2B Edition] | [User management](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management) |
|[!DNL  Journey Orchestration] | [Access management](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management) |
| [!DNL Marketo Engage] | [Understanding Marketo Subscription and User Migration to the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console) |
| [!DNL Marketo Measure] | [Adobe Admin Console Setup](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup) |
| [!DNL Mix Modeler] | [Access controls](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls) |
| [!DNL Pass] | [Get started with Account IQ](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started) |
| [!DNL Target] | [Administrator first steps](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target) <p> [User management](https://experienceleague.adobe.com/en/docs/target/using/administer/manage-users/user-management) |
| [!DNL Workfront] | [Manage users in the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console) |

 -->

* [Advertising Search, Social y Commerce](https://experienceleague.adobe.com/en/docs/advertising/search-social-commerce/new-ui/user-administration)
* [Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home)
* [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace)
* [Audience Manager](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration)
* [Campaign v8](https://experienceleague.adobe.com/es/docs/campaign/campaign-v8/admin/permissions/gs-permissions)
* [Campaign Standard](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs)
* [Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config)
* [Dynamic Media Classic](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration)
* [Experience Manager as a Cloud Service](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console)
* [Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview) y [recopilación de datos](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)
* [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning)
* [Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions)
* [Journey Optimizer B2B edition](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management)
* [Journey Orchestration](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management)
* [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console)
* [Marketo Measure](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup)
* [Mix Modeler](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls)
* [Adobe Pass](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started)
* [Target](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target)
* [Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console)

La mayor parte de la ayuda de Admin Console para todas las aplicaciones de Adobe está documentada en [Guía de administración de empresas y equipos](https://helpx.adobe.com/es/enterprise/admin-guide.html).
