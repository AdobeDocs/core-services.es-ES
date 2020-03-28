---
description: Información general sobre la administración de Ofertas, cómo acceder a ella y cómo otorgar permisos de usuario.
seo-description: Información general sobre la administración de Ofertas, cómo acceder a ella y cómo otorgar permisos de usuario.
seo-title: Primeros pasos
title: Primeros pasos
uuid: 28d83606-ee36-4bbf-b52d-bbe8b097f6d5
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Administración de Ofertas de Adobe {#section_07CBD4C01F4049A5A19781737D2DCD35}

[!UICONTROL La administración] de Ofertas proporciona la creación, administración y toma de decisiones de ofertas en todos los canales de Experience Cloud. Sirve como catálogo de ofertas central donde puede asociar reglas de elegibilidad y varios fragmentos de contenido con cada _objeto de oferta._ Puede publicar estas ofertas en canales y ubicaciones, y ofrecer la mejor oferta para cada cliente en cada interacción. Estas funciones le permiten ofrecer continuamente la mejor oferta a sus clientes de una manera consistente y coordinada en toda su experiencia.

Los beneficios incluyen:

* Se ha mejorado el rendimiento de la campaña de correo electrónico al ofrecer ofertas más personalizadas en los correos electrónicos.
* Flujo de trabajo mejorado: En lugar de crear varios envíos o campañas, los equipos de marketing pueden mejorar el flujo de trabajo creando un único envío y variar las ofertas en diferentes partes de la plantilla.
* Permite crear, administrar y aprobar ofertas fuera del flujo de trabajo de campaña de correo electrónico de Adobe Campaign Standard.
* Controlar la cantidad de veces que se muestra una oferta entre campañas y clientes de correo electrónico.

## Acceso a Ofertas {#task_DEB6F6A4B6E04E15AD3E1817D700688E}

Obtenga información sobre cómo acceder a Administración de Ofertas.

1. Póngase en contacto con Adobe para realizar el aprovisionamiento.

   Una organización de Experience Cloud debe tener una instancia de Campaign Standard. Adobe también puede activar una función en Campaña que le permite crear actividades de oferta dentro de los correos electrónicos.

1. En el menú de navegación de Experience Cloud, haga clic en el selector de soluciones y, a continuación, haga clic en **[!UICONTROL Ofertas]**.

   ![](assets/access-offers.png)

   Para acceder a Ofertas en Campaign Standard, haga clic en el icono de **[!UICONTROL Ofertas]** de una plantilla de correo electrónico.

   ![](assets/campaign-add-offer.png)

   Una vez que vea ambos elementos en Marketing Cloud y en su cuenta de Adobe Campaign, se le ha configurado la funcionalidad necesaria para comenzar.

## Users and Permissions {#concept_81F0ABB07ACC49E099EDCD87AA0436E1}

Los administradores pueden agregar usuarios a Administración de [!UICONTROL Ofertas] en Admin Console. Se envía una invitación por correo electrónico al nuevo usuario con instrucciones para acceder al producto. Una vez agregado el usuario, puede ajustar sus permisos, dándole acceso a diferentes funcionalidades a través de la Administración de [!UICONTROL Ofertas].

Para obtener más información sobre el uso de la Consola de administración, consulte la documentación [de la Consola de administración de](https://helpx.adobe.com/enterprise/help/aedash.html)HelpX.

En Campaña, los usuarios estándar tienen automáticamente el derecho de incrustar actividades de oferta en una plantilla de correo electrónico.

>[!NOTE]
>
>Para la versión beta, no hay permisos en su lugar. Todos los usuarios que se hayan agregado a Ofertas tendrán acceso completo a todas las funciones dentro de Administración de [!UICONTROL Ofertas].

## Crear un perfil de producto para la administración de Ofertas

Un perfil de producto es un conjunto de permisos que se pueden combinar para crear una función de usuario dentro de un producto. Se deben crear perfiles de producto y luego se les deben asignar usuarios o grupos.

1. Vaya a Adobe [Admin Console](https://adminconsole.adobe.com/).

1. Haga clic en el producto (por ejemplo,**[!UICONTROL Ofertas]**).

1. En la página Perfiles  del producto, haga clic en **[!UICONTROL Nuevo Perfil]**.

1. Escriba un nombre y una descripción para el perfil del producto y, a continuación, haga clic en **[!UICONTROL Finalizado]**.

1. Haga clic en **[!UICONTROL Guardar]**.

### Permisos: definiciones

Descripción de los permisos de Administración [!UICONTROL de] Ofertas disponibles para perfiles de productos en la Consola [!UICONTROL de]administración.

| Elemento | Descripción |
|--- |--- |
| Crear y editar ofertas | Proporciona a los usuarios acceso para crear y editar ofertas en Administración de [!UICONTROL Ofertas]. Si un usuario tiene este permiso pero no el permiso _Aprobar ofertas_ , solo puede crear una oferta y enviarla para su aprobación. No puede utilizarse en una actividad de oferta hasta que se haya aprobado. |
| Eliminar ofertas | Otorga a los usuarios acceso para eliminar ofertas. |
| Aprobar ofertas | Permite a los usuarios aprobar una oferta. Los usuarios con este permiso verán una notificación al iniciar sesión en Administración de Ofertas si alguna oferta necesita aprobación. Si un usuario tiene este permiso y el permiso _crear y editar ofertas_ , puede crear y aprobar ofertas en un único flujo de trabajo. |
| Archivar ofertas | Permite a los usuarios archivar una oferta. |
| Creación de etiquetas | Permite a los usuarios crear etiquetas, tanto en la ficha Etiqueta como en línea en la pantalla de creación de ofertas. Sin este permiso, un usuario solo podrá seleccionar ofertas precreadas al crear una oferta. |
| Editar etiquetas | Permite al usuario editar etiquetas en la ficha Etiquetas. |
| Eliminar etiquetas | Permite al usuario eliminar etiquetas en la ficha Etiquetas. |
| Creación de colocaciones | Permite al usuario crear colocaciones en la ficha Colocaciones. |
| Editar colocaciones | Permite al usuario editar las colocaciones en la ficha Colocaciones. |
| Eliminar colocaciones | Permite al usuario eliminar colocaciones en la ficha Colocaciones. **Nota:** Solo se pueden eliminar las colocaciones que no se utilicen en una actividad de oferta. |