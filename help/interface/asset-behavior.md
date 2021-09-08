---
description: Obtenga información sobre las reglas para el comportamiento de las carpetas compartidas al moverlas, eliminarlas y restaurarlas en Experience Cloud.
keywords: compartir recursos;Creative Cloud;servicios principales
solution: Experience Cloud
title: 'Comportamiento de archivos compartidos '
uuid: 86348401-f4b1-4efe-acd1-7e73a7030edf
feature: Assets
topic: Administración
role: Admin
level: Experienced
exl-id: 5ddcb2f0-b491-466d-b357-aeacbfcf0b8e
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: ht
source-wordcount: '569'
ht-degree: 100%

---

# Comportamiento de archivos compartidos

Reglas sobre cómo se comportan las carpetas compartidas cuando se mueven, eliminan o restauran.

>[!NOTE]
>
>Las carpetas y recursos compartidos de Experience Cloud se ven reflejados en el escritorio Creative Cloud en una relación de 1:1. Si un usuario de Experience Cloud cambia una carpeta (elimina, añade o deja de compartir), la acción se refleja en las versiones de escritorio y web de Creative Cloud. De este modo, si se deja de compartir una carpeta, la carpeta y los recursos se eliminarán del equipo local. Una vez que se deja de compartir, la carpeta y sus contenidos se mueven a la papelera de su equipo local, donde puede restaurarlos en su equipo.

## Carpeta no compartida en una carpeta compartida {#section_A9BAC1A244A246A984AC62660E61E0C0}

Si mueve una carpeta no compartida a una carpeta compartida:

![](assets/01_assets_move.png)

**Resultado**: Ambas carpetas se comparten.

## Carpeta compartida en una carpeta no compartida {#section_8BA83001DCEC4CF084B980C4A660F59A}

Si mueve una carpeta compartida a una carpeta no compartida.

![](assets/02_assets_move.png)

**Resultado**: La carpeta no compartida permanece sin compartir. La carpeta compartida permanece compartida.

## Contenido de una carpeta no compartida a una carpeta compartida {#section_2941ED0DC52E4573AC1AB4C22313DD8E}

El contenido de una carpeta no compartida se mueve a una carpeta compartida.

![](assets/03_assets_move.png)

**Resultado:** El contenido ahora se comparte y todos los colaboradores pueden verlo. El almacenamiento aumenta según el tamaño del contenido.

## Contenido compartido archivado y eliminado {#section_5210D5F4943A44D0BA675D8EB4EAE20F}

El contenido que reside en una carpeta compartida se archiva o elimina.

![](assets/04_assets_move.png)

**Resultado:** El contenido se archiva para el propietario de la carpeta. Los colaboradores que no son propietarios del contenido ya no pueden acceder a él.

## Contenido compartido propio a una carpeta no compartida {#section_3810A364B67E4B8C9CA244BC52BF91BB}

El contenido de una carpeta compartida suya se mueve a una carpeta no compartida.

![](assets/05_assets_move.png)

**Resultado:** El contenido ya no se comparte. Los colaboradores de la carpeta compartida ya no tendrán acceso al contenido.

## Contenido que no es de su propiedad a una carpeta no compartida {#section_310766EBF0DC4C0BB4AB3E8A4DAEBE07}

El contenido de una carpeta compartida de otra persona se mueve a una carpeta no compartida.

![](assets/06_assets_move.png)

**Resultado:** El contenido aparece en la carpeta no compartida y se elimina de la carpeta compartida. Los colaboradores de la carpeta compartida ya no tendrán acceso al contenido. El contenido se archiva para el propietario de la carpeta compartida.

Los propietarios y editores pueden mover el contenido que no es de su propiedad, pero los visualizadores no pueden. Si los propietarios y editores mueven contenido, este no estará disponible en ninguna carpeta compartida para ningún usuario.

## Carpeta propia archivada o eliminada {#section_B314B13512A5409C87C49DFDB7602E14}

Puede archivar (a través de la Web) o eliminar (a través del escritorio) una carpeta compartida suya.

![](assets/07_assets_move.png)

**Resultado:** La carpeta no se comparte y, a continuación, se archiva. Los colaboradores ya no tienen acceso a la carpeta.

## Carpeta compartida en otra carpeta compartida {#section_0A3F203D048D4D1586E9850DC92C51E9}

Una carpeta compartida suya se mueve a otra carpeta compartida suya o de otra persona.

![](assets/09_assets_move.png)

**Resultado:** A medida que la carpeta se mueve a la carpeta 2, esta se comparte con los nuevos colaboradores.

## Contenido compartido en otra carpeta compartida {#section_69F6C312792A4CD2831BD14A340F850E}

El contenido de una carpeta compartida se mueve a otra carpeta compartida.

![](assets/11_assets_move.png)

**Resultado:** El contenido aparece en la carpeta 2 y ahora se comparte con los nuevos colaboradores. El contenido se elimina de la carpeta 1 y el propietario lo ve como archivado, mientras que los demás colaboradores ya no tienen acceso a él.

## Contenido restaurado del archivo {#section_DEA990B3581741F89FBB81D18C2AB449}

Se restaura el contenido de un archivo que pertenecía a una carpeta compartida. El contenido era suyo en el momento en que se archivó.

![](assets/12_assets_move.png)

**Resultado:** el contenido se restaura a la carpeta compartida y todos los colaboradores pueden acceder a él de nuevo. Si la carpeta compartida ya no existe, el contenido se coloca en una copia no compartida de sus carpetas principales originales.
