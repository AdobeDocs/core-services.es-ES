---
description: Obtenga información sobre la herramienta de administración de Experience Cloud para vista de una lista ordenable y filtrable de todos los usuarios de Experience Cloud.
keywords: core services
seo-description: Obtenga información sobre la herramienta de administración de Experience Cloud para vista de una lista ordenable y filtrable de todos los usuarios de Experience Cloud.
seo-title: Vista de los usuarios de Experience Cloud y los detalles del usuario
solution: Experience Cloud
title: 'Vista de los usuarios de Experience Cloud y los detalles del usuario '
index: true
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Vista de usuarios de Experience Cloud en la herramienta de administración

Los administradores pueden realizar la vista de una lista ordenable y filtrable de todos los usuarios de Experience Cloud y sus detalles en la herramienta de administración. Los detalles del usuario incluyen el acceso al producto, las funciones y la información a la que accedió por última vez. (**Nota:** La administración de usuarios y productos está configurada en la Consola [de administración](admin-getting-started.md)).

1. Iniciar sesión en `https://experience.adobe.com/.`

   ![](assets/admin-tool.png)

1. En la página de inicio de Experience Cloud, haga clic en Herramienta **[!UICONTROL de administración.]**

   (Como alternativa, en la URL de página de inicio puede reemplazar _inicio_ por _admin._)

   Se abre la página [!UICONTROL Usuarios] .

## Página Usuarios

Esta página muestra la lista completa de usuarios con acceso a Experience Cloud en su organización. Proporciona información sobre la asignación de derechos de la solución y el último inicio de sesión. Puede buscar, ordenar y filtrar vistas personalizadas de la lista del usuario.

![](assets/admin-tool-users.png)

| Elemento | Descripción |
|---|---|
| [!UICONTROL Nombre] | Nombre y Apellido del usuario. Puede ordenar esta columna de A a Z y de Z a A.  Haga clic en el nombre de un usuario para ver más detalles sobre el mismo. |
| [!UICONTROL Correo electrónico] | La dirección de correo electrónico asociada al usuario. La columna puede ordenarse A->Z, Z->A. |
| [!UICONTROL Tipo de ID] | Tipo de identidad de la cuenta del usuario. El filtro se puede aplicar a tipos de ID específicos de vista. Consulte [Administrar tipos](https://helpx.adobe.com/enterprise/using/identity.html) de identidad para obtener más información. |
| [!UICONTROL Soluciones] | Resumen de las soluciones de Experience Cloud a las que puede acceder el usuario. Puede aplicar filtros para reducir la lista de los usuarios con acceso específico a la solución. |
| [!UICONTROL Último inicio de sesión] | Hora y fecha del inicio de sesión más reciente del usuario en Experience Cloud. Esta columna se puede ordenar por fechas ascendente o descendentes. <br> **Importante:** A partir del 13 de enero de 2020, los datos de inicio de sesión de un usuario se conservarán durante 365 días. Esta información está pensada para mostrar la actividad de inicio de sesión actual en Experience Cloud y no para recomendar que se realicen acciones en cuentas inactivas antes del 13 de enero de 2020. |

## Personalización de la vista de lista del usuario

Puede buscar, ordenar o filtrar las columnas para personalizar la lista del usuario.

* Buscar usuarios por nombre o correo electrónico. Las búsquedas coinciden con la cadena de texto que escriba.
* Ordenar la columna por valores ascendentes o descendentes. Esto se aplica a las columnas [!UICONTROL Nombre,] [!UICONTROL Correo electrónico,] y [!UICONTROL Último inicio de sesión] .
* Haga clic en el icono **[!UICONTROL Filtrar por]** para aplicar varios filtros a los usuarios de lista con criterios específicos. Cuando se aplican varias categorías de filtro, las búsquedas contienen una solución de tipo de `AND` ID de dominio de correo electrónico `AND` .

| Elemento | Descripción |
|---------|----------|
| [!UICONTROL Filtro Dominio] de correo electrónico | Busque cadenas de caracteres en la columna Correo electrónico para reducir los resultados a uno o varios dominios. Añadir varios filtros pulsando Intro después de cada término de búsqueda |
| [!UICONTROL Tipo] de ID, filtro | Elija entre los tipos de ID disponibles. Se pueden usar varios tipos de ID como filtro. |
| [!UICONTROL Filtro de solución] | Elija entre las soluciones disponibles. Varios filtros de soluciones buscan resultados que contengan la Solución 1 `OR` Solución 2. |

## Detalles del usuario de la Vista

En la página [!UICONTROL Usuarios] , para vista de los detalles de un usuario, haga clic en el correo electrónico del usuario.

![](assets/admin-tool-user-details.png)

Una vista detallada de cada usuario muestra detalles importantes sobre el acceso a la solución del usuario, las funciones de administración y del producto y la información de acceso más reciente.

## Acerca de la sección

Esta sección muestra un resumen de la cuenta de usuario, que incluye:

* Avatar del usuario y distintivo del administrador del sistema (si corresponde)
* Nombre
* Correo electrónico
* Nombre de usuario (es posible que las cuentas de Federated ID tengan nombres de usuario diferentes a los de la dirección de correo electrónico)
* [Tipo de ID](https://helpx.adobe.com/enterprise/using/identity.html)
* País
* Último inicio de sesión

## Resumen de soluciones

Esta sección muestra un resumen de las soluciones de Experience Cloud a las que el usuario puede acceder. Incluye la función administrativa del producto cuando corresponde

## Lista detallada de acceso al producto

Esta sección muestra una lista completa de todos los miembros de perfiles de producto para el usuario.

| Elemento | Descripción |
|---------|----------|
| [!UICONTROL Producto] | Nombre del producto asociado con el perfil del producto. |
| [!UICONTROL Instancia] | Nombre de la instancia (como la compañía de inicio de sesión o el inquilino) asociada al perfil de producto y producto. |
| [!UICONTROL Perfil del producto] | Nombre único del perfil del producto. |
| [!UICONTROL Asignado por grupo] | Nombre del grupo de usuarios que asocia al usuario a un perfil de productos. Los resultados en blanco indican que el usuario se asignó directamente al perfil del producto, no a través de un grupo. |
| [!UICONTROL Funciones del producto] | Asignación de funciones del usuario dentro del perfil del producto. Actualmente, esta información solo se aplica a perfiles de productos de Adobe Destinatario. |
