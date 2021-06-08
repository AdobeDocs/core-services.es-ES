---
description: Consideraciones y prácticas recomendadas con respecto a la información de identificación personal (PII) cargada y utilizada en Adobe Experience Cloud.
keywords: Atributos del cliente;servicios principales
solution: Experience Cloud
title: 'Consideraciones de privacidad sobre atributos de cliente '
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
feature: 'Atributos del cliente '
topic: Administración
role: Administrator
level: Experienced
exl-id: 27c026ff-198b-4f49-9718-f25f77a9e716
source-git-commit: c7ed1324015beb7ebcf7a4ee21b05601e36e608f
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 84%

---

# Consideraciones de privacidad sobre atributos de cliente

Consideraciones y prácticas recomendadas con respecto a información de identificación personal (PII) cargada y utilizada en Adobe Experience Cloud.

* Nombre y apellidos
* Domicilio u otra dirección física
* Correo electrónico Dirección
* Número de teléfono
* Número de seguridad social
* Otro identificador que permite el contacto físico o en línea de un individuo. (Varía por ubicación. Verifique y cumpla con las leyes y regulaciones locales relacionadas con la privacidad y PII para todos los lugares donde usted lleve a cabo su actividad comercial).

Adobe proporciona herramientas que permiten a los anunciantes recopilar información sobre el comportamiento de los consumidores que visitan sus sitios o utilizan sus aplicaciones. Adobe también proporciona herramientas que permiten a los anunciantes mejorar esta información con registros de clientes externos o sin conexión que el anunciante pueda tener en otros sistemas de administración de la información.

Un motivo común por el cuales los anunciantes hacen esto es para mejorar la información disponible cuando toman decisiones de publicidad y marketing adecuada para el cliente. Adobe Analytics y Target permiten a los anunciantes cargar información de identificación personal (PII), como direcciones de correo electrónico, solo después de haber pasado el hash para que sea imposible utilizarla para ponerse en contacto con el usuario. La información con hash puede seguir utilizándose para realizar análisis y para marketing. Como recordatorio, Adobe prohíbe a los anunciantes enviar información personal confidencial a Adobe, como registros médicos, información de cuentas financieras e información sobre menores.

Adobe es consciente de que estos tipos de decisiones de marketing y publicidad pueden tener implicaciones para la privacidad del consumidor, por lo que Adobe ha incorporado controles de privacidad para ayudar a los anunciantes a satisfacer las expectativas de sus consumidores. Adobe recomienda que sus anunciantes consideren cuidadosamente qué información es apropiada para usar con fines de marketing y en qué circunstancias el anunciante tiene permiso para usar esa información.

## Prácticas recomendadas

Al cargar PII en Adobe Analytics o Adobe Target, Adobe recomienda que el cliente introduzca hash en PII antes de cargarlo en Adobe. La información con hash puede seguir utilizándose para realizar análisis y para marketing. Como recordatorio, Adobe prohíbe a los anunciantes enviar información personal confidencial a Adobe Analytics y Adobe Target, como registros médicos, información de cuentas financieras e información sobre menores.

Adobe recomienda que sus anunciantes consideren cuidadosamente qué información es apropiada para usar con fines de marketing y en qué circunstancias el anunciante tiene permiso para usar esa información.

Dado que la legislación respecto a la privacidad de los consumidores sigue en constante cambio, Adobe recomienda que los anunciantes respeten tres principios comunes:

1. Haga lo que diga (en su política de privacidad).
1. Diga lo que hace (en su política de privacidad).
1. No sorprenda a sus consumidores.

Teniendo en cuenta estas expectativas, Adobe recomienda que cuando un anunciante asocie actividades de exploración a PII, el proporcione avisos o mensajes personalizados que indiquen que el consumidor está autenticado. Un ejemplo de esto es incluir un saludo en el encabezado del sitio web. Adobe también recomienda que los anunciantes describan en su política de privacidad qué tipo de información de navegación asocia con PII y en qué circunstancias la información de navegación está asociada con PII. Por último, Adobe recomienda encarecidamente que los anunciantes revisen las opciones de exclusión que proporcionan a sus consumidores para que entiendan si pueden utilizar información de perfil no autenticada tras la exclusión y cómo pueden hacerlo.
