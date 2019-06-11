---
description: Cree el origen de atributo del cliente y cargue los datos.
keywords: atributos del cliente; servicios principales
seo-description: Cree el origen de atributo del cliente y cargue los datos.
seo-title: Crear un origen de atributo de cliente y cargar el archivo de datos
solution: Experience Cloud
title: Crear un origen de atributo de cliente y cargar el archivo de datos
uuid: 53 dca 789-9 a 91-4385-839 d-c 9 d 1 aa 36 b 9 be
translation-type: tm+mt
source-git-commit: b6058194725c3ad50d280a3daad737cd53416204

---


# Crear un origen de atributo de cliente y cargar el archivo de datos

Cree el origen de atributo del cliente y cargue los datos. Puede activar el origen de datos cuando esté listo. Una vez esté listo el origen de los datos, comparta los datos del atributo con Analytics y Target.

## Flujo de trabajo de atributos del cliente {#concept_BF0AF88E9EF841219ED4D10754CD7154}

![](assets/crs.png)

1. [Cree un archivo de datos](../attributes/t-crs-usecase.md#task_B5FB8C0649374C7A94C45DCF2878EA1A)
1. [Crear un origen de atributo y cargar el archivo de datos](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [Validar el esquema](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [Configure suscripciones y activar el origen de atributos](../attributes/t-crs-usecase.md#task_1ACA21198F0E46A897A320C244DFF6EA)


Una vez el origen de datos esté activo, podrá:

* [Utilizar los atributos del cliente en Adobe Analytics](../attributes/t-crs-usecase.md#task_7EB0680540CE4B65911B2C779210915D)
* [Utilizar los atributos del cliente en Adobe Target](../attributes/t-crs-usecase.md#task_FC5F9D9059114027B62DB9B1C7D9E257)



>[!IMPORTANT]
>
>Para acceder a esta función, los usuarios deben estar asignados al perfil de producto Atributos del cliente (Atributos del cliente - Acceso predeterminado. ( **[!UICONTROL Administración]** &gt; Consola **[!UICONTROL de administración]** &gt; **[!UICONTROL Usuarios]** &gt;). Los usuarios que se agregan al grupo Atributos del cliente verán el elemento de menú [!UICONTROL Atributos del cliente] en [!UICONTROL Audiencia], en la parte izquierda de la interfaz de Experience Cloud.
>
>También es necesaria la pertenencia al grupo de la solución.

Para utilizar la función Atributos del cliente, los usuarios deben pertenecer al grupo Atributos del cliente de Adobe en la administración de usuarios, y a grupos en el nivel de solución (Analytics o Target).

Consulte [Usuarios y grupos](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9).

## Crear un archivo de datos {#task_B5FB8C0649374C7A94C45DCF2878EA1A}

Estos datos son datos de cliente empresarial de su CRM. Los datos pueden incluir datos de suscriptor de productos, incluidos los ID de miembro, productos con derechos, productos más utilizados y demás.


1. Cree un [!DNL .csv].


   >[!NOTE]
   >
   >Más adelante en este proceso, podrá arrastrar y soltar el [!DNL .csv] archivo para cargar el archivo. Sin embargo, si [carga mediante FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B), también necesitará [!DNL .fin] un archivo con el mismo nombre que [!DNL .csv]el.



   Archivo de datos de cliente empresarial de muestra:

   ![](assets/01_crs_usecase.png)

1. Antes de continuar, revise la información importante en [los requisitos](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)del archivo de datos antes de cargar el archivo.
1. [Cree un origen de atributo de cliente y cargue los datos](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78), que se describen a continuación.

## Crear un origen de atributo y cargar el archivo de datos {#task_09DAC0F2B76141E491721C1E679AABC8}

Siga estos pasos en la página Crear nuevo origen de atributos del cliente en Experience Cloud.


>[!IMPORTANT]
>
>Al crear, modificar o eliminar orígenes de atributos del cliente, hay un retraso de hasta una hora antes de que los ID empiecen a sincronizarse con la nueva fuente de datos. Debe tener derechos administrativos en Audience Manager para crear o modificar orígenes de atributos del cliente. Póngase en contacto con el servicio de atención al cliente de Audience Manager o con asesoría para obtener derechos administrativos.


1. En [!DNL Experience Cloud], haga clic ![](assets/menu-icon.png) en el icono Menú.
1. Haga clic **[!UICONTROL en Personas]** y, a continuación, haga clic **[!UICONTROL en Atributos del cliente]**.

   En la página [!UICONTROL Atributos del cliente] se gestionan y editan los orígenes de datos de atributos existentes.

   ![Resultado de paso](assets/03_crs_usecase.png)
1. Haga clic **[!UICONTROL en Nuevo]**.

   ![Resultado de paso](assets/04_crs_usecase.png)
1. En la página [!UICONTROL Editar origen de atributos del cliente], configure los siguientes campos:


   * **[!UICONTROL Nombre:]** Un nombre descriptivo para el origen de atributos de datos. Para [!DNL Adobe Target], los nombres de atributo no pueden incluir espacios. Si se pasa un atributo con un espacio [!DNL Target] , se omite. Otros caracteres que no se admiten son: `< , >, ', "`.

   * **[!UICONTROL Descripción:]** (Opcional) Descripción del origen de atributos de datos.

   * **[!UICONTROL ID de alias:]** Representa una fuente de datos de atributos del cliente, como un sistema CRM específico. Se utiliza un ID único en su código de origen de atributos del cliente. El ID debe ser único, en minúsculas y sin espacios. El valor que se introduce en el campo de ID de alias para un origen de atributos del cliente en la interfaz de usuario de Experience Cloud debe coincidir con los valores que se han pasado en la implementación (tanto mediante Dynamic Tag Management como JavaScript de SDK móvil).

      El ID de alias se corresponde con ciertas áreas en las que establece valores de ID de cliente adicionales. Por ejemplo:

      * **Administración dinámica de etiquetas:** El ID de alias se corresponde con *el valor Código* de integración en [!UICONTROL Configuración]del cliente, en [la herramienta Experience](https://marketing.adobe.com/resources/help/en_US/dtm/?f=macid) Cloud ID Service.

      * **API de visitante:** El ID de Alias se corresponde con los [ID de cliente](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_customer_ids) que puede asociar con cada visitante.

         Por ejemplo, *&quot;crm_ id&quot;* en:


         ```
         "crm_id":"67312378756723456"
         ```


      * **iOS:** El ID de alias corresponde a *&quot;idtype&quot;* en [visitorsyncidentifiers: identificadores](https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=methods).

         Por ejemplo:

         `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`


      * **Android:** el ID de alias se corresponde con *&quot; Idtype &quot;* en [syncidentifiers](https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=methods).

         Por ejemplo:

         `identifiers.put(`**`"idType"`**`, "idValue");`

         Consulte [Aprovechamiento de varias fuentes de datos](../attributes/crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB) para obtener información adicional sobre el procesamiento de datos con relación al campo ID de alias e ID de cliente.
   * **[!UICONTROL Carga de archivos:]** Puede arrastrar y soltar el archivo [!DNL .csv] de datos, o cargar los datos por medio de FTP. (El uso de FTP también requiere [!DNL .fin] un archivo). Consulte [Cargar los datos mediante FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B).


      >[!IMPORTANT]
      >
      >Existen requisitos de archivo de datos específicos. Consulte [Requisitos del archivo de datos](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) para obtener más información.


      Una vez cargado el archivo, los datos de la tabla se muestran en el encabezado de [!UICONTROL Carga de archivos] en esta página. Puede validar el esquema, configurar suscripciones o configurar el FTP.



      **Gráfico de carga de archivos**

      ![](assets/file_upload_attributes.png)

   * **[!UICONTROL ID de cliente único:]** Muestra cuántos ID únicos ha cargado en este origen de atributos.

   * **[!UICONTROL ID proporcionados por el cliente Alias en ID de visitante de Experience Cloud:]** Muestra cuántos ID se han creado alias en ID de visitante de Experience Cloud.

   * **[!UICONTROL ID proporcionados por el cliente con recuentos de alias elevados:]** Muestra el recuento de ID proporcionados por el cliente con 500 o más alias creados de ID de visitante de Experience Cloud. Es muy probable que estos identificadores proporcionados por el cliente no representen a individuos, sino algún tipo de inicio de sesión compartido. El sistema distribuye los atributos asociados a esos ID a los 500 ID de visitante de Experience Cloud con alias creados más recientemente, hasta que el recuento alcanza los 10 000. En este momento, el sistema invalida el ID proporcionado por el cliente y ya no puede distribuir los atributos asociados.










## Validar el esquema {#task_404AAC411B0D4E129AB3AC8B7BE85859}

El proceso de validación le permite asignar nombres para mostrar y descripciones en atributos cargados (cadenas, números enteros, números y demás). También puede eliminar los atributos actualizando el esquema.

Consulte [Validación del esquema](../attributes/validate-schema.md#concept_B3A01A15D04E4F998118E09B3A9B5043).

Para eliminar los atributos, consulte [(Opcional) Actualizar el esquema (elimina los atributos)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C).

## (Opcional) Actualice el esquema (eliminar atributos) {#task_6568898BB7C44A42ABFB86532B89063C}

Cómo eliminar atributos y reemplazar atributos en el esquema.


1. En [!UICONTROL la página Editar origen] de atributos del cliente, elimine la suscripción **[!UICONTROL de Target]** o **[!UICONTROL Analytics]** (en [!UICONTROL Configurar suscripciones]).
1. [Cargue un nuevo archivo de datos con campos actualizados](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8).

## Configurar suscripciones y activar el origen de atributos {#task_1ACA21198F0E46A897A320C244DFF6EA}

La configuración de una suscripción establece el flujo de datos entre Experience Cloud y las soluciones. Activar el origen de atributos permite el flujo de datos a las soluciones suscritas. Los registros de cliente que ha cargado concuerdan con las señales de ID entrantes de su sitio web o aplicación.

Consulte [Configurar suscripciones](../attributes/subscription.md#concept_ECA3C44FA6D540C89CC04BA3C49E63BF).

**Para activar un origen de atributos**

En el [! UICONTROL Crear nueva [o Editar] fuente de atributos del cliente], localice el encabezado [!UICONTROL Activar] y haga clic **[!UICONTROL en Activo]**.

![Resultado de paso](assets/activate_attribute_source.png)

## Utilizar los atributos del cliente en Adobe Analytics {#task_7EB0680540CE4B65911B2C779210915D}

Con los datos ahora disponibles en soluciones como
<keyword>
Adobe Analytics
</keyword>, puede crear informes sobre los datos, analizarlos y tomar la acción adecuada en sus campañas de marketing.

El ejemplo siguiente muestra un segmento de [!DNL Analytics] basado en los atributos cargados. El segmento muestra los suscriptores de Photoshop Lightroom cuyo producto más utilizado sea Photoshop.

![](assets/08_crs_usecase.png)

Cuando publica un segmento en Experience Cloud, pasa a estar disponible en las audiencias de Experience Cloud y en Audience Manager.

Consulte [Informe de atributos del cliente](https://marketing.adobe.com/resources/help/en_US/reference/?f=reports_customer_attributes) en la ayuda de Analytics para obtener más información.

## Utilizar los atributos de cliente en Adobe Target {#task_FC5F9D9059114027B62DB9B1C7D9E257}

En Target, puede seleccionar un atributo del cliente en la sección Perfil del visitante cuando cree una audiencia. Todos los atributos del cliente tendrán el prefijo [!DNL crs.] en la lista. Combine estos atributos según sea necesario con otros atributos de datos para crear audiencias.

![](assets/crs-add-attribute-target.png)

Consulte [Creación de una nueva audiencia](https://marketing.adobe.com/resources/help/en_US/target/target/?f=t_creating_a_new_audience) en la ayuda de Target.
