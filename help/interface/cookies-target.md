---
description: Obtenga información sobre cómo Adobe Target usa cookies para ofrecer a los administradores del sitio web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.
solution: Experience Cloud,Analytics,Target
title: Cookies de Adobe Target
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 15%

---

# Cookies de Adobe Target

[!DNL Adobe Target] utiliza cookies para ofrecer a los administradores del sitio web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.

>[!NOTE]
>
>La información de este artículo se aplica a [[!DNL Target] Biblioteca JavaScript de at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=es){target=_blank} solo.
>
>Para obtener información sobre las cookies utilizadas en un [!DNL Target] implementación con el [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es){target=_blank}, see "Does the [!DNL Adobe Experience Platform Web SDK] use cookies? If so, what cookies does it use?" in [Frequently Asked questions in the DNL Platform Web SDK overview guide](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html){target=_blank}.
>
>Puede cambiar la configuración que se describe en este artículo si es necesario, excepto durante la duración de la cookie. [Consulte a su representante de cuentas](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank} al cambiar la configuración de las cookies.
>
>[!DNL Target] los usuarios también pueden crear cookies de terceros personalizadas.

## Cookies de origen

Las siguientes cookies de origen se almacenan en el dominio del cliente:

| Cookie | Detalles |
| --- | --- |
| mbox | Almacena identificadores anónimos sobre el visitante.<P>**Dominio de cookie**: Dominio desde el cual se proporciona el mbox. Dado que esta cookie se proporciona desde el dominio de la empresa, se trata de una cookie de origen. Ejemplo: `mycompany.com`. Si alguno de los nombres de dominio incluye un código de país, como `mycompany.co.uk`, colabore con los servicios de cliente para configurar at.js de modo que admita este código. Para obtener información sobre cómo personalizar el dominio de la cookie, si es necesario, consulte &quot;`cookieDomain`&quot; en [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=es){target=_blank} en el *[!DNL Adobe Target]Guía para desarrolladores*.<P>**Dominio del servidor**: `clientcode.tt.omtrdc.net`, usando el código de cliente para su [!DNL Target] cuenta.<P>**Duración de cookie**: La cookie permanece en el explorador del visitante dos años después del último inicio de sesión. No puede cambiar la duración de la cookie.<P>La cookie conserva algunos valores para administrar la experiencia de los visitantes [!DNL Target] actividades:<P>**session ID**: identificador único de una sesión de usuario determinada. De forma predeterminada, la sesión caduca tras 30 minutos de inactividad. Si está generando `sessionId` usted mismo (por ejemplo, para [implementaciones del lado del servidor](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html?lang=es){target=_blank}), asegúrese de lo siguiente:<ul><li>El identificador de sesión puede ser cualquier cadena imprimible, excepto un espacio, un signo de interrogación ( ? ) o una barra diagonal (/).</li><li>El ID de sesión debe tener entre 1 y 128 caracteres de longitud.</li><li>Para una sesión en particular, el valor de la cookie debe ser el mismo en varias solicitudes.</li><li>Nunca debe tener sesiones paralelas (distintas) `sessionIds`) de un visitante determinado en cualquier momento.</li></ul>El enrutamiento a un nodo en particular del clúster perimetral se realiza mediante el ID de sesión.<ul><li>La sesión está activa durante 30 minutos en el servidor. Por lo tanto, no debe utilizar un ID de sesión diferente para un en particular `tntId/thirdPartyId` en un plazo de 30 minutos a partir de la última solicitud realizada con el `tntId/thirdPartyId`. De lo contrario, los cambios en el perfil podrían ser incoherentes e impredecibles.</li><li>Se debe usar un nuevo ID de sesión tras treinta minutos de inactividad de un visitante.</li><li>Uso del mismo ID de sesión con varios `tntIds/thirdPartyIds` puede provocar cambios impredecibles en los perfiles identificados por el `tntId/thirdPartyIDs`.</li></ul>NOTA: Consulte [límite en el número de solicitudes simultáneas](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=es#content-delivery){target=_blank} para un ID de sesión determinado.<P>**pc ID**: Un ID semipermanente para el explorador de un visitante. Dura hasta que las cookies se eliminan manualmente.<P>**check**: un valor de prueba simple utilizado para determinar si un visitante admite cookies. Se establece cada vez que un visitante solicita una página.<P>**disable**: Se establece si el tiempo de carga de un visitante supera el tiempo de espera fijado en el archivo at.js. De forma predeterminada, este tiempo de espera dura una hora. |
| at_check | Cookie temporal para comprobar si la capacidad de lectura y escritura de cookies está habilitada en el explorador. |
| mboxEdgeCluster | Esta cookie solo está presente cuando/si [overrideMboxEdgeServer, configuración](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=es){target=_blank} se establece en `true`. |

No es posible utilizar HTTPOnly en estas cookies de origen. La biblioteca JavaScript de at.js debe leer/escribir en estas cookies. at.js crea estas cookies y no se establecen desde el servidor.

El `secure` La configuración de se puede habilitar en todas estas cookies usando la variable `secureOnly: true` en la implementación de at.js.

## Cookies de terceros

Las siguientes cookies de terceros se almacenan en `tt.omtrdc.net`:

| Cookie | Detalles |
| --- | --- |
| customerclientcode!mboxPC | Esta cookie está presente si el dominio cruzado está habilitado. |
| customerclientcode!mboxSession | Esta cookie está presente si el dominio cruzado está habilitado. |

Estas cookies de terceros solo están listas para usarse y las establece el [!DNL Target] servidores Edge.

El `secure` se puede habilitar en todas las cookies usando la variable `secureOnly: true` en la implementación de at.js.