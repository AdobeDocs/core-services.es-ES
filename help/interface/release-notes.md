---
description: '''Últimas funciones, notas de la versión y problemas conocidos de los servicios de Experience Cloud, como atributos del cliente, audiencias y administración de usuarios.'''
keywords: servicios principales
solution: Experience Cloud
title: 'Notas de versión acumuladas '
uuid: fcff8cc6-e587-4bf2-9a75-261d4eabc7d4
feature: '"Atributos del cliente"'
topic: Administración
role: Admin
level: Experienced
exl-id: b71d144c-a097-4cdb-9721-671519d38aff
source-git-commit: 31cfb3a85c255b72cbe5599aca09494c22fe4301
workflow-type: tm+mt
source-wordcount: '4224'
ht-degree: 88%

---

# Notas de versión acumuladas

Funciones, notas de la versión y problemas conocidos de los componentes de la interfaz central del Experience Cloud.

Para obtener una lista de actualizaciones de documentación, consulte [Experience Cloud](doc-updates.md#concept_4C8983FCD23848A4B1E4C2D99ED82784).

Para ver las notas de la versión de todas las soluciones, consulte las [Notas de la versión de Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=es).

## Julio de 2021

La búsqueda unificada se ha actualizado para que esté disponible para Journey Optimizer, Ofertas y Experience League. Anteriormente, esta función solo estaba disponible para usuarios Experience Platform.

## Junio de 2021

| Función | Fecha | Descripción |
| ------- | ------- | ------- |
| Compatibilidad con inicio de sesión único para Federated ID de Adobe | 17 de junio de 2021 | Si utiliza Federated ID, puede iniciar sesión en Experience Cloud sin tener que indicar una dirección de correo electrónico o contraseña. Para utilizar esta función, añada `#/sso:@domain` a la dirección URL del Experience Cloud. <br>Por ejemplo, suponga que es el propietario del dominio `adobecustomer.com` y que desea iniciar sesión en Adobe Analytics. La dirección URL sería: `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`. |
| Búsqueda en Experience League | 1 de junio de 2021 | Se ha mejorado la búsqueda de documentación de Experience League. Vaya a [Experience League](https://experienceleague.corp.adobe.com/docs/?lang=en) y utilice el campo **[!UICONTROL Búsqueda]** para encontrar tutoriales, documentación, cursos y más. |

{style=&quot;table-layout:auto&quot;}

## Mayo de 2021

| Función | Fecha | Descripción |
| ------- | ------- | ------- |
| Encabezado y navegación de Experience Cloud | 20 de mayo de 2021 | Las actualizaciones de Adobe Experience Cloud incluyen un cambio del encabezado en el tema claro, con la capacidad de volver fácilmente al tema oscuro y un vínculo para controlar las preferencias adicionales de su avatar de usuario en el encabezado de Experience Cloud. Aunque no todas las aplicaciones de Experience Cloud admiten temas, esta función desbloquea la futura compatibilidad con temas. |
| Búsqueda global en Experience Cloud | 20 de mayo de 2021 | Con esta versión, la búsqueda global en Experience Cloud le permite buscar en cualquiera de los documentos, cursos y tutoriales de [Experience League](https://experienceleague.adobe.com/?lang=es#home). (Actualmente, la búsqueda global solo está disponible para los usuarios de Experience Platform. La búsqueda global de [!UICONTROL Platform] le permite buscar cualquier objeto empresarial en Experience Cloud, como segmentos, conjuntos de datos, esquemas, etc.). |
| Preferencias de idioma de Experience Cloud | 20 de mayo de 2021 | Esta actualización incluye la posibilidad de establecer sus idiomas preferidos en las [Preferencias](https://experience.adobe.com/preferences) de Experience Cloud. |

{style=&quot;table-layout:auto&quot;}

## Agosto de 2020

| Función | Descripción |
| -----------| ---------- |
| Herramienta de administrador: políticas | Esta página muestra la lista completa de las directivas de Experience Cloud en su organización. Proporciona información sobre productos, instancias, usuarios y desarrolladores. Puede buscar, ordenar y filtrar vistas personalizadas de la lista de directivas. Consulte la ayuda de la [herramienta de administración de Experience Cloud](admin-tool-experience-cloud.md) para obtener más información. |

{style=&quot;table-layout:auto&quot;}

## Abril de 2020

* La página [!UICONTROL Fuente] de Experience Cloud estaba en desuso. (EXC-8505)
* La página de inicio de sesión de Experience Cloud se ha actualizado para incluir detalles de las marcas. (EXC-10747)

## Febrero de 2020

| Función | Descripción |
| -----------| ---------- |
| Herramienta de administración: ver detalles del usuario | Los administradores pueden ver una lista de los usuarios de Experience Cloud que pueden ordenar y filtrar, y sus detalles en la nueva herramienta de administración. Los detalles del usuario incluyen el acceso al producto, las funciones y la información a la que accedió por última vez. Consulte la ayuda de la [herramienta de administración de Experience Cloud](admin-tool-experience-cloud.md) para obtener más información. |

{style=&quot;table-layout:auto&quot;}

**Correcciones**

* **Atributos del cliente:** La interfaz de usuario de Atributos del cliente ahora muestra estados adicionales de perfiles sincronizados en Target. (MCUI-10231)
* **Servicio principal de Triggers:** Debido a la falta de uso, se ha eliminado la puntuación de propensión “Probabilidad de retorno en 30 días” al crear un activador de tipo Abandono. (MCUI-10056)

## Enero de 2020

* La página Fuente dejó de usarse en diciembre de 2019. Busque un aviso de obsolescencia del producto. (MCUI-10039)

## Agosto de 2019

* Se ha corregido un problema crítico en el inicio de sesión de Experience Cloud que llevaba al cierre de sesión de algunos usuarios. (MCUI-6908)
* Se ha actualizado el inicio de sesión de Experience Cloud para mejorar el rendimiento y reducir la latencia. (MCUI-6854, MCUI-6869, MCUI-6883)
* Interfaz actualizada de forma cosmética. (MCUI-6861, MCUI-6911, MCUI-6862)
* Se ha corregido un problema con los [!UICONTROL Triggers] de Experience Cloud, que provocaba una interpretación incorrecta de la cláusula _Me gusta_ en la definición de [!UICONTROL Activador]. (MCUI-6611)

## Abril de 2019

* Se ha actualizado el conmutador de aplicación para incluir Marketo en el paquete de soluciones de Experience Cloud y se han añadido actualizaciones de marca en Experience Platform. (MCUI-6529)
* Se ha actualizado Experience Cloud Home para incluir vínculos de navegación a las páginas de Fuentes y Administración. (MCUI-6682)
* Se ha corregido un problema en la definición [!UICONTROL de activador] para el uso correcto de la cláusula &quot;like&quot;. (MCUI-6611)
* Se han mejorado los Atributos del cliente para un mejor inicio de sesión en el servicio de Suscripción. (MCUI-6519)

## Versión 19.1.1: 17 de enero de 2019

**Nota:** En marzo de 2019, la interfaz de Experience Cloud no admitirá Internet Explorer 11.

* Se ha corregido un problema que impedía que la búsqueda de ayuda devolviera resultados. (MCUI-1670)
* Se corrigió y mejoró la administración de eVar en Triggers. (MCUI-6400)

## Versión 16.5.1: 26 de mayo de 2016 {#section_3785F182BC13493F84903CA69EB6D0A8}

**Características y mejoras**

<table id="table_ABBCE1A66F534059BD728BC2B9AEFA80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Configuraciones de producto preconfiguradas en Admin Console </p> </td> 
   <td colname="col2"> <p>Los administradores de clientes Experience Cloud pueden utilizar configuraciones de producto precreadas y asignadas a grupos de permisos predeterminados para Analytics y Dynamic Tag Management. </p> <p>Esta optimización está disponible para las organizaciones que se han aprovisionado recientemente y reduce la cantidad de tiempo que las organizaciones necesitan para administrar usuarios en Admin Console. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mejora de la fuente </p> </td> 
   <td colname="col2"> <p> Al crear una publicación en la fuente de Experience Cloud, la línea "A" utiliza ahora el tema que se encuentra activo en lugar de utilizar la organización de forma predeterminada.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* Se ha corregido un problema que impedía que se mostrasen las miniaturas de los activos compartidos desde Assets on Demand a la fuente de Experience Cloud. (MAC-29955)

## Versión 16.2: 18 de febrero de 2016 {#section_D9610373116C4D77A38F67815C725EA3}

<table id="table_C9B288CF42034F329C3C72D95D22E515"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Mejoras en Experience Cloud Assets </p> </td> 
   <td colname="col2"> <p>En Experience Cloud Assets, puede almacenar, compartir y sincronizar sus recursos digitales desde una ubicación central. Recursos de Experience Cloud utiliza algunas de las funciones disponibles en <span class="keyword"> Adobe Experience Manager</span> (AEM). </p> <p>Consulte <a href="experience-cloud-assets.md#concept_DDA5224C907D4A4F817D795DA0ED64D0" format="dita" scope="local">Experience Cloud</a></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mejoras en la vinculación de cuentas </p> </td> 
   <td colname="col2"> <p>Mejora del flujo de trabajo de la interfaz para vincular cuentas de soluciones con Experience Cloud (Adobe ID). Este nuevo flujo de trabajo localiza todas las cuentas de usuario asociadas con una organización y le permite elegir la cuenta que desea vincular. También hemos optimizado la experiencia de vinculación de cuentas para que ya no tenga que acceder a la página Administrar organizaciones para vincular cuentas manualmente. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* Se ha corregido un problema que impedía la vinculación y SSO para Analytics. Este problema mostraba el mensaje “Notificación: Mensaje de error: ERROR IMS SSO: No se puede encontrar la compañía vinculada”.

**Problema conocido**

Si accede a Dynamic Tag Management a través de la interfaz de **[!UICONTROL Experience Cloud]** > **[!UICONTROL Activation]**, pero su cuenta de Dynamic Tag Management no está vinculada a Experience Cloud (Adobe ID), no podrá iniciar sesión en Dynamic Tag Management. Para evitar este problema, acceda directamente a la página `dtm.adobe.com` en una nueva pestaña del navegador.

## Versión 16.1: 21 de enero de 2016 {#section_33B3F7DF6CA347E3AA93801BAC6232CE}

<table id="table_4223658257DA41C999AC710A10D26771"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Mensajes de la biblioteca de audiencias </td> 
   <td colname="col2"> <p> Hemos mejorado la biblioteca de audiencias para incluir mensajes útiles al crear audiencias o en caso de tiempos de espera. </p> <p>Por ejemplo, cuando se agregan más de cinco reglas, aparece un mensaje que indica que se ha superado el máximo permitido de reglas. (MAC-27376, MAC-27375) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Microsoft® está [terminando con soporte](https://www.microsoft.com/es-es/WindowsForBusiness/End-of-IE-support) para Internet Explorer 8, 9 y 10. Debido a esto, no corregiremos los problemas notificados en relación con estas versiones específicas de Internet Explorer.

## Versión 15.10: 14 de octubre de 2015 {#section_68123833D3634BD3A473C12862BF9606}

**Problemas conocidos**

* Los clientes no pueden iniciar sesión en el Report Builder si realizan un inicio de sesión único (SSO) en Analytics mediante Experience Cloud. Este problema no afecta a los clientes que utilizan credenciales de Analytics heredadas.
* Problema conocido con la función “Vincular a informe” en Analytics. Los clientes que inician sesión en Analytics mediante Experience Cloud son dirigidos a una página de inicio de sesión que no es único para Analytics al intentar compartir un informe.

## Versión 15.9: 10 de septiembre de 2015 {#section_BCCE3E7DF62A4FF5A57B9C8FE2A5F37B}

* Se ha corregido un problema de rendimiento de la API de Audience Manager que provocaba agotamientos intermitentes del tiempo de espera al cargar datos de los Atributos del cliente. (MAC-26305)
* Se ha corregido un problema que impedía a los usuarios añadir un máximo de 200 Atributos del cliente a una suscripción. (MAC-26188)
* Se ha corregido un problema con la biblioteca de audiencias que impedía compartir audiencias desde la segmentación de Analytics. Este problema hacía que se mostrara “Recopilación de datos” (0 audiencias). Para evitar este problema, Adobe recomienda mantener el tamaño de los segmentos por debajo de los 50 000 miembros de la audiencia por segmento. (MAC-25788)
* Se ha corregido un problema ya conocido en la página Atributos del cliente: Editar esquema que daba lugar a la aparición de un error Según el contenido al cambiar un nombre para mostrar. (MAC-25589, AN-103834)

## Versión 15.7: 22 de julio de 2015 {#section_2683A152176944E48EF6C943892975B7}

* Se ha corregido un problema que impedía que las descripciones de atributos especificadas en la página Vista/Editar esquema (en atributos del cliente) se actualizaran en los informes de Analytics. (MAC-25985)
* Se ha corregido un problema que impedía que se representaran las miniaturas de los recursos cargados. (MAC-25863)
* Se ha corregido un problema que impedía que los nuevos segmentos creados en Reports &amp; Analytics estuvieran disponibles en Experience Cloud Audiences. (MAC-25817)
* Se ha corregido un problema que impedía compartir audiencias desde Analytics cuando se utiliza el servicio de ID de visitante. (MAC-25788, MAC-25747)
* Ahora se admiten caracteres multibyte en los Atributos del cliente. (MAC-25552)

**Problema conocido**

Un problema conocido provoca la creación de cuentas autogeneradas duplicadas en Audience Manager y su vinculación automática con la identidad de un usuario en Experience Cloud. Este problema se produce si intenta navegar a Audience Manager antes de vincular las cuentas. Adobe recomienda vincular las cuentas de Audience Manager a Experience Cloud antes de navegar a Audience Manager. (MAC-25640)

## Versión 15.6.1: 11 de junio de 2015 {#section_AD2019F8D2F84C9EB2B0533FAACF7043}

No hay información disponible.

## Versión 15.5.1: 13 de mayo de 2015 {#section_EF197410964E40D294D0D8024738CFBA}

<table id="table_14E7B35E06C84A258A21D09691B58354"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>Los menús de navegación de la izquierda se han actualizado y organizado para proporcionar acceso a todos los servicios y soluciones principales. Los cambios más destacables incluyen: </p> 
    <ul id="ul_5BEBAB86B9234A239C4E2DAF8826D8E3"> 
     <li id="li_7FA9F64CE69144B8A8A92746BF40E5A1">Las selecciones de menú<span class="term"> Biblioteca de audiencias </span> y <span class="term"> Atributos del cliente </span> ahora se encuentran en <span class="term">Audiencias</span>. </li> 
     <li id="li_95D62A43AE6243DBB2A65EDB830D05C4">La selección de menú <span class="term"> Exchange </span> se ha trasladado del menú desplegable Ayuda al carril de navegación izquierdo. </li> 
     <li id="li_0443FD50C78446CD8AA27A4F272CAD31"> Se ha eliminado <span class="term">Soluciones</span>. Podrá iniciar todas las soluciones desde la mitad inferior del carril de navegación. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

* Se ha corregido un problema que impedía que los atributos del cliente se sincronizaran para algunos clientes.
* Se ha corregido un problema que impedía que [la página de documentación de producto de Adobe Target](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=es) se mostrara en japonés.
* Se ha corregido un problema que impedía el uso de texto en japonés en comentarios entre [!DNL Creative Cloud] el y [!DNL Experience Cloud]el.

## Versión 15.4.1: 8 de abril de 2015 {#section_75634120CC934B3381EDEA7F6F976F0A}

<table id="table_3A6FBAE36558425A803B078150862C92"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Mejoras en la administración: </p> 
    <ul id="ul_7D5FCBEFA262435D865CA1018BFB792E"> 
     <li id="li_6E98974CCB094ABBAB57C51ED56C3F00"> <span class="wintitle"> Admin Console</span> </li> 
     <li id="li_8CDAB6301FD44C3999EE4EEB1A0A2FD6">Soporte empresarial y para Federated ID </li> 
    </ul> </td> 
   <td colname="col2"> <p>La funcionalidad de administración de usuarios y grupos se ha trasladado a Admin Console. La nueva ruta de navegación es: </p> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol">Administration</span> &gt; <span class="uicontrol">Iniciar Admin Console</span></p> <p> Además, se ha agregado compatibilidad con Enterprise ID y Federated ID. Puede utilizar Enterprise ID, Federated ID y Adobe ID en la misma implementación empresarial. Por ejemplo, utilice un Adobe ID para los usuarios que puedan utilizar otros productos y servicios de Adobe. Utilice Enterprise ID o Federated ID para los usuarios en los que desee administrar estrictamente sus cuentas. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* Se ha corregido un problema que impedía el inicio de sesión único entre [!DNL Experience Cloud] y [!DNL Media Optimizer].

**Problemas conocidos**

* Vincular y desvincular la organización de Dynamic Tag Management con Experience Cloud no funciona para las organizaciones de Experience Cloud recién creadas. Adobe está trabajando para corregir esto y restaurar la funcionalidad normal con la versión de mayo. Si tiene problemas al intentar realizar el inicio de sesión único en la Dynamic Tag Management por medio de Experience Cloud, use el inicio de sesión preexistente en [!DNL dtm.adobe.com].
* Un problema recurrente impide el uso compartido de audiencias de grupos de informes que no son propiedad de la cuenta de Analytics vinculada. Se están tomando medidas correctivas

## Versión 15.3.2: 19 de marzo de 2015 {#section_07760FD9CA43497FA8BDCCA990A24BFD}

<table id="table_54025DBE2D094FF1BE837BA60816C6DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Atributos del cliente </p> </td> 
   <td colname="col2"> <p>Si captura los datos del cliente empresarial en una base de datos de administración de la relación con los clientes (CRM), puede cargar los datos en un origen de datos de Atributos del cliente en el Experience Cloud. Una vez cargados los datos, puede ejecutar los informes de <span class="uicontrol">Perfil del visitante</span> &gt; <span class="uicontrol">Atributos del cliente</span> en Analytics. </p> <p>También puede utilizar los datos cargados como un segmento de audiencia en <span class="keyword">Adobe Target</span>. </p> <p>Consulte la documentación del producto <a href="attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1" format="dita" scope="local">Atributos del cliente</a>. </p> <p> Para obtener información sobre la modernización de las soluciones para los servicios principales, consulte <a href="core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">Activación de las soluciones para los servicios principales</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Versión 15.3.1: 4 de marzo de 2015 {#section_57CB69C044DD47BDBC1A1BEC38957551}

<table id="table_EB3FFBA2DF904546A5185EC9A63BBA98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Asignación de grupos </p> </td> 
   <td colname="col2"> <p>La página Administración de grupos se ha rediseñado como interfaz administrativa que permite crear grupos, agregar usuarios a grupos y aplicar permisos en las soluciones de Experience Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Asignación de uno a varios </p> </td> 
   <td colname="col2"> <p>Al vincular cuentas de soluciones en Experience Cloud, si cuenta con varias soluciones y organizaciones, ahora puede asignar varios productos y servicios a una única organización. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activation </p> </td> 
   <td colname="col2"> <p> <a href="activation.md#concept_EE756B6B0A0643DAB8CA3A00E665406C" format="dita" scope="local"> Activation</a> ahora aparece en la sección de navegación izquierda de <span class="keyword">Experience Cloud</span>. <span class="wintitle"> </span> Activationes un servicio de  <span class="keyword"> Experience </span> Cloud que actualmente consta de la tecnología de administración dinámica de etiquetas y le dirige allí cuando está seleccionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Actualizaciones de documentación: Servicios principales </p> </td> 
   <td colname="col2"> <p>Se ha añadido el tema <a href="core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">Activación de las soluciones en los servicios principales</a> para ayudarle en la implementación de los servicios principales. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Versión 15.2.1: 19 de febrero de 2015 {#section_BC694D5AE16A4E16B44B353ED67947F3}

Correcciones:

* Se ha mejorado el flujo de trabajo de invitación de correo electrónico del usuario para el aprovisionamiento de cuentas.
* Se ha corregido un problema de carpeta de recursos que impedía [!DNL Experience Cloud] que [!DNL Adobe Campaign] se mostraran jerarquías de carpeta idénticas.
* Se ha corregido un problema que impedía eliminar audiencias que formaban parte de las actividades de [!DNL Target] desactivadas.
* Se ha corregido un problema que impedía que el icono Agregar (más) se mostrase en [!UICONTROL Reglas] en la página [!UICONTROL Crear nueva audiencia].
* Se ha mejorado la compatibilidad de la interfaz de Experience Cloud con Internet Explorer 9.

## Versión 15.1.1: 15 de enero de 2015 {#section_F1A352E928AF432E94CC0A289C345184}

Nuevas funciones y correcciones en la interfaz de colaboración y uso compartido de [!DNL Adobe Experience Cloud].

<table id="table_AD0A8CA760E64227BB04BA6B0E425E80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Acceso de solo lectura. </p> </td> 
   <td colname="col2"> <p>Los administradores ahora pueden otorgar acceso de solo lectura a los usuarios no administradores. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* Se corrigió un problema en el cual los archivos PNG no se podían representar en una tarjeta.
* Se ha corregido un problema con la carga de archivos en Experience Cloud Assets mediante un proceso de arrastrar y soltar.

**Problemas conocidos**

* Los usuarios no pueden compartir archivos de PowerPoint en tableros.
* Los cambios en grupos y autorizaciones realizados en Administración de usuarios no se aplican hasta después de volver a iniciar sesión.
* Algunos usuarios pueden tener problemas al cargar tipos de archivos de tamaño grande a los recursos de Experience Cloud.
* Los usuarios pueden echar en falta enlaces en sus tarjetas de Experience Cloud procedentes de Media Optimizer.
* Algunos usuarios administrativos pueden tener problemas al enlazar sus cuentas después de aceptar una invitación para unirse a Experience Cloud.
* El rendimiento de la interfaz de Experience Cloud se puede reducir cuando varios usuarios la utilizan en paralelo.
* Algunos usuarios pueden eliminar un recurso que no esté actualizado en lugar de recibir una notificación de error.
* Algunos usuarios pueden tener problemas al iniciar sesión en dos exploradores con el mismo Adobe ID simultáneamente.
* Puede ser que algunos usuarios no puedan añadir de nuevo un usuario de Creative Cloud a una carpeta compartida después de que se haya eliminado el usuario de Creative Cloud.
* Algunos usuarios pueden experimentar un retraso en la notificación que se produce cuando una carpeta se comparte desde Experience Cloud en Creative Cloud.
* Algunos usuarios pueden tener problemas al compartir una carpeta entre Experience Cloud y Creative Cloud.
* Algunos usuarios pueden tener problemas para crear una audiencia dentro de un grupo de informes de Analytics después de habilitar las audiencias compartidas.
* Es posible que algunos usuarios tengan problemas al cargar recursos en un tablero.

## Versión 14.11.1: 13 de noviembre de 2014 {#section_A6CF1D4F27B9496892A89C983EB39102}

Problemas conocidos:

* Algunos usuarios pueden eliminar un recurso que no esté actualizado en lugar de recibir una notificación de error.
* Algunos archivos [!DNL .png] no se pueden representar en una tarjeta.
* Es posible que algunos usuarios tengan problemas al cargar recursos en un tablero.
* Los cambios en grupos y autorizaciones realizados en administración de usuarios no se aplican hasta después de volver a iniciar sesión.
* Los administradores deben cerrar la sesión y volver a iniciarla para ver los cambios realizados en Configuración de la cuenta.
* Los usuarios no pueden compartir archivos de PowerPoint en tableros.
* El rendimiento de la interfaz de [!DNL Experience Cloud] se puede reducir cuando muchos usuarios la utilizan en paralelo.
* La sincronización de Adobe Experience Manager con Creative Cloud no funciona.

## Versión 14.10.1: 16 de octubre de 2014 {#section_E3A0F4423B814707AA3745E083500835}

Nuevas funciones y correcciones en la interfaz de colaboración y uso compartido de [!DNL Adobe Experience Cloud].

<table id="table_7C1ACE8108D54782AE128ACD35069DF5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Editar permisos de usuario </p> </td> 
   <td colname="col2"> <p>Los propietarios de un tablero ahora pueden editar los permisos de usuario en el tablero. </p> <p> 
     <ol id="ol_B12251C510744538AF9BCE60ACB04016"> 
      <li id="li_87B3EDE9542B47CEBE0BE7F2D1DE844D">En el tablero, seleccione <span class="uicontrol"> Configuración</span>. </li> 
      <li id="li_0F4786B0E1E743069D082E7DC488A031">Junto a cada propietario, especifique <span class="uicontrol">Propietario</span>, <span class="uicontrol">Visualizador</span> o <span class="uicontrol">Editor</span>. </li> 
     </ol> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* Crear una tarjeta desde un PDF y compartirla en el tablero devolvía un mensaje de error.

**Problemas conocidos**

* Es posible que algunos usuarios tengan problemas al cargar recursos en un tablero.
* Algunos archivos [!DNL .png] no se pueden representar en una tarjeta.
* Los cambios en grupos y autorizaciones realizados en administración de usuarios no se aplican hasta después de volver a iniciar sesión.
* Es posible que algunos usuarios no puedan crear una tarjeta a partir de un PDF y compartirla en un tablero.
* Algunos usuarios pueden eliminar un recurso que no esté actualizado en lugar de recibir una notificación de error.
* Los usuarios no pueden compartir archivos de PowerPoint en tableros.
* El rendimiento de la interfaz de [!DNL Experience Cloud] se puede reducir cuando muchos usuarios la utilizan en paralelo.
* Los vínculos de [!DNL Search&Promote] no están disponibles en la página [!UICONTROL Organización y acceso a productos].

## Versión 14.9.1: 18 de septiembre de 2014 {#section_20F156A9CC2F4FC59C4970075C181D3A}

**Correcciones y mejoras**

* Cuando navega a [!DNL experience.adobe.com], la experiencia de inicio de sesión es ahora coherente con el inicio de sesión de Creative Cloud de Adobe.
* En la página Administrar organizaciones, la experiencia de vinculación (una vez recibida la invitación) ahora es consistente en todas las soluciones.

**Problemas conocidos**

* Los cambios en grupos y autorizaciones realizados en administración de usuarios no se aplican hasta después de volver a iniciar sesión.
* Algunos usuarios no pueden crear una tarjeta a partir de un PDF y compartirla en un tablero.
* Es posible que algunos usuarios tengan problemas al cargar recursos en un tablero.
* Algunos usuarios pueden eliminar un recurso que no esté actualizado en lugar de recibir una notificación de error.
* Los usuarios no pueden compartir archivos de PowerPoint en tableros.
* Algunos archivos [!DNL .png] no se pueden representar en una tarjeta.
* El rendimiento de la interfaz de [!DNL Experience Cloud] se puede reducir cuando muchos usuarios la utilizan en paralelo.
* Los vínculos de [!DNL Search&Promote] no están disponibles en la página [!UICONTROL Organización y acceso a productos].
* Puede que algunos usuarios observen que el contenido de [!DNL Creative Cloud] se elimina de sus carpetas si se deja de compartir el contenido en [!DNL Experience Cloud].

## Versión 14.8.1: 21 de agosto de 2014 {#section_03BF00F6A95A490C91BCC0A1988FA7AA}

Nuevas funciones y correcciones en la interfaz de colaboración y uso compartido de [!DNL Adobe Experience Cloud].

<table id="table_1E7DBEB5E83B4E4285B6FD1D718CD16D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>Ahora puede acceder a <span class="keyword">Adobe Mobile Services</span> desde el menú de navegación de la izquierda. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemas conocidos**

* Los cambios en grupos y autorizaciones realizados en administración de usuarios no se aplican hasta después de volver a iniciar sesión.
* Es posible que algunos usuarios no puedan crear una tarjeta a partir de un PDF y compartirla en un tablero.
* Es posible que algunos usuarios tengan problemas al cargar recursos en un tablero.
* Es posible que algunos usuarios no puedan iniciar sesión en [!DNL Target] desde [!DNL Experience Cloud].
* Algunos usuarios de Audience Manager no pueden iniciar sesión en [!DNL Experience Cloud].
* Algunos usuarios pueden eliminar un recurso que no esté actualizado en lugar de recibir una notificación de error.
* Los archivos eliminados de [!DNL Experience Cloud] no se eliminan de [!DNL Digital Asset Management].
* Los usuarios no pueden compartir archivos de PowerPoint en tableros.
* Algunos archivos [!DNL .png] no se pueden representar en una tarjeta.
* El rendimiento de la interfaz de [!DNL Experience Cloud] se puede reducir cuando muchos usuarios la utilizan en paralelo.
* Los vínculos de [!DNL Search&Promote] no están disponibles en la página [!UICONTROL Organización y acceso a productos].
* Puede que algunos usuarios observen que el contenido de [!DNL Creative Cloud] se elimina de sus carpetas si se deja de compartir el contenido en [!DNL Experience Cloud].

## Versión 14.7.1: 24 de julio de 2014 {#section_B22D4F830756463DB27BB4D508D9ADD5}

Nuevas funciones y correcciones en la interfaz de colaboración y uso compartido de [!DNL Adobe Experience Cloud].

**Problemas conocidos**

* Los archivos eliminados de [!DNL Experience Cloud] no se eliminan de [!DNL Digital Asset Management].
* Puede que algunos usuarios de [!UICONTROL Exchange] encuentren sus nombres en los comentarios como un ID de cadena largo en lugar de sus nombres.
* Algunos archivos [!DNL .png] no se pueden representar en una tarjeta
* La carga de archivos permite más tipos de archivo que el método de arrastrar y soltar. Para obtener los mejores resultados, realice la carga mediante [!UICONTROL Assets].
* Los vínculos de [!DNL Search&Promote] no están disponibles en la página [!UICONTROL Organización y acceso a productos].
* Los usuarios de [!DNL Exchange] deben borrar las cookies para obtener una mejor experiencia.
* La interfaz de [!DNL Experience Cloud] se puede ralentizar cuando la usan en paralelo varios usuarios.
* Puede que algunos usuarios observen que el contenido de [!DNL Creative Cloud] se elimina de sus carpetas si se deja de compartir el contenido en [!DNL Experience Cloud].
* Su sesión se cerrará tras 15 minutos de inactividad. Además, cuando se cierra la sesión en una ubicación, también se cierra la sesión de [!DNL Experience Cloud].
* Es probable que algunos usuarios no puedan vincular su cuenta de Audience Manager con [!DNL Experience Cloud].
* Los usuarios de [!UICONTROL Exchange] solo pueden ver la opción Inglés en el selector de idioma.

**Correcciones**

Ninguna en esta versión.

## Versión 14.6.1: 19 de junio de 2014 {#marketing_cloud_interface}

Nuevas funciones y correcciones en la interfaz de colaboración y uso compartido de [!DNL Adobe Experience Cloud].

**Mejora**

<table id="table_C9BD63436BF0414B97B8D07387D1993B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Botón <span class="wintitle">Guardar</span> en Audiences </p> </td> 
   <td colname="col2"> <p>Cuando crea una audiencia, el botón <span class="wintitle">Guardar</span> en la página <span class="wintitle">Crear audiencia nueva</span> ahora está desactivado hasta que se cumplimenten los campos obligatorios. 
     <!--MAC-19712 --></p> </td> 
  </tr> 
 </tbody> 
</table>

**Problemas conocidos**

* Los archivos eliminados de [!DNL Experience Cloud] no se eliminan de [!DNL Digital Asset Management].
* La carga de archivos permite más tipos de archivo que el método de arrastrar y soltar. Para obtener los mejores resultados, realice la carga mediante Assets.
* Los vínculos de [!DNL Search&Promote] no están disponibles en la página [!UICONTROL Organización y acceso a productos].
* Los filtros aplicados en los informes de tendencias de [!DNL Analytics] no se aplican a las tarjetas en [!DNL Experience Cloud].
* Algunos usuarios no pueden vincular su cuenta de gestión de audiencia con su cuenta de [!DNL Experience Cloud].
* Su sesión se cerrará tras 15 minutos de inactividad. Además, cuando se cierra la sesión en una ubicación, también se cierra la sesión del Experience Cloud.
* Puede que algunos usuarios de Exchange encuentren sus nombres en los comentarios como un ID de cadena largo en lugar de sus nombres.

**Correcciones**

* Se ha corregido un problema que impedía la carga de vídeo en las aplicaciones.

## Versión 14.5.1: 22 de mayo de 2014 {#section_7E22B2CB3ABA4D6EAED8CA8EFDE5433E}

<table id="table_4E4B34EEE3D94D78BA1A1FBC62950559"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud Exchange </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol">Ayuda</span> &gt; <span class="uicontrol">Exchange</span></p> <p><span class="keyword">Experience Cloud</span> <span class="wintitle">Exchange</span> es un destino único en el que puede buscar, examinar, seleccionar, adquirir y descargar extensiones de marketing digital mediante aplicaciones. </p> <p>Las aplicaciones incluyen Data Connectors, configuraciones personalizadas para el producto central del Adobe, aplicaciones de terceros, informes y tarjetas <span class="keyword"> Experience Cloud</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Audiencias de Experience Cloud </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol">Audiencias</span></p> <p> En <span class="wintitle">Audiencias</span> es donde se crean, editan y administran audiencias, de forma parecida a como se trabaja con segmentos. Por ejemplo, puede crear un segmento en Reports &amp; Analytics y luego compartirlo en <span class="wintitle"> Experience Cloud</span><span class="wintitle"> Audiencias</span>. Una vez que se crea, la audiencia queda disponible en <span class="keyword">Adobe Target</span> para actividades de campaña y en Adobe Audience Manager para la segmentación. </p> <p> <p>Nota: Para solicitar la habilitación en Target, visite <a href="https://adobe.allegiancetech.com/cgi-bin/qwebcorporate.dll?idx=X8SVES" format="http" scope="external"> https://adobe.allegiancetech.com/cgi-bin/qwebcorporate.dll?idx=X8SVES</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>Los usuarios que se mencionan en tarjetas de <span class="keyword">Experience Cloud</span> ahora tienen permiso para acceder a ellas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>Los nuevos usuarios de Adobe pueden vincular sus cuentas de Scene7 a Adobe ID y a los integrantes del equipo. Los administradores también pueden desvincular usuarios de cuentas de Scene7. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sincronización de recursos. </p> </td> 
   <td colname="col2"> <p> Puede compartir recursos dentro de Recursos de Experience Manager con el Experience Cloud y el Creative Cloud. Cualquier cambio en estos recursos se refleja en las copias compartidas de los recursos en Experience Cloud y Creative Cloud. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* [!DNL Experience Cloud] no se estaba vinculando a [!DNL Adobe Target]. Este problema ocurría si el inicio de sesión en [!DNL Adobe Target] se puede usar en varios servidores de [!DNL Target].
* [!DNL Adobe Media Optimizer] no creaba usuarios automáticamente cuando estos se habían creado en [!DNL Experience Cloud].
* Las opciones en los cuadros combinados utilizados para agregar nuevos usuarios de forma temporal desaparecían al escribir.
* El vínculo Comentarios en la vista de tarjetas de recursos no se podía seleccionar.
* Después de agregar una etiqueta personalizada a un recurso, no se mantenían otros cambios en los metadatos.
* Al eliminar una imagen, Assets no informa de si la imagen se utiliza en Adobe Target Essentials.
* El rendimiento de la interfaz de [!UICONTROL Experience Cloud] era lento cuando muchos usuarios lo utilizaban simultáneamente.
* Al eliminar una imagen en [!UICONTROL Experience Cloud Assets], no se mostraba una advertencia si la imagen se estaba utilizando en [!DNL Adobe Target Essentials].
* Si la opción **[!UICONTROL Recordarme]** no estaba seleccionada durante el inicio de sesión, se cerraba la sesión del usuario a los 15 minutos.
* Los usuarios debían cerrar la sesión y volver a iniciarla para que se apliquen todos los cambios de permisos y autorizaciones.
* El inicio de sesión en [!DNL Experience Cloud] tardaba más de un segundo.
* Para determinados usuarios, al eliminar archivos de [!DNL Experience Cloud] no se realizó la sincronización con [!DNL Digital Asset Management].
* Se cerraba la sesión de los usuarios tras solo 15 minutos de inactividad del explorador.
* Los usuarios no podían compartir archivos de PowerPoint en tableros.
* Algunos usuarios tenían un diseño visual deficiente en Internet Explorer 10.

## Versión 14.4.1: 22 de abril de 2014 {#section_E2A699764E744D2E8D418E9A3D40AF6B}

<table id="table_D95C0DC64F2A4B47BAC83E504CFD6825"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Creación de tarjetas a partir de temas de ayuda </p> </td> 
   <td colname="col2"> <p>Después de habilitar la función Compartir con Adobe Experience Cloud en la barra de herramientas Marcadores del explorador, ahora puede compartir páginas de ayuda desde la dirección URL del micrositio. </p> <p> <b>Para compartir un tema de ayuda</b> </p> 
    <ol id="ol_F94B816121494B0FA16CC07B0E96AED8"> 
     <li id="li_F47187D4B5FE46D3A51D257DD569B4D6"> <p>En el <span class="keyword"> Experience Cloud</span>, seleccione <span class="uicontrol"> Administración</span>. </p> </li> 
     <li id="li_94EF58E7A4974B63951E14F72A710183"> <p>Arrastre el botón <span class="uicontrol">Compartir en Adobe Experience Cloud</span> a la barra de herramientas de Marcadores. </p> </li> 
     <li id="li_69EEC4F25D8F4AD7AA106A10B7F50FF6"> <p>Navegue a una página de ayuda (o permanezca en esta) y luego seleccione <span class="uicontrol"> Compartir con Adobe Experience Cloud</span> en la barra de herramientas de Marcadores del explorador. </p> <p>Este paso crea una tarjeta, que puede visualizar en <span class="wintitle">Experience Cloud</span>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* Después de agregar una etiqueta personalizada a un recurso, no se pueden mantener otros cambios en los metadatos.
* Los usuarios deben actualizar el tablero para que las tarjetas eliminadas desaparezcan de la vista.
* Cuando no se selecciona **[!UICONTROL Recordarme]** durante el inicio de sesión, se cierra la sesión del usuario tras 15 minutos.
* En la página de aterrizaje de la solución [!DNL Analytics] se muestran errores de formato.
* Los usuarios deben cerrar la sesión y volver a iniciarla para que se apliquen todos los cambios de permisos y autorizaciones.
* Al eliminar una imagen, [!UICONTROL Assets] no informa de si la imagen se utiliza en [!DNL Adobe Target Essentials].
* El vínculo Comentarios en la vista de tarjetas de recursos no se puede seleccionar.
* Las opciones en los cuadros combinados para agregar nuevos usuarios de forma temporal desaparecen al escribir.
* El inicio de sesión en [!DNL Experience Cloud] tarda más de un segundo.
* Los datos compartidos de [!DNL Media Optimizer] no se representan correctamente en [!DNL Experience Cloud].
* Adobe [!DNL Media Optimizer] no crea usuarios automáticamente cuando el usuario ha sido creado en [!DNL Experience Cloud].
* [!DNL Experience Cloud] no se puede vincular a [!DNL Adobe Target] si las credenciales de [!DNL Adobe Target] se pueden usar en varios servidores de [!DNL Target].
* La interfaz de [!DNL Experience Cloud] se puede ralentizar cuando la usan en paralelo varios usuarios.
* Los vínculos de [!DNL Search&Promote] no están disponibles en la página [!UICONTROL Organización y acceso a productos].
* Las tarjetas de simulación de [!DNL Adobe Media Optimizer] no se representan correctamente.
* Los filtros aplicados en los informes de tendencias de [!DNL Analytics] no se aplican a las tarjetas en [!DNL Experience Cloud].
* Los filtros aplicados en los informes de tendencias de Analytics no se aplican a las tarjetas en Experience Cloud.
* Algunos archivos CSV o de Excel no pueden cargarse en un tablero.
* Es probable que algunos usuarios no puedan vincular su cuenta de gestión de audiencia con su [!DNL Experience Cloud].
* Algunos usuarios experimentan un error al compartir segmentos de [!DNL Analytics] en [!DNL Experience Cloud].
* Es probable que algunos usuarios no puedan explorar las subcarpetas del [!UICONTROL Selector de recursos].
* Algunos usuarios no pueden compartir sus gadgets de AdLens en [!DNL Experience Cloud].

## Versión 14.3.1: 13 de marzo de 2014 {#section_5D142E3225E3477A84DC01B8197D39BC}

La versión 14.3.1 es una versión de mantenimiento que se centra en la velocidad, la estabilidad y la seguridad. No incluye nuevas funciones principales.

**Correcciones**

* Se añadió la capacidad de eliminar la imagen del avatar.
* Se ha corregido un problema impedía desvincular cuentas de [!DNL Adobe Media Optimizer].

**Problemas conocidos**

* Al eliminar una imagen en Experience Cloud Assets no se informa de si la imagen se utiliza en Adobe Target Essentials.
* Al actualizar una tarjeta en [!DNL Analytics], a veces podía causar que apareciera un gráfico vacío en la tarjeta ampliada.
* Los usuarios deben cerrar la sesión y volver a iniciarla para que se apliquen todos los cambios de permisos y autorizaciones.
* Cuando *`Remember me`* no se selecciona durante el inicio de sesión, la sesión del usuario se cierra a los 15 minutos.
* En la página de aterrizaje de la solución [!DNL Analytics] se muestran errores de formato.
* El vínculo Comentarios en la vista de tarjetas de recursos no se puede seleccionar.
* La interfaz de Experience Cloud se puede ralentizar cuando la usan en paralelo varios usuarios.
* Experience Cloud no se puede vincular a [!DNL Adobe Target] si las credenciales de [!DNL Adobe Target] se pueden usar en varios servidores de Target.
* El inicio de sesión en Experience Cloud tarda más de un segundo.
* Después de agregar una etiqueta personalizada a un recurso, no se pueden mantener otros cambios en los metadatos.
* [!DNL Adobe Media Optimizer] no crea usuarios automáticamente cuando el usuario ha sido creado en Experience Cloud.
* Las opciones en los cuadros combinados para agregar nuevos usuarios de forma temporal desaparecen al escribir.
* Los datos compartidos de [!DNL Media Optimizer] no se representan correctamente en Experience Cloud.
* Se producen errores al compartir imágenes de Flickr.
* Los filtros aplicados en los informes de tendencias de [!DNL Analytics] no se aplican a las tarjetas en Experience Cloud.
* Los cambios en grupos y autorizaciones realizados en administración de usuarios no se aplican hasta después de volver a iniciar sesión.
* Los vínculos de [!DNL Search&Promote] no están disponibles en [!UICONTROL Acceso de organizaciones y productos].
* Los usuarios deben actualizar el tablero para que las tarjetas eliminadas desaparezcan de la vista.
* Algunos archivos CSV o de Excel no pueden cargarse en un tablero.
* Las tarjetas de simulación de [!DNL Adobe Media Optimizer] no se representan correctamente.
* Algunos archivos PNG no se pueden representar en una tarjeta.
* No se puede enviar el comentario de la versión beta.

## Versión 14.2.1: 24 de febrero de 2014 {#section_5AD81B0737C843AFB4BE9C4420D70EB3}

<table id="table_DFAB002358C94A17A7F91DAB323A488F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Función </th> 
   <th colname="col2" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>OEmbed </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Actualización de datos </p> </td> 
   <td colname="col2"> <p> 
     <!--MAC-18174-->El icono <span class="uicontrol">Actualización de datos</span> que se muestra para un gráfico de una tarjeta ahora está oculto si la solución no admite la actualización de datos. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correcciones**

* Se ha corregido un problema que impedía que los informes compartidos de [!DNL Analytics] aplicaran filtros de segmento.
* Se ha corregido un problema que provocaba que las soluciones se mostraran como vinculadas en la página [!UICONTROL Soluciones de Experience Cloud] aunque las cuentas de las soluciones no estuvieran vinculadas.
* Se ha corregido un problema que impedía que los clientes de [!DNL Adobe Target] de Asia pudieran seleccionar el botón **[!UICONTROL Continuar al Experience Cloud]** en la página de vinculación.
* Se ha corregido un problema que impedía compartir vídeos de YouTube.
