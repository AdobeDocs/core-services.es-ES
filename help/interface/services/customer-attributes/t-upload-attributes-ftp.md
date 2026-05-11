---
description: Aprenda a cargar datos de atributos del cliente a CX Enterprise a través de FTP.
solution: Experience Cloud
title: Cargar archivo de datos de atributos del cliente mediante FTP
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
TQID: 'https://experienceleague.adobe.com/VkV54Ix1ryiVxbDsPejsS1-0EVLrZC9ZPqGiG3aQ-94'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id:id:
role_v2: id:
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f01d85af42b8f2c27dbada8f73546bc6fe4bf710
workflow-type: tm+mt
source-wordcount: 379
ht-degree: 53%

---

# Cargar el archivo de datos mediante FTP (opcional)

Si no carga mediante arrastrar y soltar, puede cargar datos de atributos del cliente mediante FTP a CX Enterprise.

Puede cargar los datos una vez que haya creado un origen de atributos del cliente y una cuenta FTP en CX Enterprise. Puede crear una cuenta FTP por cada origen de atributos. Los archivos cargados se almacenan en la carpeta raíz de esa cuenta. Los datos deben tener el formato `.csv`, con un segundo archivo `.fin` para indicar que la carga ha finalizado.

>[!IMPORTANT]
>
>Revise [los archivos y orígenes de datos de atributos del cliente](crs-data-file.md) antes de cargar el archivo.

Las cargas de archivos al sitio FTP de atributos del cliente se pueden realizar mediante FTP o SFTP:

* Necesita un cliente que admita conexiones SFTP.
* Puede conectarse con SFTP con un nombre de usuario o una contraseña o sin contraseña, como se describe [aquí](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html).

**Para cargar el archivo de datos a través de FTP**

1. [Creación de un origen de atributos del cliente y carga del archivo de datos...](t-crs-usecase.md).

   Asegúrese de haber iniciado sesión en su sitio FTP en `ftp.adobe.com/<sftpname>`.

1. Haga clic en **[!UICONTROL Actions]** > **[!UICONTROL File Upload]**.

1. Cargue un archivo `.fin` para que su archivo se pueda recuperar.

   El tipo de archivo `.fin` lo crea el usuario e indica que la carga ha finalizado. Puede ser un archivo del bloc de notas en blanco. Por ejemplo, si carga `crs123.csv`, también carga `crs123.fin`.

   Si la carga se realiza correctamente, ambos archivos se mueven a una carpeta denominada **Procesados**.

   Consulte [Archivos y orígenes de datos de atributos del cliente](crs-data-file.md) para obtener información importante acerca de los nombres y estructura de los archivos.

## Configuración de una cuenta de FTP

Configure una cuenta FTP por cada origen de atributos.

En la página [!UICONTROL File Upload and Schema Validation], haga clic en **[!UICONTROL FTP Setup]**.

![Edición de un esquema](assets/ftp-account.png)

Los archivos cargados se almacenan en la carpeta raíz de esa cuenta. Los datos deben tener el formato `.csv`, con un segundo archivo `.fin` para indicar que la carga ha finalizado.

Los nombres que aplique a las cadenas, números enteros y números se utilizan para crear métricas de [!DNL Analytics].

* **[!UICONTROL attribute:]** datos de atributo leídos del archivo subido `.csv`.

* **[!UICONTROL Type:]** El tipo de datos, como:

   * **Cadena:** Secuencia de caracteres.

   * **Enteros:** Números enteros.

   * **Números:** Pueden tener hasta dos decimales.

* **[!UICONTROL Display Name:]** Un nombre descriptivo para el atributo. Por ejemplo, puede cambiar un atributo *customer age* a *customer Since*.

* **[!UICONTROL Description:]** Una descripción del atributo.

