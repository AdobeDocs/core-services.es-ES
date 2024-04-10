---
description: Preguntas frecuentes sobre [!DNL Customer Attributes] en Adobe Experience Cloud, para Adobe Analytics y Adobe Target.
solution: Experience Cloud
title: Preguntas más frecuentes sobre [!DNL Customer Attributes]
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 63%

---

# Preguntas frecuentes sobre [!DNL Customer Attributes]

Preguntas frecuentes y prácticas recomendadas para [!DNL Customer Attributes] en Adobe Analytics y Adobe Target.

## Prácticas recomendadas y limitaciones {#section_7F5189B3DAA84EE6865B91D2026EE05A}

Directrices y limitaciones al utilizar [!DNL Customer Attributes].

| Problema | Descripción |
|--- |--- |
| Limitaciones de suscripción de [!UICONTROL atributos del cliente] | Cuando actualice a Analytics Premium, no podrá disponer de los atributos hasta haber transcurrido 24 horas. Durante este periodo, puede aparecer el error [!UICONTROL Máximas suscripciones a atributos]. |
| Varios inicios de sesión en el mismo dispositivo | Al utilizar [!DNL Customer Attributes] para cargar perfiles de clientes en una fuente de datos, el Adobe recomienda que no se compartan dispositivos (es decir, el mismo ID de Experience Cloud). El Experience Cloud ID (ECID) persiste en el dispositivo. Compartir dispositivos puede hacer que el ECID vincule varios usuarios al mismo ECID, lo que provoca resultados inesperados en [!DNL Target]. **Nota:** En el caso de dispositivos móviles, el ECID es permanente después de instalar la aplicación móvil y debe volver a instalar la aplicación para generar un nuevo ECID. Para su uso en la web, se genera un nuevo ECID después de borrar la cookie del explorador. |
| Límite diario de carga de frecuencia | El Adobe recomienda actualizar [!DNL Customer Attributes] solo una vez al día. Debe esperar al menos 24 horas para cargar otro archivo de datos de perfil del cliente para el mismo conjunto de perfiles. |
| ID de Analytics personalizado (`s.visitorID`) | El establecimiento de un ID de cliente mediante `s.visitorID` es un método para identificar a los usuarios en Analytics. Sin embargo, integraciones en las que [!DNL Analytics] Los datos exportados o importados mediante el servicio de ID no funcionan cuando se identifica un visitante mediante `s.visitorID.`<br>Entre ellas se cuentan las audiencias compartidas, [!DNL Analytics] para Adobe Target (A4T), y [!DNL Customer Attributes].<br>Estas integraciones no admiten la configuración de un ID de Analytics personalizado. |
| Limitaciones de longitud de caracteres en [!DNL Analytics] | Al crear una suscripción de [!DNL Analytics], las longitudes de campo de los archivos cargados se truncan a 255. |

{style="table-layout:auto"}

## Preguntas frecuentes sobre [!DNL Customer Attributes] {#section_E47866EEA83348E09FE43CEC5E44C461}

| Pregunta | Respuesta |
|--- |--- |
| ¿Puedo recibir notificaciones sobre el estado de carga de? [!DNL Customer Attributes]? | Sí. |
| ¿Qué debo hacer para empezar a usar? [!DNL Customer Attributes]? | <ol><li>Aprovisione sus soluciones. Si es cliente de Analytics, Adobe le proporcionará para lo siguiente [!DNL Customer Attributes]. Si solo usa Adobe Target y no tiene Analytics, debe solicitar el aprovisionamiento de servicios principales poniéndose en contacto con el Servicio de atención al cliente.</li> <li>Póngase en contacto con su equipo de CRM. Descubra qué tipo de datos de clientes están disponibles y que desea utilizar en Analytics y en Experience Cloud.</li><li>Implemente servicios principales. Consulte [Activación de las aplicaciones para servicios principales](core-services.md) para ver los pasos necesarios para modernizar la implementación. (Consulte la sección sobre la sincronización de ID de cliente para obtener información importante).</li></ol> **Nota:** Hay disponible una sección de preguntas más frecuentes para implementar los servicios principales [aquí](faq.md). |
| ¿Cuántos [!DNL Customer Attributes] ¿Se me permite utilizar? | Puede cargar cientos de columnas `.csv` en el servicio de atributos del cliente. Sin embargo, al configurar suscripciones y seleccionar atributos, se aplican los límites siguientes por grupos de informes, según las aplicaciones que tenga:  <ul><li>Foundation: 0</li><li>Select: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 en total</li><li>Premium: 200</li><li>Adobe Target Standard: 5</li><li>Adobe Target Premium: 200</li></ul> |
| ¿Se requiere la migración al Servicio de Experience Cloud ID? | La migración depende de las aplicaciones que utilice. <ul><li>Adobe Analytics: Recomendado </li><li>Adobe Target: Necesario. </li></ul><br>El uso del servicio de Experience Cloud ID permite la funcionalidad de Experience Cloud más reciente, incluidos los públicos en tiempo real, la modernización de Adobe Target, la integración de Analytics y el seguimiento de Video Heartbeat. <br> Para obtener más información, consulte [Activación de las aplicaciones en los servicios principales](core-services.md). <br>**Nota:** El [servicio Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=es) es la implementación modernizada de lo que antes se conocía como _Servicio de ID de visitante de Analytics._ |
| ¿Cómo se relaciona la funcionalidad de atributos del cliente con Adobe Audience Manager? | Aunque el Audience Manager puede recibir datos para hacer la identificación de audiencias, no puede realizar funciones de análisis que vinculen atributos a datos de comportamiento históricos. Tampoco proporciona las funciones de sistema de informes, análisis y segmentación disponibles en Adobe Analytics. [!UICONTROL People] permite que los datos enriquecidos de todas las aplicaciones se unan y asocien con un solo ID para su uso en todo el Experience Cloud. <br>En Adobe Target, [!DNL Customer Attributes] aparecen como atributos individuales que se pueden combinar con otras reglas para crear audiencias. Los públicos compartidos con el servicio de [!UICONTROL Usuarios] son públicos completos que no se pueden modificar. |
| **(Solo Analytics)** ¿En qué se diferencia esta funcionalidad de la que se proporciona en Analytics Premium? | En el pasado, los clientes interesados en combinar datos de atributos del cliente con datos de Analytics dependían en gran medida de la herramienta Data Workbench para esta funcionalidad. [!DNL Customer Attributes] expone esta funcionalidad a una audiencia mayor al proporcionar [!DNL Customer Attributes] como dimensiones y métricas en reports &amp; analytics, Ad Hoc Analysis y report builder. Los clientes de Analytics Standard tienen acceso a [!DNL Customer Attributes], pero con capacidades limitadas. Los clientes de Analytics Premium pueden disfrutar de todas las funciones. |
| **(Solo Adobe Target)** ¿Puedo cargar o precargar datos para clientes que Adobe Target nunca ha visto? | Sí. Cuando un visitante realiza la primera solicitud a Adobe Target, el sistema busca el Adobe de información existente sobre él en [!DNL Customer Attributes] y utilizar esos datos para la segmentación. **Nota:** La recuperación de estos datos puede tardar 20 minutos tras la primera interacción del visitante con Adobe Target. |
| **(Solo Adobe Target)** ¿Puedo crear un superpúblico combinando datos de atributos del cliente con datos de público compartidos? | No. Los datos de un público compartido son un público completado. |
| **(solo Adobe Target)** ¿Cómo funciona [!DNL Customer Attributes] funcionalidad comparada con la API de perfil en bloque de Adobe Target? | La API de perfil en bloque permite actualizar los perfiles de Adobe Target directamente mediante la API, para un perfil individual o en bloque. La capacidad es similar a [!DNL Customer Attributes], con las siguientes diferencias clave:<ul><li>La API de perfil es una llamada a la API de REST y [!DNL Customer Attributes] utiliza FTP.</li><li>La API de perfil de Adobe Target solo envía datos a Adobe Target en lugar de a todo Experience Cloud.</li><li>[!DNL Customer Attributes] proporciona una interfaz sencilla para crear y administrar estos datos externos.</li></ul> |
| **(solo Adobe Target)** ¿La carga de datos desde [!DNL Customer Attributes] Adobe Target para ampliar la duración del perfil del visitante de Adobe Target? | Sí. Consulte [Duración del perfil del visitante](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=es) en la ayuda de Adobe Target. |
| **(solo Adobe Target)** ¿Puedo segmentar los datos cargados en? [!DNL Customer Attributes] inmediatamente después de que el ID de cliente identifique el visitante? | Sí. En la llamada del servidor a Adobe Target, que incluye el ID de terceros de mbox, están disponibles todos los datos de atributos del cliente. |
| **(Solo Adobe Target)** ¿Qué representa la columna **[!UICONTROL Estado de sincronización]** para los archivos cargados en el origen de atributos del cliente? | Para ver el número de registros publicados y sincronizados por Adobe Target, haga clic en el icono Estado de sincronización respecto a un archivo de atributos específico. `Sync %` es una métrica en tiempo real que especifica el % de perfiles que se han sincronizado en Adobe Target.<br> **Nota:** Los atributos pueden tardar hasta 24 horas en sincronizarse con Adobe Target. |
| ¿Qué representan las métricas de carga de archivos en? [!DNL Customer Attributes] ¿Fuente? | Puede comprobar el estado de los atributos cargados en [!DNL Customer Attributes] con la ayuda de las siguientes métricas: <ul><li>Registros: Número de registros en el archivo de atributos.</li><li>**Nuevos registros:** Número de registros nuevos presentes en el archivo de atributos.</li> <li>**Registros actualizados:** Número de registros en que existen en [!DNL Customer Attributes] con valores actualizados en el archivo.</li><li>**Todos los datos (registros):** Número total de registros cargados correctamente en [!DNL Customer Attributes].</li></ul> |

{style="table-layout:auto"}