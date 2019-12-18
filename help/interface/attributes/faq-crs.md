---
description: Preguntas más frecuentes y prácticas recomendadas para atributos del cliente en Analytics y Target.
keywords: customer attributes
seo-description: Preguntas más frecuentes y prácticas recomendadas para atributos del cliente en Analytics y Target.
seo-title: Preguntas más frecuentes, limitaciones y prácticas recomendadas
solution: Experience Cloud
title: Preguntas más frecuentes, limitaciones y prácticas recomendadas
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: 5151026cf3ccf004d7fd311913b2cac1a272ff8d

---


# Preguntas más frecuentes, limitaciones y prácticas recomendadas

Preguntas más frecuentes y prácticas recomendadas para atributos del cliente en Analytics y Target.


## Prácticas recomendadas y limitaciones  {#section_7F5189B3DAA84EE6865B91D2026EE05A}

Sugerencias y limitaciones en el uso de Atributos del cliente.

| Problema | Descripción |
|--- |--- |
| Limitaciones de la suscripción a Atributos del cliente | Cuando actualice a Analytics Premium, no podrá disponer de los atributos adicionales hasta que transcurran transcurrido 24 horas. Durante este periodo, puede aparecer el error Máximas suscripciones a atributos. |
| Límite diario de carga de frecuencia | Adobe recomienda actualizar los atributos del cliente solo una vez al día. Debe esperar al menos 24 horas para cargar otro archivo de datos de perfil de cliente para el mismo conjunto de perfiles. |
| ID de Analytics personalizado (s.visitorID) | Configurar un ID de cliente con    s.visitorID es un modo de identificar usuarios en Analytics. Sin embargo, las integraciones en las que se exportan o importan datos de Analytics mediante el servicio de ID no funcionarán cuando se identifique a un visitante mediante s.visitorID.<br>Entre ellas se cuentan las audiencias compartidas, Análisis para objetivo (A4T) y atributos del cliente.<br>Estas integraciones no admiten la configuración de un ID de Analytics personalizado. |
| Limitaciones de extensión de caracteres en Analytics | Cuando se crea una suscripción a Analytics, la longitud de campo para los archivos cargados se trunca a 255. |

## Preguntas más frecuentes sobre los atributos del cliente  {#section_E47866EEA83348E09FE43CEC5E44C461}

<table id="table_88631069013B408EBB0A810657662B36"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Pregunta </th> 
   <th colname="col2" class="entry"> Respuesta </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>¿Puedo recibir notificaciones acerca del estado de carga de atributos del cliente? </p> </td> 
   <td colname="col2"> <p>Sí. Consulte <a href="../admin-getting-started/organizations.md#concept_0105453AD71847B8BFCAF4A40915F157" format="dita" scope="local">Administración de notificaciones</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> ¿Qué debo hacer para empezar a utilizar los atributos del cliente? </p> </td> 
   <td colname="col2"> 
    <ol id="ol_1FACEF0990B6486B8DE86245D17695A8"> 
     <li id="li_F0C1542853684F8591FDC1B441D31A56"> <p>Realice un aprovisionamiento. </p> <p>Si es cliente de <b>Analytics</b>, Adobe realizará el aprovisionamiento de atributos del cliente. Si solo utiliza <b>Target</b> y no tiene Analytics, debe solicitar el aprovisionamiento de servicios principales poniéndose en contacto con el servicio de atención al cliente. </p> </li> 
     <li id="li_444FEDEE4B7244F79BA847662F5B17CB"> <p>Hable con el equipo de CRM. Descubra qué tipo de datos de cliente están disponibles y pueden ser interesantes de utilizar en Analytics y en Experience Cloud. </p> </li> 
     <li id="li_32D4AAF8C29748A78801A0E1BFB37AF5"> <p>Implemente los servicios principales. </p> <p>Consulte <a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local"> Introducción: Activación de las soluciones en los servicios principales</a> para ver los pasos necesarios para modernizar su implementación de servicios principales. (Consulte la sección sobre sincronización de ID de clientes para obtener información importante). </p> </li> 
    </ol> <p> <b>Nota:</b> Hay disponible una sección de preguntas más frecuentes para implementar los servicios principales  <a href="../admin-getting-started/faq.md#concept_13219B4E51784577B6FF78AAA203DE91" format="dita" scope="local"> aquí</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> ¿Cuántos atributos del cliente puedo utilizar? </p> </td> 
   <td colname="col2"> <p>Puede cargar cientos de columnas <span class="filepath">.csv</span> en el servicio de atributos del cliente. Sin embargo, al configurar suscripciones y seleccionar atributos, se aplican los límites siguientes (por grupo de informes), según las soluciones que posea:</p> <p> 
     <ul>
     <li>Foundation: 0</li>
     <li>Select: 3</li>
     <li>Prime: 15</li>
     <li>Ultimate: 200</li>
     <li>Standard: 3 en total</li>
     <li>Premium: 200</li>
     <li>Target Standard: 5</li>
     <li>Target Premium: 200</li></ul>
     </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>¿Hace falta migrar al servicio Experience Cloud ID? </p> </td> 
   <td colname="col2"> <p>La migración depende de las soluciones que utilice. </p> <p> 
     <ul id="ul_9C473434B5DA4C6299AAB209DEDFCDE7"> 
      <li id="li_8BC10EB2825F4ADF8CA61F71D4994A28"> <b>Adobe Analytics</b>: extremadamente recomendable. </li> 
      <li id="li_56F518E3F3DF4C93B6F7EF3B40ACC52F"> <b>Adobe Target:</b> necesario. </li> 
     </ul> </p> <p>El uso del servicio de ID mejora la funcionalidad y abre las puertas al uso de las funcionalidades de Experience Cloud más recientes, incluidas las audiencias en tiempo real, la modernización de destino, la integración con Analytics y el seguimiento del funcionamiento del vídeo. </p> <p>Para ver información detallada, consulte <a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">Servicios principales: Activar las soluciones</a> </p> <p> <b>Nota</b>: El servicio <span class="term"> Experience Cloud ID</span> es la implementación modernizada de lo que antes se conocía como <span class="term">Servicio de ID de visitante de Analytics</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>¿De qué forma se relaciona la función de atributos del cliente con Adobe Audience Manager? </p> </td> 
   <td colname="col2"> <p>Aunque que Audience Manager puede recibir datos y realizar la identificación de la audiencia, no puede realizar la función de análisis que une los atributos con los datos de comportamiento históricos ni proporcionar las funciones de generación de informes, análisis y segmentación disponibles en Adobe Analytics. El servicio principal People permite que los datos enriquecidos de las distintas soluciones se unan y asocien a un único ID que se utiliza en todo Experience Cloud. </p> <p> En Adobe Target, los atributos del cliente aparecen como atributos individuales que se pueden combinar con otras reglas para crear audiencias. Las audiencias compartidas en el servicio principal People son completas y no se pueden modificar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(Solo Analytics) </b>¿Qué diferencias hay entre esta funcionalidad y la de Analytics Premium? </p> </td> 
   <td colname="col2"> <p>Anteriormente, los clientes interesados en combinar datos de atributos del cliente con datos de Analytics confiaban en gran medida en la herramienta de Data Workbench para esta operación. Los atributos del cliente exponen esta función a una audiencia mayor al proporcionar atributos del cliente tales como dimensiones y métricas en Reports &amp; Analytics, Ad Hoc Analysis y Report Builder. Los clientes de Analytics Standard tendrán acceso a los atributos del cliente, pero con funciones limitadas. Las funciones al completo están disponibles para los clientes de Analytics Premium. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(Solo Target)</b> ¿Puedo cargar o precargar datos sobre clientes que Target nunca haya visto? </p> </td> 
   <td colname="col2"> <p> Sí. Cuando un visitante realiza la primera solicitud a Target, el sistema busca la información de la que disponemos sobre el visitante en Atributos del cliente y usa los datos para la segmentación. </p> <p> <p>Nota: La recuperación de estos datos puede tardar 20 minutos tras la primera interacción del visitante con Target. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(Solo Target)</b> ¿Puedo crear una superaudiencia combinando datos sobre los atributos del cliente y datos sobre audiencias compartidas? </p> </td> 
   <td colname="col2"> <p>No. Los datos sobre audiencias compartidas son una audiencia completa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(Solo Target) </b>¿En qué se diferencia la funcionalidad de los atributos del cliente con la API de perfil en bloque de Target? </p> </td> 
   <td colname="col2"> <p> La <a href="https://www.adobe.io/apis/experiencecloud/target.html" format="https" scope="external">API de perfil en bloque</a> permite actualizar los perfiles de Target directamente mediante la API, para un perfil individual o en bloque. La capacidad es similar a los atributos del cliente, con las siguientes diferencias clave: </p> 
    <ul id="ul_5AAA4A8497C04F50A8AAA9F776BB868E"> 
     <li id="li_B20AEA397F3B4C86A1140CDA61ABD575">La API de perfil es una llamada de API REST y los atributos del cliente utilizan FTP. </li> 
     <li id="li_7FBE428EF5D34B6AA09B6368E8210344">La API de perfil de Target solo envía datos a Target en lugar de a todo Experience Cloud. </li> 
     <li id="li_CBB4D3FAF53944E0A066A4AD9F9C8760">Los atributos del cliente proporcionan una interfaz sencilla para crear y administrar estos datos externos. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(Solo Target)</b> ¿La carga de datos desde los atributos del cliente a Adobe Target amplía la duración del perfil del visitante de Target? </p> </td> 
   <td colname="col2"> <p>Sí. Consulte <a href="https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html" format="https" scope="external">Duración del perfil del visitante</a> en la ayuda de Adobe Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> (Solo Target)</b> ¿Puedo tener como destino los datos cargados en los atributos del cliente inmediatamente después de identificar al visitante con el ID del cliente? </p> </td> 
   <td colname="col2"> <p>Sí. </p> <p>En la llamada del servidor a Target, que incluye el ID de terceros de mbox, estarán disponibles todos los datos de atributos del cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>
