---
description: Obtenga información sobre cómo validar el esquema  [!DNL Customer Attributes] en Adobe Experience Cloud.
solution: Experience Cloud
title: Validar el  [!DNL Customer Attributes] esquema
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
source-git-commit: d2244e249c7af27bc1b4fc7bfe628bc25b37f4d4
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 49%

---

# Validar el esquema

El proceso de validación le permite asignar nombres para mostrar y descripciones en atributos cargados (cadenas, números enteros, números y demás).

Se crea un esquema basado en esta configuración. El esquema se utiliza para validar todos los datos futuros cargados a esta fuente de datos. El proceso de asignación no altera los datos originales.

>[!NOTE]
>
>Actualizar el esquema tras la validación elimina los atributos del cliente. Consulte [Actualizar el esquema (también elimina los atributos)](t-crs-usecase.md).

**Para validar el esquema**

1. En [!DNL Customer Attributes], haga clic en el origen del atributo que desea editar.

1. En **[!UICONTROL Editar atributo del cliente Source]**, haga clic en **[!UICONTROL Cargar archivo]**.

1. En la página [!UICONTROL Carga de archivos y validación de esquemas], haga clic en **[!UICONTROL Acciones]** > **[!UICONTROL Ver o editar esquema]**

   ![Edición de un esquema](assets/actions.png)

   En la página [!UICONTROL Editar esquema], cada fila del esquema representa una columna del archivo CSV cargado.

   ![Editar página de esquema en Experience Cloud](assets/schema-edit.png)

**Acciones**

* **[!UICONTROL Añadir datos:]** Le permite cargar datos de atributo nuevos a esta fuente de datos.

* **[!UICONTROL Ver/Editar Esquema:]** Asigna nombres para mostrar en los datos de atributo, como se describe en el siguiente paso.

* **[!UICONTROL Configuración de FTP:]** Cree su cuenta de FTP para [cargar los datos a través de FTP](t-upload-attributes-ftp.md) (opcional).

* **[!UICONTROL Búsqueda de ID:]** Escriba un ID de cliente (CID) de su `.csv` para buscar información de Experience Cloud sobre el ID. Esta función es útil para resolver problemas sobre por qué no se muestran los datos de atributo de un visitante:

   * **[!UICONTROL ECID (Experience Cloud ID):]** Muestra si utiliza el servicio de Experience Cloud ID más reciente. Si está en el servicio de ECID pero no hay ningún ID en la lista, Experience Cloud no ha recibido un alias para ese CID. Lo cual significa que el visitante no ha iniciado sesión o su implementación no ha pasado dicha ID.

   * **[!UICONTROL CID (ID de cliente):]** Los atributos asociados con este CID. Si utiliza una propiedad o eVar para cargar CID (AVID) y ve que se muestran atributos pero no hay AVID, esto indica que el visitante no ha iniciado sesión en su sitio.

   * **[!UICONTROL AVID (Analytics visitor ID):]** Muestra si utiliza una prop o una eVar para cargar los CID. Si estos ID se pasan a Experience Cloud, aquí se mostrarán todos los ID de visitante asociados al CID que ha introducido.
