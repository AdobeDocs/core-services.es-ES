---
description: Obtenga información sobre cómo validar el esquema  [!DNL Customer Attributes] en Adobe Experience Cloud.
solution: Experience Cloud
title: Validar el  [!DNL Customer Attributes] esquema
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
source-git-commit: e63dd988abba199049da2b3620eed9ebf51043d1
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 37%

---

# Validar el esquema

El proceso de validación le permite asignar nombres para mostrar y descripciones en atributos cargados (cadenas, números enteros, números y demás).

Se crea un esquema basado en esta configuración. El esquema se utiliza para validar todos los datos futuros cargados a esta fuente de datos. El proceso de asignación no altera los datos originales.

>[!NOTE]
>
>Actualizar el esquema tras la validación elimina los atributos del cliente. Consulte [Actualizar el esquema (también elimina los atributos)](t-crs-usecase.md).

**Para validar el esquema**

1. En [!DNL Customer Attributes], haga clic en el origen del atributo que desea editar.

1. En **[!UICONTROL Edit Customer Attribute Source]**, haga clic en **[!UICONTROL File Upload]**.

1. En la página [!UICONTROL File Upload and Schema Validation], haga clic en **[!UICONTROL Actions]** > **[!UICONTROL View/Edit Schema]**

   ![Edición de un esquema](assets/actions.png)

   En la página [!UICONTROL Edit Schema], cada fila del esquema representa una columna del archivo CSV cargado.

   ![Editar página de esquema en Experience Cloud](assets/schema-edit.png)

**Acciones**

* **[!UICONTROL Add Data:]** Cargar nuevos datos de atributo en este origen de datos.

* **[!UICONTROL View/Edit Schema:]**: asigne nombres para mostrar a los datos de atributo, tal como se describe en el paso siguiente.

* **[!UICONTROL FTP Setup:]** Cree su cuenta de FTP para [cargar sus datos a través de FTP](t-upload-attributes-ftp.md) (opcional).

* **[!UICONTROL ID Lookup:]** Escriba un ID de cliente (CID) de su `.csv` para buscar información de Experience Cloud sobre el ID. Esta función es útil para resolver problemas sobre por qué no se muestran los datos de atributo de un visitante:

   * **[!UICONTROL ECID (Experience Cloud ID):]** muestra si está usando el servicio de Experience Cloud ID más reciente. Si está en el servicio de ECID pero no hay ningún ID en la lista, Experience Cloud no ha recibido un alias para ese CID. Lo cual significa que el visitante no ha iniciado sesión o su implementación no ha pasado dicha ID.

   * **[!UICONTROL CID (customer ID):]** Los atributos asociados con este CID. Si utiliza una propiedad o eVar para cargar CID (AVID) y ve que se muestran atributos pero no hay AVID, esto indica que el visitante no ha iniciado sesión en su sitio.

   * **[!UICONTROL AVID (Analytics visitor ID):]** muestra si usa una propiedad o un eVar para cargar CID. Si estos ID se pasan a Experience Cloud, aquí se mostrarán todos los ID de visitante asociados al CID que ha introducido.
