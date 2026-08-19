# Bitácora — Clase 22

**Proyecto:** Manorigen IA — rotulación vehicular  
**Estudiante:** Loreto Calderón

## Ejercicio de embeddings

Para el ejercicio se eligieron palabras del proceso real de rotulación:

`rotulacion`, `vinilo`, `impresion`, `corte`, `instalacion`, `vehiculo`, `branding`, `logotipo`, `color`, `composicion`, `medidas`, `cliente`.

### ¿Qué me interesa observar?

Me interesa ver si el modelo acerca los conceptos técnicos —por ejemplo, **vinilo, corte, instalación y medidas**— a los conceptos visuales —**branding, logotipo, color y composición**—. En la práctica todos forman parte del mismo proyecto, pero para un modelo pueden aparecer como grupos distintos.

### ¿Qué combinación podría resultar extraña?

Puede ocurrir que el modelo acerque “vinilo” a “branding” más de lo que acerca “vinilo” a “instalación”, porque fue entrenado con usos del lenguaje más amplios que el contexto específico de Manorigen. Esto demuestra que una similitud matemática no equivale a una verdad del proyecto.

## Modelo analítico vs. generativo

### Frases probadas en clasificación

1. “La propuesta se ve moderna y respeta muy bien la identidad de la marca.”
2. “El diseño se corta justo en la tapa de combustible y así no se puede instalar.”
3. “La propuesta está bien, pero todavía falta revisar las medidas del portalón.”
4. “El cliente aprobó el concepto general, aunque pidió agrandar el logo lateral.”
5. “La información llegó incompleta y tuvimos que rehacer parte del montaje.”

### Observación

El modelo analítico entrega una etiqueta concreta para cada frase. Es útil para **ordenar feedback**, detectar mensajes problemáticos o clasificar observaciones. El modelo generativo, en cambio, produce texto nuevo y cambia entre ejecuciones; puede ayudar a explorar soluciones, pero exige más revisión.

## Prompt generativo usado

> En un proyecto de rotulación vehicular de Manorigen, una propuesta de diseño debe equilibrar identidad visual, legibilidad, medidas reales del vehículo, zonas que no pueden cubrirse y facilidad de instalación. Una buena asistencia de IA debería...

### Reflexión

La parte más interesante fue entender que el sistema no “ve” el proyecto como una diseñadora o instalador. Convierte palabras y textos en representaciones matemáticas y busca patrones. Eso puede acelerar tareas, pero no reemplaza el conocimiento sobre materiales, cortes, molduras, tapas, puertas, proporciones o lectura visual.

## Tres modelos de Hugging Face que llamaron mi atención

1. **sentence-transformers/all-MiniLM-L6-v2** — porque convierte texto en embeddings y permite comparar conceptos o documentos.
2. **nlptown/bert-base-multilingual-uncased-sentiment** — porque puede clasificar el tono de comentarios en español y sirve como ejemplo de modelo analítico.
3. **stabilityai/stable-diffusion-xl-base-1.0** — porque representa el lado generativo visual y permite pensar cómo la IA puede apoyar exploración de estilos y composición.

## Pregunta de cierre

Lo más importante para mí es distinguir entre **usar una IA para explorar** y **delegarle una decisión**. En diseño, una respuesta plausible puede ser útil como punto de partida, pero sigue necesitando criterio profesional y verificación técnica.
