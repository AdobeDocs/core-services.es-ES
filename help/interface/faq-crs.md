---
description: Preguntas frecuentes sobre los atributos de cliente en Adobe Experience Cloud, para Adobe Analytics y Adobe Target.
keywords: 'Atributos del cliente '
solution: Experience Cloud
title: 'Obtenga respuestas a las preguntas frecuentes sobre atributos de cliente '
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: 'Atributos del cliente '
topic: Administración
role: Administrator
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: 23ebc782838de74dcf0ae84d91b3b158794a2466
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 74%

---

# Preguntas más frecuentes sobre [!UICONTROL Atributos del cliente]

Preguntas más frecuentes y prácticas recomendadas para [!UICONTROL Atributos del cliente] en Adobe Analytics y Adobe Target.

## Prácticas recomendadas y limitaciones {#section_7F5189B3DAA84EE6865B91D2026EE05A}

Directrices y limitaciones al usar los [!UICONTROL Atributos del cliente].

| Problema | Descripción |
|--- |--- |
| Limitaciones de suscripción de [!UICONTROL atributos del cliente] | Cuando actualice a Analytics Premium, no podrá disponer de los atributos hasta haber transcurrido 24 horas. Durante este retraso, podría aparecer el error [!UICONTROL Máx. de suscripción a atributos]. |
| Varios inicios de sesión en el mismo dispositivo | Al utilizar [!UICONTROL Atributos del cliente] para cargar perfiles del cliente en una fuente de datos, el Adobe recomienda que no se compartan dispositivos (es decir, el mismo ID de Experience Cloud). El Experience Cloud ID (ECID) persiste en el dispositivo. Compartir dispositivos puede hacer que el ECID vincule varios usuarios al mismo ECID, lo que provoca resultados inesperados en [!DNL Target]. **Nota:** En el caso de dispositivos móviles, el ECID es permanente después de instalar la aplicación móvil. Vuelva a instalar la aplicación para generar un nuevo ECID. Para su uso en la web, se genera un nuevo ECID después de borrar la cookie del explorador. |
| Límite diario de carga de frecuencia | Adobe recomienda actualizar los Atributos del cliente solo una vez al día. Debe esperar al menos 24 horas para cargar otro archivo de datos de perfil del cliente para el mismo conjunto de perfiles. |
| ID de Analytics personalizado (`s.visitorID`) | El establecimiento de un ID de cliente mediante `s.visitorID` es un método para identificar a los usuarios en Analytics. Sin embargo, las integraciones en las que se exportan o importan datos [!DNL Analytics] mediante el servicio de ID no funcionan cuando se identifica un visitante mediante `s.visitorID.`<br>Esto incluye, entre otras cosas, audiencias compartidas, [!DNL Analytics] para Adobe Target (A4T) y [!UICONTROL Atributos del cliente].<br>Estas integraciones no admiten la configuración de un ID de Analytics personalizado. |
| Limitaciones de longitud de caracteres en [!DNL Analytics] | Al crear una suscripción [!DNL Analytics], las longitudes de campo de los archivos cargados se truncan a 255. |

## Preguntas frecuentes sobre los Atributos del cliente {#section_E47866EEA83348E09FE43CEC5E44C461}

| Pregunta | Respuesta |
|--- |--- |
| ¿Puedo recibir notificaciones sobre el estado de carga de Atributos del cliente? | Sí. |
| ¿Qué debo hacer para empezar a usar los Atributos del cliente? | <ol><li>Aprovisione sus soluciones. Si es cliente de Analytics, Adobe le proporcionará los Atributos del cliente. Si solo usa Adobe Target y no tiene Analytics, debe solicitar el aprovisionamiento de servicios principales poniéndose en contacto con el Servicio de atención al cliente.</li> <li>Póngase en contacto con su equipo de CRM. Descubra qué tipo de datos de clientes están disponibles y que quisiera usar en Analytics y en Experience Cloud.</li><li>Implementar servicios principales. Consulte [Activación de las soluciones para servicios principales](core-services.md) para ver los pasos necesarios para modernizar la implementación. (Consulte la sección sobre la sincronización de ID de cliente para obtener información importante).</li></ol> **Nota:** Hay disponible una sección de preguntas más frecuentes para implementar los servicios principales [aquí](faq.md). |
| ¿Cuántos Atributos del cliente puedo utilizar? | Puede cargar cientos de columnas `.csv` en el servicio de atributos del cliente. Sin embargo, al configurar suscripciones y seleccionar atributos grupo de informes, se aplican los límites siguientes por grupos de informes, según la solución que tenga:  <ul><li>Foundation: 0</li><li>Select: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 en total</li><li>Premium: 200</li><li>Adobe Target Standard: 5</li><li>Adobe Target Premium: 200</li></ul> |
| ¿Se requiere la migración al Servicio de Experience Cloud ID? | La migración depende de las soluciones que utilice. <ul><li>Adobe Analytics: Recomendado </li><li>Adobe Target: Necesario. </li></ul><br>El uso del servicio de Experience Cloud ID permite la funcionalidad de Experience Cloud más reciente, incluidas las audiencias en tiempo real, la modernización de Adobe Target, la integración de Analytics y el seguimiento de Video Heartbeat. <br> Para obtener más información, consulte [Activación de las soluciones en los servicios principales](core-services.md). <br>**Nota:** El servicio [Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en) es la implementación modernizada de lo que antes se conocía como _Servicio de ID de visitante de Analytics._ |
| ¿Cómo se relaciona la funcionalidad de atributos del cliente con Adobe Audience Manager? | Aunque el Audience Manager puede recibir datos para hacer la identificación de audiencias, no puede realizar funciones de análisis que vinculen atributos a datos de comportamiento históricos. Tampoco proporciona las funciones de sistema de informes, análisis y segmentación disponibles en Adobe Analytics. [!UICONTROL People] permite que los datos enriquecidos de todas las soluciones se unan y asocien con un solo ID para su uso en Experience Cloud. <br>En Adobe Target, los Atributos del cliente aparecen como atributos individuales que se pueden combinar con otras reglas para crear audiencias. Las Audiencias compartidas con el servicio de [!UICONTROL Usuarios] son audiencias completas que no se pueden modificar. |
| **(Solo Analytics)** ¿En qué se diferencia esta funcionalidad de la que se proporciona en Analytics Premium? | En el pasado, los clientes interesados en combinar datos de atributos del cliente con datos de Analytics dependían en gran medida de la herramienta de Data Workbench para esta funcionalidad. [!UICONTROL Los ] atributos del cliente exponen esta funcionalidad a una audiencia mayor al proporcionar atributos del cliente como dimensiones y métricas en Reports &amp; Analytics, Ad Hoc Analysis y Report Builder. Los clientes de Analytics Standard tienen acceso a los Atributos del cliente, pero con capacidades limitadas. Los clientes de Analytics Premium pueden disfrutar de todas las funciones. |
| **(Solo Adobe Target)** ¿Puedo cargar o precargar datos para clientes que Adobe Target nunca ha visto? | Sí. Cuando el visitante realiza su primera solicitud a Adobe Target, el sistema busca el Adobe de información existente sobre el visitante en Atributos del cliente y usa esos datos para la segmentación. **Nota:** La recuperación de estos datos puede tardar 20 minutos tras la primera interacción del visitante con Adobe Target. |
| **(Solo Adobe Target)** ¿Puedo crear una superaudiencia combinando datos de atributos del cliente con datos de audiencia compartidos? | No. Los datos de audiencia compartida son una audiencia completada. |
| **(Solo Adobe Target)**[!UICONTROL  ¿En qué se diferencia la funcionalidad de atributos del cliente de la API de perfil en bloque de Adobe Target?] | La API de perfil en bloque permite actualizar los perfiles de Adobe Target directamente mediante la API, para un perfil individual o en bloque. La capacidad es similar a los Atributos del cliente, con las siguientes diferencias clave:<ul><li>La API de perfil es una llamada a la API de REST y los Atributos del cliente utilizan un FTP.</li><li>La API de perfil de Adobe Target solo envía datos a Adobe Target en lugar de a todo Experience Cloud.</li><li>Los Atributos del cliente proporcionan una interfaz sencilla para crear y administrar estos datos externos.</li></ul> |
| **(Solo Adobe Target)** ¿La carga de datos de atributos del cliente a Adobe Target amplía la duración del perfil del visitante de Adobe Target? | Sí. Consulte [Duración del perfil del visitante](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=en) en la ayuda de Adobe Target. |
| **(Solo Adobe Target)** ¿Puedo segmentar los datos cargados en los Atributos del cliente inmediatamente después de que el ID del cliente identifique el visitante? | Sí. En la llamada del servidor a Adobe Target, que incluye el ID de terceros de mbox, están disponibles todos los datos de atributos del cliente. |
| **(Solo Adobe Target)** ¿Qué representa la columna **[!UICONTROL Estado de sincronización]** para los archivos cargados en el origen de atributos del cliente? | Para ver el número de registros publicados y sincronizados por Adobe Target, haga clic en el icono Estado de sincronización con un archivo de atributos específico. `Sync %` es una métrica en tiempo real que especifica el % de perfiles que se han sincronizado en Adobe Target.<br> **Nota:** Los atributos pueden tardar hasta 24 horas en sincronizarse con Adobe Target. |
| ¿Qué representan las métricas de carga de archivos en la fuente de atributos del cliente? | Puede comprobar el estado de los atributos cargados en Atributos del cliente con la ayuda de las siguientes métricas: <ul><li>Registros: Número de registros en el archivo de atributos.</li><li>**Nuevos registros:** Número de registros nuevos presentes en el archivo de atributos.</li> <li>**Registros actualizados:** Número de registros que existen en Atributos del cliente con valores actualizados en el archivo.</li><li>**Todos los datos (registros):** Número total de registros cargados correctamente en Atributos del cliente.</li></ul> |
