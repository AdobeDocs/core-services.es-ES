---
source-git-commit: 58ccef353b492b1c2adfbb8c2471e1f92263e6e4
translation-type: tm+mt

---
# Instrucciones

**Nota: Esta página (o cualquier página readme.md) no se publicará en la documentación de cliente**

## TOC

+ `TOC.md` en la raíz de la guía del usuario proporciona los temas contenidos en la guía para esta solución a la organización.
+ Cada guía del usuario tendrá su propio `TOC.md`, en el cual puede ordenar todas las páginas o temas según sea necesario.
+ La primera página de todas las guías del usuario es `overview.md`.

## Guía de usuario

+ La introducción a la guía del usuario se llama `overview.md`
+ Cada tema de la guía del usuario tiene su propio directorio.
   + Si hay un tema en la guía llamado *Implementación*, el directorio correspondiente es `/implementation`
+ Todos los recursos de imagen se almacenan en `/assets` la base de la guía del usuario.
   + Todas las imágenes del directorio `/assets` se localizarán.
   + Las imágenes del directorio `/no-localize` no se localizarán. Esto se puede utilizar para asegurar que, en versiones localizadas, los recursos específicos no se reproducen de forma innecesaria.

## Metadatos del nivel de guía del usuario

+ Los metadatos que describen la guía del usuario se almacenan en `TOC.md`. Esto incluye:
   + product: nombre de producto/capacidad.
   + cloud: nube a la que pertenece este producto.
   + audience: audiencia o arquetipo a la que se dirige la guía.
   + user-guide: nombre de la guía del usuario.

## Metadatos de nivel de página

+ Los metadatos necesarios para describir un documento se almacenan como parte de cada página individual. Esto incluye:
   + title: título de la página.
   + description: descripción de la página.
   + seo-title: título alternativo seo.
   + seo-description: título alternativo para propósitos de SEO.
   + short-title: (campo opcional).
   + index (sí/no): la plataforma de búsqueda de Adobe indexará la página.
   + translate (sí/no): la página se localizará.
   + version: se utiliza principalmente para AEM y Campaign para denotar la versión del producto.
   + private-feature-pack: se usa principalmente para AEM.
   + beta: ¿este producto está en fase beta?
   + redirect: se puede utilizar para crear una referencia a una página nueva si es necesario.
   + doc-type: reference (por defecto) / troubleshooting / developer / tutorial / kb / whitepaper.

## Más información

Para obtener más instrucciones de publicación, guías de estilo, muestras y otros recursos, visite el [Repositorio de documentación de colaboración](https://git.corp.adobe.com/AdobeDocs/collaborative-doc-instructions)
