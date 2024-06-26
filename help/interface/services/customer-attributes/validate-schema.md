---
description: Obtenga información sobre cómo validar el esquema de atributos del cliente en Adobe Experience Cloud.
solution: Experience Cloud
title: Validación del esquema de atributos del cliente
uuid: 163a4dbe-d60b-4089-8ff8-65f7461fbdf7
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 84%

---

# Validar el esquema

El proceso de validación le permite asignar nombres para mostrar y descripciones en atributos cargados (cadenas, números enteros, números y demás). Se crea un esquema basado en esta configuración. El esquema se utiliza para validar todos los datos futuros cargados a esta fuente de datos. El proceso de asignación no altera los datos originales.

>[!NOTE]
>
>Actualizar el esquema tras la validación elimina los Atributos del cliente. Consulte [Actualizar el esquema (también elimina los atributos)](t-crs-usecase.md).

**[!UICONTROL Origen de atributos del cliente]** > **[!UICONTROL Crear un nuevo origen de atributos del cliente]** > **[!UICONTROL Ver/Editar Esquema]**

![Edición de un esquema](assets/view_edit_schema.png)

En la página [!UICONTROL Validación de un esquema], cada fila del esquema representa una columna del archivo CSV cargado.

![Validación de una página de esquema en Experience Cloud](assets/06_crs_usecase.png)

* **[!UICONTROL Añadir datos:]** Le permite cargar datos de atributo nuevos a esta fuente de datos.

* **[!UICONTROL Ver/Editar Esquema:]** Asigna nombres para mostrar en los datos de atributo, como se describe en el siguiente paso.

* **[!UICONTROL Configuración de FTP:]** [Cargue los datos a través de un FTP](t-upload-attributes-ftp.md).

* **[!UICONTROL Búsqueda de ID:]** Introduzca un ID de cliente (CID) de su `.csv` para buscar información sobre ese ID en Experience Cloud. Esta función es útil para resolver problemas sobre por qué no se muestran los datos de atributo de un visitante:

   * **[!UICONTROL ECID (Experience Cloud ID):]** Muestra si utiliza el servicio de Experience Cloud ID más reciente. Si está en el servicio de ECID pero no hay ningún ID en la lista, Experience Cloud no ha recibido un alias para ese CID. Lo cual significa que el visitante no ha iniciado sesión o su implementación no ha pasado dicha ID.

   * **[!UICONTROL CID (ID de cliente):]** Los atributos asociados con este CID. Si utiliza una propiedad o eVar para cargar CID (AVID) y ve que se muestran atributos pero no hay AVID, esto indica que el visitante no ha iniciado sesión en su sitio.

   * **[!UICONTROL AVID (Analytics visitor ID):]** Muestra si utiliza una prop o una eVar para cargar los CID. Si estos ID se pasan al Experience Cloud, aquí se mostrarán todos los ID de visitante asociados al CID que ha introducido.

También puede cargar los datos mediante FTP una vez que haya creado un origen de atributos del cliente y una cuenta FTP en Experience Cloud. Puede crear una cuenta FTP por cada origen de atributos. Los archivos cargados se almacenan en la carpeta raíz de esa cuenta. Los datos deben tener el formato `.csv`, con un segundo archivo `.fin` para indicar que la carga ha finalizado.

Los nombres que aplique a las cadenas, números enteros y números se utilizan para crear métricas de [!DNL Analytics].

* **[!UICONTROL Atributo:]** Lectura de datos de atributo desde un archivo cargado `.csv`.

* **[!UICONTROL Tipo:]** El tipo de datos, como por ejemplo:

   * **Cadena:** Secuencia de caracteres.

   * **Enteros:** Números enteros.

   * **Números:** Pueden tener hasta dos decimales.

* **[!UICONTROL Mostrar nombre:]** Un nombre descriptivo para el atributo. Por ejemplo, puede cambiar un atributo de *Edad del cliente* a *Cliente desde*.

* **[!UICONTROL Descripción:]** Una descripción del atributo.
