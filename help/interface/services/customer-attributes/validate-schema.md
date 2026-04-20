---
description: Obtenga información sobre cómo validar el esquema  [!DNL Customer Attributes] en Adobe CX Enterprise.
solution: Experience Cloud
title: Validar el  [!DNL Customer Attributes] esquema
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
TQID: https://experienceleague.adobe.com/J-AaDn4HtD1bS-VCPn2XiPLVBbTnYyl5o1NpJ9HFj1g
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 308
ht-degree: 43%

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

   ![Editar página de esquema en CX Enterprise](assets/schema-edit.png)

**Acciones**

* **[!UICONTROL Add Data:]** Cargar nuevos datos de atributo en este origen de datos.

* **[!UICONTROL View/Edit Schema:]**: asigne nombres para mostrar a los datos de atributo, tal como se describe en el paso siguiente.

* **[!UICONTROL FTP Setup:]** Cree su cuenta de FTP para [cargar sus datos a través de FTP](t-upload-attributes-ftp.md) (opcional).

* **[!UICONTROL ID Lookup:]** Escriba un ID de cliente (CID) de su `.csv` para buscar información de CX Enterprise sobre el ID. Esta función es útil para resolver problemas sobre por qué no se muestran los datos de atributo de un visitante:

   * **[!UICONTROL ECID (CX Enterprise ID):]** muestra si está usando el servicio de CX Enterprise ID más reciente. Si está en el servicio de ECID pero no hay ningún ID en la lista, CX Enterprise no ha recibido un alias para ese CID. Lo cual significa que el visitante no ha iniciado sesión o su implementación no ha pasado dicha ID.

   * **[!UICONTROL CID (customer ID):]** Los atributos asociados con este CID. Si utiliza una propiedad o eVar para cargar CID (AVID) y ve que se muestran atributos pero no hay AVID, esto indica que el visitante no ha iniciado sesión en su sitio.

   * **[!UICONTROL AVID (Analytics visitor ID):]** muestra si usa una propiedad o un eVar para cargar CID. Si estos ID se pasan a CX Enterprise, aquí se mostrarán todos los ID de visitante asociados al CID que ha introducido.
