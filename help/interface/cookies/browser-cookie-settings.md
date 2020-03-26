---
description: Elimine los usuarios que bloquearon todas las cookies en el escritorio y en los navegadores móviles. Esta configuración de privacidad excluye a los usuarios que exclusión la recopilación de datos de Analytics.
keywords: cookies;privacy
seo-description: Elimine los usuarios que bloquearon todas las cookies en el escritorio y en los navegadores móviles. Esta configuración de privacidad excluye a los usuarios que exclusión la recopilación de datos de Analytics.
seo-title: Habilitación de la configuración de privacidad para las cookies de navegador
solution: Marketing Cloud,Adobe Analytics,Adobe Target,Adobe Social
title: Habilitación de la configuración de privacidad para las cookies de navegador
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Habilitación de la configuración de privacidad para las cookies de navegador{#enable-privacy-settings-for-browser-cookies}

Puede eliminar usuarios que hayan bloqueado todas las cookies en los exploradores de escritorio y móviles. Esta función es una configuración de privacidad que excluye a los usuarios que exclusión de la recopilación de datos, lo que le permite respetar la intención del usuario de detener el procesamiento de Analytics.

**Para habilitar la configuración de privacidad para las cookies del explorador**

1. Navigate to **[!UICONTROL Admin Tools]** > **[!UICONTROL Report Suites]**.
1. Click **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Privacy Settings]**.
1. Habilite **[!UICONTROL Configuración de privacidad]** (para escritorio o móvil).

>[!IMPORTANT]
>
>Tenga en cuenta que muchas aplicaciones móviles (como el navegador integrado para Facebook o Twitter) pueden aparecer como un navegador móvil estándar pero no permiten todas las cookies. Si se habilita esta función, se podría excluir una gran proporción del tráfico móvil de los informes de Analytics.

**Acerca de la configuración de privacidad del explorador**

Las leyes y las directrices reglamentarias han indicado que la acción del usuario para bloquear las cookies es la misma que la del usuario para exclusión la creación de perfiles. Al habilitar esta función, los datos recopilados de los exploradores de escritorio, donde el usuario ha configurado el explorador para bloquear todas las cookies, se excluirán de los informes de Analytics. Si Adobe no puede reconocer el explorador web, los datos se incluirán en los informes de Analytics.

Los legisladores de todo el mundo han afirmado (tanto en la guía como en los acuerdos) que la configuración de los navegadores de cookies es una indicación de la preferencia del usuario por exclusión la elaboración de perfiles. Específicamente, estos legisladores han declarado que la configuración del explorador para bloquear cookies de terceros es una solicitud de exclusión del seguimiento de terceros (entre sitios). Bloquear todas las cookies es una solicitud de exclusión para todo el seguimiento. Aunque los identificadores de servidor (como la dirección IP o el agente de usuario) pueden ser una opción deseable que evita la configuración del navegador de cookies, algunos legisladores los vistas como una elusión de la elección del usuario.