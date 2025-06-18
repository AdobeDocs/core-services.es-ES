---
description: Obtenga información sobre cómo cargar datos de atributos del cliente a Experience Cloud a través de FTP.
solution: Experience Cloud
title: Carga del archivo de datos de atributos del cliente mediante FTP
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 71%

---

# Opcional: cargar el archivo de datos a través de FTP

Si no carga mediante arrastrar y soltar, puede cargar datos de atributos del cliente mediante FTP a Experience Cloud.

Puede cargar los datos una vez que haya creado un origen de atributos del cliente y una cuenta FTP en Experience Cloud. Puede crear una cuenta FTP por cada origen de atributos. Los archivos cargados se almacenan en la carpeta raíz de esa cuenta. Los datos deben tener el formato `.csv`, con un segundo archivo `.fin` para indicar que la carga ha finalizado.

>[!IMPORTANT]
>
>Compruebe los [Requisitos de archivos de datos para cargar atributos del cliente](crs-data-file.md) antes de cargar el archivo.

Las cargas de archivos al sitio FTP de atributos del cliente se pueden realizar mediante FTP o SFTP:

* Necesita un cliente que admita conexiones SFTP.
* Puede conectarse con SFTP con un nombre de usuario o una contraseña o sin contraseña, como se describe [aquí](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=es).

**Para cargar el archivo de datos a través de FTP**

1. [Creación de un origen de atributos del cliente y carga del archivo de datos...](t-crs-usecase.md).

   Asegúrese de haber iniciado sesión en su sitio FTP en `ftp.adobe.com/<sftpname>`.

1. Haga clic en **[!UICONTROL Acciones]** > **[!UICONTROL Carga de archivo]**.

1. Cargue un archivo `.fin` para que su archivo se pueda recuperar.

   El tipo de archivo `.fin` lo crea el usuario e indica que la carga ha finalizado. Puede ser un archivo del bloc de notas en blanco. Por ejemplo, si carga `crs123.csv`, también carga `crs123.fin`.

   Si la carga se realiza correctamente, ambos archivos se mueven a una carpeta denominada **Procesados**.

   Consulte [Requisitos del archivo de datos para la carga de atributos de cliente](crs-data-file.md) para obtener información importante acerca de los nombres y estructura de los archivos.
