# Bitácora — Clase 22

**Proyecto:** Agencia de Diseño Gráfico y Comunicación Visual  
**Estudiante:** Loreto Calderón

## Objetivo de la clase

Personalizar los ejercicios de IA con el proyecto que venimos desarrollando en el Diplomado, evitando ejemplos genéricos y trabajando directamente con problemas reales de coordinación de una agencia creativa.

## Caso elegido

La agencia recibe briefs, correos, mensajes y solicitudes de cambio que deben pasar por Comercial, Coordinación de Proyectos, Dirección Creativa y Diseño. Cuando la información llega incompleta o queda dispersa, aparecen retrasos, correcciones y reprocesos.

## Ejercicio 1 — Palabras y relaciones semánticas

Palabras utilizadas:

- brief
- cliente
- diseño
- cambio
- aprobación
- plazo
- producción
- requerimiento
- prioridad
- corrección

La idea fue observar que conceptos que en una agencia están relacionados también deberían aparecer cercanos para un modelo semántico. Por ejemplo, `brief` debería relacionarse con `requerimiento`, mientras que `cambio` debería asociarse con `corrección`, `aprobación` y `plazo`.

## Ejercicio 2 — Clasificación de mensajes

Se plantearon mensajes típicos del flujo de trabajo:

- “El cliente aprobó el diseño final.” → **aprobación**
- “Necesitamos cambiar el color y el tamaño del logo antes de imprimir.” → **solicitud de cambio**
- “Falta confirmar la medida final y el material.” → **información faltante**
- “La entrega debe estar lista mañana antes de las 12:00.” → **urgente**
- “Gracias, quedó perfecto.” → **sin acción requerida**

Este ejercicio muestra una posible función analítica del asistente: detectar qué mensajes requieren seguimiento y cuáles son solamente informativos.

## Ejercicio 3 — Generación de resumen

Prompt usado como caso del proyecto:

> Resume el siguiente brief de un cliente de una agencia de diseño. Separa objetivo, piezas solicitadas, requisitos obligatorios, información faltante, plazo y cambios pendientes. No inventes información. Si algo no aparece, márcalo como “por confirmar”.

### Aprendizaje

Un resumen puede reducir carga de lectura, pero también puede generar exceso de confianza. Por eso el sistema debe mantener visible el texto original y diferenciar claramente entre hechos, inferencias y recomendaciones.

## Ejercicio 4 — Comparación analítico vs. generativo

### Modelo analítico

Puede clasificar mensajes, detectar urgencia, extraer fechas, identificar responsables o comprobar campos faltantes.

### Modelo generativo

Puede resumir briefs, redactar minutas, preparar reportes de avance o convertir conversaciones extensas en información estructurada.

### Decisión para el proyecto

El asistente necesita ambos enfoques. Primero debe **detectar y estructurar** información; después puede **generar** resúmenes y borradores útiles para el equipo.

## Modelos candidatos

1. **Gemini Flash** para clasificación rápida, extracción y tareas repetitivas.
2. **Gemini Pro** para análisis de contexto más largo, briefs complejos y generación de síntesis.
3. **Google AI Studio** como entorno de prototipado para probar instrucciones, formato de salida y comportamiento.

## Riesgos detectados

- Confundir una recomendación con una instrucción aprobada.
- Omitir una excepción importante al resumir.
- Priorizar mal una alerta.
- Tomar un mensaje ambiguo como cambio confirmado.
- Automatizar una decisión que debería validar una persona.

## Criterio de diseño

La IA debe ayudar a que el equipo vea mejor la información, no a reemplazar la decisión creativa. Las acciones sensibles deben incluir fuente, contexto, aprobación humana y posibilidad de corregir.

## Reflexión personal

Esta clase me ayudó a entender que los ejercicios técnicos tienen más sentido cuando se conectan con un problema real del proyecto. En nuestro caso, la IA puede aportar mucho en ordenar y revisar información, pero el valor creativo y las decisiones con clientes siguen dependiendo del equipo humano.
