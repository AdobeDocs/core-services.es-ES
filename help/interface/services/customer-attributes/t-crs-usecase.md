---
description: Cree un origen de atributos del cliente y cárguelo en Adobe Experience Cloud.
solution: Experience Cloud
title: Crear un atributo de cliente de Source y cargar el archivo de datos
uuid: 53dca789-9a91-4385-839d-c9d1aa36b9be
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 21ed7c35-aac9-46f1-a50c-84e7c075209c
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 50%

---

# Crear un origen de atributo del cliente y cargar el archivo de datos

Cree el origen de atributos del cliente (`.csv` y `.fin` archivos) y cargue los datos. Puede activar el origen de los datos cuando esté preparado. Una vez que esté listo el origen de los datos, comparta los datos del atributo con Analytics y Target.

## flujo de trabajo atributos del cliente {#concept_BF0AF88E9EF841219ED4D10754CD7154}

![flujo de trabajo de atributos del cliente](assets/crs.png)

>[!IMPORTANT]
>
>Para acceder a esta función, los usuarios deben estar asignados al perfil de producto atributos del cliente (atributos del cliente - Acceso predeterminado). Vaya a **[!UICONTROL Admin Console]** > **[!UICONTROL Productos]**. Si *atributos del cliente* se muestra como uno de los [!UICONTROL perfiles de producto], está listo para empezar. Los usuarios que se agregan al grupo atributos del cliente ven el menú [!UICONTROL atributos del cliente] a la izquierda de la interfaz de Experience Cloud.
>
>Para usar la característica Atributos del cliente, los usuarios también deben pertenecer a grupos de nivel de aplicación (Adobe Analytics o [!DNL Target]).

## Crear un archivo de datos {#create-data}

Estos datos son datos de clientes empresariales de su CRM. Los datos pueden incluir datos de suscriptores sobre productos, incluidos los ID de miembro, productos destacados, productos más utilizados, etc.

1. Crear un archivo de `.csv`.

   >[!NOTE]
   >
   >Cuando avance en este proceso, arrastre y suelte el archivo `.csv` para cargar el archivo. Sin embargo, si [lo sube a través de un FTP](t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B), también necesitará un archivo `.fin` con el mismo nombre que el `.csv`.

   Archivo de datos de cliente empresarial de muestra:

   ![Archivo de datos de cliente empresarial de muestra](assets/01_crs_usecase.png)

1. Antes de continuar, revise la información relevante en los [Requisitos del archivo de datos](crs-data-file.md) antes de cargar el archivo.
1. [Cree un origen de atributo de cliente y cargue los datos](t-crs-usecase.md), como se describe a continuación.

## Crear un origen de atributos y cargar el archivo de datos {#create-source}

Siga estos pasos en la página Crear nuevo origen de atributos del cliente en Experience Cloud.

>[!IMPORTANT]
>
>Al crear, modificar o eliminar orígenes de atributos del cliente, se produce un retraso de hasta una hora antes de que los identificadores empiecen a sincronizarse con la nueva fuente de datos. Debe tener derechos administrativos en Audience Manager para crear o modificar orígenes de atributos del cliente. Póngase en contacto con el Servicio de atención al cliente de Audience Manager o con su asesor para obtener derechos administrativos.

1. En [!DNL Experience Cloud], seleccione el icono ![menú](assets/menu-icon.png) del menú.
1. Seleccione **[!UICONTROL atributos del cliente]**.

   En la página [!UICONTROL atributos del cliente] es donde puede administrar y editar los orígenes de datos de atributos existentes.

   ![pantalla principal de atributos del cliente](assets/cust-attr.png)

1. Haga clic en **[!UICONTROL Nuevo]**.

   ![Resultado de los pasos](assets/04_crs_usecase.png)

1. En la página [!UICONTROL Crear atributo de cliente Source], configure los campos siguientes:

   * **[!UICONTROL Nombre:]** Un nombre descriptivo para el origen de atributos de datos. Para [!DNL Adobe Target], los nombres de atributos no pueden incluir espacios. Si pasa un atributo con un espacio, [!DNL Target] lo ignorará. Otros caracteres que no se admiten son: `< , >, ', "`.

   * **[!UICONTROL Descripción:]** (Opcional) Descripción del origen del atributo de datos.

   * **[!UICONTROL ID de alias:]** Representa una fuente de datos de atributos del cliente, como un sistema CRM específico, por ejemplo. [!UICONTROL ID de alias] es un ID único que se usa en su código de [!UICONTROL Source] de atributo del cliente. El ID debe ser único, en minúsculas y sin espacios. El valor introducido en el campo [!UICONTROL ID de alias] para un origen de atributos del cliente en Experience Cloud debe coincidir con los valores que se pasan desde la implementación (ya sea mediante la recopilación de datos de Platform o JavaScript de Mobile SDK).

     >[!IMPORTANT]
     >
     >Al eliminar una fuente de datos asociada con un ID de alias, este no se encuentra disponible, ya que el ID de alias se guarda en varios servicios y se utiliza para asignar perfiles entre ellos.

     El ID de alias corresponde a ciertas áreas en las que se configuran valores de ID de cliente adicionales. Por ejemplo:

      * **Etiquetas:** El ID de alias corresponde al valor de *Código de integración* en [!UICONTROL Configuración del cliente], en la herramienta [Servicio de Experience Cloud ID](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=es).

      * **API de visitante:** El ID de alias corresponde a los [ID de cliente](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=es) adicionales que puede asociar con cada visitante.

        Por ejemplo, *&quot;crm_id&quot;* en:

        ```
        "crm_id":"67312378756723456"
        ```

      * **iOS:** El ID de alias corresponde a *“idType”* en [visitorSyncIdentifiers:identifiers](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=es).

        Por ejemplo:

        `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`

      * **Android™:** El ID de alias corresponde a *“idType”* en [syncIdentifiers](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=es).

        Por ejemplo:

        `identifiers.put(`**`"idType"`**`, "idValue");`

        Consulte [Aprovechamiento de varias fuentes de datos](crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB) para obtener información adicional sobre el procesamiento de datos con respecto al campo ID de alias e ID de clientes.

   * **[!UICONTROL Código de área de nombres:]** Use este valor para identificar el origen de atributos del cliente al usar [IdentityMap](https://experienceleague.adobe.com/es/docs/experience-platform/web-sdk/identity/overview) como parte de una implementación de WebSDK de AEP.

## Cargar archivo {#upload}


1. Haga clic en Cargar archivo.

2. Arrastre y suelte el archivo de datos `.csv`, `.zip` o `.gzip` en la ventana de arrastrar y soltar.

>[!IMPORTANT]
>
>Existen requisitos específicos para los archivos de datos. Consulte los [Requisitos de archivos de datos](crs-data-file.md) para obtener más información.

Después de cargar el archivo, los datos de la tabla se muestran en el encabezado [!UICONTROL Carga de archivos] de esta página. Puede validar el esquema, configurar suscripciones o configurar el FTP.


![atributos](assets/file_upload_attributes.png)

* **[!UICONTROL ID único de cliente:]** Muestra cuántos ID únicos ha subido a este origen de atributos.

* **[!UICONTROL ID proporcionados por el cliente asociados a ID de visitante de Experience Cloud:]** Muestra cuántos ID se han asociado a los ID de visitante de Experience Cloud.

* **[!UICONTROL ID proporcionados por el cliente con muchos alias:]** Muestra el recuento de ID proporcionados por el cliente con 500 o más ID de visitante de Experience Cloud asociados. Es muy probable que estos ID proporcionados por el cliente no representen a individuos sino algún tipo de inicio de sesión compartido. El sistema distribuye los atributos asociados con estos ID a los 500 ID de visitante de Experience Cloud con alias creados más recientemente, hasta que el recuento alcanza los 10 000. En este momento, el sistema invalida el ID proporcionado por el cliente y ya no puede distribuir los atributos asociados. —>

## Validar el esquema {#validate-schema}

El proceso de validación le permite asignar nombres para mostrar y descripciones en atributos cargados (cadenas, números enteros, números y demás). También puede eliminar atributos actualizando el esquema.

Consulte [Validar el esquema](validate-schema.md).

Para eliminar atributos, consulte [(Opcional) Actualizar el esquema (elimina los atributos)](t-crs-usecase.md).

## (Opcional) Actualizar el esquema (elimina los atributos) {#task_6568898BB7C44A42ABFB86532B89063C}

Eliminar y reemplazar atributos en el esquema.

1. En la página [!UICONTROL Editar atributo de cliente Source], quite la suscripción de **[!UICONTROL Target]** o **[!UICONTROL Analytics]** (en [!UICONTROL Configurar suscripciones]).
1. [Cargue un nuevo archivo de datos con campos actualizados](t-crs-usecase.md).

## Configurar suscripciones y activar el origen de atributos {#task_1ACA21198F0E46A897A320C244DFF6EA}

La configuración de una suscripción configura el flujo de datos entre Experience Cloud y las aplicaciones. La activación del origen de atributos permite que los datos fluyan a las aplicaciones suscritas. Los registros de cliente que ha cargado coinciden con las señales de ID entrantes de su sitio web o aplicación.

Consulte [Configurar suscripciones](subscription.md).

**Para activar un origen de atributos**

En la página [!UICONTROL Crear nuevo o editar atributo de cliente Source], busque el encabezado [!UICONTROL Activar] y, a continuación, haga clic en **[!UICONTROL Activo]**.

![Resultado de los pasos](assets/activate_attribute_source.png)

## Uso de atributos del cliente en Adobe Analytics {#task_7EB0680540CE4B65911B2C779210915D}

Ahora que los datos están disponibles en aplicaciones como Adobe Analytics, puede informar sobre los datos, analizarlos y tomar las medidas adecuadas en sus campañas de marketing.

El ejemplo siguiente muestra un segmento de [!DNL Analytics] basado en los atributos cargados. El segmento muestra los suscriptores de [!DNL Photoshop Lightroom] cuyo producto más utilizado sea Photoshop.

![Segmento de Analytics basado en los atributos cargados](assets/08_crs_usecase.png)

Cuando publica un segmento en Experience Cloud, pasa a estar disponible en Audiencias de Experience Cloud y Audience Manager.

## Uso de atributos del cliente en Adobe Target {#task_FC5F9D9059114027B62DB9B1C7D9E257}

En [!DNL Target], puede seleccionar un atributo del cliente en la sección [!UICONTROL Perfil del visitante] cuando cree un público. Todos los atributos del cliente tienen el prefijo `crs.` en la lista. Combine estos atributos según sea necesario con otros atributos de datos para crear públicos.

![Utilizar los atributos de cliente en Adobe Target](assets/crs-add-attribute-target.png)

Consulte [Creación de un nuevo público](https://experienceleague.adobe.com/docs/target/using/audiences/create-audiences/audiences.html?lang=es) en la ayuda de [!DNL Target].
