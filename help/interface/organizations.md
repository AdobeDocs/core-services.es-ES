---
description: Obtenga información acerca de las organizaciones (ID de organización de IMS) y la vinculación de cuentas de solución a Experience Cloud.
keywords: Servicios de Adobe Experience Cloud
solution: Experience Cloud
title: 'Organizaciones y vinculación de cuentas '
uuid: ae47ad18-ac33-4efa-8b68-2bfaf77397aa
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 6eb58530-2a7a-48c7-9a5b-48a6e980a034
source-git-commit: c6884ade4a793f1cedbc5d497cb9c8ea798a7408
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 80%

---

# Organizaciones en Experience Cloud

Obtenga información sobre la administración y el cambio de organizaciones en Experience Cloud.

## Identificación de la organización {#concept_384D169B0B724B799D573B8ECB5C39BF}

Un *organización* (ID de organización) es la entidad que permite a un administrador configurar grupos y usuarios, así como controlar el inicio de sesión único en el Experience Cloud. La organización funciona como una empresa de inicio de sesión que abarca todos los productos y aplicaciones de Experience Cloud. La mayoría de las veces, la organización es el nombre de empresa. Sin embargo, una empresa puede tener muchas organizaciones.

Para comprobar que ha iniciado sesión en su organización correcta, haga clic en el avatar de perfil para ver el nombre de la organización. Si tiene acceso a más de una organización, también puede ver y cambiar a otra organización directamente en la barra de encabezado.

Si su organización utiliza Federated ID, Experience Cloud le permite iniciar sesión con el inicio de sesión único de su organización sin necesidad de escribir su dirección de correo electrónico y contraseña. Para utilizar esta función, añada `#/sso:@domain` a la dirección URL de Experience Cloud (`https://experience.adobe.com`).

Por ejemplo, para una organización con Federated IDs y el dominio `adobecustomer.com`, establezca el vínculo URL en `https://experience.adobe.com/#/sso:@adobecustomer.com`. También puede ir directamente a una aplicación específica marcando esta URL, anexada con la ruta de la aplicación. (Por ejemplo, para Adobe Analytics, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`).

![Resultado de los pasos](assets/organization-switch.png)

## Ver el ID de organización {#concept_EA8AEE5B02CF46ACBDAD6A8508646255}

Es posible que deba localizar el identificador de organización asignado con fines de asistencia. Mediante el menú **[!UICONTROL Organización]** puede verificar que esté en la organización correcta o cambiar de una organización a otra.

El identificador de organización es el ID asociado con la compañía que ha seleccionado en Experience Cloud. Se trata de una cadena alfanumérica de 24 caracteres seguida de `@AdobeOrg` (que debe incluirse).

Puede ver su ID de organización, junto con otra información de la cuenta, mediante el método abreviado de teclado **Ctrl + i** desde cualquier página en `https://experience.adobe.com`.

**Para ver su ID de organización**

1. En [Experience Cloud](https://experience.adobe.com), pulse **Ctrl + i** en el teclado.

   ![ID de organización asignado](assets/assigned-organization.png)

1. En **[!UICONTROL Información del usuario]**, busque **[!UICONTROL ID de organización actual]** y verá el ID de organización.

   Los administradores también pueden iniciar sesión en el Admin Console (Vaya a [https://adminconsole.adobe.com](https://adminconsole.adobe.com)) y ver su ID de organización en la dirección URL.

   Por ejemplo, en la siguiente dirección URL:

   `https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

   El identificador es:

   `C538193582390300A495CC9@AdobeOrg`

## Vinculación de una cuenta de aplicaciones a un Adobe ID {#task_FD389E78640848919E247AC5E95B8369}

Normalmente, los administradores de Experience Cloud otorgan acceso a aplicaciones y servicios. En circunstancias excepcionales, es posible que deba vincular las credenciales de la aplicación a un Adobe ID.

1. Siga los pasos de la invitación del correo electrónico para utilizar Experience Cloud.
1. Inicie sesión con su Adobe ID o Enterprise ID.
1. Seleccione el selector de aplicaciones. (![](assets/menu-icon.png)).

   ![Vinculación de una cuenta de aplicaciones a un Adobe ID](assets/solutions-active.png)

   Las aplicaciones a las que tiene acceso se muestran coloreadas.
1. Seleccione la aplicación que desee:

   ![Seleccione la aplicación que desee](assets/analytics-link-accounts.png)

   Este tipo de mensaje se muestra si es parte del grupo apropiado (y tiene permisos para la aplicación), pero todavía no ha vinculado sus credenciales de cuenta a su Adobe ID.
1. Seleccione **[!UICONTROL Vincular cuenta]**, luego proporcione las credenciales.

## Especificación de una organización y una página de aterrizaje predeterminadas {#concept_6A191B42A9874A9780882903BA18F071}

Puede especificar la organización y la página de aterrizaje predeterminadas que se pueden utilizar cuando inicia sesión.

En su perfil, seleccione **[!UICONTROL Editar perfil]**.

![Editar perfil](assets/edit-profile.png)

En la organización y la página de aterrizaje predeterminadas, puede personalizar la forma de iniciar sesión.

![Organización y página de aterrizaje predeterminadas](assets/default-organization.png)

## Solución de problemas de vinculación de cuentas {#concept_DFCB29A3B4834FC59AA29E0BBA301584}

Ayuda relacionada con los problemas que se derivan de la vinculación de cuentas.

Normalmente, la vinculación de cuentas falla porque el Adobe ID está vinculado a un usuario anterior. Cuando falla la vinculación de cuentas, puede:

* [Ponerse en contacto con el Servicio de atención al cliente de Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;lang=es#support).
* Acceder a la aplicación mediante el inicio de sesión estándar mientras el problema se soluciona.
