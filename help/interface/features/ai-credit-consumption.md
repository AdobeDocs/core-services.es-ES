---
title: Trabajos de agente y consumo de crédito de IA
description: Obtenga información acerca de los trabajos del agente y las tasas de consumo de crédito de IA en las aplicaciones de Experience Cloud.
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: bb6adf13bed37d4a885b5baec28199efade592e1
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 3%

---

# Trabajos de agente de Adobe Experience Platform y consumo de créditos de IA

Obtenga información acerca de los trabajos de IA auténticos y el consumo de crédito de IA en aplicaciones de Experience Cloud. Para obtener información sobre cómo habilitar las capacidades de IA agéntica en aplicaciones de Experience Cloud existentes, consulte [IA agéntica en Experience Cloud](agentic-ai.md#existing-apps).

## Trabajos del agente

Un _trabajo de agente_ es una serie de tareas y acciones que ejecuta un agente para lograr un resultado específico, según lo indicado por las entradas del cliente.

Con las indicaciones en lenguaje natural a través del asistente de IA, puede pedir a los agentes que realicen trabajos específicos. En función de estas entradas, Agent Orchestrator coordina los agentes adecuados para ejecutar cada paso dentro de las aplicaciones de Experience Cloud relevantes.

## Créditos de IA

Un _crédito de IA_ es una métrica basada en el uso que cuantifica la ejecución de trabajos del agente. Los créditos de IA no se aplican a [aplicaciones con prioridad de IA](/help/interface/features/agentic-ai.md).

## Consumo de crédito de IA

El uso del crédito de IA puede variar según la complejidad y el valor del trabajo ejecutado:

* Las tareas sencillas (a menudo de un solo paso) consumen menos créditos
* Las tareas complejas (a menudo de varios pasos) consumen más créditos
* Las tareas que implican razonamiento avanzado, validación, coordinación de varios agentes o integración consumen más créditos

### Tasas estimadas de consumo de crédito de IA

| Agente | Trabajo | Aplicaciones compatibles | Créditos estimados de IA | Ejemplos de peticiones de datos |
| ------ |-----|------------------------|----------------------|----------------|
| Audience Agent | Audiencia/ideación de cuenta | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li>Mostrar campos para compradores adinerados</li><li>Buscar todos los campos relacionados con las preferencias del cliente</li></ul> |
| Audience Agent | Creación de cuentas/audiencias basada en el conocimiento | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 150 | <ul><li>Cree una audiencia compuesta por personas que viven en California</li><li>Genere una audiencia de miembros de VIP que gastaron más de 1000 dólares este trimestre</li><li>Crear una audiencia de usuarios que compraron artículos de ropa pero que no han realizado una compra en los últimos 60 días</li></ul> |
| Audience Agent | Administración de audiencias y cuentas | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>¿Tengo audiencias duplicadas?</li><li>Muéstrame mis 5 audiencias más grandes.</li><li>Mostrar las audiencias que no están activadas en ningún destino</li><li>Enumerar todas las audiencias utilizadas en recorridos en directo</li></ul> |
| Audience Agent | Análisis de audiencia/cuenta | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>¿Qué audiencias han aumentado en más de un 20 % en la última semana?</li><li>¿Cuánto ha cambiado la audiencia &quot;Platino fiel&quot; en comparación con el valor de hace 30 días?</li><li>¿Cuál es mi audiencia que crece más rápido?</li></ul> |
| Audience Agent | Ideación de grupo de compra | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>¿Qué cuentas muestran intención para estos productos?</li><li>Mostrar las personas principales por intención de producto para XYZ.</li><li>¿Qué grupos compradores tienen más de 5 miembros?</li></ul> |
| Data Insights Agent | Análisis y visualización de datos | <ul><li>Customer Journey Analytics (Ediciones B2C y B2B)</li></ul> | 25 | <ul><li>Tendencia de pedidos en julio</li><li>Mostrar ingresos por región.</li><li>Mostrar pedidos por género, de marzo a junio.</li><li>Cuáles fueron mis 10 SKU principales por beneficio en junio</li><li>Proporción de compras por mes del año</li><li>Porcentaje de ingresos por categoría de producto</li></ul> |
| Journey Agent | ideación de recorrido | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>Cree un recorrido para cuentas de espacio en blanco con la intención de mi solución, centrado en las personas que participan con contenido en el sitio web</li></ul> |
| Journey Agent | creación de recorridos | <ul><li>Adobe Journey Optimizer (Ediciones B2B y B2C)</li></ul> | 30 | <ul><li>Genere un recorrido para enviar un recordatorio a los usuarios que no hayan completado su primera compra en los últimos 7 días</li><li>Cuando los usuarios completen su primera compra, envíen una confirmación por SMS y una explicación de los beneficios de seguimiento por correo electrónico pasados 3 días</li></ul> |
| Journey Agent | análisis de recorrido | <ul><li>Adobe Journey Optimizer (Ediciones B2B y B2C)</li></ul> | 50 | <ul><li>Quiero analizar las visitas en el orden previsto por nodo para la campaña del 4 de julio de recorrido.</li><li>¿Hay algún conflicto de programación para el recorrido X?</li><li>Mostrar conflictos de superposición de audiencias para el recorrido X</li></ul> |
| Journey Agent | administración de recorrido | <ul><li>Adobe Journey Optimizer (Ediciones B2B y B2C)</li></ul> | 25 | <ul><li>¿Cuántos recorridos en vivo tengo?</li><li>Enumere todos los recorridos con la audiencia X.</li><li>Mostrar todos los recorridos que se encuentran actualmente en modo de prueba</li></ul> |
| Agente de soporte del producto | Solución de problemas basada en conocimientos | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (Ediciones B2C y B2B)</li><li>Customer Journey Analytics (Ediciones B2C y B2B)</li></ul> | 0 | <ul><li>¿Por qué difiere el recuento de perfiles en el Tablero de uso de licencias y en la página de inicio de Experience Platform?</li><li>¿Cuáles son las razones por las que un recorrido no se activa?</li><li>¿Cómo crea Adobe Experience Platform experiencias en tiempo real?</li><li>¿Cómo se configuran y utilizan las alertas en Adobe Experience Platform?</li><li>¿Cuál es el límite promedio de riqueza de perfiles en Adobe Experience Platform Activation?</li></ul> |
| Agente de soporte del producto | Creación y seguimiento de casos de soporte | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li>Adobe Journey Optimizer (Ediciones B2C y B2B)<li>Customer Journey Analytics (Ediciones B2C y B2B)</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li>Crear un nuevo ticket de asistencia para mi trabajo de segmentación con errores</li><li>¿Cuál es el estado del billete E-001772068?</li></ul> |
| Agente del Asesor de contenido | Detección de contenido | <ul><li>Adobe Experience Manager Cloud Services</li></ul> | 5 | <ul><li>Mostrar fragmentos de contenido para crear una campaña de ofertas WKND.</li><li>Busque imágenes PNG de empaquetado de productos.</li><li>Mostrar imágenes etiquetadas como office en la carpeta WKND.</li><li>¿Hay algún svg en la carpeta WKND?</li><li>Mostrar todos los formularios de solicitud de préstamo.</li><li>Estoy buscando formularios de incorporación de empleados.</li></ul> |
| Agente del Asesor de contenido | <ul><li>Actualización de contenido</li><li>Optimización de contenido</li><li>Creación de Forms</li></ul> | <ul><li>Adobe Experience Manager Cloud Services</li></ul> | 10 | <ul><li>Cree una representación de 2000 px como JPEG con una calidad del 80 %.</li><li>Crear una representación para una historia de Instagram.</li><li>Superponga la imagen con gráficos de descuento del 30% sobre el banner promocional, colocándolo a 100 px del centro.</li><li>Cambie el color de fondo del PNG a #ff8932.</li></ul> |
| Brand Experience Agent | <ul><li>Asistencia de Experience</li><li>Compatibilidad de implementación</li></ul> | <ul><li>Adobe Experience Manager Cloud Services</li></ul> | 5 | <ul><li>Solucionar problemas de canalización con errores</li><li>Enumerar mis canalizaciones con errores para el programa principal.</li><li>Analizar mi canalización fallida llamada &quot;Canalización de desarrollo&quot;.</li><li>Solucionar problemas de ejecución de 1234567</li></ul> |
| Brand Experience Agent | Modernización del sitio | Adobe Experience Manager Cloud Services | 100 | <ul><li>Migre la página https://wknd-trendsetters.site</li></ul> |

>[!NOTE]
>
>El consumo real de crédito de IA puede variar según el número de pasos ejecutados y las iteraciones por paso.

## Más ayuda sobre este tema

* [Inteligencia artificial aplicada a la agencia en Experience Cloud](/help/interface/features/agentic-ai.md)
* [Prueba enlazada a uso de agentes de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)