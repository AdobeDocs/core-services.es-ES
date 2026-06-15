---
description: Obtenga información sobre la función de búsqueda unificada para determinadas aplicaciones en CX Enterprise.
solution: Experience Cloud
title: Búsqueda unificada de Experience Cloud
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Beginner
exl-id: 70586f18-6f84-4308-bab3-1da7fab823d6
TQID: https://experienceleague.adobe.com/xE4H6kdjbKSwVygCsOV4zTBqPoBHAVMHfJMyYOummg0
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 660
ht-degree: 17%

---

# [!UICONTROL Búsqueda unificada] en CX Enterprise

La búsqueda [!UICONTROL Búsqueda unificada] le permite encontrar objetos o entidades empresariales en los que realizar búsquedas de manera uniforme, sin problemas y con un solo clic. Esta búsqueda también muestra los objetos a los que ha accedido recientemente.

![Buscar globalmente objetos y entidades](../assets/platform-search.png)

## Obteniendo acceso a [!UICONTROL búsqueda unificada]

[!UICONTROL Búsqueda unificada] está disponible en todas las páginas del encabezado de CX Enterprise en la parte superior de la página. También puede usar el método abreviado de teclado `command /` o `ctrl /` para acceder a la búsqueda.

Esta función solo está disponible para productos compatibles, que actualmente son:

* Experience Platform (AEP)
* Journey Optimizer (AJO)

A medida que se indexa más contenido, esta función se añade a las aplicaciones relevantes.

## Objetos y campos que se pueden buscar

A medida que escribe, se muestran los resultados principales coincidentes de los objetos a los que tiene acceso.

Nuestros algoritmos muestran primero los registros más relevantes. El orden de los resultados depende de varios factores, como:

Su capacidad y permisos de objeto
Porcentaje de coincidencia
Si hay una coincidencia exacta

![[!UICONTROL Búsqueda unificada] en CX Enterprise](../assets/unified-search-results.png)

Los objetos empresariales que se pueden buscar incluyen:

* Segmentos (nombre, descripción, ID)
* Esquema (nombre, descripción, ID)
* Conjuntos de datos (nombre, descripción, ID)
* Fuentes (nombre, descripción, ID)
* Destinos (nombre, descripción, ID)
* Consultas (nombre, descripción, ID)
* Mensajes (nombre, descripción, ID)
* Ofertas (nombre, descripción, ID)
* Componentes (nombre, descripción e ID)
* Recorridos (nombre, descripción, ID)

Si una palabra clave coincide con una página de navegación, puede obtener un vínculo de acceso rápido a los conjuntos de datos de ejemplo de la página de navegación. La sección de resultados principales muestra los 30 resultados principales.

También puede encontrar los artículos de ayuda de Experience League y Communities. Se admiten consultas de lenguas naturales

Por ejemplo, _Cómo crear un esquema_ produce resultados de Experience League en _[!UICONTROL Aprendizaje]_:

![[!UICONTROL Búsqueda unificada] en la ayuda de CX Enterprise](../assets/unified-search-learning.png)

Los algoritmos de búsqueda muestran primero los registros más relevantes. El orden de los resultados depende de varios factores, como:

* Permisos de usuario para acceder a objetos
* Porcentaje de coincidencia
* Coincidencias exactas
* La sección _[!UICONTROL Resultados principales]_ muestra los 30 resultados principales.

Para restringir la búsqueda, haga clic en una de las siguientes opciones:

* **[!UICONTROL Todo el aprendizaje]**: Abre la búsqueda en Experience League.
* **[!UICONTROL Mostrar todo...]**: permite restringir y filtrar aún más los resultados.

## Características de [!UICONTROL búsqueda unificada]

Las siguientes funciones están disponibles en la búsqueda unificada.

| Función | Descripción |
| ------- | ------- |
| Compatibilidad con idiomas globales | La búsqueda global comprende las consultas y produce resultados para alemán, español, francés, italiano, japonés, coreano, portugués y chino. |
| Tipotolerancia | La búsqueda unificada proporciona una sólida tolerancia a errores tipográficos mediante algoritmos avanzados. Estos algoritmos calculan las ediciones y proporcionan los resultados adecuados. |
| Resaltado | La respuesta de búsqueda resalta la palabra clave coincidente de la consulta de búsqueda para que pueda encontrar fácilmente la sección y las palabras que coinciden con la consulta. El resaltado también funciona para palabras mal escritas. |
| Fragmentos | En la respuesta de búsqueda, puede ver un fragmento del resultado. Los fragmentos devuelven las palabras coincidentes y parte del contenido alrededor de las palabras clave coincidentes. |
| Detener palabras | Algunas palabras de uso común en inglés se definen como _palabras de detención_. Si se incluyen palabras de detención en la consulta de búsqueda, se les da menos peso. <br>Las palabras de detención incluyen: _a, y, y, son, como, en, ser, pero, por, por, por, si, en, es, no, no, de, o, tal, que, su, entonces, allí, estos, ellos, esto, a, era, voluntad, con_. <br>No se admiten palabras de detención en otros idiomas globales. |
| Consultas del lenguaje natural | Cuando busque un artículo de ayuda o un debate en las comunidades de Experience League, puede escribir su pregunta con lenguaje natural y obtener la respuesta. Búsqueda de ejemplo: &quot;¿Cómo se crea un esquema?&quot; |
| Búsqueda exacta entre comillas | Puede realizar una búsqueda exacta utilizando comillas en la consulta. No se realiza ninguna corrección de error tipográfico en las consultas de coincidencia exacta. Por ejemplo: &quot;Recorrido de Luma 2022&quot;. |
| Filtros | Puede aplicar filtros como _Tipo de objeto_ y otros filtros específicos de objeto en la ventana emergente de resultados de búsqueda completa. Cuando pulse Intro después de vincular la consulta de búsqueda, se abrirá una ventana emergente de página completa que incluye los filtros. |

{style="table-layout:auto"}

## ¿No lo encuentra?

Pruebe estas sugerencias:

* Introduzca un término de búsqueda más específico
* Revisar la ortografía
* Intente escribir el término de búsqueda completo
* Asegúrese de que dispone de los permisos para los objetos que busca

