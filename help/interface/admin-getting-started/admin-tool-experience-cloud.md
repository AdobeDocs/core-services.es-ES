---
description: Obtenga información sobre la herramienta de administración de Experience Cloud para ver una lista de todos los usuarios de Experience Cloud que se puede ordenar y filtrar.
keywords: core services
seo-description: Obtenga información sobre la herramienta de administración de Experience Cloud para ver una lista de todos los usuarios de Experience Cloud que se puede ordenar y filtrar.
seo-title: Ver los detalles de usuarios y usuarios de Experience Cloud
solution: Experience Cloud
title: 'Ver los detalles de usuarios y usuarios de Experience Cloud '
translation-type: tm+mt
source-git-commit: 3595229c176bf4999ed149377adfeb55efc80071

---


# Herramienta de administración de Experience Cloud

La herramienta de administración de Experience Cloud permite a los administradores ver una lista ordenable y filtrable de todos los usuarios de Experience Cloud. Cada página de detalles del usuario contiene detalles importantes sobre el acceso al producto, las funciones y la información a la que accedió por última vez un usuario.  

1. Log in to <https://experience.adobe.com/>.

   ![](assets/admin-tool.png)

1. En la página de inicio de Experience Cloud, haga clic en Herramienta **[!UICONTROL de administración.]** (Como alternativa, en la dirección URL de la página principal puede reemplazar _la página principal_ por _admin._)

   Se abre la página [!UICONTROL Usuarios] .

## Página Usuarios

Esta página muestra una lista completa de los usuarios con acceso a Experience Cloud en su organización. Proporciona información sobre la asignación de derechos de la solución y el último inicio de sesión. Puede buscar, ordenar y filtrar las vistas personalizadas de la lista de usuarios.

![](assets/admin-tool-users.png)

| Elemento | Descripción |
|---|---|
| [!UICONTROL Nombre] | Nombre y Apellido del usuario. Puede ordenar esta columna de A a Z y de Z a A.  Haga clic en el nombre de un usuario para ver más detalles sobre el mismo. |
| [!UICONTROL Correo electrónico] | La dirección de correo electrónico asociada al usuario. La columna puede ordenarse A->Z, Z->A. |
| [!UICONTROL Tipo de ID] | Tipo de identidad de la cuenta del usuario. El filtro se puede aplicar para ver tipos de ID específicos. Consulte [Administrar tipos](https://helpx.adobe.com/enterprise/using/identity.html) de identidad para obtener más información. |
| [!UICONTROL Soluciones] | Resumen de las soluciones de Experience Cloud a las que puede acceder el usuario. Puede aplicar filtros a la lista desplegable de usuarios con acceso a la solución específico. |
| [!UICONTROL Último inicio de sesión] | Hora y fecha del inicio de sesión más reciente del usuario en Experience Cloud. Esta columna se puede ordenar por fechas ascendente o descendentes. <br> **** Importante: Los datos del último inicio de sesión no se conservan durante más de 30 días antes del valor de fecha, por lo que es posible que los usuarios no tengan información sobre el último inicio de sesión. [!UICONTROL A partir de (FECHA)] : los datos de inicio de sesión del usuario se conservan durante 365 días. Puede utilizar esta información para ver la actividad de inicio de sesión actual en Experience Cloud, pero no para realizar acciones en cuentas inactivas. Además, es posible que los usuarios creados recientemente no tengan el estado de último inicio de sesión. |

## Personalización de la vista de lista de usuarios

Puede buscar, ordenar o filtrar las columnas para personalizar la lista de usuarios.

* Buscar usuarios por nombre o correo electrónico. Las búsquedas coinciden con la cadena de texto que escriba.
* Ordenar la columna por valores ascendentes o descendentes. Esto se aplica a las columnas [!UICONTROL Nombre,] [!UICONTROL Correo electrónico,] y [!UICONTROL Último inicio de sesión] .
* Haga clic en el icono **[!UICONTROL Filtrar por]** para aplicar varios filtros a la lista de usuarios con criterios específicos. Cuando se aplican varias categorías de filtros, las búsquedas contienen la solución `AND` ID de dominio de correo electrónico TYPE `AND` .

| Elemento | Descripción |
|---------|----------|
| [!UICONTROL Filtro Dominio] de correo electrónico | Busque cadenas de caracteres en la columna Correo electrónico para reducir los resultados a uno o varios dominios. Agregue varios filtros presionando Intro después de cada término de búsqueda |
| [!UICONTROL Tipo] de ID, filtro | Elija entre los tipos de ID disponibles. Se pueden usar varios tipos de ID como filtro. |
| [!UICONTROL Filtro de solución] | Elija entre las soluciones disponibles. Los filtros de varias soluciones buscan resultados que contengan la Solución 1 `OR` Solución 2. |

## Ver detalles del usuario

En la página [!UICONTROL Usuarios] , para ver los detalles de un usuario, haga clic en el correo electrónico del usuario.

![](assets/admin-tool-user-details.png)

Una vista detallada de cada usuario muestra detalles importantes sobre el acceso a la solución del usuario, las funciones de administrador y del producto, y la información de último acceso.

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

## Lista detallada de acceso a productos

Esta sección muestra una lista completa de todos los miembros de perfiles de producto para el usuario.

| Elemento | Descripción |
|---------|----------|
| [!UICONTROL Producto] | Nombre del producto asociado al perfil de producto. |
| [!UICONTROL Instancia] | Nombre de la instancia (como empresa de inicio de sesión o inquilino) asociada con el producto y el perfil de producto. |
| [!UICONTROL Perfil del producto] | Nombre único del perfil de producto. |
| [!UICONTROL Asignado por grupo] | Nombre del grupo de usuarios que asocia al usuario a un perfil de producto. Los resultados en blanco indican que el usuario se asignó directamente al perfil de producto, no a través de un grupo. |
| [!UICONTROL Funciones del producto] | Asignación de funciones del usuario dentro del perfil de producto. Actualmente, esta información solo se aplica a perfiles de producto de Target. |
