---
description: El proceso de validación le permite asignar nombres para mostrar y descripciones en atributos cargados (cadenas, números enteros, números y demás). Se ha creado un esquema basado en estos ajustes. El esquema se utiliza para validar todos los datos futuros cargados a este origen de datos. Este proceso de asignación no altera los datos originales.
keywords: atributos del cliente; servicios principales
seo-description: El proceso de validación le permite asignar nombres para mostrar y descripciones en atributos cargados (cadenas, números enteros, números y demás). Se ha creado un esquema basado en estos ajustes. El esquema se utiliza para validar todos los datos futuros cargados a este origen de datos. Este proceso de asignación no altera los datos originales.
seo-title: Validar el esquema
solution: Experience Cloud
title: Validar el esquema
uuid: 163 a 4 dbe-d 60 b -4089-8 ff 8-65 f 7461 fbdf 7
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# Validar el esquema

El proceso de validación le permite asignar nombres para mostrar y descripciones en atributos cargados (cadenas, números enteros, números y demás). Se ha creado un esquema basado en estos ajustes. El esquema se utiliza para validar todos los datos futuros cargados a este origen de datos. Este proceso de asignación no altera los datos originales.


>[!NOTE]
>
>Actualizar el esquema después de la validación elimina los atributos del cliente. Consulte [Actualizar el esquema (también elimina atributos)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C).


**[!UICONTROL Origen de atributos del cliente]** &gt; **[!UICONTROL Crear nuevo origen de atributos de cliente]** &gt; **[!UICONTROL Ver/Editar esquema]**

![](assets/view_edit_schema.png)

En la página [!UICONTROL Validar esquema], cada fila del esquema representa una columna del archivo CSV cargado.

![](assets/06_crs_usecase.png)

* **[!UICONTROL Agregar datos:]** Cargue nuevos datos de atributo en esta fuente de datos.

* **[!UICONTROL Ver/Editar esquema:]** Asigne nombres para mostrar a los datos de atributos, tal como se describe en el paso siguiente.

* **[!UICONTROL Configuración de FTP:]**[Cargue los datos mediante FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B).

* **[!UICONTROL Búsqueda de ID:]** Introduzca un ID de cliente (CID) desde el [!DNL .csv] para buscar información de Experience Cloud para el ID. Esta función es útil para resolver problemas sobre por qué no se muestran los datos de atributo de un visitante:

   * **[!UICONTROL MCID (Experience Cloud ID):]** Muestra si está utilizando el servicio Experience Cloud ID más reciente. Si se encuentra en el servicio MCID pero no hay ningún ID en la lista, Experience Cloud no ha recibido un alias para dicho CID. Lo cual significa que el visitante no ha iniciado sesión o su implementación no ha pasado dicha ID.

   * **[!UICONTROL CID (ID de cliente):]** Atributos asociados con este CID. Si utiliza una propiedad o eVar para cargar CID (AVID) y ve que se muestran atributos pero no hay AVID, esto indica que el visitante no ha iniciado sesión en su sitio.

   * **[!UICONTROL AVID (ID de visitante de Analytics):]** Se muestra si utiliza una propiedad o evar para cargar CID. Si estos ID se pasan a Experience Cloud, cualquier ID de visitante asociado con el CID que ha introducido se muestra aquí.






También puede cargar los datos mediante FTP una vez haya creado un origen de atributos del cliente y una cuenta FTP en Experience Cloud. Puede crear una cuenta FTP por cada origen de atributos. Los archivos cargados se almacenan en la carpeta raíz de dicha cuenta. Los datos deben tener el formato .csv, con un segundo archivo .fin para indicar que la carga ha finalizado

Los nombres que se aplican a las cadenas, enteros y números se utilizan para crear [!DNL Analytics] métricas. Consulte [Informe de atributos del cliente](https://marketing.adobe.com/resources/help/en_US/reference/?f=reports_customer_attributes) en la ayuda de para obtener más información.[!DNL Analytics]

* **[!UICONTROL Atributo:]** Lectura de datos de atributo desde [!DNL .csv] el archivo cargado.

* **[!UICONTROL Tipo:]** El tipo de datos, como:

   * **Cadena:** una secuencia de caracteres.

   * **Enteros**: números enteros.

   * **Números**: puede tener hasta dos cifras decimales.




* **[!UICONTROL Nombre para mostrar:]** Un nombre descriptivo para el atributo. Por ejemplo, puede cambiar una edad *de cliente de atributo* a *Cliente desde*.

* **[!UICONTROL Descripción:]** Una descripción descriptiva del atributo.



