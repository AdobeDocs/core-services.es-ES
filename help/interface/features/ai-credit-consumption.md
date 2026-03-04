---
title: Trabajos de agente y consumo de crédito de IA
description: Obtenga información acerca de los trabajos del agente y las tasas de consumo de crédito de IA en las aplicaciones de Experience Cloud.
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: ae927640b65458cb1c0df1a817207220f7dfe0ec
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 4%

---

# Trabajos de agente de Adobe Experience Platform y consumo de créditos de IA

Actualización: **jueves, 04 de marzo de 2026**

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
| Audience Agent | Audiencia/ideación de cuenta | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li><em>Mostrarme campos para compradores adinerados</em></li><li><em>Buscar todos los campos relacionados con las preferencias del cliente</em></li></ul> |
| Audience Agent | Creación de cuentas/audiencias basada en el conocimiento | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 150 | <ul><li><em>Crear una audiencia compuesta por personas que viven en California</em></li><li><em>Genera una audiencia de miembros de VIP que gastaron más de $1000 este trimestre</em></li><li><em>Crea una audiencia de usuarios que compraron artículos de ropa pero que no compraron en los últimos 60 días</em></li></ul> |
| Audience Agent | Administración de audiencias y cuentas | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li><em>¿Tengo audiencias duplicadas?</em></li><li><em>Mostrarme las 5 audiencias más grandes.</em></li><li><em>Mostrar audiencias que no están activadas en ningún destino</em></li><li><em>Enumerar todas las audiencias utilizadas en recorridos activos</em></li></ul> |
| Audience Agent | Análisis de audiencia/cuenta | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li><em>¿Qué audiencias aumentaron en tamaño en más de un 20% en la última semana?</em></li><li><em>¿Cuánto ha cambiado la audiencia &quot;Platino fiel&quot; en comparación con el valor de hace 30 días?</em></li><li><em>¿Cuál es mi audiencia que crece más rápido?</em></li></ul> |
| Audience Agent | Ideación de grupo de compra | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li><em>¿Qué cuentas muestran intención para estos productos?</em></li><li><em>Mostrarme las personas principales por intención de producto para XYZ.</em></li><li><em>¿Qué grupos compradores tienen más de 5 miembros?</em></li></ul> |
| Data Insights Agent | Análisis y visualización de datos | <ul><li>Customer Journey Analytics (Ediciones B2C y B2B)</li></ul> | 25 | <ul><li><em>Tendencia de pedidos en julio</em></li><li><em>Mostrar ingresos por región.</em></li><li><em>Mostrar pedidos por sexo, de marzo a junio.</em></li><li><em>Cuáles fueron mis 10 SKU principales por beneficio en junio</em></li><li><em>Proporción de compras por mes del año</em></li><li><em>Porcentaje de ingresos por categoría de producto</em></li></ul> |
| Journey Agent | ideación de recorrido | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li><em>Cree un recorrido para cuentas de espacio en blanco con intención de usar mi solución, centrándose en las personas que participan con contenido en el sitio web</em></li></ul> |
| Journey Agent | creación de recorridos | <ul><li>Adobe Journey Optimizer (Ediciones B2B y B2C)</li></ul> | 30 | <ul><li><em>Genere un recorrido para enviar un recordatorio a los usuarios que no hayan completado su primera compra en los últimos 7 días</em></li><li><em>Cuando los usuarios completen su primera compra, envíenos una confirmación por SMS y una explicación de los beneficios de seguimiento por correo electrónico pasados 3 días</em></li></ul> |
| Journey Agent | análisis de recorrido | <ul><li>Adobe Journey Optimizer (Ediciones B2B y B2C)</li></ul> | 50 | <ul><li><em>Quiero analizar las visitas en el orden previsto por nodo para la campaña del 4 de julio de recorrido.</em></li><li><em>Hay algún conflicto de programación para el recorrido X</em></li><li><em>Mostrarme conflictos de superposición de audiencia para el recorrido X</em></li></ul> |
| Journey Agent | administración de recorrido | <ul><li>Adobe Journey Optimizer (Ediciones B2B y B2C)</li></ul> | 25 | <ul><li><em>¿Cuántos recorridos activos tengo?</em></li><li><em>Enumerar todos los recorridos con la audiencia X.</em></li><li><em>Enumerar todos los recorridos que se encuentran actualmente en modo de prueba</em></li></ul> |
| Agente de soporte del producto | Solución de problemas basada en conocimientos | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li><li>Adobe Journey Optimizer (Ediciones B2C y B2B)</li><li>Customer Journey Analytics (Ediciones B2C y B2B)</li></ul> | 0 | <ul><li><em>¿Por qué difiere el recuento de perfiles en el Tablero de uso de licencias y en la página de inicio de Experience Platform?</em></li><li><em>¿Cuáles son las razones por las que no se activa un recorrido?</em></li><li><em>¿Cómo crea Adobe Experience Platform experiencias en tiempo real?</em></li><li><em>¿Cómo se configuran y utilizan las alertas en Adobe Experience Platform?</em></li><li><em>¿Cuál es el límite promedio de riqueza de perfiles en Adobe Experience Platform Activation?</em></li></ul> |
| Agente de soporte del producto | Creación y seguimiento de casos de soporte | <ul><li>Real-Time CDP (Ediciones B2B, B2C y B2P)</li>Adobe Journey Optimizer (Ediciones B2C y B2B)<li>Customer Journey Analytics (Ediciones B2C y B2B)</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li><em>Crear un nuevo ticket de soporte para mi trabajo de segmentación con errores</em></li><li><em>¿Cuál es el estado del ticket E-001772068?</em></li></ul> |
| Agente del Asesor de contenido | Detección de contenido | <ul><li>Adobe Experience Manager</li></ul> | 5 | <ul><li><em>Mostrar fragmentos de contenido para crear la campaña de ofertas WKND.</em></li><li><em>Buscar imágenes PNG para empaquetar productos.</em></li><li><em>Mostrar imágenes etiquetadas de Office en la carpeta WKND.</em></li><li><em>¿Hay algún svg en la carpeta WKND?</em></li><li><em>Mostrarme todos los formularios de solicitud de préstamo.</em></li><li><em>Busco formularios de incorporación de empleados.</em></li></ul> |
| Agente del Asesor de contenido | <ul><li>Optimización de contenido</li></ul> | <ul><li>Adobe Experience Manager Assets y Dynamic Media</li></ul> | 10 | <ul><li><em>Cree una representación de 2000 px como JPEG con una calidad del 80 %.</em></li><li><em>Crear una representación para una historia de Instagram.</em></li><li><em>Superponga la imagen con gráficos con un descuento del 30% sobre el titular promocional, situándola a 100 píxeles del centro.</em></li><li><em>Cambiar el color de fondo del PNG a #ff8932.</em></li></ul> |
| Agente de control de marca | <ul><li>Comprobaciones de directivas de marca</li></ul><ul><li>Permisos con Content Hub</li></ul><ul><li>Solución de problemas de canalización</li></ul> | <ul><li>Adobe Experience Manager Sites (Políticas de marca)</li></ul><ul><li>Adobe Experience Manager Assets</li></ul> | 25 | <ul><li><em>¿Esta página está alineada con mi marca? `https://www.website/en.html`</em></li><li><em>Mostrar todas las reglas ABAC de Content Hub existentes</em></li><li><em>¿Alguno de mis recursos caducará pronto?</em></li></ul> |
| Brand Experience Agent | <ul><li>Actualización de contenido</li><li>Creación de Forms</li><li>Solución de problemas de canalización</li></ul> | <ul><li>Adobe Experience Manager Cloud Services</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li><em>Crear un formulario de contacto con campos de nombre, correo electrónico y mensaje</em></li><li><em>Solucionar problemas de mi canalización con errores</em></li><li><em>Enumerar mis canalizaciones con errores para el programa principal.</em></li></ul> |

>[!NOTE]
>
>El consumo real de crédito de IA puede variar según el número de pasos ejecutados y las iteraciones por paso.

## Más ayuda sobre este tema

* [GenAI en Experience Cloud](/help/interface/features/generative-ai.md)
* [Inteligencia artificial aplicada a la agencia en Experience Cloud](/help/interface/features/agentic-ai.md)
* [Prueba enlazada a uso de agentes de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)
