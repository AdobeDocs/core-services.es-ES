---
description: Obtenga información sobre cómo Adobe Target usa cookies para ofrecer a los operadores del sitio web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.
solution: Target
title: 'Cookies de Adobe Target '
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: 2fbf283e5ef06314a679b364fd3f0dfc262a884d
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 16%

---

# Cookies de Adobe Target

Adobe Target usa cookies para ofrecer a los operadores de sitios Web la capacidad de probar cuáles son las ofertas y el contenido en línea más relevantes para los visitantes.

>[!NOTE]
>
>La información de este artículo solo se aplica a la [biblioteca JavaScript de Adobe Target](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} (`at.js`). Consulte [Cookies de Adobe Experience Platform Web SDK](web-sdk.md) para obtener información sobre las implementaciones de Target que utilizan Web SDK.
>
>Puede cambiar la configuración que se describe en este artículo si es necesario, excepto durante la duración de la cookie. [Consulte a su representante de cuentas](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank} al cambiar la configuración de las cookies.

## Cookies de origen

Las siguientes cookies de origen se almacenan en el dominio del cliente:

| Cookie | Detalles |
| --- | --- |
| `mbox` | Almacena identificadores anónimos sobre el visitante.<P>**Dominio de cookie**: Dominio desde el cual se proporciona el mbox. Dado que esta cookie se proporciona desde el dominio de la empresa, se trata de una cookie de origen. Si alguno de los nombres de dominio incluye un código de país, como `example.co.uk`, trabaje con Servicios de cliente para configurar `at.js` de modo que admita este código. Para obtener información sobre cómo personalizar el dominio de la cookie, si es necesario, consulte `cookieDomain` en [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} en la guía para desarrolladores de Adobe Target.<P>**Dominio del servidor**: `clientcode.tt.omtrdc.net`, que usa el código de cliente para su cuenta de Adobe Target.<P>**Duración de la cookie**: la cookie permanece en el explorador del visitante dos años después del último inicio de sesión. No puede cambiar la duración de la cookie.<P>La cookie conserva algunos valores para administrar la forma en que los visitantes viven las actividades de [!DNL Target]:<P>**ID de sesión**: Un identificador único para una sesión de usuario determinada. De forma predeterminada, la sesión caduca tras 30 minutos de inactividad. Si está generando `sessionId` usted mismo (por ejemplo, para [implementaciones del lado del servidor](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}), asegúrese de lo siguiente:<ul><li>El identificador de sesión puede ser cualquier cadena imprimible, excepto un espacio, un signo de interrogación ( ? ), llaves ( { } ) o una barra diagonal ( / ).</li><li>El ID de sesión debe tener entre 1 y 128 caracteres de longitud.</li><li>Para una sesión en particular, el valor de la cookie debe ser el mismo en varias solicitudes.</li><li>Nunca debe tener sesiones paralelas (distintas de `sessionIds`) para un visitante determinado en ningún momento.</li></ul>El enrutamiento a un nodo en particular del clúster perimetral se realiza mediante el ID de sesión.<ul><li>La sesión está activa durante 30 minutos en el servidor. Por lo tanto, no debe usar un identificador de sesión diferente para un(a) `tntId/thirdPartyId` en particular en los 30 minutos posteriores a la última solicitud realizada con el(la) `tntId/thirdPartyId`. De lo contrario, los cambios en el perfil podrían ser incoherentes e impredecibles.</li><li>Se debe usar un nuevo ID de sesión tras treinta minutos de inactividad de un visitante.</li><li>El uso del mismo id. de sesión con varios `tntIds/thirdPartyIds` puede provocar cambios impredecibles en los perfiles identificados por `tntId/thirdPartyIDs`.</li></ul>NOTA: Vea [límite en el número de solicitudes simultáneas](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html#content-delivery){target=_blank} para un ID de sesión determinado.<P>**pc ID**: Un identificador semipermanente para el explorador de un visitante. Dura hasta que las cookies se eliminan manualmente.<P>**check**: Valor de prueba simple utilizado para determinar si un visitante admite cookies. Se establece cada vez que un visitante solicita una página.<P>**disable**: se establece si el tiempo de carga de un visitante supera el tiempo de espera fijado en el archivo at.js. De forma predeterminada, este tiempo de espera dura una hora. |
| `at_check` | Cookie temporal para comprobar si la capacidad de lectura y escritura de cookies está habilitada en el explorador. |
| `mboxEdgeCluster` | Esta cookie solo está presente cuando/si [overrideMboxEdgeServer](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} está establecido en `true`. |

No es posible usar `HTTPOnly` en estas cookies de origen. La biblioteca JavaScript `at.js` debe leer y escribir en estas cookies. Estas cookies las crea `at.js` y no se establecen desde el servidor.

La configuración `secure` se puede habilitar en todas estas cookies mediante la configuración `secureOnly: true` en `at.js`.

## Cookies de terceros

Los usuarios de Adobe Target pueden crear cookies de terceros personalizadas. Las siguientes cookies de terceros se almacenan en `tt.omtrdc.net`:

| Cookie | Detalles |
| --- | --- |
| `customerclientcode!mboxPC` | Presente si el dominio cruzado está habilitado. |
| `customerclientcode!mboxSession` | Presente si el dominio cruzado está habilitado. |

Estas cookies de terceros solo están listas para usarse y las configuran los servidores de recopilación de datos de Adobe Target.

La configuración `secure` se puede habilitar en todas las cookies mediante la configuración `secureOnly: true` en `at.js`.
