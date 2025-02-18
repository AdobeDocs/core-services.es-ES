---
description: Obtenga información sobre las organizaciones (ID de organización de IMS) y la vinculación de cuentas de soluciones a Experience Cloud.
solution: Experience Cloud
title: Organizaciones y vinculación de cuentas
uuid: ae47ad18-ac33-4efa-8b68-2bfaf77397aa
feature: Organizations
topic: Administration
role: Admin
level: Experienced
exl-id: 6eb58530-2a7a-48c7-9a5b-48a6e980a034
source-git-commit: 1e0206286d4ac0f1987ee053bcbfce8649902ccd
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 55%

---

# Organizaciones en Experience Cloud

Una *organización* (identificador de organización) es la entidad que permite a un administrador configurar grupos y usuarios, así como para controlar el inicio de sesión único en Experience Cloud.

La organización funciona como una empresa de inicio de sesión que abarca todos los productos y aplicaciones de Experience Cloud. Generalmente, la organización es el nombre de la empresa. Sin embargo, una empresa puede tener muchas organizaciones.

![Organizaciones de Experience Cloud](../assets/organizations-menu.png)

Para comprobar que ha iniciado sesión en su organización correcta, haga clic en **[!UICONTROL Perfil]** para ver el nombre de organización predeterminado. Si tiene acceso a más de una organización, también puede ver y cambiar a otra organización en la barra de encabezado.

## Federated ID

Si su organización utiliza Federated ID, Experience Cloud le permite iniciar sesión con el inicio de sesión único de su organización sin necesidad de escribir su dirección de correo electrónico y contraseña. Agregar `#/sso:@domain` a la dirección URL de Experience Cloud (`https://experience.adobe.com`) para realizar esta tarea.

Por ejemplo, para una organización con Federated IDs y el dominio `adobecustomer.com`, establezca el vínculo URL en `https://experience.adobe.com/#/sso:@adobecustomer.com`. También puede ir directamente a una aplicación específica marcando esta URL, anexada con la ruta de la aplicación. (Por ejemplo, para Adobe Analytics, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`).

## Ver su ID de organización {#concept_EA8AEE5B02CF46ACBDAD6A8508646255}

Puede localizar el ID de organización asignado con fines de asistencia. Puede comprobar que se encuentra en la organización correcta o cambiar de una organización a otra mediante el selector **[!UICONTROL Organización]** del encabezado.

El identificador de organización es el ID asociado con la compañía que ha seleccionado en Experience Cloud. Se trata de una cadena alfanumérica de 24 caracteres seguida de `@AdobeOrg` (que debe incluirse).

Puede ver su identificador de organización, junto con otra información de la cuenta, mediante el método abreviado de teclado **Ctrl+i** desde cualquier página de `https://experience.adobe.com`.

**Para ver el identificador de su organización**

1. En [Experience Cloud](https://experience.adobe.com), presione **Ctrl+i** en el teclado.

   ![ID de organización asignado](../assets/assigned-organization.png)

1. En **[!UICONTROL Información de usuario]**, busque **[!UICONTROL Id. de organización actual]** y podrá encontrar el Id. de organización.

   Los administradores también pueden iniciar sesión en Admin Console (vaya a [https://adminconsole.adobe.com](https://adminconsole.adobe.com)) y ver su identificador de organización en la dirección URL.

   Por ejemplo, en la siguiente dirección URL:

   `https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

   El identificador es:

   `C538193582390300A495CC9@AdobeOrg`

## Vinculación de una cuenta de aplicaciones a un Adobe ID {#task_FD389E78640848919E247AC5E95B8369}

Normalmente, los administradores de Experience Cloud otorgan acceso a aplicaciones y servicios. En circunstancias excepcionales, puede vincular las credenciales de la aplicación a una Adobe ID.

1. Siga los pasos de la invitación del correo electrónico a Experience Cloud.

1. Inicie sesión con su Adobe ID o Enterprise ID.

1. Haga clic en **[!UICONTROL Selector de aplicación]**. (![menú](../assets/apps-icon.png)).

   ![Vinculación de una cuenta de aplicaciones a un Adobe ID](../assets/solutions-active.png)

   Las aplicaciones a las que tiene acceso se muestran coloreadas.

1. Haga clic en la aplicación deseada.

   ![Haga clic en su aplicación](../assets/analytics-link-accounts.png)

   Este tipo de mensaje se muestra si es parte del grupo apropiado (y tiene permisos para la aplicación), pero todavía no ha vinculado sus credenciales de cuenta a su Adobe ID.

1. Haga clic en **[!UICONTROL Vincular cuenta]** y, a continuación, proporcione las credenciales.

## Especificar una organización predeterminada {#concept_6A191B42A9874A9780882903BA18F071}

Puede especificar la organización predeterminada que se utilizará al iniciar sesión.

1. En el encabezado, haga clic en **[!UICONTROL Perfil]** y, a continuación, haga clic en Preferencias.

1. En [!UICONTROL General], seleccione una organización predeterminada.


![Editar perfil](../assets/edit-profile.png)

## Solución de problemas de vinculación de cuentas {#concept_DFCB29A3B4834FC59AA29E0BBA301584}

Ayuda relacionada con los problemas que se derivan de la vinculación de cuentas.

Normalmente, la vinculación de cuentas falla porque el Adobe ID está vinculado a un usuario anterior. Cuando falla la vinculación de cuentas, puede:

* [Ponerse en contacto con el Servicio de atención al cliente de Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;lang=es#support).
* Acceder a la aplicación mediante el inicio de sesión estándar mientras el problema se soluciona.
