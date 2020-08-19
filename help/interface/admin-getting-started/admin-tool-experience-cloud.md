---
description: Obtenga información sobre la Herramienta de administración de Experience Cloud para vista de una lista ordenable y filtrable de todos los usuarios y políticas de Experience Cloud.
keywords: core services
seo-description: Obtenga información sobre la Herramienta de administración de Experience Cloud para vista de una lista ordenable y filtrable de todos los usuarios y políticas de Experience Cloud.
seo-title: Vea los usuarios de Experience Cloud y sus detalles
solution: Experience Cloud
title: 'Vea los usuarios de Experience Cloud y sus detalles '
index: true
translation-type: tm+mt
source-git-commit: 7b34db76f3091c895863ebe771fb3c0baa05b13e
workflow-type: tm+mt
source-wordcount: '1271'
ht-degree: 53%

---


# Directivas y usuarios del Experience Cloud de vista en la herramienta de administración

Los administradores pueden vista una lista ordenable y filtrable de todos los usuarios y políticas de Experience Cloud con los detalles de la herramienta de administración. Los detalles del usuario incluyen el acceso al producto, las funciones y la información a la que accedió por última vez. Los detalles de la directiva incluyen la lista de usuario, grupo, desarrollador, integración y administrador de una directiva (perfil de producto), así como información detallada sobre los permisos y recursos de la directiva. (**Note:** User and product management is configured in the [Admin Console](admin-getting-started.md).)

1. Iniciar sesión en `https://experience.adobe.com/.`

   ![](assets/admin-tool.png)

1. En la página de inicio de Experience Cloud, haga clic en **[!UICONTROL Herramienta de administración.]**

   (Como alternativa, en la URL de página de inicio puede reemplazar _inicio_ por _admin_).

   Se abre la página [!UICONTROL Usuarios].

## Página Usuarios

Esta página muestra la lista completa de usuarios con acceso a Experience Cloud en su organización. Proporciona información sobre la asignación de derechos de la solución y el último inicio de sesión. Puede buscar, ordenar y filtrar vistas personalizadas de la lista del usuario.

![](assets/admin-tool-users.png)

| Elemento | Descripción |
|---|---|
| [!UICONTROL Nombre] | Nombre y apellido del usuario. Puede ordenar esta columna de la A a Z y de la Z a A. Haga clic en el nombre de un usuario para ver más detalles sobre el mismo. |
| [!UICONTROL Correo electrónico] | La dirección de correo electrónico asociada al usuario. La columna puede ordenarse de la A a la Z y de la Z a la A. |
| [!UICONTROL Tipo de ID] | Tipo de identidad de la cuenta del usuario. El filtro se puede aplicar a tipos de ID específicos de la vista. Consulte [Administrar tipos de identidad](https://helpx.adobe.com/es/enterprise/using/identity.html) para obtener más información. |
| [!UICONTROL Soluciones] | Resumen de las soluciones de Experience Cloud a las que puede acceder el usuario. Puede aplicar filtros para reducir la lista de los usuarios con acceso específico a la solución. |
| [!UICONTROL Último inicio de sesión] | Hora y fecha del inicio de sesión más reciente del usuario en Experience Cloud. Esta columna se puede ordenar por fechas en orden ascendente o descendente. <br> **Importante:** A partir del 13 de enero de 2020, los datos de inicio de sesión de un usuario se conservarán durante 365 días. Esta información está pensada para mostrar la actividad de inicio de sesión actual en Experience Cloud y no para recomendar que se realicen acciones en cuentas inactivas antes del 13 de enero de 2020. |

## Personalización de la vista de lista del usuario

Puede buscar, ordenar o filtrar las columnas para personalizar la lista del usuario.

* Busque usuarios por nombre o correo electrónico. Las búsquedas coinciden con la cadena de texto que escriba.
* Ordene la columna por valores ascendentes o descendentes. Esto se aplica a las columnas [!UICONTROL Nombre,] [!UICONTROL Correo electrónico] y [!UICONTROL Último inicio de sesión].
* Haga clic en el icono **[!UICONTROL Filtrar por]** para aplicar varios filtros a los usuarios de lista con criterios específicos. Cuando se aplican varias categorías de filtro, las búsquedas contienen Dominio de correo electrónico `AND` TIPO DE ID `AND` Solución.

| Elemento | Descripción |
|---------|----------|
| Filtro [!UICONTROL Dominio de correo electrónico] | Busque cadenas de caracteres en la columna Correo electrónico para reducir los resultados a uno o varios dominios. Añada varios filtros pulsando Intro después de cada término de búsqueda. |
| Filtro [!UICONTROL Tipo de ID] | Elija entre los tipos de ID disponibles. Se pueden usar varios tipos de ID como filtro. |
| Filtro [!UICONTROL Solución] | Elija entre las soluciones disponibles. Varios filtros de soluciones buscan resultados que contengan Solución 1 `OR` Solución 2. |

## Ver detalles del usuario

En la página [!UICONTROL Usuarios], para ver los detalles de un usuario, haga clic en el correo electrónico del usuario.

![](assets/admin-tool-user-details.png)

Una vista detallada de cada usuario muestra detalles importantes sobre el acceso a la solución del usuario, las funciones de administración y del producto y la información de acceso más reciente.

## Sección Acerca de

Esta sección muestra un resumen de la cuenta de usuario, que incluye:

* Avatar del usuario y distintivo del administrador del sistema (si corresponde)
* Nombre
* Correo electrónico
* Nombre de usuario (es posible que las cuentas de Federated ID tengan nombres de usuario diferentes de las direcciones de correo electrónico)
* [Tipo de ID](https://helpx.adobe.com/es/enterprise/using/identity.html)
* País
* Último inicio de sesión

## Resumen de soluciones

Esta sección muestra un resumen de las soluciones de Experience Cloud a las que el usuario puede acceder. Incluye la función administrativa del producto cuando corresponde.

## Lista detallada de acceso al producto

Esta sección muestra una lista completa de todos los miembros de perfiles de producto para el usuario.

| Elemento | Descripción |
|---------|----------|
| [!UICONTROL Producto] | Nombre del producto asociado con el perfil del producto. |
| [!UICONTROL Instancia] | Nombre de la instancia (como la compañía de inicio de sesión o el inquilino) asociados al producto y al perfil del producto. |
| [!UICONTROL Perfil del producto] | Nombre único del perfil del producto. |
| [!UICONTROL Grupo que lo asigna] | Nombre del grupo de usuarios que asocia al usuario a un perfil de productos. Los resultados en blanco indican que el usuario se asignó directamente al perfil del producto, no a través de un grupo. |
| [!UICONTROL Funciones del producto] | Asignación de funciones del usuario dentro del perfil del producto. Actualmente, esta información solo se aplica a perfiles de productos de Adobe Target. |

## Página Directivas

Esta página muestra la lista completa de las directivas de Experience Cloud en su organización. Proporciona información sobre productos, instancias, usuarios y desarrolladores. Puede buscar, ordenar y filtrar vistas personalizadas de la lista de directivas.

| Elemento | Descripción |
|---|---|
| [!UICONTROL Perfil del producto] | Nombre del perfil del producto. La columna puede ordenarse A->Z, Z->A. Haga clic en el nombre de un perfil de producto para ver más detalles sobre la directiva. |
| [!UICONTROL Producto] | El producto asociado con el perfil del producto. La columna puede ordenarse de la A a la Z y de la Z a la A. |
| [!UICONTROL Instancia] | La instancia (por ejemplo, compañía de inicio de sesión o inquilino) asociada con el perfil del producto. Los productos que no tengan instancias únicas o inquilinos mostrarán un &quot; - &quot; para el valor. La columna puede ordenarse de la A a la Z y de la Z a la A. |
| [!UICONTROL Número de usuarios] | Recuento único de usuarios asociados con el perfil del producto, incluida la asignación directa y la asignación de grupos. Las columnas pueden ordenarse de menor a mayor o de mayor a menor. |
| [!UICONTROL Número de desarrolladores] | Recuento de funciones de desarrollador asociadas con el perfil del producto. Las columnas pueden ordenarse de menor a mayor o de mayor a menor. |

## Personalizar la vista de lista de políticas

Puede buscar, ordenar o filtrar las columnas para personalizar la lista de políticas.

* Busque perfiles de producto por nombre. Las búsquedas coinciden con la cadena de texto que escriba.
* Ordene la columna por valores ascendentes o descendentes. Esto se aplica a Perfil [!UICONTROL de productos,] [!UICONTROL Producto,] [!UICONTROL Instancia,] [!UICONTROL Número de usuarios,] y [!UICONTROL Número de programadores,] Columnas.
* Click the **[!UICONTROL Filter By]** icon to apply multiple filters to list product profiles with specific criteria. Cuando se aplican varias categorías de filtro, las búsquedas contienen Grupos asociados `AND` a la solución Instancia `AND` .

| Elemento | Descripción |
|---------|----------|
| [!UICONTROL Filtro de instancia] | Busque cadenas de caracteres en la columna de instancia para reducir los resultados a una o varias instancias. Añada varios filtros pulsando Intro después de cada término de búsqueda. |
| Filtro [!UICONTROL Solución] | Elija entre las soluciones disponibles. Varios filtros de soluciones buscan resultados que contengan Solución 1 `OR` Solución 2. |

## Detalles de la política de vista

En la página [!UICONTROL Directivas] , para vista de los detalles de una política, haga clic en el nombre del perfil del producto.

Una vista detallada de cada perfil del producto muestra detalles importantes sobre los temas del perfil del producto (usuarios, grupos, etc.), y los permisos y recursos habilitados por el perfil del producto.  Los detalles del perfil del producto se pueden exportar a archivos CSV.  La opción [!UICONTROL Exportar CSV] producirá 2 archivos CSV: Detalles del asunto (usuarios, grupos de usuarios, desarrolladores, integraciones, administradores) y elementos de permisos y recursos.

## Sección de resumen

Esta sección muestra un resumen del perfil del producto, que incluye:

* Nombre del perfil del producto
* Número de usuarios
* Número de desarrolladores
* Número de integraciones
* Productos asociados
* Instancia


## Lista detallada del asunto

Esta sección muestra una lista completa de todos los usuarios, grupos de usuarios, desarrolladores, integraciones y administradores asignados al perfil del producto.

| Tabulación | Descripción |
|---------|----------|
| [!UICONTROL Usuarios] | Lista de usuarios incluidos en el perfil del producto. La asociación de grupos de usuarios aparecerá en la columna [!UICONTROL Asignado por grupo] . |
| [!UICONTROL Grupos de usuarios] | Lista de los grupos de usuarios asociados con el perfil del producto. |
| [!UICONTROL Desarrolladores] | Lista de desarrolladores asociados con el perfil del producto. |
| [!UICONTROL Integraciones] | Lista de integraciones asociadas con el perfil del producto. |
| [!UICONTROL Administradores] | Lista de los administradores asociados con el perfil del producto. |

## Listas detalladas de permisos y recursos

Esta sección muestra una lista completa de los permisos y recursos disponibles para el perfil del producto. Los permisos y recursos que se han incluido en el perfil del producto se han marcado con un &quot;✔&quot;.  Las listas de permisos y recursos se han clasificado en fichas y columnas para facilitar la visualización.  Las fichas y las columnas muestran la lista de las secciones que se aplican al producto actual.

