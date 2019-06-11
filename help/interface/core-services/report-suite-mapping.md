---
description: Obtenga más información sobre cómo asignar uno o más grupos de informes a una organización.
seo-description: Obtenga más información sobre cómo asignar uno o más grupos de informes a una organización.
seo-title: Asignación de grupos de informes a una organización
title: Asignación de grupos de informes a una organización
uuid: b 983 d 5 a 6-b 3 d 0-4137-ac 53-bc 5681 d 3 e 58 b
translation-type: tm+mt
source-git-commit: d9d6cebc0e9e14eac2471dc79b91276a154e35e0

---


# Asignación de grupos de informes a una organización {#topic_7C4740559EAC4E0FA5F8DEF886B580DA}

Obtenga más información sobre cómo asignar uno o más grupos de informes a una organización.

Los servicios de Experience Cloud (como el servicio Experience Cloud ID y People) están asociados a una organización y no a un grupo de informes individual. Para asegurar el correcto funcionamiento de estos servicios, cada grupo de informes de Analytics debe asignarse a una organización. El proceso de asignación:

* Establece una organización de Experience Cloud como organización principal para el grupo de informes.
* No cambia quién puede acceder a un grupo de informes (el acceso se sigue determinado según la cuenta de inicio de sesión en Adobe Analytics de cada usuario).


**Requisitos**

Debe ser administrador de Analytics en una empresa de inicio de sesión con acceso al grupo de informes que desea asignar. Además, esta cuenta debe estar [vinculada a una organización de Experience Cloud](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1) para asignar grupos de informes a dicha organización.

Las organizaciones aparecen en gris si se carece de permisos de administrador de Analytics para una empresa de inicio de sesión en ellas y con acceso al grupo de informes dado.

## Asignar un grupo de informes a una organización {#task_23993FE78DF6455FA8D7BE60686EA16C}

1. Haga clic **[!UICONTROL en Experience Cloud]** &gt; **[!UICONTROL Administración]** &gt; **[!UICONTROL Asignación de grupos de informes]**

   También puede utilizar una [URL directa](https://audience.marketing.adobe.com/rsmapping/ui.html).

1. Si desea ver las empresas de inicio de sesión que tienen acceso a cada grupo de informes, haga clic en **[!UICONTROL Visible para empresas de inicio de sesión]**.

   Esta vista pretende ayudarlo a tomar una decisión fundamentada acerca de la asignación.

1. Haga clic en el menú desplegable en la columna **[!UICONTROL Organización asignada]junto a un grupo de informes y seleccione la organización a la que desea asignar.**

   Consulte la siguiente sección para obtener sugerencias sobre cómo seleccionar una organización de Experience Cloud.

## Asignar varios grupos de informes a una organización {#task_94955B0D8ABA4CB1A38746ECF8E32711}

1. Haga clic **[!UICONTROL en Experience Cloud]** &gt; **[!UICONTROL Administración]** &gt; **[!UICONTROL Asignación de grupos de informes]**.

   También puede utilizar una [URL directa](https://audience.marketing.adobe.com/rsmapping/ui.html).

1. Seleccione los grupos de informes que desea asignar.

   ![](assets/rs-mapping-multiple.png)

1. Seleccione la organización (Outdoors Inc, en este ejemplo) y, a continuación, haga clic en **[!UICONTROL Seleccionar]**.

   Consulte la siguiente sección para obtener sugerencias sobre cómo seleccionar una organización de Experience Cloud.

1. Haga clic en **[!UICONTROL Guardar asignación]**.

## Sugerencias para seleccionar una organización de Experience Cloud {#mapping-tips}

Esta sección contiene sugerencias para ayudarlo a seleccionar la organización de Experience Cloud a la que debe asignar un grupo de informes.

**¿Qué organización debo elegir?**

Si el servicio Experience Cloud ID está implementado en el grupo de informes, asegúrese de que la organización seleccionada en la herramienta Report Suite Mapping sea la misma especificada en el archivo [!DNL visitorAPI.js] de su sitio web. Puede utilizar las instrucciones de [Comprobación y verificación del servicio Experience Cloud ID](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-test-verify.html) para encontrar el identificador de organización que utiliza el servicio de ID de visitante.

Si el servicio ID de visitante de Experience Cloud no está implementado en los sitios que recopilan datos para el grupo de informes y lo implementa en el futuro, tendrá que asegurarse de que la implementación coincida con la organización elegida en la herramienta Report Suite Mapping.

**¿Por qué algunas organizaciones aparecen en gris?**

Indica que carece de privilegios suficientes para asignar al grupo de informes en gris. Consideremos el siguiente ejemplo:
![](assets/rs-mapping.png) En este diagrama, la llave azul indica privilegios de administrador. Las líneas grises indican visibilidad.

Este usuario tiene acceso a dos organizaciones de Experience Cloud. Ha hecho lo siguiente:

* Ha vinculado su cuenta de administrador en la empresa de inicio de sesión chapek de Analytics a su cuenta de organización de Experience Cloud Chapek Corp.
* Ha vinculado su cuenta de no administrador en la empresa de inicio de sesión doohan de Analytics a su cuenta de organización de Experience Cloud Chapek Corp.
* Ha vinculado su cuenta de no administrador en la empresa de inicio de sesión nigel de Analytics a su cuenta de organización de Experience Cloud Nigel Inc.

Los siguientes puntos indican las acciones de asignación que este usuario puede y no puede realizar respecto a estos grupos de informes:

* El grupo de informes Chapek-prod se puede asignar a la organización Chapek Corp porque este usuario es administrador de una empresa de inicio de sesión vinculada de Analytics (chapek) y su cuenta está vinculada a esta organización.
* Este usuario no puede vincular el grupo de informes Nigel-prod porque no es administrador de ninguna empresa de inicio de sesión para la que este grupo de informes sea visible.
* El grupo de informes Doohan-prod puede asignarse a Chapek Corp porque este usuario es administrador de una empresa de inicio de sesión (chapek) vinculada a la organización de Experience Cloud (nótese que no es administrador de la empresa de inicio de sesión doohan de Analytics). Es importante ser conscientes de que el grupo de informes Doohan-prod también puede asignarse a la organización Nigel Inc de Experience Cloud, aunque este usuario no pueda realizar dicha asignación. En este caso, ambas organizaciones de Experience Cloud se muestran en la lista, aunque Nigel Inc aparece en gris. Antes de la asignación, este usuario debería consultar a un administrador de la empresa de inicio de sesión nigel para determinar qué organización es la mejor candidata para la asignación. La interfaz muestra el aviso “Posible conflicto” si selecciona una organización distinta de aquella bajo la que se creó en un principio el grupo de informes.

## Preguntas frecuentes {#section_099E485805994C929FF9C9F75219BEE1}

**¿Por qué no veo todos mis grupos de informes?**

Algunos de sus grupos de informes podrían ser visibles en una empresa de inicio de sesión distinta. Puede cambiar la empresa de inicio de sesión actual mediante el menú desplegable en la parte superior de la pantalla.

**¿Qué sucede si no reconozco algunas de las organizaciones indicadas en el menú desplegable de uno de mis grupos de informes?**

La lista muestra todas las organizaciones * posibles * a las que podría asignarse su grupo de informes, aunque no tenga permiso para asignar a todos esos grupos de informes. Si no está seguro de si el grupo de informes debe asignarse a uno de los grupos de informes en gris de la lista, consulte a un administrador de Experience Cloud de su organización para determinar la mejor opción.

**¿Qué sucede si no reconozco algunas de las empresas de inicio de sesión indicadas para un grupo de informes en la columna “Visible para empresas de inicio de sesión”?**

En algún punto, este grupo de informes se compartió con otra empresa de inicio de sesión que puede ser parte de una organización de Experience Cloud distinta.

**¿Qué es el error “Posible conflicto” que indica que el grupo de informes lo generó otra organización? ¿Es eso importante?**

Es una notificación que le ayuda a tomar una decisión fundamentada acerca de la asignación de su grupo de informes. Queremos que sea consciente de que el grupo de informes se creó en un primer momento en una organización distinta, ya que dicha organización podría ser más apropiada para el grupo de informes.

**¿Cómo sé si un grupo de informes está asignado?**

Los grupos de informes asignados aparecen en un formato no editable. Si necesita cambiar una asignación, póngase en contacto con el Servicio de atención al cliente.

**¿Qué sucede si solo conozco el identificador de mi organización de Experience Cloud? ¿Cómo busco el nombre de mi identificador de organización?**

Puede encontrar el nombre de su organización en [Organizaciones y configuración de cuentas](https://marketing.adobe.com/resources/help/en_US/mcloud/?f=organizations).

**Veo una fecha en la columna “Fecha de asignación”. ¿Quién realizó esta asignación?**

Puede consultar el registro de Cambios del grupo de informes, en la interfaz de Analytics, para ver qué identificador de usuario realizó el cambio. Busque el evento “Suite associated to IMS Organization” (Grupo asociado a organización IMS).
