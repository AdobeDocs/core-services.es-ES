---
description: Elimine los usuarios que bloquearon todas las cookies en el escritorio y en los navegadores móviles. Esta configuración de privacidad excluye a los usuarios que desactivan la recopilación de datos de Analytics.
keywords: cookies;privacy
seo-description: Elimine los usuarios que bloquearon todas las cookies en el escritorio y en los navegadores móviles. Esta configuración de privacidad excluye a los usuarios que desactivan la recopilación de datos de Analytics.
seo-title: Habilitación de la configuración de privacidad para las cookies de navegador
solution: Marketing Cloud,Analytics,Target,Social
title: Habilitación de la configuración de privacidad para las cookies de navegador
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
translation-type: tm+mt
source-git-commit: 688272e19e9d1828d070889bf8689cab7ed2c9c1

---


# Habilitación de la configuración de privacidad para las cookies de navegador{#enable-privacy-settings-for-browser-cookies}

Puede eliminar usuarios que hayan bloqueado todas las cookies en los exploradores de escritorio y móviles. Esta función es una configuración de privacidad que excluye a los usuarios que desactivan la recopilación de datos, lo que le permite respetar la intención del usuario de detener el procesamiento de Analytics.

**Para habilitar la configuración de privacidad para las cookies del explorador**

1. Vaya a **[!UICONTROL Herramientas administrativas]** &gt; **[!UICONTROL Grupos de informes]**.
1. Haga clic en **[!UICONTROL Editar configuración]** &gt; **[!UICONTROL General]** &gt; **[!UICONTROL Configuración de privacidad**].
1. Habilite **[!UICONTROL Configuración de privacidad]** (para escritorio o móvil).

>[!IMPORTANT]
>
>Tenga en cuenta que muchas aplicaciones móviles (como el navegador integrado para Facebook o Twitter) pueden aparecer como un navegador móvil estándar pero no permiten todas las cookies. Habilitar está función podría excluir una gran parte del tráfico móvil de los informes de Analytics.

**Acerca de la Configuración de privacidad del navegador**

Las leyes y las directrices reglamentarias han expresado que la acción de un usuario para bloquear cookies es la misma que la acción de un usuario para excluir la creación de perfiles. Al habilitar esta función, los datos recopilados de los exploradores de escritorio, donde el usuario ha configurado el explorador para bloquear todas las cookies, se excluirán de los informes de Analytics. Si Adobe no reconoce el navegador web, los datos se incluirán en los informes de Analytics.

Los legisladores de todo el mundo han declarado (tanto en la guía como en los acuerdos) que la configuración de los navegadores de cookies es una indicación de la preferencia del usuario por no participar en la elaboración de perfiles. Específicamente, estos legisladores han declarado que la configuración del explorador para bloquear cookies de terceros es una solicitud de exclusión del seguimiento de terceros (entre sitios). Bloquear todas las cookies es una solicitud de exclusión para todo el seguimiento. Mientras los identificadores del lado del servidor (tales como una dirección IP o un agente de usuario) pueden ser una opción adecuada para evitar la configuración de cookies del navegador, algunos legisladores lo ven como una elusión de la elección del usuario.