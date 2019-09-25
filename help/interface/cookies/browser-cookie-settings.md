---
description: Elimine los usuarios que bloquearon todas las cookies en el escritorio y en los navegadores móviles.
keywords: cookies,privacidad
seo-description: Elimine los usuarios que bloquearon todas las cookies en el escritorio y en los navegadores móviles.
seo-title: Habilitación de la configuración de privacidad para las cookies de navegador
solution: Experience Cloud,Analytics,Target,Social
title: Habilitación de la configuración de privacidad para las cookies de navegador
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
index: y
internal: n
snippet: y
translation-type: ht
source-git-commit: 426c1fecf16e1cf83cd28971e4de6fdb66b0e10d

---


# Habilitación de la configuración de privacidad para las cookies de navegador{#enable-privacy-settings-for-browser-cookies}

Elimine los usuarios que bloquearon todas las cookies en el escritorio y en los navegadores móviles.

Esta configuración le permite respetar la intención del usuario de parar el proceso Analytics si este bloquea todas las cookies en su configuración de las cookies de navegador.

1. Vaya a **[!UICONTROL Herramientas administrativas]** &gt; **[!UICONTROL Grupos de informes]**.
1. Haga clic en **[!UICONTROL Editar configuración]** &gt; **[!UICONTROL General]** &gt; **[!UICONTROL Configuración de privacidad**].
1. Habilite **[!UICONTROL Configuración de privacidad]** (para escritorio o móvil).

   Al habilitar esta función, se excluirán de los informes de Analytics los datos recopilados en los navegadores de escritorio que el usuario haya configurado para que bloqueen todas las cookies. Si Adobe no reconoce el navegador, los datos se incluirán en los informes de Analytics.

>[!IMPORTANT]
>
>Tenga en cuenta que varias aplicaciones móviles (como en el caso del navegador de la aplicación para Facebook o Twitter) pueden aparecer como un navegador móvil convencional, pero no permiten todas las cookies. Habilitar está función podría excluir una gran parte del tráfico móvil de los informes de Analytics.

**Acerca de la Configuración de privacidad del navegador**

En las leyes y regulaciones se estipula que la acción de un usuario de bloquear las cookies equivale a excluirse de la creación de perfiles. Al habilitar esta función, se excluirán de los informes de Analytics los datos recopilados en los navegadores de escritorio que el usuario haya configurado para que bloqueen todas las cookies. Si Adobe no reconoce el navegador web, los datos se incluirán en los informes de Analytics.

Legisladores de todo el mundo han declarado (tanto en forma de orientación como de acuerdo) que la configuración de las cookies en un navegador indica la preferencia del usuario de excluirse de la creación de perfiles. Concretamente, estos legisladores han declarado que la configuración del navegador para bloquear cookies de terceros es una solicitud de exclusión del seguimiento de terceros (entre sitios) y que el hecho de bloquear todas las cookies es una solicitud de exclusión de todo el seguimiento. Mientras los identificadores del lado del servidor (tales como una dirección IP o un agente de usuario) pueden ser una opción adecuada para evitar la configuración de cookies del navegador, algunos legisladores lo ven como una elusión de la elección del usuario.