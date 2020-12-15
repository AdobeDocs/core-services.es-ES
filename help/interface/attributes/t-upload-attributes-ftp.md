---
description: Si no carga mediante arrastrar y soltar, puede cargar datos de atributo del cliente mediante FTP a Experience Cloud.
keywords: Customer Attributes;core services
solution: Experience Cloud
title: 'Cargar el archivo de datos de atributos del cliente mediante FTP '
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
translation-type: tm+mt
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 97%

---


# Opcional: cargar el archivo de datos a través de FTP

Si no carga mediante arrastrar y soltar, puede cargar datos de atributo del cliente mediante FTP a Experience Cloud.

Puede cargar los datos una vez que haya creado un origen de atributos del cliente y una cuenta FTP en Experience Cloud. Puede crear una cuenta FTP por cada origen de atributos. Los archivos cargados se almacenan en la carpeta raíz de esa cuenta. Los datos deben tener el formato `.csv`, con un segundo archivo `.fin` para indicar que la carga ha finalizado.

>[!IMPORTANT]
>
>Compruebe los [Requisitos de archivos de datos para cargar los Atributos del cliente](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) antes de cargar el archivo.

Las cargas de archivos al sitio FTP de Atributos del cliente se pueden realizar mediante FTP o SFTP:

* Necesita un cliente que admita conexiones SFTP.
* Puede conectarse con SFTP con un nombre de usuario o una contraseña o sin contraseña, como se describe [aquí](https://docs.adobe.com/help/es-ES/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html).

**Para cargar el archivo de datos a través de FTP**

1. [Creación de un origen de atributos del cliente y carga del archivo de datos...](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   Asegúrese de haber iniciado sesión en su sitio FTP en `ftp.adobe.com/<sftpname>`.

1. Haga clic en **[!UICONTROL Acciones]** > **[!UICONTROL Carga de archivo]**.

1. Cargue un archivo `.fin` para que su archivo se pueda recuperar.

   El tipo de archivo `.fin` lo crea el usuario e indica que la carga ha finalizado. Puede ser un archivo del bloc de notas en blanco. Por ejemplo, si carga [!DNL crs123.csv], también carga [!DNL crs123.fin].

   Si la carga se realiza correctamente, ambos archivos se mueven a una carpeta denominada **Procesados**.

   Consulte [Requisitos del archivo de datos para la carga de Atributos del cliente](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) para obtener información importante acerca de los nombres y la estructura de los archivos.
