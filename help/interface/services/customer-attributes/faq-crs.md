---
description: Obtenga respuestas a las preguntas más frecuentes sobre  [!DNL Customer Attributes] en Adobe CX Enterprise, para Adobe Analytics y Adobe Target.
solution: Experience Cloud
title: Preguntas frecuentes sobre  [!DNL Customer Attributes]
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
TQID: 'https://experienceleague.adobe.com/MnXP6RE4S42KlbcI023sMsSs97vTD5KL5DiZq1biXHc'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4bid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id:id:
role_v2: id:
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c4147b6e-073b-4d3c-9ab1-d60f2f4434efid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: f01d85af42b8f2c27dbada8f73546bc6fe4bf710
workflow-type: tm+mt
source-wordcount: 1058
ht-degree: 60%

---

# Preguntas frecuentes sobre [!DNL Customer Attributes]

Preguntas frecuentes y prácticas recomendadas sobre [!DNL Customer Attributes] en Adobe Analytics y Adobe Target.

## Prácticas recomendadas y limitaciones

Directrices y limitaciones al usar [!DNL Customer Attributes].

| Problema | Descripción |
| --- | --- |
| Limitaciones de [!DNL Customer Attributes] [suscripción](subscription.md) | Cuando actualice a Analytics Premium, no podrá disponer de los atributos hasta haber transcurrido 24 horas. Durante esta demora, podría aparecer un error [!UICONTROL attribute Subscription Max]. |
| Varios inicios de sesión en el mismo dispositivo | Cuando se usa [!DNL Customer Attributes] para cargar perfiles de clientes en una fuente de datos, Adobe recomienda que no se compartan dispositivos (es decir, el mismo CX Enterprise ID). El Enterprise ID de CX (ECID) persiste en el dispositivo. Compartir dispositivos puede hacer que el ECID vincule varios usuarios al mismo ECID, lo que provoca resultados inesperados en [!DNL Target]. **Nota:** Para dispositivos móviles, el ECID es permanente después de instalar la aplicación móvil. Vuelva a instalar la aplicación para generar un nuevo ECID. Para su uso en la web, se genera un nuevo ECID después de borrar la cookie del explorador. |
| Límite diario de carga de frecuencia | Adobe recomienda actualizar los [!DNL Customer Attributes] solo una vez al día. Debe esperar al menos 24 horas para cargar otro archivo de datos de perfil del cliente para el mismo conjunto de perfiles. |
| ID de Analytics personalizado (`s.visitorID`) | Configurar un ID de cliente con `s.visitorID` es un método para identificar a los usuarios en Adobe Analytics. Sin embargo, las integraciones en las que se exportan o importan datos de [!DNL Analytics] mediante el servicio de ID no funcionan cuando se identifica un visitante mediante `s.visitorID.`<br>Esto incluye, entre otras cosas, audiencias compartidas, [!DNL Analytics] para Adobe Target (A4T) y [!DNL Customer Attributes].<br>Estas integraciones no admiten la configuración de un ID de Analytics personalizado. |
| Limitaciones de longitud de caracteres en [!DNL Analytics] | Al crear una [!DNL Analytics] [suscripción](subscription.md), las longitudes de campo de los archivos cargados se truncan a 255. |

{style="table-layout:auto"}

## Preguntas frecuentes sobre [!DNL Customer Attributes]

| Pregunta | Respuesta |
| --- | --- |
| ¿Puedo recibir notificaciones sobre el estado de carga de [!DNL Customer Attributes]? | Sí. |
| ¿Qué debo hacer para empezar a usar los [!DNL Customer Attributes]? | <ol><li>Aprovisione sus soluciones. Si es cliente de Adobe Analytics, Adobe le proporcionará [!DNL Customer Attributes]. Si solo usa Adobe Target y no tiene Analytics, debe solicitar el aprovisionamiento de servicios principales poniéndose en contacto con el Servicio de atención al cliente.</li> <li>Póngase en contacto con su equipo de CRM. Descubra qué tipo de datos de clientes están disponibles y que desea utilizar en Analytics y en CX Enterprise.</li><li>Implementar servicios principales.</li></ol> Consulte [requisitos previos](t-crs-usecase.md#prerequisites-for-using-customer-attributes) antes de cargar los datos para obtener más información sobre cómo permitir que los usuarios usen esta característica. |
| ¿Cuántos atributos del cliente puedo utilizar? | Puede cargar cientos de columnas `.csv` en el servicio de atributos del cliente. Sin embargo, al configurar suscripciones y seleccionar atributos, se aplican los límites siguientes por grupos de informes, según las aplicaciones que tenga:  <ul><li>Foundation: 0</li><li>Select: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 en total</li><li>Premium: 200</li><li>Adobe Target Standard: 5</li><li>Adobe Target Premium: 200</li></ul> |
| ¿Es necesaria la migración al servicio CX Enterprise ID? | La migración depende de las aplicaciones que utilice. <ul><li>Adobe Analytics: Recomendado </li><li>Adobe Target: Necesario. </li></ul>El uso del servicio CX Enterprise ID permite la funcionalidad empresarial de CX más reciente, incluidas las audiencias en tiempo real, la modernización de Adobe Target, la integración de Analytics y el seguimiento de Video Heartbeat. |
| ¿Cómo se relaciona la funcionalidad de atributos del cliente con Adobe Audience Manager? | Aunque el Audience Manager puede recibir datos para hacer la identificación de audiencias, no puede realizar funciones de análisis que vinculen atributos a datos de comportamiento históricos. Tampoco proporciona las funciones de sistema de informes, análisis y segmentación disponibles en Adobe Analytics. [!DNL Customer Attributes] permite que los datos enriquecidos de todas las aplicaciones se unan y asocien con un solo ID para su uso en CX Enterprise. <br>En Adobe Target, los atributos del cliente aparecen como atributos individuales que se pueden combinar con otras reglas para crear públicos. Las audiencias compartidas en el servicio [!UICONTROL People] son audiencias completas que no se pueden modificar. |
| **(solo Adobe Analytics)** ¿En qué se diferencia esta funcionalidad de la que se proporciona en Analytics Premium? | En el pasado, los clientes interesados en combinar datos de atributos del cliente con datos de Analytics dependían en gran medida de la herramienta Data Workbench para esta funcionalidad. [!DNL Customer Attributes] expone esta funcionalidad a una audiencia mayor al proporcionar atributos del cliente tales como dimensiones y métricas en Report Builder. Los clientes de Analytics Standard tienen acceso a los [!DNL Customer Attributes], pero con capacidades limitadas. Los clientes de Analytics Premium pueden disfrutar de todas las funciones. |
| **(Solo Adobe Target)** ¿Puedo cargar o precargar datos para clientes que Adobe Target nunca ha visto? | Sí. Cuando un visitante realiza la primera solicitud a Adobe Target, el sistema busca la información de la que dispone Adobe sobre el visitante en [!DNL Customer Attributes] y usa los datos para la segmentación. **Nota:** La recuperación de estos datos puede tardar 20 minutos tras la primera interacción del visitante con Adobe Target. |
| **(Solo Adobe Target)** ¿Puedo crear un superpúblico combinando datos de atributos del cliente con datos de público compartidos? | No. Los datos de un público compartido son un público completado. |
| **(solo Adobe Target)** ¿En qué se diferencia [!DNL Customer Attributes] de la API de perfil en bloque de Adobe Target? | La API de perfil en bloque permite actualizar los perfiles de Adobe Target directamente mediante la API para un perfil individual o en bloque. La capacidad es similar a los [!DNL Customer Attributes], con las siguientes diferencias clave:<ul><li>La API de perfil es una llamada a la API de REST y a los [!DNL Customer Attributes] utilizan un FTP.</li><li>La API de perfil de Adobe Target solo envía datos a Adobe Target en lugar de a toda CX Enterprise.</li><li>Los [!DNL Customer Attributes] proporcionan una interfaz sencilla para crear y administrar estos datos externos.</li></ul> |
| **(Solo para Adobe Target)** ¿La carga de datos de [!DNL Customer Attributes] a Adobe Target amplía la duración del perfil del visitante de Adobe Target? | Sí. Consulte [Duración del perfil del visitante](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html) en la ayuda de Adobe Target. |
| **(Solo para Adobe Target)** ¿Puedo segmentar los datos cargados en [!DNL Customer Attributes] inmediatamente después de que el ID del cliente identifique el visitante? | Sí. En la llamada del servidor a Adobe Target, que incluye el ID de terceros de mbox, están disponibles todos los datos de atributos del cliente. |
| **(solo Adobe Target)** ¿Qué representa la columna **[!UICONTROL Sync Status]** para los archivos cargados en el origen de atributos del cliente? | Para ver el número de registros publicados y sincronizados por Adobe Target, haga clic en el icono Estado de sincronización respecto a un archivo de atributos específico. `Sync %` es una métrica en tiempo real que especifica el % de perfiles que se han sincronizado en Adobe Target.<br> **Nota:** Los atributos pueden tardar hasta 24 horas en sincronizarse con Adobe Target. |
| ¿Qué representan las métricas de carga de archivos en la fuente de [!DNL Customer Attributes]? | Puede comprobar el estado de los atributos cargados en [!DNL Customer Attributes] con la ayuda de las siguientes métricas: <ul><li>Registros: Número de registros en el archivo de atributos.</li><li>**Nuevos registros:** Número de registros nuevos presentes en el archivo de atributos.</li> <li>**Registros actualizados:** número de registros que existen en [!DNL Customer Attributes] con valores actualizados en el archivo.</li><li>**Todos los datos (registros):** número total de registros cargados correctamente en [!DNL Customer Attributes].</li></ul> |

{style="table-layout:auto"}
