---
description: El proceso de validación le permite asignar nombres para mostrar y descripciones en atributos cargados (cadenas, números enteros, números y demás). Se crea un esquema basado en esta configuración. El esquema se utiliza para validar todos los datos futuros cargados a esta fuente de datos. Este proceso de asignación no altera los datos originales.
keywords: customer attributes;core services
seo-description: El proceso de validación le permite asignar nombres para mostrar y descripciones en atributos cargados (cadenas, números enteros, números y demás). Se crea un esquema basado en esta configuración. El esquema se utiliza para validar todos los datos futuros cargados a esta fuente de datos. Este proceso de asignación no altera los datos originales.
seo-title: Validar el esquema
solution: Experience Cloud
title: Validar el esquema
uuid: 163a4dbe-d60b-4089-8ff8-65f7461fbdf7
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Validar el esquema

El proceso de validación le permite asignar nombres para mostrar y descripciones en atributos cargados (cadenas, números enteros, números y demás). Se crea un esquema basado en esta configuración. El esquema se utiliza para validar todos los datos futuros cargados a esta fuente de datos. Este proceso de asignación no altera los datos originales.

>[!NOTE]
>
>Actualizar el esquema tras la validación elimina los atributos del cliente. Consulte [Actualizar el esquema (también elimina los atributos)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C).

**[!UICONTROL Origen]** de atributos del cliente > **[!UICONTROL Crear nuevo origen]** de atributos del cliente > **[!UICONTROL Vista/Editar Esquema]**

![](assets/view_edit_schema.png)

En la página [!UICONTROL Validar esquema], cada fila del esquema representa una columna del archivo CSV cargado.

![](assets/06_crs_usecase.png)

* **[!UICONTROL Añadir datos:]** Le permite cargar datos de atributo nuevos a esta fuente de datos.

* **[!UICONTROL Ver/Editar Esquema:]** Asigna nombres para mostrar en los datos de atributo, como se describe en el siguiente paso.

* **[!UICONTROL Configuración de FTP:]**[ Cargue los datos a través de un FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B).

* **[!UICONTROL Búsqueda de ID:]** Introduzca un ID de cliente (CID) de su `.csv` para buscar información sobre ese ID en Experience Cloud. Esta función es útil para resolver problemas sobre por qué no se muestran los datos de atributo de un visitante:

   * **[!UICONTROL ECID (Experience Cloud ID):]** Muestra si está utilizando el servicio Experience Cloud ID más reciente. Si está en el servicio MCID pero no hay ningún ID en la lista, Experience Cloud no ha recibido un alias para ese CID. Lo cual significa que el visitante no ha iniciado sesión o su implementación no ha pasado dicha ID.

   * **[!UICONTROL CID (ID de cliente):]** Los atributos asociados con este CID. Si utiliza una propiedad o eVar para cargar CID (AVID) y ve que se muestran atributos pero no hay AVID, esto indica que el visitante no ha iniciado sesión en su sitio.

   * **[!UICONTROL AVID (Analytics visitor ID):]** Muestra si utiliza una prop o una eVar para cargar los CID. Si estos ID se pasan a Experience Cloud, aquí se mostrarán todos los ID de visitante asociados al CID que ha introducido.

También puede cargar los datos mediante FTP una vez que haya creado un origen de atributos del cliente y una cuenta FTP en Experience Cloud. Puede crear una cuenta FTP por cada origen de atributos. Los archivos cargados se almacenan en la carpeta raíz de esa cuenta. Los datos deben tener el formato .csv, con un segundo archivo .fin para indicar que la carga se ha completado

Los nombres que aplique a las cadenas, números enteros y números se utilizan para crear métricas de [!DNL Analytics] Consulte Informe [Atributos](https://docs.adobe.com/help/en/analytics/components/variables/dimensions-reports/reports-customer-attributes.html) del cliente en la [!DNL Analytics] ayuda para obtener más información.

* **[!UICONTROL Atributo:]** Lectura de datos de atributo desde un archivo cargado `.csv`.

* **[!UICONTROL Tipo:]** El tipo de datos, como por ejemplo:

   * **Cadena:** Secuencia de caracteres.

   * **Integradores:** Números enteros.

   * **Números:** Puede tener hasta dos decimales.

* **[!UICONTROL Mostrar nombre:]** Un nombre descriptivo para el atributo. Por ejemplo, puede cambiar un atributo de *Edad del cliente* a *Cliente desde*.

* **[!UICONTROL Descripción:]** Una descripción del atributo.
