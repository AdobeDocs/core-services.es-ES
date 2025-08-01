---
description: Preguntas frecuentes sobre  [!DNL customer attributes]  en Adobe Experience Cloud para Adobe Analytics y Adobe Target.
solution: Experience Cloud
title: Preguntas frecuentes sobre  [!DNL customer attributes]
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 81%

---

# Preguntas frecuentes sobre [!DNL customer attributes]

Preguntas frecuentes y prácticas recomendadas sobre [!DNL customer attributes] en Adobe Analytics y Adobe Target.

## Prácticas recomendadas y limitaciones {#best_practices}

Directrices y limitaciones al usar [!DNL customer attributes].

| Problema | Descripción |
|--- |--- |
| [!UICONTROL limitaciones de suscripción de atributo del cliente] | Cuando actualice a Analytics Premium, no podrá disponer de los atributos hasta haber transcurrido 24 horas. Durante este periodo, es posible que veas un error de [!UICONTROL atributo Subscription Max]. |
| Varios inicios de sesión en el mismo dispositivo | Cuando se utilizan los [!DNL customer attributes] para cargar los perfiles del cliente en una fuente de datos, Adobe recomienda que no se compartan dispositivos (es decir, el mismo Experience Cloud ID). El Experience Cloud ID (ECID) persiste en el dispositivo. Compartir dispositivos puede hacer que el ECID vincule varios usuarios al mismo ECID, lo que provoca resultados inesperados en [!DNL Target]. **Nota:** En el caso de dispositivos móviles, el ECID es permanente después de instalar la aplicación móvil y debe volver a instalar la aplicación para generar un nuevo ECID. Para su uso en la web, se genera un nuevo ECID después de borrar la cookie del explorador. |
| Límite diario de carga de frecuencia | Adobe recomienda actualizar los [!DNL customer attributes] solo una vez al día. Debe esperar al menos 24 horas para cargar otro archivo de datos de perfil del cliente para el mismo conjunto de perfiles. |
| ID de Analytics personalizado (`s.visitorID`) | Configurar un ID de cliente con `s.visitorID` es un método para identificar a los usuarios en Adobe Analytics. Sin embargo, las integraciones en las que se exportan o importan datos de [!DNL Analytics] mediante el servicio de ID no funcionan cuando se identifica un visitante mediante `s.visitorID.`<br>. Esto incluye, entre otras cosas, públicos compartidos, [!DNL Analytics] para Adobe Target (A4T) y [!DNL customer attributes].<br>Estas integraciones no admiten la configuración de un ID de Analytics personalizado. |
| Limitaciones de longitud de caracteres en [!DNL Analytics] | Al crear una suscripción de [!DNL Analytics], las longitudes de campo de los archivos cargados se truncan a 255. |

{style="table-layout:auto"}

## Preguntas frecuentes sobre [!DNL customer attributes] {#section_E47866EEA83348E09FE43CEC5E44C461}

| Pregunta | Respuesta |
|--- |--- |
| ¿Puedo recibir notificaciones sobre el estado de carga de [!DNL customer attributes]? | Sí. |
| ¿Qué debo hacer para empezar a usar los [!DNL customer attributes]? | <ol><li>Aprovisione sus soluciones. Si es cliente de Adobe Analytics, Adobe le proporcionará [!DNL customer attributes]. Si solo usa Adobe Target y no tiene Analytics, debe solicitar el aprovisionamiento de servicios principales poniéndose en contacto con el Servicio de atención al cliente.</li> <li>Póngase en contacto con su equipo de CRM. Descubra qué tipo de datos de clientes están disponibles y qué quisiera usar en Analytics y Experience Cloud.</li><li>Implementar servicios principales.</li></ol> |
| ¿Cuántos [!DNL customer attributes] puedo utilizar? | Puede cargar cientos de columnas `.csv` en el servicio de atributos del cliente. Sin embargo, al configurar suscripciones y seleccionar atributos, se aplican los límites siguientes por grupos de informes, según las aplicaciones que tenga:  <ul><li>Foundation: 0</li><li>Select: 3</li><li>Prime: 15</li><li>Ultimate: 200</li><li>Standard: 3 en total</li><li>Premium: 200</li><li>Adobe Target Standard: 5</li><li>Adobe Target Premium: 200</li></ul> |
| ¿Se requiere la migración al Servicio de Experience Cloud ID? | La migración depende de las aplicaciones que utilice. <ul><li>Adobe Analytics: Recomendado </li><li>Adobe Target: Necesario. </li></ul><br>El uso del servicio Experience Cloud ID habilita la funcionalidad Experience Cloud más reciente, incluidas las audiencias en tiempo real, la modernización de Adobe Target, la integración de Analytics y el seguimiento de Video Heartbeat. |
| ¿Cómo se relaciona la funcionalidad de atributos del cliente con Adobe Audience Manager? | Aunque el Audience Manager puede recibir datos para hacer la identificación de audiencias, no puede realizar funciones de análisis que vinculen atributos a datos de comportamiento históricos. Tampoco proporciona las funciones de sistema de informes, análisis y segmentación disponibles en Adobe Analytics. [!UICONTROL Atributos del cliente] permite que los datos enriquecidos de todas las aplicaciones se unan y asocien con un solo ID para su uso en Experience Cloud. <br>En Adobe Target, los [!DNL customer attributes] aparecen como atributos individuales que se pueden combinar con otras reglas para crear públicos. Los públicos compartidos con el servicio de [!UICONTROL Usuarios] son públicos completos que no se pueden modificar. |
| **(solo Adobe Analytics)** ¿En qué se diferencia esta funcionalidad de la que se proporciona en Analytics Premium? | En el pasado, los clientes interesados en combinar datos de atributos del cliente con datos de Analytics dependían en gran medida de la herramienta Data Workbench para esta funcionalidad. [!DNL customer attributes] expone esta funcionalidad a una audiencia mayor al proporcionar [!DNL customer attributes] como dimensiones y métricas en Report Builder. Los clientes de Analytics Standard tienen acceso a los [!DNL customer attributes], pero con capacidades limitadas. Los clientes de Analytics Premium pueden disfrutar de todas las funciones. |
| **(Solo Adobe Target)** ¿Puedo cargar o precargar datos para clientes que Adobe Target nunca ha visto? | Sí. Cuando un visitante realiza la primera solicitud a Adobe Target, el sistema busca la información de la que dispone Adobe sobre el visitante en [!DNL customer attributes] y usa los datos para la segmentación. **Nota:** La recuperación de estos datos puede tardar 20 minutos tras la primera interacción del visitante con Adobe Target. |
| **(Solo Adobe Target)** ¿Puedo crear un superpúblico combinando datos de atributos del cliente con datos de público compartidos? | No. Los datos de un público compartido son un público completado. |
| **(Solo para Adobe Target)** ¿En qué se diferencia la funcionalidad de [!DNL customer attributes] de la API de perfil en bloque de Adobe Target? | La API de perfil en bloque permite actualizar los perfiles de Adobe Target directamente mediante la API para un perfil individual o en bloque. La capacidad es similar a los [!DNL customer attributes], con las siguientes diferencias clave:<ul><li>La API de perfil es una llamada a la API de REST y a los [!DNL customer attributes] utilizan un FTP.</li><li>La API de perfil de Adobe Target solo envía datos a Adobe Target en lugar de a todo Experience Cloud.</li><li>Los [!DNL customer attributes] proporcionan una interfaz sencilla para crear y administrar estos datos externos.</li></ul> |
| **(Solo para Adobe Target)** ¿La carga de datos de [!DNL customer attributes] a Adobe Target amplía la duración del perfil del visitante de Adobe Target? | Sí. Consulte [Duración del perfil del visitante](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=es) en la ayuda de Adobe Target. |
| **(Solo para Adobe Target)** ¿Puedo segmentar los datos cargados en [!DNL customer attributes] inmediatamente después de que el ID del cliente identifique el visitante? | Sí. En la llamada del servidor a Adobe Target, que incluye el ID de terceros de mbox, están disponibles todos los datos de atributos del cliente. |
| **(Solo Adobe Target)** ¿Qué representa la columna **[!UICONTROL Estado de sincronización]** para los archivos cargados en el origen de atributos del cliente? | Para ver el número de registros publicados y sincronizados por Adobe Target, haga clic en el icono Estado de sincronización respecto a un archivo de atributos específico. `Sync %` es una métrica en tiempo real que especifica el % de perfiles que se han sincronizado en Adobe Target.<br> **Nota:** Los atributos pueden tardar hasta 24 horas en sincronizarse con Adobe Target. |
| ¿Qué representan las métricas de carga de archivos en la fuente de [!DNL customer attributes]? | Puede comprobar el estado de los atributos cargados en [!DNL customer attributes] con la ayuda de las siguientes métricas: <ul><li>Registros: Número de registros en el archivo de atributos.</li><li>**Nuevos registros:** Número de registros nuevos presentes en el archivo de atributos.</li> <li>**Registros actualizados:** número de registros que existen en [!DNL customer attributes] con valores actualizados en el archivo.</li><li>**Todos los datos (registros):** número total de registros cargados correctamente en [!DNL customer attributes].</li></ul> |

{style="table-layout:auto"}
