---
description: Obtenga información sobre los componentes de la interfaz central en Experience Cloud. La ayuda incluye la administración de usuarios y productos en Admin Console, lo que permite crear aplicaciones para los servicios de Experience Cloud y recibir ayuda en la biblioteca de audiencias, los atributos del cliente, los activos de Experience Cloud, etc.
solution: Experience Cloud
title: Documentación y temas de ayuda sobre la interfaz de Experience Cloud
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 657d7e665ac3d20b80bdb26db0e3e62e421218bf
workflow-type: ht
source-wordcount: '1347'
ht-degree: 100%

---

# Guía de componentes de la interfaz central de Experience Cloud

[Experience Cloud](https://experience.adobe.com) es la familia integrada de aplicaciones, productos y servicios de marketing digital de Adobe. Desde la intuitiva interfaz, puede acceder rápidamente a sus aplicaciones, funciones de productos y servicios en la nube.

![Experience Cloud](assets/landing.png)

En el encabezado de Experience Cloud encuentra las siguientes funciones:

* Acceso a sus aplicaciones y servicios
* En el menú Ayuda, busque documentación del producto, tutoriales y publicaciones de la comunidad. Ver resultados en Experience League.
* Haga una búsqueda general de objetos empresariales mediante una búsqueda global (solo usuarios de Experience Platform) en el campo Búsqueda.
* Administración de las preferencias de la cuenta (alertas, notificaciones y suscripciones)

## Inicie sesión en Experience Cloud {#signin}

Inicie sesión y verifique que se encuentra en la [organización](organizations.md) correcta.

1. Vaya a [Adobe Experience Cloud](https://experience.adobe.com).
1. Escriba su dirección de correo electrónico de Adobe y seleccione **[!UICONTROL Continuar]**.

   Los administradores pueden consultar [Autenticación de usuario de Experience Cloud](admin-getting-started.md#migration) para ver las actualizaciones importantes de los tipos de identidad (ID empresarial).

1. Seleccione una cuenta.
1. Escriba la contraseña.
1. Compruebe que se encuentra en la organización correcta.

   ![Compruebe que se encuentra en la organización correcta](assets/organizations-menu.png)

   **Verifique su organización**

   Para comprobar que ha iniciado sesión en la [organización](organizations.md) correcta, haga clic en el avatar de perfil para ver el nombre de la organización. Si tiene acceso a más de una organización, también puede ver y cambiar a otra organización directamente en la barra de encabezado.

   Si su organización utiliza Federated ID, Experience Cloud le permite iniciar sesión con el inicio de sesión único de su organización sin necesidad de escribir su dirección de correo electrónico y contraseña. Agregar `#/sso:@domain` a la dirección URL de Experience Cloud (`https://experience.adobe.com`) para realizar esta tarea.

   Por ejemplo, para una organización con Federated IDs y el dominio `adobecustomer.com`, establezca el vínculo URL en `https://experience.adobe.com/#/sso:@adobecustomer.com`. También puede ir directamente a una aplicación específica marcando esta URL, anexada con la ruta de la aplicación. (Por ejemplo, para Adobe Analytics, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`).

## Acceso a aplicaciones de Experience Cloud {#navigation}

Después de iniciar sesión en Experience Cloud, puede acceder rápidamente a todas sus aplicaciones, servicios y organizaciones desde el encabezado unificado.

Para acceder a las aplicaciones y servicios de Experience Cloud proporcionados por usted dentro de su organización, vaya al ![menú](assets/menu-icon.png) del selector de aplicaciones.

![Acceso a aplicaciones de Experience Cloud](assets/platform-core-services.png)

## Compatibilidad con exploradores en Experience Cloud {#browser}

Para obtener el mejor rendimiento, Experience Cloud está optimizado para los exploradores más populares, incluida la versión más reciente, además de las dos versiones anteriores.

* Chrome
* Edge
* Firefox
* Opera
* Safari

Si el explorador no aparece en la lista, puede que sea compatible, pero se recomienda que utilice uno de los exploradores enumerados.

>[!NOTE]
>
>No todas las aplicaciones que se ejecutan en el dominio de Experience Cloud admiten todos los exploradores. Si no está seguro, consulte la documentación de la aplicación específica.

## Compatibilidad de idiomas en Experience Cloud {#languages}

Experience Cloud admite los idiomas preferidos para cada usuario, tal como se establecen en las preferencias de cuenta de usuario de Adobe. Actualmente se admiten los siguientes idiomas:

* Chino
* Inglés
* Francés
* Alemán
* Italiano
* Japonés
* Coreano
* Portugués
* Español
* Taiwanés

Aunque todos los equipos de aplicaciones están comprometidos con el soporte de idiomas global, no todas las aplicaciones se ofrecen en todos los idiomas mencionados anteriormente. Si el idioma principal no es compatible con una aplicación de Experience Cloud, también puede establecer un idioma secundario de forma predeterminada cuando corresponda. Esto se puede hacer en [preferencias de usuario de Experience Cloud](https://experience.adobe.com/preferences).

## Obtener ayuda y asistencia {#support}

Acceda a aprendizaje y ayuda mediante el icono de Ayuda (![recurso](assets/help-icon.png)) del encabezado, que incluye contenido de ayuda (documentación, tutoriales y cursos) en [Experience League](https://experienceleague.adobe.com/?lang=es#home), así como recursos adicionales para aplicaciones individuales. También puede enviar comentarios abiertos y crear tickets de asistencia con prioridad.

![Obtener ayuda y asistencia](assets/search-menu.png)

El menú [!UICONTROL Ayuda] también le permite acceder a:

* **[!UICONTROL Asistencia técnica]:** Cree un ticket de asistencia o póngase en contacto con el [!UICONTROL Soporte técnico] mediante Twitter.
* **[!UICONTROL Comentarios]:** Comparta comentarios sobre su experiencia de Experience Cloud. Los comentarios se utilizan para mejorar los productos y servicios de Adobe.
* **[!UICONTROL Estado]:** Vaya a `https://status.adobe.com/experience_cloud` y compruebe el estado operativo del producto y [!UICONTROL Administrar suscripciones].
* **[!UICONTROL Developer Connection]:** Navegación hasta `adobe.io` y búsqueda de documentación para desarrolladores.

## Perfil de usuario y preferencias de cuenta {#preferences}

Las preferencias de Experience Cloud incluyen notificaciones, suscripciones y alertas. En el menú de preferencias de cuenta, puede hacer lo siguiente:

* Especifique un tema oscuro (no todas las aplicaciones admiten este tema)
* Buscar [Organizaciones](organizations.md)
* Cerrar sesión
* Configurar las preferencias, notificaciones y suscripciones de la cuenta

Para administrar las preferencias, seleccione **[!UICONTROL Preferencias]** en el menú ![preferencias](assets/preferences-icon-sm.png) de su cuenta.

![Perfil de usuario y preferencias de cuenta](assets/preferences-page.png)

En [!UICONTROL preferencias de Experience Cloud], puede configurar las siguientes funciones:

| Función | Descripción |
|--- |--- |
| Organización [predeterminada](organizations.md) | Seleccione la organización que desea ver al iniciar Experience Cloud. |
| [!UICONTROL Recopilación de datos del producto] | Seleccione qué tecnologías puede utilizar Adobe para recopilar datos sobre cómo aprovechar sus productos. |
| [!UICONTROL Recomendaciones y promociones de formación personalizadas] | Seleccione dónde desea recibir ayuda personalizada para sus productos de Adobe. Esta ayuda está disponible por correo electrónico, en el producto y en las comunidades de Experience League. [Más información.](personalized-learning-preferences.md) |
| [!UICONTROL Suscripciones] | Seleccione los productos y las categorías a los que desea suscribirse. Notificaciones en la ventana emergente [!UICONTROL Notificaciones] y en el correo electrónico. |
| [!UICONTROL Prioridad] | Seleccione las categorías que desea que se consideren de alta prioridad. Estas categorías están marcadas con la etiqueta High y pueden configurarse para entregarlas como alertas. |
| [!UICONTROL Alertas] | Seleccione las notificaciones de las que desea ver las alertas mostradas en el explorador. Las alertas aparecen en la esquina superior derecha de la ventana durante unos segundos. |
| Correos electrónicos | Especifique la frecuencia con la que desea recibir los correos electrónicos de notificación. (No enviado, instantáneo, diario o semanal). |

{style="table-layout:auto"}

## Notificaciones y anuncios {#notifications}

Seleccione **[!UICONTROL Notificaciones]** para recibir alertas acerca de actualizaciones relevantes y disponibles, incluidas versiones de productos, avisos de mantenimiento, elementos compartidos y solicitudes de aprobación.

![Notificaciones y anuncios](assets/notifications-menu-small.png)

## Dominios de Experience Cloud {#domains}

Experience Cloud utiliza los siguientes hosts para ofrecer la aplicación, mejorar el rendimiento y la experiencia del producto. Adobe recomienda añadir estos dominios a la lista de permitidos del cortafuegos para una experiencia óptima. También pueden estar en uso dominios adicionales para aplicaciones de Experience Cloud específicas, como Adobe Analytics. Consulte la documentación de esas aplicaciones para obtener más información.

| Tecnología | Dominios |
|--- |--- |
| Dominios de Adobe Experience Cloud | `adobe.com`, `adobe.net`, `adobe.io` |
| Servicio Identity Management de Adobe (IMS) | `adobelogin.com` |
| Fuentes de Experience Cloud | `typekit.net` |
| Recopilación de datos de Adobe (para obtener orientación y ayuda sobre el producto) | `adobedtm.com` |
| Gainsight (para obtener ayuda y orientación sobre el producto) | `esp.aptrinsic.com` |

## Obtener ayuda sobre administración y servicios entre aplicaciones

Esta guía proporciona acceso a la ayuda sobre la administración de usuarios y productos de Experience Cloud en Admin Console, lo que permite crear aplicaciones para los servicios de plataforma. También puede acceder a la ayuda de la Biblioteca de audiencias, atributos del cliente, activos de Experience Cloud y mucho más:

* [[!UICONTROL Biblioteca de audiencias]](audience-library.md)
* [[!UICONTROL Atributos del cliente]](attributes.md)
* [[!UICONTROL Triggers]](triggers.md)
* [[!UICONTROL Recursos] de Experience Cloud](experience-cloud-assets.md)
* [Cookies de Experience Cloud](cookies-privacy.md)
* [Administración de usuarios y productos](admin-getting-started.md) (Admin Console)
* [Activación de las aplicaciones para los servicios principales](core-services.md)
* [Preguntas frecuentes](admin-getting-started.md)
* [Organizaciones y vinculación de cuentas](organizations.md)
* [Integraciones](marketing-cloud-integrations.md)
* [Integración de Adobe Target con Experience Cloud](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=es)
* [Información general sobre seguridad y confidencialidad en Experience Cloud](assets/Adobe-Marketing-Cloud-Privacy-and-Security-Overview.pdf)
* [Precarga de DNS](admin-getting-started.md#concept_6BC8C6856E3644F8956D7AD0A96383B7)

## Guías

Las guías de Experience Cloud relacionadas incluyen:

* [Adobe Mobile](https://experienceleague.adobe.com/docs/mobile-services/using/home.html?lang=es)
* [Gráfico de cooperación Experience Platform](https://experienceleague.adobe.com/docs/device-co-op/using/home.html?lang=es)
* [Exchange](https://exchange.adobe.com/experiencecloud)
* [Servicio de Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=es)
* [Recopilación de datos de Experience Platform/Launch](https://experienceleague.adobe.com/docs/launch.html?lang=es)
* [Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=es)
* [[!UICONTROL Dynamic Tag Management]](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=es)

## Tutoriales

Aproveche los tutoriales de autoayuda y los consejos rápidos de Experience League:

* [Todos los tutoriales de Experience League](https://experienceleague.adobe.com/?lang=es#quick-how-tos)
* [Tutoriales de Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/data-collection/overview.html?lang=es)
* [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/application-services/rtcdp/understanding-the-real-time-customer-data-platform.html?lang=es)

## Notas de la versión y ayuda relacionada con Experience Cloud

* [Documentación del producto para todas las aplicaciones de Experience Cloud](https://experienceleague.adobe.com/docs/home.html?lang=es): Busque ayuda en Aprendizaje y asistencia de Experience Cloud
* [Notas de la versión y actualizaciones de productos](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=es): Descubra las novedades de Experience Cloud y suscríbase para obtener actualizaciones
* [Tutoriales para implementar servicios principales](https://experienceleague.adobe.com/docs/platform-learn/data-collection/overview.html?lang=es): Explore vídeos y tutoriales sobre servicios principales
* [Ayuda de expertos en Experience League](https://experienceleague.adobe.com/?lang=es): Descubra todo lo que tiene que saber sobre nuestras soluciones gracias a nuestros expertos y a nuestra comunidad
* [Educación y formación](https://helpx.adobe.com/es/learning.html?promoid=KAUDK): Póngase en contacto con Adobe para asegurarse de sacar el máximo partido de sus productos
* [Blog de la experiencia del cliente](https://blog.adobe.com/es/topics/digital-transformation): Lea el blog de Experience Cloud
* [Servicio de atención al cliente](https://experienceleague.adobe.com/?support-solution=General&amp;lang=es#support): Póngase en contacto con el Servicio de atención al cliente de Adobe
