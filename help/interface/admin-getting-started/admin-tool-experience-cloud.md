---
description: Obtenga información sobre la herramienta de administración de Experience Cloud para ver una lista ordenable y filtrable de todos los usuarios de Experience Cloud.
keywords: core services
seo-description: Obtenga información sobre la herramienta de administración de Experience Cloud para ver una lista ordenable y filtrable de todos los usuarios de Experience Cloud.
seo-title: Vea los usuarios de Experience Cloud y sus detalles
solution: Experience Cloud
title: 'Vea los usuarios de Experience Cloud y sus detalles '
index: true
translation-type: ht
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e
workflow-type: ht
source-wordcount: '693'
ht-degree: 100%

---


# Vea los usuarios de Experience Cloud en la herramienta de administración

Los administradores pueden ver una lista de los usuarios de Experience Cloud que pueden ordenar y filtrar y sus detalles en la herramienta de administración. Los detalles del usuario incluyen el acceso al producto, las funciones y la información a la que accedió por última vez. (**Nota:** La administración de usuarios y productos está configurada en [Admin Console](admin-getting-started.md)).

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
