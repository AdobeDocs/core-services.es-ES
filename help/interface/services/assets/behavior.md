---
description: Obtenga información sobre las reglas para el comportamiento de las carpetas compartidas al moverlas, eliminarlas y restaurarlas en CX Enterprise.
keywords: compartir recursos;Creative Cloud;servicios principales
solution: Experience Cloud
title: Comportamiento de las carpetas compartidas
uuid: 86348401-f4b1-4efe-acd1-7e73a7030edf
feature: Assets
topic: Administration
role: Admin
level: Experienced
exl-id: 5ddcb2f0-b491-466d-b357-aeacbfcf0b8e
TQID: https://experienceleague.adobe.com/sRgVt31HAxmjTMmMB0Kfs5fYEXKDjDu73hhAgfixu4o
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 627
ht-degree: 90%

---

# Comportamiento de archivos compartidos

Reglas sobre cómo se comportan las carpetas compartidas cuando se mueven, eliminan o restauran.

>[!NOTE]
>
>Las carpetas y recursos compartidos de CX Enterprise se reflejan en el escritorio de Creative Cloud en una relación de 1:1. Si un usuario de CX Enterprise cambia una carpeta (elimina, agrega o deja de compartir), la acción se refleja en el escritorio y en la web de Creative Cloud. De este modo, si se deja de compartir una carpeta, la carpeta y los recursos se eliminarán del equipo local. Una vez que se deja de compartir, la carpeta y sus contenidos se mueven a la papelera de su equipo local, donde puede restaurarlos en su equipo.

## Carpeta no compartida en una carpeta compartida

Si mueve una carpeta no compartida a una carpeta compartida:

![Carpeta no compartida en una carpeta compartida](../../assets/01_assets_move.png)

**Resultado**: ambas carpetas se comparten.

## Carpeta compartida en una carpeta no compartida

Si mueve una carpeta compartida a una carpeta no compartida.

![Carpeta compartida en una carpeta no compartida](../../assets/02_assets_move.png)

**Resultado**: La carpeta no compartida permanece sin compartir. La carpeta compartida permanece compartida.

## Contenido de una carpeta no compartida a una carpeta compartida

El contenido de una carpeta no compartida se mueve a una carpeta compartida.

![Contenido de una carpeta no compartida a una carpeta compartida](../../assets/03_assets_move.png)

**Resultado:** El contenido ahora se comparte y todos los colaboradores pueden verlo. El almacenamiento aumenta según el tamaño del contenido.

## Contenido compartido archivado y eliminado

El contenido que reside en una carpeta compartida se archiva o elimina.

![Contenido compartido archivado y eliminado](../../assets/04_assets_move.png)

**Resultado:** El contenido se archiva para el propietario de la carpeta. Los colaboradores que no son propietarios del contenido ya no pueden acceder a él.

## Contenido compartido propio a una carpeta no compartida

El contenido de una carpeta compartida suya se mueve a una carpeta no compartida.

![Contenido compartido propio a una carpeta no compartida](../../assets/05_assets_move.png)

**Resultado:** El contenido ya no se comparte. Los colaboradores de la carpeta compartida ya no tendrán acceso al contenido.

## Contenido que no es de su propiedad a una carpeta no compartida

El contenido de una carpeta compartida de otra persona se mueve a una carpeta no compartida.

![Contenido que no es de su propiedad a una carpeta no compartida](../../assets/06_assets_move.png)

**Resultado:** El contenido aparece en la carpeta no compartida y se elimina de la carpeta compartida. Los colaboradores de la carpeta compartida ya no tendrán acceso al contenido. El contenido se archiva para el propietario de la carpeta compartida.

Los propietarios y editores pueden mover el contenido que no es de su propiedad, pero los visualizadores no pueden. Si los propietarios y editores mueven contenido, este no estará disponible en ninguna carpeta compartida para ningún usuario.

## Carpeta propia archivada o eliminada

Puede archivar (a través de la Web) o eliminar (a través del escritorio) una carpeta compartida suya.

![Carpeta propia archivada o eliminada](../../assets/07_assets_move.png)

**Resultado:** La carpeta no se comparte y, a continuación, se archiva. Los colaboradores ya no tienen acceso a la carpeta.

## Carpeta compartida en otra carpeta compartida

Una carpeta compartida suya se mueve a otra carpeta compartida suya o de otra persona.

![Carpeta compartida en otra carpeta compartida](../../assets/09_assets_move.png)

**Resultado:** a medida que la carpeta se mueve a la carpeta 2, esta se comparte con los nuevos colaboradores.

## Contenido compartido en otra carpeta compartida

El contenido de una carpeta compartida se mueve a otra carpeta compartida.

![Contenido compartido en otra carpeta compartida](../../assets/11_assets_move.png)

**Resultado:** El contenido aparece en la carpeta 2 y ahora se comparte con los nuevos colaboradores. El contenido se elimina de la carpeta 1 y el propietario lo ve como archivado, mientras que los demás colaboradores ya no tienen acceso a él.

## Contenido restaurado del archivo

Se restaura el contenido de un archivo que pertenecía a una carpeta compartida. El contenido era suyo en el momento en que se archivó.

![Contenido restaurado del archivo](../../assets/12_assets_move.png)

**Resultado:** el contenido se restaura a la carpeta compartida y todos los colaboradores pueden acceder a él de nuevo. Si la carpeta compartida ya no existe, el contenido se coloca en una copia no compartida de sus carpetas principales originales.
