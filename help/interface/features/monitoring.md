---
title: Monitorización del uso de IA agente
description: Obtenga información sobre los paneles para la monitorización del uso de IA en CX Enterprise. Rastree la adopción, revise las conversaciones y los comentarios y administre los créditos de IA para el uso, la calidad y la visibilidad de los costes.
solution: Experience Cloud, Experience Platform
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
autotag-review: '2026-05-27T16:30:16.764Z'
TQID: 'https://experienceleague.adobe.com/J74yr0gGkFu1bzTmMvhrQ8TNaRX6nRjWY9WAwd3uydk'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
  - id: e1971122-7081-4556-9222-8a31bd71800c
feature_v2:
  - id: f84b2906-3ce9-4ef0-86f6-cda249273937
subfeature_v2:
  - id: cda95149-19e1-4cfa-a57e-751283a32378
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
source-git-commit: 19922aed1ca7f9beb0229cea90e6f68abda0d217
workflow-type: tm+mt
source-wordcount: 882
ht-degree: 2%

---

# Paneles de monitorización de IA automática

El tablero de monitorización de la inteligencia artificial aplicada a la agencia proporciona a los miembros del Centro de excelencia (COE) y a otras partes interesadas en la gobernanza visibilidad del uso y la adopción de la IA auténtica. Puede ver las tendencias de los períodos de 7 o 30 días para ver quién usa [!DNL AI Assistant] u otras superficies de conversación (como [Adobe Marketing Agent for Microsoft 365 Copilot](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/agents/ama-ms)) para interactuar con [!DNL Experience Platform Agents], qué hace en esas interacciones y el valor que recibe. En conjunto, estas vistas le ayudan a guiar la adopción de agentes con datos en lugar de suposiciones.

El tablero de monitorización de inteligencia artificial aplicada a la agencia incluye las siguientes vistas:

| Panel de control | Objetivo |
| --- | --- |
| **Información general** | Métricas agregadas entre usuarios, conversaciones, comentarios y consumo de crédito |
| **Usuarios** | Frecuencia de uso, distribución y participación del usuario |
| **Comentarios** | Señales sobre calidad de respuesta y satisfacción del usuario |
| **Créditos de IA** | Tendencias del consumo de crédito y saldo restante |

Los agentes con ámbito para la supervisión del uso se enumeran en [agentes de IA en aplicaciones empresariales de CX existentes](agentic-ai.md#existing-apps-table) en la [inteligencia artificial aplicada a agentes en Adobe CX Enterprise](agentic-ai.md).

[Ver vídeo introductorio](https://video.tv.adobe.com/v/3491864?learn=on)

## Habilitación de permisos de tablero (administradores) {#permissions}

Conceda acceso al panel en [!DNL Adobe Experience Platform] al actualizar el perfil de producto o la función para cada usuario autorizado. La característica [!UICONTROL Supervisión] se muestra a los usuarios en la página de inicio de CX Enterprise después de habilitar los permisos.

1. Vaya a [!DNL Experience Platform] **Administración** > **Permisos**.

1. Abra el perfil de producto o la función que desee actualizar.

   ![Habilitar permisos de tablero](../features/assets/dashboards-permissions.png)

1. En los permisos de **[!UICONTROL Asistente de IA]**, haga clic en **[!UICONTROL Agregar recurso]** y, a continuación, habilite **[!UICONTROL Ver tablero de uso del Asistente de IA]**.

   Este permiso concede acceso a los paneles de monitorización de uso de inteligencia artificial aplicada a la agencia.

1. En **[!UICONTROL Permisos de paneles]**, configure el acceso a los paneles en función de las responsabilidades de cada usuario.

   ![Habilitar permisos de tablero](../features/assets/dashboards-add-resource.png)

   Permisos recomendados para usuarios de gobernanza autorizados:

   * **[!UICONTROL Ver tablero de uso de licencias]**
   * **[!UICONTROL Ver paneles estándar]**
   * **[!UICONTROL Exportar datos de panel]** (opcional; solo para usuarios de administración aprobados)

   Permisos adicionales que puede conceder cuando sea necesario:

   * **[!UICONTROL Administrar paneles personalizados]**
   * **[!UICONTROL Ver paneles personalizados]**
   * **[!UICONTROL Administrar paneles estándar]**

1. Para ver los paneles, vuelva al inicio de CX Enterprise y haga clic en **[!UICONTROL Supervisión]**.

![Panel de monitorización de inteligencia artificial aplicada a la agencia](../features/assets/monitoring.png)

## Panel de información general

El panel Información general es el lugar central para las métricas de adopción y participación en toda la organización. Conecta las tendencias de alto nivel con un análisis más profundo. Desde cualquier métrica, puede profundizar en conversaciones individuales para ver qué impulsa los números.

### Métricas en el tablero Información general

* **Indicadores a lo largo del tiempo:** Tendencias generales de crecimiento y adopción de uso.
* **Usuarios activos y conversaciones:** Cantidad de usuarios que interactúan con [!DNL Experience Platform Agents].
* **Promedio de mensajes por conversación:** Profundidad de participación por conversación.
* **Comentarios:** Distribución de comentarios de usuarios con miniaturas hacia arriba y miniaturas hacia abajo (solo para [!DNL AI Assistant] interacciones).

[Ver vídeo](https://video.tv.adobe.com/v/3491865?learn=on)

### Reproducción de conversación

La reproducción de la conversación muestra interacciones individuales, no solo acumulaciones. Puede analizar los patrones en muchas conversaciones y pasar de tendencias de alto nivel a una conversación específica.

* **Historial de mensajes y respuestas:** El mensaje del usuario y las respuestas entregadas.
* **Señales de comentarios:** Interacciones que los usuarios marcaron con los pulgares hacia arriba o hacia abajo para identificar fricciones, bloqueadores o necesidades de habilitación. Esta información ayuda a su organización a mejorar la relevancia rápida y ayuda a Adobe a mejorar la calidad de la respuesta con el paso del tiempo.

[Ver vídeo](https://video.tv.adobe.com/v/3491866?learn=on)

## Panel de usuarios

El panel Usuarios muestra cómo la adopción y la participación de los agentes varían entre los usuarios a lo largo del tiempo. Se puede ver quién usa activamente [!DNL Experience Platform Agents], qué superficie usa y con qué frecuencia interactúa. Los administradores y los miembros del COE pueden explorar en profundidad la actividad y las conversaciones de cada usuario para comprender los patrones de participación y el comportamiento de uso.

### Métricas en el panel de usuarios

* **Tendencias de adopción y participación con el paso del tiempo:** Rastree cómo cambian los segmentos de usuario durante el período seleccionado. Los usuarios se clasifican como:
   * **Nuevo:** Primera actividad en el período seleccionado, sin actividad en los 12 meses anteriores.
   * **Repetir:** Actividad tanto en el período seleccionado como en el período anterior.
   * **Devolver:** Actividad en el período seleccionado, pero no en el período anterior.
   * **Inactiva:** No hay actividad en el período seleccionado, sino actividad en el período anterior.
* **Patrones de participación del usuario:** La frecuencia con la que los usuarios interactúan con los agentes y cómo cambia la participación con el paso del tiempo.
* **Actividad de conversación:** Número de conversaciones y mensajes por usuario.
* **Usuarios activos principales:** Usuarios y equipos altamente comprometidos que impulsan la adopción de agentes.

[Ver vídeo](https://video.tv.adobe.com/v/3491868?learn=on)

## Tablero de comentarios

El panel de comentarios muestra los comentarios del usuario enviados para las interacciones del agente. Puede ver qué conversaciones marcaron positiva o negativamente los usuarios e investigar las interacciones detrás de los comentarios. En los resúmenes de comentarios, explore en profundidad las conversaciones individuales para revisar los mensajes, las respuestas, los detalles del razonamiento y las notas de los comentarios.

### Métricas en el panel de comentarios

* **Los comentarios cambian con el tiempo:** Cómo cambian los comentarios de los usuarios con el paso del tiempo.
* **Pulgares arriba y pulgares abajo comentarios:** Señales de interacción positivas y negativas.
* **Categorías de comentarios:** Motivo detrás de cada pulgar hacia arriba y hacia abajo.
* **Historial de mensajes y respuestas:** Mensajes de usuario y respuestas asociadas con los comentarios enviados.
* **Notas y detalles de comentarios:** Contexto y comentarios adicionales de los usuarios durante el envío de comentarios.

[Ver vídeo](https://video.tv.adobe.com/v/3491878?learn=on)

## Panel de créditos de IA

El panel Créditos de IA muestra cómo el uso de [!DNL Experience Platform Agents] por parte de su organización se traduce en consumo de créditos de IA.

### Métricas en el panel Créditos de IA

* **Créditos de IA totales consumidos:** Uso general del agente en créditos de IA.
* **Tendencias diarias y mensuales:** picos, caídas y cambios en los patrones de consumo.
* **Créditos de inteligencia artificial restantes:** Saldo restante para que pueda planificar de forma proactiva y evitar cargos adicionales.

[Ver vídeo](https://video.tv.adobe.com/v/3491867?learn=on)

## Más ayuda sobre este tema

* [Panel de uso de licencias](https://experienceleague.adobe.com/en/docs/experience-platform/dashboards/guides/license-usage) en [!DNL Experience Platform]
* [Inteligencia artificial aplicada a la agencia en Adobe CX Enterprise](agentic-ai.md)
* [Trabajos del agente y consumo de crédito de IA](ai-credit-consumption.md)
* [Panel de uso de licencias](https://experienceleague.adobe.com/en/docs/experience-platform/dashboards/guides/license-usage) (Experience Platform)
