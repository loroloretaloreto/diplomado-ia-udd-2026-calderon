# Hallazgos NotebookLM — Clase 24

**Proyecto:** Agencia de Diseño Gráfico y Comunicación Visual  
**Estudiante:** Loreto Calderón

## Hallazgo 1 — El problema principal no es creativo, sino de información y coordinación

Las fuentes muestran que muchos errores y reprocesos aparecen por briefs incompletos, cambios que no quedan registrados, información distribuida entre distintos canales y pérdida de contexto entre Comercial, Coordinación de Proyectos, Dirección Creativa y Diseño.

**Implicancia para el proyecto:** el asistente IA debe priorizar orden, trazabilidad y revisión de información antes que intentar “diseñar por el equipo”.

## Hallazgo 2 — La IA aporta más valor como asistente de gestión que como sustituto creativo

Las tareas más adecuadas para automatizar son revisar completitud, resumir requerimientos, detectar faltantes, comparar versiones, clasificar mensajes, generar alertas y preparar reportes. La evaluación estética, la negociación con clientes y la aprobación de cambios importantes deben mantenerse en manos humanas.

**Implicancia:** el sistema debe diseñarse como una capa de apoyo al flujo creativo, no como un agente que toma decisiones creativas finales.

## Hallazgo 3 — Un resumen útil también puede generar sesgo de automatización

Cuando una IA resume un brief, prioriza una alerta o interpreta un cambio, ya está influyendo en la decisión del usuario. Si la interfaz presenta una respuesta con demasiada seguridad, el equipo puede aceptar una síntesis incompleta como si fuera la verdad del proyecto.

**Implicancia:** cada salida importante debe mostrar fuente, nivel de certeza y posibilidad de volver al material original.

## Hallazgo 4 — Coordinación de Proyectos y Dirección Creativa son los usuarios clave

El Coordinador de Proyectos necesita ordenar tareas, plazos, solicitudes y cambios. El Director Creativo necesita mantener coherencia entre el brief vigente y el trabajo desarrollado. El Diseñador Gráfico se beneficia indirectamente al recibir instrucciones más claras y menos contradictorias.

**Implicancia:** el prototipo debe priorizar las necesidades de estos dos roles y no tratar a toda la agencia como si tuviera el mismo flujo de trabajo.

## Hallazgo 5 — La adopción depende tanto de la organización como de la tecnología

No basta con elegir un buen modelo de IA. La agencia necesita información utilizable, procesos claros, seguridad de datos, apoyo organizacional, capacitación y reglas de supervisión humana. Los marcos TOE y DOI ayudan a evaluar si la solución realmente puede incorporarse de forma responsable.

**Implicancia:** antes de escalar el asistente, se debe validar preparación tecnológica, organizacional y humana.

## Síntesis general

La oportunidad principal del proyecto está en **reducir carga operativa sin reducir agencia humana**. Una buena implementación no es la que automatiza más, sino la que vuelve visible la información correcta, mantiene trazabilidad y deja las decisiones sensibles bajo control de las personas.

## Decisiones de diseño derivadas

- Fuente original siempre disponible.
- Cambios de alcance requieren aprobación humana.
- Alertas explicables y reordenables.
- Recomendaciones etiquetadas como recomendaciones.
- Historial de versiones y responsables.
- Posibilidad de corregir, rechazar y deshacer.
- No inferir emociones o intenciones sin evidencia.
- Medir éxito por reducción de reprocesos y errores, no solo por velocidad.
