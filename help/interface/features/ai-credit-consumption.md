---
title: Trabajos de agente y consumo de crédito de IA
description: Obtenga información acerca de los trabajos del agente y las tasas de consumo de crédito de IA en las aplicaciones de Experience Cloud.
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: d9d9eb0b3bad1abd517e4c6b0bd5ecaa45a7930d
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 4%

---

# Trabajos de agente de Adobe Experience Platform y consumo de créditos de IA

Actualización: **miércoles, 03 de marzo de 2026**

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
| ------ | ----- | ------------------------ | ----------------------- | ----------------- |
| Audience Agent | Audiencia/ideación de cuenta | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li>_Mostrarme campos para compradores adinerados_</li><li>_Buscar todos los campos relacionados con las preferencias del cliente_</li></ul> |
| Audience Agent | Creación de cuentas/audiencias basada en el conocimiento | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 150 | <ul><li>_Crear una audiencia compuesta por personas que viven en California_</li><li>_Genera una audiencia de miembros de VIP que gastaron más de $1000 este trimestre_</li><li>_Crea una audiencia de usuarios que compraron artículos de ropa pero que no compraron en los últimos 60 días_</li></ul> |
| Audience Agent | Administración de audiencias y cuentas | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>_¿Tengo audiencias duplicadas?_</li><li>_Mostrarme las 5 audiencias más grandes._</li><li>_Mostrar audiencias que no están activadas en ningún destino_</li><li>_Enumerar todas las audiencias utilizadas en recorridos activos_</li></ul> |
| Audience Agent | Análisis de audiencia/cuenta | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>_¿Qué audiencias aumentaron en tamaño en más de un 20% en la última semana?_</li><li>_¿Cuánto ha cambiado la audiencia &quot;Platino fiel&quot; en comparación con el valor de hace 30 días?_</li><li>_¿Cuál es mi audiencia que crece más rápido?_</li></ul> |
| Audience Agent | Ideación de grupo de compra | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>_¿Qué cuentas muestran intención para estos productos?_</li><li>_Mostrarme las personas principales por intención de producto para XYZ._</li><li>_¿Qué grupos compradores tienen más de 5 miembros?_</li></ul> |
| Data Insights Agent | Análisis y visualización de datos | <ul><li>Customer Journey Analytics (Ediciones B2C y B2B)</li></ul> | 25 | <ul><li>_Tendencia de pedidos en julio_</li><li>_Mostrar ingresos por región._</li><li>_Mostrar pedidos por sexo, de marzo a junio._</li><li>_Cuáles fueron mis 10 SKU principales por beneficio en junio_</li><li>_Proporción de compras por mes del año_</li><li>_Porcentaje de ingresos por categoría de producto_</li></ul> |
| Journey Agent | ideación de recorrido | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>_Cree un recorrido para cuentas de espacio en blanco con intención de usar mi solución, centrándose en las personas que participan con contenido en el sitio web_</li></ul> |
| Journey Agent | creación de recorridos | <ul><li>Adobe Journey Optimizer (Ediciones B2B y B2C)</li></ul> | 30 | <ul><li>_Genere un recorrido para enviar un recordatorio a los usuarios que no hayan completado su primera compra en los últimos 7 días_</li><li>_Cuando los usuarios completen su primera compra, envíenos una confirmación por SMS y una explicación de los beneficios de seguimiento por correo electrónico pasados 3 días_</li></ul> |
| Journey Agent | análisis de recorrido | <ul><li>Adobe Journey Optimizer (Ediciones B2B y B2C)</li></ul> | 50 | <ul><li>_Quiero analizar las visitas en el orden previsto por nodo para la campaña del 4 de julio de recorrido._</li><li>_Hay algún conflicto de programación para el recorrido X_</li><li>_Mostrarme conflictos de superposición de audiencia para el recorrido X_</li></ul> |
| Journey Agent | administración de recorrido | <ul><li>Adobe Journey Optimizer (Ediciones B2B y B2C)</li></ul> | 25 | <ul><li>_¿Cuántos recorridos activos tengo?_</li><li>_Enumerar todos los recorridos con la audiencia X._</li><li>_Enumerar todos los recorridos que se encuentran actualmente en modo de prueba_</li></ul> |
| Agente de soporte del producto | Solución de problemas basada en conocimientos | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (Ediciones B2C y B2B)</li><li>Customer Journey Analytics (Ediciones B2C y B2B)</li></ul> | 0 | <ul><li>_¿Por qué difiere el recuento de perfiles en el Tablero de uso de licencias y en la página de inicio de Experience Platform?_</li><li>_¿Cuáles son las razones por las que no se activa un recorrido?_</li><li>_¿Cómo crea Adobe Experience Platform experiencias en tiempo real?_</li><li>_¿Cómo se configuran y utilizan las alertas en Adobe Experience Platform?_</li><li>_¿Cuál es el límite promedio de riqueza de perfiles en Adobe Experience Platform Activation?_</li></ul> |
| Agente de soporte del producto | Creación y seguimiento de casos de soporte | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li>Adobe Journey Optimizer (Ediciones B2C y B2B)<li>Customer Journey Analytics (Ediciones B2C y B2B)</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li>_Crear un nuevo ticket de soporte para mi trabajo de segmentación con errores_</li><li>_¿Cuál es el estado del ticket E-001772068?_</li></ul> |
| Agente del Asesor de contenido | Detección de contenido | <ul><li>Adobe Experience Manager Assets</li></ul> | 5 | <ul><li>_Mostrar fragmentos de contenido para crear la campaña de ofertas WKND._</li><li>_Buscar imágenes PNG para empaquetar productos._</li><li>_Mostrar imágenes etiquetadas de Office en la carpeta WKND._</li><li>_¿Hay algún svg en la carpeta WKND?_</li><li>_Mostrarme todos los formularios de solicitud de préstamo._</li><li>_Busco formularios de incorporación de empleados._</li></ul> |
| Agente del Asesor de contenido | <ul><li>Optimización de contenido</li></ul> | <ul><li>Adobe Experience Manager Assets</li></ul> | 10 | <ul><li>_Cree una representación de 2000 px como JPEG con una calidad del 80 %._</li><li>_Crear una representación para una historia de Instagram._</li><li>_Superponga la imagen con gráficos con un descuento del 30% sobre el titular promocional, situándola a 100 píxeles del centro._</li><li>_Cambiar el color de fondo del PNG a #ff8932._</li></ul> |
| Agente de control de marca | <ul><li>Actualización de contenido</li><li>Creación de Forms</li><li>Solución de problemas de canalización</li></ul> | <ul><li>Adobe Experience Manager Cloud Services</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li>_Solucionar problemas de mi canalización con errores_</li><li>_Enumerar mis canalizaciones con errores para el programa principal._</li><li>_Analizar mi canalización con error llamada &quot;Canalización de desarrollo&quot;._</li><li>_Solucionar problemas de ejecución de canalización 1234567_</li></ul> |
| Brand Experience Agent | Modernización del sitio | Adobe Experience Manager Cloud Services | 100 | <ul><li>_Migrar la página`https://wknd-trendsetters.site`_</li></ul> |

>[!NOTE]
>
>El consumo real de crédito de IA puede variar según el número de pasos ejecutados y las iteraciones por paso.

## Más ayuda sobre este tema

* [Inteligencia artificial aplicada a la agencia en Experience Cloud](/help/interface/features/agentic-ai.md)
* [Prueba enlazada a uso de agentes de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)
