---
description: Aprenda a cargar datos de atributos del cliente a Experience Cloud a través de FTP.
solution: Experience Cloud
title: Carga del archivo de datos de atributos del cliente mediante FTP
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: eb2ad8a8255915be47b6002a78cc810b522170d2
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 100%

---

# Opcional: cargar el archivo de datos a través de FTP

Si no carga mediante arrastrar y soltar, puede cargar datos de atributo del cliente mediante FTP a Experience Cloud.

Puede cargar los datos una vez que haya creado un origen de atributos del cliente y una cuenta FTP en Experience Cloud. Puede crear una cuenta FTP por cada origen de atributos. Los archivos cargados se almacenan en la carpeta raíz de esa cuenta. Los datos deben tener el formato `.csv`, con un segundo archivo `.fin` para indicar que la carga ha finalizado.

>[!IMPORTANT]
>
>Compruebe los [Requisitos de archivos de datos para cargar los Atributos del cliente](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) antes de cargar el archivo.

Las cargas de archivos al sitio FTP de Atributos del cliente se pueden realizar mediante FTP o SFTP:

* Necesita un cliente que admita conexiones SFTP.
* Puede conectarse con SFTP con un nombre de usuario o una contraseña o sin contraseña, como se describe [aquí](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=es).

**Para cargar el archivo de datos a través de FTP**

1. [Crear un origen de Atributo del cliente y cargar el archivo de datos...](t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   Asegúrese de haber iniciado sesión en su sitio FTP en `ftp.adobe.com/<sftpname>`.

1. Seleccione **[!UICONTROL Acciones]** > **[!UICONTROL Carga de archivo]**.

1. Cargue un archivo `.fin` para que su archivo se pueda recuperar.

   El tipo de archivo `.fin` lo crea el usuario e indica que la carga ha finalizado. Puede ser un archivo del bloc de notas en blanco. Por ejemplo, si carga [!DNL crs123.csv], también carga [!DNL crs123.fin].

   Si la carga se realiza correctamente, ambos archivos se mueven a una carpeta denominada **Procesados**.

   Consulte [Requisitos del archivo de datos para la carga de Atributos del cliente](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) para obtener información importante acerca de los nombres y la estructura de los archivos.
