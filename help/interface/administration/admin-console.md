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
source-git-commit: 9932f21e4aa4d4a5bf08d7f1617b4c25d4fb14bb
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 3%

---

# Administración de usuarios y licencias de productos

Esta página proporciona información específica para administradores de Experience Cloud, con vínculos a documentación común de administración de usuarios y productos.

Para obtener ayuda general sobre la administración de identidades aplicable a todas las aplicaciones de Adobe, consulte la [Guía de administración de empresas y equipos](https://helpx.adobe.com/es/enterprise/admin-guide.html).

Las secciones siguientes proporcionan vínculos a recursos de la ayuda de Admin Console.

## Funciones administrativas en Admin Console

Admin Console proporciona tres funciones administrativas principales, cada una con niveles específicos de acceso y responsabilidad:

**Administrador del sistema:** Acceso completo: administra todos los aspectos de la consola.

Responsabilidades clave:

* Agregar, quitar y administrar usuarios.
* Asignar y revocar licencias de productos.
* Configure las opciones de identidad y autenticación.
* Ver y administrar la información de facturación.
* Configure administradores y funciones delegadas adicionales.

  **Ideal para:** administradores de TI o jefes de equipo que supervisan el entorno de Adobe de toda la organización.

**Administrador de productos:** Administración específica de productos: controla el acceso y los permisos para productos específicos de Adobe.

Responsabilidades clave:

* Asigne y administre licencias para un producto específico.
* Crear y administrar perfiles de producto.
* Agregar o quitar usuarios de los productos asignados.

  **Ideal para:** equipos o usuarios que administran software específico como Marketo Engage o Adobe Creative Cloud.

**Administrador de perfil de producto:** Administración de funciones granular: se centra en administrar grupos de usuarios y permisos dentro de un producto.

* Responsabilidades clave:
* Crear y administrar perfiles de producto.
* Asigne permisos y acceso a funciones dentro de los perfiles.
* Agregar o quitar usuarios dentro de perfiles.

  **Ideal para:** Directores de departamento o gerentes de equipo que supervisan grupos más pequeños con necesidades especializadas

  Los administradores pueden combinar funciones para obtener una mayor flexibilidad, según los requisitos de la organización.

## Configuración de Admin Console

Para administrar licencias de identidad y productos para aplicaciones de Experience Cloud, ve a [Admin Console](https://adminconsole.adobe.com/enterprise/).

* [Configurar la identidad y el inicio de sesión único](https://helpx.adobe.com/es/enterprise/using/set-up-identity.html) - Aprenda a configurar las cuentas de los usuarios con diferentes tipos de ID con o sin el inicio de sesión único (SSO). Configure SSO para el software de Adobe, la configuración de SAML y revise las preguntas y los errores más comunes.

* [Configurar la organización mediante confianza de directorio](https://helpx.adobe.com/enterprise/using/directory-trust.html): use la confianza de directorio para autenticar a los usuarios en un dominio que ya reclama otra organización.

  Consulte [Organizaciones en Experience Cloud](organizations.md) para obtener información sobre las organizaciones.

* [Configuración de autenticación (empresarial)](https://helpx.adobe.com/enterprise/using/authentication-settings.html): Admin Console admite varios niveles y directivas de protección con contraseña para garantizar la seguridad. Puede especificar el uso de un nivel de protección de contraseña para aplicarlo a todos los usuarios de su organización. El Servicio de atención al cliente de Adobe ofrece tres niveles de seguridad.

* [Contactos de privacidad y seguridad](https://helpx.adobe.com/enterprise/using/security-contacts.html): Adobe hace hincapié en la protección de los datos de su organización y de los usuarios. En caso de que se produzca un incidente de seguridad relacionado con nuestras soluciones de software, las notificaciones se envían a los responsables de cumplimiento correspondientes.

  Las empresas tienen su propio personal cuya función es específica para la protección de datos, la integridad y otras cuestiones de cumplimiento. Por lo tanto, la información de contacto de dicho personal es fundamental para garantizar una notificación rápida en caso de un incidente de seguridad.

## Administración de usuarios

* [Administrar varios usuarios](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) Carga masiva de CSV: aprenda a administrar varios usuarios mediante la carga masiva de CSV en Adobe Admin Console.

* [Tipos de identidad](https://helpx.adobe.com/es/enterprise/using/identity.html): los tipos de identidad permiten a la organización diferentes niveles de control sobre las cuentas y los datos de los usuarios. La elección del modelo de identidad afecta a la forma en que su organización almacena y comparte recursos. Aunque la organización crea y administra los modelos de Federated ID y Enterprise ID, el individuo crea y administra los Adobe ID.

* [Herramienta de sincronización de usuarios](https://helpx.adobe.com/enterprise/using/user-sync.html) (UST): La herramienta de sincronización de usuarios de Adobe es una aplicación de escritorio que se utiliza para automatizar el proceso de sincronización de datos de usuario entre el sistema de administración de identidades de una organización (como Active Directory) y Adobe Admin Console de Adobe. La herramienta permite a los administradores optimizar el aprovisionamiento de usuarios, las actualizaciones y la desactivación en todos los productos de Adobe.

  La herramienta de sincronización de usuarios permite a las organizaciones simplificar la administración de cuentas de usuario y licencias mediante la sincronización automática de los datos de usuario (como roles, grupos y permisos de acceso) entre su servicio de directorio y los sistemas de Adobe. Esta herramienta es especialmente útil para las empresas con equipos grandes. Ayuda a mantener la coherencia y la seguridad, al tiempo que garantiza que los usuarios solo tengan acceso a los productos y servicios a los que tienen derecho.

* [Ver detalles del usuario (Herramienta de administración)](admin-tool-experience-cloud.md): Los administradores pueden ver una lista ordenable y filtrable de todos los usuarios y directivas de Experience Cloud con detalles en [!UICONTROL Herramienta de administración].

## Informes y registros

* [Registro de auditoría](https://helpx.adobe.com/enterprise/using/audit-logs.html) Para realizar un seguimiento de todos los cambios realizados en Admin Console.

Para obtener ayuda no descrita en las ubicaciones anteriores, consulte [Guía de administración de empresas y equipos](https://helpx.adobe.com/es/enterprise/admin-guide.html).

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