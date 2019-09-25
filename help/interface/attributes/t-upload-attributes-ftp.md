---
description: Si no carga mediante arrastrar y soltar, puede cargar datos de atributo del cliente mediante FTP a Experience Cloud.
keywords: atributos del cliente;servicios principales
seo-description: Si no carga mediante arrastrar y soltar, puede cargar datos de atributo del cliente mediante FTP a Experience Cloud.
seo-title: 'Opcional: cargar el archivo de datos a través de FTP'
solution: Experience Cloud
title: 'Opcional: cargar el archivo de datos a través de FTP'
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
translation-type: ht
source-git-commit: f8b48077d936e289d66c1a93a96fe9ebaa4f0136

---


# Opcional: cargar el archivo de datos a través de FTP

Si no carga mediante arrastrar y soltar, puede cargar datos de atributo del cliente mediante FTP a Experience Cloud.

Puede cargar los datos una vez que haya creado un origen de atributos del cliente y una cuenta FTP en Experience Cloud. Puede crear una cuenta FTP por cada origen de atributos. Los archivos cargados se almacenan en la carpeta raíz de dicha cuenta. Los datos deben tener el formato `.csv`, con un segundo archivo `.fin` para indicar que la carga ha finalizado.

>[!IMPORTANT]
>
>Compruebe los [Requisitos de archivos de datos para cargar atributos del cliente](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) antes de cargar el archivo.


Las cargas de archivos al sitio FTP de atributos del cliente pueden realizarse por FTP o SFTP.

* Necesita un cliente que admita las conexiones SFTP.
* Puede conectarse con SFTP si usa un nombre de usuario con o sin contraseña, como se describe [aquí](https://marketing.adobe.com/resources/help/es_ES/whitepapers/ftp/?f=ftp_sftp_cert_auth).



<!-- <p>Error states - get with Matt and Dave </p> 
<p>What are the most common reasons for doing this? Retail? Do a use case example, then show an AN example. </p> 
<p>You create one FTP per attribute source. Files go to the root folder in that account. The file type .fin is user-created. (For example, upload a .csv then a .fin of the same name, which signals you have completed the upload. https://wiki.corp.adobe.com/display/marketingcloud/Customer+Record+Services#CustomerRecordServices-FileFormats (leverage for doc). Possibly link from FTP File Reqs page to a help file about naming conventions. Need a new file type page for this. Similar content here: https://marketing.adobe.com/resources/help/en_US/reference/c_general_file_structure.html and here: https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/ftp_datasources.html </p> 
<p>Drag-n-drop and zip functionality for uploads - 1/21/2015. S/b less than 100 megs for drag and drop zip file. Fin file not required for drag/drop. </p> 
<p>Preview Data - shows the last upload (?) </p> 
<p>Need a link to the "instructions" on that information icon with the image. </p> 
<p>Workflow: Drag and drop, validate schema, configure subscription, save/activate. </p> -->
**Para cargar el archivo de datos a través de FTP**

1. [Creación de un origen de atributos del cliente y carga del archivo de datos...](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   Asegúrese de haber iniciado sesión en su sitio FTP en [!DNL ftp.adobe.com/<sftpname>].

1. Haga clic en **[!UICONTROL Acciones]** &gt; **[!UICONTROL Carga de archivo]**.

1. Cargue un archivo `.fin` para que su archivo se pueda recuperar.

   El tipo de archivo `.fin` lo crea el usuario e indica que la carga ha finalizado. Puede ser un archivo del bloc de notas en blanco. Por ejemplo, si carga [!DNL crs123.csv], también carga [!DNL crs123.fin].

   Si la carga se realiza correctamente, ambos archivos se mueven a una carpeta llamada **procesado**.


   Consulte  [Requisitos del archivo de datos para la carga de atributos de cliente](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) para obtener información importante acerca de los nombres y estructura de los archivos.
