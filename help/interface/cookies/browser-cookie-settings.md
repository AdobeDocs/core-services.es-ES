---
description: Aprenda a habilitar la configuración de la privacidad para las cookies del explorador. Puede eliminar los usuarios que bloquearon todas las cookies en el escritorio y en los navegadores móviles.
keywords: cookies,privacidad
solution: Experience Cloud, Analytics, Target, Social
title: 'Configuración de la privacidad para las cookies de explorador '
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
feature: Cookies
topic: Administración
role: Administrator
level: Experienced
exl-id: 5d852e0e-4004-4f94-a6f7-3a14a96cd42f
translation-type: ht
source-git-commit: f4add6d5e64678c6b578237c18ceda9ee2245033
workflow-type: ht
source-wordcount: '302'
ht-degree: 100%

---

# Habilitación de la configuración de privacidad para las cookies de navegador {#enable-privacy-settings-for-browser-cookies}

Puede eliminar los usuarios que bloquearon todas las cookies en el escritorio y en los navegadores móviles. Esta funcionalidad es una configuración de privacidad que excluye a los usuarios que exclusión de la recopilación de datos, lo que le permite respetar la intención del usuario de detener el procesamiento de Analytics.

**Para habilitar la configuración de privacidad para las cookies de navegador**

1. Vaya a **[!UICONTROL Herramientas de administración]** > **[!UICONTROL Grupos de informes]**.
1. Haga clic en **[!UICONTROL Editar configuración]** > **[!UICONTROL General]** > **[!UICONTROL Configuración de privacidad]**.
1. Habilite **[!UICONTROL Configuración de privacidad]** (para escritorio o móvil).

>[!IMPORTANT]
>
>Tenga en cuenta que varias aplicaciones móviles (como en el caso del navegador de la aplicación para Facebook o Twitter) pueden aparecer como un navegador móvil convencional, pero no permiten todas las cookies. Si se habilita esta función, se podría excluir una gran proporción del tráfico móvil de los informes de Analytics.

**Acerca de la configuración de privacidad del explorador**

En las leyes y regulaciones se estipula que la acción de un usuario de bloquear las cookies equivale a excluirse de la creación de perfiles. Al habilitar esta función, se excluirán de los informes de Analytics los datos recopilados en los navegadores de escritorio que el usuario haya configurado para que bloqueen todas las cookies. Si Adobe no puede reconocer el explorador web, los datos se incluirán en los informes de Analytics.

Legisladores de todo el mundo han declarado (tanto en forma de orientación como de acuerdo) que la configuración de las cookies en un navegador indica la preferencia del usuario de excluirse de la creación de perfiles. Específicamente, estos legisladores han declarado que la configuración del explorador para bloquear cookies de terceros es una solicitud de exclusión del seguimiento de terceros (entre sitios). Bloquear todas las cookies es una solicitud de exclusión para todo el seguimiento. Aunque los identificadores del lado del servidor (como la dirección IP o el agente de usuario) pueden ser una opción deseable que evita la configuración del navegador de cookies, algunos legisladores los ven como una elusión de la elección del usuario.
