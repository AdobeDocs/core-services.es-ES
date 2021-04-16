---
description: Obtenga información sobre cómo Adobe Target usa cookies para ofrecer a los administradores del sitio web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.
keywords: cookies,privacidad
solution: Experience Cloud,Analytics,Target,Social
title: 'Cookies de Adobe Target  '
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administración
role: Administrator
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
translation-type: tm+mt
source-git-commit: dcb6fa5d8458995cba66bc2f89c954aa6bcd5923
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 55%

---

# Cookies de Adobe Target {#target-cookies}

Adobe Target usa cookies para ofrecer a los administradores de sitios Web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.

Puede cambiar esta configuración si es necesario, excepto por la duración de la cookie. Póngase en contacto con el representante de la cuenta cuando cambie la configuración de la cookie.

>[!NOTE]
>
>Los usuarios de Adobe Target también pueden crear cookies de terceros personalizadas.

| Configuración | Información |
| --- | --- |
| Nombre de la cookie | mbox. |
| Dominio de la cookie | Niveles segundo y superior de los dominios desde los que se proporciona el mbox. Dado que se proporciona desde el dominio de la compañía, se trata de una cookie de origen. Ejemplo: `mycompany.com`. |
| Dominio del servidor | `clientcode.tt.omtrdc.net`[!DNL Adobe Target], usando el código de cliente de su cuenta. |
| Duración de la cookie | La cookie permanece en el explorador del visitante dos años después de su último inicio de sesión. No puede cambiar la duración de la cookie. |



>[!NOTE]
>
>Si alguno de los nombres de dominio incorpora un código de país (como `mycompany.co.uk`), colabore con los servicios de cliente para configurar [!DNL at.js] de forma que lo admita.

La cookie conserva una serie de valores para administrar la forma en que los visitantes viven las campañas de Adobe Target:

| Valor | Definición |
| --- | --- |
| session ID | Identificador único de una sesión de usuario determinada. De forma predeterminada, la sesión caduca tras 30 minutos de inactividad. Si está generando sessionId (por ejemplo, para implementaciones del lado del servidor), asegúrese de lo siguiente:<ul><li>El ID de sesión puede ser cualquier cadena imprimible excepto un espacio, un signo de interrogación ( ? ) o una barra diagonal ( / ).</li><li>* El ID de sesión debe tener entre 1 y 128 caracteres de longitud.</li><li>Para una sesión en particular, su valor debe ser el mismo en varias solicitudes</li><li>Nunca debe tener sesiones paralelas (sessionIds distintos) para un visitante determinado en ningún momento.</li></ul>El enrutamiento a un nodo en particular del clúster perimetral se realiza mediante el ID de sesión.<ul><li>La sesión está activa durante 30 minutos en el servidor. Por lo tanto, no debe utilizar un identificador de sesión diferente para un `tntId/thirdPartyId` en particular en los 30 minutos posteriores a la última solicitud realizada con el `tntId/thirdPartyId`. De lo contrario, los cambios en el perfil podrían ser incoherentes e impredecibles.</li><li>El uso del mismo ID de sesión con varios `tntIds/thirdPartyIds` puede provocar cambios impredecibles en los perfiles identificados por el `tntId/thirdPartyIDs`.</li></ul> |
| pc ID | Un ID semipermanente para el explorador de un visitante. Dura hasta que las cookies se eliminan manualmente. |
| check | Un valor de prueba simple utilizado para determinar si un visitante admite cookies. Se establece cada vez que un visitante solicita una página. |
| disable | Se establece si el tiempo de carga de un visitante supera el tiempo de espera fijado en el archivo at.js . De manera predeterminada, tiene una duración de 1 hora. |

